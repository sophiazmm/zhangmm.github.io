---
title: 安装R包之DESeq2
date: 2021-03-15 23:00:00
categories: DataScience
tags:
  - R
---
1. 安装：
   ```
   install.packages("DESeq2")
   ```
   报错：
   
   ![](https://tva1.sinaimg.cn/large/e6c9d24ely1gokpxv6mgtj20z809e75y.jpg)
   
2. 如下安装：

   


```shell
if (!requireNamespace("BiocManager", quietly = TRUE))
  install.packages("BiocManager")

BiocManager::install("DESeq2")
```

