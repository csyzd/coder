---
title: "关于"
date: 2021-01-25T09:26:02+08:00
lastmod: 2021-01-25T09:26:02+08:00
draft: false
keywords: []
description: ""
tags: []
categories: []
author: ""

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

# 个人综述
具有10+年的技术积累，英文听说读写流利，具备扎实的Java基础，熟悉目前主流的微服务架构和相关的开源的技术，如Spring，MyBatis等。曾负责Oracle Fusion Financials中的Expense产品的研发。对于软件的稳定性，可维护性，可扩展性等具有深刻的认知，具备从前端到后端的调优经验，多次帮助客户和同事解决技术问题。由于技术过硬，成为了中国研发中心TA团队的一员，专门解决各种技术疑难杂症。同时具备优秀的领导能力和组织协调能力，带领团队高效率高质量完成项目任务，曾多次组织跨国团队协作解决世界500强企业（如HSBC，FedEx，YUM）客户的疑难问题。

# 技能概述
- 熟悉Java基础，例如：IO/多线程/集合框架等
- 熟悉JVM底层机制
- 熟悉Linux日常使用
- 熟悉MySQL数据库
- 熟悉常见开源框架，如Spring Cloud, MyBatis, Redis, RabbitMQ
- 擅长分析问题，解决问题
- 英文听说读写流利
- 拥有优秀的领导能力，沟通能力和强烈的团队合作精神
- 具有很强的快速学习能力
- 熟悉性能调优并具备强烈的代码质量意识

# 工作经历
## Oracle，2016.09 ~ 2020.08，高级软件开发
### 主要工作职责
1.	与Oracle公司的全球客户，如HSBC，FedEx，YUM等世界500强企业举行电话会议，理解客户的关切，解决客户的各种难题，找出疑难问题的根本原因。
2.	解决整个中国研发中心Fusion团队成员的日常开发技术难题。
3.	撰写新特性的技术设计文档
4.	编写/测试核心业务代码
5.	审阅团队成员提交的代码。对具有Smell的代码作出comment，对好的代码作出表扬，号召团队学习。在团队中贯彻质量代码意识，帮助大家编写可读性强，可维护性好的代码。同时，要求所有提交的业务代码必须要有JUnit 单元测试。
6.	领导一支5人的团队，践行Scrum敏捷开发模型。整个团队步调一致，工作积极性高，按期举行每周计划会议，每日站立会议，每周总结反思会议，扫除团队成员的工作障碍，得到了团队成员的积极反馈。
7.	培训引导新人，帮助他们快速成长并适应新的工作环境。
8.	举行技术/业务分享会议。通过深入浅出的讲述，将复杂晦涩难懂的技术，以幽默和平易近人的方式，与同事分享。积极参与团队技术讨论，解惑答疑,  被同事公认为技术专家。

### 主要业绩
1.	连续三年获得中国区最佳年度个人奖项；
2.	团队成员培养卓有成效。新人加入团队后，在流程上，技术上对他们进行培训；定期检查座谈，给予必要的帮助；从而使其两周后即可开始承担开发工作，远远低于其他团队培训平均需６周的时间。两周后带领团队修复Bug，半个月内将bug数量从120+降到60+，得到了公司VP的盛赞，赢得了Support和客户的衷心感谢，整个团队获得了满满的荣誉感，同时，也收获同事的信任与爱戴。

### 项目经验
- 2020 年4 月，解决Expense Auditor页面性能问题
该问题表现为客户的 Expense Auditor点击页面上的一个链接后，加载非常缓慢最长超过70s的时间。影响范围为HSBC，FedEX，YUM等美巨头客户，该问题的严重性在几天之内直接升级为P1。该问题的关键在于仅仅找到执行缓慢的SQL还不够，另外还需要开发人员对Oracle的MDS技术有一定的了解．通过与美国Cloud/Ops，PSR DB团队，本地团队以及客户跨时区多次沟通，分析并确认最终的问题是由定制引起的；再与客户商讨确定修改不合理的定制，在两周内解决了该问题，得到了客户的一致信任与认可。

