## Learning from Mistakes — A Comprehensive Study on Real World Concurrency Bug Characteristics 


对于现实世界的并发bug特征的一个全面的研究

一些有趣的发现：

1. 1/3被检测的非死锁并发错误，是由于程序员安排的操作时序被破坏，而这一点是早期的同步技术无法监测到的
2. 34%由多变量引起，无法检测
3. 92%的检测到bug可以使用不超过4个memory操作就能够重现
4. 73%的错误难以被程序员准确的定位出原因


传统的方法存在着不少的问题：

Concurrency bug detection ：虽然以前已经有很多人针对data race和deadlock做出了很多方案，但是这些方法都不够的全面，例如无法找到更多的bug，对bug的修复没有什么帮助等等。

Concurrent program testing and model checking ：很多的bug需要特定的输入和特定的执行序列才能触发，很难设计Test input

Concurrent programming language design ：到底能找到哪一类的bug，能不能更加有效的帮助程序员理解bug的出现原因

本文研究主要集中在bug的这些特征：bug pattern，manifestation（表现形式）fix strategy（修复策略），建立目录如下：

寻找bug，用比较常用的程序进行寻找，Mysql等，然后从bug database里面挑出典型的bug（随机），再由人工确认