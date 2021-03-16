---
title: 安装R包的三种不同途径
date: 2021-03-16 23:00:00
categories: DataScience
tags:
  - R
---
**1. 三种途径：**

CRAN：install.packages

Bioconductor：biocLite 

GitHub：devtools::install_github

**2. 举例**

(1)
install.packages("xxxxxx") 

(2)
if (!requireNamespace("BiocManager", quietly = TRUE))
  install.packages("BiocManager")

BiocManager::install("xxxxxx")

(3)
devtools::install_github('xxxxxx‘')