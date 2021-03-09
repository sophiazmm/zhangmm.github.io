---
title: Data visualization with ggplot2 -- Geoms
categories: DataScience
tags:
  - R 
  - ggplot2
  - Visualization
  - Geoms
  - Two variable
date: 2021-03-08  20:00:00
---


**Two Variables**

**1. Continuous X, Continuous Y**

*f <- ggplot(mpg, aes(city, hwy))*

![](https://tva1.sinaimg.cn/large/008eGmZEly1gocp23r9ayj30ns0qkgpi.jpg)

**2. Continuous Bivariate Distribution**

*j <- ggplot(movies, aes(year, rating))*

![](https://tva1.sinaimg.cn/large/008eGmZEly1gocp53lut3j30ny0co0um.jpg)

**3. Continuous Function**

*j<- ggplot(economics, aes(data, unemployment))*

![](https://tva1.sinaimg.cn/large/008eGmZEly1gocp939nmnj30ny0ccta9.jpg)

**4. Discrete X, Continuous Y**

*g <- ggplot(mpg, aes(class, hwy))*

![](https://tva1.sinaimg.cn/large/008eGmZEly1gocpzbnq27j30n40g0418.jpg)

**5. Discrete X, Discrete Y**

*h <- ggplot(diamonds, aes(cut, color))*

![image-20210308192842408](/Users/sophia/Library/Application Support/typora-user-images/image-20210308192842408.png)

**6. Visualizing error**

*df <- data.frame(grp = c("A", "B"), fit = 4:5, se = 1:2)*

*k <- ggplot(df, aes(grp, fit, ymin = fit-se, max = fit+se))*

![](https://tva1.sinaimg.cn/large/008eGmZEly1gocq7ibc25j30ny0fyq9f.jpg)

**7. Maps**

*data <- data.frame(murder = USArrests$Murder, state = tolower(rownames(USArrests)))*

*map <- map_data("state")*

*I <- ggplot(data, ase(fill = murder))*

![](https://tva1.sinaimg.cn/large/008eGmZEly1gocqd0kz80j30nw05g3zi.jpg)

*好记性不如烂笔头系列*

