---
title: 学习Linux系统miniconda安装
categories: DataScience
tags:
  - Linux
  - miniconda
date: 2021-03-011  23:00:00
---

**1.miniconda官方：**

 https://docs.conda.io/en/latest/miniconda.html

 https://docs.conda.io/en/latest/miniconda.html/Miniconda3-latest-Linux-x86_64

下载最新版本:

```shell
wget -c https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
```

![](https://tva1.sinaimg.cn/large/008eGmZEly1gog9j8pzdfj31xu0dotm6.jpg)

**2. 安装miniconda**

```shell
chmod 777 Miniconda3-latest-Linux-x86_64.sh
```

```shell
bash Miniconda3-latest-Linux-x86_64.sh
```

![](https://tva1.sinaimg.cn/large/008eGmZEly1gog9n7n85fj30ze0ougzl.jpg)

**3. 启用miniconda**

```shell
cd  /home/meng/miniconda3/bin
```

```shell
chmod 777 activate
```

```shell
. ./activate
```

![](https://tva1.sinaimg.cn/large/008eGmZEly1goga4g41gjj30s610ine8.jpg)

**4. 添加清华镜像**

```shell
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/ 
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/bioconda/
```

**5. 显示安装的镜像**

```shell
conda config --set show_channel_urls yes 
```

查看已经添加的频道

```shell
conda config --get channels
```

![](https://tva1.sinaimg.cn/large/008eGmZEly1goga8jc4iaj318m07yjwz.jpg)

**6. 安装软件**

```shell
 conda install nextflow
```

![](https://tva1.sinaimg.cn/large/008eGmZEly1gogd7pw1fpj31y40ggdsp.jpg)

**7. 退出环境**

```shell
. ./deactivate
& conda deactivate
```