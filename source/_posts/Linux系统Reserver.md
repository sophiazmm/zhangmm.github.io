---
title: Rserver修改用户package文件夹
date: 2021-02-01 23:00:00
categories: DataScience
tags:
  - Rserver
  - Linux
---

# 迁移/备份文件

cp -a /home/wuji/R /m/data/wuji/

mv -u /home/wuji/R  /home/wuji/R.bak

# 建立软连接

sudo ln -fs /m/data/wuji/R  /home/wuji/R

# 关闭session 重建测试下是否有问题

![](https://tva1.sinaimg.cn/large/008eGmZEly1gn5sgjincoj30k20fs43r.jpg)

# 删除备份文件

sudo rm -rf /home/wuji/R.bak