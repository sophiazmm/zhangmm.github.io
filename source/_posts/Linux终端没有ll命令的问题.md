---
title: Linux终端没有ll命令
date: 2021-01-27 22:30:30
categories: DataScience
tags: 
  - Linux
  - ll
---

# 问题描述：

ecs-c6s-2xlarge-2-linux-20201117102944:~$ ll
ll: command not found

# 编辑～/.bashrc，添加alias：

vim ~/.bashrc 

添加:

alias ll='ls -alF' 

alias la='ls -A' 

alias vi='vim' 

alias sub='sublime-text-dev'

# 保存：

:wq!

#执行命令：#

source ~/.bashrc

# 问题解决 

![](https://tva1.sinaimg.cn/large/008eGmZEgy1gn2mp39tlbj30ln0cq40w.jpg)

