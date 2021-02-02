---
title: Linux系统下,四步解决sudo执行权限问题解决
date: 2021-01-28 18:53:58
categories:DataScience
tags:Linux,sudo
---

** 1. 切换到root用户： 

执行命令：su - 

输入root用户password

** 2. 添加sudo文件写权限：

chmod u+w /etc/sudoers

** 3. 编辑sudoers file

vi /etc/sudoers
find： root ALL=(ALL) ALL

下一行，添加“ *your user name* ”ALL=(ALL) ALL

** 4. 撤销sudoers文件写权限

chmod u-w /etc/sudoers

*** ok！***