---
layout: default
title: "Horizon Summary: 2026-07-26 (ZH)"
date: 2026-07-26
lang: zh
---

> 从 28 条内容中筛选出 7 条重要资讯。

---

1. [vLLM v0.26.0 新增 Inkling 模型，提升 DeepSeek-V4 性能](#item-1) ⭐️ 9.0/10
2. [SGLang v0.5.16：引入 DSpark 投机解码与 Inkling 支持](#item-2) ⭐️ 9.0/10
3. [开放权重 AI 迎来 Kubernetes 式的转折点](#item-3) ⭐️ 8.0/10
4. [草根运动破坏 Flock 监控摄像头](#item-4) ⭐️ 8.0/10
5. [Ruff v0.16.0 默认规则从 59 条增至 413 条](#item-5) ⭐️ 8.0/10
6. [Claude Opus 5 展现出强抗提示注入能力](#item-6) ⭐️ 8.0/10
7. [AMD 打破英伟达 CUDA 护城河的战略](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [vLLM v0.26.0 新增 Inkling 模型，提升 DeepSeek-V4 性能](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 9.0/10

vLLM v0.26.0 引入了对 Inkling 模型族的支持，为 DeepSeek-V4 提供了性能改进，并新增了通过 head\_dtype 实现的 fp32 lm\_head、灵活注意力后端以及成熟的 KV 卸载等功能。 此版本巩固了 vLLM 作为前沿开放权重模型（如 975B 参数的 Inkling）推理引擎的地位，并优化了广泛使用的 DeepSeek 模型的性能，惠及研究人员和实际部署。 Inkling 支持包括基础建模、分段 CUDA 图、Hopper FA4 相对注意力、MTP=1 推测解码、LoRA 和 NVFP4 量化。DeepSeek-V4 获得了专用路由内核（端到端 TPOT 提升 2.94%）和 fused\_topk\_bias（内核速度提升 1.5–2 倍）。

github · khluu · 7月25日 10:38

**背景**: vLLM 是一个高性能的开源 LLM 推理库，支持多种模型和硬件。Inkling 模型是一个 975B 参数的混合专家 transformer，拥有 41B 活跃参数，在 45 万亿 token 上预训练，支持高达 100 万 token 的上下文。NVFP4 是一种 4 位浮点量化格式，比 INT4 保留更高的动态范围。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thinkingmachines.ai/news/introducing-inkling/">Inkling: Our Open-Weights Model - Thinking Machines Lab</a></li>
<li><a href="https://www.technology.org/2026/07/16/thinking-machines-inkling-open-weights-model/">Thinking Machines Releases Inkling, Its First Open-Weights Model, Trained From Scratch</a></li>
<li><a href="https://developer.nvidia.com/blog/introducing-nvfp4-for-efficient-and-accurate-low-precision-inference/">Introducing NVFP4 for Efficient and Accurate Low-Precision Inference | NVIDIA Technical Blog</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#release`, `#DeepSeek`, `#performance`

---

<a id="item-2"></a>
## [SGLang v0.5.16：引入 DSpark 投机解码与 Inkling 支持](https://github.com/sgl-project/sglang/releases/tag/v0.5.16) ⭐️ 9.0/10

SGLang v0.5.16 引入了 DSpark 投机解码，在 DeepSeek-V4-Pro 上达到 383.7 tok/s，并增加了对 975B 参数 Inkling 多模态 MoE 模型的支持。本次发布包含来自 169 位贡献者的 574 个拉取请求，是一次重大更新。 此版本通过自适应投机解码显著提升了 LLM 推理性能，并将 SGLang 的支持范围扩展至前沿的多模态 MoE 模型，使研究人员和生产部署均受益。 DSpark 采用半自回归草稿生成和基于置信度的验证，在 Blackwell B300 TP8 上可达 383.7 tok/s，接受长度约 5。Inkling 结合了滑动窗口、完整注意力和 Mamba2 线性注意力，配备 NVFP4 MoE 和原生 MTP，最高可实现 71.7k tok/s 的输入吞吐率和 171.0 tok/s 的每用户解码速度。

github · Qiaolin-Yu · 7月25日 00:13

**背景**: 投机解码是一种使用较小的草稿模型生成多个 token，然后由较大的目标模型进行验证的技术，可在不损失质量的前提下实现加速。SGLang 是一个面向大语言模型的开源服务框架，专为快速推理而优化。DSpark 最初由 DeepSeek 发布，通过基于置信度调度验证，可将推理延迟降低最高 85%。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.techtimes.com/articles/319236/20260628/deepseek-releases-dspark-speculative-decoding-makes-v4-85-percent-faster.htm">DeepSeek Releases DSpark: Speculative Decoding Makes V4 Up to 85 Percent Faster</a></li>
<li><a href="https://thinkingmachines.ai/news/introducing-inkling/">Inkling: Our Open-Weights Model - Thinking Machines Lab</a></li>
<li><a href="https://www.marktechpost.com/2026/07/15/thinking-machines-lab-releases-inkling-a-975b-parameter-open-weights-multimodal-moe-with-41b-active-parameters-and-controllable-thinking-effort/">Thinking Machines Lab Releases Inkling: A 975B-Parameter Open ...</a></li>

</ul>
</details>

**标签**: `#speculative decoding`, `#LLM serving`, `#SGLang`, `#multimodal MoE`, `#high performance`

---

<a id="item-3"></a>
## [开放权重 AI 迎来 Kubernetes 式的转折点](https://tobi.knaup.me/2026-07-25-open-weight-ai-is-having-its-kubernetes-moment/) ⭐️ 8.0/10

一篇文章认为，开放权重 AI 模型正在成为标准的基础设施层，类似于 Kubernetes 成为云计算中容器编排的标准。 这一类比表明，开放权重模型可能成为不可或缺的基础设施，重塑竞争、监管和初创公司的生存能力，并对美国实验室如何与中国模型竞争产生影响。 开放权重模型发布训练好的参数（权重），但不一定包括训练数据或完整源代码，允许任何人托管、微调或在其基础上构建，但缺乏完全开源透明度。

hackernews · tknaup · 7月25日 14:49 · [社区讨论](https://news.ycombinator.com/item?id=49048034)

**背景**: Kubernetes 是一个开源系统，用于自动化容器化应用程序的部署、扩展和管理，已成为事实上的标准云基础设施层。类似地，开放权重 AI 模型发布神经网络学习到的权重，允许用户进行推理或微调，但不同于完全开源 AI（还包括训练数据和代码）。该文章将两者类比为标准化的、广泛采用的基础设施，支持在其上进行创新。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.linkedin.com/pulse/open-weight-ai-what-we-finally-opened-bonnet-nicolas-pistorio-n3ulf">Open - weight AI : what if we finally opened the bonnet ?</a></li>
<li><a href="https://openai.com/index/introducing-gpt-oss/">Introducing gpt-oss | OpenAI</a></li>

</ul>
</details>

**社区讨论**: 社区评论强调了几个关键点：有人认为按原产国禁止模型在技术上不可行，因为权重只是数字（ozgung）；另一些人认为“代币经济学”定价令人困惑（firasd）；有人支持像 Linux 那样由多家公司协作构建 AI 模型（pianopatrick）；还有人指出 OpenAI 发布过较旧的开放权重模型但很少更新（drnick1）。总体态度是正面的，但担忧实际和监管挑战。

**标签**: `#open-weight models`, `#AI infrastructure`, `#Kubernetes`, `#open source AI`, `#AI regulation`

---

<a id="item-4"></a>
## [草根运动破坏 Flock 监控摄像头](https://www.theguardian.com/us-news/ng-interactive/2026/jul/25/flock-surveillance-cameras) ⭐️ 8.0/10

《卫报》报道，公民出于隐私侵犯和对当局的不信任，越来越多地直接破坏 Flock 监控摄像头。 Flock 摄像头是执法部门使用的车牌读取器，但 2021 年一项研究发现其输出错误率达 10%。破坏运动包括使用带纸板的泳池捞网遮挡摄像头等行为。

hackernews · bookofjoe · 7月25日 19:02 · [社区讨论](https://news.ycombinator.com/item?id=49050538)

**背景**: Flock Safety 是一家向警察局和私人实体销售自动车牌识别摄像头的公司。这些摄像头安装在公共场所，记录每一辆经过的车辆，这引发了严重的隐私担忧。批评者认为，这种监控可能被滥用，并侵蚀公众信任。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Flock_Safety">Flock Safety - Wikipedia</a></li>
<li><a href="https://trafficvision.live/blog/flock-cameras">Flock Cameras : What They Are &amp; Can You Watch... | TrafficVision.Live</a></li>

</ul>
</details>

**社区讨论**: 评论表达了对草根行动的强烈支持，有人指出高层政治中的极端犯罪破坏了摄像头的宣称目的。其他人建议采取反制措施，例如将摄像头对准政客的住所。普遍情绪是，当人们感到意见不被听取时，私刑行为不可避免。

**标签**: `#surveillance`, `#privacy`, `#civil liberties`, `#vigilantism`, `#technology`

---

<a id="item-5"></a>
## [Ruff v0.16.0 默认规则从 59 条增至 413 条](https://simonwillison.net/2026/Jul/25/ruff/#atom-everything) ⭐️ 8.0/10

Astral 于 7 月 23 日发布了 Ruff v0.16.0，将默认的 lint 规则集从 59 条增加到 413 条，使得许多之前需要手动启用的检查现在默认开启。 这一变化将影响几乎所有 Ruff 用户和 CI 流水线，现有项目可能突然出现数百条新警告或错误。使用未锁定依赖的开发者可能会遇到 CI 构建失败，直到他们更新代码或锁定旧版 Ruff。 默认规则集自 Ruff v0.1.0 以来未曾更新，而可用规则总数已从 708 条增长至 968 条。该版本包含用于自动修复的 &\#x27;unsafe-fixes&\#x27; 选项，新闻作者成功对三个主要项目应用自动修复，每个项目最多修复了 1,538 个错误。

rss · Simon Willison · 7月25日 22:44

**背景**: Ruff 是一个用 Rust 编写的极速 Python 代码检查器和格式化工具，旨在替代 Flake8、isort 和 pyupgrade 等工具。它从数十个现有工具中重新实现了超过 900 条 lint 规则，运行速度比前辈工具快 10 到 100 倍。以前的默认规则集只启用了一个小子集（59 条规则），以减少新用户的误报，但此版本将更多规则默认开启，以便更早地捕获问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.astral.sh/ruff/linter/">The Ruff Linter | Ruff - Astral</a></li>
<li><a href="https://github.com/astral-sh/ruff">GitHub - astral-sh/ruff: An extremely fast Python linter and ... ruff · PyPI Ruff - Astral Ruff: Complete Guide to Python&#x27;s Fastest Linter | pydevtools GitHub - sartcod/ruff: An extremely fast Python linter and ... Ruff: A Modern Python Linter for Error-Free and Maintainable ...</a></li>

</ul>
</details>

**标签**: `#Python`, `#linting`, `#Ruff`, `#tooling`

---

<a id="item-6"></a>
## [Claude Opus 5 展现出强抗提示注入能力](https://simonwillison.net/2026/Jul/25/boris-cherny/#atom-everything) ⭐️ 8.0/10

Boris Cherny 指出，Anthropic 的 Claude Opus 5 模型是迄今为止最难被提示注入的模型，这一点在其系统卡中有详细说明。 这标志着大语言模型在安全性上的重大进步，解决了可能绕过模型防护的关键漏洞。增强的提示注入抵抗力对于在敏感应用中部署 AI 至关重要。 该声明基于提示注入评估和红队测试，详细信息见于 Claude Opus 5 系统卡的第 73 页。该模型似乎极难被成功注入提示。

rss · Simon Willison · 7月25日 00:42

**背景**: 提示注入是一种网络安全攻击，恶意输入可导致 LLM 忽略开发者指令或执行非预期操作。它可以是直接的，也可以是间接的（例如通过网页内容）。红队测试是一种对抗性测试，用于发现漏洞。这些评估对 AI 安全至关重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection">Prompt injection</a></li>
<li><a href="https://en.wikipedia.org/wiki/Red_teaming">Red teaming</a></li>
<li><a href="https://owasp.org/www-community/attacks/PromptInjection">Prompt Injection - OWASP Foundation</a></li>

</ul>
</details>

**标签**: `#prompt-injection`, `#anthropic`, `#claude`, `#ai-safety`, `#generative-ai`

---

<a id="item-7"></a>
## [AMD 打破英伟达 CUDA 护城河的战略](https://newsletter.semianalysis.com/p/can-amd-break-the-cuda-moat-amd-advancing) ⭐️ 8.0/10

SemiAnalysis 的详细分析揭示了 AMD 挑战英伟达 CUDA 主导地位的多方面策略，包括智能体内核生成、软件质量改进、高达 105%折扣的激进定价，以及面临生产爬坡挑战的 Helios MI455X 机架级系统。 如果成功，AMD 的努力可能会削弱英伟达在 AI 训练和推理领域的近乎垄断地位，可能降低 AI 开发者的成本并增加硬件选择。该分析突出了可能改变竞争格局的技术和财务策略。 AMD 的智能体内核生成（例如 GEAK）旨在自动化内核优化，解决软件质量的关键弱点。然而，内部开发集群仍然不稳定，Helios MI455X 的生产爬坡被描述为“地狱”，而金融工程提供了高达 105%的股权回扣折扣以吸引 OpenAI 等客户。

rss · Semianalysis · 7月25日 00:33

**背景**: 英伟达的 CUDA 生态系统长期以来一直是竞争对手难以逾越的壁垒，因为许多 AI 框架和优化库都是为 CUDA 专门构建的。AMD 的 ROCm 软件堆栈旨在提供兼容性和性能，但历史上在质量和开发者采用方面落后。智能体内核生成利用 AI 自动创建优化的 GPU 内核，可能减少匹配英伟达性能所需的手动工作。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://newsletter.semianalysis.com/p/can-amd-break-the-cuda-moat-amd-advancing">Can AMD break the CUDA Moat? AMD Advancing AI 2026</a></li>
<li><a href="https://www.tomshardware.com/pc-components/gpus/amd-takes-the-wraps-off-its-instinct-mi455x-ai-accelerator-cdna-5-and-helios-rack-scale-architecture-combine-to-take-the-fight-to-nvidia-in-the-data-center">AMD takes the wraps off its Instinct MI455X AI accelerator — CDNA 5 and Helios rack-scale architecture combine to take the fight to Nvidia in the data center | Tom&#x27;s Hardware</a></li>
<li><a href="https://www.amd.com/en/products/rackscale-solutions/helios.html">AMD Helios Rackscale Solution – Powering Frontier AI</a></li>

</ul>
</details>

**标签**: `#AMD`, `#CUDA`, `#GPU Computing`, `#AI Hardware`, `#Software Ecosystem`

---