---
layout: default
title: "Horizon Summary: 2026-10-17 (ZH)"
date: 2026-10-17
lang: zh
---

> 从 37 条内容中筛选出 7 条重要资讯。

---

1. [Claude 破解 NIST ECDSA 曲线种子起源之谜](#item-1) ⭐️ 8.0/10
2. [Jake Archibald 对比 JPEG XL 与 AVIF 在网页图片中的应用](#item-2) ⭐️ 8.0/10
3. [Claude Code 团队如何进行代码审查](#item-3) ⭐️ 8.0/10
4. [Mercor 研究：美国 90%的工作时长缺乏 AI 基准测试覆盖](#item-4) ⭐️ 8.0/10
5. [Big Fish：利用 OpenBSD 的 37 年内核漏洞](#item-5) ⭐️ 8.0/10
6. [ORL 让扩散语言模型提速，单张 RTX 5090 上达 2,788 tokens/s](#item-6) ⭐️ 8.0/10
7. [投资者将 Anthropic IPO 估值预期下调至约 1.5 万亿美元](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Claude 破解 NIST ECDSA 曲线种子起源之谜](https://www.anthropic.com/research/ecdsa-curve-origins) ⭐️ 8.0/10

Anthropic 前沿红队（Frontier Red Team）报告称，Claude 在不到半小时内找到了 NIST P-192、P-224、P-256、P-384 和 P-521 这几条曲线种子的来源：它们并非任何哈希算法的输出，而是 C 标准库中 lrand48 随机数生成器以一个 Unix 时间戳作为种子产生的输出。 这一发现解开了一个困扰密码学界数十年的谜团——当今部署最广泛的椭圆曲线标准的种子究竟是如何生成的；同时它也在很大程度上削弱了长期以来关于 NSA 刻意操纵 NIST 曲线、植入后门的阴谋论。它还是 AI 辅助研究攻克密码学长期未解难题的一次极具说服力的展示。 第五个二进制域种子 B-163 与 Claude 尝试过的任何方法都不吻合，至今仍无法解释。更关键的是，这一结果只确认了生成方法，而非筛选过程：由于被丢弃的候选时间戳无从查证，仍不能完全排除有人通过遍历时间戳来刻意挑选具备某种特定性质的曲线。

hackernews · ahlCVA · 10月16日 18:55 · [社区讨论](https://news.ycombinator.com/item?id=50122800)

**背景**: ECDSA 是使用最广泛的椭圆曲线密码标准；NIST 于 2000 年将其纳入 FIPS 186-2 数字签名标准，其中列出了一组不同规模和安全性等级的标准化曲线。为了让曲线具备“可验证随机性”，标准规定先对一个种子做哈希运算来导出曲线参数，这样任何人都能重跑计算、确认其中没有隐藏后门——但种子本身的来源从未公开。斯诺登事件以及 NSA 相关的 Dual\_EC\_DRBG 后门被曝光之后，外界的怀疑进一步加剧，许多人由此认定 NIST 曲线同样被刻意埋入了秘密弱点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/research/ecdsa-curve-origins">Claude reveals ECDSA curve origins \ Anthropic</a></li>
<li><a href="https://www.unite.ai/anthropic-says-claude-traced-nist-ecdsa-curve-seeds-to-a-1990s-rng/">Anthropic Says Claude Traced NIST ECDSA Curve Seeds to a ...</a></li>
<li><a href="https://www.explainx.ai/blog/claude-ecdsa-nist-curve-seeds-lrand48-anthropic-frontier-red-team-backdoor-question-2026">ECDSA Curve Seeds Solved: Claude Found lrand48 (2026 ...</a></li>

</ul>
</details>

**社区讨论**: 社区情绪在调侃与审慎之间：有评论调侃“为了一个 srand48\(time\(NULL\)，人们戴了 13 年锡箔帽”，也有人称这是“对整个一代 NIST 密码学阴谋论而言的毁灭性消息”。但主要反驳意见是：确认生成方法并不等于确认筛选过程——被丢弃的候选值无从查证，曲线仍可能是通过遍历时间戳刻意挑选出来的；另外也有人认为无法解释的 B-163 种子可能只是当年发布时数字被误打了一位。

**标签**: `#cryptography`, `#ECDSA`, `#NIST curves`, `#AI-assisted research`, `#security`

---

<a id="item-2"></a>
## [Jake Archibald 对比 JPEG XL 与 AVIF 在网页图片中的应用](https://jakearchibald.com/2026/jpeg-xl-vs-avif/) ⭐️ 8.0/10

网页性能专家 Jake Archibald 发布了一篇针对网页图片传输的技术对比文章，比较 JPEG XL 与 AVIF，并结合开发者实测的编码参数给出建议。该文章引发大量讨论（194 分、143 条评论），开发者在其中分享了具体的编码器配置，并就哪种编码格式最终胜出展开争论。 图片通常是网页体积中占比最大的部分，因此 JPEG XL 与 AVIF 之间的选择会直接影响大规模网站的加载速度、带宽成本以及 Core Web Vitals 指标。这一对比之所以重要，是因为两种格式目前各有取舍：AVIF 已在主流浏览器中广泛支持，而 JPEG XL 压缩率和功能更强，却缺乏广泛的浏览器原生支持。 JPEG XL 同时支持有损与无损压缩，设计目标是在无需硬件加速的情况下实现高效的软件编解码；而 AVIF 源自 AV1 视频编解码器，由开放媒体联盟（Alliance for Open Media）支持。社区成员指出，libjxl 在最高压缩努力级别下速度极慢——相比默认设置仅能让照片文件缩小 2–7%，却需要耗时 9–46 秒，主要原因是对感知误差指标 Butteraugli 进行迭代式优化循环，而替代编码器 jixel 可在几秒内达到相近效果。

hackernews · farlight · 10月16日 16:12 · [社区讨论](https://news.ycombinator.com/item?id=50120224)

**背景**: JPEG XL 是由联合图像专家组（JPEG）联合 Google 与 Cloudinary 开发的下一代图片格式，同时支持有损和无损压缩，单位体积下的画质明显优于老旧 JPEG。AVIF 是开放媒体联盟推出的 AV1 图像文件格式，使用 AV1 视频编解码器压缩静态图片，目前已获得大多数主流浏览器支持。两种格式要解决的是同一个问题：用更小的文件体积、在画质相当或更好的前提下取代已有数十年的 JPEG。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/JPEG_XL">JPEG XL - Wikipedia</a></li>
<li><a href="https://shortpixel.com/blog/what-is-avif-and-why-is-it-good/">What is AVIF and why is it good? - ShortPixel Blog</a></li>
<li><a href="https://jpeg.org/jpegxl/">JPEG - JPEG XL</a></li>

</ul>
</details>

**社区讨论**: 评论者大体认同这些技术取舍确实存在，但认为编码格式之争需要多年才能见分晓：有人解释 libjxl 最慢档位源于其基于 Butteraugli 的评估循环（并指出 jixel 快得多），也有人分享了一条经过实测、可保留 PNG 透明通道的 ffmpeg AVIF 命令。一位更谨慎的评论者回顾了 MP3/LAME 与 WebP 时代，提醒不要把任何早期的“赢家”结论奉为定论；还有评论者批评 AVIF 在文章所给 F1 示例图中明显抹掉了高光细节。

**标签**: `#image-compression`, `#jpeg-xl`, `#avif`, `#web-performance`, `#codecs`

---

<a id="item-3"></a>
## [Claude Code 团队如何进行代码审查](https://claude.dev/blog/solving-code-review-at-anthropic/) ⭐️ 8.0/10

Anthropic 的 Claude Code 团队介绍了一套自动化、由评估驱动的代码审查流程，最多只需一名人工审查员，这在 Hacker News 上引发了关于合规、内部风险和 AI 生成文本的尖锐争论。

hackernews · pretext · 10月16日 19:04 · [社区讨论](https://news.ycombinator.com/item?id=50122951)

**标签**: `#AI-assisted-code-review`, `#software-engineering-practices`, `#Anthropic`, `#SOC2-compliance`, `#developer-tooling`

---

<a id="item-4"></a>
## [Mercor 研究：美国 90%的工作时长缺乏 AI 基准测试覆盖](https://www.mercor.com/research/labor-index/benchmark-map/) ⭐️ 8.0/10

Mercor 发布了一份名为“Labor Index: Benchmark Map”（劳动力指数：基准测试地图）的研究，发现美国约 90%的工作时长花在现有 AI 基准测试几乎或完全没有覆盖的任务上。研究还指出，即便在控制了“AI 暴露度”之后，工资总额更高的职业所对应的 O\*NET 任务，在基准测试提示词中仍被显著过度代表。 如果基准测试主要衡量的是并不代表美国人实际工作内容的任务，那么排行榜分数和能力宣称可能很难反映真实的经济影响或自动化风险。这会削弱企业、政策制定者和 AI 实验室对模型“就绪程度”的判断，也意味着以基准测试驱动的“哪些工作有风险”的叙事，可能系统性地偏向高薪知识型工作。 读者提出的一个关键方法论疑问是：该研究似乎把“覆盖良好”用得很宽松，只要有少量提示词就算覆盖——有评论者指出，一个“社会工作者/护理—就育儿问题为家长提供咨询”的类别仅凭 13 条提示词就被标为“覆盖良好”。此外，该分析基于 O\*NET 职业任务分类体系和工资总额加权，因此其结论在很大程度上取决于覆盖阈值和 AI 暴露度控制变量的定义方式。

hackernews · speckx · 10月16日 17:08 · [社区讨论](https://news.ycombinator.com/item?id=50121179)

**背景**: AI 基准测试是用于比较模型能力并生成排行榜的标准化测试集，例如题库或任务提示词。O\*NET 是美国劳工部的职业数据库，把各类工作拆解成细颗粒度的任务，研究者借此把“AI 暴露度”映射到劳动力市场上。Mercor 是一家成立于 2023 年、总部位于旧金山的 AI 数据初创公司，为前沿 AI 实验室提供领域专家来做后训练工作，包括 RLHF、监督微调、模型评估和基准构建——这意味着基准测试在哪里存在空白，与它的商业利益直接相关。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.mercor.com/">Mercor | Organizing human intelligence to power the AI economy</a></li>
<li><a href="https://en.wikipedia.org/wiki/Mercor">Mercor - Wikipedia</a></li>
<li><a href="https://arxiv.org/html/2607.01254">The Benchmark Ceiling: Human Judgment, Evaluation Scarcity, and...</a></li>

</ul>
</details>

**社区讨论**: 评论者总体上认同这一发现有意义，但对其表述方式提出质疑：有人认为这类似于“门童谬误”（Doorman Fallacy）——自动化掉一个看似明显的任务，却摧毁了该员工同时提供的隐性价值；另有人指出“覆盖良好”实际上被当成了“有覆盖”的同义词。还有人把它与鲍莫尔成本病（Baumol&\#x27;s Cost Disease）联系起来——个体的效率提升会被周围难以自动化的活动（如做演示、写 Jira 工单、做 QA）吸收；也有人呼应 Karpathy 的说法，即 AI 目前实际只解决约 2-5%的工作，而重度使用者与几乎不用者之间的差距正在拉大。

**标签**: `#AI benchmarks`, `#labor economics`, `#AI evaluation`, `#future of work`, `#research analysis`

---

<a id="item-5"></a>
## [Big Fish：利用 OpenBSD 的 37 年内核漏洞](https://calif.io/research/big-fish) ⭐️ 8.0/10

一篇题为“Big Fish”的技术文章（发布于 calif.io/research/big-fish）详细介绍了如何利用 OpenBSD 中一个已有 37 年历史的内核漏洞，并讨论了这类长期存在的漏洞为何能逃过代码审查。文章给出了漏洞利用，并指出该漏洞在一个以重度审计著称的代码库中存活了数十年。 OpenBSD 被广泛视为以安全为核心的操作系统，因此一个存在 37 年的内核漏洞会动摇人们对仅靠代码审查即可保障安全的信心。该发现凸显了 fuzzing、静态分析和人工分析利用原语在发现深层内核漏洞方面的必要性，并可能影响人们对 OpenBSD 以及复用其代码的下游项目的信任。 社区讨论指出，同样的代码在 NetBSD 于 1999 年 8 月的一次重写中被意外修复，这有助于解释为何该漏洞在 OpenBSD 中持续存在，而在其姊妹 BSD 中未持续。该文章不仅是漏洞报告，还包含漏洞利用分析，评论者质疑 fuzzing 或静态分析能否现实地发现这一类漏洞。

hackernews · rs\_rs\_rs\_rs\_rs · 10月16日 14:44 · [社区讨论](https://news.ycombinator.com/item?id=50118977)

**背景**: OpenBSD 是一个以安全为核心的类 Unix 操作系统，基于 BSD，由 Theo de Raadt 于 1995 年从 NetBSD 1.0 分叉而来。该项目强调主动安全、正确性和代码审计，其代码被用于 macOS 的 PF 防火墙、Android 的 Bionic libc、LLVM 的正则表达式库以及 Windows 的 OpenSSH 等项目中。内核漏洞是操作系统核心中的缺陷，有时可被利用来令系统崩溃或提升权限。所谓已有 37 年历史的漏洞，意味着有问题代码早于 OpenBSD 本身，继承自更早的 BSD 源码，并经历了多次审计与重写仍未被发现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenBSD">OpenBSD</a></li>
<li><a href="https://www.openbsd.org/">OpenBSD</a></li>

</ul>
</details>

**社区讨论**: 评论者感叹该漏洞能在审计最严格的代码库之一中存活 37 年，并指出 NetBSD 在 1999 年的一次重写中意外修复了它。他们争论 fuzzing 或静态分析能否现实地发现这类漏洞，还是必须依靠人类对利用原语进行思考。也有人以轻松口吻称赞文章采用 OpenBSD Release 风格的图形，并期待主题曲。

**标签**: `#security`, `#openbsd`, `#kernel`, `#vulnerability`, `#exploit`

---

<a id="item-6"></a>
## [ORL 让扩散语言模型提速，单张 RTX 5090 上达 2,788 tokens/s](https://www.reddit.com/r/MachineLearning/comments/1x7qgr0/research_2788_tokenss_on_a_single_rtx_5090_with_a/) ⭐️ 8.0/10

研究者发布了 ORL（On-Policy Residual Learning，同策略残差学习），一种面向扩散语言模型的后期训练方法，让模型在每次去噪前向中确定更多 token，并配套推出自研推理引擎 dlmrt。实测结果是：LLaDA-2.1-mini + ORL 在单张 RTX 5090 上达到 2,788 tokens/s，DiffusionGemma 26B MoE + ORL 采用 NVFP4 在 8× B200 上达到 7,708 tokens/s；在他们从 Qwen3-4B 转换而来的 QwenDLM-4B 上，端到端吞吐提升约 6.9 倍，HumanEval pass@1 从 82.9% 提升到 89.6%。团队已将模型、训练代码、评测流程和推理引擎全部开源。 扩散语言模型一直宣称能并行生成 token，但很难把这种并行性转化为真实的墙钟时间加速；ORL 在减少前向次数的同时反而提升准确率，这可能让扩散语言模型成为自回归解码的现实替代方案。该工作还直接对标目前生产级服务栈（如 vLLM）中主流的加速手段——推测解码：在单张 H100 上、在测量精度相当的前提下，QwenDLM-4B + ORL 达到 1,298 tokens/s，而 DFlash 为 746 tokens/s、EAGLE3 为 405 tokens/s。 所有公布数字均为 batch size 1 的单请求解码，且是特定基准上的峰值成绩而非平均表现；比较属于端到端系统级对比，其中 ORL 使用 dlmrt，而推测解码基线运行在 vLLM 上。训练效率同样值得关注：LLaDA-2.1-mini 的后训练仅需 420 万个自生成训练 token 和 36 个 H100 GPU 小时，团队还围绕高效的残差状态捕获、专用注意力 kernel 和计算均衡打包共同设计了训练系统，使训练步速最高提升 5.2 倍。

reddit · r/MachineLearning · /u/arty\_photography · 10月16日 20:03

**背景**: 自回归大模型一次只生成一个 token，因此每生成一个 token 都要付出一次完整前向的代价。扩散语言模型则从噪声或掩码出发，并行地对一整块 token 迭代去噪，一次细化多个位置——但只有当模型能用更少的去噪步数收敛时，它才真正更快。ORL 针对这一场景中的两个问题：跨去噪步携带的残差状态由模型自身产生，其分布在训练中会漂移（因此作者使用当前模型新生成的同策略轨迹训练，而非陈旧的离线残差）；同时，仅监督最终输出并不能教会模型更快收敛，他们提出的 Adjacent Entropy Contraction 损失通过奖励每一步降低不确定性的行为来解决这一点，并对已经高置信的预测加门控以避免无谓的推动。dlmrt 则在系统层面配合算法：它把整个去噪循环捕获进 CUDA graph，使其在 GPU 上执行，避免每步由 CPU 发起与同步的开销，并支持 Blackwell GPU（包括消费级 RTX 5090）上的 NVFP4 推理。

**标签**: `#diffusion-language-models`, `#llm-inference`, `#model-optimization`, `#open-source`, `#machine-learning-research`

---

<a id="item-7"></a>
## [投资者将 Anthropic IPO 估值预期下调至约 1.5 万亿美元](https://www.reuters.com/business/finance/investors-temper-anthropic-ipo-valuation-expectations-over-revenue-growth-2026-10-15/) ⭐️ 8.0/10

Anthropic 第三季度营收达 168 亿美元，环比增长 45%，并实现经调整后盈利和季度现金流转正；但部分投资者仍将其 IPO 估值预期从 2 万亿美元下调至约 1.5 万亿美元。此次下调的原因包括增速放缓、前沿模型之间的价格竞争加剧，以及算力投入带来的持续压力。 这一调整表明，公开市场投资者开始以更严格的标准审视 AI 公司的增长质量、利润率和资本效率，而不再单纯为营收增长买单。它可能成为智谱、MiniMax、Kimi 和 DeepSeek 等 AI 公司的估值压力测试，市场关注点将更多转向收入持续性、毛利率和资本效率。 即便营收环比增长 45% 且现金流转正，估值预期的下调说明投资者折价的是未来增速预期，而非当下的业绩表现。文中列出的三个驱动因素——增速放缓、模型价格竞争加剧和巨额算力资本开支——同样也是大多数大模型开发商面临的普遍压力。

telegram · zaihuapd · 10月16日 15:46

**背景**: Anthropic 是一家 AI 公司，以开发 Claude 系列大语言模型而闻名，IPO 意味着其股票将首次在公开交易所上市。上市前的估值预期反映的是投资者认为该公司值多少钱，会随着新披露的财务数据和市场情绪而上下浮动。训练和运行前沿 AI 模型需要消耗海量算力，因此算力开支是决定这类公司能否把营收增长转化为可持续利润的核心因素。

**标签**: `#Anthropic`, `#IPO`, `#AI industry`, `#valuation`, `#AI investment`

---