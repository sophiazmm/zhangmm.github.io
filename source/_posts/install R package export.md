---
title: install R package export
categories: DataScience
tags:
  - R
  - export
abbrlink: 4eb2368d
date: 2021-01-21 22:00:00
---

需要先安装依赖，然后github下载源码，修改源码后打包，并使用devtools安装

# 安装依赖包

~~~R
install.packages("officer")
install.packages("rvg")
install.packages("openxlsx")
install.packages("ggplot2")
install.packages("flextable")
install.packages("xtable")
install.packages("rgl")
install.packages("stargazer")
install.packages("tikzDevice")
install.packages("xml2")
install.packages("broom")
install.packages("devtools")
library(devtools)
~~~

# 下载源码

~~~shell
wget https://github.com/tomwenseleers/export/releases/tag/0.2.2
~~~

# 修改源码

为什么要修改？？因为新版本的officer包没有ph_with_vg_at函数。

![](https://tva1.sinaimg.cn/large/008eGmZEly1gmvpjtx5voj30iw05ot96.jpg)

export包中使用ph_with_vg_at函数的地方，全部换成ph_with应该就可以。

~~~R
doc = ph_with_vg_at(doc, code = myplot(), left = offx, top = offy, width = w, height = h, ...)
~~~

替换为

~~~R
doc = officer::ph_with(doc, value = rvg::dml(myplot()), location = ph_location(left = offx, top = offy, width = w, height = h))
~~~

# 重新打包（压缩即可）

~~~
tar -zcvf ./export export.tar.gz
~~~

# 安装export

~~~R
install.packages("./export.tar.gz", repos = NULL, type = "source")
~~~

