---
title: pvactools docker安装及应用
date: 2021-01-29 21:00:00
categories: DataScience
tags:
  - pvactools
  - pipeline
  - docker
---

# download pvaactools image

```
docker run -it griffithlab/pvactools
```

# make dir of example input and out data

```
mkdir /mnt/data/meng/pvactools/pvacseq_example_data
mkdir /mnt/data/meng/pvactools/pvacseq_output_data
```

#  run 

```
docker run \
-v /mnt/data/meng/pvactools/pvacseq_example_data:/pvacseq_example_data \
-v /mnt/data/meng/pvactools/pvacseq_output_data:/pvacseq_output_data \
-it griffithlab/pvactools
```

#  download example data

~~~
pvacseq download_example_data /tmp/
mv /tmp/pvacseq_example_data/*  /pvacseq_example_data/

~~~

# run pvacseq example

```
pvacseq run \
/pvacseq_example_data/input.vcf \
Test \
HLA-A*02:01,HLA-B*35:01,DRB1*11:01 \
MHCflurry MHCnuggetsI MHCnuggetsII NNalign NetMHC PickPocket SMM SMMPMBEC SMMalign \
/pvacseq_output_data \
-e 8,9,10
```

