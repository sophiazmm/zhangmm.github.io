---
title: R language -- help and basic
categories: DataScience
tags:
  - R
  - basic，help
abbrlink: b8bd4b55
date: 2021-01-22 22:00:00
---

help (topic) /?topic    关于topic的文档
help.search("topic")    搜索帮助系统
apropos("topic")    返回在搜索路径下包含(部分)关键词"topic"的所有对象名称
help.start()    HTML形式的帮助
demo() R    功能演示
example(f)    运行在线帮助中的例子
str(a)    显示R对象的内在属性(*str*ucture)或简要说明对象
summary(a)    给出a的概要，通常是一个一般性统计概要；且它对不同属性的a有不同的操作方式
ls()    显示“搜索路径”下的对象；也可按指定条件搜索
ls.str()    str()搜索路径下的每个变量与其属性
dir()/list.files()    显示当前目录下的文件
getwd()    获得工作路径信息
setwd()    设置工作路径
methods(a)    显示a的“S3 method”
methods(class = class(a))    列表所有可以解决属于对象类的方法
options(...)    设置或检验全局参数；常用参数有：width, digits, error
install.packages(pkg)    安装pkg包
update.packages()    自动对比包版本，并询问更新
library(pkg)/require(x)    加载pkg包
library(help = pkg)    展示包pkg的信息
attach(x)    将x指向R的搜索路径；x可以使一个列表，数据框，或者是由save创建的R data file. 使用search()来显示搜索路径.
detach(x)    attach的逆过程
assign(x, value)    将value赋值给x, 即是“< -”
quit()    退出当前R会话(q()或ctrl.z)

#好记性不如烂笔头系列#