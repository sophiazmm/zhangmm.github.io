---
title: R language -- parameter
date: 2021-02-03 21:31:03
categories: DataScience
tags:
  - R
  - plot
  - parameter
---

可以使用par(...)来永久性改变绘图参数；很多参数也可以作为绘图命令的选项

adj    控制文字对齐方式(0左对齐，0.5居中对齐，1右对齐)

bg    指定背景颜色(如：bg = "red", bg = "blue", ... 用colors()可以显示657种可用颜色)

bty    控制图形边框形状，可使用的值为：“0”，“1”，“7’，”c", "u"或“J”(边框和字符想象)；如果bty = "n"则不绘制边框

cex    控制缺省状态下符号和文字大小的值；下面的参数有 同样的功能：cex.axis，坐标轴刻度，cex.lab，坐标轴标签，cex.main，标题，cex.sub, 副标题

col    控制符号和连线的颜色；使用颜色名称：“red", "blue"参考colors()或作为“#RRGGBB”；参考rgb(),hsv(),grey(),和rainbow();同参数cex类似：col.axis, col.lab, col.main, col.sub

font    控制文本字体的整数(1:正常，2:斜体，3:粗体，4:斜粗体)；还可以使用font.axis, font.lab, font.main, font.sub

las    控制坐标轴刻度数字标记方向的整数(0:平行于轴，1:横排，2:垂直于轴，3:竖排)

lty    控制连线的类型，可以是整数或字符(1:"solid", 2:"dashed", 3:"dotted", 4: "dotdash", 5:"longish", 6:"twodash"), 或不超过8个字符的字符串(“0”至“9”间的数)交替指定线和空白的长度，单位为磅("points")和像素，如Its = "44"和Its = 2一样

lwd    控制连线宽度的数字，默认1

mar    控制图形边空的有4个值的向量c(bottom, left, top, right), 默认值为c(5.1， 4.1， 4.1， 2.1)

mex    声明图形同边缘协调成都的字符大小的附加变量。注意，它并不改变字体的大小。

Mfcol    用c(nr, nc)向量分割绘图窗口为nr行和nc列，按列使用子窗口

pch    控制符号的类型，可以是1至25的整数，或是“”里的单个字符

ps    控制文字大小的整数，单位为磅(points)

pty    指定绘图区域类型的字符，“s”：正方形，“m”：最大利用

tck    指定轴上刻度长度的值，单位上百分比，以图形宽、高中最小一个作为基数；如果tck = 1则绘制grid

tcl     同上，但以文本行的高度为基数(默认为tcl = -0.5)

xaxt    如果xaxt = "n"则设置x-轴但不显示(有助于和axis(side = 1, ...)一起使用）

Yaxt    同上，y-轴

#好记性不如烂笔头系列#