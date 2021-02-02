---
title: R language--plot
date: 2021-02-01 21:31:03
categories: DataScience
tags: R,plot
---

plot(x).   在x轴上顺次地绘制x值（y轴上）

plot(x, y).   双变量绘图（散点图）

hist(x)    x的频数直方图

barplot(x)    x的条形图；使用horiz = FALSE改变绘图水平或垂直

dotchart(x).   如果x为数据框，绘制Cleveland dot图(stacked plots line-by-line and column-by-column)

pie(x).   饼图

boxplot(x).   箱线图

curve(expr, from, to, add = FALSE)    根据给定函数或表达在区间‘[from，to]’上绘制曲线

sunflowerplot(x, y)    是以相似坐标的点作为花朵，其花瓣数目为点的个数

coplot(x~y| z)    根据z值或值间隔绘制x和y的双变量图

interaction.plot(f1, f2, y)    如果f1和f2是因子，作y的均值图，以f1的不同值作为x轴，而f2的不同值对应不同曲线：可以选项fun指定y的其他的统计量(缺省计算均值，fun = mean)

marplot(x, y).   二元图，其中x的第一列对应y的第一列，x的第二列对应y的第二列，依次类推

fourfoldplot(x).   用四个四分之一圆显示2x2列联表情况(x必须是dim = c(2, 2, k))的数组，或者是dim = c(2, 2)的矩阵，如果k = 1)

assocplot(x)    Cohen-Friendly图，显示在二维列联表中行、列变量偏离独立性的程度

mosaicplot(x).   列联表的对数线性回归残差的马赛克图

pairs(x).   如果x是矩阵或是数据框，作x的各列之间的二元图

plot.ts(x)    如果x是类ts的对象，作x的时间序列曲线，x可以是多元的，但是序列必须有相同的频率和时间

ts.plot(x).   同上，但如果x是多元的，序列可有不同的时间但须有相同的频率

qqnorm(x).   正态分位数图

qqplot(x,y).    x对y的分位数-分位数图

contour(x, y, z)    绘制轮廓图(画曲线时使用内插替换补充空白的值)，x和y必须为向量，z必须为矩阵，使得dim(z) = c(length(x), length(y))(x和y可以省略)

filled.contour(x, y, z)    同上，等高线之间的区域时彩色的，并且绘制彩色对应的值的图例

image(x, y, z)    同上，但是实际数据大小用不同色彩表示

persp(x, y, z)    同上，但为透视图

stars(x).   如果x是矩阵或者数据框，用星形和线段画出，星代表x的每一行线段代表列的长度

symbols(x, y, ...)    在由x和y给定坐标画符号（圆，正方形，长方形，星，温度计式或者盒形图），符号的类型、大小、颜色等由另外的变量指定

termplot(mod, obj)    绘制回归模型（mod, obj）的（偏）影响图

add = FALSE   如果TRUE，在前一个图上（如果存在）添加绘图

axes = TRUE  如果FALSE, 不绘出坐标轴和盒子

type = "p"  指定绘制图的类型，“p”：点， “1”：线，”b“：用线连接的点，“o”：同上.但线穿过点，“h”：垂直的线， “s”:阶梯， 但数据由垂直线的顶端代表，“s”：阶梯，但数据由垂直线的底端代表

xlim = , ylim = 指定坐标轴的最小和最大限制

xlab = , ylab = 注释坐标轴

main = 主标题

sub =  副标题（小号字体）

#好记性不如烂笔头系列#