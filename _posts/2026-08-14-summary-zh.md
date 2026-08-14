---
layout: default
title: "Horizon Summary: 2026-08-14 (ZH)"
date: 2026-08-14
lang: zh
---

> 从 34 条内容中筛选出 11 条重要资讯。

---

1. [Qwen 3.8 27B 本地大模型以强大推理与创意获好评](#item-1) ⭐️ 9.0/10
2. [GLM-5.3：前沿编程与涌现式网络能力](#item-2) ⭐️ 9.0/10
3. [将《毁灭战士》渲染器编译成 210 亿参数 Transformer，无需训练](#item-3) ⭐️ 9.0/10
4. [小红书开源 dots3-note：280B MoE 仅 16B 激活参数](#item-4) ⭐️ 9.0/10
5. [RustDesk 为 Wayland 带来真正的无人值守远程访问](#item-5) ⭐️ 8.0/10
6. [Firefox 成为最后仍支持 uBlock Origin 的主流浏览器](#item-6) ⭐️ 8.0/10
7. [torch-preflight：一个用于检测 PyTorch 训练错误并估算 VRAM 的静态检查工具](#item-7) ⭐️ 8.0/10
8. [AI 机器人实验室每年测 300 万人体组织，有望终结动物测试](#item-8) ⭐️ 8.0/10
9. [美法官令谷歌一周内取消第三方应用商店安装阻碍](#item-9) ⭐️ 8.0/10
10. [PostgreSQL 修复高危 to\_char 堆溢出漏洞，可致任意代码执行](#item-10) ⭐️ 8.0/10
11. [苹果联手阿里自研中国专属 AI 模型，力争首家获批外企](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Qwen 3.8 27B 本地大模型以强大推理与创意获好评](https://huggingface.co/Qwen/Qwen3.8-27B-FP8) ⭐️ 9.0/10

Qwen 发布了 Qwen3.8-27B，这是一个新的开源权重本地大语言模型，支持图像和视频理解，并具有灵活思考控制能力。该模型在 Hacker News 上迅速引发热议，用户称赞其推理性能和创意生成能力。 此次发布意义重大，因为它表明本地模型在推理任务上可与更大的商业模型媲美，可能加速向私有化、端侧 AI 的转变。社区的强烈反响表明 Qwen3.8-27B 有望成为 2026 年本地 AI 的重要参照。 Qwen3.8-27B 是一个原生视觉语言模型，具有灵活思考控制和多步任务可靠性。AMD 在其 Ryzen AI Max 处理器和 Radeon GPU 上提供了 Day 0 支持；社区用户还指出其显存利用率不如 Gemma 4 或 Glimmer，并且部分用户反映在 Ollama 中处理思考 token 及 Jinja 模板时存在问题。

hackernews · erdaltoprak · 8月14日 15:00 · [社区讨论](https://news.ycombinator.com/item?id=49299605)

**背景**: Qwen 是由阿里巴巴开发的开源权重大语言模型系列，3.8 代包含了针对本地运行优化的模型。由于隐私、成本和离线需求，本地运行 LLM 越来越流行，Ollama、LM Studio 和 llama.cpp 等工具让用户可以在消费级硬件上运行 Qwen3.8-27B 等模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/Qwen/Qwen3.8-27B">Qwen/Qwen3.8-27B · Hugging Face</a></li>
<li><a href="https://www.amd.com/en/blogs/2026/run-qwen-3-8-27b-on-amd-ryzen-ai-max-and-radeon-graphics-cards-day-0.html">Run Qwen 3.8 27B on AMD Ryzen™ AI Max Agentic PCs and Radeon ™ GPUs</a></li>
<li><a href="https://medium.com/@rosgluk/qwen-3-8-27b-is-coming-and-it-could-be-the-most-important-local-ai-release-of-2026-c1cf381d5292">Qwen 3.8 27B Is Coming - and It Could Be the Most Important Local AI Release of 2026 | by Rost Glukhov | Aug, 2026 | Medium</a></li>

</ul>
</details>

**社区讨论**: 社区反应总体正面，用户称赞该模型通过私有基准测试的能力及其详细的创作输出（如一幅逼真的鹈鹕画）。也有人对显存效率和独特的思考痕迹格式提出担忧；部分用户尝试在 Ollama 中禁用思考或使用自定义模板来提升性能。

**标签**: `#AI`, `#LLM`, `#Qwen`, `#local models`, `#reasoning`

---

<a id="item-2"></a>
## [GLM-5.3：前沿编程与涌现式网络能力](https://z.ai/blog/glm-5.3) ⭐️ 9.0/10

Z.ai 于 2026 年 8 月 14 日发布了 GLM-5.3，这是一款面向编程和长时程任务的旗舰模型，参数量为 743B，上下文长度达 1M token。它沿用 GLM-5.2 的基础模型，但通过大规模后训练改进，展现出自动发现漏洞和成功开展安全研究等涌现式网络能力。 这次发布标志着编程模型正进化为自主安全研究工具，可能降低漏洞发现与红队测试的门槛。它也加剧了前沿 AI 实验室之间的竞争，对在 OpenAI、Anthropic 和 Z.ai 之间做选择的企业产生影响。 GLM-5.3 并非新的基础模型；Z.ai 表示它使用与 GLM-5.2 相同的基础模型，通过后训练实现提升，配置为 743B 参数和 1M token 上下文。社区测试报告称其在红队场景中取得成功，包括 WordPress 插件的 0-day 漏洞利用、RCE 和内核漏洞利用，并且 Z.ai 在 cvd.z.ai 运营着一个协调漏洞披露门户。

hackernews · pella · 8月14日 05:19 · [社区讨论](https://news.ycombinator.com/item?id=49294997)

**背景**: 前沿编程模型是专为软件工程任务（如代码生成、调试和长时程自主智能体工作）优化的大型语言模型。涌现能力指当模型规模扩大时出现的意想不到的行为，有时包括工具使用和多步推理。自动漏洞发现利用 AI 大规模扫描源代码并发现安全缺陷，这一趋势因近期基于 LLM 的系统而加速。Z.ai 的 GLM 系列是一个中国开发的大模型家族，与 OpenAI、Anthropic 等西方实验室竞争。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openlm.ai/glm-5.2/">GLM-5.3 - openlm.ai</a></li>
<li><a href="https://kingy.ai/blog/glm-5-3-specs-benchmarks-api-how-to-use/">GLM-5.3 Just Launched: Specs, Benchmarks, API &amp; How to Use It</a></li>
<li><a href="https://www.emergentmind.com/topics/emergent-capabilities">Emergent Capabilities in AI</a></li>

</ul>
</details>

**社区讨论**: 社区反应热烈但克制。有评论者报告了使用 GLM-5.3 进行红队测试和漏洞利用开发的实际成功，也有人指出它仍落后于 Mythos 5 等模型，并称其为“GLM 5.2 加后训练魔法”。一些人称赞 Z.ai 的行文风格和 CVD 披露工作，而怀疑者则质疑从 OpenAI 切换过来的经济理由。

**标签**: `#AI`, `#GLM-5.3`, `#cybersecurity`, `#coding`, `#frontier models`

---

<a id="item-3"></a>
## [将《毁灭战士》渲染器编译成 210 亿参数 Transformer，无需训练](https://www.reddit.com/r/MachineLearning/comments/1voazhm/i_compiled_dooms_renderer_into_a_21bparameter/) ⭐️ 9.0/10

作者用自研编译器 torchwright 将《毁灭战士》的渲染算法移植进一个 210 亿参数的 Transformer，编译器直接把计算图转换为模型权重，而不是训练模型。生成的标准 Hugging Face 检查点可直接加载；渲染一帧时，输入 3,614 个 token 的场景提示，再生成 53,747 个 token，其中编码了像素绘制命令。 这项工作表明，复杂且带有状态的渲染程序可以被编译进普通的 Transformer 权重，而无需任何基于梯度的训练，这模糊了程序合成与预训练神经计算之间的界限。它可能为机械可解释性研究，以及理解 Transformer 检查点究竟能编码什么，开辟新的方向。 用于加载检查点、生成渲染结果并把输出解析为 E1M1 画面的宿主程序只有 43 行 Python，而更长的计算图定义则被编译进 Transformer 本身。性能方面，原版《毁灭战士》在 486 上能达到 35 FPS，而这个 Transformer 在 NVIDIA B200 上大约每天只能生成 35 帧。

reddit · r/MachineLearning · /u/notforrob · 8月14日 15:50

**背景**: torchwright 是一个编译器，它把计算图转换为 Transformer 的权重：先将计算图调度到各层中，再根据源计算图直接算出每一个权重。Doom 引擎的渲染器使用二叉空间分割（BSP）树对几何体排序，墙壁以垂直纹理列的方式绘制，地面和天花板则使用类似泛洪填充的算法。把这种命令式算法编译进静态的注意力与前馈权重并不常见，因为 Transformer 权重通常是通过梯度下降学习得到的，而不是由编译器构造出来的。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/physicsrob/torchwright">physicsrob/torchwright: A compiler that transforms computation ...</a></li>
<li><a href="https://doomwiki.org/wiki/Doom_rendering_engine">Doom rendering engine - The Doom Wiki at DoomWiki.org</a></li>
<li><a href="https://en.wikipedia.org/wiki/Doom_engine">Doom engine - Wikipedia</a></li>

</ul>
</details>

**标签**: `#transformer`, `#compilation`, `#program synthesis`, `#interpretability`, `#neural networks`

---

<a id="item-4"></a>
## [小红书开源 dots3-note：280B MoE 仅 16B 激活参数](https://x.com/dotsstudioai/status/2088083314855018521) ⭐️ 9.0/10

小红书 dots 实验室开源了 dots3-note preview，这是 dots3 系列首个开放权重模型，总参数 280B，激活参数仅 16B。该发布引入了 TEMPO 强化学习方法，并在 Hugging Face 开放权重，同时发布 VibeSearchBench、VibeLifeBench 两个新基准。 此次发布意义重大，因为它以较低的推理成本提供了前沿规模的 MoE 能力，使开源社区也能使用 280B 级的多模态理解模型。TEMPO 方法以及真实场景基准可能会影响长程 AI 智能体的训练与评测方式。 该模型支持 512K 上下文，可处理文字、图片、视频和音频。根据官方公告，TEMPO 通过自批判和测试时价值估计来训练长程智能体。

telegram · zaihuapd · 8月14日 08:27

**背景**: 在混合专家（MoE）模型中，总参数表示加载到内存中的全部专家，而激活参数是处理每个 token 时实际使用的子集，它决定推理计算成本。这种设计让模型可以扩大容量而不成比例地增加计算开销。VibeSearchBench 是一个用于评测长程主动搜索能力的基准，采用无预置 schema 的知识图谱匹配；VibeLifeBench 则面向真实生活场景中的智能体任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.f22labs.com/blogs/active-vs-total-parameters-whats-the-difference/">Active vs Total Parameters: What’s the Difference?</a></li>
<li><a href="https://osfoundry.io/articles/mixture-of-experts-explained">Mixture of Experts Explained: Total vs Active Parameters ...</a></li>
<li><a href="https://arxiv.org/abs/2605.27882">[2605.27882] VibeSearchBench: Benchmarking Long-horizon ...</a></li>

</ul>
</details>

**标签**: `#MoE`, `#Open Source`, `#Multimodal`, `#Reinforcement Learning`, `#AI`

---

<a id="item-5"></a>
## [RustDesk 为 Wayland 带来真正的无人值守远程访问](https://rustdesk.com/blog/unattended-remote-access-wayland/) ⭐️ 8.0/10

RustDesk 现已支持在 Wayland 上实现真正的无人值守远程访问，用户无需屏幕上有人点击接受即可连接并控制 Linux 机器。这解决了此前 Wayland 系统面临的一个已知限制。 Wayland 的安全设计历来让远程桌面控制变得困难，因此这一变化为 Linux 用户填补了一个重要空白。这同时巩固了 RustDesk 作为 TeamViewer、AnyDesk 等专有工具的开源、可自托管替代方案的地位。 新功能主要针对无人值守会话，即无需用户在场即可访问空闲或锁定的机器。有社区用户指出，自托管 RustDesk 部署仍不支持加密连接，并引用了 GitHub issue \#3714。

hackernews · rustdesk · 8月14日 16:12 · [社区讨论](https://news.ycombinator.com/item?id=49300759)

**背景**: RustDesk 是一款开源远程桌面应用，支持 Windows、macOS、Linux 和 Android，并且可以完全自托管。Wayland 是现代 Linux 显示服务器协议，它限制客户端在未经用户明确同意的情况下注入输入或抓取屏幕，因此历史上使远程控制工具在 Wayland 上的能力不如旧版 X11 系统。无人值守远程访问允许管理员和支持团队全天候连接机器，而无需等待远端用户接受提示。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://rustdesk.com/">RustDesk: Open-Source Remote Desktop with Self-Hosted Server Solutions</a></li>
<li><a href="https://en.wikipedia.org/wiki/Wayland_%28protocol%29">Wayland (protocol) - Wikipedia</a></li>
<li><a href="https://anydesk.com/en/features/unattended-access">Unattended Access Remote Desktop Software | AnyDesk</a></li>

</ul>
</details>

**社区讨论**: 社区反应总体积极，有用户很高兴两天前遇到的这个问题现已解决。评论者还提出了注意事项：有人指出自托管情况下的加密缺口，还有人询问 RustDesk 与 VNC 或通过 SSH/Tailscale 使用 Remmina 相比如何。

**标签**: `#remote-desktop`, `#wayland`, `#linux`, `#rustdesk`, `#open-source`

---

<a id="item-6"></a>
## [Firefox 成为最后仍支持 uBlock Origin 的主流浏览器](https://www.pcworld.com/article/3212428/firefox-is-now-the-last-major-browser-that-still-supports-ublock-origin.html) ⭐️ 8.0/10

Firefox 现在是唯一仍完全支持 uBlock Origin 的主流浏览器，此前基于 Chromium 的浏览器已全面强制执行谷歌的 Manifest V3 变更。这使得 Firefox 成为希望获得全面广告拦截功能的用户的最后选择。 这一转变标志着浏览器扩展能力的重大变化，因为 Manifest V3 限制了大多数主流浏览器中广告拦截器的运作方式。重视隐私和广告拦截的用户可能会越来越转向 Firefox，这可能重塑浏览器市场格局。 Manifest V3 用声明式 netRequest 规则取代了 uBlock Origin 所使用的阻塞式 webRequest API，从而限制了过滤列表和实时拦截能力。Firefox 继续支持 Manifest V2 扩展，使 uBlock Origin 能够保留其完整功能。

hackernews · DemiGuru · 8月14日 19:03 · [社区讨论](https://news.ycombinator.com/item?id=49303202)

**背景**: Manifest V3 是谷歌为 Chrome 及基于 Chromium 的浏览器推出的最新扩展框架，旨在提升安全性和性能。然而，它弃用了强大广告拦截器所依赖的实时阻止网络请求的 API，迫使 uBlock Origin 等扩展要么改用功能受限的版本（如 uBlock Origin Lite），要么停止工作。Firefox 使用自己的扩展系统，选择不禁用 Manifest V2 支持，因此 uBlock Origin 仍能完整运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.chrome.com/docs/extensions/develop/migrate/what-is-mv3">Extensions / Manifest V3 | Chrome for Developers</a></li>
<li><a href="https://adblock-tester.com/ad-blockers/manifest-v3-ad-blocker-impact/">The Manifest V3 Changes — Did Google Just Break Your Ad ...</a></li>
<li><a href="https://brave.com/blog/brave-shields-manifest-v3/">What Manifest V3 means for Brave Shields and the use of extensions in the Brave browser | Brave</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了对 Firefox 的支持和对谷歌变更的不满，其中一位指出 Firefox 会对热门扩展进行安全审查。一些用户谈到了使用 uBlock Origin Lite 的体验，还有人提到因 Manifest V3 而关闭了自己的扩展。

**标签**: `#Firefox`, `#uBlock Origin`, `#Manifest V3`, `#Browser Extensions`, `#Privacy`

---

<a id="item-7"></a>
## [torch-preflight：一个用于检测 PyTorch 训练错误并估算 VRAM 的静态检查工具](https://www.reddit.com/r/MachineLearning/comments/1vo8vv0/a_linter_for_pytorch_torchpreflight_p/) ⭐️ 8.0/10

开发者已在 Reddit 和 PyPI 上发布了 torch-preflight。该工具通过 13 条静态分析规则检查 PyTorch 代码，可捕获常见训练错误并估算 VRAM 占用，无需运行代码，也无需 GPU 或安装 torch。 该工具能在昂贵硬件上运行训练之前发现训练错误，从而为开发者节省大量 GPU 机时和云成本。其 VRAM 估算功能可帮助从业者在付费租用实例前判断训练是否能在目标 GPU 上运行。 torch-preflight 目前实现了 13 条规则，其 VRAM 估算在四块模型、一块 T4 上的测试结果与实测峰值误差在 4%以内。该工具从不导入或执行用户代码，因此无需 GPU 和 torch 安装；目前仍在开发中，欢迎贡献代码。

reddit · r/MachineLearning · /u/LeJanbandhu · 8月14日 14:30

**背景**: PyTorch 的 autograd 系统通过记录张量和操作来构建有向无环图（DAG），从而在反向传播时自动计算梯度。常见错误包括把 loss 保存在列表中，导致 autograd 计算图一直被保留、最终耗尽 GPU 显存；或者忘记调用 zero\_grad\(\)，导致梯度不断累积。在使用 DDP 进行分布式训练时，如果使用普通采样器而不是 DistributedSampler，每个 rank 都会在相同批次上训练。linter（静态检查工具）不执行代码，而是通过静态分析源码来发现这类模式，从而实现低成本的训练前检查。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.pytorch.org/tutorials/beginner/blitz/autograd_tutorial.html">A Gentle Introduction to torch.autograd — PyTorch Tutorials 2.13.0+cu130 documentation</a></li>
<li><a href="https://github.com/pytorch/pytorch/blob/main/torch/utils/data/distributed.py">pytorch/torch/utils/data/distributed.py at main · pytorch ...</a></li>

</ul>
</details>

**标签**: `#PyTorch`, `#linter`, `#machine-learning`, `#developer-tools`, `#VRAM`

---

<a id="item-8"></a>
## [AI 机器人实验室每年测 300 万人体组织，有望终结动物测试](https://www.fastcompany.com/91589344/the-worlds-largest-biological-datacenter-could-help-make-animal-testing-obsolete) ⭐️ 8.0/10

Vivodyne 位于旧金山湾区的自主“蜂巢”实验室利用 AI 设计并每年执行超过 300 万次的人体组织受控实验，其容量约为全美临床试验总量的一倍。这种工业化规模的平台可能使动物测试在药物开发中变得过时。 鉴于约 90%的临床试验在通过动物测试后仍然失败，像 Vivodyne 这样的人体组织平台可能大幅提高药物成功率并加速疗法开发。这标志着向 AI 驱动、与人类相关的临床前测试的重大转变，可能重塑生物技术和制药行业。 该系统目前由 12 个“蜂巢”机器人实验室组成，每个实验室约一个衣柜大小，负责培养人体组织并运行 AI 设计的实验。Vivodyne 声称其容量超过了美国所有临床试验的总量。

telegram · zaihuapd · 8月14日 01:48

**背景**: 类器官是模拟真实器官结构和功能的三维细胞培养物，而器官芯片设备利用微流控通道模拟器官级别的反应；两者都是公认的动物模型替代方案。Vivodyne 在这些技术基础上，利用 AI 将其工业化、自动化，为药物发现和毒理学测试生成与人类相关的数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.vivodyne.com/">Vivodyne | Make biology computable</a></li>
<li><a href="https://en.wikipedia.org/wiki/Organoid">Organoid - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Organ-on-a-chip">Organ-on-a-chip</a></li>

</ul>
</details>

**标签**: `#AI`, `#biotech`, `#drug discovery`, `#animal testing`, `#automation`

---

<a id="item-9"></a>
## [美法官令谷歌一周内取消第三方应用商店安装阻碍](https://www.androidauthority.com/google-play-store-remove-third-party-app-store-friction-3698697/) ⭐️ 8.0/10

美国地区法官下令谷歌在一周内删除 Play Store 中安装第三方安卓应用商店时的多余步骤和警告弹窗。这一指令源自 Epic 诉谷歌反垄断案，陪审团此前裁定谷歌在安卓应用分发上构成非法垄断。 这是一项具有很短时间内合规期限的重大反垄断执法行动，直接改变了安卓用户安装竞争性应用商店的方式。它可能大幅降低替代应用市场的准入门槛，并重塑安卓应用分发的商业格局。 法官 James Donato 认定，Play Store 中‘查看’后才出现‘安装’等多步提示是蓄意制造的‘反竞争摩擦’，目的是劝阻普通用户安装竞品商店。谷歌必须让安装第三方商店像安装普通安卓应用一样直接，并在命令下达后一周内完成修改。

telegram · zaihuapd · 8月14日 09:55

**背景**: 在安卓系统中，‘侧载’（sideloading）通常指通过 APK 格式安装 Play 商店之外的应用程序。Google Play Protect 会扫描应用是否有害行为，并常在用户尝试侧载时显示警告，批评者认为这种做法可能被用来吓阻用户。此次命令是 Epic 诉谷歌案的一部分，该案的核心问题是谷歌对安卓应用分发的控制是否构成非法垄断。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Sideloading">Sideloading - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Google_Play_Protect">Google Play Protect</a></li>

</ul>
</details>

**标签**: `#antitrust`, `#android`, `#google`, `#app-store`, `#regulation`

---

<a id="item-10"></a>
## [PostgreSQL 修复高危 to\_char 堆溢出漏洞，可致任意代码执行](https://www.postgresql.org/support/security/CVE-2026-14669/) ⭐️ 8.0/10

PostgreSQL 披露了 CVE-2026-14669，这是 to\_char\(timestamptz\) 函数在处理超长 POSIX 时区缩写时出现的严重堆缓冲区溢出漏洞。该漏洞（CVSS 8.8）可让低权限数据库用户以 PostgreSQL 服务进程的操作系统权限执行任意代码。 这是一个只需低权限数据库账户即可触发的高危漏洞，对任何运行 PostgreSQL 的组织都至关重要。管理员必须立即修补，因为一旦被利用成功，可能导致服务器被完全控制。 受影响版本包括 18.5、17.11、16.15、15.19 和 14.24 之前的 PostgreSQL 版本；由于 18.5 因回归问题未正式发布，18 系列用户应直接升级到 18.6。此次小版本更新不需要转储数据库或运行 pg\_upgrade，只需更新程序文件并重启服务。

telegram · zaihuapd · 8月14日 14:35

**背景**: PostgreSQL 的 to\_char\(timestamptz\) 函数用于将带时区的时间戳转换为格式化的文本字符串。堆缓冲区溢出是指写入动态分配内存区域的数据量超出其分配大小，此类缺陷通常可被利用来执行任意代码。POSIX 时区字符串（如 EST5EDT）编码了偏移量和夏令时规则，过长的时区缩写会触发该溢出。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Heap_overflow">Heap overflow - Wikipedia</a></li>
<li><a href="https://cwe.mitre.org/data/definitions/122.html">CWE - CWE-122: Heap-based Buffer Overflow (4.20)</a></li>
<li><a href="https://www.enterprisedb.com/docs/epas/latest/reference/sql_reference/03_functions_and_operators/07_data_type_formatting_functions/">EDB Postgres Advanced Server v18 - Data type formatting functions</a></li>

</ul>
</details>

**标签**: `#PostgreSQL`, `#security`, `#CVE`, `#vulnerability`, `#database`

---

<a id="item-11"></a>
## [苹果联手阿里自研中国专属 AI 模型，力争首家获批外企](https://www.reuters.com/business/retail-consumer/apple-trains-its-own-ai-model-china-market-with-alibabas-support-sources-say-2026-08-14/) ⭐️ 8.0/10

据知情人士透露，苹果已在阿里巴巴支持下为中国市场训练了一款专属大语言模型。中国网信办上月已备案苹果的生成式 AI 服务，Apple Intelligence 预计未来数月随 iOS 更新在华上线。 这一战略举措可能使苹果成为首个获准在华提供自有 AI 模型的外国公司，从而更好地掌控中国市场的 AI 体验，并为其他外资 AI 企业应对中国严格的监管环境开创先例，也有助于苹果与本土厂商竞争。 苹果此前在华依赖第三方模型，自研方式将使其在内容审核等功能上拥有更大掌控力。中国网信办上月已完成对其生成式 AI 服务的备案，但具体模型细节和上线日期尚未透露。

telegram · zaihuapd · 8月14日 14:47

**背景**: Apple Intelligence 是苹果推出的生成式 AI 系统，深度集成于 iOS 18、iPadOS 18 和 macOS Sequoia，结合设备端与服务器端处理，已于 2024 年秋季在美国上线，2025 年逐步开放更多国家。根据 2023 年 8 月 15 日施行的《生成式人工智能服务管理暂行办法》，凡向中国境内公众提供具有舆论属性或社会动员能力的生成式 AI 服务，无论内资还是外资主体，上线前均须向国家网信办完成备案。这一监管要求同样适用于外国企业。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zh.wikipedia.org/wiki/Apple_Intelligence">Apple Intelligence - 维基百科，自由的百科全书</a></li>
<li><a href="https://www.gov.cn/zhengce/zhengceku/202307/content_6891752.htm">生成式人工智能服务管理暂行办法_国务院部门文件_中国政府网</a></li>
<li><a href="https://blog.csdn.net/2409_87369594/article/details/161394346">生成式人工智能网信办备案全流程详解 - CSDN博客</a></li>

</ul>
</details>

**标签**: `#Apple`, `#AI`, `#China`, `#Alibaba`, `#LLM`

---