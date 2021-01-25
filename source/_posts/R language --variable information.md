---
layout: R language -- variable information
title: R language -- variable information
date: 2021-01-25 14:01:37
tags: R；variable
---

#变量变换#

as.array(x), as.data.frame(x), as.numeric(x), as.logical(x), as.complex(x), as.character(x)等

转换变量类型；使用如下命令得到全部列表：methods(as)

#变量信息#

is.na(x), is.null(x), is.array(x), is.data.frame(x),is.numeric(x), is.complex(x), is.character(x), ...

检验变量类型；使用如下命令得到全部列表，methods

length(x).     x中元素的个数

dim(x).    重新设置或设置对象的维数；dim(x) < - c(3,2)

dimnames(x).    重新设置或设置对象的名称

nrow(x)和NROW(x).    返回行的个数dim(x)[1]

ncol(x)和NCOL(x).    返回列的个数dim(x)[2]

class(x).    得到或设置x的类； class(x) <- "myclass"

unclass(x).    删除x的类

names(x).    查看或设置对象名称(names)

unnamed(x).    删除R对象的名称(names)或维名称(dimnames)

enlist(x).    将列表x转化为向量

attr(x, which).    得到或设置x的属性类型which

attributes(obj).    得到或设置obj的属性列表



#好记性不如烂笔头系列#