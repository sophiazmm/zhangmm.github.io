---
title: Linux系统下docker修改默认存储目录
date: 2021-02-02 21:00:00
categories: DataScience
tags:
  - Linux
  - docker
---

# 关闭docker 服务

sudo service docker stop

# 迁移/备份文件

cp -a /var/lib/docker /m/data/wuji/

mv -u /var/lib/docker /var/lib/docker.bak

# 建立软连接

sudo ln -fs /m/data/wuji/docker /var/lib/docker

# 重启docker

sudo service docker start

#也可以通过修改配置文件的方式，但是不如这个简单

# 删除备份文件

sudo rm -rf /var/lib/docker.bak

https://ld246.com/article/1566017283738