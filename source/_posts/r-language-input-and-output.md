---
title: R language--input and output
date: 2021-01-23 22:31:03
categories: DataScience
tags: R,input,output
---

load()    加载由save命令得到的资料集

data(x)    加载指定的数据

edit()    调用文本编辑器修改R对象

fix(x)    'fix'调用“edit”修改‘x’

data.entry(x)    使用电子数据表形式的录入编辑器

scan(x)    从控制台或文件中读取数据为向量或列表

read.table(file)    读取表格式的文件并将其创建成数据框；默认分割符sep=""为任意空白；使用header= TRUE读取第一行作为列标题；使用as.is = true防止字符向量变为factors；使用comment.char=""防止“#”被解释为注释；使用skip=n在读数据前跳过n行；详细见帮助关于行命名，NA处理

read.csv("filename", header = TRUE)    同上，但默认设置为读取csv文件(Comma Separated values)

read.delim("filename", header = TRUE)    同上，默认设置为读取tab分割文件

read.fwf(file, widths,header = F, sep = "\t", as.is = FALSE)    以fixed width formatted 形式读取数据至数据框; widths是整数向量，用于设置调整宽度字段

save(file, ...)    以不分平台的二进制保存指定的对象

save.image(file)    保存所有的对象

dump("x","...")    将对象x保存在“...”里

cat(..., file = "", sep="")    强制转化为字符后打印对象的赋值，sep为对象赋值间的分割符号

print(a, ...)    显示a的赋值，对于不同的对象可以有不同的表达方式

format(x, ...)    格式化，更好的显示R对象

write.table(x, file = "", row.names = T, col.names = T, sep="")    在把x转化为数据框后，写到文件；如果quote为TRUE, 字符和因子列就会被(")所包围；sep是字段分割符；eol为尾行分割符；na为缺失值字符串；使用col.names = NA增加列标题以便于和表格输入一致

sink(file)    输出到文件file，直到输入命令sink()

大部分I/O函数都有file参量，经常用一个字符串来命名文件或连接. file = ""意味着标准输入或输出，连接(connections)可以包含文件(file),管道(pipes),压缩文件(zipped files)或R变量

在Windows操作环境下，数据共享可以通过写字板(cliboard)的方式.读取excel表：可以将Excel中数据拷贝至写字板(内存)，使用x <- read.delim("clipboard")方式读取数据。如果要将数据供Excel使用，write.table(x, "clipboard", sep="\t", col.name= NA)可以数据库方面的交互应用，请见RODBC, DBI, RMySQL, and ROracle包，读取其他文件格式参考XML, hdf5, netCD等包。



#好记性不如烂烂笔头系列#