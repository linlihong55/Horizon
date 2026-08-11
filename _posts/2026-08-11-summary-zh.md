---
layout: default
title: "Horizon Summary: 2026-08-11 (ZH)"
date: 2026-08-11
lang: zh
---

> 从 37 条内容中筛选出 9 条重要资讯。

---

1. [Meta 发布开源 30B 智能体模型 Muse Glimmer](#item-1) ⭐️ 9.0/10
2. [英伟达发布 Nemotron 3.5 Lightning 与 NeMo Switchyard](#item-2) ⭐️ 8.0/10
3. [压缩即预测：信息论与机器学习的交汇](#item-3) ⭐️ 8.0/10
4. [Mojo 1.0 正式发布：融合 Python 易用性与 C 级性能](#item-4) ⭐️ 8.0/10
5. [研究人员从专有 LLM API 中窃取隐藏推理轨迹](#item-5) ⭐️ 8.0/10
6. [Stratechery 分析英伟达 AI 基础设施主导地位面临的风险](#item-6) ⭐️ 8.0/10
7. [伦敦地铁试点人脸识别 隐私争议再起](#item-7) ⭐️ 8.0/10
8. [解耦下降：利用 AMP Onsager 修正实现训练-测试误差精确追踪](#item-8) ⭐️ 8.0/10
9. [HyperSAE：庞加莱几何加持稀疏自编码器，MSE 降低 9.8%](#item-9) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Meta 发布开源 30B 智能体模型 Muse Glimmer](https://simonwillison.net/2026/Aug/10/introducing-muse-glimmer/#atom-everything) ⭐️ 9.0/10

Meta 发布了 Muse Glimmer，一个采用 Apache 2.0 许可证的 300 亿参数开放权重模型，专为端到端智能体任务、可靠工具使用和多步推理而优化。该模型设计为可在单张消费级 GPU 上本地运行，Simon Willison 已通过 LM Studio 对其进行了快速测试。 这一举措意义重大，因为 Meta 改用宽松的 Apache 2.0 许可证，不同于以往限制较多的 Llama 许可证，并且精准定位于许多开发者与研究者关心的本地智能体与工具使用场景。这可能加速设备端智能体 AI 的发展，并为更大规模的闭源模型提供一个强有力的开源替代方案。 该模型是多模态的（支持视觉），Meta 强调其在深度搜索问答、MCP-Atlas、τ-Bench 和 SWE-Bench 等完整任务基准上的表现。Simon Willison 在 LM Studio 中运行了 18.16 GB 的量化版本，并利用其 llm-coding-agent 插件对一个 Datasette 代码库进行了测试。

rss · Simon Willison · 8月10日 23:56

**背景**: 开放权重模型允许开发者下载并在本地运行模型，从而避免云 API 成本和隐私问题。Apache 2.0 是一种宽松许可证，与 Meta 之前限制较多的 Llama 许可证不同，它允许广泛的商业和研究用途且几乎不受限制。智能体任务要求模型自主使用外部工具、执行多步计划并从错误中恢复；MCP-Atlas（基于模型上下文协议）和τ-Bench 等基准正是用来评估这些能力。Muse Glimmer 体现了当前面向智能体工作流优化的高性能本地模型这一更大趋势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://research.meta.ai/blog/introducing-muse-glimmer-open-agentic-model">Introducing Muse Glimmer: An Open Agentic Model That Runs on Your Device | Meta AI Research</a></li>
<li><a href="https://huggingface.co/meta-models/Muse-Glimmer-30B">meta-models/Muse-Glimmer-30B · Hugging Face</a></li>
<li><a href="https://github.com/scaleapi/mcp-atlas">GitHub - scaleapi/mcp-atlas: MCP Atlas</a></li>

</ul>
</details>

**标签**: `#AI`, `#Meta`, `#open-weights`, `#agentic`, `#LLM`

---

<a id="item-2"></a>
## [英伟达发布 Nemotron 3.5 Lightning 与 NeMo Switchyard](https://blogs.nvidia.com/blog/nemotron-lightning-switchyard-rtx-dgx/) ⭐️ 8.0/10

NVIDIA 发布了 Nemotron 3.5 Lightning，这是一个开放、30B 参数的混合专家（MoE）小语言模型，仅激活 3B 参数，专为智能体工作负载优化。同时发布了 NeMo Switchyard，这是一个开源的 Rust 代理和库，用于在多个 LLM 之间智能路由请求。 这一发布表明行业正加速转向更小、更高效的模型，这类模型能够以更低的成本和延迟提供强大的任务特定准确性。Switchyard 还有望成为智能体 AI 系统的标准组件，帮助其在多个模型之间平衡能力、成本与延迟。 该模型输出速度最高提升 4 倍，智能体任务完成速度提升 30%，并随附多种投机解码（speculative decoding）方法；Hugging Face 上提供 NVFP4 版本，可商用。Switchyard 是一个 Rust 代理和库，支持免调优和可调优的路由器，用于在模型间调度智能体工作负载。

hackernews · droidjj · 8月11日 19:35 · [社区讨论](https://news.ycombinator.com/item?id=49263340)

**背景**: 小语言模型（SLM）是紧凑型大语言模型，以一定能力为代价换取更低计算成本和更快推理，常采用混合专家（MoE）设计，每个 token 只激活一部分参数。模型路由是一种新兴模式，调度器根据任务、成本或延迟目标将每个请求分发给最合适的模型。NeMo Switchyard 属于 NVIDIA NeMo 生态，Nemotron 3.5 Lightning 也可用 NeMo 在私有数据上继续训练，以提升特定领域准确性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blogs.nvidia.com/blog/nemotron-lightning-switchyard-rtx-dgx/">NVIDIA Nemotron 3.5 Lightning and NeMo Switchyard Deliver Faster, Smarter, More Efficient Agentic AI | NVIDIA Blog</a></li>
<li><a href="https://developer.nvidia.com/blog/nvidia-nemotron-3-5-lightning-delivers-fast-accurate-specialized-task-execution-for-long-running-agents/">NVIDIA Nemotron 3.5 Lightning Delivers Fast, Accurate Specialized Task Execution for Long-Running Agents | NVIDIA Technical Blog</a></li>
<li><a href="https://developer.nvidia.com/blog/route-ai-agent-workloads-across-models-with-nvidia-nemo-switchyard/">Route AI Agents Across Models with NVIDIA NeMo Switchyard | NVIDIA Technical Blog</a></li>

</ul>
</details>

**社区讨论**: 评论者总体持积极态度，尤其看好小模型高效化趋势，并惊讶于 Nemotron 模型能通过 MLX 在 Apple Silicon 上流畅运行。但也有人质疑路由器在多次对话中如何处理提示缓存，另有人批评其基准对比遗漏了大多数 Qwen 模型，认为不够公平。

**标签**: `#NVIDIA`, `#LLM`, `#model routing`, `#AI`, `#open source`

---

<a id="item-3"></a>
## [压缩即预测：信息论与机器学习的交汇](https://ngrok.com/blog/compression-is-prediction) ⭐️ 8.0/10

ngrok 博客发表了一篇题为《压缩即预测》（Compression is prediction）的文章，探讨数据压缩与预测之间的理论等价关系，并借鉴信息论与机器学习的视角。该文将压缩不仅仅视为存储技术，而是视为智能预测背后的基本原则。 这一讨论意义重大，因为它将算法信息论中的基础思想（如柯氏复杂度与 Solomonoff 归纳）与现代机器学习实践联系起来。它为模型选择与泛化问题提供了有原理可循的视角，对构建预测系统的研究者和工程师都有参考价值。 据称，该文章在“数据分布完全代表所有未来问题”的假设下将压缩与预测等同；评论者指出，当需要泛化时这种等价关系会变得微妙，因为测试分布可能任意不同。社区回复还提到了 Schmidhuber 的早期工作以及 Grant Sanderson 的《压缩即智能》视频系列等资源。

hackernews · nikolay · 8月11日 19:49 · [社区讨论](https://news.ycombinator.com/item?id=49263497)

**背景**: 压缩与预测相关联的想法源于算法信息论。柯氏复杂度（Kolmogorov complexity）度量生成给定对象的最短程序长度，而 Solomonoff 归纳则通过给算法描述更短的理论更高的先验概率来形式化奥卡姆剃刀原则。最小描述长度（MDL）原理将这一思想应用于模型选择，选择能最好地压缩数据的模型。这些概念为理解“压缩可被视为一种预测”提供了理论基础。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kolmogorov_complexity">Kolmogorov complexity</a></li>
<li><a href="https://en.wikipedia.org/wiki/Solomonoff_induction">Solomonoff induction</a></li>
<li><a href="https://en.wikipedia.org/wiki/Minimum_description_length">Minimum description length</a></li>

</ul>
</details>

**社区讨论**: 评论者对该话题进行了深入讨论：有人提到剑桥大学开设的《信息论、推断与学习算法》课程，认为信息论与机器学习本应属于同一领域；还有人指出 Grant Sanderson 的视频系列。也有评论补充了细微差别——ssivark 认为，只有当数据分布与未来问题完全一致时，压缩与预测才等价，否则泛化会使问题更加复杂。还有人指出先行工作，rrherr 引用了 Schmidhuber 关于压缩驱动进步的研究，QuadrupleA 则提及 Ted Chiang 将 ChatGPT 比作“网络的模糊 JPEG”的文章。

**标签**: `#compression`, `#prediction`, `#machine learning`, `#information theory`, `#ngrok`

---

<a id="item-4"></a>
## [Mojo 1.0 正式发布：融合 Python 易用性与 C 级性能](https://www.modular.com/blog/modular-26-5-mojo-1-0-is-here) ⭐️ 8.0/10

Modular 发布了 Mojo 1.0，这是其面向 AI 的编程语言的一个重要里程碑，同时上线了该语言的官方网站 mojolang.org。此次发布强调将类似 Python 的易用性与 C/C++ 级性能结合起来，并支持从 CPU 到 GPU 的多样硬件。 Mojo 1.0 之所以重要，是因为它为 AI 开发者提供了一种潜在的新选择：既能享受 Python 的开发效率，又能获得系统级语言的速度，从而减少用 C、C++ 或 Rust 编写底层扩展的需求。如果该语言获得广泛应用，它可能会改变 AI 基础设施和模型服务代码的编写方式。 Mojo 基于 MLIR 编译器框架而非直接基于 LLVM，因此能够为 CPU、GPU、TPU、ASIC 及其他加速器生成代码。标准库以 Apache 2.0 许可证开源，但编译器目前仍为闭源，Modular 承诺于 2026 年秋季将其开源；路线图也显示，Mojo“可能会、也可能不会”发展成完整的 Python 超集。

hackernews · dayanruben · 8月11日 16:56 · [社区讨论](https://news.ycombinator.com/item?id=49261128)

**背景**: Mojo 是 Modular 公司正在开发中的系统编程语言，其语法设计得酷似 Python，语义则受 Rust 启发，包括静态类型和借用检查器。它最初被设想为 Python 的超集，但这一目标已被弱化，可能不会完全实现。该语言旨在让开发者无需受特定供应商限制，即可为异构硬件编写快速且内存安全的代码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mojo_%28programming_language%29">Mojo (programming language) - Wikipedia</a></li>
<li><a href="https://mojolang.org/">Mojo - Modular</a></li>

</ul>
</details>

**社区讨论**: 社区反应谨慎乐观，但带有明显的质疑。多位评论者对闭源编译器的价值提出疑问，认为已有的基于 Rust 或 C 的 Python 库同样能提供性能；还有人询问 Mojo 是否仍要成为 Python 超集，并批评公告中使用 AI 生成的图片；此外，路线图“可能不会”完全超集 Python 的表述也引发关注。总体来看，许多人仍抱有希望，但希望官方给出更清晰的定位并加快开源进程。

**标签**: `#Mojo`, `#programming-language`, `#AI`, `#compiler`, `#release`

---

<a id="item-5"></a>
## [研究人员从专有 LLM API 中窃取隐藏推理轨迹](https://stolen-thoughts.com/) ⭐️ 8.0/10

研究人员展示了一种方法，通过将前沿模型的推理轨迹重放给较弱的兄弟模型并对其越狱，来提取专有 LLM API 中隐藏的思维链推理。该技术详见论文《Stealing Reasoning Traces from Proprietary LLM APIs》（arXiv:2608.09867），可绕过加密和系统级过滤器。 此事之所以重要，是因为专有 LLM 提供商隐藏思维链以保护知识产权并限制信息泄露，而这次攻击表明这些防御可以被绕过。它引发了关于模型安全、用户隐私以及用其他模型输出训练的道德问题的紧迫讨论。 该攻击的原理是将前沿模型生成的轨迹重放到较弱的兄弟模型中，然后越狱较弱的模型以揭示被加密的推理文本。论文指出，对能力更强的模型进行直接提取攻击，需要同时绕过模型级对齐以及输入过滤器、输出子串匹配过滤器等系统级防御。

hackernews · quantumgarbage · 8月11日 13:22 · [社区讨论](https://news.ycombinator.com/item?id=49257876)

**背景**: 领先的大型语言模型提供商如今都会隐藏模型的逐步推理（即思维链），以保护知识产权并限制信息泄露。这些轨迹并非存储在服务器端，而是作为加密文本块返回给客户端，客户端在后续每次请求时再将其传回。此前关于模型提取攻击的研究主要集中于复制模型行为、恢复训练数据或窃取提示词；这项工作将这一研究方向扩展到加密的推理轨迹。更广泛的背景还涉及一场辩论：当输出是由用户付费 token 生成时，“窃取”一词是否恰当。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2608.09867">Stealing Reasoning Traces from Proprietary LLM APIs</a></li>
<li><a href="https://arxiv.org/pdf/2608.09867">Stealing Reasoning Traces from Proprietary LLM APIs - arXiv.org</a></li>
<li><a href="https://stolen-thoughts.com/paper.pdf">Stealing Reasoning Traces from Proprietary LLM APIs</a></li>

</ul>
</details>

**社区讨论**: 评论区观点不一：有人认为“窃取”是一个带有误导性和道德色彩的词，因为用户已经为 token 付费；也有人指出提取可以通过更简单的方式完成，例如禁用思考并提供一个“deep\_think”工具。一位评论者提到，他们通过自动注入开发者提示词在 Codex 上实现了类似效果；还有人猜测提供商是否故意允许这种攻击。另一条评论指出，API 摘要往往会让推理看起来比实际更干净，这种失真正是论文所证实的。

**标签**: `#LLM`, `#security`, `#interpretability`, `#AI safety`, `#reverse engineering`

---

<a id="item-6"></a>
## [Stratechery 分析英伟达 AI 基础设施主导地位面临的风险](https://stratechery.com/2026/nvidias-risky-business/) ⭐️ 8.0/10

Stratechery 发表了一篇战略分析文章，审视威胁英伟达在 AI 基础设施领域主导地位的风险，重点关注其 CUDA 软件生态面临的挑战以及 AI 算力需求增长的可持续性。这篇文章引发了社区围绕技术与经济假设的广泛讨论。 英伟达在 AI 行业中处于核心地位，因此其主导地位的任何削弱都会波及硬件供应链、云服务商和 AI 初创公司。对于评估英伟达 CUDA 护城河和增长预期是否可持续的投资者和技术人员来说，这篇分析具有重要参考价值。 这篇文章因其高价值的战略视角获得了 8.0/10 的评分，社区评论围绕 CUDA 的生态扎根程度是否能弥补其糟糕的开发者体验展开辩论。提出的一个关键经济警告是：虽然算力需求肯定在增长，但预期的增长率可能被夸大了。

hackernews · jonbaer · 8月11日 10:02 · [社区讨论](https://news.ycombinator.com/item?id=49255710)

**背景**: CUDA（Compute Unified Device Architecture）是英伟达专有的并行计算平台和 API，于 2007 年首次发布，允许软件利用 GPU 进行通用计算。它已深度嵌入机器学习研究，为英伟达提供了与硬件相辅相成的软件护城河。正因如此，许多人认为即使竞争对手在开发替代方案，英伟达的地位也难以撼动。Stratechery 的分析则审视了这条护城河以及围绕 AI 基础设施需求建立的增长假设是否真的那么稳固。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/CUDA">CUDA</a></li>

</ul>
</details>

**社区讨论**: 评论者观点不一：有人认为 CUDA 的生态扎根掩盖了其糟糕的开发者体验（例如 C++ 的各种陷阱）；也有人指出算力需求确实存在，但增长预期很可能被夸大。还有评论者对 AI 在生物效率面前能否实现奇点表示怀疑，而另一人则反驳说英伟达正在进军机器人领域，并且除中国外仍是西方市场的主导者。

**标签**: `#Nvidia`, `#AI infrastructure`, `#business strategy`, `#CUDA`, `#investment analysis`

---

<a id="item-7"></a>
## [伦敦地铁试点人脸识别 隐私争议再起](https://www.btp.police.uk/news/btp/news/england/btp-expands-live-facial-recognition-lfr-trial-into-london-underground-stations/) ⭐️ 8.0/10

英国交通警察正在将实时人脸识别（LFR）试点扩展到伦敦地铁站，此前该技术已在公共活动等场所部署。此举紧随伦敦警察厅在面临法律挑战的情况下仍计划加强全伦敦 LFR 使用的步伐。 这标志着人脸识别技术向日常公共交通领域深入渗透的重要一步，每天有数百万人使用伦敦地铁网络。这加剧了关于大规模监控、隐私权以及该技术带来的公共安全收益是否值得以公民自由为代价的争论。 LFR 系统通过闭路电视摄像头实时扫描面部，并与警方关注名单中的通缉或嫌疑人进行匹配。批评者指出存在误报、种族偏见和缺乏独立监督的风险，而警方则声称该技术在识别嫌疑人和减少暴力犯罪方面已被证明有效。

hackernews · BlueBerry2001 · 8月11日 09:40 · [社区讨论](https://news.ycombinator.com/item?id=49255496)

**背景**: 实时人脸识别（LFR）是一种监控工具，可从摄像头画面中捕捉人脸，并立即与已知人员数据库进行比对。伦敦警察厅多年来已在公共活动和特定区域试用 LFR，此次扩展到地铁等交通枢纽代表了该技术的新前沿。支持者认为它有助于抓捕重罪犯，但公民自由团体警告说，这会使大规模监控常态化，并削弱人们在公共空间中的匿名活动权利。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.met.police.uk/advice/advice-and-information/facial-recognition/live-facial-recognition-trial/">Live Facial Recognition | Metropolitan Police</a></li>
<li><a href="https://www.biometricupdate.com/202511/metropolitan-police-to-expand-live-facial-recognition-use-even-amid-legal-challenge">Metropolitan Police to expand live facial recognition use ...</a></li>
<li><a href="https://www.theguardian.com/technology/2026/jun/23/met-to-expand-live-facial-recognition-central-london">Met to expand use of live facial recognition into central ...</a></li>

</ul>
</details>

**社区讨论**: 社区评论以批评为主，许多用户对隐私和公民自由的侵犯表示愤怒。有人认为，随着非接触式支付系统的普及，地铁匿名出行的权利早已丧失；还有人质疑试点的目的，指出无论结果如何都不太可能终止推广；少数人将此情形与其他国家对比，或引用了奥威尔式的警示意象。

**标签**: `#facial recognition`, `#privacy`, `#surveillance`, `#London`, `#civil liberties`

---

<a id="item-8"></a>
## [解耦下降：利用 AMP Onsager 修正实现训练-测试误差精确追踪](https://www.reddit.com/r/MachineLearning/comments/1vlu1se/decoupled_descent_enforcing_exact_traintest_error/) ⭐️ 8.0/10

作者提出了一种名为解耦下降（DD）的训练算法，利用近似消息传递（AMP）的 Onsager 修正，保证每个参数迭代处的训练误差渐近等于测试误差。论文在风格化的高斯混合模型上研究全批量梯度下降，并在两层 XOR 模型上进行了 100 次模拟。 这项工作为训练-测试误差差距提供了一个新的理论视角，将其视为数据复用偏差，并可在训练过程中被可证明地控制。如果该方法能扩展到更大规模，它可能为神经网络提供有原则的最优停止和超参数调优方法，并启发梯度下降之外的新训练规则。 一个关键局限是结果具有渐近性，目前仅限于风格化的高斯混合模型和全批量梯度下降；作者也指出距离大规模模型还有很长的路要走。作者计划发布一个兼容 PyTorch 的软件包，并欢迎功能建议。

reddit · r/MachineLearning · /u/mlovik1 · 8月11日 21:06

**背景**: 近似消息传递（AMP）是一类用于高维统计问题（如压缩感知）的迭代算法，其特点是在每一步加入记忆项/Onsager 修正项，使算法行为可以通过标量状态演化来跟踪。Onsager 修正以 Lars Onsager 命名，用于消除迭代与历史噪声之间的相关性，这正是基于 AMP 的方法能够精确预测训练和测试误差的原因。解耦下降（DD）将这一思想应用于神经网络训练，从而在每个迭代点提供训练-测试误差匹配的保证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2201.07487">A Concise Tutorial on Approximate Message Passing A unifying tutorial on Approximate Message Passing Lecture 19: Approximate message passing algorithms Approximate Message Passing Tutorial - GitHub Pages Message-passing algorithms for compressed sensing A unifying tutorial on Approximate Message Passing Note on Approximate Message Passing - Peng Xu</a></li>
<li><a href="https://arxiv.org/abs/2105.02180">A unifying tutorial on Approximate Message Passing Lecture 19: Approximate message passing algorithms Approximate Message Passing Tutorial - GitHub Pages Message-passing algorithms for compressed sensing A unifying tutorial on Approximate Message Passing Note on Approximate Message Passing - Peng Xu</a></li>
<li><a href="https://arxiv.org/abs/2601.07095">Score-Based VAMP with Fisher-Information-Based Onsager Correction</a></li>

</ul>
</details>

**标签**: `#approximate-message-passing`, `#generalization`, `#training theory`, `#neural networks`, `#high-dimensional statistics`

---

<a id="item-9"></a>
## [HyperSAE：庞加莱几何加持稀疏自编码器，MSE 降低 9.8%](https://www.reddit.com/r/MachineLearning/comments/1vlpyh2/hypersae_decoupled_poincar%C3%A9_geometry_for_sparse/) ⭐️ 8.0/10

HyperSAE 是一个新的 PyTorch 库，将庞加莱双曲几何应用于稀疏自编码器（SAE）以进行机制可解释性研究。在 Gemma-2-2B 第 13 层、2000 万 token 的测试中，它使重建 MSE 降低 9.8%，死潜变量（dead latents）从 3.8% 降至 0.2%，CE 损失恢复率提升 3.4 个百分点。 这项工作通过使用与 LLM 中概念的分层分支结构相匹配的双曲几何，解决了 SAE 训练中两个已知痛点：特征碰撞（feature collisions）和死潜变量。由于 HyperSAE 的前向传播保持欧几里得形式，推理开销为零，可能使基于 SAE 的可解释性工具在大模型上更可靠、更可扩展。 HyperSAE 采用解耦的双速设计：前向传播和因果干预保持欧几里得形式（单向量加法），仅在训练时将字典权重投影到庞加莱球中。蕴含锥损失（entailment cone loss）将父概念安排在原点附近、子概念安排在边界附近；TriPartite 损失结合了重建、L1 稀疏性和蕴含项，库中还包括共激活队列跟踪和单类训练器接口。

reddit · r/MachineLearning · /u/visha1v · 8月11日 18:37 · [社区讨论](https://www.reddit.com/r/MachineLearning/comments/1vlpyh2/hypersae_decoupled_poincar%C3%A9_geometry_for_sparse/)

**背景**: 稀疏自编码器（SAE）在机制可解释性中用于将神经网络激活分解为稀疏、可解释的特征。标准 SAE 将字典原子嵌入欧几里得空间，其体积按多项式增长，而 LLM 学到的概念常形成按指数增长的分层结构，导致在大字典规模下出现特征碰撞和死特征。庞加莱模型是双曲几何的标准表示，距离向边界呈指数扩展，因此天然适合树状层次结构。蕴含锥是一种在此类空间中嵌入层级关系的技术。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2406.04093">[2406.04093] Scaling and evaluating sparse autoencoders Scaling and evaluating sparse autoencoders - OpenAI ICLR Poster Scaling and evaluating sparse autoencoders (PDF) Scaling and evaluating sparse autoencoders - ResearchGate Dead Feature Counts in Sparse Autoencoders Predict Underlying ... Beyond Input Activations: Identifying Influential Latents by ...</a></li>
<li><a href="https://openaccess.thecvf.com/content_CVPRW_2020/papers/w50/Dhall_Hierarchical_Image_Classification_Using_Entailment_Cone_Embeddings_CVPRW_2020_paper.pdf">Hierarchical Image Classiﬁcation using Entailment Cone Embeddings</a></li>

</ul>
</details>

**标签**: `#sparse autoencoders`, `#mechanistic interpretability`, `#hyperbolic geometry`, `#representation learning`, `#LLM interpretability`

---