---
title: Linux系统下解压文件报错：invalid compressed data -- format violated
date: 2021-03-13 10:00:00
categories: DataScience
tags:
  - Linux
  - docker
---

**1. 问题描述：解压文件报错，具体如下：**

   1.1 下载人类参考基因组：

   nohup wget ftp://ftp.ensembl.org/pub/release-102/fasta/homo_sapiens/dna/Homo_sapiens.GRCh38.dna.toplevel.fa.gz &

   1.2 解压文件，报错，如图所示

![image-20210209092540712](/Users/sophia/Library/Application Support/typora-user-images/image-20210209092540712.png)

**2. 解决问题方案：**

   2.1 直接IDM下载

   2.2 在传输之前，使用命令ftp> bin指定传输格式，可以解决此问题

**3. 问题分析：**

   传输文件的时候是默认按照netascii的格式进行传输的，没有按照二进制文件的形式传输

   FTP中传输模式：BIN与ASC

   ASCII 和BINARY模式区别：

   用HTML 和文本编写的文件必须用ASCII模式上传，用BINARY模式上传会破坏文件，导致文件执行出错。

   BINARY模式用来传送可执行文件，压缩文件，和图片文件。

   如果你用ASCII模式传，会显示一堆乱码，你必须重新用BINARY模式传。