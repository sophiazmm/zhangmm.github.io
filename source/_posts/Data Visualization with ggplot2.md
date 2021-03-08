---
title: Data visualization with ggplot2 -- Basics
categories: DataScience
tags:
  - R 
  - ggplot2
  - Basics
date: 2021-03-06  19:00:00
---

**ggplot2** is based on the grammar of graphics, the idea that you can build every graph from the same few components: a data set, a set of geoms - visual marks that represent data points, and a coordinate system.
![](https://tva1.sinaimg.cn/large/008eGmZEly1goco4b62itj30f607q0ti.jpg)

To display data values, map variables in the data set to aesthetic properties of the geom like size, color, and x and y locations.

![](https://tva1.sinaimg.cn/large/e6c9d24ely1go73l07jgjj20f808qtau.jpg)

Build a graph with **qplot() **or **ggplot()**

![](https://tva1.sinaimg.cn/large/008eGmZEly1gocnctyw5pj30nu0omn8s.jpg)

**last_plot**

​    Returns the last plot

**ggsave("plot.png", width = 5, height = 5)**

​    Saves last plot as 5'✖️5‘file named “plot.png” in working directory. Matches file type to file extension.

