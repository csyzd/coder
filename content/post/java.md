---
title: "Java程序员必知必会"
date: 2021-01-29T09:31:15+08:00
lastmod: 2021-01-29T09:31:15+08:00
draft: true
keywords: []
description: ""
tags: ["Java"]
categories: ["Java"]
author: "Yuzhao"

# You can also close(false) or open(true) something for this content.
# P.S. comment can only be closed
comment: false
toc: false
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
# 概述
架构师，architect，这个角色在不同的公司里面，定义的职责不完全一样。这里无意引起口水之战，我们着重从技术层面来剖析下，一个合格的架构师，究竟应该具备什么样的技术知识。

首先，我们来看一张图，

![架构师技术图](/images/architect.png)

# 详解
相信一看到这个图，很多人的第一想法可能是：太多了。。。

但是，别着急，虽说内容挺多，但是掌握起来，还是有迹可循的。下面，咱们来聊聊这里面的“门道”，也就是所谓的学习路线。

## 基础
基础部分，首当其冲的就要数计算机科学的四大核心：操作系统，数据结构，计算机网络，计算机组成原理与设计，相信大多数人都已经学过。我们呢这里毋需赘言，重要性也不言而喻。提醒一点，在很多大厂的面试中，基本上都会考察算法的设计与实现，所以，记得多刷刷算法题，熟悉常见的数据结构和算法，做好万全的准备。

其次，就是Java SE的基础部分。这里包含常用的一些API的设计与实现以及底层原理，我们需要熟悉。典型的有：JVM，Collections，IO/NIO/NIO2，多线程等。

再次，就是需要熟练掌握Linux操作系统。因为，大多数的系统最终都是运行在Linux上的。以后，实际的线上环境基本上都是Linux的，我们需要学会怎么去拿日志文件，怎么在大量的文件中快速定位我们需要的信息。

紧接着，就是数据库部分。我们所有重要的数据，最终都会以某种持久化的形式保存在存储介质上。而且，为了方便管理和查询，我们一般使用数据库系统。所以，掌握一个常见的数据库系统很有必要。当然，这里的掌握不仅仅是指该数据库系统的常见用法，我们还需要掌握该数据库系统的特点，底层的一些原理，比如说存储索引结构。

## 进阶
当死磕完基础部分以后，就要熟悉市面上常见的流行开源框架了。框架的作用就是避免重复造轮子，在有限的时间，财力和人力情况下，尽可能的高效的完成开发任务。常用的包括Spring全家桶系列，MyBatis等。值得注意的是，这里要搞清楚框架怎么用，还要搞清楚为什么框架这么设计，有什么好处，怎么提高开发人员的效率的。
