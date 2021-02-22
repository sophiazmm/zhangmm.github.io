---
title: sratoolkit进行组学数据格式转换(from sra to fq)
date: 2021-02-21 22:30:30
categories: DataScience
tags: Genomic data

---

# Step1: 下载安装  sratoolkit.2.10.9
wget --output-document sratoolkit.tar.gz http://ftp-trace.ncbi.nlm.nih.gov/sra/sdk/current/sratoolkit.current-ubuntu64.tar.gz
tar -vxzf sratoolkit.2.10.9-ubuntu64.tar.gz
# Step2: 确认下载数据为单端还是双端

返回值为4，为单端SE；若返回值为8，则为双端PE

sratoolkit.2.10.9-ubuntu64/bin/fastq-dump -X 1 --split-spot -Z SRR7094748.1 | wc -l
# Step3: 格式转换命令
for i in SRR*; do echo $i; sratoolkit.2.10.9-ubuntu64/bin/fastq-dump 

\#single-end 单端测序 

fastq-dump SRRxxxxxxx.sra.    # 结果生成SRRxxxxxxx.fastq 

fastq-dump --fasta SRRxxxxxxx.sra     # 结果生成SRRxxxxxxx.fastq 

\#pair-end 双端测序 

fastq-dump --split-3 SRRxxxxxxx.sra     # 结果生成 SRRxxxxxxx_1.fastq，SRRxxxxxxx_2.fastq