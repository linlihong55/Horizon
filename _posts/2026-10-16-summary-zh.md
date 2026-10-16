---
layout: default
title: "Horizon Summary: 2026-10-16 (ZH)"
date: 2026-10-16
lang: zh
---

> 从 42 条内容中筛选出 5 条重要资讯。

---

1. [Citizen Lab：定向广告被用作零点击雇佣间谍软件的投递管道](#item-1) ⭐️ 9.0/10
2. [Meta 发布 816B 参数开放权重 MoE 模型 Muse Spark Open](#item-2) ⭐️ 8.0/10
3. [Goodfire 的 Nick Cammarata 主张神经网络学到的是干净、可分离的特征](#item-3) ⭐️ 8.0/10
4. [ASML 被曝正在研发混合键合设备](#item-4) ⭐️ 8.0/10
5. [随机神经网络自组装出学习基元，性能逼近反向传播](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Citizen Lab：定向广告被用作零点击雇佣间谍软件的投递管道](https://citizenlab.ca/research/how-discover-tech-turned-targeted-ads-into-a-pipeline-for-spyware/) ⭐️ 9.0/10

Citizen Lab 于 2026 年 10 月 15 日发布题为《揭露 AdFection：Discover-Tech 如何将定向广告变成零点击雇佣间谍软件的投递管道》的报告，指称以色列广告公司 Discover-Tech 投放的定向广告可在无需用户任何交互的情况下，于受害者设备上静默安装雇佣间谍软件。据对该报告的报道，其广告基础设施覆盖了超过 7 万个应用和 12 万多个网站。 据报道，这是首例被确认通过定向广告投递雇佣间谍软件的案例，意味着零点击威胁已从即时通讯应用转移到嵌入在大量日常应用和网站中的广告层。这也对广告技术供应链的责任归属提出尖锐问题，因为广告及其背后的 SDK 几乎是普遍存在且基本不受审计的攻击面。 报道指出，该报告在一定程度上详细记录了基于广告的分发与命令控制（C&amp;amp;C）基础设施，但对究竟是何种机制触发零点击激活则叙述较为模糊，也没有公开点名某一广告网络或某一漏洞是唯一投递途径。据称这些广告可被用于针对特定目标投放间谍软件，说明是选择性而非大规模目标攻击，而受影响的应用与网站数量达到数万级别。

hackernews · jcomp · 10月15日 10:43 · [社区讨论](https://news.ycombinator.com/item?id=50101813)

**背景**: 雇佣间谍软件是出售给政府及其他客户的商业监控软件，通常用于远程入侵手机并窃取消息、位置等数据；苹果等公司会定期向被此类工具攻击的用户发送威胁通知。“零点击”指的是受害者无需点击、下载或点开链接即可被入侵，过去主要通过即时通讯或通信类应用的漏洞实现。广告技术（AdTech）则是把广告投放到应用和网站中的网络、交易平台与软件开发工具包（SDK）生态，并在这一过程中收集用户定向数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://citizenlab.ca/research/exposing-adfection-executive-summary/">Exposing AdFection Executive Summary - The Citizen Lab</a></li>
<li><a href="https://arstechnica.com/security/2026/10/targeted-ads-delivered-0-click-exploits-to-install-mercenary-malware/">Targeted ads delivered 0-click exploits to install mercenary ...</a></li>
<li><a href="https://www.theguardian.com/technology/2026/oct/15/israeli-firm-digital-ads-enabling-installation-of-zero-click-spyware-researchers-say">Online ads weaponised to deliver ‘zero-click’ spyware ...</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论非常热烈且观点分歧明显：一位自称在广告技术行业工作 13 年的工程师认为“零点击”的说法过于煽情，报告对真正的激活机制语焉不详，并强调在高度碎片化的广告技术生态中根本不存在单一可追责的“广告提供商”。另一些评论者则聚焦地缘政治，认为以色列网络安全公司应被视为与国家绑定，并追问以色列为何能成为如此强势的网络强国，也有人只是贴出了 Citizen Lab 原始报告的链接。

**标签**: `#security`, `#spyware`, `#adtech`, `#privacy`, `#surveillance`

---

<a id="item-2"></a>
## [Meta 发布 816B 参数开放权重 MoE 模型 Muse Spark Open](https://research.meta.ai/blog/muse-spark-open) ⭐️ 8.0/10

Meta 发布了 Muse Spark Open，这是一个 816B 参数的混合专家（MoE）开放权重模型，在 Hugging Face 上以 Muse-Spark-Open-816B-A42B 的名称提供，即总参数 816B、每个 token 约激活 42B。Meta 同时发布了构建与部署文档，并宣传该模型经过优化，可在 Mac Studio 等本地硬件上运行。 Meta 推出 816B 级别的开放权重模型对开放权重生态是一大事件，因为它为开发者提供了一个可本地部署、无需依赖托管 API 的大型选择。但据称该模型在 Artificial Analysis 上落后于 Qwen3.8 Flash Next 和 GLM 5.3 Flash 等竞品，因此这次发布与其说是技术飞跃，不如说是 Meta 对自身开放权重战略的一次表态。 从命名看，这是一个稀疏 MoE 架构，总参数 816B、激活参数约 42B；根据社区反馈与 Meta 的部署文档，Meta 在运行器适配上投入颇多，支持范围涵盖 Unsloth 和 MLX。其许可证对多数用途较为宽松，但包含「模型即服务」（Model as a Service）条款：若被许可方及其关联方的总营收超过 2000 万美元，则不得通过 API 或类似接口向第三方转售模型输出。

hackernews · bigwheels · 10月15日 17:47 · [社区讨论](https://news.ycombinator.com/item?id=50107379)

**背景**: 混合专家（MoE）模型把网络拆分为多个被称为「专家」的子网络，并通过路由器为每个 token 只激活最相关的部分，从而在不大幅增加单 token 计算量的前提下把参数量扩展到极大。这也是参数量通常有两个数字的原因：总参数决定存放权重所需的内存，激活参数决定每个 token 消耗的算力。「开放权重」意味着训练好的权重被公开发布，但许可证仍可能限制商业用途——从 Apache 2.0 这类宽松许可，到带有营收门槛和用途限制的自定义许可，形成了不同的光谱。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.f22labs.com/blogs/active-vs-total-parameters-whats-the-difference/">Active vs Total Parameters: What’s the Difference?</a></li>
<li><a href="https://researchaudio.io/p/mixture-of-experts-moe-in-large-language-models">Mixture of Experts ( MoE ) in Large Language Models</a></li>
<li><a href="https://intuitionlabs.ai/articles/open-weight-ai-model-licenses">Open-Weight AI Model Licenses: Commercial Use Rules Explained</a></li>

</ul>
</details>

**社区讨论**: 评论区整体态度较为克制而非惊艳：有人指出该模型性能不及 Qwen3.8 Flash Next 和 GLM 5.3 Flash（两者均可在单台 B300 上运行），并批评 Artificial Analysis 只提供最高推理等级下的对比，而这一等级在高并发生产场景中基本不可用。也有人细读许可证中的「模型即服务」营收条款，认为这算不上真正的开放权重；还有人赞赏其广泛的运行器支持（Unsloth、MLX），并就 Meta 的开放权重路线究竟是社区贡献还是围绕高粘性产品构建护城河展开争论。

**标签**: `#open-weight-models`, `#meta-ai`, `#large-language-models`, `#model-release`, `#licensing`

---

<a id="item-3"></a>
## [Goodfire 的 Nick Cammarata 主张神经网络学到的是干净、可分离的特征](https://already-clean.goodfire.com/) ⭐️ 8.0/10

Goodfire 联合创始人、曾在 OpenAI 参与早期机械可解释性研究的 Nick Cammarata 发表了一篇题为《Neural networks are clean》的新文章（already-clean.goodfire.com），主张神经网络学到的特征其实出人意料地干净、可分离，而非该领域长期假设的那种混乱、高度叠加的表征。文章很快在 Hacker News 上获得 489 分和 187 条以技术讨论为主的评论。 如果这一主张成立，将大幅降低机械可解释性研究的难度，因为该领域此前的悲观情绪很大程度上建立在“特征深度纠缠、难以分离”的假设之上。这对 AI 对齐研究意义重大——不少研究者认为，如果我们无法理解自己构建的系统，就无法对其对齐与掌控。 这篇文章更像一份庞大的证据综述：它重新审视了那些著名的多义神经元，梳理了可解释性工具失效的案例，并标出了网络中“混乱”仍然潜伏的位置。讨论中的批评者指出，这些证据未必能排除参数过载（parameter overloading）的可能，并援引了更早的结果，如 Lottery Ticket Hypothesis 以及 Multimodal Gap 论文（arXiv:2203.02053），后者暗示网络倾向于形成凝练的表征。

hackernews · themgt · 10月15日 16:04 · [社区讨论](https://news.ycombinator.com/item?id=50105647)

**背景**: 机械可解释性是可解释 AI 的一个子领域，目标是把神经网络逆向工程为人类可理解的特征、回路和算法。其核心障碍一直是叠加（superposition）与多义性（polysemanticity）：由于模型承载的概念多于神经元数量，单个神经元常常对许多互不相关的概念同时激活，导致干净的特征提取十分困难。Cammarata 曾在 OpenAI 参与早期可解释性工作（包括对视觉模型的回路式分析），之后联合创办了专注可解释性工具的初创公司 Goodfire，因此他由悲观转向乐观的态度在社区中颇具分量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mechanistic_interpretability">Mechanistic interpretability - Wikipedia</a></li>
<li><a href="https://arxiv.org/abs/2404.14082">[2404.14082] Mechanistic Interpretability for AI Safety -- A ... Mechanistic Interpretability for Neural Networks: Circuits ... Mechanistic Interpretability: Peeking Inside an LLM Mechanistic Interpretability Explained (2026) | Taskade Blog Mechanistic Interpretability in Neural Networks</a></li>

</ul>
</details>

**社区讨论**: 社区反应热烈但存在争议：sebmellen 称 Cammarata 是“一股自然之力”，并指出其发布帖把可解释性视为当今可能最重要的科学问题；而 bluejay2387 认为文章结论超出了已有证据所能支持的范围，并援引 Lottery Ticket Hypothesis 与 Multimodal Gap 研究，指出它们与参数过载并不矛盾。dleeftink 提出哲学层面的质疑，认为神经元所处的外部语境与它的生成历史可能比权重本身更重要；antics 则把该文概括为一份证据综述，论证“给 AI 基因组测序”比想象中更容易。

**标签**: `#mechanistic-interpretability`, `#AI-alignment`, `#neural-networks`, `#deep-learning`, `#research-discussion`

---

<a id="item-4"></a>
## [ASML 被曝正在研发混合键合设备](https://newsletter.semianalysis.com/p/asml-is-building-a-hybrid-bonding) ⭐️ 8.0/10

根据 SemiAnalysis 的分析报道，ASML 正在研发一款混合键合（hybrid bonding）设备，正式进军先进封装设备领域，但公司尚未对此发布任何官方公告。这一判断基于 ASML 自身的专利申请、一则新闻报道以及其公开的技术路线图，三者均指向该公司正在布局混合键合产品。 混合键合是先进封装与 3D 芯片堆叠的核心技术，随着 AI 加速器需求爆发，该领域需求激增，而台积电的 CoWoS 与 SoIC 产能持续紧张。若作为 EUV 光刻机绝对主导供应商的 ASML 进入这一领域，可能重塑先进封装设备的竞争格局，并为公司开辟光刻以外的全新增长曲线。 目前证据仍是间接的：尚未披露任何产品名称、规格、时间表或客户承诺。值得注意的是，混合键合要求介质表面极为平整、互连间距极细，使两颗芯片上的铜垫直接接触，这一工艺更接近晶圆级沉积与 CMP，而非光刻与套刻。

rss · Semianalysis · 10月15日 19:27

**背景**: 混合键合是一种先进封装技术，将铜垫嵌入极其平整的介质表面，使两片晶圆或芯片无需焊球即可在极细的互连间距下直接键合。它是 3D IC 堆叠与异质集成的关键，通过将多颗芯片或芯粒（chiplet）集成在一个封装内来获得性能提升，而不再单纯依赖晶体管微缩。先进封装已成为延续摩尔定律的重要途径，随着 AI、机器学习与 5G 应用的兴起，相关需求大幅增长。ASML 以光刻系统闻名，因此若进军键合设备，将意味着其设备产品组合的扩张。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Advanced_packaging_%28semiconductors%29">Advanced packaging (semiconductors)</a></li>
<li><a href="https://www.linkedin.com/posts/asmpt-semi-solutions_??-???-????-???-??-??-activity-7460607355387281408-2YHp">What is Hybrid Bonding in Semiconductor Technology | LinkedIn</a></li>

</ul>
</details>

**标签**: `#ASML`, `#hybrid bonding`, `#semiconductor manufacturing`, `#advanced packaging`, `#lithography`

---

<a id="item-5"></a>
## [随机神经网络自组装出学习基元，性能逼近反向传播](https://www.reddit.com/r/MachineLearning/comments/1x6hmyg/how_artificial_neural_networks_build_their_own/) ⭐️ 8.0/10

2026 年 10 月 9 日发表于《PNAS》的论文《How Biological Synapses Self-Assemble Gradient Learning》提出了“自组装学习”（SAM）：由共享的局部可塑性规则支配的、初始随机连接的类神经元单元，能够自行组织出学习基元（motif），而由这些基元搭建的网络在模式识别和图像分类任务上取得了与所测试的反向传播训练网络相近的准确率。MIT 麦戈文研究所于 2026 年 10 月 13 日对该成果进行了报道，将其描述为机器学习网络无需设计者提供详细蓝图即可获得学习机制的一种演示。 该成果把问题从“手工设计学习电路”转向“给出局部规则、让学习机制自行组织”，而这正是关于大脑局部突触过程能否解释全局信用分配这一长期争论的核心。若这种自组装具备稳健性，它可能为类脑可塑性学习理论以及通过局部更新而非全局梯度传输来学习的低功耗硬件提供启示；不过作者将其定位为生物合理性的论证，而非反向传播的替代方案。 论文指出，SAM 在两个尺度上自组装：单个基元在异突触可塑性（heterosynaptic plasticity）规则下从初始随机连接中涌现，而由 SAM 按层级组合成的网络会自组织出可证明近似于广义随机梯度下降的动力学，从而达到与反向传播相当的性能。作者明确提醒，自组织现象并不能证明大脑确实使用这一机制；悬而未决的问题包括基元在不同初始连接下的稳定性，以及该方法能否扩展到所演示的简单任务之外。

reddit · r/MachineLearning · /u/Dorian182 · 10月15日 10:01

**背景**: 反向传播是现代深度学习背后的核心算法，它需要把全局误差信号反向传遍整个网络，而这在生物上被认为不可信，因为真实突触只能获取局部信息。神经科学则用赫布学习等局部可塑性规则描述学习：突触根据所连接神经元的活动改变强度；但简单赫布规则已知不稳定，通常会被 BCM 理论、Oja 规则等变体取代。信用分配问题——局部变化如何累积为全局有效的学习——催生了一批通过元学习来发现可塑性规则、或在脉冲网络中搜索可解释局部规则的研究。而“自组装”进一步提问：不仅是权重，连学习电路本身能否从随机的初始连接中涌现出来。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.pnas.org/doi/10.1073/pnas.2606245123">How biological synapses self-assemble gradient learning | PNAS</a></li>
<li><a href="https://news.mit.edu/2026/how-artificial-neural-networks-build-their-own-learning-machinery-1013">How artificial neural networks build their own learning machinery</a></li>
<li><a href="https://en.wikipedia.org/wiki/Hebbian_theory">Hebbian theory - Wikipedia</a></li>

</ul>
</details>

**标签**: `#neuroscience`, `#machine-learning`, `#self-organization`, `#plasticity`, `#backpropagation`

---