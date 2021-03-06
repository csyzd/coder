---
title: "分布式系统架构技术研究系列-01-总体概述"
date: 2021-02-08T21:49:30+08:00
lastmod: 2021-02-08T21:49:30+08:00
draft: false
keywords: ["分布式"]
description: "分布式技术"
tags: ["分布式"]
categories: ["分布式"]
author: ""

# You can also close(false) or open(true) something for this content.
# P.S. comment can only be closed
comment: false
toc: true
autoCollapseToc: false
postMetaInFooter: false
hiddenFromHomePage: false
# You can also define another contentCopyright. e.g. contentCopyright: "This is another copyright."
contentCopyright: false
reward: false
mathjax: false
mathjaxEnableSingleDollar: false
mathjaxEnableAutoNumber: false

# You unlisted posts you might want not want the header or footer to show
hideHeaderAndFooter: false

# You can enable or disable out-of-date content warning for individual post.
# Comment this out to use the global config.
#enableOutdatedInfoWarning: false

flowchartDiagrams:
  enable: false
  options: ""

sequenceDiagrams: 
  enable: false
  options: ""

---

<!--more-->
# 引言
现在的程序员，如果不知道分布式系统，不知道高并发，不知道高可用等等高大上的名词，都不好意思说自己是程序员。其实，分布式系统也没有大家想象的那么复杂，只不过是我们平时只是专注于自己的一亩三分地---只顾着编写代码，而忽略了相关的架构设计而已。就像“苹果”砸了牛顿的脑袋，牛顿可以发现，但是普通人没有发现。同样的，分布式其实真实的存在于我们每天实际使用的软件系统中的。只要一个APP被人使用，而且QPS不是很少的几百几千的那种，基本上，都会涉及到高并发。有人可能会说了：我们公司的产品APP的确用户量很大，我每天也在写代码，但是没有感觉到什么分布式啊。。。那我这里就得啰嗦两句：同学，因为有人已经为你设计好了高并发高可用架构，你只需要添砖加瓦就够了。如果想深入学习，获得更深层次的发展，建议你好好研究你们公司的APP产品架构设计。

本文就是从通用的分布式架构设计角度来进行总结与反思的，希望可以起到抛砖引玉的作用。
# Why分布式架构
从历史角度讲，传统的单体应用将应用层，DB层全部偶合在一起。随着用户量和访问量的增大，依赖单一硬件的单体应用变得逐渐臃肿和难以扩展。因此，将数据库，应用服务器等等作拆分，做集群，做负载均衡，加缓存等，在廉价的硬件上进行部署应用变得更加可行。但是，拆分在带来便利的同时，也不可避免的受限于许多挑战，如：
- 网络分区问题（Partition）。根据CAP理论以及现实的实际情况，我们几乎可以认为网络分区在分布式架构下是不可避免的。我们不是科学家，只需要记住这个结论就好了，无需我们去证明之。常见的应对网络分区问题的技术方案有：重试，优化，减少传输内容，采用合理的传输协议等。
- 服务的可用性问题（Availability）。简单来说，就是服务器有没有挂掉，服务APP是否还可以被使用，是否变得不能使用了或者说响应变得极其缓慢而难以被用户接受。解决可用性问题的常用方案列举如下：使用探针监控，心跳检测等对服务器进行监控。同时，可以采用负载均衡，失效转移，主从切换等方案来保证服务的可用性。
- 数据的一致性等（Consistency）。由于是分布式系统，因此就存在多个节点。多个节点之间进行分工协作，来共同完成系统的功能。但是，节点与节点之间不是孤立的，它们需要彼此之间进行通信。不同节点之间通信的时候，由于链路不同或者通信方式不同，可能会产生脏数据或者异常的数据。一般此类问题的应对方案有：超时机制加消息队列加失败处理。

虽说分布式架构存在诸多技术难点，但是，本人觉得，这也正是分布式架构相关技术的魅力所在。
# 分布式架构的理念
其实，隐藏在分布式架构背后的一个关键的思想就是：
> 拆分：将大的模块拆成粒度更小的模块或者服务，从而使得可以使用更多的廉价的PC、Server来支撑业务的运行。

拆分的目标就是为了：
- 服务之间的耦合性更低
- 服务的容错性更好。为了达到这个目的，通常我们有以下技术方案：
> - 重试
> - 降级
> - 熔断
> - 限流
- 整体应用的性能更好

# 总结
本篇文章是从高屋建瓴的角度来简要阐述分布式架构的一些基本概念。后续文章中，我们会来剖析整个架构技术栈。加油！💪🏻

# 参考资料
[用大白话聊聊分布式系统](https://waylau.com/talk-about-distributed-system/)