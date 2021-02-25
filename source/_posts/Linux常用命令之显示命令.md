---
title: Linux常用命令之显示命令：
categories: DataScience
tags:
  - Linux
date: 2021-02-25  23:00:00
---

**cat：**

查看文件的内容

​      显示和连接一个或者多个文件至标准输出

​      cat file1 ...



**more：**

逐页显示文件内容



**less：**

逐页显示文件内容



**head：**

​           -n num 显示文件前num行

​           -c num 显示文件前num个字符

​           缺省时默认显示前10行



**tail：**

​          -n num 显示文件后num行

​          -c num 显示文件后num个字符

​          缺省时默认显示后10行



**sort：**

对文件排序（首字符向后，依次按ASCII码值进行比较，升序输出）

用法：sort [参数] file

​            -r：降序输出

​            -n：以数值来排序

​            -o：输出到新文件



**uniq：**

比较相邻的行，显示不重复的行

​           -i ：忽略大小写

​           -c ：计数



