---
layout: default
title: "Horizon Summary: 2026-08-13 (ZH)"
date: 2026-08-13
lang: zh
---

> 从 34 条内容中筛选出 11 条重要资讯。

---

1. [新工具利用 Rowhammer 逆向 DRAM 寻址](#item-1) ⭐️ 9.0/10
2. [选择无聊技术：为创新代币设定预算](#item-2) ⭐️ 9.0/10
3. [DeepMind 推手语转文字模型 SL2T，首次落地 Pixel 11 键盘与实时字幕](#item-3) ⭐️ 9.0/10
4. [DeepSeek-V4-Pro 上线，推出 Agent 增强与峰谷定价](#item-4) ⭐️ 9.0/10
5. [谷歌发布 Gemini 3.7 Flash，支持视觉且价格将上调](#item-5) ⭐️ 8.0/10
6. [Cerebras 与 OpenAI 加速 GPT-5.6 Sol 超快速模式](#item-6) ⭐️ 8.0/10
7. [DeepSeek 发布开源 AI harness 开发者预览版](#item-7) ⭐️ 8.0/10
8. [Gloomberb 为金融数据带来开源平铺终端。](#item-8) ⭐️ 8.0/10
9. [DeepSeek V4 Pro 0813 发布，开放权重已上架 Hugging Face](#item-9) ⭐️ 8.0/10
10. [特朗普签署备忘录，允许私企参与海外监控与网络攻击](#item-10) ⭐️ 8.0/10
11. [DeepSeek 发布开源 Harness 与 V4-Pro-0813 权重](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [新工具利用 Rowhammer 逆向 DRAM 寻址](https://github.com/xoreaxeaxeax/skitter-creek-bath-salts) ⭐️ 9.0/10

Christopher Domas 发布了「Spaghettifying DRAM」工具，利用 Rowhammer 效应逆向工程 DRAM 的行/组/列地址映射。该工具在 GitHub 上以「skitter-creek-bath-salts」仓库发布。 这项研究揭示了现代 DRAM 中一个巨大且大部分隐藏的攻击面，可能使拥有 ring-0 权限的攻击者触及通常受“负环”保护的数据。它还对 Xbox 和 PlayStation 等游戏机的安全构成潜在威胁，此前这些硬件隔离被认为很强。 该工具适用于 2013 年的 AMD Jaguar 架构；README 中提到 Zen 3 的内存控制器寄存器基地址不同，因此对更新 CPU 的适用性尚不明确。通过推导行、组、列物理地址位分配，它能够实现定向的 Rowhammer 攻击和更深入的内存检查。

hackernews · matt\_d · 8月13日 14:17 · [社区讨论](https://news.ycombinator.com/item?id=49286341)

**背景**: DRAM 芯片按组\(bank\)、行\(row\)和列\(column\)组织，内存控制器通常使用专有的位分配将物理地址映射到这些结构。Rowhammer 效应是 DRAM 的一种可靠性副作用，快速访问一行可能导致相邻行中的比特翻转，并且它已成为已知的安全漏洞。了解确切的地址映射可以提高攻击者定位翻转的能力，该工具正是实现了这一过程的自动化。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Row_hammer">Row hammer - Wikipedia</a></li>
<li><a href="https://www.mdpi.com/1424-8220/24/2/592">Rowhammer Attacks in Dynamic Random-Access Memory and ... - MDPI</a></li>
<li><a href="https://people.inf.ethz.ch/omutlu/pub/onur-Bogazici-June-13-2013-lecture2-1-dram-basics-and-scaling-afterlecture.pptx">Memory Systems in the Multi-Core EraLecture 1: DRAM Basics and...</a></li>

</ul>
</details>

**社区讨论**: 评论者对 Christopher Domas 即将进行的 Black Hat 演讲表示热情，称赞他解释复杂研究的能力。一些评论者担心这对游戏机安全的影响，另一些则询问除旧款 AMD Jaguar 架构外，哪些较新的 CPU 也受影响。

**标签**: `#DRAM`, `#security`, `#reverse-engineering`, `#hardware`, `#rowhammer`

---

<a id="item-2"></a>
## [选择无聊技术：为创新代币设定预算](https://mcfunley.com/choose-boring-technology) ⭐️ 9.0/10

丹·麦金利（Dan McKinley）2015 年的文章《选择无聊技术》提出，每家公司的“创新代币”预算大约只有三枚，应只把它们花在能直接让产品与众不同的技术上。这篇文章近日在 Hacker News 重新引发讨论，获得 212 个积分和 116 条评论。 “创新代币”框架为工程师和管理者提供了一种简单且易记的方式，用于论证务实的技术选择并抵制追逐热点的技术采纳。在团队评估新工具、AI 智能体以及基础设施决策时，这一框架依然具有很强的现实意义。 麦金利于 2015 年首次发表这篇文章，基于他构建可扩展系统的经验；他认为，每引入一项新技术都会带来维护和集成成本。在 Hacker News 的讨论中，有评论者指出，一个合理的现代应用方式是把所有创新代币花在 AI 智能体层上，而让周边技术栈保持“无聊”。

hackernews · tosh · 8月13日 17:48 · [社区讨论](https://news.ycombinator.com/item?id=49289512)

**背景**: 这篇文章让“创新代币”一词广为人知：它是偏离常规做法时的有限预算。所谓“boring（无聊）技术”并不是指平淡无奇的工具，而是指成熟、被充分理解、失败模式已知的技术。这一概念与横井军平提出的“枯れた技術の水平思考”（利用过时技术的横向思维）等早期工程理念相呼应，并已成为软件工程中务实主义与追求新奇之间辩论的经典参照。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mcfunley.com/choose-boring-technology">Dan McKinley :: Choose Boring Technology</a></li>
<li><a href="https://www.lessannoyingbusiness.com/post/innovation-tokens">Innovation Tokens - When to break from the status quo</a></li>
<li><a href="https://xebia.com/blog/how-innovation-tokens-can-change-your-life/">How Innovation Tokens Can Change Your Life | Xebia</a></li>

</ul>
</details>

**社区讨论**: 评论者大多称赞这篇文章：有人说这是自己最喜欢的博文，“创新代币”概念有助于向各级同事解释权衡；还有人希望有一个专门筛选务实工程文化的招聘平台。有评论者提出，在 AI 智能体时代，团队应把所有创新代币投入到智能体中，并在其周围使用“分布内”的无聊技术。然而，也有反对者认为“创新代币”过于随意，“新颖”只是风险和价值的薄弱代理指标。

**标签**: `#technology-choice`, `#innovation-tokens`, `#software-engineering`, `#pragmatism`, `#engineering-culture`

---

<a id="item-3"></a>
## [DeepMind 推手语转文字模型 SL2T，首次落地 Pixel 11 键盘与实时字幕](https://deepmind.google/blog/putting-sign-language-ai-into-users-hands/) ⭐️ 9.0/10

谷歌 DeepMind 发布了多语言手语转文字模型 SL2T，并首次将其部署到 Pixel 11 的 Gboard 和 Live Transcribe 中，首批支持美国手语到英语的转换。 这标志着手语 AI 首次被集成到主流消费产品中，有望改善聋人和听障用户的无障碍体验，并为未来各类设备上的无障碍功能树立了先例。 SL2T 使用超过 10 万小时、涵盖 50 多种手语的视频数据训练，在 FLEURS-ASL 基准上零样本得分为 70 BLEURT。出于隐私保护，它只处理手部和身体姿态关键点，而不读取原始视频帧。

telegram · zaihuapd · 8月13日 08:55

**背景**: BLEURT 是一种基于学习得到的自然语言生成评估指标，通过参考文本与候选文本的流畅度和语义一致性来衡量翻译或生成质量。FLEURS-ASL 是 FLORES/FLEURS 基准的扩展，首次加入美国手语视频，用于评估手语翻译任务。姿态关键点检测是计算机视觉技术，通过追踪人体手部和身体的关键位置，使模型无需存储或处理可识别的原始视频即可理解手语。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2004.04696">BLEURT: Learning Robust Metrics for Text Generation BLEURT: Learning Robust Metrics for Text Generation BLEURT Explained: A Learned Metric for AI Text Quality Bleurt Metric: A Comprehensive Guide for 2025 - Shadecoder ... bleurt/README.md at master · google-research/bleurt · GitHub bleurt.py · evaluate-metric/bleurt at main - Hugging Face</a></li>
<li><a href="https://aclanthology.org/2025.naacl-long.314/">FLEURS-ASL: Including American Sign Language in Massively Multilingual Multitask Evaluation - ACL Anthology</a></li>
<li><a href="https://viso.ai/deep-learning/pose-estimation-ultimate-overview/">Real-Time Pose Estimation in Computer Vision</a></li>

</ul>
</details>

**标签**: `#sign language`, `#accessibility`, `#DeepMind`, `#AI model`, `#Pixel`

---

<a id="item-4"></a>
## [DeepSeek-V4-Pro 上线，推出 Agent 增强与峰谷定价](https://api-docs.deepseek.com/zh-cn/updates) ⭐️ 9.0/10

DeepSeek-V4-Pro 现已正式在 App、网页端和 API 上线，模型名为 deepseek-v4-pro。新版本增强了 Agent 能力，原生支持 Responses API 格式以兼容 Codex，并自 2026 年 8 月 17 日起实行峰谷定价，闲时价格为高峰时段的一半。 DeepSeek 是一个被广泛采用的模型系列，因此这次重大更新将强化其在构建 Agent 应用的开发者中的竞争力。兼容 OpenAI 的 Responses API 和 Codex 降低了团队在现有工具链中使用或切换至 DeepSeek 的门槛，而分时定价也为成本优化提供了新的杠杆。 API 调用方式保持不变，模型名设为 deepseek-v4-pro。V4-Pro 和 V4-Flash 的思考模式现在支持 low、high、max 三档，新价格自 2026 年 8 月 17 日 0 时起生效。

telegram · zaihuapd · 8月13日 11:12

**背景**: DeepSeek 是一家提供大语言模型 API 的中国 AI 公司。Responses API 是 OpenAI 于 2025 年 3 月发布的一种开发者工具，旨在简化 Agent 应用的构建；Codex 则是 OpenAI 的 AI 编程智能体，可集成到多种 IDE 中。通过原生支持 Responses API 格式，DeepSeek 使其模型可以在围绕该标准构建的工具和工作流中使用，包括兼容 Codex 的环境。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://grokipedia.com/page/OpenAI_Responses_API">OpenAI Responses API</a></li>
<li><a href="https://en.wikipedia.org/wiki/Codex_%28AI_agent%29">Codex (AI agent)</a></li>
<li><a href="https://developers.openai.com/api/reference/responses/overview">Responses Overview | OpenAI API Reference</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#AI`, `#API`, `#LLM`, `#Pricing`

---

<a id="item-5"></a>
## [谷歌发布 Gemini 3.7 Flash，支持视觉且价格将上调](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-3-7-flash/) ⭐️ 8.0/10

谷歌发布了 Gemini 3.7 Flash，这是基于 Gemini 3.6 Flash 构建、支持视觉的新模型，其介绍性定价将于 2026 年 12 月 31 日翻倍。该模型在文档处理与自动化基准测试上提升显著，并已开始为 AI Pro 和 Ultra 订阅用户的 Gemini Spark 提供支持。 Gemini 3.7 Flash 强化了谷歌面向低成本、大规模场景的“主力”模型层级，让开发者与企业更容易获得先进的推理与多模态能力。此次发布也加剧了与 GPT-5.6 Luna、Terra 等快速廉价模型之间的竞争，价格与实际性能正成为关键竞争点。 该模型基于 Gemini 3.6 Flash，支持 1M token 上下文窗口，可输入文本、图像、音频和视频。它在 GDP.pdf 基准上较 3.6 Flash 提升明显（34.0% 对 22.0%），在 AutomationBench 上亦如此（30.4% 对 17.0%）；在高推理强度下，其每任务耗时比 GPT-5.6 Terra \(max\) 快 40%，且在促销期内输入 token 仅 $1.50/1M、输出 token 仅 $7.50/1M。

hackernews · thisisauserid · 8月13日 17:23 · [社区讨论](https://news.ycombinator.com/item?id=49289112)

**背景**: Gemini Flash 是谷歌面向大规模、低延迟任务（如摘要、解析、编程智能体）设计的高性价比模型系列，与更高端的 Pro 模型形成互补。Gemini 3.7 Flash 延续了这一路线，加入了可调推理强度（高/中/低）和多模态支持。这类混合推理模型通常会引起社区围绕性价比与基准成绩的大量实测与讨论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-3-7-flash/">Gemini 3 . 7 Flash : our most intelligent workhorse model</a></li>
<li><a href="https://deepmind.google/models/model-cards/gemini-3-7-flash/">Gemini 3 . 7 Flash - Model Card — Google DeepMind</a></li>
<li><a href="https://artificialanalysis.ai/articles/gemini-3-7-time-frontier">Gemini 3 . 7 Flash : On the Intelligence vs . Time per Task Pareto frontier</a></li>

</ul>
</details>

**社区讨论**: 评论者分享了实际测试与不同看法：有人认为 Gemini 3.7 Flash 在图像转 HTML 方面表现不错，但仍不如 Opus 5；也有人认可其性价比，但质疑在 3.6 Flash 发布仅几周后便计划提价。还有多位评论者将其与 GPT-5.6 Luna、Terra 对比，认为 Luna 更便宜且在 DeepSWE 上表现更强，可能削弱 Flash 系列的价值。

**标签**: `#AI`, `#Google`, `#Gemini`, `#LLM`, `#Model Release`

---

<a id="item-6"></a>
## [Cerebras 与 OpenAI 加速 GPT-5.6 Sol 超快速模式](https://www.cerebras.ai/blog/accelerating-gpt-5-6-sol-ultrafast-with-openai) ⭐️ 8.0/10

OpenAI 与 Cerebras 宣布，GPT-5.6 Sol 的“超快速”模式仅用 11 小时 11 分钟回答了 Humanity&\#x27;s Last Exam 的全部 2,500 道题，约为竞争对手 Claude Fable 5 所需 78 小时的七分之一，同时保持了相当的准确性。这一结果标志着两家公司合作取得了重要里程碑。 这一加速意义重大，因为前沿推理任务（如解答 Humanity&\#x27;s Last Exam）目前需要数小时连续计算；将其速度提升 7 倍，可以拓展更多实际应用并降低部署成本。这也表明 Cerebras 的晶圆级引擎等专用硬件，能够在最先进的推理负载中与基于 GPU 的云服务展开有力竞争。 尽管速度大幅提升，但 Cerebras 和 OpenAI 均未明确表示超快速模式在全部基准上都与标准 GPT-5.6 Sol 表现一致——官方文章仅称其在 HLE 上“准确性相当”。OpenAI 的配套文章也未公布该模式的定价，且独立排行榜给出的输出速度存在差异（如 Artificial Analysis 显示超快速模式比 Fable 5 快 11 倍、比 Opus 4.8 Fast 快 5 倍）。

hackernews · pr337h4m · 8月13日 18:10 · [社区讨论](https://news.ycombinator.com/item?id=49289844)

**背景**: Humanity&\#x27;s Last Exam \(HLE\) 是一个前沿 AI 基准测试，包含 2,500 道由专家编写的涵盖数学、科学与人文学科的问题，旨在衡量大语言模型的知识上限。Cerebras Systems 是一家硅谷公司，以晶圆级引擎（Wafer-Scale Engine）闻名，这是世界上最大的 AI 处理器，被用于其 CS-3 超级计算机和 AI 推理/训练云服务。GPT-5.6 Sol 是 OpenAI 在 GPT-5.6 系列中的旗舰模型，面向复杂推理、编程和智能体工作流。此次合作旨在证明 Cerebras 的晶圆级硬件能够在长程推理任务中以远超传统 GPU 集群的速度运行这类模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cerebras_Systems">Cerebras Systems - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Humanity&#x27;s_Last_Exam">Humanity&#x27;s Last Exam - Wikipedia</a></li>
<li><a href="https://openrouter.ai/openai/gpt-5.6-sol">GPT - 5 . 6 Sol - API Pricing &amp; Benchmarks | OpenRouter</a></li>

</ul>
</details>

**社区讨论**: 社区反应是兴奋与怀疑并存。部分评论者对 OpenAI 与 Cerebras 的合作终于带来了瞩目的加速感到激动，并认为更快的推理支持迭代思考和更优输出；但也有评论者指出，两家公司都没有明确确认超快速模式在行为上与标准 GPT-5.6 Sol 完全一致，而且未公布定价，暗示它可能面向小众且昂贵的应用场景。

**标签**: `#AI`, `#LLM`, `#inference speed`, `#OpenAI`, `#Cerebras`

---

<a id="item-7"></a>
## [DeepSeek 发布开源 AI harness 开发者预览版](https://deepseek.com/harness/en/) ⭐️ 8.0/10

DeepSeek 已在 GitHub 上以 MIT 许可证发布 DeepSeek Harness 的早期开发者预览版，具备完整运行可追溯性和基于插件的架构。该预览版包含文档，并被定位为一个粗糙、可能存在破坏性变更的早期版本。 这很重要，因为一家主要 AI 实验室正在开源一个核心智能体基础设施工具，可能加速社区在 AI 智能体开发方面的创新。完整的可追溯性功能尤其值得关注，因为它提供了可审计的事件流，评论者称美国模型并不提供这一能力。 该 harness 使用 Cordis v4，这是一个支持热重载的插件系统，可以在不重启进程的情况下卸载插件并回滚其副作用。每次运行都会写入仅追加的会话日志，涵盖系统提示、推理、工具调用和子智能体调度，从而支持恢复、分叉、搜索和重放操作。

hackernews · bjin · 8月13日 12:58 · [社区讨论](https://news.ycombinator.com/item?id=49285244)

**背景**: AI agent harness 是围绕语言模型的软件脚手架，用于管理工具、记忆、沙箱和反馈循环，将模型转变为智能体。AI 可追溯性指的是通过关联数据源、提示词、模型版本和部署上下文来重建模型输出产生过程的能力，这有助于审计和问责。DeepSeek Harness 似乎通过为智能体工作负载提供透明、基于插件的运行时，将这两个概念结合起来。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://harness-engineering.ai/blog/agent-harness-complete-guide/">The Complete Guide to Agent Harness: What It Is and Why It ...</a></li>
<li><a href="https://www.databricks.com/blog/ai-harness">What is an AI Agent Harness? | Databricks Blog</a></li>
<li><a href="https://data.world/blog/what-is-ai-traceability-benefits-tools-best-practices/">What is AI traceability? Benefits, tools &amp; best practices</a></li>

</ul>
</details>

**社区讨论**: 一位作者确认这是 MIT 许可证下的早期开发者预览版，并欢迎反馈。评论者强调完整可追溯性是一个杀手级功能，尤其是与来自美国模型的加密或混淆轨迹相比；其他人则指出插件系统与 Cordis/Koishi 相似，也有人表达了对插件疲劳的担忧。

**标签**: `#DeepSeek`, `#AI tools`, `#open-source`, `#developer tools`, `#tracing`

---

<a id="item-8"></a>
## [Gloomberb 为金融数据带来开源平铺终端。](https://gloom.sh/) ⭐️ 8.0/10

Gloomberb 是一款开源的终端金融终端，已推出以命令栏为优先的平铺界面，用户可输入股票代码或 DES AAPL 等快捷键直接进入行情视图。它通过开源技术栈提供市场数据，但不包含 Bloomberg 的专有数据连接。 这很重要，因为它将类似 Bloomberg 的终端体验带入了开源生态，可能降低开发者与散户使用专业金融数据工具的门槛。它反映出金融领域对替代性终端界面的需求日益增长，尽管无法取代 Bloomberg 的专有数据。 平铺界面将面板以非重叠方式布局，且界面以命令栏为优先，支持 TOP 等快捷键。一些用户反映，让某个面板跟随另一面板所选股票代码的操作并不直观；目前安装方式为 curl 脚本，而非标准包管理器。

hackernews · rbanffy · 8月13日 13:52 · [社区讨论](https://news.ycombinator.com/item?id=49285982)

**背景**: Gloomberb 是一款运行在用户终端中的金融终端，灵感来自 Bloomberg Terminal——一种广泛用于专业领域的订阅制金融软件。Bloomberg Terminal 提供实时行情、新闻和分析，每位用户每年费用约为 31,980 美元。Gloomberb 使用非专有数据源提供类似的命令驱动和平铺界面，但缺少 Bloomberg 的专有数据源。平铺窗口管理器是 Gloomberb 界面的设计理念，它把窗口组织成非重叠框架。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://gloom.sh/">Gloomberb</a></li>
<li><a href="https://github.com/gloom-sh/gloomberb">GitHub - gloom-sh/gloomberb: Finance terminal, in your ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Tiling_window_manager">Tiling window manager</a></li>

</ul>
</details>

**社区讨论**: 评论者总体上很感兴趣，但也指出了局限：有人质疑基于 curl 的安装方式和依赖处理，还有人指出 Bloomberg 的真正价值在于专有数据，而非终端界面。一些用户认为平铺界面实用易学，但也有人对面板股票联动感到困惑，另有人提到了 Godel Terminal 等替代终端。

**标签**: `#terminal`, `#finance`, `#TUI`, `#open-source`, `#bloomberg`

---

<a id="item-9"></a>
## [DeepSeek V4 Pro 0813 发布，开放权重已上架 Hugging Face](https://simonwillison.net/2026/Aug/12/deepseek-v4-pro-0813/) ⭐️ 8.0/10

DeepSeek V4 Pro 0813 现已通过 OpenRouter 提供 API 服务，其开放权重也已上传到 Hugging Face，参数规模达 1.7 万亿（约 893 GB）。此次发布没有 DeepSeek 官方的公告页面，因此 OpenRouter 的模型列表和 Hugging Face 的上传成为主要获取渠道。 这是 DeepSeek 在开放权重领域一次重要的大模型发布，而 DeepSeek 是该领域最有影响力的开发者之一。这款 1.7T 参数的模型很可能推动其在 API 产品和本地部署中的广泛采用，延续了强大开放权重模型挑战闭源产品的行业趋势。 Hugging Face 仓库显示该模型有 1.7 万亿参数、文件大小约 893 GB，是目前最大的开放权重模型之一。基准测试最初发布在 DeepSeek 官方微信群中，随后被转贴到 Reddit 但遭到版主以“低质量”为由删除，最终又出现在 Hacker News 的一个 ASCII 艺术表格里；另外 Simon Willison 在“鹈鹕骑自行车”的渲染测试中发现，低、中、高三种推理级别下输出差异异常明显。

rss · Simon Willison · 8月12日 23:59

**背景**: 开放权重模型允许任何人下载训练好的权重并在本地运行推理，但通常不包含完整训练数据和训练流程，这与真正的开源 AI 有所不同。DeepSeek 历来以开放权重的方式发布模型，因此被开发者和研究人员广泛使用。OpenRouter 是一个统一的 API 平台，用户可以通过一个端点访问来自不同提供商的数百种大语言模型，这也是为什么在新模型官方文档尚未发布时，OpenRouter 常常成为第一个可实际试用该模型的渠道。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openrouter.ai/models">Compare AI Models : Pricing, Context &amp; Benchmarks | OpenRouter</a></li>
<li><a href="https://www.pbs.org/newshour/science/whats-the-difference-between-closed-open%E2%80%91source-and-open-weight-ai-a-researcher-explains">What&#x27;s the difference between closed, open‑source and open-weight AI? A researcher explains | PBS News</a></li>
<li><a href="https://neysa.ai/blog/open-weights-open-source/">AI Models: Why Open Weights ≠ Open Source</a></li>

</ul>
</details>

**社区讨论**: 社区讨论内容有限：基准测试表格最初被 Reddit 版主以“低质量”删除，之后又被发布在 Hacker News 上以 ASCII 艺术表格形式流传。总体来看，社区认为此次发布本身影响重大，但缺少官方公告以及基准测试传播方式零散也引发了一些批评。

**标签**: `#AI`, `#DeepSeek`, `#model release`, `#open weights`, `#LLM`

---

<a id="item-10"></a>
## [特朗普签署备忘录，允许私企参与海外监控与网络攻击](https://www.bloomberg.com/news/articles/2026-08-13/trump-enlists-private-sector-to-boost-cyber-offensive-arsenal) ⭐️ 8.0/10

美国总统特朗普签署备忘录，允许在联邦政府直接监督下的私营企业在海外开展监控和网络攻击，以打击针对美国人的外国犯罪网络。国土安全部将负责运行该项目，并与司法部协调监督。 这是一项重大政策转变，将私营部门引入美国政府背书的进攻性网络行动和监控领域，可能扩大美国的网络武器库，同时也引发对监督和问责的担忧。这种做法可能为其他国家树立先例，并加深私营企业在国家安全中的角色。 参与企业必须维持至少 100 万美元的保证金或托管款，如不遵守合同约定，该款项将被没收。该项目由联邦政府直接控制和监督，国土安全部牵头，司法部协调监督。

telegram · zaihuapd · 8月13日 05:10

**背景**: 传统上，进攻性网络行动和监控属于国家安全局、美国网络司令部等政府机构的职责范围。这份备忘录背离了这一惯例，授权私营企业在美国政府背书下行动，反映出利用私营部门网络安全专长的更广泛趋势。然而，这也引发了关于企业在军事化行动中参与边界的新的法律和伦理问题。

**标签**: `#cybersecurity`, `#government policy`, `#surveillance`, `#cyber warfare`, `#private sector`

---

<a id="item-11"></a>
## [DeepSeek 发布开源 Harness 与 V4-Pro-0813 权重](https://mp.weixin.qq.com/s/mANdGRI4fO_sEbC1ECEoZQ) ⭐️ 8.0/10

DeepSeek 以 MIT 协议发布了开源应用 DeepSeek Harness，并在 Hugging Face 开放了 DeepSeek-V4-Pro-0813 模型权重。该 Harness 采用“一切皆插件”的架构，提供标准、PTC、极简和创造四种运行模式。 此次发布提供了一个开源的、与模型无关的智能体基础设施替代方案，类似于 Claude Code 和 Codex 背后的架构，降低了开发者构建自定义 agent harness 的门槛。同时开放 V4-Pro-0813 权重也进一步提升了整个 AI/ML 社区对模型的可获取性。 DeepSeek Harness \(dsh\) 由 Cordis 驱动，其设计在《A Programming Paradigm for Spatiotemporal Composability》中描述。DeepSeek-V4-Pro-0813 是一个混合专家模型，拥有 1,048,576 token 的上下文窗口和 384,000 token 的最大输出长度；Hugging Face 页面曾短暂返回 404，随后已恢复。

telegram · zaihuapd · 8月13日 12:39

**背景**: Agent harness 是一种软件框架，用于编排模型、工具和 UI 以构建 AI 智能体，类似于测试 harness 编排测试执行。DeepSeek 的做法把每一项能力——模型、工具、技能、会话、沙箱、存储、调度和 UI——都设计为可替换插件，从而实现灵活重组。混合专家（MoE）是一种 LLM 架构，每个 token 会激活不同的专用子网络（专家），使大模型比密集模型更具计算效率。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/deepseek-ai/deepseek-harness/tree/master">DeepSeek Harness - GitHub</a></li>
<li><a href="https://huggingface.co/multimodalart/DeepSeek-V4-Pro-0813">multimodalart/ DeepSeek - V 4 - Pro - 0813 · Hugging Face</a></li>
<li><a href="https://venturebeat.com/technology/deepseek-harness-launches-as-open-source-rival-to-claude-code-alongside-v4-pro-on-api-with-higher-prices">DeepSeek Harness launches as open source rival to Claude Code ...</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#LLM`, `#open-source`, `#AI`, `#model-release`

---