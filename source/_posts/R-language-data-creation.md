---
title: R language -- data creation
date: 2021-01-24 11:38:28
categories: DataScience
tags: R language, data
---

c(...).    常见的将一系列参量转化为向量的函数；通过recursive = TRUE降序排列列表并组合所有的元素为向量

from:to    产生一个序列；“:”有较高级别的优先级；1:4+1得到“2,3,4,5”

seq(from, to).    产生一个序列by= 指定要求长度

seq(along=x).   产生1,2,...,  length(along); 常用在循环上 

rep(x, times).   重复x times次；使用each= 来指定元素x重复的次数；rep(c(1,2,3),2)将得到1 2 3 1 2 3; rep(c(1,2,3), each=2)将得到1 1 2 2 3 3 

data.frame(...).   创建数据框，当然变量可能被命名或不被命名；data.frame(v=1:4), ch=c("a","B","c","d"), n=10; 相对较短的向量会被循环填充到最长向量长度

list(...).   创建一个由变量组成的列表，变量可能被命名或未被命名；list(a=c(1,2), b="hi", c=3i);

array(x, dim=).   产生由x组成的数组；使用类似dim=c(3,4,2)指定维数；如果x不够长度，则x自动循环

matrix(x, nrow=, ncol=).    矩阵；同上

factor(x, levels=).   把向量x编码成为因子

gl(n, k, length=n*k, labels=1:n).   通过指定水平方式产生水平(因子)；k为水平的个数；n为重复的次数

expand.grid().   提供的向量或因子所有组合构成的数据框

rbind(...).   把以行的形式组合矩阵，数据框或其他

cbind(...).   把以列的形式组合矩阵，数据框或其他



#好记性不如烂笔头系列#