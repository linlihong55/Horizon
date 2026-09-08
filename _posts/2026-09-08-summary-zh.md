---
layout: default
title: "Horizon Summary: 2026-09-08 (ZH)"
date: 2026-09-08
lang: zh
---

> 从 32 条内容中筛选出 5 条重要资讯。

---

1. [LLM 引导的程序演化刷新 10 项圆填充最优解](#item-1) ⭐️ 9.0/10
2. [TPU 推理外部化加速：InferenceX 显示 Ironwood 每美元性能提升最高 50%](#item-2) ⭐️ 8.0/10
3. [用 31,352 次重复基准测试测量 LLM 性能漂移](#item-3) ⭐️ 8.0/10
4. [华为时隔六年推出麒麟 9050 Pro，首款逻辑折叠芯片](#item-4) ⭐️ 8.0/10
5. [最高法发布 AI 纠纷司法解释 明确换脸与算法杀熟责任](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [LLM 引导的程序演化刷新 10 项圆填充最优解](https://www.reddit.com/r/MachineLearning/comments/1w9xlyi/llmguided_program_evolution_improves_10_bestknown/) ⭐️ 9.0/10

一个名为 Discovery Loop 的系统没有直接求解圆填充问题，而是利用 LLM 引导的程序演化来迭代改进优化算法。在 Packomania csqv 基准上，它使 N 在 101 到 114 之间的 10 个规模的最佳已知半径和提升了 2.4% 至 5.4%，共迭代 15 次，LLM 总成本为 27.72 美元。 这项工作表明，LLM 不仅能生成代码，还能自主发现超越现有基准的算法改进。由于 Packomania 已独立验证并接受这些结果，它为 AI 驱动的算法发现与优化提供了一条可信且低成本的路径。 该系统从一个简单的种子求解器出发，让 LLM 根据成绩板和过往尝试历史提出算法修改。每个候选方案都由独立验证器评分，因此改进会被保留、失败会被丢弃；作者特别指出“平台期检测停止规则”是他最希望被批评指正的部分。

reddit · r/MachineLearning · /u/SIGH\_I\_CALL · 9月7日 16:54

**背景**: Packomania csqv 基准是一个经典的圆填充问题：在单位正方形内放置 N 个可变半径的圆，使半径之和最大化，这常被称为半径和变体。LLM 引导的程序演化是一种新兴方法，让大语言模型直接修改和提出代码，并通过评分系统的适应度反馈来引导选择。类似的思路，例如 LLM Guided Evolution 框架中的方法，曾被 DeepMind 的 AlphaEvolve 引用，并用于演化出精度更高的神经网络结构。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2609.05093">[2609.05093] LLM-Guided Program Evolution for Circle Packing: Breaking 10 Packomania Records for $28</a></li>
<li><a href="https://arxiv.org/html/2609.05093">LLM-Guided Program Evolution for Circle Packing:Breaking 10 Packomania Records for $28</a></li>

</ul>
</details>

**标签**: `#LLM`, `#program evolution`, `#optimization`, `#circle-packing`, `#benchmark`

---

<a id="item-2"></a>
## [TPU 推理外部化加速：InferenceX 显示 Ironwood 每美元性能提升最高 50%](https://newsletter.semianalysis.com/p/tpu-inferencex-full-steam) ⭐️ 8.0/10

SemiAnalysis 通过 InferenceX 官方预览版首次发布了谷歌 TPUv7 Ironwood 的第三方推理基准结果。在与 NVIDIA B200/B300 的可比测试中，Ironwood 的每美元性能最高提升 50%，该结论同时基于谷歌内部 TCO 和外部客户 TCO 得出。 这标志着谷歌 TPU 栈正在快速外部化：Ironwood 是谷歌首个主动面向他人的推理工作负载销售或出租的 TPU 世代，而不只是内部使用。这样的性价比优势可能显著削弱 NVIDIA CUDA 在 AI 硬件生态中的竞争护城河。 InferenceX 基准覆盖了 Pareto 前沿的大部分区域，并从两个角度评估经济性：谷歌内部 TCO 和真实客户支付的外部 TCO。需注意，新闻标签中写的是“TPUv8i”，但官方文档将 Ironwood 标识为第七代 TPU，即 TPUv7。

rss · Semianalysis · 9月7日 20:00

**背景**: TPU 是谷歌为神经网络工作负载定制的专用集成电路（ASIC），常被用于基于 Transformer 的大语言模型推理。InferenceX 是 SemiAnalysis 推出的开放、可复现基准套件，随 GPU、TPU、LPU 及软件栈的演进持续更新。Ironwood 专为高吞吐、低延迟推理设计，由两个独立 chiplet 组成，每个 chiplet 具有独立内存空间。谷歌表示 Ironwood 将在 Google Cloud 上正式可用，也可直接购买。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://newsletter.semianalysis.com/p/tpu-inferencex-full-steam">TPU Inference Externalization Full Steam Ahead - InferenceX</a></li>
<li><a href="https://docs.cloud.google.com/tpu/docs/tpu7x">TPU7x (Ironwood) | Google Cloud Documentation</a></li>
<li><a href="https://cloud.google.com/blog/products/compute/ironwood-tpus-and-new-axion-based-vms-for-your-ai-workloads">Ironwood TPUs and new Axion-based VMs for your AI workloads | Google Cloud Blog</a></li>

</ul>
</details>

**标签**: `#TPU`, `#Inference`, `#AI Hardware`, `#CUDA`, `#Cloud Computing`

---

<a id="item-3"></a>
## [用 31,352 次重复基准测试测量 LLM 性能漂移](https://www.reddit.com/r/MachineLearning/comments/1w9llr4/measuring_llm_performance_drift_observations_and/) ⭐️ 8.0/10

AI Stupid Level 团队对 49 个大语言模型进行了 31,352 次重复基准观察，发现日间方差（8.43 分）约为日内方差（2.80 分）的 3 倍，表明同一名称背后的模型会发生静态排行榜无法捕捉的变化。这项研究将基准测试视为纵向时间序列测量，而非一次性排名。 这一发现很重要，因为 API 提供的 LLM 可能在版本、基础设施或配置变更时悄然发生变化，因此依赖静态基准分数来选择模型或用于生产系统可能会产生误导。纵向基准测试为监控漂移、发现性能回退以及随时间验证行为提供了一种更可靠的方法。 该方法论将基准配置进行版本化管理，仅比较兼容测量条件下产生的观察结果，并尽可能使用基于执行的评估而不是 LLM 评判。它还将可用性和基础设施故障与有效的任务结果区分开来，并对生成的时间序列进行变化检测，以标记真正的模型漂移。

reddit · r/MachineLearning · /u/ionutvi · 9月7日 07:44

**背景**: 传统的 LLM 基准测试往往是快照式的：模型被评估一次，分数被公布，然后被视为该模型的稳定属性。然而，API 提供的模型可能会因基础设施、配置或版本更新而在同一模型名称背后发生变化，因此静态排行榜上的数字可能无法反映随时间变化的真实行为。纵向基准测试则相反，它在版本受控的条件下重复跟踪同一模型，并将结果与该模型自身的基线进行比较。该帖还讨论了相关的基准污染问题：公开每一道实时任务、提示变换或隐藏测试，都会改变该基准本应测量的对象。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://data-today.net/llm-performance-drift-benchmark-variance/">LLM performance drift : why your benchmark scores... | Data Today</a></li>
<li><a href="https://www.logicmonitor.com/blog/llms-dont-stand-still-how-to-monitor-and-trust-the-models-powering-your-ai">How to Monitor and Trust the LLMs Powering Your AI | LogicMonitor</a></li>
<li><a href="https://arxiv.org/html/2508.05452v1">LLMEval-3: A Large-Scale Longitudinal Study on Robust and ...</a></li>

</ul>
</details>

**标签**: `#LLM`, `#benchmarking`, `#performance drift`, `#evaluation`, `#MLOps`

---

<a id="item-4"></a>
## [华为时隔六年推出麒麟 9050 Pro，首款逻辑折叠芯片](https://www.news.cn/20260907/adf46c5c003240d28cc3cf6de54f9b5f/c.html) ⭐️ 8.0/10

9 月 7 日，华为发布了搭载全新麒麟 9050 Pro 芯片的 Mate XT 2 三折叠手机。这是首款采用逻辑折叠技术的高性能芯片，也是继 Mate 40 发布之后，华为时隔六年再次推出全新旗舰麒麟处理器。 此次发布结束了华为旗舰芯片长达六年的空窗期，标志着其在传统平面芯片设计之外迈出了重要一步。它可能重塑后摩尔时代半导体发展的预期，并增强华为在高端智能手机和先进封装领域与对手竞争的地位。 麒麟 9050 Pro 在单芯片内将逻辑单元分层排布，并增设垂直互联通道，从而缩短信号传输路径、降低时延。得益于晶圆对晶圆混合键合形成的双层垂直立体架构，Mate XT 2 整机性能相比 Mate XTs 提升了 42%。

telegram · zaihuapd · 9月7日 08:20

**背景**: 逻辑折叠技术是华为在 ISCAS 2026 上随“韬\(τ\)定律”一同提出的半导体创新技术，属于三维集成电路（3D IC）与先进封装技术范畴。它通过细粒度动态重构实现硬件资源的时间复用，以应对后摩尔时代的面积效率需求。传统芯片将逻辑单元放在单一平面上，而逻辑折叠将这些单元在芯片内垂直排布，如同从“平层”升级为“复式”，并通过垂直互联通道形成“电梯”式连接。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ithome.com/0/999/300.htm">华为继 Mate 40 后时隔六年再次发布高性能芯片，麒麟 9050 Pro 首发逻辑折叠技术 - IT之家</a></li>
<li><a href="https://i.ifeng.com/c/8w8hG82QYNl">全球首款逻辑折叠芯片！麒麟9050 Pro本月登场：华为三折叠首发_凤凰网</a></li>
<li><a href="https://zhuanlan.zhihu.com/p/2042626173432328269">陈巍：一文看懂逻辑折叠（logic folding）背后的关键技术和产业玩家</a></li>

</ul>
</details>

**标签**: `#Huawei`, `#semiconductor`, `#Kirin`, `#smartphone`, `#technology`

---

<a id="item-5"></a>
## [最高法发布 AI 纠纷司法解释 明确换脸与算法杀熟责任](https://www.cnr.cn/news/20260907/t20260907_527806795.shtml) ⭐️ 8.0/10

9 月 7 日，最高人民法院发布人工智能纠纷案件司法解释，共 5 部分 24 条，聚焦 AI 换脸、算法杀熟、冒充他人代言、自动驾驶和知识产权等问题。解释明确，未经同意用 AI 制作可识别的人脸、声音等可能构成人格权侵权，算法价格歧视侵害消费者权益的应承担责任。 这一司法解释为中国 AI 相关损害确立了法律问责规则，为深度伪造、算法公平和 AI 冒充他人等问题设立了具有影响力的先例。它将直接影响在中国运营或与中国合作的人工智能开发者、科技平台及企业，并可能通过展示自上而下的监管路径来影响全球 AI 治理讨论。 解释明确，AI 冒充他人代言诱导消费的，可依法支持惩罚性赔偿请求。解释还依法规制利用人工智能实施“开盒”“人肉搜索”等侵害自然人隐私权的行为，将既有法律原则适用于 AI 驱动的不法行为。

telegram · zaihuapd · 9月7日 09:32

**背景**: 中国法律体系中已有“算法杀熟”（平台对老客户定价高于新客户）和“开盒”（通过非法手段获取并公开他人隐私信息的网络暴力，是人肉搜索的升级版）等概念。惩罚性赔偿是指超过实际损失范围、用于惩罚性质恶劣行为的额外赔偿。此次司法解释将这些既有法律概念扩展到 AI 换脸、AI 冒充代言和算法定价等 AI 特定场景，填补了快速发展的技术领域中的法律空白。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bswxw.org.cn/web/article/1493984301637644288/web/content_1493984301637644288.html">莫让 算 法 “ 杀 熟 ”寒了人心-璧山网</a></li>
<li><a href="https://baike.baidu.com/item/%E5%BC%80%E7%9B%92/58943997">开盒（网络热词）_百度百科</a></li>
<li><a href="https://zh.wikipedia.org/zh-hans/%E6%87%B2%E7%BD%B0%E6%80%A7%E8%B3%A0%E5%84%9F">惩罚性赔偿 - 维基百科，自由的百科全书</a></li>

</ul>
</details>

**标签**: `#AI governance`, `#legal regulation`, `#deepfake`, `#algorithmic fairness`, `#privacy`

---