- 2019 年 11 月，解决重复的Invoice问题
由于没有日志，代码逻辑复杂混乱，缺少注释，客户可提供的信息资料有限，测试步骤繁琐，测试环境复杂, 该问题潜伏达 18 个月, 受影响客户数多达45个世界500强企业巨头。经与客户沟通，首先使用SQL帮助客户甄别出重复交易的款项，并让客户联系银行。然后通过化繁为简，动态更新代码，模拟测试等手段进行仔细的代码走读和调试，找到问题的根源并修复，为客户挽回巨额损失，获得客户的衷心感谢。事后，撰写技术文档，分享模块代码和业务知识，得到同事, 尤其是美国总部高层管理人员的一致好评。

- 2018年03月，解决Mac上的Web-AddIn无法加载问题
客户提出需要Oracle的ERP产品尽快支持在Mac上运行Microsoft Office Excel的Web-AddIn，但本地开发团队反映Web-AddIn始终无法正确加载，导致开发进度陷于停滞。解决该问题的挑战在于两点。一是需要快速的学习Microsoft的Office上的Web-AddIn的运行原理；二是定性该问题为Microsoft相关产品的bug，需要跨公司和Microsoft Office开发团队进行沟通。经过一周的多次线上会议，与美国的Microsoft团队共同确认了问题所在，Microsoft很快修复了问题，使得本地的开发人员得以继续进行后续开发工作，保证了项目的正常进度。同时，获得了Microsoft Office团队的盛赞。


- 2017 年08 月，解决时间日期列表无法显示的问题 
该问题表现为Oracle的ADFdi Workbook打开后，日期下拉列表的所有选择项目全部显示为空白项。该问题的挑战在于开发人员必须具备诸多知识：浏览器如何渲染页面，怎样抓HTTP包，使用什么工具抓包，以及如何验证该问题的RCA是否分析的正确, 甚至涉及到Microsoft Windows平台的相关开发知识。反复测试发现，实际上选择某一个条目后，实际的数据会被提交到后台。因此，作为一个workaround，建议客户先手动数一下，选择对应的条目。同时，开发通过研究对比正常的行为和Workbook中的控件的行为，使用Fiddler获取控件渲染的HTML源码，发现，原来是控件渲染的Select标签下的option子元素上的文本内容为空。找到问题后，将分析归档，然后上报Bug给Middleware团队处理修复。通过指导新人处理这个问题并撰写技术分享文档，许多同事反映，该案例帮助他们成功高效地处理了很多类似的问题。		

## Beyond Soft，2012.02 ~ 2016.08，高级软件开发
### 主要工作职责
1.	审阅业务需求文档
2.	开发测试新功能
3.	审查其他团队成员的代码
4.	修复测试/产品报告的问题
5.	给美国总部的管理人员做演示

### 主要业绩　
在该公司任职期间，与美国HP总部的产品经理一起沟通产品的功能，UI特性等，及时完成新feature的研发，bug的修复以及代码的merge。曾编写辅助开发测试工具，将平常需要频繁获取token的操作时间由人均每次30+s直接优化到一键获取，而时间只需要2s，大大提升了团队的工作效率，得到了美国HP总部经理，产品经理等的赞赏，后来，该工具还被引入美国HP总部，纳入VCS进行管理。由于工作能力突出，于2015财年获得优秀员工奖项。

## Pragmatic Hi-Tech (Shenzhen)， 2010.07 ~ 2012.01, 初级软件开发
### 主要工作职责
1.	编写开发PEM的代码；
2.	按照测试驱动开发的要求来编写单元测试；
3.	跟丹麦客户就他们的关切进行沟通，并给出解决方案；
4.	分析/开发新的APP部署脚本，使用PEM来部署；

# 教育经历
- 2006.09 ～2010.07 天津科技大学 工学学士
- 2006.09 ～2010.07 天津科技大学 管理学学士

# 外语水平
大学英语六级，可正常沟通交流。

# 兴趣爱好
阅读，探索极客技术。
