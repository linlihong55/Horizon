---
layout: default
title: "Horizon Summary: 2026-08-07 (ZH)"
date: 2026-08-07
lang: zh
---

> 从 38 条内容中筛选出 10 条重要资讯。

---

1. [中国团队首次证实胶球这一全新物质形态](#item-1) ⭐️ 9.0/10
2. [AMD 收购 Taalas，将 AI 模型蚀刻进硅片以提升推理性能](#item-2) ⭐️ 8.0/10
3. [AI 接管代码后，品味成为人类最后的优势](#item-3) ⭐️ 8.0/10
4. [Qwen3.8 Max 登顶智能体指数，引发模型平权与本地部署讨论](#item-4) ⭐️ 8.0/10
5. [双向扩散模型通过往返一致性预测自身推演误差](#item-5) ⭐️ 8.0/10
6. [字节跳动拟训练超 5 万亿参数大模型，张一鸣反对蒸馏](#item-6) ⭐️ 8.0/10
7. [阿里云 Wan3.0 视频模型公测，单次可生成 30 秒](#item-7) ⭐️ 8.0/10
8. [DeepSeek 2080 万美元入股宇树 IPO，携手共研具身智能](#item-8) ⭐️ 8.0/10
9. [GPT-5 一周年，OpenAI 推出 Agent Plugins 开放标准](#item-9) ⭐️ 8.0/10
10. [阿里巴巴拟对下一代 Qwen 开源模型大型用户收费](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [中国团队首次证实胶球这一全新物质形态](https://mp.weixin.qq.com/s/pvyNR1lN7QPx3IrpB3WtUg) ⭐️ 9.0/10

2026 年 8 月 6 日，北京谱仪 III 国际合作组在巴西举行的国际高能物理大会上宣布已证实胶球的存在。经过 15 年研究，团队测定了 X\(2370\)粒子的自旋宇称和味单态性质，证明其主要成分正是胶球。 这是胶球——这种标准模型长期预言却从未被观测到的纯胶子物质的首次实验证实。它为量子色动力学提供了关键检验，为研究强相互作用打开了新窗口。 X\(2370\)于 2011 年首次被观测到；2024 年团队利用 100 亿个 J/ψ粒子衰变测得其自旋宇称为 0−+，与格点量子色动力学预言一致。2026 年的新结果测定了多个新衰变模式，并确立其味单态性质，补全了证据链。

telegram · zaihuapd · 8月6日 07:31

**背景**: 在标准模型中，夸克通过传递强相互作用的胶子结合成质子、中子等粒子。由于胶子本身带色荷，它们之间可以相互吸引而形成不含价夸克的束缚态，即理论上预言的胶球。北京谱仪 III 是北京正负电子对撞机（BEPCII）上的大型通用磁谱仪，用于在粲物理能区研究粒子的产生和衰变性质。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cas.cn/cm/202608/t20260806_5117959.shtml">【新华社】科研人员确证新型粒子“胶球”的存在----中国科学院</a></li>
<li><a href="https://zh.wikipedia.org/zh-hans/%E8%86%A0%E7%90%83">胶球 - 维基百科，自由的百科全书</a></li>
<li><a href="https://bes3.ihep.ac.cn/">Beijing Spectrometer (BESIII) Experiment----Institute of High ...</a></li>

</ul>
</details>

**标签**: `#particle physics`, `#glueball`, `#Standard Model`, `#experiment`, `#scientific breakthrough`

---

<a id="item-2"></a>
## [AMD 收购 Taalas，将 AI 模型蚀刻进硅片以提升推理性能](https://www.theregister.com/systems/2026/08/06/amd-acquires-ai-chip-startup-taalas-to-boost-inference-performance-by-etching-models-into-silicon/5284344) ⭐️ 8.0/10

2026 年 8 月 6 日，AMD 宣布收购 AI 芯片初创公司 Taalas，后者将特定神经网络模型直接固化到硅片中。AMD 计划将 Taalas 的技术纳入其加速器路线图，并与 Instinct GPU、EPYC CPU 及 ROCm 软件结合，打造系统级解决方案。 这笔收购表明 AMD 正发力快速增长的 AI 推理市场，在该市场中低延迟和高吞吐量日益关键。此举也加剧了与英伟达的竞争——英伟达近期实质上收购了 AI 芯片初创公司 Groq——并引发了关于将模型蚀刻进硅片能否跟上模型快速迭代步伐的讨论。 Taalas 的做法是将某个模型的固定版本直接制造在芯片中，从而实现更快的 token 生成，但这也使它成为一个专用、灵活性较低的加速器。AMD 表示，该技术将补充其全栈 AI 平台（包括 Helios 机架级系统），并将在未来与 Instinct GPU 搭配的加速器产品中出现。

hackernews · itvision · 8月6日 20:23 · [社区讨论](https://news.ycombinator.com/item?id=49201970)

**背景**: AI 推理是指运行已训练的神经网络进行预测的过程，目前正成为数据中心的主要工作负载。GPU 是可以运行多种模型的通用加速器，而 ASIC 则可以针对单一架构甚至单一模型进行优化，从而实现更高的效率。Taalas 属于包括 Groq 和 Etched 在内的一批初创公司，它们希望通过专用硬件在推理速度上超越 GPU。然而，由于制造芯片需要时间和资金，固定为某一模型版本的芯片在出货时可能已经过时，这是公司和行业仍在权衡的问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.eetimes.com/ai-chip-startup-taalas-acquired-by-amd/">AI Chip Startup Taalas Acquired by AMD - EE Times</a></li>
<li><a href="https://www.cnbc.com/2026/08/06/amd-buys-taalas-startup-that-hardwires-ai-models-into-its-silicon.html">AMD buys Taalas, startup that hardwires AI models into its ...</a></li>
<li><a href="https://ir.amd.com/news-events/press-releases/detail/1296/amd-acquires-taalas-to-advance-compute-solutions-for-rapidly-growing-ai-inference-market">AMD Acquires Taalas to Advance Compute Solutions for Rapidly ...</a></li>

</ul>
</details>

**社区讨论**: 评论者的情绪兼具兴奋与怀疑。有人惊叹于几年后 AI 推理速度大幅提升的前景，也有人质疑在模型快速迭代的背景下，把快速演进的模型蚀刻进芯片是否合理——芯片出货时模型可能已经落后一代。业内护城河的讨论也很热烈：有人对 OpenAI 和 Anthropic 没有先收购 Taalas 感到意外，并指出 Google 已经在借助 TPU 做类似工作；还有评论者强调了前沿模型&\#x27;峰值性能&\#x27;与&\#x27;可靠性能&\#x27;之间的区别。

**标签**: `#AMD`, `#AI hardware`, `#acquisition`, `#inference`, `#semiconductors`

---

<a id="item-3"></a>
## [AI 接管代码后，品味成为人类最后的优势](https://notashelf.dev/posts/taste-is-all-thats-left) ⭐️ 8.0/10

一篇名为《Taste Is All That&\#x27;s Left》的文章认为，随着 AI 工具越来越多地处理软件工程中的技术执行，人类的品味——即对设计和质量做出合理判断的能力——成为关键的区别因素。这篇文章在 Hacker News 上引发了长达 203 分、158 条评论的热烈讨论，辩论品味在 AI 辅助开发中的作用。 随着基于 LLM 的编程工具成为主流，软件开发的瓶颈从编写代码转移到做出良好的设计决策。这改变了工程师的评价方式，也引发了关于如何在 AI 生成的代码库中保持质量的思考。 文章全文未提供，但讨论揭示了关键关切：LLM 生成的代码和文章往往缺乏“信号”或真正的洞察力，而 AI 生成的代码库在多个开发者长时间扩展时可能变得难以管理。评论者争论“品味”这个术语是否恰当，有些人倾向于用“判断力”作为更可操作的概念。

hackernews · tsak · 8月6日 17:01 · [社区讨论](https://news.ycombinator.com/item?id=49199346)

**背景**: 在软件工程中，“品味”指的是对良好设计的直觉——选择简单、可维护的解决方案而非巧妙但复杂的方案——并且被认为有别于纯粹的技术技能。软件工匠运动强调对工作的自豪感和持续改进，与这一理念有相似之处。随着 LLM 越来越多地自动化代码生成，这种主观的质量感成为更稀缺、更有价值的人类特质。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://davegriffith.substack.com/p/what-do-engineers-mean-when-we-say">What Do Engineers Mean When We Say &quot;Taste&quot;?</a></li>
<li><a href="https://www.seangoedecke.com/taste/">What is &quot;good taste&quot; in software engineering?</a></li>

</ul>
</details>

**社区讨论**: 评论中既有共鸣也有怀疑。一位用户引用了苏珊·桑塔格关于品味的论述，另一位则对 LLM 糟糕的写作质量及其在真实项目中难以扩展表示沮丧。一位有数十年经验的程序员从自身经历出发表示认同，但质疑如果结果能用，“品味”是否还重要；还有人认为这种讨论“过于文艺”，更偏好“判断力”一词。

**标签**: `#AI`, `#software engineering`, `#taste`, `#LLM`, `#craftsmanship`

---

<a id="item-4"></a>
## [Qwen3.8 Max 登顶智能体指数，引发模型平权与本地部署讨论](https://artificialanalysis.ai/?intelligence=agentic-index) ⭐️ 8.0/10

Artificial Analysis 的 Agentic Index 将阿里巴巴的 Qwen3.8 Max 评为综合最佳模型，超越了 Opus Max 等竞品。这一排名引发了社区关于分数稳定性以及模型平权意义的讨论。 这一事件意义重大，因为它标志着中国 AI 模型在智能体任务上已与西方领先模型平起平坐，而智能体被认为是对话式 AI 之后的下一前沿。它也让一个实际问题重新成为焦点：像 Qwen 这样的开源权重模型能否很快在消费级硬件上本地运行复杂智能体。 Qwen3.8-Max 是一个 2.4 万亿参数的混合专家（MoE）模型，支持 100 万上下文，在 OpenRouter 上输入价格每百万 tokens 2 美元、输出每百万 tokens 6 美元。Artificial Analysis 的 Agentic Index 将工具调用准确率、多步骤规划和指令遵循能力综合为一个复合分数。

hackernews · apitman · 8月6日 18:44 · [社区讨论](https://news.ycombinator.com/item?id=49200652)

**背景**: Agentic Index 是 Artificial Analysis 推出的基准，用于衡量模型处理智能体工作流（包括工具使用、规划、自主性和复杂问题解决）的能力。Qwen 是阿里巴巴的开源权重模型系列，Qwen3.8-Max 是其旗舰型号，作为预览版的正式后续版本发布，并承诺开放权重。本地模型爱好者目前认为 Qwen 3.6 27B 这类小型模型是在消费级硬件上运行 AI 的最佳选择，并希望 3.8 系列的较小版本能让本地智能体默认可用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://artificialanalysis.ai/">AI Model &amp; API Providers Analysis | Artificial Analysis</a></li>
<li><a href="https://www.marktechpost.com/2026/08/03/alibaba-qwen-releases-qwen3-8-max/">Alibaba Qwen Releases Qwen3.8-Max: A 2.4 Trillion Parameter MoE Model and the Most Capable One in the Qwen Family to Date - MarkTechPost</a></li>
<li><a href="https://openrouter.ai/qwen/qwen3.8-max">Qwen3.8 Max - API Pricing &amp; Benchmarks | OpenRouter</a></li>

</ul>
</details>

**社区讨论**: 评论者意见不一：有人认为这一排名证明中国已经追上，并称赞 Qwen 实际排查问题的能力；也有人质疑基准的稳定性，指出刷新后分数发生了变化。有用户认为任何将 Opus 5 列为第一的基准都失去可信度，另有人指出 Opus 在单独的 Intelligence Index 中仍居首位，并在他们自己的综合排行榜中领先。还有几位评论者对即将推出的、可本地运行的小型 Qwen 3.8 版本表示期待。

**标签**: `#qwen`, `#agentic-ai`, `#benchmark`, `#ai-models`, `#artificial-analysis`

---

<a id="item-5"></a>
## [双向扩散模型通过往返一致性预测自身推演误差](https://www.reddit.com/r/MachineLearning/comments/1vh2gn1/roundtrip_consistency_bidirectional_diffusion/) ⭐️ 8.0/10

研究人员训练了一个条件潜扩散模型，通过方向标志使动力学系统既能向前也能向后演化。他们证明，往返不一致性（即向前推演后再向后推演回到起点时的差异）可以作为无需测量、自监督的推演误差代理指标。 这为部署阶段估计预测可靠性提供了一种实用方法，无需集成模型、留出数据或控制方程。在视频生成和湍流等离子体数字孪生等缺少真实值的长时间推演预测应用中，该方法可以提升预测质量。 该双向模型在同一个网络中同时学习两个方向，且性能优于分别针对每个方向训练的两个专用模型。在 LE-PDE-UQ 湍流 Navier-Stokes 基准上，其精度达到十个模型集成的 1.3 倍以内，而训练成本约为后者的十分之一，并实现了最好的免训练像素级校准。

reddit · r/MachineLearning · /u/Clean-Hovercraft5825 · 8月6日 12:10

**背景**: 自回归潜扩散模型和流模型通过反复预测下一状态来生成长时间序列，但小误差会不断累积，而部署阶段往往没有真实值可供比对。往返一致性利用了所学动力学模型的可逆性：如果模型既能向前也能向后演化，那么先向前再向后就应该回到初始状态，因此任何不一致性都可作为误差信号。这一思想基于双向扩散——一种由前向与后向互相耦合驱动生成或优化的扩散设计范式，而非单向映射。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2608.00675">[2608.00675] Round-Trip Consistency: Bidirectional Diffusion ...</a></li>
<li><a href="https://arxiv.org/html/2608.00675v1">Round-Trip Consistency: Bidirectional Diffusion Models Can ...</a></li>
<li><a href="https://github.com/alexscheinker/round-trip-consistency/blob/main/README.md">round-trip-consistency/README.md at main · alexscheinker ...</a></li>

</ul>
</details>

**标签**: `#machine learning`, `#diffusion models`, `#self-supervised learning`, `#dynamical systems`, `#latent diffusion`

---

<a id="item-6"></a>
## [字节跳动拟训练超 5 万亿参数大模型，张一鸣反对蒸馏](https://mp.weixin.qq.com/s/_SGStRsaJmpos2_deXUs8A) ⭐️ 8.0/10

字节跳动正讨论训练一个参数规模超过 5 万亿的大语言模型，由 Seed Foundation 负责人项亮主导，并与大语言模型预训练数据负责人沈科合作。若计划落地，将超越阿里 Qwen 3.8-Max 和月之暗面 Kimi K3，成为国内已知参数规模最大的模型。 这标志着中国 AI 竞赛正转向追求原创前沿大模型，而非蒸馏西方模型。张一鸣明确反对蒸馏路线、鼓励追求智能上限，可能重塑字节跳动在阿里、月之暗面及美国实验室面前的竞争地位。 该计划目前仍处于早期阶段。消息称，两周前的 Seed 全员会上，张一鸣认为蒸馏只是复制 Claude 的既有能力、难以实现超越，并鼓励团队接受短期落后。Seed 正在重新梳理组织、取消赛马机制并收拢资源，且将编程视为关键方向，已整合火山引擎、飞书和豆包资源补课。

telegram · zaihuapd · 8月6日 13:10

**背景**: 字节跳动 Seed 团队成立于 2023 年，是豆包、即梦视频和 Seedream 图像生成器等模型背后的 AI 研究部门。目前国内已知最大模型包括阿里的 Qwen 3.8-Max（2.4 万亿参数）和月之暗面的 Kimi K3（2.8 万亿参数），5 万亿参数的模型将显著提升规模。蒸馏是一种让小模型学习大模型能力的技术，但据报道张一鸣认为它只是复制而非真正的超越。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://seed.bytedance.com/en/">ByteDance Seed</a></li>
<li><a href="https://openlm.ai/qwen3.8/">Qwen3.8 | OpenLM.ai</a></li>
<li><a href="https://www.moonshot.ai/">Moonshot AI</a></li>

</ul>
</details>

**标签**: `#AI`, `#LLM`, `#ByteDance`, `#Model Training`, `#Strategic Direction`

---

<a id="item-7"></a>
## [阿里云 Wan3.0 视频模型公测，单次可生成 30 秒](https://mp.weixin.qq.com/s/4ivdFBuZFsycAaQH1LESKA) ⭐️ 8.0/10

阿里云正式开启新一代视频生成模型 Wan3.0 的公测，单次可生成 30 秒视频，并首次支持 doc、xls、ppt、pdf、md 等文档格式输入。用户现可通过阿里云百炼、万镜一刻、万相官网、千问创作 PC 端等平台体验，API 定价 480P 为 0.3 元/秒。 Wan3.0 通过创新的文档转视频能力，让用户能把日常办公文件直接变成视频，是 AI 视频生成领域的重要进展。凭借有竞争力的 API 定价和多个阿里平台的开放渠道，它增强了阿里云在与 Sora 等模型竞争中的市场地位。 API 定价方面，480P、720P、1080P 分别为 0.3、0.6、1.2 元/秒，接口将于近期全量开放。模型在人像生成上追求“千人千面”，并在角色、道具、场景、风格等维度保持一致性；千问 APP 目前为灰度开放。

telegram · zaihuapd · 8月6日 14:17

**背景**: Wan 是阿里云旗下由通义实验室开发的视频生成模型系列，此前已有 Wan 2.7 等版本。与纯文本生成视频的工具不同，Wan3.0 还支持文档输入，阿里云将其定位为 OpenAI Sora 等闭源模型之外的开源权重（open-weight）选择。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bottlerocketcontent.com/wan3-0-alibaba-omni-reference-launch/">Wan 3 . 0 : Alibaba &#x27;s New AI Video Model , Explained</a></li>
<li><a href="https://flowith.io/blog/wan-3-0-vs-sora-2-0-comparable-quality-free/">Wan 3 . 0 vs. Sora 2.0: Is OpenAI&#x27;s Closed Model Still... - Flowith Blog</a></li>

</ul>
</details>

**标签**: `#AI`, `#video generation`, `#Alibaba Cloud`, `#Wan3.0`, `#machine learning`

---

<a id="item-8"></a>
## [DeepSeek 2080 万美元入股宇树 IPO，携手共研具身智能](https://www.reuters.com/world/asia-pacific/deepseek-invests-208-million-unitrees-shanghai-ipo-2026-08-06/) ⭐️ 8.0/10

DeepSeek 以 1.408 亿元人民币（约 2080 万美元）参与宇树科技在上海 IPO 的战略配售，获得 93.3399 万股，并签署战略合作，共同开发面向人形机器人的 AI 模型。两家总部均位于杭州的公司将在模型训练服务、技术方案、机器人采购和具身智能应用上相互优先考虑。 此次合作将领先的 AI 实验室与顶尖人形机器人制造商连接起来，目标直指机器人‘大脑’的核心瓶颈——理解陌生环境并可靠执行指令。它还可能为 DeepSeek 提供稀缺的物理世界数据，以增强其多模态视觉能力，从而加速具身智能的商业化。 根据交易所文件，宇树在采购模型训练服务和技术方案时将优先选择 DeepSeek；DeepSeek 在购买机器人或开展具身智能应用时同样优先考虑宇树。这 93.3399 万股占宇树科技在上交所（代码 688836.SS）IPO 战略配售股份总数的 2.31%。

telegram · zaihuapd · 8月6日 14:23

**背景**: 具身智能是一种 AI 研究方法，聚焦于拥有物理身体的智能体（如人形机器人），它们通过传感器感知环境、通过执行器作用于环境，智能源于身体、大脑与环境之间的紧密耦合。视觉语言模型（VLM）是能同时从图像和文本中学习的多模态模型，被视为让机器更深入理解物理世界的关键一步。人形机器人长期面临‘大脑’难题：理解非结构化、陌生的环境并可靠执行复杂任务，需要高级的感知、推理和规划能力。IPO 战略配售允许投资者在公开交易前以固定价格购买股份，通常与长期业务合作绑定。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Embodied_intelligence">Embodied intelligence</a></li>
<li><a href="https://huggingface.co/blog/vlms">Vision Language Models Explained</a></li>
<li><a href="https://grokipedia.com/page/embodied_agent">Embodied agent</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#宇树科技`, `#具身智能`, `#人形机器人`, `#AI投资`

---

<a id="item-9"></a>
## [GPT-5 一周年，OpenAI 推出 Agent Plugins 开放标准](https://9to5mac.com/2026/08/06/gpt-5-turning-one-as-openai-shares-new-agent-plugins-standard/) ⭐️ 8.0/10

2026 年 8 月 6 日，OpenAI 发布了 Agent Plugins 开放标准，这是一种打包可复用 AI 代理组件的厂商中立标准，可移植为插件。其 1.0.0 规范定义了 Agent Skills 与 MCP 服务器的统一格式，项目由亚马逊、Cursor、微软、OpenAI 和 Vercel 组成的指导委员会公开治理。 此举意义重大，因为各 AI 代理客户端即使封装相同底层组件，也各自发展出了私有插件格式，导致生态碎片化。在亚马逊、微软等巨头支持下，统一标准能让代理扩展跨工具移植，降低开发者门槛并加速普及，尤其是在 GPT-5.6 和 GPT-6 暗示表明前沿快速推进的当下。 Agent Plugins 将 Agent Skills 与 MCP 服务器打包在一起，使兼容客户端能够统一发现并加载。过去一年，GPT-5 系列从 5.1 迭代到 5.6，苹果在 iOS 26 中将 GPT-5 接入 Apple Intelligence，Codex 应用在 7 月成为新的 ChatGPT 桌面客户端；OpenAI 还暗示了 GPT-6，但仅透露内部 Astra 模型解决了 10 个长期未决的数学和计算机科学问题，而 GPT-5.6 的发布曾因美国政府安全审查而短暂推迟。

telegram · zaihuapd · 8月7日 00:46

**背景**: AI 代理需要技能（如数据库连接器、浏览器自动化等模块化能力）和 MCP 服务器来连接外部工具。MCP 是 Anthropic 于 2024 年 11 月推出的开放标准，旨在规范 LLM 系统与数据和工具的集成方式。然而，各代理客户端都创建了自己的插件格式，导致很难跨产品打包、共享和版本化这些组件；Agent Plugins 正是为解决这一问题而生。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://open-plugins.com/">Open Plugins</a></li>
<li><a href="https://agent-plugins.org/">Agent Plugins</a></li>
<li><a href="https://9to5mac.com/2026/08/06/gpt-5-turning-one-as-openai-shares-new-agent-plugins-standard/">GPT-5 turning one as OpenAI shares new Agent Plugins standard</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#AI Agents`, `#标准`, `#GPT-5`, `#MCP`

---

<a id="item-10"></a>
## [阿里巴巴拟对下一代 Qwen 开源模型大型用户收费](https://www.reuters.com/business/retail-consumer/alibaba-plans-charge-big-users-its-next-open-source-ai-model-sources-say-2026-08-07/) ⭐️ 8.0/10

据两位知情人士透露，阿里巴巴计划对下一代 Qwen 开源 AI 模型的大型商业用户收取收入分成。这一做法与月之暗面（Moonshot）上个月为 Kimi K3 采用的许可模式类似。 这标志着阿里巴巴改变了此前允许开源模型在自有数据中心免费部署的政策，也表明中国 AI 厂商正在推动开源模型商业化变现。此举可能重塑开放权重模型的许可方式，并影响基于 Qwen 构建产品的企业。 具体的收入分成比例仍在讨论中。参照 Kimi K3 的许可条款，年收入超过 2000 万美元的服务商需要签署商业协议，据称分成比例最高可达 30%。

telegram · zaihuapd · 8月7日 01:29

**背景**: Qwen 是阿里云推出的大语言模型系列，此前许多 Qwen 模型以 Apache License 等免费许可发布，允许客户在自有数据中心部署。月之暗面的 Kimi K3 采用了定制化的开放权重许可，以收入规模作为商业协议触发条件，为原本开放的模型设置了变现先例。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Qwen">Qwen - Wikipedia</a></li>
<li><a href="https://github.com/MoonshotAI/Kimi-K3/blob/main/LICENSE">Kimi-K3/LICENSE at main · MoonshotAI/Kimi-K3 · GitHub</a></li>
<li><a href="https://www.digitalapplied.com/blog/kimi-k3-open-weights-shipped-license-restrictions-2026">Kimi K3 Open Weights Shipped: What the Licence Says</a></li>

</ul>
</details>

**标签**: `#AI`, `#Open Source`, `#Licensing`, `#Alibaba`, `#Qwen`

---