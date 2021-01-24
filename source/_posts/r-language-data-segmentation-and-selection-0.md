---
title: r language -- data segmentation and selection
date: 2021-01-24 16:36:21
categories: DataScience
tags: R 
---

#向量索引#

x[n].    第n个元素

x[-n].    除了第n个元素的x

x[1:n].    前n个元素

x[-(1:n)].    第n+1至最后的元素

x[c(1,4,2)].    指定元素

x[“name”].    名为“name”的元素

x[x > 3].    所有大于3的元素

x[ x > 3 & x < 5 ].    区间(3,5)的元素

x[x %in% c("a",“and”,"the")].    给定组中的元素

#列表索引#

x[n].    列表显示元素n

x[[n]].    列表的第n个元素

x[[“name”]].    列名为“name"的元素

x$name.    名为”name“的元素

#矩阵索引#

x[i, j].    下标为(i,j)的元素

x[i, ].    第i行

x[, j].    第j列

x[x, c(1,3)].    第1和3列

x["name", ].    名为“name”的行

#数据框索引(矩阵索引加下述)#

x[["name"]].   列名为“name”的列

x$name.    列名为“name”的列