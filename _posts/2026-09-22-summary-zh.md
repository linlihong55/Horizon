---
layout: default
title: "Horizon Summary: 2026-09-22 (ZH)"
date: 2026-09-22
lang: zh
---

> 从 38 条内容中筛选出 5 条重要资讯。

---

1. [小米开源 MiMo-V2.6 Pro 与 Flash 混合专家模型](#item-1) ⭐️ 8.0/10
2. [NASA 火星采样返回任务实际已被取消](#item-2) ⭐️ 8.0/10
3. [Bryan Cantrill 剖析 Sun Microsystems 的致命失误](#item-3) ⭐️ 8.0/10
4. [TypeSafe AI 发布 Jev：输出类型化概率的“System One”决策模型](#item-4) ⭐️ 8.0/10
5. [SemiAnalysis 深度解析：将 MoE 模型映射到推理硬件](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [小米开源 MiMo-V2.6 Pro 与 Flash 混合专家模型](https://mimo.xiaomi.com/mimo-v2-6) ⭐️ 8.0/10

9 月 22 日，小米 MiMo 团队发布并开源 MiMo-V2.6 系列，包括旗舰级 MiMo-V2.6-Pro（总参数 1.02T、激活参数 42B）与主打效率的 MiMo-V2.6-Flash（总参数 309B、激活参数 15B），两者均为原生全模态模型，覆盖编程、电脑操作、3D 场景与视听内容创作等智能体任务。除模型权重外，小米还公开了异常详尽的技术报告、实时强化学习训练看板、约 7000 个多样化环境、完整强化学习框架，以及由 MiMo 训练轨迹蒸馏出的 Qwen 模型。 这次发布抬高了开源权重模型领域对“开放”的定义标准：小米不只是放出权重，还把强化学习过程公之于众，使其既是可用工具也是教学素材。它同时加剧了有关中国开源模型性价比优势的讨论——Flash 以 309B 的 MoE 架构号称在 SWE-Bench Verified 上达到 73.4%，并具备高推理速度，直接与西方前沿模型及开源模型展开竞争。 MiMo-V2.6-Pro 支持 100 万 token 上下文窗口，Flash 则在 SWE-Bench Verified 上以 73.4% 排名第一，推理速度约为每秒 150 token。小米表示面向高吞吐场景的 Pro-UltraSpeed 变体正在逐步推出，同等质量下输出速度最高可提升 20 倍；训练方案采用 MixRL 联合训练中等难度、可验证的代码与智能体任务，再把难验证或超长任务单独训练，并通过 MOPD 合并能力。MiMo 负责人罗福莉称，这可能是开源模型团队迄今按算力计规模最大的单次强化学习训练之一，其研发与工程挑战超过她此前参与的 DeepSeek R1。

hackernews · volf\_ · 9月21日 20:12 · [社区讨论](https://news.ycombinator.com/item?id=49792730)

**背景**: 混合专家（MoE）是一种模型架构，内部包含大量专门化的子网络（即“专家”）以及一个路由机制，每次输入只激活其中少数几个，因此模型可以拥有极大的总参数量，而每个 token 实际参与计算的参数更少、算力消耗也更低。这正是 MiMo-V2.6-Pro 能有 1.02T 总参数却只激活 42B、Flash 总参数 309B 只激活 15B 的原因。强化学习（RL）是后训练阶段，通过奖励机制让模型给出更好的答案和智能体行为；“开放权重”指训练好的参数可以下载，但训练数据与训练代码往往并不公开。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mimo.xiaomi.com/mimo-v2-6">MiMo - V 2 . 6 | Xiaomi</a></li>
<li><a href="https://mimo.mi.com/docs/en-US/news/latest/v2-6">Xiaomi MiMo Home</a></li>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论者普遍对联名透明度而非跑分成绩表示赞赏：有人称实时强化学习训练看板是“极佳的学习与教学工具”，也有人表示如今中国模型比美国模型更令其兴奋，主要原因是价格可负担。其他人则聚焦具体规格（Flash 309B/15B、Pro 1.02T/42B），也有人调侃这些模型生成的网页设计总爱用“01 - UPPERCASE TEXT”这套排版套路。

**标签**: `#LLM`, `#open-source-models`, `#Mixture-of-Experts`, `#model-release`, `#AI-research`

---

<a id="item-2"></a>
## [NASA 火星采样返回任务实际已被取消](https://www.science.org/content/article/nasa-s-mars-sample-return-mission-dead) ⭐️ 8.0/10

NASA 与 ESA 合作的火星采样返回（MSR）计划——即回收“毅力号”火星车所采集并缓存样本的任务——实际上已被取消。NASA 方面认定，原有方案的成本已膨胀到约 80 亿至 110 亿美元，且样本可能要到 2040 年前后才能送回地球。这一决定终结了 2022 年正式获批、最初设想在 2033 年前后带回火星样本的旗舰级任务。 火星采样返回被普遍视为未来十年行星科学的首要目标，其取消将重塑无人行星探测的未来格局，也影响主导该任务的 NASA 喷气推进实验室（JPL）的机构地位。与此同时，NASA 科学预算正承压，这一决定还可能把火星采样返回的首创优势拱手让给计划在 2028 至 2029 年发射窗口实施的中国“天问三号”。 原方案包含三个组成部分——作为采样火星车的“毅力号”、搭载火星上升器的样本回收着陆器，以及地球返回轨道器。批评者认为，JPL 是按照 Ariane 64 等传统运载火箭来设计任务的，而没有依托 Starship 或 New Glenn 这类成本更低、运力更大的商业火箭来降低费用与复杂度。作为规模对比，阿波罗任务带回了 842 磅（约 382 公斤）月球岩石，而 MSR 原本只打算带回约 1.1 磅（约 0.5 公斤）火星物质。

hackernews · Muhammad523 · 9月21日 19:14 · [社区讨论](https://news.ycombinator.com/item?id=49791939)

**背景**: 火星采样返回是一类拟议中的任务，目标是在火星上采集岩石、土壤和大气样本并带回地球，以便实验室进行远比任何星载仪器更深入的分析——尤其是检验火星历史上是否曾存在生命。NASA 与 ESA 于 2022 年联合批准了这一计划，基础是“毅力号”火星车已经封装好的样本管，并由喷气推进实验室（JPL，由加州理工学院管理的 NASA 联邦资助研发中心）牵头实施。对于火星样本可能对地球生物圈造成“反向污染”的担忧，一般被认为风险较低。与之竞争的方案包括中国的双次发射任务“天问三号”、俄罗斯的 Mars-Grunt，以及日本 JAXA 从火星卫星火卫一采样返回的 MMX 任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mars_sample-return_mission">Mars sample-return mission</a></li>
<li><a href="https://en.wikipedia.org/wiki/NASA-ESA_Mars_Sample_Return">NASA-ESA Mars Sample Return - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Jet_Propulsion_Laboratory">Jet Propulsion Laboratory - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者大多认为取消在财务上不可避免：有人称该任务“财务上根本不可行”，也有人认为 NASA 砍掉的正是 JPL 领导层推高到 110 亿美元、拖到 2040 年、并且绑定传统火箭而非 Starship 或 New Glenn 的旧架构。多位评论者提到国际上并行的努力，尤其是中国的“天问三号”（2028 年发射）以及一再推迟的 ExoMars“罗莎琳德·富兰克林”火星车——在失去俄罗斯火箭后现计划 2028 年发射。还有人指出，相比阿波罗带回的 842 磅月球样本，此次科学收获实在有限；也有人认为这篇文章不过是那些从旧 NASA 经费模式中获益的机构在“自我怜悯”。

**标签**: `#NASA`, `#Mars Sample Return`, `#space exploration`, `#JPL`, `#science policy`

---

<a id="item-3"></a>
## [Bryan Cantrill 剖析 Sun Microsystems 的致命失误](https://bcantrill.dtrace.org/2026/09/20/what-sun-got-wrong/) ⭐️ 8.0/10

DTrace 的创造者、Oxide Computer 联合创始人 Bryan Cantrill 于 2026 年 9 月 20 日在其 dtrace.org 博客上发表题为《What Sun got wrong》的文章，剖析了导致 Sun Microsystems 走向衰败的战略与技术失误。该文在 Hacker News 上引发了一个大型讨论帖（494 分、283 条评论），前员工与客户纷纷分享亲身经历。 Sun 曾是 Unix 工作站与服务器市场的主导厂商，也是 Java、NFS、ZFS 和 DTrace 的诞生地，因此它在 2010 年被 Oracle 收购的结局，长期被视为“技术领先者如何丢掉市场”的经典反面教材。这场讨论还保存了官方历史中很少记录的亲历者记忆——毕竟累计约有 23.5 万人曾以 Sun 员工的身份工作过。 评论者列举了若干具体决策，例如 Sun 在 2002 年短暂取消 Solaris 的 x86 版本，把客户推向了替代方案；以及 2002 年与 Google 的交易告吹，据称原因是 Sun 坚持要弄清 Google 究竟有多少台服务器。还有人指出，Sun 繁琐的报价与面谈式销售流程，与 Dell 次日送达、送货上门的模式形成了鲜明对比。

hackernews · chmaynard · 9月21日 14:03 · [社区讨论](https://news.ycombinator.com/item?id=49787436)

**背景**: Sun Microsystems 由 Andreas Bechtolsheim、Bill Joy、Vinod Khosla 和 Scott McNealy 于 1982 年创立，最初销售低成本、高性能的 Unix 工作站，1986 年上市，随后成长为以自家 SPARC 处理器和 Solaris 操作系统为核心的服务器领导厂商。Solaris 于 1993 年取代 SunOS，以可扩展性以及 DTrace、ZFS、容器等创新著称；Sun 于 2005 年将其大部分代码以 OpenSolaris 之名开源。Oracle 在 2010 年收购 Sun 后，Solaris 更名为 Oracle Solaris，OpenSolaris 被终止并催生了 Illumos 分支。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Sun_Microsystems">Sun Microsystems - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Solaris_operating_system">Solaris operating system</a></li>
<li><a href="https://spectrum.ieee.org/after-the-sun-microsystems-sets-the-real-stories-come-out">After the Sun (Microsystems) Sets, the Real Stories Come Out - IEEE Spectrum</a></li>

</ul>
</details>

**社区讨论**: 整体情绪交织着对 Sun 技术的赞赏与对其商业文化的无奈：一位采购者回忆说，仅一台 Alpha 服务器的导轨和电源线就比一台次日送达的完整 Dell 服务器还贵；另一位则把 2002 年取消 Solaris x86 版本和与 Google 的谈判破裂列为自伤之举。也有人怀念大学时代以终端为中心、启动虽慢但用起来畅快的 Sun 瘦客户机；还有评论者认为 Sun 从来就对经营企业缺乏兴趣，只关心打造顶尖技术，并忍受销售只是为了赚钱。

**标签**: `#sun-microsystems`, `#industry-history`, `#bryan-cantrill`, `#solaris`, `#business-strategy`

---

<a id="item-4"></a>
## [TypeSafe AI 发布 Jev：输出类型化概率的“System One”决策模型](https://simonwillison.net/2026/Sep/21/jev/) ⭐️ 8.0/10

TypeSafe AI 发布了其首个“System One 模型”Jev：它接收以“state”对象形式给出的非结构化文本输入，但不生成文本，而是返回类型化的概率结果，例如是/否的置信度分数、在所给选项上的概率分布，以及浮点评分。其定价为每百万输入 token 收费 0.042 美元且输出免费，比 OpenAI 的 GPT-5 Nano（每百万 0.05 美元）还要便宜。 Jev 预示着一种全新类别的模型，它面向软件直接调用而非对话场景，这可能让垃圾信息识别、打标签、优先级排序和搜索重排序等分类任务以远低的成本和更快的速度落地。但与此同时，它也让 AI 更加走向不透明的黑箱：当一个条目被判定为垃圾信息时，你只会得到一个数字，而无法得知是哪些内容信号导致了该判定。 Jev 接受的“状态”可以是字符串、字符串数组或一组名称-值对，只要放得进上下文窗口就可以提交任意多的问题，且所有问题并行评估，因此提交很多问题与提交一个问题的耗时大致相同。它支持三类问题：“Noul”是/否问题（返回 0 到 1 之间的伯努利概率）、返回选项概率分布的选择题，以及沿数值区间给出分数的评分题；该模型基于全新架构、并行采样器，以及 TypeSafe 称为“面向校准决策的强化学习”（RLCD）的训练方法。

rss · Simon Willison · 9月21日 23:09

**背景**: 传统 LLM 是“文本进、文本出”的、供人阅读的系统，而 System One 模型则被设计为直接输出可供其他软件消费的决策结果，这一命名呼应了 Daniel Kahneman 所描述的“系统 1”式快速直觉思维。TypeSafe AI 的名字借用了编程语言中的类型安全概念——把取值约束在声明好的类型上以便尽早发现错误；Jev 的输出同样被约束为浮点数与类别，而非自由文本。Simon Willison 指出，他更倾向于 Maggie Appleton 提出的“决策模型”（decision models）这一叫法，因为它更能说明这类模型实际在做什么。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://typesafe.ai/blog/introducing-system-one-models-and-jev">Introducing System One Models &amp; Jev - TypeSafe AI Blog</a></li>
<li><a href="https://en.wikipedia.org/wiki/Jev_%28AI_model%29">Jev (AI model) - Wikipedia</a></li>
<li><a href="https://docs.typesafe.ai/concepts/system-one">System One - TypeSafe AI</a></li>

</ul>
</details>

**标签**: `#LLM`, `#decision-models`, `#TypeSafe-AI`, `#Jev`, `#probabilistic-models`

---

<a id="item-5"></a>
## [SemiAnalysis 深度解析：将 MoE 模型映射到推理硬件](https://newsletter.semianalysis.com/p/computation-and-data-movement-for) ⭐️ 8.0/10

SemiAnalysis 发布了一篇题为《Computation and Data Movement for Inference》的技术深度文章，系统分析了混合专家（MoE）模型如何映射到推理硬件之上，内容涵盖模型结构、数据流动以及高效的服务化（serving）策略。文章的核心关注点在于支配 MoE 推理性能的两大瓶颈：计算与数据搬运。 MoE 已经成为前沿开源权重模型的主流架构，因为它把总参数量与单 token 计算量解耦；但同样的稀疏性使推理变得受内存带宽约束、难以高效服务化。随着越来越多机构发布大型 MoE 模型，理解专家、路由与权重搬运如何与加速器及互连相互作用，直接决定了部署方的服务成本、延迟与吞吐。 该分析强调，MoE 推理的瓶颈已从纯粹的浮点算力转向数据搬运：每个 token 只激活少数专家，因此权重需要在存储层级之间、甚至跨设备进行收集与交换，使内存带宽、缓存行为和 GPU 间通信成为限制因素。文章还讨论了专家并行（expert parallelism）与批处理等服务策略的权衡——更大的批次能提升效率，但会让路由和专家间的负载均衡更加复杂。

rss · Semianalysis · 9月21日 18:14

**背景**: 混合专家（MoE）是一种机器学习方法，它把模型拆分为多个“专家”子网络，每个专家擅长处理输入数据中的一部分，再由路由机制决定每个 token 交给哪些专家处理。由于每个 token 只激活少数专家，MoE 模型可以用远少于同等总规模稠密模型的计算量完成预训练，从而在相同算力预算下扩展参数量或数据量。难点在于推理：一个总参数量达 1320 亿、但每个 token 仅激活一小部分的模型，仍需存储并搬运全部权重，因此真正的约束是数据搬运而非算术运算——这也是机器学习系统研究中长期关注的问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained</a></li>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://www.ibm.com/think/topics/mixture-of-experts">What is mixture of experts? | IBM</a></li>

</ul>
</details>

**标签**: `#MoE`, `#inference`, `#hardware`, `#data movement`, `#ML systems`

---