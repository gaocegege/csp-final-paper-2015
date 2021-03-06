# CSP-Final-Paper

## 纪要

### 15.12.16

主题确定：Finding Concurrency Bugs

	1	find concurrency bugs:
		a	MUVI, SOSP 2007 : 通过code analysis 找到application中存在的concurrency bugs
		b	Automated concurrency0bug fixing OSDI 2012
		c	SKI: exposing kernel concurrency bugs through systematic schedule exploration, OSDI 2014  找到的是kernel中的concurrency bug


## 目录结构

	paper/                    论文目录
		relevant/             相关论文
		referenced-by-MUVI/   被MUVI引用的论文
		who-references-MUVI/  引用MUVI的论文
	style-guide/              格式参考，内含ROP讲课的学长刘宇涛的paper
	paper-summary/            论文总结
	readme.md                 readme

##论文查找

###李菁菁 

    1   Learning from Mistakes（ASPLOS'08）— A Comprehensive Study on Real World Concurrency Bug Characteristics：对现实世界中concurrency bug特性的全面研究。
    2   ConSeq: Detecting Concurrency Bugs through Sequential Errors(ASPLOS’11)：bug detectiion的一种方法。
    3   A Case for an Interleaving Constrained Shared-Memory Multi-Processor(ISCA’09):提出一种限制策略来减少concurrency bugs.
    4   Efficient Concurrency-Bug Detection Across Inputs(OOPSLA ’13):we use open-source software to study how existing concurrency-bug detection tools work for a set of inputs.
- - -
####文章放在了relevant文件夹下

    5   Non-Race Concurrency Bug Detection Through Order-Sensitive Critical Sections(ISCA'13):运行时bug detectio,针对non-race concurrency bugs.
    6   Detecting Concurrency Bugs from the Perspectives of Synchronization Intentions(TPDS'11): 同样为Currency Bug Detection.AVIO+MUVI.感觉这篇文章下阶段最值得读。
    7   ConMem(ASPLOS’10):针对并发错误中导致程序crash的detector.
    8   Static Data Race Detection for Cocurrent Programs with Asynchronous Calls(ESEC-FSE'09):多线程（以C语言为例）中函数异步调用时static data race detection technique.
    9  Bug Characteristics in open source software: 开源软件的bug特征。
    10  Finding Complex Concurrency Bugs in Large Multi-Threaded Application(EuroSys'11)：一种在程序执行时找到触发并发错误的detector。

###夏亦谦
    1   Colorama: Architectural Support for Data-Centric Synchronization. 一个简化编写并行程序的复杂度的系统。能帮我们debug传统的大部分代码，但是需要一些硬件支持，有较少的开销。
    2   Autolocker: Synchronization Inference for Atomic Sections. 提出了一种不太牺牲性能或者兼容性的类“transactional memory”的方法，用了一种基于锁的方法，适合多核处理器架构。
    3   AVIO: Detecting Atomicity Violations via Access-Interleaving Invariants. 提出了一种检测atomicity violation bugs的方法。

## 任务分配

Paper                                                                           | Assigned to
-------------                                                                   | -------------
MUVI(SOSP‘07)                                                                   | 夏亦谦、高策、张坚鑫、李菁菁
ConSeq: Detecting Concurrency Bugs through Sequential Errors(ASPLOS’11)         | 刘宁、夏亦谦
Efficient Concurrency-Bug Detection Across Inputs(OOPSLA’13)                    | 刘宁、张坚鑫
Goldilocks: a race and transaction-aware java runtime(PLDI '07)  | 高策、李菁菁
Learning from Mistakes: A Comprehensive Study on Real World Concurrency Bug Characteristics(ASPLOS'08)  | 张坚鑫
Non-Race Concurrency Bug Detection Through Order-Sensitive Critical Sections(ISCA'13) | 刘宁
Detecting Concurrency Bugs from the Perspectives of Synchronization Intentions(TPDS'11) | 李菁菁、夏亦谦
AVIO: Detecting Atomicity Violations via Access-Interleaving Invariants(ASPLOS'06) | 高策

## 其他资料
* [作者Lu Shan的论文列表](http://dblp.uni-trier.de/pers/hd/l/Lu:Shan):列出了很多关于concurrency bug detection的文章，可以参考。
