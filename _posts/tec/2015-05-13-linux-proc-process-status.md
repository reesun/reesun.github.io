---
layout: post
title: linux查看进程信息 /proc/:pid/status 
category: 技术
tags: linux进程 linux进程内存 linux进程信息
keywords: linux process status
description: 
---

linux中可以通过`/proc/<pid>/staus`查看进程的相关信息。包括内存使用等情况

	$ cat /proc/9744/status

- Name: gedit /*进程的程序名*/
-  State: S (sleeping) /*进程的状态信息*/
- Tgid: 9744 /*线程组号*/
- Pid: 9744 /*进程pid*/
- PPid: 7672 /*父进程的pid*/
- TracerPid: 0 /*跟踪进程的pid*/
- Uid: 1000    1000    1000    1000 /*uid euid suid fsuid*/
- Gid: 1000    1000    1000    1000 /*gid egid sgid fsgid*/
- FDSize: 256 /*文件描述符的最大个数，file->fds*/
- Groups: 0 4 20 24 25 29 30 44 46 107 109 115 124 1000 /*启动该进程的用户所属的组的id*/
- VmPeak: 60184 kB /*进程地址空间的大小*/
- VmSize: 60180 kB /*进程虚拟地址空间的大小reserved_vm：进程在预留或特殊的内存间的物理页*/
- VmLck: 0 kB /*进程已经锁住的物理内存的大小.锁住的物理内存不能交换到硬盘*/
- VmHWM: 18020 kB /*文件内存映射和匿名内存映射的大小*/
- VmRSS: 18020 kB /*应用程序正在使用的物理内存的大小，就是用ps命令的参数rss的值 (rss)*/
- VmData: 12240 kB /*程序数据段的大小（所占虚拟内存的大小），存放初始化了的数据*/
- VmStk: 84 kB /*进程在用户态的栈的大小*/
- VmExe: 576 kB /*程序所拥有的可执行虚拟内存的大小,代码段,不包括任务使用的库 */
- VmLib: 21072 kB /*被映像到任务的虚拟内存空间的库的大小*/
- VmPTE: 56 kB /*该进程的所有页表的大小*/
- Threads: 1 /*共享使用该信号描述符的任务的个数*/
- SigQ: 0/8183 /*待处理信号的个数/目前最大可以处理的信号的个数*/
- SigPnd: 0000000000000000 /*屏蔽位，存储了该线程的待处理信号*/
- ShdPnd: 0000000000000000 /*屏蔽位，存储了该线程组的待处理信号*/
- SigBlk: 0000000000000000 /*存放被阻塞的信号*/
- SigIgn: 0000000000001000 /*存放被忽略的信号*/
- SigCgt: 0000000180000000 /*存放被俘获到的信号*/
- CapInh: 0000000000000000 /*能被当前进程执行的程序的继承的能力*/
- CapPrm: 0000000000000000 /*进程能够使用的能力，可以包含CapEff中没有的能力，这些能力是被进程自己临时放弃的*/
- CapEff: 0000000000000000 /*是CapPrm的一个子集，进程放弃没有必要的能力有利于提高安全性*/
- Cpus_allowed: 01 /*可以执行该进程的CPU掩码集*/
- Mems_allowed: 1 /**/
- voluntary_ctxt_switches: 1241 /*进程主动切换的次数*/
- nonvoluntary_ctxt_switches: 717 /*进程被动切换的次数*/