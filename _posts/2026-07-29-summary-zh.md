---
layout: default
title: "Horizon Summary: 2026-07-29 (ZH)"
date: 2026-07-29
lang: zh
---

> 从 41 条内容中筛选出 14 条重要资讯。

---

1. [文档传播的 AI 蠕虫通过 Word 的 Copilot 自我复制](#item-1) ⭐️ 9.0/10
2. [月之暗面融资 35 亿美元，估值达 350 亿美元](#item-2) ⭐️ 9.0/10
3. [开源引擎在 Mac 上仅用 2GB RAM 运行 Gemma 4 26B](#item-3) ⭐️ 8.0/10
4. [Mitchell Hashimoto 推出 Superlogical 进军代理计算](#item-4) ⭐️ 8.0/10
5. [Kimi 推出 K3-256k：成本更低的短上下文版本](#item-5) ⭐️ 8.0/10
6. [Handbook.md 基准显示 LLM 无法可靠遵循长政策文档](#item-6) ⭐️ 8.0/10
7. [Matthew Green 强调 AI 在后量子密码分析中的机遇](#item-7) ⭐️ 8.0/10
8. [模块化数据中心：解决劳动力短缺](#item-8) ⭐️ 8.0/10
9. [ncnn Vulkan 后端实现跨平台边缘设备 ML 推理](#item-9) ⭐️ 8.0/10
10. [Claude 共享对话和 Artifacts 遭谷歌索引暴露](#item-10) ⭐️ 8.0/10
11. [OpenAI 重置用量限制，改进 GPT-5.6 Sol 消耗](#item-11) ⭐️ 8.0/10
12. [俄联邦安全局指控 Telegram 创始人杜罗夫协助恐怖活动](#item-12) ⭐️ 8.0/10
13. [报告：Hugging Face 被广泛用于生成深度伪造裸照](#item-13) ⭐️ 8.0/10
14. [中国公布反网络暴力法草案，规制 AI 网暴](#item-14) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [文档传播的 AI 蠕虫通过 Word 的 Copilot 自我复制](https://enklypesalt.com/posts/context-collapse-part3-ai-worming-through-word/) ⭐️ 9.0/10

Håkon Måløy 展示了一种提示注入变体，将 Microsoft Copilot for Word 变成自我复制 AI 蠕虫的载体，文档中隐藏的恶意指令可改变输出并传播到新文档。 此漏洞至关重要，因为它利用生产力软件中广泛使用的 AI 助手，可能允许自动化、自我复制的攻击在组织间传播而不被用户察觉，破坏对 AI 工具的信任。 攻击利用白色文本或 Unicode 技巧在 Word 文档中隐藏恶意提示；当 Copilot 处理文档时，会遵循这些指令，修改内容并将相同提示注入新创建的文件，从而形成蠕虫。

hackernews · Canopy9560 · 7月29日 11:44 · [社区讨论](https://news.ycombinator.com/item?id=49096188)

**背景**: 提示注入攻击利用了大语言模型（LLM）无法区分系统指令和用户提供数据的特性。当 Copilot 等 AI 助手处理文档时，嵌入的文本可以劫持其行为。这项工作表明此类攻击可被制成自我复制，将孤立注入变为传播性蠕虫。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://enklypesalt.com/posts/context-collapse-part3-ai-worming-through-word/">Context Collapse, Part 3 - AI Worming through Word | En Klype Salt</a></li>
<li><a href="https://www.theregister.com/security/2026/07/29/word-worm-crawls-into-copilot-spreads-chaos/5280588">Word worm crawls into Copilot, spreads chaos</a></li>
<li><a href="https://arxiv.org/html/2606.03811v1">AI Agents Enable Adaptive Computer Worms</a></li>

</ul>
</details>

**社区讨论**: 评论者表示担忧，认为只要 AI 混淆指令与数据，此类漏洞就根本无法修复。有人强调了授予 AI 代理广泛权限的更大风险，还有人分享了如 Unicode 操作等绕过检测的实际技术。

**标签**: `#AI security`, `#adversarial attacks`, `#copilot`, `#LLM vulnerabilities`, `#prompt injection`

---

<a id="item-2"></a>
## [月之暗面融资 35 亿美元，估值达 350 亿美元](https://www.bloomberg.com/news/articles/2026-07-29/china-s-moonshot-ai-passes-funding-goal-to-hit-35-billion-value) ⭐️ 9.0/10

中国 AI 初创公司月之暗面（Moonshot AI）完成 35 亿美元融资，远超最初 10–20 亿美元的目标，因其发布的 Kimi K3 模型性能接近 OpenAI 和 Anthropic 的前沿水平。此轮融资后公司估值达 350 亿美元。 这一事件标志着中国 AI 的重要里程碑，表明本土初创公司能够在前沿水平竞争并引发类似此前“DeepSeek 时刻”的市场震荡。它预示着全球 AI 竞争加剧，并可能改变投资者对中国 AI 公司的看法。 Kimi K3 是月之暗面功能最强的模型，拥有 2.8 万亿参数，采用 Kimi Delta Attention（KDA）混合线性注意力机制，并支持 100 万 token 的上下文窗口。公司已启动新一轮融资，投前估值 500 亿美元，并计划最早今年内在香港 IPO。

telegram · zaihuapd · 7月29日 10:12

**背景**: 月之暗面是一家中国 AI 公司，开发了以长上下文能力著称的 Kimi 聊天机器人。其最新模型 Kimi K3 已开源，性能堪与西方前沿模型媲美。“DeepSeek 时刻”指 2025 年 1 月 DeepSeek 发布具竞争力的开源模型后引发的股市震荡，凸显了中国 AI 的快速进步。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kimi_%28AI%29">Kimi (AI) - Wikipedia</a></li>
<li><a href="https://platform.kimi.ai/docs/guide/kimi-k3-quickstart">Kimi K3 - Kimi API Platform</a></li>
<li><a href="https://huggingface.co/blog/ResterChed/kimi-k3-model-overview-mxfp4-quantization-open-wei">Kimi K3 Model Overview: 2.8T Parameters, MXFP4 Quantization, and What the Open Weights Mean for the Community</a></li>

</ul>
</details>

**标签**: `#AI`, `#Funding`, `#Chinese AI`, `#Large Language Models`, `#Moonshot AI`

---

<a id="item-3"></a>
## [开源引擎在 Mac 上仅用 2GB RAM 运行 Gemma 4 26B](https://github.com/drumih/turbo-fieldfare) ⭐️ 8.0/10

TurboFieldfare 是一个用 Swift 和 Metal 编写的开源推理引擎，通过从 SSD 流式传输路由专家，可在任何 M 系列 Mac 上运行 4 位量化版 Gemma 4 26B-A4B-IT 模型，仅需约 2 GB 内存。 这种方法大幅降低了在消费级设备上运行大型 MoE 模型的硬件门槛，使内存受限的 Mac 能够实现实用的设备端 AI。它挑战了模型必须完全装入 RAM 的假设，为边缘部署开辟了新的可能性。 模型的 4 位量化权重总计约 14 GB，但只有共享部分和 KV 缓存保留在 RAM 中，专家则通过小型缓存和受限并行 pread 从 SSD 流式传输。TurboFieldfare 在 8 GB M2 MacBook Air 上达到 5–6 tok/s，在 M5 MacBook Pro 上达到 31–35 tok/s。

hackernews · gitpusher42 · 7月29日 15:05 · [社区讨论](https://news.ycombinator.com/item?id=49098510)

**背景**: 混合专家 \(MoE\) 模型将计算拆分为多个专门的“专家”，由门控网络将每个 token 仅路由到一部分专家，从而减少计算量。这使得流式传输切实可行，因为每个 token 只需加载所需的专家。KV 缓存是 transformer 推理中的标准技术，用于存储先前 token 的键值对，避免重复计算。SSD 流式传输将模型权重存储在磁盘上，在推理时仅加载所需部分，从而有效扩展可用内存。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained</a></li>
<li><a href="https://huggingface.co/blog/not-lain/kv-caching">KV Caching Explained: Optimizing Transformer Inference Efficiency</a></li>

</ul>
</details>

**社区讨论**: 评论者对该创新方法表示赞赏，有些人指出这不是第一次见到这种技术。一位用户分享了针对较旧 macOS 版本的编译解决方法。另一位将其与 llama.cpp 的 mmap 进行比较，询问 SSD 流式传输有何不同。还有人对与类似 DiffusionGemma 项目的潜在合作感兴趣。

**标签**: `#inference engine`, `#on-device AI`, `#Gemma`, `#macOS`, `#model quantization`

---

<a id="item-4"></a>
## [Mitchell Hashimoto 推出 Superlogical 进军代理计算](https://www.superlogical.com/) ⭐️ 8.0/10

Mitchell Hashimoto 宣布成立新公司 Superlogical，基于开源 libghostty 终端库构建代理计算环境，并将 Ghostty 的所有权转让给了非营利组织。 这标志着将终端技术与自主 AI 代理相融合的重要一步，有望为开发者创建一个直接从命令行构建和编排代理工作流的新平台。 Superlogical 将使用与所有人相同的 MIT 许可证下的 libghostty 组件，并承诺将共享的终端工作上游化，使所有 libghostty 消费者受益。libghostty 是一个跨平台、无依赖的 C 和 Zig 库，用于构建终端模拟器或利用终端功能。

hackernews · yan · 7月29日 15:41 · [社区讨论](https://news.ycombinator.com/item?id=49098965)

**背景**: 代理计算（agentic computing）指的是在有限监督下自主行动以达成目标的 AI 系统。libghostty 是 Ghostty（一款快速、功能丰富的终端模拟器）背后的核心终端引擎。通过在开源基础上构建，Superlogical 旨在创建一个 AI 代理可以以可组合、可编程的方式与终端交互的环境。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ghostty-org/ghostty">GitHub - ghostty-org/ghostty: Ghostty is a fast, feature-rich, and...</a></li>
<li><a href="https://www.dootrix.com/what-is-agentic-computing-the-future-of-software-is-autonomous">What is Agentic Computing? The Future of Software is Autonomous</a></li>

</ul>
</details>

**社区讨论**: 社区反应积极，用户赞扬将 Ghostty 转让给非营利组织并以开源依赖构建 Superlogical 的决定。一些评论者将其与 COM/DCOM 等早期技术以及现代的代理多路复用器进行比较，突显了该项目的新颖性和潜力。

**标签**: `#agentic-computing`, `#terminal`, `#open-source`, `#mitchell-hashimoto`, `#startup`

---

<a id="item-5"></a>
## [Kimi 推出 K3-256k：成本更低的短上下文版本](https://www.kimi.com/code/docs/en/kimi-code/models) ⭐️ 8.0/10

Moonshot AI 发布了 Kimi K3-256k，这是其旗舰模型 K3 的一个变体，具有 256k token 的上下文窗口，配额成本仅为原 1M 上下文版本的一半。 这一定价策略使 K3 更适用于日常场景，因为大多数用户使用的上下文不超过 256k tokens，从而为许多应用降低了一半成本，并加剧了 LLM 市场的竞争。 根据 API 文档，K3-256k 在 256k 上下文窗口内提供了与完整版 K3 相同的结果，每个请求仅消耗一半的配额。

hackernews · monneyboi · 7月29日 19:25 · [社区讨论](https://news.ycombinator.com/item?id=49101852)

**背景**: Kimi K3 是 Moonshot AI 开发的一款拥有 2.8 万亿参数的开源模型，此前以其采用线性注意力的 100 万 token 上下文窗口而闻名。许多 LLM API 根据 token 数量和上下文长度收费，更长的上下文成本更高。256k 的上下文窗口被认为是许多实际任务的实用上限，因为输入过长时模型性能可能会下降。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kimi_%28AI%29">Kimi (AI) - Wikipedia</a></li>
<li><a href="https://platform.kimi.ai/docs/guide/kimi-k3-quickstart">Kimi K3 - Kimi API Platform</a></li>
<li><a href="https://huggingface.co/blog/ResterChed/kimi-k3-model-overview-mxfp4-quantization-open-wei">Kimi K3 Model Overview: 2.8T Parameters, MXFP4 Quantization, and What the Open Weights Mean for the Community</a></li>

</ul>
</details>

**社区讨论**: 社区反响积极，用户 timcobb 认为 100 万上下文是奢侈且默认不必要的，madihaa 则表示自己通常保持在 200k 以下。一些人认为这表明 LLM 正在变成商品，MangoCoffee 认为能提供廉价 token 的厂商将获胜。xyzsparetimexyz 称这次降价幅度巨大。

**标签**: `#LLMs`, `#pricing`, `#competitive landscape`, `#AI models`, `#commoditization`

---

<a id="item-6"></a>
## [Handbook.md 基准显示 LLM 无法可靠遵循长政策文档](https://arxiv.org/abs/2607.25398) ⭐️ 8.0/10

名为 Handbook.md 的新基准测试表明，当前大型语言模型（LLM）无法一致地遵循长政策文档，前沿模型准确率均未超过 25%。 这一发现挑战了依赖长上下文指令的 AI 代理系统的可靠性，可能阻碍其在需要严格政策合规的企业应用中的采用。 该基准涵盖五个企业领域，使用独特的强化学习环境和内部工具及外部 MCP 服务器。前沿模型准确率均未超过 25%，凸显了长上下文遵循方面的基本局限性。

hackernews · spIrr · 7月29日 13:01 · [社区讨论](https://news.ycombinator.com/item?id=49096969)

**背景**: AI 代理系统是指通过模仿人类决策以有限监督实现特定目标的系统。许多代理部署在模型上下文中放置长政策文档，期望模型在整个任务中遵循它。然而，模型在长上下文注意力和指令遵循方面存在已知问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2607.25398">[2607.25398] HANDBOOK.md: A Benchmark for Long-Context ...</a></li>
<li><a href="https://arxiv.org/html/2607.25398v1">HANDBOOK.md: A Benchmark for Long-Context - arXiv.org</a></li>
<li><a href="https://surgehq.ai/blog/handbook-md">HANDBOOK.md Benchmark: Can AI Agents Follow a 100-Page ...</a></li>

</ul>
</details>

**社区讨论**: 评论者同意研究结果，有人指出本地推理可以缓解问题，另有人指出人类也难以遵循长政策文档。一位用户分享轶事，Claude 在大约 10 分钟后忽略 CLAUDE.md 文件中的指令，表明上下文随时间衰减。

**标签**: `#AI safety`, `#LLM limitations`, `#long context`, `#agent reliability`, `#policy compliance`

---

<a id="item-7"></a>
## [Matthew Green 强调 AI 在后量子密码分析中的机遇](https://simonwillison.net/2026/Jul/29/matthew-green/#atom-everything) ⭐️ 8.0/10

著名密码学家 Matthew Green 指出，从 RSA/ECC 向后量子算法的历史性转型为 AI 推动公开密码分析创造了完美时机。他引用了 Anthropic 的近期工作，其中 Claude AI 发现了 NIST 后量子候选算法 HAWK-256 的一个弱点。 这很重要，因为后量子标准正在最终确定，AI 可能削弱或加强这些新算法，影响全球网络安全。如果 AI 在密码分析上成功，可能会带来更稳健的标准，或在广泛部署前揭示隐藏的漏洞。 Anthropic 的 Claude Mythos 在 60 小时内破解了 HAWK-256，人类密码学家两年未发现此漏洞，但该结果仅针对较小的 HAWK-256 参数集，且需要不切实际的选择明文条件。对 AES 的部分破解只适用于十轮中的七轮。

rss · Simon Willison · 7月29日 18:18

**背景**: 后量子密码学开发能抵御经典和量子计算机的算法，以替代可被 Shor 算法破解的 RSA 和 ECC。NIST 正在标准化多种方案，包括基于格的 HAWK。AI 密码分析利用机器学习寻找数学弱点。Impagliazzo 的五世界是探索 P 与 NP 复杂度类可能关系的框架。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thehackernews.com/2026/07/claude-ai-just-cracked-post-quantum.html">Claude AI Just Cracked a Post-Quantum Test Scheme and Found a ...</a></li>
<li><a href="https://hawk-sign.info/">Hawk</a></li>

</ul>
</details>

**标签**: `#cryptography`, `#post-quantum`, `#AI`, `#cryptanalysis`, `#cybersecurity`

---

<a id="item-8"></a>
## [模块化数据中心：解决劳动力短缺](https://newsletter.semianalysis.com/p/the-wild-wild-west-of-lego-datacenters) ⭐️ 8.0/10

文章解释了数据中心建设的模块化如何应对行业日益严重的劳动力短缺，减少对大量现场劳动力的依赖。 这很重要，因为劳动力短缺正在延迟全球数据中心部署；模块化施工可实现更快、更可预测的建设，这对扩展人工智能和云基础设施至关重要。 模块化数据中心在受控环境中异地预制，然后在现场组装，可将施工时间缩短 40%以上，并减少现场劳动力需求。

rss · Semianalysis · 7月29日 22:09

**背景**: 传统数据中心建设是劳动密集型产业，面临熟练劳动力短缺。模块化数据中心由工厂生产的模块组成，包括电源、冷却和 IT 基础设施，允许现场准备和模块制造并行进行。这种方法具有可扩展性、更快的部署和更低的成本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Modular_data_center">Modular data center - Wikipedia</a></li>
<li><a href="https://www.modular.org/office-data-center-sector/">Office &amp; Data Center Sector Overview | Modular Building Institute</a></li>
<li><a href="https://www.se.com/us/en/product-category/7550-prefabricated-data-center-modules/">Prefabricated Data Center Modules - Schneider Electric USA</a></li>

</ul>
</details>

**标签**: `#datacenter`, `#modular construction`, `#labor`, `#infrastructure`, `#technology`

---

<a id="item-9"></a>
## [ncnn Vulkan 后端实现跨平台边缘设备 ML 推理](https://www.reddit.com/r/MachineLearning/comments/1v9s4mz/vendoragnostic_ml_inference_on_production_edge/) ⭐️ 8.0/10

作者描述了在生产边缘设备上使用 ncnn 的 Vulkan 后端进行与厂商无关的机器学习推理，相比于 ONNX CPU，在人脸检测和嵌入模型上实现了 10 倍加速。 这展示了一种在多样化 GPU（NVIDIA、AMD、Intel、Apple Silicon）上运行 ML 模型的实用方案，无需特定厂商的运行时，降低了跨平台边缘 AI 的部署复杂性。 在 NVIDIA 4070 上，ArcFace R50 从 30ms 降至 3ms，SCRFD 从 25ms 降至 2.5ms；模型大小从 174 MB（ONNX fp32）减半至 87 MB（ncnn fp16）。Vulkan 驱动已在大多数系统上预装，无需额外下载运行时。

reddit · r/MachineLearning · /u/ppchaos · 7月29日 10:22

**背景**: ncnn 是由腾讯开发的轻量级神经网络推理框架，针对移动和边缘设备进行了优化。Vulkan 是一种低开销、跨平台的 GPU API，支持计算着色器进行通用 GPU 计算。通过将 ncnn 与 Vulkan 结合，开发者可以利用 GPU 加速，而不必受限于特定厂商的 CUDA 或 ROCm 生态系统，非常适合异构设备环境。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ncnn.readthedocs.io/en/latest/home.html">home — ncnn documentation</a></li>
<li><a href="https://github.com/Tencent/ncnn/releases">Releases · Tencent/ncnn - GitHub</a></li>

</ul>
</details>

**标签**: `#ML Inference`, `#Vulkan`, `#Edge AI`, `#Vendor-Agnostic`, `#ncnn`

---

<a id="item-10"></a>
## [Claude 共享对话和 Artifacts 遭谷歌索引暴露](https://thenextweb.com/news/claude-shared-chats-artifacts-google-search-indexed) ⭐️ 8.0/10

自周末以来，Claude 的共享对话和 Artifacts 链接被谷歌和必应索引，导致医疗记录、公司文件等敏感用户数据可被公开搜索。 此事件突显了 AI 共享功能中的重大隐私风险，影响数千用户在不知情的情况下泄露机密信息，并强调需要改进数据处理实践。 Anthropic 表示系统未被入侵，共享是设计使然；他们于周一下午阻止了新的索引，但旧链接仍可访问。类似事件此前也影响了 ChatGPT 和 Grok。

telegram · zaihuapd · 7月29日 02:40

**背景**: Claude Artifacts 允许用户生成并分享交互式代码预览和应用程序。共享对话链接旨在选择性分享，但并非自动设为私密；用户需自行管理分享设置。谷歌索引抓取了这些可公开访问的 URL，这是搜索引擎的常见行为。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cybersecuritynews.com/claude-ai-shared-chats/">Claude AI Shared Chats Reportedly Exposed in Google Search ...</a></li>
<li><a href="https://support.claude.com/en/articles/9487310-what-are-artifacts-and-how-do-i-use-them">What are artifacts and how do I use them? | Claude Help Center</a></li>
<li><a href="https://thecybersecguru.com/news/claude-shared-chats-google-search-privacy/">Claude Share Links Became Searchable on Google and Bing: What ...</a></li>

</ul>
</details>

**标签**: `#privacy`, `#security`, `#Claude`, `#AI`, `#data exposure`

---

<a id="item-11"></a>
## [OpenAI 重置用量限制，改进 GPT-5.6 Sol 消耗](https://x.com/thsottiaux/status/2082317452755751098) ⭐️ 8.0/10

OpenAI 已重置所有 ChatGPT Work 和 Codex 用户的用量限制，并针对 GPT-5.6 Sol 消耗令牌过快的问题推出多项改进。此前暂停的五小时限额将于次日恢复。 这一变化直接惠及依赖 GPT-5.6 Sol 执行复杂任务的开发者和重度用户，缓解了对意外高用量的担忧。这也表明 OpenAI 对用户反馈的响应速度以及透明沟通的承诺。 改进后典型使用时长可增加约 18%，部分用户提升更大。OpenAI 承认他们在开发过程中过于关注平均用量，忽视了重度用户场景。

telegram · zaihuapd · 7月29日 04:27

**背景**: GPT-5.6 Sol 是 OpenAI 的旗舰模型，专为复杂推理、编码和代理工作流设计，API 价格为每百万输入标记 5 美元、每百万输出标记 30 美元。用量限制指在给定时间内用户可使用的标记或请求数量上限，常以滚动窗口形式执行。Sol 由于倾向于大量调用工具和处理长期任务，消耗的标记比之前的模型更多。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openrouter.ai/openai/gpt-5.6-sol">GPT-5.6 Sol - API Pricing &amp; Benchmarks | OpenRouter</a></li>
<li><a href="https://developers.openai.com/api/docs/models/gpt-5.6-sol">GPT - 5 . 6 Sol Model | OpenAI API</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#GPT-5`, `#usage limits`, `#Sol`, `#ChatGPT`

---

<a id="item-12"></a>
## [俄联邦安全局指控 Telegram 创始人杜罗夫协助恐怖活动](https://www.interfax.ru/russia/1106228) ⭐️ 8.0/10

7 月 29 日，俄罗斯联邦安全局（FSB）依据《刑法》第 205.1 条第 1.1 款（协助恐怖活动）对 Telegram 创始人帕维尔·杜罗夫提起刑事指控，并将其列入国际通缉名单。 这一针对大型科技创始人的史无前例的法律行动引发了对平台治理、数字隐私和言论自由的严重担忧，可能为全球其他社交媒体平台及其领导者树立一个寒蝉效应般的先例。 FSB 指控 Telegram 管理层拒不删除被乌克兰情报机构及恐怖、极端主义组织用于在俄境内策划破坏活动、恐怖袭击、大规模杀戮及网络诈骗的频道、群组和机器人，造成包括妇女儿童在内的多人伤亡和数十亿卢布损失。

telegram · zaihuapd · 7月29日 05:56

**背景**: 帕维尔·杜罗夫是出生于俄罗斯的企业家，于 2013 年创立了安全消息应用 Telegram。该平台因其对内容审核的不干涉态度而受到批评，经常与要求访问加密通信的政府发生冲突。俄罗斯此前曾在 2018 年试图屏蔽 Telegram，但因该应用广泛使用和技术规避手段而失败。

**标签**: `#Telegram`, `#Pavel Durov`, `#terrorism`, `#Russia`, `#freedom of speech`

---

<a id="item-13"></a>
## [报告：Hugging Face 被广泛用于生成深度伪造裸照](https://www.theverge.com/ai-artificial-intelligence/971723/hugging-face-nudify-deepfake-undress-women-children) ⭐️ 8.0/10

欧洲非营利组织 AI Forensics 发布报告称，Hugging Face 平台上的模型被轻易用于制作非自愿的深度伪造裸照，包括儿童色情内容。研究发现，排名前九的图像编辑模型中有七个能通过简单提示为女性“脱衣”，其设置的蜜罐在 7 天内收到超过 1000 条请求，其中 73%涉及性内容，近 7%针对未成年人。 这凸显了开源 AI 模型托管平台在安全方面的严重漏洞，威胁隐私和儿童安全。亟需政策和技术措施防止滥用，影响平台责任和监管。 报告指出，Hugging Face 几乎没有平台级防护措施来阻止生成非自愿性内容，与其自身政策相矛盾。研究人员无需精心构造提示词，简单指令即可绕过限制。

telegram · zaihuapd · 7月29日 08:20

**背景**: Hugging Face 是一个流行的开源社区和平台，用于共享机器学习模型和数据集。蜜罐是一种安全机制，通过模拟脆弱目标来检测或转移攻击者。在本研究中，AI Forensics 在 Hugging Face 上设置了蜜罐以观察实际滥用情况。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Hugging_Face">Hugging Face</a></li>
<li><a href="https://en.wikipedia.org/wiki/Honeypot_%28computing%29">Honeypot (computing) - Wikipedia</a></li>

</ul>
</details>

**标签**: `#AI Ethics`, `#Deepfakes`, `#Hugging Face`, `#Safety`, `#Platform Responsibility`

---

<a id="item-14"></a>
## [中国公布反网络暴力法草案，规制 AI 网暴](https://mp.weixin.qq.com/s/PrzKFhbwjgFEGBPADvFD6Q) ⭐️ 8.0/10

2026 年 7 月 29 日，国家互联网信息办公室公布《中华人民共和国反网络暴力法（征求意见稿）》，明确将利用 AI 技术制作、传播网络暴力信息纳入法律规制。 这是中国首次将 AI 网暴纳入法律规制，对科技公司和 AI 治理具有直接影响。 草案要求平台建立监测识别机制和防护功能，并引入人格权侵害禁令等司法保护措施，受害者有权请求精神损害赔偿。

telegram · zaihuapd · 7月29日 10:59

**背景**: 网络暴力在中国日益严重，AI 工具使制作和传播有害内容更加容易。该草案旨在构建多部门协同的政府治理体系，明确平台和个人的法律责任。

**标签**: `#网络安全`, `#法律`, `#AI治理`, `#网络暴力`, `#政策`

---