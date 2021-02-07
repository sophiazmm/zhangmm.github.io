---
title: R language--plot 2
date: 2021-02-03 21:31:03
categories: DataScience
tags: R,plot
---

points(x, y)    添加点(选项type = 可以使用)

lines(x, y)    同上，但用线

text(x, y, labels, ...)    在坐标点(x, y)加入文字

典型的使用方法：plot(x, y, type = "n"); text(x, y, names)

mtext(test, side = 3, line = 0, ...)     在指定的side添加文字(参考axis); line指定添加文字的绘图区域

segments(x0, y0, x1, y1)    从点(x0, y0)划线至点(x1, y1)

arrows(x0, y0, x1, y1, angle = 30, code = 2)    同上，当code=2以点(x0, y0)为基原点的箭头，当code=1以点（x1，y1)为原点的箭头，当code=3双箭头；angle控制箭头张开的角度

abline(a, b)    以截距为a斜率b的斜线

abline(h = y)   在y点的垂线

abline(v = x)    在x点的水平线

abline(lm, obj)    根据lm.obj做出回归线

rect(x1, y1, x2, y2)    做出左，右，底，高限制为x1,x2,y1,y2的四边形

polygon(x, y)    多边形作图

legend(x, y, legend)    在点(x, y)添加图例

title()    添加标题

axis(side, at)    添加坐标轴，底部(side = 1),左侧(2),顶部(3)或右侧(4);可选参数at指定画刻度线点位置坐标

box()    在当前图形周围加一个盒子

rug(x)    在x-轴上添加_rug_(1-d plot), 来代表数据

locator(n, type="n", ...)    在用户使用鼠标在图上点击n次返回n次点击点坐标(x, y); 并可以在点击处绘制符号(type = "p")或线(type = "1"), 缺省情况下不画符号或连线(type = "n")

#好记性不如烂笔头系列#