---
layout: default
title: "Horizon Summary: 2026-07-28 (ZH)"
date: 2026-07-28
lang: zh
---

> 从 29 条内容中筛选出 10 条重要资讯。

---

1. [月之暗面开源 Kimi K3：2.8 万亿参数模型](#item-1) ⭐️ 10.0/10
2. [vLLM v0.26.0 发布：支持 Inkling 模型、DeepSeek-V4 优化、fp32 lm\_head](#item-2) ⭐️ 9.0/10
3. [Anthropic 明确对开源权重模型的立场](#item-3) ⭐️ 8.0/10
4. [法官驳回谷歌利用 DMCA 阻止爬取搜索结果的尝试](#item-4) ⭐️ 8.0/10
5. [Paged Out \#9：免费技术杂志赢得黑客社区喜爱](#item-5) ⭐️ 8.0/10
6. [提出机器学习训练前数据审计门控机制](#item-6) ⭐️ 8.0/10
7. [谷歌透露 Gemini 4 为迄今最雄心预训练](#item-7) ⭐️ 8.0/10
8. [Fastjson2 曝出严重远程代码执行漏洞，尚无补丁](#item-8) ⭐️ 8.0/10
9. [中方驳斥美方以模型蒸馏为由制裁中国 AI 企业](#item-9) ⭐️ 8.0/10
10. [中国开始量产国产 DUV 光刻机](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [月之暗面开源 Kimi K3：2.8 万亿参数模型](https://huggingface.co/moonshotai/Kimi-K3) ⭐️ 10.0/10

月之暗面（Moonshot AI）发布了 Kimi K3 的权重，这是首个开放权重的 2.8 万亿参数模型，激活参数为 1040 亿，采用 896 个专家的新型混合专家（MoE）架构。 这标志着开放 AI 研究的重大里程碑，因为 K3 与 GPT-5.6 Sol 和 Claude Fable 5 等专有前沿模型竞争，同时可自由下载和部署。 该模型使用 Kimi Delta Attention \(KDA\) 和 Attention Residuals \(AttnRes\) 实现高效线性注意力机制，采用 Stable LatentMoE 框架，每个 token 激活 896 个专家中的 16 个，支持 100 万 token 上下文窗口和 MXFP4 量化。许可协议对大规模商业使用施加了限制。

telegram · zaihuapd · 7月27日 15:15

**背景**: 大型语言模型通常有数十亿参数，但 K3 达到了万亿级别。混合专家（MoE）模型每个 token 只激活部分参数，以平衡规模和计算成本。KDA 是一种线性注意力机制，相比标准 softmax 注意力可减少内存使用。MXFP4 是一种 4 位浮点格式，能大幅减小模型尺寸而不显著损失精度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.kimi.com/blog/kimi-k3">Kimi K3 Tech Blog: Open Frontier Intelligence</a></li>
<li><a href="https://huggingface.co/blog/RakshitAralimatti/learn-ai-with-me">What’s MXFP4? The 4-Bit Secret Powering OpenAI’s GPT‑OSS Models on Modest Hardware</a></li>

</ul>
</details>

**社区讨论**: 根据提供的 RSS 内容和评论（来自 Simon Willison），社区指出 K3 的许可协议比 K2 更严格，要求大型“模型即服务”业务另行签订协议。月之暗面并未称其为“开源”，而是“开放权重”。OpenRouter 已从多家提供商提供 K3，定价具有竞争力。

**标签**: `#open-source`, `#large language model`, `#Moonshot AI`, `#2.8 trillion parameters`, `#MoE`

---

<a id="item-2"></a>
## [vLLM v0.26.0 发布：支持 Inkling 模型、DeepSeek-V4 优化、fp32 lm\_head](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 9.0/10

vLLM v0.26.0 引入了对 Inkling 模型家族的支持（975B MoE、多模态、1M 上下文），并对 DeepSeek-V4 进行了显著的性能改进，包括专门的路由内核和 fused\_topk\_bias。此外，还通过 head\_dtype 为生成模型添加了 fp32 lm\_head 支持，并允许按 KV-cache 组灵活选择注意力后端。 此版本极大地扩展了 vLLM 的模型支持和推理性能，使 Inkling 和 DeepSeek-V4 等大规模 MoE 模型用户受益。fp32 lm\_head 和灵活的注意力后端提高了混合模型的准确性和适应性，巩固了 vLLM 作为领先 LLM 推理引擎的地位。 此版本包含来自 212 位贡献者的 411 次提交，其中 61 位是新贡献者。新增模型包括 Inkling 系列、BertForMaskedLM 和 RobertaForTokenClassification。KV 卸载和分层辅助存储得到显著完善，Rust 前端增加了多模态视频和音频支持。

github · khluu · 7月27日 01:06

**背景**: vLLM 是一个用于快速 LLM 推理和服务的开源库，支持多种模型架构和量化方法。Inkling 模型是由 Thinking Machines Lab 开发的 975B 参数混合专家模型，具有多模态输入和 1M 上下文窗口。DeepSeek-V4 是 DeepSeek 系列的最新迭代，是一个大型 MoE 模型。FP32 lm\_head 指对语言模型头使用 float32 精度以提高生成准确性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://inkling-model.com/">Inkling Model : Architecture, Capabilities, Context &amp; Access</a></li>
<li><a href="https://www.digitalocean.com/community/tutorials/flashattention-4-llm-inference-optimization">FlashAttention 4: Faster, Memory-Efficient Attention for... | DigitalOcean</a></li>
<li><a href="https://www.spheron.network/blog/nvfp4-vs-mxfp4-gpu-cloud-4bit-quantization-guide/">NVFP 4 vs MXFP4: 4-Bit Quantization Format Decision... | Spheron Blog</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#release`, `#performance optimization`, `#AI infrastructure`

---

<a id="item-3"></a>
## [Anthropic 明确对开源权重模型的立场](https://www.anthropic.com/news/position-open-weights-models) ⭐️ 8.0/10

Anthropic 发布了一份立场声明，澄清他们并不主张禁止开源权重模型，但支持对所有足够强大的模型（包括开放和封闭模型）进行强制安全测试。 这一立场影响了当前关于 AI 监管的辩论，因为如果测试要求变得难以承受或被选择性执行，强制安全测试可能实际上限制开源权重模型，并为未来监管树立先例。 该声明由 Anthropic 首席执行官 Dario Amodei 撰写，并包括对禁止向中国出售芯片等措施的支持，批评者认为这与不主张禁令的说法相矛盾。

hackernews · surprisetalk · 7月27日 22:03 · [社区讨论](https://news.ycombinator.com/item?id=49076057)

**背景**: 开源权重模型是其训练参数（权重）公开的 AI 模型，允许任何人下载、运行并在自己的硬件上进行微调。与完全开源的 AI 不同，开源权重模型可能不包括训练数据、代码或文档。这场辩论的核心在于这些模型是否应在发布前接受安全测试以防止滥用，人们担心这种测试可能被用作开放获取的障碍。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>
<li><a href="https://opensource.org/ai/open-weights">Open Weights: not quite what you’ve been told</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍批评 Anthropic 的立场，认为强制安全测试实际上等同于禁令，并引用了历史上通过认证流程限制准入的例子。其他人指出，支持硬件禁令的同时反对软件禁令存在不一致，并质疑 Anthropic 因其商业利益而动机不纯。

**标签**: `#AI safety`, `#open-weights`, `#regulation`, `#Anthropic`, `#open source`

---

<a id="item-4"></a>
## [法官驳回谷歌利用 DMCA 阻止爬取搜索结果的尝试](https://www.techdirt.com/2026/07/27/judge-rejects-googles-attempt-to-dmca-its-way-out-of-being-scraped/) ⭐️ 8.0/10

一名法官裁定，谷歌试图利用《数字千年版权法》（DMCA）阻止对其搜索结果的爬取是无效的。这一裁决是对谷歌起诉 SerpAPI（一家爬取谷歌搜索结果的第三方服务）一案的回应。 这一裁决确立了重要法律先例，即 DMCA 不能保护搜索引擎免受爬取，可能影响大型科技公司保护其数据的方式。同时，这也凸显了谷歌自身网络爬取起源与其当前限制搜索结果访问之间的紧张关系。 法官认为，谷歌的搜索结果不具备 DMCA 要求的原创性或创造性选择，因此不属于可版权保护的汇编。该案未涉及其他法律依据（如违约或非法侵入），为未来的诉讼留下了空间。

hackernews · cdrnsf · 7月27日 18:15 · [社区讨论](https://news.ycombinator.com/item?id=49073513)

**背景**: 《数字千年版权法》（DMCA）是美国版权法，用于保护控制访问版权作品的技术措施。网络爬取，即自动收集网站数据，一直是一个法律争议领域，法院通常裁定爬取公共数据不违反《计算机欺诈和滥用法》（CFAA）。但在此之前，DMCA 对搜索引擎结果页面的适用性尚不明确。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Digital_Millennium_Copyright_Act">Digital Millennium Copyright Act - Wikipedia</a></li>
<li><a href="https://blog.apify.com/is-web-scraping-legal/">Is web scraping legal? Yes, if you know the rules.</a></li>

</ul>
</details>

**社区讨论**: 社区评论强烈批评谷歌的行为，许多人指出谷歌本身建立在爬取网络的基础上，现在却试图阻止爬取的讽刺之处。一些人强调缺乏良好的 API 是推动爬取的原因，另一些人指出了版权法在司法管辖区之间的差异。还有评论提到爬取对于打击广告骗局的重要性。

**标签**: `#web scraping`, `#DMCA`, `#Google`, `#legal`, `#APIs`

---

<a id="item-5"></a>
## [Paged Out \#9：免费技术杂志赢得黑客社区喜爱](https://pagedout.institute/download/PagedOut_009.pdf) ⭐️ 8.0/10

Paged Out \#9 是一本免费且设计精美的技术杂志，包含关于 C 语言编程、子像素渲染、可计算镶嵌等深度、充满黑客好奇心的文章。它以 PDF 形式发布，并提供可购买的印刷版。 这本杂志复兴了 2600 和 Phrack 等经典黑客杂志的精神，免费提供高质量的技术内容，这在当今的出版界中十分罕见。它培养了一个由好奇的程序员和工程师组成的社区，他们热衷于深入探讨冷门话题。 该杂志由 Paged Out 研究所出版，可免费下载。社区评论特别提到了《C 语言的婴儿步骤》、《子像素动物园》以及一篇关于可计算镶嵌的文章，该文章重新发现了 1960 年代 Wang 的工作。

hackernews · laurensr · 7月27日 14:22 · [社区讨论](https://news.ycombinator.com/item?id=49070138)

**背景**: 子像素渲染是一种利用显示器中独立的红、绿、蓝子像素来提高有效分辨率的技术，常用于文本清晰度。可计算镶嵌由 Wang 在 1960 年代研究，将多米诺骨牌问题（一组瓷砖能否铺满平面）与停机问题联系起来，表明镶嵌具有计算完备性。这些主题在杂志的文章中有所探讨。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Subpixel_rendering">Subpixel rendering</a></li>
<li><a href="https://dl.ifip.org/db/conf/ifipTCS/ifipTCS2008/LafitteW08.pdf">Computability of Tilings .</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了对杂志内容和设计的热情，将其与经典杂志进行比较。一位用户指出一个有趣的事实：可计算镶嵌文章是未注明出处地重新发现了 Wang 的工作，将多米诺骨牌问题与停机问题联系起来。其他用户则对《C 语言的婴儿步骤》文章感到好笑，并计划购买印刷版。

**标签**: `#magazine`, `#hacker`, `#technical`, `#free`, `#programming`

---

<a id="item-6"></a>
## [提出机器学习训练前数据审计门控机制](https://www.reddit.com/r/MachineLearning/comments/1v8a3nu/training_data_needs_a_real_gonogo_gate_before/) ⭐️ 8.0/10

一位 Reddit 用户提出了一套正式、可复现的训练前数据审计系统，该系统基于数据泄露、矛盾、冗余和覆盖等明确证据来控制训练流程，且不依赖大语言模型做出判决。 这一概念通过增加训练前的严格门控，弥补了机器学习流程中的一个关键缺口，有望提升可复现性、减少失败，并增强模型开发的信任度。 该系统输出 PASS、WARNING、FAIL 或 FAIL\_SECURITY 等判决，并可生成修复方案，仅对衍生副本应用经批准的修改，同时保留原始数据。系统通过清单和校验和实现可追溯性。

reddit · r/MachineLearning · /u/jesusmjk · 7月27日 19:13

**背景**: 机器学习中的数据泄露指训练数据包含预测时无法获得的信息，导致性能估计过于乐观。矛盾检测识别数据集中或跨数据集的冲突数据点。数据溯源追踪数据在机器学习生命周期中的来源和转换过程。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Leakage_%28machine_learning%29">Leakage (machine learning) - Wikipedia</a></li>
<li><a href="https://www.shadecoder.com/topics/contradiction-detection-a-comprehensive-guide-for-2025">Contradiction Detection: A Comprehensive Guide for 2025 - Shadecoder - 100% Invisibile AI Coding Interview Copilot</a></li>
<li><a href="https://mlip-cmu.github.io/s2023/slides/21_provenance/provenance.pdf">Versioning, Provenance</a></li>

</ul>
</details>

**标签**: `#machine learning`, `#data quality`, `#training data`, `#MLOps`, `#reproducibility`

---

<a id="item-7"></a>
## [谷歌透露 Gemini 4 为迄今最雄心预训练](https://9to5google.com/2026/07/26/google-gemini-4-teases/) ⭐️ 8.0/10

谷歌 CEO Sundar Pichai 在 Alphabet 2026 年第二季度财报电话会议上宣布，下一代大模型 Gemini 4 已开始训练，称其为公司迄今为止最雄心勃勃的预训练项目。该模型预计于 2026 年底发布，可能在 11 月或 12 月。 这表明谷歌继续保持引领 AI 前沿的承诺，Gemini 4 旨在超越前代模型取得重大进展。其发布可能影响大语言模型的竞争格局，并加速通用人工智能（AGI）的发展。 Pichai 强调，算力资源将优先用于前沿 AGI 研发，以确保 Gemini 4 发布时仍处于行业前沿。此外，Gemini 3.x Flash 系列将保持几乎每月一次的迭代频率，重点提升智能编码等能力。

telegram · zaihuapd · 7月27日 04:06

**背景**: Gemini 是谷歌的大语言模型系列，与 OpenAI 的 GPT 系列竞争。预训练是指在大量无标签数据上训练模型以学习通用语言模式，然后再针对特定任务进行微调。谷歌的目标是实现通用人工智能（AGI），即 AI 能完成人类可以完成的任何智力任务。

**标签**: `#Gemini`, `#AI`, `#Google`, `#Large Language Model`, `#AGI`

---

<a id="item-8"></a>
## [Fastjson2 曝出严重远程代码执行漏洞，尚无补丁](https://mp.weixin.qq.com/s/LJaul1jNjK9pXRAkoUiMEA) ⭐️ 8.0/10

2024 年 7 月 27 日，长亭科技披露了 Fastjson2 中的一个远程代码执行漏洞，影响 2.0.62 及之前所有版本。攻击者可通过精心构造的 JSON 数据绕过 AutoType 类型校验并执行任意代码。 Fastjson2 被广泛应用于 Java 应用程序，尤其在 Dubbo 等阿里生态项目中。此高危漏洞使大量应用面临远程攻击风险，开发者必须立即禁用 AutoType 或采取临时缓解措施，直至官方补丁发布。 漏洞细节和利用代码尚未公开。这是本月 Fastjson 系列中继 Fastjson1 漏洞后的第二个严重漏洞。维护者已确认该问题，但修复 PR \#7695 未被合并到主分支，所有已发布版本均存在风险。

telegram · zaihuapd · 7月27日 10:31

**背景**: Fastjson2 是阿里巴巴开发的高性能 Java JSON 库，作为 Fastjson 的继任者。它支持 AutoType 特性，允许在反序列化时通过 JSON 指定类型，但这历史上一直是反序列化漏洞的根源。之前的 Fastjson 版本曾多次出现类似的远程代码执行漏洞，开发者需要了解启用 AutoType 的风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/alibaba/fastjson2">GitHub - alibaba/fastjson2: 🚄 FASTJSON2 is a Java JSON library with excellent performance.</a></li>
<li><a href="https://www.alphabot.com/security/blog/2020/java/Fastjson-exceptional-deserialization-vulnerabilities.html">Fastjson: exceptional deserialization vulnerabilities - Alphabot Security</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#Fastjson2`, `#RCE`, `#Java`

---

<a id="item-9"></a>
## [中方驳斥美方以模型蒸馏为由制裁中国 AI 企业](https://www.mofcom.gov.cn/syxwfb/art/2026/art_7f1622463a7c48ef9fad600ce0ef702f.html) ⭐️ 8.0/10

7 月 27 日，中国商务部发表声明，驳斥美方以所谓&\#x27;蒸馏&\#x27;美国前沿模型为由调查并制裁中国 AI 企业的计划，称相关指控缺乏事实和法律依据，并警告将采取反制措施。 这标志着中美科技紧张局势的重大升级。模型蒸馏是行业常用技术，美方此举可能破坏全球 AI 合作和开源生态系统。 商务部指出，近 200 家美国初创企业已呼吁美国政府不要限制访问中国开源模型，并强调美国企业同样在蒸馏中国模型。

telegram · zaihuapd · 7月27日 11:01

**背景**: 模型蒸馏（知识蒸馏）是一种机器学习技术，让较小的&\#x27;学生&\#x27;模型从较大的&\#x27;教师&\#x27;模型学习，以较低计算成本实现相似性能，在 AI 开发中广泛用于缩小模型规模和减少推理时间。美国近年来对中国 AI 进步日益担忧，导致出口管制和制裁升级，旨在限制中国获取前沿 AI 技术。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Knowledge_distillation">Knowledge distillation - Wikipedia</a></li>
<li><a href="https://labelbox.com/guides/model-distillation/">What is Model Distillation?</a></li>

</ul>
</details>

**标签**: `#AI`, `#China`, `#US`, `#regulation`, `#trade`

---

<a id="item-10"></a>
## [中国开始量产国产 DUV 光刻机](https://www.theinformation.com/articles/china-starts-mass-producing-homegrown-duv-chipmaking-tools-advance-local-chip-industry) ⭐️ 8.0/10

中国已开始大规模生产自主研发的浸没式 DUV 光刻机，计划今年生产约 5 台，到 2027 年生产约 20 台，目标交付给中芯国际、华虹半导体等国内芯片制造商。 这一里程碑推进了中国半导体自给自足的能力，并可能逐步侵蚀 ASML 在中国市场的份额，尤其是在西方出口限制收紧的情况下。 国产 DUV 设备在性能和可靠性上仍落后于 ASML，芯片商需要数月时间进行测试。部分关键部件来自日本，今年本地供应链延误已影响进度。

telegram · zaihuapd · 7月27日 14:10

**背景**: DUV 光刻使用深紫外光（如 193nm ArF 激光）在硅片上刻蚀电路图案。浸没式光刻在镜头和晶圆之间使用液体层以提高分辨率，可实现 7nm 及以下的制程。ASML 主导高端光刻机市场，但出口管制刺激了中国开发国产替代方案的努力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DUV_lithography">DUV lithography</a></li>
<li><a href="https://en.wikipedia.org/wiki/Immersion_lithography">Immersion lithography</a></li>

</ul>
</details>

**标签**: `#semiconductor`, `#lithography`, `#China`, `#ASML`, `#chip manufacturing`

---