---
layout: default
title: "Horizon Summary: 2026-08-29 (ZH)"
date: 2026-08-29
lang: zh
---

> 从 31 条内容中筛选出 10 条重要资讯。

---

1. [智谱开源 GLM-5.3，编程与智能体能力大幅提升](#item-1) ⭐️ 9.0/10
2. [Triton 3.8.0 发布：新增聚合类型与 tl.topk 选项](#item-2) ⭐️ 8.0/10
3. [键盘驱动的图形界面：关于无障碍与高级用户的争论](#item-3) ⭐️ 8.0/10
4. [Htmx 4.0 发布，带来新特性和兼容性改进](#item-4) ⭐️ 8.0/10
5. [OpenAI 因模型蒸馏风险限制被 SpaceX 收购后的 Cursor](#item-5) ⭐️ 8.0/10
6. [美国将意大利托管组织 Autistici/Inventati 列为恐怖实体实施制裁](#item-6) ⭐️ 8.0/10
7. [仅凭漏洞传闻即可催生利用工具，维护者不堪重负](#item-7) ⭐️ 8.0/10
8. [《盗梦空间》风格的弯曲地图用于逐向导航](#item-8) ⭐️ 8.0/10
9. [在 RP2350 上运行微型潜流 Transformer，生成 128x128 人脸图像](#item-9) ⭐️ 8.0/10
10. [腾讯发布 Hy4 预览版，盲测小幅领先对手](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [智谱开源 GLM-5.3，编程与智能体能力大幅提升](https://huggingface.co/zai-org/GLM-5.3) ⭐️ 9.0/10

GLM-5.3 现已以开放权重形式发布，权重已在 Hugging Face 开放下载。官方称其代码能力比 GLM-5.2 提升 50%，并在 Terminal Bench 3.0 与 Agents&\#x27; Last Exam 上取得开源模型最优结果。 这是一次重要的开放权重大模型发布，增强了可下载模型的生态，使其有能力与领先闭源模型竞争。它为开发者和研究人员在编程和智能体任务上提供了一个高性能、可运行的选择，社区反响显示它可能改变部分用户对其它开源或商业模型的取舍。 GLM-5.3 与 GLM-5.2 共用同一基础模型，全部提升来自后训练。官方许可允许个人与中小企业自由使用、微调和商用，但对连续 12 个月营收超过 100 亿美元且对外提供特定模型服务的公司设有额外限制；API 用户从旧版迁移时还需调整 thinking/reasoning 设置。

hackernews · jeudesprits · 8月28日 15:20 · [社区讨论](https://news.ycombinator.com/item?id=49479878)

**背景**: 开放权重模型是指将训练后的参数公开释出的大语言模型，任何人都能下载、运行和修改，无需通过厂商的 API。GLM 是智谱 AI（Z.ai）开发的大模型系列，GLM-5.3 是最新的开放权重版本，定位于强编程与智能体能力。Hugging Face 发布说明称，它在 Terminal Bench 3.0、Agents&\#x27; Last Exam 等公开基准上取得了开源模型最优成绩。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/zai-org/GLM-5.3">zai-org/ GLM - 5 . 3 · Hugging Face</a></li>
<li><a href="https://docs.z.ai/guides/llm/glm-5.3">GLM - 5 . 3 - Overview - Z.AI DEVELOPER DOCUMENT</a></li>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>

</ul>
</details>

**社区讨论**: 评论区整体反馈积极，不少人分享了本地使用体验：有用户认为它在两节点 DGX Spark 上“相当惊艳”，具备 DeepSeek Flash 4 所欠缺的直觉；也有人觉得用起来像 Opus 4.8。一些用户将其视为效率与能力之间的理想折中，也有人借机追问：既然开源模型已如此强大，过去以安全为由不发布 GPT-3 的决定是否还站得住脚。

**标签**: `#LLM`, `#open-weights`, `#AI`, `#GLM`, `#model-release`

---

<a id="item-2"></a>
## [Triton 3.8.0 发布：新增聚合类型与 tl.topk 选项](https://github.com/triton-lang/triton/releases/tag/v3.8.0) ⭐️ 8.0/10

Triton 3.8.0 正式发布，引入了通过 @triton.aggregate 和 @gluon.aggregate 公开的聚合类型、tl.topk 新增 descending 参数，以及针对 NVIDIA 和 AMD/HIP 后端的众多编译器和后端改进。该版本还包含破坏性变更，以及针对 IEEE 舍入、NaN 处理和 block-pointer 填充的 bug 修复。 Triton 是 ML/系统生态中广泛使用的 GPU 编程语言与编译器，为 PyTorch 等框架提供内核支持。本次发布的聚合类型提升了代码可读性和参数传递效率，tl.topk 的增强则扩展了采样和搜索内核的可用性，使更广泛的 GPU 计算社区受益。 聚合类型现在支持字段继承、默认值、自动生成的构造函数、不可变实例以及 aggregate\_replace\(\)。tl.topk 新增 descending 参数（默认 True）以返回最小值；张量描述符现在可以位于元组值内核参数中传入，解释器也增加了对 tl.dot\_scaled 的支持。本次版本还包含破坏性变更以及更新了 LLVM 修订版本，修复了 GFX950 BF16 误编译问题。

github · warrendeng · 8月28日 18:25

**背景**: Triton 是一种开源的领域特定语言和编译器，用于编写 GPU 内核，其类 Python 语法抽象了内存布局和同步等底层细节。Gluon 是构建在同一编译器栈上的更低级语言，让用户显式控制布局，与 Triton 的自动优化形成互补。聚合类型此前属于内部 API，本次在 Triton 和 Gluon 中均成为公开 API，简化了向 JIT 编译内核传递结构化数据的过程。tl.topk 是一种标准操作，用于沿指定维度选取最大的 k 个元素或最小的 k 个元素，常用于采样和 top-k 解码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://triton-lang.org/main/python-api/generated/triton.language.topk.html">triton .language. topk — Triton documentation</a></li>
<li><a href="https://triton-lang.org/main/getting-started/tutorials/gluon/intro.html">Introduction to Gluon — Triton documentation</a></li>
<li><a href="https://www.lei.chat/posts/gluon-explicit-performance/">Gluon : Explicit Performance | Lei.Chat()</a></li>

</ul>
</details>

**标签**: `#triton`, `#gpu`, `#compiler`, `#release`, `#ml`

---

<a id="item-3"></a>
## [键盘驱动的图形界面：关于无障碍与高级用户的争论](https://ckardaris.com/blog/2026/08/28/keyboard-driven-guis.html) ⭐️ 8.0/10

一篇博客文章主张图形界面应完全由键盘驱动，在 Hacker News 上引发了热烈讨论（666 分，324 条评论）。讨论聚焦于无障碍性、高级用户和用户体验的权衡。 这场辩论凸显了高级用户效率与主流易用性之间的张力，促使工程师和设计师将键盘支持视为核心需求。其结果影响着残障人士以及偏好以键盘为中心工作流程的用户所使用软件的无障碍程度。 评论者强调键盘导航对运动障碍用户至关重要，但也指出可发现性和学习曲线仍是挑战。一位评论者区分了“键盘驱动”与仅仅“键盘兼容”，认为仅分配快捷键是不够的。

hackernews · ckardaris · 8月28日 15:17 · [社区讨论](https://news.ycombinator.com/item?id=49479837)

**背景**: 键盘驱动的图形界面允许用户通过键盘快捷键和焦点导航完成所有交互，而无需鼠标或触摸屏。这对于 ADA 等无障碍合规至关重要，也是高级用户的普遍期望。设计此类界面需要仔细关注焦点管理、快捷键可发现性和视觉指示。Hacker News 的讨论反映了行业内关于无障碍功能是否应强制用于所有软件的更广泛辩论。

**社区讨论**: 评论者普遍认为键盘无障碍性很重要，但对于每个图形界面是否都必须完全由键盘驱动存在分歧。一些人认为高级用户的需求与普通用户不同，强制键盘驱动设计可能会损害主流可用性。

**标签**: `#accessibility`, `#keyboard-driven UI`, `#UX`, `#software design`, `#HN discussion`

---

<a id="item-4"></a>
## [Htmx 4.0 发布，带来新特性和兼容性改进](https://four.htmx.org/announcements/2026-08-28-htmx-4.0.0-is-released) ⭐️ 8.0/10

Htmx 4.0.0 于 2026 年 8 月 28 日发布，引入了新特性和兼容性改进，包括用于解决与 Alpine.js 兼容性问题的 hx-alpine-compat 属性。此次发布引发了社区的热烈讨论，目前有 138 条评论和 565 个点赞。 这个以超媒体为导向的流行库的重大版本发布，强化了向更简单的服务器端渲染方法发展的趋势，为重型的 JavaScript 框架提供了一种替代方案。社区的热烈反应突显了 htmx 在前端生态中的影响力，以及围绕其角色的持续争论。 Htmx 仍然保持小巧（压缩后约 16k）、无依赖且可扩展，通过 HTML 属性提供 AJAX、CSS 过渡、WebSocket 和 Server-Sent Events。新的 hx-alpine-compat 功能解决了 htmx 与 Alpine.js 之间的兼容性问题，同时该库继续支持渐进增强。

hackernews · rmsaksida · 8月28日 13:28 · [社区讨论](https://news.ycombinator.com/item?id=49478178)

**背景**: Htmx 是一个 JavaScript 库，通过属性扩展 HTML，让开发者利用超文本的简洁性来构建现代用户界面，无需复杂的状态管理或水合（hydration）。它遵循超媒体方法，服务器返回 HTML 片段来更新页面的特定部分而不需要整体刷新，因此成为偏好服务器端渲染的开发者的热门选择。该库以小巧、无依赖和可扩展著称，并支持渐进增强等技术，在 JavaScript 禁用时也能优雅降级。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Htmx">htmx - Wikipedia</a></li>
<li><a href="https://htmx.org/">htmx - high power tools for html</a></li>
<li><a href="https://htmx.org/docs/">htmx ~ Documentation</a></li>

</ul>
</details>

**社区讨论**: 社区反应总体积极，用户表达兴奋之情并分享实际用例，如将 Go、htmx 和 SQLite 结合使用，还有人称赞该库的简洁性和自然发展。然而也有相反观点：一位评论者指出，对于习惯 .NET API 后端和 Angular 的开发者来说，htmx 可能会让事情变得复杂；另一位则提到 alpine-ajax 是一个更小的替代品，满足了他的需求。HTMX 的 CEO 也在此讨论中公开了自己的身份，为话题增添了透明度。

**标签**: `#htmx`, `#javascript`, `#web development`, `#hypermedia`, `#release`

---

<a id="item-5"></a>
## [OpenAI 因模型蒸馏风险限制被 SpaceX 收购后的 Cursor](https://openai.com/index/our-decision-on-cursor-following-its-acquisition-by-spacex/) ⭐️ 8.0/10

OpenAI 已决定在 Cursor 被 SpaceX 收购后限制其对 OpenAI 模型的使用，理由是担心模型蒸馏风险。此举实际上限制了 AI 编程助手 Cursor 使用 OpenAI 专有模型的方式。 这一决定重塑了 AI 编程工具的竞争格局，依赖 Cursor 搭配 OpenAI 模型的开发者可能会失去该集成。这也表明，当转售方被竞争对手模型提供商收购时，主要 AI 提供商会积极执行服务条款。 OpenAI 提到了模型蒸馏方面的担忧，即利用较大模型的输出来微调较小模型的做法。Cursor 此前一直在转售第三方 API 的使用权，而其被 SpaceX（一个竞争性模型提供商）收购触发了这一限制。

hackernews · meetpateltech · 8月29日 01:47 · [社区讨论](https://news.ycombinator.com/item?id=49486172)

**背景**: Cursor 是一家成立于 2022 年的 AI 驱动代码编辑器和开发环境，以允许开发者通过自然语言指令编写代码而闻名；其估值达到 293 亿美元，年经常性收入超过 30 亿美元。模型蒸馏是指通过在较大模型的输出上进行微调，将知识从大型高性能模型转移到更小、更便宜的模型的过程，许多 AI 公司出于竞争原因禁止这种做法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cursor_%28code_editor%29">Cursor (company) - Wikipedia</a></li>
<li><a href="https://openai.com/index/api-model-distillation/">Model Distillation in the API - OpenAI</a></li>
<li><a href="https://cursor.com/">AI Coding Agent for Building Ambitious Software | Cursor</a></li>

</ul>
</details>

**社区讨论**: 评论者大多表示他们预见到了这一点，并指出 Cursor 转售他人 API 的商业模式不可持续。有人指出，Anthropic 此前已因类似的服务条款违规行为封禁了 xAI；另一位 Cursor 和 Claude 订阅用户表示，此举将促使他们转回 Anthropic。一些用户表示，他们对在 Cursor 中使用 Grok 或 Composer 感到满意，并不需要 OpenAI 模型。

**标签**: `#AI`, `#OpenAI`, `#Cursor`, `#SpaceX`, `#Model Governance`

---

<a id="item-6"></a>
## [美国将意大利托管组织 Autistici/Inventati 列为恐怖实体实施制裁](https://www.inventati.org/) ⭐️ 8.0/10

2026 年 8 月下旬，美国国务院和财政部将意大利的 Autistici/Inventati（A/I）集体（其运营 noblogs.org 博客平台）列为“特别指定的全球恐怖分子”（SDGT），并对这一基础设施提供商实施制裁。 这是一个重大升级，因为一个非暴力的基础设施提供商被贴上了恐怖组织标签，为隐私工具、言论自由平台和更广泛的互联网生态创下了令人不寒而栗的先例。它可能使托管商、开发者和用户因担心遭受类似制裁而不敢提供或使用保护隐私的服务。 该指定明确点名 Autistici/Inventati 集体，禁止美国人与之进行交易；该集体的网站（包括 autistici.org 和 noblogs.org）已部分无法访问或完全下线。批评者指出，将 A/I 与恐怖主义联系起来的透明证据不足，认为该指定似乎源于其长期为活动人士提供通讯服务的历史。

hackernews · exiguus · 8月28日 12:58 · [社区讨论](https://news.ycombinator.com/item?id=49477854)

**背景**: Autistici/Inventati（A/I）是一个非营利集体，2001 年由来自自治反资本主义运动的个人和团体在米兰创立，为活动人士和公民社会组织提供电子邮件、网站托管和博客工具。Noblogs.org 是 A/I 运营的博客平台，托管了大量独立媒体和社会运动网站，包括与 Indymedia 相关的项目。此次制裁将“提供通信基础设施”本身视为对恐怖主义的支持，这与以往通常只针对与暴力集团有直接关联的个人或组织的制裁有所不同。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.autistici.org/">autistici.org - Welcome to Autistici / Inventati</a></li>
<li><a href="https://crimethinc.com/2026/08/27/us-government-designates-host-of-noblogsorg-a-global-terrorist">US Government Designates Host of NoBlogs . org a &quot;Global Terrorist&quot;</a></li>
<li><a href="https://www.radiorebelde.cu/english/u-s-designates-palestine-action-masar-badil-and-autistici-inventati-as-terrorist-groups-26082026/">U.S. Designates Palestine Action, Masar Badil, and Autistici Inventati ...</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍感到震惊，认为将基础设施提供者定性为恐怖实体是前所未有的先例，可能威胁到 I2P、Monero、Veilid、Tox 和 Signal 等项目。有人质疑 A/I 的实际性质，并指出难以核实其与库尔德工人党（PKK）的联系，还有人补充了 A/I 在 2001 年热那亚抗议等运动中的历史背景。总体而言，讨论对政府行动及其对隐私基础设施的寒蝉效应持批评态度。

**标签**: `#sanctions`, `#privacy`, `#hosting`, `#civil liberties`, `#surveillance`

---

<a id="item-7"></a>
## [仅凭漏洞传闻即可催生利用工具，维护者不堪重负](https://anil.recoil.org/notes/rumour-is-the-exploit) ⭐️ 8.0/10

文章认为，如今仅凭关于漏洞的传闻就足以引发利用代码的发现，AI 辅助工具大大加速了这一过程。这导致安全披露数量激增，也给开源维护者带来了巨大的额外负担。 基于大语言模型的代码分析与自动漏洞利用生成相结合，意味着攻击者能比以往更快地将模糊线索武器化。开源维护者面临不可持续的报告洪流，威胁着整个安全生态的响应能力。 以 rclone 为例，该项目在最初 10 年里共收到约 20 份 GitHub 安全披露，而最近一个月就处理了超过 40 份，其中约 75%确实含有需要处理的问题。AI 模型如今还能从日常提交中识别隐藏的修复行为，并辅助补丁对比分析，降低了漏洞利用的技术门槛。

hackernews · avsm · 8月28日 15:58 · [社区讨论](https://news.ycombinator.com/item?id=49480466)

**背景**: 漏洞研究历来包括从补丁差异、提交消息或随口一句话中推导利用方法，但这需要相当高的技术水平。大语言模型让这些技术变得对更多参与者触手可及，能够大规模地进行自动漏洞利用生成和漏洞发现。DeepBinDiff 和 ChatGPT 等工具被用于 AI 辅助补丁差异分析，以识别隐藏修复。这使得瓶颈从发现漏洞转移到了修复漏洞以及快速部署补丁上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2505.01065">Good News for Script Kiddies? Evaluating Large Language Models ...</a></li>
<li><a href="https://www.sans.org/cyber-security-courses/offensive-ai-attack-tools-techniques">SEC535: Offensive AI - Attack Tools and Techniques | SANS ...</a></li>
<li><a href="https://github.com/huhusmang/Awesome-LLMs-for-Vulnerability-Detection">GitHub - huhusmang/Awesome-LLMs-for- Vulnerability -Detection: The...</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认同文章论点，并分享维护者亲身经历与不同视角。一位开源维护者报告安全披露数量激增，约 75%有实际价值，耗费大量时间；另一些人则认为真正的问题在于组织层面缺乏修复意愿，以及即时打补丁并不现实；还有人指出技术本身并不新，新的只是漏洞利用的大众化。

**标签**: `#security`, `#open source`, `#AI-assisted exploitation`, `#vulnerability disclosure`, `#maintainer burden`

---

<a id="item-8"></a>
## [《盗梦空间》风格的弯曲地图用于逐向导航](https://www.orbify.eu/demo/) ⭐️ 8.0/10

Orbify 发布了一款《盗梦空间》风格的弯曲地图演示，用于逐向导航，将前方道路弯折成透视曲线。这一可视化在 Hacker News 上引发了大量讨论，获得了 147 条评论和 447 个点赞。 这款演示为传统 2D 或 3D 导航地图提供了一种极具视觉冲击力的替代方案，可能改变驾驶者对前方转弯的感知方式。尽管只是一个概念验证，它已引发了关于可用性的热烈讨论，表明人们对新颖地图可视化有强烈兴趣。 该演示是概念验证而非成品，可在 orbify.eu/demo 上查看。批评者指出，在转弯前一刻，视图几乎不提供前方路线的信息，导致连续转弯难以导航；有人建议旋转视角或将急转弯展开以进行补偿。

hackernews · smoser · 8月28日 12:29 · [社区讨论](https://news.ycombinator.com/item?id=49477564)

**背景**: 这种视觉风格呼应了电影《盗梦空间》中折叠城市的场景，也可以追溯到更早的地图艺术，如 Berg London 2009 年的“Here and There”海报。传统逐向导航地图保持平面并跟随车辆移动，而这个演示将前方道路投影成弯曲的透视表面，虽然更有电影感，但可能遮挡即将到来的转弯信息。该演示似乎采用高斯泼溅（Gaussian-splat）渲染，带来交互式、照片级的效果。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://lemmy.world/post/51241241">Inception - style curved map for turn-by-turn directions - Lemmy.World</a></li>
<li><a href="https://googlemapsmania.blogspot.com/2026/08/bending-maps-inception-style.html">Bending Maps , Inception Style</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞该演示是“纯 Bret-Victorian 式的魔法”和出色的概念验证，但许多人对其实用性提出质疑。主要担忧包括转弯前后视野受限、可预测距离不稳定以及可能引起晕车，有人甚至调侃说“恶心即服务”（Nausea as a Service）。

**标签**: `#UI/UX`, `#Maps`, `#Visualization`, `#Navigation`, `#Hacker News`

---

<a id="item-9"></a>
## [在 RP2350 上运行微型潜流 Transformer，生成 128x128 人脸图像](https://www.reddit.com/r/MachineLearning/comments/1w10tax/i_implemented_a_very_tiny_image_generation_model/) ⭐️ 8.0/10

开发者（u/cpldcpu）在 RP2350 微控制器上实现了一个参数量仅 240 万至 400 万的潜流 Transformer（latent flow transformer），可在约 20 秒内生成 128×128 的人脸图像。模型使用 int8 量化并完全在设备端运行，推理引擎通过 DMA 从闪存流式加载权重，同时计算上一层。 这表明现代扩散式图像生成模型可以被压缩到约 1 美元的微控制器上运行，将边缘 AI 的能力从分类扩展到生成任务。它是面向设备端生成、隐私保护 AI 与超低功耗机器学习的一个重要概念验证。 该模型是一个 12 层潜流 Transformer，使用 AdaLN-Zero 归一化机制进行类别/时间步条件控制，并支持无分类器引导（CFG），显著提升了生成质量。它采用 ReLU²激活函数提高稀疏性，使推理引擎能够跳过部分计算；生成结果可显示在显示器上或通过 USB 传输。

reddit · r/MachineLearning · /u/cpldcpu · 8月28日 19:48

**背景**: 潜流 Transformer（Latent Flow Transformer, LFT）是一种较新的架构，它用通过学习得到的传输算子替代一整块层，并通过流匹配（flow matching）训练，从而大幅压缩生成模型。流匹配与扩散模型都学习如何把噪声样本逐步变换为数据；AdaLN-Zero 则是扩散 Transformer（如 DiT）中常用的零初始化自适应归一化条件机制。RP2350 是树莓派公司推出的双核微控制器（可选 Arm Cortex-M33 或 Hazard3 RISC-V 内核），用于 Raspberry Pi Pico 2 开发板，价格低廉、自带板载闪存。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2505.14513">Abstract page for arXiv paper 2505.14513: Latent Flow Transformer</a></li>
<li><a href="https://en.wikipedia.org/wiki/RP2350">RP2350</a></li>
<li><a href="https://openreview.net/forum?id=E4roJSM9RM">Unveiling the Secret of AdaLN-Zero in Diffusion Transformer</a></li>

</ul>
</details>

**标签**: `#edge-ai`, `#microcontrollers`, `#image-generation`, `#model-compression`, `#efficient-inference`

---

<a id="item-10"></a>
## [腾讯发布 Hy4 预览版，盲测小幅领先对手](https://mp.weixin.qq.com/s/ymr3X878B8oa2XP15CH8TQ) ⭐️ 8.0/10

2026 年 8 月 28 日，腾讯发布了迄今最强的开源模型 Hy4 preview。这款混合专家（MoE）模型总参数量为 770B，活跃参数 49B，上下文窗口为 1M token，在 203 个工程任务的盲测中取得 2.99 分，略高于 GLM-5.3（2.92）和 Kimi K3（2.94）。 此次发布加剧了中国 AI 实验室在开源大模型领域的竞争，表明腾讯能够比肩甚至小幅超越智谱 GLM 和月之暗面 Kimi 等同行。1M token 的上下文窗口以及对长周期软件工程和科学研究的侧重，瞄准了实际生产力场景。 该模型已上线腾讯云、GitHub、Hugging Face、ModelScope、AtomGit 和 OpenRouter 等渠道，API 定价为每 1M 输入 tokens 0.834 美元、每 1M 输出 tokens 2.501 美元。由于是预览版，最终版本的基准分数和可用性可能发生变化。

telegram · zaihuapd · 8月28日 06:11

**背景**: 混合专家（MoE）是一种架构，对于每个输入 token 只激活模型参数的一个子集，从而在不按比例增加计算成本的情况下扩大总参数量。在 Hy4 preview 中，每个 token 只激活 770B 总参数中的 49B。盲测评估在不让评测者知道输出来自哪个模型的情况下展示模型输出，以减少品牌偏差；这类测试正越来越多地用于比较 LLM 的质量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2507.11181">[2507.11181] Mixture of Experts in Large Language Models A Closer Look into Mixture-of-Experts in Large Language Models Mixture of Experts Explained - Hugging Face Applying Mixture of Experts in LLM Architectures | NVIDIA ... A Closer Look into Mixture-of-Experts in Large Language Models Understanding Mixture of Experts (MoE): The Architecture ...</a></li>
<li><a href="https://www.f22labs.com/blogs/active-vs-total-parameters-whats-the-difference/">Active vs Total Parameters: What’s the Difference?</a></li>
<li><a href="https://zylos.ai/research/2026-01-16-llm-evaluation-benchmarking/">LLM Evaluation and Benchmarking 2026 | Zylos Research</a></li>

</ul>
</details>

**标签**: `#AI`, `#LLM`, `#Tencent`, `#open-source`, `#model release`

---