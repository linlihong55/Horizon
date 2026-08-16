---
layout: default
title: "Horizon Summary: 2026-08-16 (ZH)"
date: 2026-08-16
lang: zh
---

> 从 32 条内容中筛选出 8 条重要资讯。

---

1. [Anthropic 官方发布 Claude 系统提示词，提升模型透明度](#item-1) ⭐️ 8.0/10
2. [AI 模型正有意让自己变“笨”](#item-2) ⭐️ 8.0/10
3. [Cloudflare 在切换 DNS 后悄悄注入分析脚本](#item-3) ⭐️ 8.0/10
4. [Qwen 3.8 27B 表现出色，但默认过度思考](#item-4) ⭐️ 8.0/10
5. [PJM 建模错误浪费 120 亿美元用户资金](#item-5) ⭐️ 8.0/10
6. [SSOG-Attention：用可分离高斯和实现亚二次注意力，替代 SDPA](#item-6) ⭐️ 8.0/10
7. [重新审视 ECA-Net：跨通道交互的核心假设并不成立](#item-7) ⭐️ 8.0/10
8. [Anthropic 第二季营收超 115 亿美元，同比增 14 倍，IPO 在即](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Anthropic 官方发布 Claude 系统提示词，提升模型透明度](https://platform.claude.com/docs/en/release-notes/system-prompts) ⭐️ 8.0/10

Anthropic 已在平台文档发布说明中公开了其 Claude 模型（包括 Opus 4.8、Fable 5 和 Mythos 5）的官方系统提示词。这一发布使开发者和研究者能够查看塑造 Claude 行为的确切指令。 这是 Anthropic 在透明度方面的重要举措，让社区难得地看到前沿 AI 模型是如何被指令的。它有助于详细分析模型行为、安全准则和优先级层次，并可能为其他 AI 实验室树立发布类似文档的先例。 系统提示词包含处理危机情况、优先考虑用户福祉以及验证图片是否存在的指令。Simon Willison 创建了一个 git 提交历史来追踪不同模型版本之间的变化，并指出最有趣的补充是关于 Claude Fable 5 和 Mythos 5 首次发布的细节。

hackernews · tosh · 8月16日 12:48 · [社区讨论](https://news.ycombinator.com/item?id=49319556)

**背景**: 系统提示词是在用户输入之前发送给大语言模型的预定义指令，定义了模型的角色、行为、语气、约束和安全边界。它们优先于用户输入，AI 部署者使用它们来确保一致的响应。通过发布这些提示词，Anthropic 允许外部分析其模型如何被对齐和控制。这是 AI 开发中日益增长的透明度趋势的一部分，尽管系统提示词只是塑造行为的复杂系统中的一个层次。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://promptengineering.org/system-prompts-in-large-language-models/">System Prompts in Large Language Models</a></li>
<li><a href="https://arxiv.org/html/2505.21091v2">Position is Power: System Prompts as a Mechanism of Bias in Large Language Models (LLMs)</a></li>
<li><a href="https://gate.ai/blog/what-is-a-system-prompt-how-does-it-differ-from-a-user-prompt">What Is a System Prompt ? How Does It Differ from a User Prompt ?...</a></li>

</ul>
</details>

**社区讨论**: 社区讨论中，Simon Willison 提供了提示词变更的 git 历史以追踪不同版本之间的差异。其他用户评论了消息的细节，如危机处理指南，而一位用户则对论坛对负面 AI 报道的审核表示担忧。总体而言，对透明度的态度是积极且技术参与的。

**标签**: `#AI`, `#LLM`, `#Claude`, `#System Prompts`, `#Transparency`

---

<a id="item-2"></a>
## [AI 模型正有意让自己变“笨”](https://w4g1.dev/blog/models-are-getting-dumber-on-purpose) ⭐️ 8.0/10

文章指出，AI 开发者正有意让大语言模型不再依赖权重中记住的事实，而是更多地在推理时依靠工具调用和检索增强生成（RAG）。这是一种刻意的设计取舍：让模型减少对内部参数化记忆的依赖，从而借助外部知识实现更高的准确性和可控性。 这一转变可能重塑 AI 系统的构建和评估方式，让“知识截止日期”变得不再重要，并让幻觉问题的解决从扩大训练数据转向架构层面的设计。开发和构建 LLM 相关产品的公司与研究者都需要把工具调用和检索当作一等公民组件，而不是可有可无的附加功能。 文章引用了不允许使用工具的事实回忆基准 SimpleQA 为例，指出目前排名第一的 Gemini 2.5 Pro 正确率也只有 53%，以此论证纯参数化记忆从根本上就不可靠。文章还预测，未来模型卡可能彻底不再标注知识截止日期，因为权重中存储的知识可能以“年”而不是“周”的尺度过时。

hackernews · hruvhwe · 8月16日 19:04 · [社区讨论](https://news.ycombinator.com/item?id=49322695)

**背景**: 传统大语言模型在预训练阶段直接把事实存储在参数里，因此它们有知识截止日期，也容易对过时或缺失的信息产生幻觉。检索增强生成（RAG）通过让模型在回答问题时从外部知识库检索相关文档来解决这一问题。工具调用则更进一步，让模型可以调用外部 API、计算器、代码解释器或搜索引擎，而不是只依赖内部知识。这些背景解释了为什么文章的观点代表了一种值得关注的架构转变。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Retrieval-augmented_generation">Retrieval - augmented generation - Wikipedia</a></li>
<li><a href="https://aws.amazon.com/what-is/retrieval-augmented-generation/">What is RAG ? - Retrieval - Augmented Generation AI Explained - AWS</a></li>
<li><a href="https://arxiv.org/abs/2307.16789">[2307.16789] ToolLLM: Facilitating Large Language Models to Master 16000+ Real-world APIs</a></li>

</ul>
</details>

**社区讨论**: 评论者大多持有建设性的态度：有人赞同文章中关于模块化、可插拔知识库的设想，也欣赏像 Cactus 的 14 MB 工具调用模型 Needle 这样的小模型。也有人质疑文章的时效性，指出 SimpleQA 已经很久没有更新，Gemini 2.5 Pro 也已是十六个月前的旧模型；还有人提出哲学层面的疑问，认为在讨论历史和人类群体行为时，推理与事实可能根本无法真正分离。

**标签**: `#AI`, `#LLM`, `#knowledge bases`, `#tool use`, `#model architecture`

---

<a id="item-3"></a>
## [Cloudflare 在切换 DNS 后悄悄注入分析脚本](https://news.ycombinator.com/item?id=49322107) ⭐️ 8.0/10

用户为在子域名上使用 R2 存储而将域名服务器切换到 Cloudflare 后，Cloudflare 自动在其原本无 JavaScript、纯 HTML 的网站上注入了分析脚本。该脚本只能通过 Analytics 仪表盘发现，并且需要用户手动关闭。 这种默认开启、需要用户手动退出的行为会改变网站行为并注入第三方代码，可能侵犯用户隐私，影响 Web 开发者和注重隐私的用户。同时它也引发了行业内关于遥测功能应默认开启还是默认关闭的讨论。 注入的脚本是来自 static.cloudflareinsights.com 的模块脚本，带有完整性哈希和包含站点 token、版本等信息的 data-cf-beacon 属性。有评论者指出，只有通过 Cloudflare 代理终止 HTTPS 时才会发生注入；仅使用 DNS 的站点并未启用 Web Analytics。

hackernews · stagas · 8月16日 17:49

**背景**: Cloudflare 是一家主要的 CDN 和反向代理服务商，同时提供 DNS、边缘计算（Workers）和对象存储（R2）。Cloudflare Web Analytics 是一项免费、注重隐私的分析服务，当网站流量经过 Cloudflare 代理时，Cloudflare 可以自动向站点注入该服务。这一背景说明，注入行为与代理模式有关，而非仅 DNS 接入的站点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cloudflare,_Inc.">Cloudflare, Inc.</a></li>
<li><a href="https://www.cloudflare.com/web-analytics/">Cloudflare Web Analytics | Cloudflare</a></li>
<li><a href="https://developers.cloudflare.com/r2/">Overview · Cloudflare R2 docs</a></li>

</ul>
</details>

**社区讨论**: 有评论者建议使用 CSP meta 标签来阻止注入的脚本，也有人确认看到了包含哈希和 token 的具体脚本，还有多位用户质疑发帖者使用的是代理模式而非仅 DNS 模式，因为仅 DNS 的域名并未启用 Web Analytics。整体上，大家对该默认开启的行为持批评态度。

**标签**: `#Cloudflare`, `#privacy`, `#analytics`, `#DNS`, `#web`

---

<a id="item-4"></a>
## [Qwen 3.8 27B 表现出色，但默认过度思考](https://simonwillison.net/2026/Aug/16/qwen-38-27b/) ⭐️ 8.0/10

阿里巴巴 Qwen 实验室本周五发布了 Qwen 3.8 27B，这是一款采用 Apache 2 许可证、具备视觉能力的 27B 参数大模型。Simon Willison 在本地硬件上测试后认为它输出质量优秀，但默认的 xhigh 推理强度会让模型在简单问题上过度思考。 此次发布增强了开源权重大模型生态，把具有竞争力的视觉能力带到可在笔记本上运行的尺寸。它默认过度思考的问题也凸显出行业日益严峻的挑战：如何在本地部署中平衡推理质量与延迟、算力成本。 Qwen 自报的基准测试显示，该模型相比 Qwen 3.6 27B 以及闭权重的 Qwen 3.7-Plus 均有提升。测试中，在默认 xhigh 设置下生成一张鹈鹕骑自行车的 SVG 花了 21 分钟，消耗 22,276 个推理 token，因此需要把 LM Studio 默认的 8,192 token 上下文限制提高到 262,144。

rss · Simon Willison · 8月16日 22:00

**背景**: Qwen 3.8 27B 这类开放权重模型会在宽松许可证下发布可下载的权重，但与完全开源项目不同，通常不公开训练数据或完整训练代码。这类模型通常支持 reasoning\_effort（推理强度）或测试时计算量控制，用更长的思维链推理换取更高准确率；当设置过高时，模型会在简单任务上“过度思考”，生成冗长而不必要的推理过程，增加延迟和成本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2508.17627v1">Stop Spinning Wheels: Mitigating LLM Overthinking via Mining Patterns for Early Reasoning Exit</a></li>
<li><a href="https://github.com/Eclipsess/Awesome-Efficient-Reasoning-LLMs">GitHub - Eclipsess/Awesome-Efficient-Reasoning-LLMs: [TMLR 2025] Stop Overthinking: A Survey on Efficient Reasoning for Large Language Models · GitHub</a></li>
<li><a href="https://theplanettools.ai/blog/closed-vs-open-weight-ai-models-how-to-choose-2026">Closed vs Open - Weight AI: How to Actually... | ThePlanetTools.ai</a></li>

</ul>
</details>

**标签**: `#LLM`, `#Qwen`, `#AI`, `#open-source`, `#benchmarks`

---

<a id="item-5"></a>
## [PJM 建模错误浪费 120 亿美元用户资金](https://newsletter.semianalysis.com/p/12b-of-us-ratepayers-money-wasted) ⭐️ 8.0/10

一项调查揭示，PJM 电网规划中的建模错误浪费了 120 亿美元的用户资金，且该组织有可能重蹈覆辙。SemiAnalysis 发布的报告指出，PJM 一直过度采购电力发电能力，有时甚至超出所需的两倍。 这很重要，因为电网运营中的建模错误可能会将数十亿美元的用户资金浪费在多余的发电容量上，推高 12 个州及华盛顿特区的电费。这也引发了对美国最大区域性输电组织（RTO）可靠性和透明度的担忧。 这一错误似乎与 PJM 使用的安全约束经济调度（SCED）和生产成本模型有关，这些模型旨在找到运行电网成本最低的方式。当模型假设有误时，就会导致长期过度采购发电容量。

rss · Semianalysis · 8月16日 22:27

**背景**: PJM Interconnection（PJM 互联）是一家区域性输电组织，负责管理美国 12 个州和华盛顿特区约 6700 万人的电网，是美国最大的 RTO。电网运营商使用生产成本模型和安全约束经济调度（SCED）来决定哪些电厂应以最低成本运行以满足需求。模型中的缺陷可能导致造成数十亿美元浪费的决策，正如这项调查所揭示的那样。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/PJM_Interconnection">PJM Interconnection - Wikipedia</a></li>
<li><a href="https://www.ncelenviro.org/articles/understanding-rtos-the-pjm-interconnection/">Understanding RTOs: the PJM Interconnection | National Caucus of...</a></li>
<li><a href="https://blog.ucs.org/mark-specht/grid-modeling-overview-four-types-of-models-guiding-the-transition-to-clean-electricity/">Grid Modeling Overview: Four Types of Models Guiding the Transition...</a></li>

</ul>
</details>

**标签**: `#grid modeling`, `#PJM`, `#energy infrastructure`, `#cost waste`, `#policy`

---

<a id="item-6"></a>
## [SSOG-Attention：用可分离高斯和实现亚二次注意力，替代 SDPA](https://www.reddit.com/r/MachineLearning/comments/1vpt6ay/ssogattention_sum_of_separable_gaussians_as_a/) ⭐️ 8.0/10

作者提出了 SSOG-Attention，一种新的注意力机制，用可分离高斯和替代标准缩放点积注意力（SDPA），将复杂度降至 O\(N·√N·d\)。实验表明，它在 CIFAR-100 上优于 SDPA，在 ImageNet 上性能相当且收敛更快。 这具有重要意义，因为 SDPA 的二次复杂度是 Transformer 扩展到长序列和高分辨率输入的主要瓶颈。如果得到验证，SSOG-Attention 有望让视觉和语言模型中的注意力机制大幅提升效率和内存友好性。 SSOG 为每个头学习少量高斯原子，并根据查询令牌对其进行几何引导；通过将原子分解为可分离和，避免了显式计算所有查询-键相似度。该方法在更大规模下速度和内存效率显著提升，作者提供了代码和博客文章。

reddit · r/MachineLearning · /u/4rtemi5 · 8月16日 10:06

**背景**: 缩放点积注意力（SDPA）计算所有令牌对之间的相似度，产生 O\(N²·d\)的时间和内存开销，这在长序列下变得难以承受。亚二次注意力方法旨在通过稀疏性、低秩近似或核技巧来降低这一复杂度类。SSOG-Attention 应用可分离高斯和，其中每个高斯是各维度上的张量积，从而无需显式构造完整的 N×N 注意力矩阵即可构建注意力分布。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/4rtemi5/ssog">GitHub - 4rtemi5/ssog: SSOG - Attention : Near-linear Visual-Attention...</a></li>
<li><a href="https://news.ycombinator.com/item?id=49318407">SSOG : Near linear Visual- Attention that doesn&#x27;t score... | Hacker News</a></li>
<li><a href="https://www.emergentmind.com/topics/sub-quadratic-self-attention">Sub - quadratic Self- Attention</a></li>

</ul>
</details>

**标签**: `#Attention`, `#Efficient Transformers`, `#Machine Learning`, `#Computer Vision`, `#Complexity Reduction`

---

<a id="item-7"></a>
## [重新审视 ECA-Net：跨通道交互的核心假设并不成立](https://www.reddit.com/r/MachineLearning/comments/1vptaw9/revisiting_the_efficient_channel_attention_paper/) ⭐️ 8.0/10

在一篇 Reddit 评论文章中，作者重新审视了 ECA-Net 论文，认为其关于跨通道交互的核心假设是错误的；在六子国际象棋残局表上的实验显示，卷积核大小为 1 的 ECA 准确率达 96.61%，与卷积核大小为 3 时的 96.68%几乎相当，削弱了该论文声称的关键要素。 ECA-Net 已被引用约 12,000 次，并被广泛用于改进卷积神经网络，因此这一批评可能促使研究者重新评估通道注意力的工作原理，并推动更严谨的模块设计。 作者还指出，在通道维度上执行一维卷积在概念上等同于把卷积神经网络应用于无序的表格型数据，因为通道没有空间拓扑结构。实验从完整的 3.7 万亿个六子残局位置中随机采样，避免了数据集偏差，并对比了 SE（96.17%）和逐通道门控（96.65%）等基线。

reddit · r/MachineLearning · /u/arkuto · 8月16日 10:13

**背景**: 像 Squeeze-and-Excitation（SE）和 Efficient Channel Attention（ECA）这样的注意力机制，通过学习每个通道的权重来重新校准特征图。SE 使用一个降维的全连接瓶颈层，而 ECA 直接用一维卷积在通道均值上操作，以捕捉局部跨通道交互，其论文声称这种交互是关键因素。这位批评者反驳说，卷积依赖于具有空间/时间结构的数据，而通道维度更像是一个无序的特征向量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/1910.03151">[1910.03151] ECA -Net: Efficient Channel Attention for Deep...</a></li>
<li><a href="https://www.emergentmind.com/topics/efficient-channel-attention-eca-mechanisms">Efficient Channel Attention Mechanisms</a></li>
<li><a href="https://github.com/BangguWu/ECANet">GitHub - BangguWu/ECANet: Code for ECA-Net: Efficient Channel ...</a></li>

</ul>
</details>

**标签**: `#deep learning`, `#attention mechanisms`, `#computer vision`, `#research critique`

---

<a id="item-8"></a>
## [Anthropic 第二季营收超 115 亿美元，同比增 14 倍，IPO 在即](https://www.cnbc.com/2026/08/15/anthropic-revenue-jumps-to-over-11point5-billion-in-q2-report.html) ⭐️ 8.0/10

彭博社援引文件称，Anthropic 第二季初步营收超过 115 亿美元，同比增长逾 14 倍（去年同期为 7.87 亿美元），也高于 2026 年第一季的 47.3 亿美元。当季调整后营业利润也转正。 对于领先的 AI 公司而言，这是一个重大财务里程碑，表明 AI 需求的激增正在转化为爆发式的商业收入。随着经营利润转正以及今秋可能启动 IPO，这一消息可能重塑市场对 AI 初创公司估值和公开市场投资的预期。 报道指出，这些数字是初步数据，仍可能被调整。Anthropic 正筹备一项大型 IPO，最快可能在今年秋季启动。

telegram · zaihuapd · 8月16日 07:26

**背景**: Anthropic 是领先的私营 AI 公司之一，其财务表现被视为衡量 AI 行业商业需求的重要风向标。对于一家筹备 IPO 的私营公司而言，强劲的营收增长和调整后营业利润转正是面向潜在投资者的关键信号。报道指出这些数字为初步数据，在最终结果发布前仍可能调整。

**标签**: `#Anthropic`, `#AI industry`, `#Revenue`, `#IPO`, `#AI startups`

---