---
layout: default
title: "Horizon Summary: 2026-09-27 (ZH)"
date: 2026-09-27
lang: zh
---

> 从 27 条内容中筛选出 2 条重要资讯。

---

1. [Conversations XMPP 客户端退出 Google Play 并转为免费](#item-1) ⭐️ 8.0/10
2. [SemiAnalysis 拆解 Intel Panther Lake 与 18A 制程](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Conversations XMPP 客户端退出 Google Play 并转为免费](https://gultsch.de/posts/breaking-up-with-google-play/) ⭐️ 8.0/10

开源 Android XMPP 客户端 Conversations 的开发者 Daniel Gultsch 宣布，该应用现在完全免费，并不再通过 Google Play 分发，理由是该平台支持太差、对开发者待遇不公。用户需要改从项目官网或其它第三方 Android 应用商店等渠道获取该应用。 一位知名开源开发者公开离开全球最大的 Android 应用商店，为当下围绕应用商店垄断、开发者抽成与平台治理的争论提供了一个具体案例。这表明即便是成熟且被广泛使用的应用，也可能因 Google Play 的支持与审核流程成本过高、难以预测而选择离开，进而可能促使更多项目转向直接分发或替代商店。 这篇文章本质上是一份第一手经历陈述，而非技术发布，因此对用户的实际影响是：Conversations 今后需要在 Google Play 之外下载，而应用本身仍然免费。评论者指出，Google 抽取的分成并不是核心不满，真正促成这一决定的是开发者得不到及时支持，以及审核和账号验证流程难以预测。

hackernews · ezst · 9月26日 10:55 · [社区讨论](https://news.ycombinator.com/item?id=49855315)

**背景**: Conversations 是一款基于 XMPP（可扩展消息与存在协议，原名 Jabber）构建的免费开源 Android 即时通讯客户端。XMPP 是一种用于即时消息、在线状态和联系人列表的开放标准，使用 XML 进行接近实时的结构化数据交换。与多数商业即时通讯服务不同，XMPP 像电子邮件一样是联邦式的：任何人都可以自建服务器，不存在中心主服务器，不同服务器上的用户也可以互通。由 Daniel Gultsch 开发的 Conversations 是最知名的移动端 XMPP 客户端之一，而 Android 历来允许用户安装来自 Google Play 之外的应用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Conversations_%28software%29">Conversations (software) - Wikipedia</a></li>
<li><a href="https://conversations.im/">Conversations - Jabber/XMPP client for Android</a></li>
<li><a href="https://en.wikipedia.org/wiki/XMPP">XMPP - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者总体上认同开发者的批评，认为问题不在于 Google 抽取的分成，而在于垄断者可以理所当然地提供糟糕且无从追责的支持。不少人分享了自己的遭遇：有人称花了一年仍无法上架产品，因为 Google 的电话号码验证预设开发者是个人；还有人指出 Play 已从爱好者的乐园变成要求企业地址和各类证件的商业平台，同时越来越不鼓励用户安装商店之外的应用。

**标签**: `#Google Play`, `#Android`, `#Open Source`, `#App Distribution`, `#Developer Experience`

---

<a id="item-2"></a>
## [SemiAnalysis 拆解 Intel Panther Lake 与 18A 制程](https://newsletter.semianalysis.com/p/intel-panther-lake-teardown) ⭐️ 8.0/10

SemiAnalysis 发布了一份免费的实物拆解报告，借助其 STEEL（拆解工程与评估实验室）对 Intel Panther Lake 客户端 SoC 进行物理分析，检视这颗基于 Intel 18A 制程打造的芯片内部结构。该分析直接观察芯片内部，涵盖背面供电（BSPD）与全环绕栅极晶体管（GAAFET）等结构，而非依赖厂商公开资料。 Intel 18A 是该公司最先进的制程节点，也是其代工战略的核心，因此对其技术特征进行独立的物理验证对整个芯片产业都很重要。Panther Lake 是首款将 18A 投入大规模量产的客户端芯片产品，这次拆解因而成为检验 Intel 制程说法能否成立的早期实地验证。 这份拆解以免费的 SemiAnalysis STEEL 分析形式发布，该实验室专门用于在物理层面剖析先进的数据中心、AI 与客户端硬件。报告聚焦 18A 特有的创新，例如背面供电与全环绕栅极晶体管，这些正是 Intel 押注其制造路线图的差异化特性。

rss · Semianalysis · 9月26日 13:36

**背景**: Intel 18A 是 Intel 最先进芯片制造制程的名称；按命名惯例，18A 指 1.8 纳米级别的节点，明显小于上一代 Intel 3。它由两项标志性技术定义：RibbonFET（Intel 对全环绕栅极晶体管的实现）与 PowerVia（其背面供电方案）。Panther Lake 是首个采用 18A 打造的客户端处理器系列（Intel Core Ultra 系列 3）。而像 SemiAnalysis STEEL 这样的拆解实验室会逐层剥离芯片，实地查看厂商通常只在幻灯片中描述的晶体管与互连结构。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://newsletter.semianalysis.com/p/intel-panther-lake-teardown">Intel Panther Lake Teardown, 18A, BSPD, GAAFET, SemiAnalysis STEEL</a></li>
<li><a href="https://www.intel.com/content/www/us/en/foundry/process/18a.html">Intel 18A | See Our Biggest Process Innovation</a></li>

</ul>
</details>

**标签**: `#semiconductors`, `#Intel 18A`, `#Panther Lake`, `#chip fabrication`, `#hardware analysis`

---