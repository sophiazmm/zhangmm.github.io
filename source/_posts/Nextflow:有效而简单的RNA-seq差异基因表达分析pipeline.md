---
title: Nextflow: 有效简单的RNA-seq差异基因表达分析pipeline
categories: DataScience
tags:
  - Conda
  - Nextflow
  - RNA-seq
  - pipeline
date: 2021-03-12  23:00:00
---

​    该pipeline是在交互式工作管理器Nextflow v20.10.0中实现的，使其可移植，可伸缩，可并行化，并确保了高水平的可重复性。


![](https://tva1.sinaimg.cn/large/008eGmZEly1gogwex8q1dj318k0u0wsg.jpg)

​            图1 Nextflow工作流程图。圆圈表示输入数据，下载图标表示资源的自动下载，星号标记的步骤目前仅适用于某些物种

**一. 安装**

1. Install `conda`

```shell
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
bash Miniconda3-latest-Linux-x86_64.sh
```

2. Install `Nextflow` via `conda`

```shell
conda create -n nextflow -c bioconda nextflow
conda activate nextflow
```

![](https://tva1.sinaimg.cn/large/008eGmZEly1gogx1jofptj31xw0pgdy9.jpg)

3. 对于转录组组装，还需要安装```Docker``` 和 ```Singularity```

​        通过conda安装singularity

```shell
conda create -n singularity -c conda-forge singularity
conda active singularity
```

​        如果已有nextflow的conda安装环境，可直接系统安装：

```shell
conda activate nextflow
conda install -c conda-forge singularity
```

**二. 快速开始**

1. 试运行开始

  ```shell
 # conda activate nextflow
nextflow run hoelzer-lab/rnaflow -profile test,conda,local
  ```

​      本地试运行（最多共有30个core）

```
nextflow run hoelzer-lab/rnaflow -profile test,conda,local -w work \
--max_cores 30 --cores 10 --softlink_results -r master
```

![](https://tva1.sinaimg.cn/large/008eGmZEly1goh118tkpbj31dk0nqtq9.jpg)

​     （试运行步骤时间略微有些长啊）

2. 请求帮助

```shell
nextflow run hoelzer-lab/rnaflow --help
```

3. 更新pipeline

```shell
nextflow pull hoelzer-lab/rnaflow
```

4. 利用特定版本

```shell
nextflow pull hoelzer-lab/rnaflow -r <RELEASE>
```

**三. 正式使用**

```shell
nextflow run hoelzer-lab/rnaflow --reads input.csv --autodownload hsa --pathway hsa --max_cores 6 --cores 2
```

利用 -- autodownload <hsa|mmu|mau|eco> build-in species, 

![](https://tva1.sinaimg.cn/large/008eGmZEly1goh1u64vfbj31co0k8420.jpg)

或是在CSV文件中定义自己的基因组参考和注释文件：

```shell
nextflow run hoelzer-lab/rnaflow --reads input.csv --genome fastas.csv --annotation gtfs.csv --max_cores 6 --cores 2
```

1. 输入文件

Read files (required)

确定read文件是FASTQ格式 -- reads input.csv

reads文件可以被压缩为.gz

单端输入文件：

```shell
Sample,R,Condition,Source
mock_rep1,/path/to/reads/mock1.fastq.gz,mock,
mock_rep2,/path/to/reads/mock2.fastq.gz,mock,
mock_rep3,/path/to/reads/mock3.fastq.gz,mock,
treated_rep1,/path/to/reads/treat1.fastq.gz,treated,
treated_rep2,/path/to/reads/treat2.fastq.gz,treated,
treated_rep3,/path/to/reads/treat3.fastq.gz,treated,
```

双端输入文件

```shell
Sample,R1,R2,Condition,Source
mock_rep1,/path/to/reads/mock1_1.fastq,/path/to/reads/mock1_2.fastq,mock,A
mock_rep2,/path/to/reads/mock2_1.fastq,/path/to/reads/mock2_2.fastq,mock,B
mock_rep3,/path/to/reads/mock3_1.fastq,/path/to/reads/mock3_2.fastq,mock,C
treated_rep1,/path/to/reads/treat1_1.fastq,/path/to/reads/treat1_2.fastq,treated,A
treated_rep2,/path/to/reads/treat2_1.fastq,/path/to/reads/treat2_2.fastq,treated,B
treated_rep3,/path/to/reads/treat3_1.fastq,/path/to/reads/treat3_2.fastq,treated,C
```

2. 基因组和注释文件

   如果没有利用 [build-in species](https://github.com/hoelzer-lab/rnaflow#build-in-species)，

   指定基因组文件 --genome fastas.csv

   ```shell
   /path/to/reference_genome1.fasta
   /path/to/reference_genome2.fasta
   ```

   指定注释文件 --annotation gtfs.csv

   ```shell
   /path/to/reference_annotation_1.gtf
   /path/to/reference_annotation_2.gtf
   ```

3. 恢复运行

   如果更改参数或输入，可以恢复运行。

   Nextflow将尝试不重新计算已经完成的步骤：

   ```shell
   nextflow run hoelzer-lab/rnaflow -profile test,conda,local -resume
   ```

**四. 结果**

1. 可产生结构合理的输出，并提供对DEG的全面解析

2. RNA-Seq结果与qRT-PCR结果密切相关

3. 与其他RNA-seq pipeline做比较分析

![](https://tva1.sinaimg.cn/large/008eGmZEly1goh55ohot6j31nt0u0jyk.jpg)


