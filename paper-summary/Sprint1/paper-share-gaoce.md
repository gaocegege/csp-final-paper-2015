# 论文分享

## MUVI

MUVI跟其他的论文比，最大的贡献在于提出了相关变量的分析。而且MUVI不单单是对于data race的detection，还涉及到其他的一些东西，比如关联变量的同时更新问题。

相比于之前的研究MUVI的优点有下面这样几点：

1. 第一次在data race detection上引入了对两个变量的分析。
2. 对于多变量还有其他的检查，比如同时更新检查等等。

为了做到这么多点，MUVI有一些改进，比如修改了两种非常经典的data race detection的算法，lockset和happen before等等。

同时，MUVI也有一些缺点，我个人认为缺点有：

1. 有N多阈值需要设置
2. 为了复杂度做了很多妥协，比如在关联度分析的时候，没有递归的函数里面的关联度分析，等等
3. 只能分析两个变量的关系

## Goldilocks

基于Java虚拟机提出了一种Race Condition Detection的方法，每当运行时候发现有数据竞争的时候会抛一个异常。

是使用了原本的基于Lockset的算法，论文里提出了一套形式化的方法，来替代原本的Lockset的更新规则，比较亮眼的地方在于支持软件层面的事务，把事务机制也加入到了数据竞争检查当中。

延伸阅读

* The Java Memory Model POPL05
* Fondations of the C++ Concurrency Memory Model PLDI’08，这两个是关于并发的内存模型的
* Software Transactional Memory PODC 95，应用层面的事务
* Eraser: A dynamic data race detector for multithreaded programs TOCS 97，最早提出LockSet方法的论文