# AVIO

## 简介

AVIO是一个基于access interleaving invariant的运行时的检查工具。文中提及了两个实现，一种实现是纯粹软件层面的，另一种实现是需要对硬件做修改的。两种各有好处。软件层面的实现简单，不过性能差。

## 之前研究的不足

只关注data race，没关注原子性。这样会造成很多问题，文章1.2主要是在讲产生的问题。比如会说data race free不代表没问题等等

## AVIO的实现

第一步，先Serializability Analysis。总结了几种pattern，比较直观。

接下来，定义完上面的各种pattern，用一个类似状态机的东西做pattern matching。也很简单