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
	readme.md                 readme

##论文查找

###李菁菁 

    1   Learning from Mistakes（ASPLOS'08）— A Comprehensive Study on Real World Concurrency Bug Characteristics：对现实世界中concurrency bug特性的全面研究。
    2   ConSeq: Detecting Concurrency Bugs through Sequential Errors(ASPLOS’11)：bug detectiion的一种方法。
    3   A Case for an Interleaving Constrained Shared-Memory Multi-Processor(ISCA’09):提出一种限制策略来减少concurrency bugs.
    4   Efficient Concurrency-Bug Detection Across Inputs(OOPSLA ’13):we use open-source software to study how existing concurrency-bug detection tools work for a set of inputs.