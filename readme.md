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

###夏亦谦
    1   Colorama: Architectural Support for Data-Centric Synchronization. 一个简化编写并行程序的复杂度的系统。能帮我们debug传统的大部分代码，但是需要一些硬件支持，有较少的开销。
    2   Autolocker: Synchronization Inference for Atomic Sections. 提出了一种不太牺牲性能或者兼容性的类“transactional memory”的方法，用了一种基于锁的方法，适合多核处理器架构。
    

## 任务分配

Paper                                                                           | Assigned to
-------------                                                                   | -------------
MUVI(SOSP‘07)                                                                   | 夏亦谦、高策、张坚鑫、李菁菁
ConSeq: Detecting Concurrency Bugs through Sequential Errors(ASPLOS’11)         | 刘宁、夏亦谦
Efficient Concurrency-Bug Detection Across Inputs(OOPSLA’13)                    | 刘宁、张坚鑫
Goldilocks: a race and transaction-aware java runtime(PLDI '07)  | 高策、李菁菁
