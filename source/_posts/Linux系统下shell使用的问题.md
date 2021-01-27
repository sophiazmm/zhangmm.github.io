---
title: linux下shell中使用上下键翻出^[[A^[[A^[[A^[[B^[[B问题解决
categories: DataScience
tags:
  - Linux
  - shell
date: 2021-01-27 23:00:00
---
# linux下shell中使用上下键翻出历史命名时出现^[[A^[[A^[[A^[[B^[[B

step1：echo $SHELL

step2：sudo chsh -s /bin/bash username

# 常见Shell介绍

Shell 是一种脚本编程语言，也是一个连接内核和用户的软件。在 Linux 发展早期，唯一能用的工具是 Shell，Linux 用户都是在 Shell 中输入文本命令，并查看文本输出。常见的 Shell 有 sh、bash、csh、tcsh、ash 等。

## **sh**

sh 的全称是 Bourne shell，由 AT&T 公司的 Steve Bourne开发。

sh 是 UNIX 上的标准 shell，很多 UNIX 版本都配有 sh， 是第一个流行的 Shell。

## **csh**

sh 之后另一个广为流传的 shell 是由柏克莱大学的 Bill Joy 设计的，这个 shell 的语法有点类似C语言，所以才得名为 C shell ，简称为 csh。

BSD 是 UNIX 的一个重要分支，后人在此基础上发展出了很多现代的操作系统，最著名的有 FreeBSD、OpenBSD 和 NetBSD。

## **tcsh**

tcsh 是 csh 的增强版，加入了命令补全功能，提供了更加强大的语法支持。

## **ash**

一个简单轻量级 Shell，占用资源少，适合运行于低内存环境。

## **bash**

bash shell 是 Linux 的默认 shell。

bash 由 GNU 组织开发，保持了对 sh shell 的兼容性，是各种 Linux 发行版默认配置的 shell。

bash 兼容 sh 意味着，针对 sh 编写的 Shell 代码可以不加修改地在 bash 中运行。

## zsh

Linux系统使用zsh，需要单独安装。
Mac系统默认有zsh。

# 查看Linux系统有哪些shell可用

#more /etc/shells #
#/etc/shells: valid login shells
/bin/sh
/bin/bash
/usr/bin/bash
/bin/rbash
/usr/bin/rbash
/bin/dash
/usr/bin/dash
/usr/bin/tmux
/usr/bin/screen

# 查看Linux系统默认的SHELL

printenv | grep SHELL
SHELL=/bin/bash
echo $SHELL
/bin/bash