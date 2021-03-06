---
title: "静态建站"
date: 2021-01-25T09:50:03+08:00
lastmod: 2021-01-25T09:50:03+08:00
draft: false
keywords: ["hugo"]
description: ""
tags: ["建站", "IT"]
categories: ["IT", "建站", "DevOps"]
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
# 建站概述
小到互联网从业的个人，大到一个企业，无论你是实体企业，还是互联网龙头企业，基本上都至少有一个网站，来让别人了解你的商品或者服务，从而创造价值。因此，站点的重要性毋庸置疑。但是，从零开始搭建一个站点，做过的人都知道，这中间需要涉及到的知识，以及投入多少时间和精力，是无法估量的。小可不才，从上学开始就一直在折腾这方面的事情，不知道熬过了多少个日日夜夜，陆陆续续的攒了不少经验，这里跟大家共同探讨下。
# 建站方案
一般来讲，建站涉及到诸多方面。从前期网站规划，到内容创建，最后到网站发布，中间会设计到许多的人力，财力和物力。从内容创作角度讲，有的是动态网站，有的是静态网站。所谓的动态，就是说不同的用户，看到的内容不一样，网站的内容会随着用户的请求不同，在服务器上经过处理后，再发给用户一些响应。而静态的就是简单的回发给用户一样的内容，张三也好，李四也好，甚至王五马六看到的内容都是一样的。他们各有利弊，这里不再赘述，有兴趣的可以查看文末的一些相关资料。今天咱们这里主要分享的是静态建站的技术。相比于动态建站，静态建站的技术更加简单，适合于初学者以及小公司来进行。
# 建站步骤
建站一般需要执行下面这些步骤，
- 申请主机
- 购买域名
- 备案
- 创作内容
- 发布
- 维护


下面我们来逐个聊聊这些步骤。
## 申请主机
现在一般很少会有企业去自己单独购买物理的硬件服务器了，因为，购买服务器以后，你还得自己花精力维护，包括但不限于硬件测试，主机操作系统的安装等等。所以现在更多的是采取购买云主机的方式来租用服务器资源。
而主机服务商一般有亚马逊，谷歌，Azure，腾讯，阿里等的。具体大家可以上他们的官网看下配置，然后选择自己需要的购买。
## 申请域名
选择一个好的域名也很重要，从而让别人可以很好的记住你的服务。这个可以去万网注册，或者国外的Goddaddy等等的地方注册。
## 域名备案
在中国，我们购买的域名需要备案的，否则国家不会让你的网站接入公网，导致别人无法看到你的网站内容。这个按照对应的域名提供商的要求来就好了，提交相应的材料上去给他们，耐心等待20个左右的工作日就OK了。
## 使用Hugo创建内容
静态网站的内容就比较好准备了，比如使用我们这里介绍的Hugo，只需要撰写对应的Markdown文件就好了。注意这里说的准备内容不是在服务器上，而是在本地的机器。
## 本地安装Hugo
Hugo还是比较好安装的。针对Mac用户，使用Homebrew直接 brew install hugo就好了。Hugo提供了许多的命令来进行网站的内容创作，比如：
- hugo new site XXX
- hugo new post/xxx.md
- ...
## 创建内容
这里就是我们自由发挥的地方，把我们的内容一.md的文件写好就可以了。
## 生成内容
在你本地的网站根目录，运行：hugo，然后所有的内容就会生成在一个public目录里面
# 发布内容
打包好上面public目录里面的所有内容，然后上传到我们的跟服务器目录。
# 维护
网站发布后，以后就需要以后进行定期更新和维护。如果有新内容的创建或者更新，重复上面的步骤即可。
# 参考资料
[静态网页和动态网页的联系和区别](https://zhuanlan.zhihu.com/p/71356116)