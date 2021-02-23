---
title: Lattice plot
date: 2021-02-23 22:31:03
categories: DataScience
tags: 
  - R
  - plot
  - lattice
---

xyplot:    (y~x)双变量散点图

barnhart(y~x):    y对x的条形图

dotplot(y~x):     cleveland点图(逐行逐列累加图)

density plot(~x):    密度函数图

histogram(~x):     x的频率直方图

box plot(y~x):    箱线图

qqmatch(~x):    x关于某理论分布的分位数-分位数图

stripplot(y~x):    一维图, x必须上数值型，y可以上因子

qq(y~x):    比较两个分布的分位数，x必须是数值型，y可以是数值，字符或者是因子，但必须是两个“水平”

splom(~x):     二维图矩阵

parallel(~x):    平行坐标图

levelplot(z~x"*"y|g1"*"g2):    在x，y坐标点的z值的彩色等值线图(x, y和z等长)

wireframe(z~x"*"y|g1"*"g2):    3d透视图(面)

在一般性Lattice公式中，y~x|g1*g2有可选择条件变量g1和g2组合绘制在单独的“panels”上.Lattice函数使用了很多相同的参量作为基础附加绘图，如data=, subset=. 使用panel=来定义定制“panel”函数(参数apropos("panel")和？llines)

Lattice函数返回一个trellis类型的对象并且是“print-ed”来生成图形。内部使用print(xyplot(...))函数时，自动绘图并无效果。使用lattice.theme和lset来改变Lattice默认设置