---
layout: default
title: "Horizon Summary: 2026-08-18 (ZH)"
date: 2026-08-18
lang: zh
---

> 从 31 条内容中筛选出 6 条重要资讯。

---

1. [Mojo 编程语言以 Apache 2.0 许可证开源](#item-1) ⭐️ 9.0/10
2. [Qwen 3.8 27B 在 AI 智能指数上得 52 分，追平 GPT-5.6 Luna](#item-2) ⭐️ 9.0/10
3. [Seth Godin：亚马逊的广告驱动搜索向消费者征收“税”](#item-3) ⭐️ 8.0/10
4. [Linux 7.3 提升显存耗尽时的性能](#item-4) ⭐️ 8.0/10
5. [中国要求政府机构提前卸载定制版 Windows 10](#item-5) ⭐️ 8.0/10
6. [国产 AI 芯片 2026 年将占中国市场近 90%，寒武纪与华为领跑](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Mojo 编程语言以 Apache 2.0 许可证开源](https://simonwillison.net/2026/Aug/18/mojo-is-now-open-source/) ⭐️ 9.0/10

2026 年 8 月 18 日，Modular 以 Apache 2.0 许可证发布了 Mojo 的编译器与工具链，此前一周项目刚刚发布了 1.0 版本。该语言现已在 Linux 和 macOS 上完全开源。 此举兑现了 Mojo 自 2023 年 5 月发布以来的开源承诺，使其成为高性能、与 Python 相邻的计算领域的可靠开源选择。借助 MLIR 和类 Python 语法，Mojo 有望改变 AI/ML 系统编程，让开发者获得一门针对 GPU 和 TPU 加速的、受 Rust 启发的语言。 Mojo 最初目标是成为 Python 的超集，但大约在 2025 年 8 月项目改变了方向，如今 Mojo 是自己的一门语言，采用受 Python 启发的语法，而非完全兼容 Python。它基于 MLIR 编译器框架，可面向 CPU、GPU、TPU 及其他加速器，并包含受 Rust 启发的静态类型和借用检查器等功能。

rss · Simon Willison · 8月18日 21:39

**背景**: Mojo 是由 Modular 公司创建的编程语言，旨在将 Python 的易用性与系统级性能结合起来。该语言于 2023 年 5 月发布时承诺最终会将编译器开源。Mojo 采用类似 Python 的语法，同时融入了所有权和借用检查等系统编程概念（类似 Rust）。通过在 MLIR 而非 LLVM 之上构建，Mojo 能为多种硬件加速器生成高度优化的代码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mojo_%28programming_language%29">Mojo (programming language)</a></li>
<li><a href="https://mojolang.org/">Mojo</a></li>

</ul>
</details>

**标签**: `#Mojo`, `#programming language`, `#open source`, `#compiler`, `#AI/ML`

---

<a id="item-2"></a>
## [Qwen 3.8 27B 在 AI 智能指数上得 52 分，追平 GPT-5.6 Luna](https://simonwillison.net/2026/Aug/17/qwen-38-27b-scores-52/) ⭐️ 9.0/10

Qwen 3.8 27B，一个 270 亿参数的模型，在 Artificial Analysis Intelligence Index 上获得 52 分，与 GPT-5.6 Luna（最大值）持平，仅比 GLM-5.2（753B）和 DeepSeek V4 Pro（1.7T）低 1 分。这一结果突显了这款相对较小的开源模型在效率上的重大突破。 这是一项重大的效率突破：一个 27B 模型能与数千亿甚至 1.7 万亿参数的模型相抗衡，表明规模并非通往智能的唯一路径。它可能降低部署成本，让前沿级 AI 更普及，并重塑业界对模型开发的认知。 Artificial Analysis Intelligence Index 是多项生产环境基准测试得分的加权平均值，范围从 0 到 100；v4.1 版本中 Agent 任务权重为 34%，编码为 24%，科学推理为 24%，通用任务为 18%。Qwen 3.8 27B 的 52 分与 GPT-5.6 Luna 持平，后者的参数量未公开，但推测远大于 27B。

rss · Simon Willison · 8月17日 23:58

**背景**: Artificial Analysis Intelligence Index 通过综合 Agent、编码、科学推理和通用知识等基准测试的分数，以 0–100 的刻度评估 AI 模型。过去，更高的智能分数与模型规模高度相关，因此小模型通常在性能上不如大型前沿系统。Qwen 3.8 27B 以极少的参数取得接近顶级的分数，打破了这一模式，表明高效的架构和训练方法正在快速进步。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://artificialanalysis.ai/evaluations/artificial-analysis-intelligence-index">Artificial Analysis Intelligence Index | Artificial Analysis</a></li>
<li><a href="https://artificialanalysis.ai/">AI Model &amp; API Providers Analysis | Artificial Analysis</a></li>

</ul>
</details>

**标签**: `#AI`, `#LLM`, `#Qwen`, `#benchmark`, `#model efficiency`

---

<a id="item-3"></a>
## [Seth Godin：亚马逊的广告驱动搜索向消费者征收“税”](https://seths.blog/2026/08/the-amazon-tax/) ⭐️ 8.0/10

Seth Godin 的博文《The Amazon tax》指出，亚马逊的搜索结果日益被广告和平台自身商业利益扭曲，让消费者付出时间和选择自由的代价。 这之所以重要，是因为亚马逊是占主导地位的购物搜索引擎，其从相关性向广告驱动排名的转变每天影响数百万买家。这也引发了对大型科技平台自我优待和搜索质量下降的更广泛担忧。 Seth Godin 用“税”的比喻来描述浏览赞助和无关结果所付出的隐性成本。该帖获得了 503 条评论，反映出读者对这一问题的强烈共鸣。

hackernews · herbertl · 8月18日 13:22 · [社区讨论](https://news.ycombinator.com/item?id=49345263)

**背景**: 亚马逊的商品搜索由 A9 算法驱动，其主要目标是将客户与他们最有可能购买的商品匹配。然而，排名因素包括赞助位和销售表现，这可能挤掉自然相关结果。监管机构和研究者也在审视“自我优待”（self-preferencing）现象，即同时销售自有产品的平台可能在推荐中偏好自有商品，而非第三方卖家的商品。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/A9.com">A9.com - Wikipedia</a></li>
<li><a href="https://myamazonguy.com/seo/amazon-a9-search-engine/">Amazon A9 Algorithm | What It Is and How It Works</a></li>
<li><a href="https://arxiv.org/pdf/2303.14947">Measuring Self-Preferencing on Digital Platforms - arXiv.org</a></li>

</ul>
</details>

**社区讨论**: 评论者大多同意 Godin 的看法，指出搜索已从“找到准确商品”变成“展示平台选定的结果”。一些人分享了因质量下滑而转向本地商店或其他平台的亲身经历；也有评论者认为，相关广告仍有价值，并以 Google 搜索广告作比较。

**标签**: `#Amazon`, `#search`, `#advertising`, `#platform economics`, `#consumer behavior`

---

<a id="item-4"></a>
## [Linux 7.3 提升显存耗尽时的性能](https://pixelcluster.dev/VRAM-Overcommit/) ⭐️ 8.0/10

文章报道称，Linux 7.3 针对显存超卖（VRAM overcommit）场景引入了性能改进，旨在减少显存耗尽时的卡顿并改善帧时间。文章还讨论了内核端的可能策略，例如更优的内存分配提示和虚拟内存碎片整理。 随着显存成为 AI 训练、游戏和渲染的瓶颈，更好的显存超卖处理可以显著改善显存受限系统的用户体验。这对依赖开源驱动并希望进一步挖掘硬件潜力的 Linux 用户尤其重要。 这篇题为《VRAM 管理第二部分：超越极限》的文章指出，显存超卖时的体验仍可能时好时坏，帧时间会随场景中观察的物体而变化。作者认为，应用程序最适合告知内核哪些内存分配应保留在显存中。

hackernews · flaburgan · 8月18日 07:51 · [社区讨论](https://news.ycombinator.com/item?id=49342719)

**背景**: 显存超卖（VRAM overcommit）允许 GPU 应用程序使用比物理显存更多的内存，方法是在显存和系统内存之间移动页面。这个换页过程通常很慢，可能导致卡顿，尤其是在游戏和机器学习工作负载中。Linux 内核一直在改进其内存管理和 GPU 换页算法，以使该过程更流畅，而文章探讨了 Linux 7.3 在这方面带来的变化。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pixelcluster.dev/VRAM-Overcommit/">VRAM Management Part 2: Beyond the Limits... | pixelcluster&#x27;s GPU blog</a></li>
<li><a href="https://www.cs.unc.edu/~anderson/papers/rtss22c.pdf">Enabling GPU Memory Oversubscription via</a></li>

</ul>
</details>

**社区讨论**: 评论者总体对这些改进表示热情，有人称赞文章“写得很好且信息丰富”，也有人表示在 7.2 之后迫不及待地等待 7.3 发布。一些人对 Nvidia 驱动仍缺少合适的 GPU 换页支持表示失望，还有评论者认为应用程序自身应向内核提供内存驻留提示。另有一条评论对年轻跨性别者为底层性能工程所做的贡献表示感谢。

**标签**: `#Linux`, `#kernel`, `#VRAM`, `#performance`, `#memory-management`

---

<a id="item-5"></a>
## [中国要求政府机构提前卸载定制版 Windows 10](https://www.bloomberg.com/news/articles/2026-08-18/china-axing-microsoft-windows-from-state-agencies-ahead-of-plan) ⭐️ 8.0/10

中国国家安全部已要求部分政府机构卸载定制版 Windows 10，比原定 2027 年 2 月的停用计划提前数月，理由是数据安全担忧。微软表示未发现影响该产品的安全事件，该产品仍在定期获得安全更新。 这一加速行动表明中国国家层面对外国软件的网络安全隐患日益警惕，对微软的政府业务和全球科技供应链都有影响。这也反映了在关键基础设施领域推广国产替代的更大趋势。 定制版 Windows 10 即通过微软与中国电科（CETC）合资公司 CMIT 于 2017 年开发的中国政府版，旨在让政府客户对安全和遥测数据有更多掌控。该指令由国家安全部发出，但未说明具体漏洞或原因。

telegram · zaihuapd · 8月18日 06:22

**背景**: Windows 10 中国政府版于 2017 年发布，由联想等厂商预装在面向中国政府客户的设备上，其功能针对本地安全和合规需求进行了定制。微软对 Windows 10 的支持已于 2025 年 10 月终止，但中国政府原本计划在 2027 年 2 月前停用。新的指令要求部分机构提前卸载。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Windows_10_China_Government_edition">Windows 10 China Government edition</a></li>
<li><a href="https://blogs.windows.com/windowsexperience/2017/05/23/announcing-windows-10-china-government-edition-new-surface-pro/">Announcing Windows 10 China Government Edition and the new Surface Pro | Windows Experience Blog</a></li>

</ul>
</details>

**标签**: `#China`, `#Microsoft`, `#Cybersecurity`, `#Government Policy`, `#Windows 10`

---

<a id="item-6"></a>
## [国产 AI 芯片 2026 年将占中国市场近 90%，寒武纪与华为领跑](https://www.tomshardware.com/tech-industry/artificial-intelligence/chinas-homegrown-ai-accelerators-to-supply-90-percent-of-the-countrys-domestic-market-analysts-suggest-cambricon-and-huawei-expected-to-be-the-biggest-winners-in-the-shift-away-from-nvidia-and-amd) ⭐️ 8.0/10

TrendForce 预测，到 2026 年中国本土 AI 加速器将占国内市场的近 90%，而去年仅为 45%。在这一摆脱英伟达和 AMD 的转变中，寒武纪与华为预计将成为最大赢家。 这标志着中国 AI 芯片供应格局发生重大转变，主要受美国出口管制和地缘政治紧张推动。此举可能重塑全球 AI 芯片市场，并加速中国的半导体自主化进程。 2025 年，英伟达在中国市场占据 55%份额，出货 220 万颗；华为出货 81.2 万颗，占比 20.3%。中国需要在一年内将高端 AI 芯片产量提升 2.2 倍，达到约 196 万颗，但产能能否跟上仍存疑虑。

telegram · zaihuapd · 8月18日 13:03

**背景**: AI 加速器又称神经处理单元，是一类专门加速人工智能和机器学习任务（如深度学习和计算机视觉）的硬件。寒武纪是一家总部位于北京的国有参股中国公司，主要设计用于云端和边缘计算的 AI 芯片。这一预测反映了美国对先进芯片出口管制的影响，促使中国大力扶持寒武纪和华为等本土供应商。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cambricon_Technologies">Cambricon Technologies - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/AI_accelerator">Neural processing unit - Wikipedia</a></li>
<li><a href="https://www.ibm.com/think/topics/ai-accelerator">What is an AI accelerator? | IBM</a></li>

</ul>
</details>

**标签**: `#AI chips`, `#China`, `#Huawei`, `#Cambricon`, `#semiconductors`

---