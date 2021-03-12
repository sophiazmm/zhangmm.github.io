---
title: Linux常用命令之任务管理
categories: DataScience
tags:
  - Linux
date: 2021-02-24  23:00:00
---

**1. ps**

*查看系统进程*

a: 显示当前终端的所有进程

u: 显示进程的用户名和启动时间等

ps au:

![](https://tva1.sinaimg.cn/large/008eGmZEly1gnz1d4vewgj31ao06277x.jpg)

USER: 用户名

PID：进程号

%CPU：进程占用CPU的百分比

%MEM：进程占用内存的百分比

VSZ：使用的虚拟内存

RSS：使用的固定内存

TTY：进程的终端号

STAT：当前状态（R，S，T，Z）

TIME：运行时间

COMMAND：指令

与重定向、管道命令组合使用，查找所需要的进程，如：

ps -e u|grep meng (查找指定用户的进程)

![](https://tva1.sinaimg.cn/large/008eGmZEly1gnz1lpfyo6j314w08o7af.jpg)



**2. kill **

*终止后台进程*

用法：kill[参数] 进程1 进程2

-s: 指定发送的信号

-l：指定信号的名称

top 查看运行的程序，获取PID

kill -s 9 8888

-s 9 制定了传递给进程的信号是9，即强制、尽快终止进程



**3. top**

*显示运行中的程序*

用法：top [参数]

-u: 显示某用户的程序

-d: 调整更新秒数，默认是5秒

如： top -d 10 -u meng 

![](https://tva1.sinaimg.cn/large/008eGmZEly1gnz1uiyvkdj30xs07ijvo.jpg)

PID：进程id 

USER：用户

PR：进程优先级

NI：nice值，正负分别表示正负优先级

VIRT：进程使用的虚拟内存总量

RES：进程使用的物理内存大小

SHR：共享内存大小

S：状态

%CPU：CPU使用占比

%MEM：内存使用占比



**3. nohup**

*投递任务到本地后台*

用法：nohuo command &  /// nohup sh work.sh &



**4. qsub**

*向集群投递任务*

用法：qsub -V -cwd -1 vf = 1G, p=4 -q reset.q job



**5. qstat**

*查询任务*

用法：qstat  /// qstat -j jobid



