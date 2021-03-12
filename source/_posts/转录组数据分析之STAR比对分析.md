---
title: 转录组数据分析之STAR比对分析：
categories: DataScience
tags:
  - Linux
  - RNA-seq
  - STAR
  - mapping
date: 2021-03-01  23:00:00
---
**1. STAR软件下载安装**

​     STAR （https://github.com/alexdobin/STAR/releases/tag/2.7.7a）
​     STAR-2.7.7a.tar.gz
​     tar -zxvf STAR-2.7.7a.tar.gz

**2. STAR比对分析流程**

```Linux
2.1 建立索引文件
../../software/STAR-2.7.7a/bin/Linux_x86_64/STAR --runMode genomeGenerate \
 --genomeDir C_genome_dir \
 --genomeFastaFiles Homo_sapiens.GRCh38.dna.primary_assembly.fa \
 --runThreadN 8 

2.2 比对RNA-seq reads到参考基因组
 
 * 1st pass
 ../../software/STAR-2.7.7a/bin/Linux_x86_64/STAR --genomeDir C_genome_dir \
  --readFilesIn C_1_paired.fq.gz C_2_paired.fq.gz \
  --runThreadN 8 \
  --readFilesCommand zcat \
  --outFilterType BySJout \
  --outFileNamePrefix C_  
 
* 建立基因组索引文件
 ../../software/STAR-2.7.7a/bin/Linux_x86_64/STAR --runMode genomeGenerate \
 --genomeDir C_genome_dir \
 --genomeFastaFiles Homo_sapiens.GRCh38.dna.primary_assembly.fa \
 --sjdbFileChrStartEnd C_SJ.out.tab \
 --sjdbOverhang 75 \
 --runThreadN 8 
 
* 2st pass，最后的比对
 ../../software/STAR-2.7.7a/bin/Linux_x86_64/STAR --genomeDir C_genome_dir \
 --readFilesIn C_1_paired.fq.gz C_2_paired.fq.gz \
 --runThreadN 8 \
 --readFilesCommand zcat \
 --outFilterType BySJout \
 --outSAMtype BAM SortedByCoordinate \
 --outSAMattrRGline ID:ENCSR000COQ1 LB:library PL:illumina PU:machine SM:GM12878 \
 --outFileNamePrefix C_

(The STAR manual tells us that we need make 2-pass mapping)

* 对产生的bam文件建立索引文件
samtools index final_alignments.bam
```