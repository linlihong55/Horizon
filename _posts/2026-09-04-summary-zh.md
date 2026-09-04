---
layout: default
title: "Horizon Summary: 2026-09-04 (ZH)"
date: 2026-09-04
lang: zh
---

> 从 33 条内容中筛选出 6 条重要资讯。

---

1. [OpenAI 发布 GPT-6 Astra，ARC-AGI-3 得分 99.9%](#item-1) ⭐️ 10.0/10
2. [开发者用 Claude LLM 将 1993 年 Amiga 汇编游戏移植到 Godot](#item-2) ⭐️ 8.0/10
3. [围棋大师申真谞让两子击败 AI KataGo](#item-3) ⭐️ 8.0/10
4. [Audacity 4.0 发布，改用 Qt6 界面，社区反应不一](#item-4) ⭐️ 8.0/10
5. [谷歌 Antigravity 条款引发担忧：第三方使用 AI 可能导致整个账号被封](#item-5) ⭐️ 8.0/10
6. [美国政府支持 OpenAI：AI 训练属合理使用](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI 发布 GPT-6 Astra，ARC-AGI-3 得分 99.9%](https://openai.com/index/gpt-6-astra/) ⭐️ 10.0/10

OpenAI 发布了新一代前沿模型 GPT-6 Astra，官方称其在 ARC-AGI-3 基准上取得 99.9% 的分数，并在其他评测中有所提升。OpenAI 同时发布了系统卡并开始推送该模型；社区也分别围绕部署、ARC-AGI-3 结果和编码智能体表现展开讨论。 接近满分的 ARC-AGI-3 成绩意义重大，因为该基准要求智能体在陌生交互环境中推断目标、学习规则，而不只是回放训练数据。若该结果经得起推敲，GPT-6 Astra 可能重新定义 OpenAI、Google、Anthropic 等实验室在智能体 AI 上的竞争格局，并让“扩展规模是否仍能推动通用智能”的争论更加激烈。 99.9% 的 ARC-AGI-3 成绩是在特定 Responses API harness 下测得的；有评论者指出，如果对旧模型使用同一套 harness，其分数也会明显上升。外部追踪平台还显示 GPT-6 Astra 在 Artificial Analysis Coding Agent Index 上进步显著，该指数综合了 DeepSWE、Terminal-Bench v2.1 和 SWE-Atlas-QnA 等基准。

hackernews · kibae · 9月3日 18:41 · [社区讨论](https://news.ycombinator.com/item?id=49554643)

**背景**: ARC-AGI-3 是 ARC Prize 社区推出的交互式推理基准：智能体必须在没有明确指令的情况下探索陌生的抽象 2D 游戏类环境、推断目标并通过操作学习规则；此前的 ARC 版本主要衡量被动流体智能。此前大部分前沿模型在 ARC-AGI-3 上得分极低甚至接近 0%，而人类可以完成全部任务。此次发布还附带系统卡，社区将模型介绍与各项评测分开讨论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arcprize.org/arc-agi/3">ARC-AGI-3</a></li>
<li><a href="https://arxiv.org/abs/2603.24621">ARC-AGI-3: A New Challenge for Frontier Agentic Intelligence ARC Prize - Leaderboard ARC-AGI-3 Leaderboard - llm-stats.com ARC-AGI-3: The New Interactive Reasoning Benchmark How enabling two settings tripled our scores on the ARC-AGI-3 ...</a></li>
<li><a href="https://artificialanalysis.ai/agents/coding-agents">AI Coding Agent Benchmarks &amp; Leaderboard | Artificial Analysis</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论者对官方宣传的基准分数持怀疑态度：intenex 认为 ARC-AGI-3 记分牌具有误导性，因为 GPT-5.6 Sol 的较低分数是在不同 harness 下测得的；abixb 则指出，除 ARC-AGI-3 外，其余提升与常见的“点版本”更新差别不大。还有人质疑演示中让 AI 自动购物的场景，astrobiased 认为进展仍更像技能获取，而非 François Chollet 所定义的通用智能。

**标签**: `#OpenAI`, `#GPT-6`, `#AI research`, `#benchmarks`, `#large language models`

---

<a id="item-2"></a>
## [开发者用 Claude LLM 将 1993 年 Amiga 汇编游戏移植到 Godot](https://babyloniantwins.com/blog/porting-a-1993-amiga-game-to-godot/) ⭐️ 8.0/10

一名开发者在七月假期里仅用一个晚上，用 Claude 将自己 1993 年用 MC68000 汇编编写的 Amiga 游戏移植到了 Godot 引擎。该 LLM 先用 vasm 重新汇编代码，直到生成的二进制文件与原始版本逐字节一致，随后将其翻译成了可运行的 Godot 移植版。 这展示了一种新颖而强大的工作流程：利用 LLM 复活并现代化几十年前的汇编语言游戏，同时保留其玩法和历史代码。它预示着复古计算保存和移植项目可以变得极其迅速，并让原始开发者与爱好者都更容易参与其中。 最初发布的二进制文件并非汇编器的干净输出，而是 AsmOne 保存的、游戏运行后的内存快照，这导致初始存在约 108 字节的不匹配，LLM 必须对此予以处理。开发者又花了好几个周末和夜晚打磨移植版的手感，并现已免费发布原版游戏。

hackernews · rabahs · 9月3日 14:28 · [社区讨论](https://news.ycombinator.com/item?id=49550375)

**背景**: Amiga 是 20 世纪 80 至 90 年代的个人电脑，以定制图形和声音著称；为了速度，开发人员常用汇编语言直接“敲击硬件”（banging-the-hardware）进行编程。MC68000 汇编是 Amiga 所用 Motorola 68000 CPU 的原生指令集。vasm 是一款可移植、可重新定目标的汇编器，常用于汇编 68000 代码；AsmOne 则是开发者 1993 年使用的集成汇编/编辑器环境。Godot 是一款现代开源游戏引擎，因此这是一次从底层遗留汇编到高层现代引擎的翻译。

<details><summary>参考链接</summary>
<ul>
<li><a href="http://sun.hasenbraten.de/vasm/">vasm portable and retargetable assembler</a></li>
<li><a href="https://aminet.net/package/dev/asm/ASM-One">Aminet - dev/asm/ASM-One.lha Asm One 1.02 Manual : Rune Gram-Madsen : Free Download ... Commodore Software - ASM-One v1.02 Manual Asm-One v1.20 by The Flame Arrows :: pouët.net ASM-One Macro Assembler - HandWiki Amiga Assembler Tutorial - Carl Henrik Asm One 1.02 Manual : Free Download, Borrow, and Streaming ...</a></li>
<li><a href="https://plugins.jetbrains.com/plugin/17268-mc68000-assembly-language-support">MC68000 Assembly Language Support - IntelliJ IDEs Plugin | Marketplace</a></li>

</ul>
</details>

**社区讨论**: 评论者热情而怀旧：mattjoyce 报告了用 Claude 将 ZX81 游戏二进制转成 Go 的类似成功经历；btbuildem 将游戏的美学风格比作《Gods: Into the Wonderful》；dannyobrien 对 1993 年在没有互联网的环境下进行汇编开发表达敬佩；hedgehog 希望看到 Claude Code 生成的工程指南；glimshe 则打算用同样方式移植另一款被遗忘的游戏。总体而言，大家对 LLM 辅助的复古移植赞叹不已且感到兴奋。

**标签**: `#LLM`, `#Godot`, `#retrocomputing`, `#assembly`, `#code translation`

---

<a id="item-3"></a>
## [围棋大师申真谞让两子击败 AI KataGo](https://www.kedglobal.com/artificial-intelligence/newsView/ked202607210007) ⭐️ 8.0/10

围棋大师申真谞尽管让两子仍击败了人工智能 KataGo，凸显了人类战略创意相对于当前 AI 系统的优势。

hackernews · gmays · 9月3日 01:11 · [社区讨论](https://news.ycombinator.com/item?id=49544762)

**标签**: `#Go`, `#Artificial Intelligence`, `#KataGo`, `#Human vs AI`, `#Game Strategy`

---

<a id="item-4"></a>
## [Audacity 4.0 发布，改用 Qt6 界面，社区反应不一](https://github.com/audacity/audacity/releases/tag/Audacity-4.0.0) ⭐️ 8.0/10

Audacity 4.0 现已发布，这是广受欢迎的开源音频编辑器的一个重要新版本，带来了基于 Qt6 的全新界面和一系列修复。此次发布标志着该应用界面在 3.x 系列之后进行了重大重写。 Audacity 是最广泛使用的免费音频编辑器之一，因此这次向 Qt6 的界面重写会影响庞大的全球用户群，并使老化的代码库现代化。社区的热烈反应表明，后端行为、隐私和工作流兼容性对这个项目的未来至关重要。 官方发布页面重点介绍了基于 Qt6 的新界面和各类修复，但更新日志并未解决所有长期存在的抱怨。一些用户指出 JACK/PipeWire 后端集成仍然不够好用，另一些人则对 audio.com 等云端/遥测功能表示担忧。

hackernews · ClydeN · 9月3日 10:53 · [社区讨论](https://news.ycombinator.com/item?id=49548395)

**背景**: Audacity 是一款历史悠久的开源音频编辑器，广泛用于 Windows、macOS 和 Linux 上进行录音和声音编辑。Qt 是一个用于构建图形界面的跨平台应用开发框架；迁移到 Qt6 可带来更好的性能、现代图形和更强的硬件支持。音频后端指的是软件实际播放和采集声音所需的底层系统 API，例如 JACK、PipeWire、PulseAudio 或 WASAPI。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Qt_%28software%29">Qt (software) - Wikipedia</a></li>
<li><a href="https://extenly.com/2024/12/20/from-qtwidgets-to-qt6-and-beyond-what-is-qt-capable-of/">From QtWidgets to Qt6 and Beyond: What Is Qt Capable Of? – Extenly</a></li>
<li><a href="https://github.com/dechamps/FlexASIO/blob/master/BACKENDS.md">FlexASIO/BACKENDS.md at master · dechamps/FlexASIO</a></li>

</ul>
</details>

**社区讨论**: 社区讨论意见不一：一些用户热情推荐开发者访谈视频并称赞界面更干净，另一些人则说 Audacity 4 依然没有解决技术问题，例如 JACK 客户端不会持久存在、PipeWire 支持不够自然。关注隐私的评论者还询问 Tenacity 和 Sneedacity 等去遥测分叉项目的情况，反映出对 Audacity 云端和分析功能的持续不信任。

**标签**: `#audacity`, `#open-source`, `#release`, `#qt6`, `#audio-editing`

---

<a id="item-5"></a>
## [谷歌 Antigravity 条款引发担忧：第三方使用 AI 可能导致整个账号被封](https://twitter.com/GergelyOrosz/status/2095453567955968398) ⭐️ 8.0/10

谷歌 Antigravity 的服务条款中有些措辞暗示，如果将平台用于第三方 AI 用途，用户可能会失去整个 Google 账号，而不仅仅是 Antigravity 服务本身。Antigravity 团队成员 Varun Mohan 在 X 上回应称，该措辞容易引起误解，将进行修改以明确其仅指向 Antigravity 账号。 这之所以重要，是因为许多人的 Google 账号承载着邮件、日历、政府服务等关键功能，一旦被封禁可能带来不成比例的严重后果。该争议也反映了用户对平台依赖、不友好的账号政策以及大型科技公司如何安全整合 AI 产品的更广泛担忧。 此讨论起源于 Gergely Orosz 的一条推文，社区用户指出封禁风险尤其严重，因为用户可能无法访问关键服务，还得与自动化客服系统纠缠。Varun Mohan 在 X 上的回复表明，官方立场是该条款指的是 Antigravity 账号，团队计划修改服务条款措辞以避免歧义。

hackernews · tosh · 9月3日 11:01 · [社区讨论](https://news.ycombinator.com/item?id=49548452)

**背景**: 谷歌 Antigravity 是谷歌推出的软件开发平台，包含以聊天为核心的开发环境、集成开发环境（IDE）、命令行界面（CLI）和软件开发工具包（SDK），用于编排自主 AI 智能体完成代码生成、执行和测试等任务。该争议源于这个新 AI 产品与庞大 Google 身份体系的绑定——理论上，违反某一产品的条款可能导致无关服务被停用。这也反映了行业内关于 AI 产品如何与现有平台账号体系互动、以及如何制定清晰且比例适当的执行政策的广泛讨论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Google_Antigravity">Google Antigravity</a></li>
<li><a href="https://antigravity.google/">Google Antigravity</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍表示强烈不满，称封禁整个账号的做法“极度不友好”，并提到用户难以联系到人工客服，可能失去多年的邮件和日历数据。还有人将其与欧洲要求使用苹果/谷歌账号的 eID 系统相类比，认为平台封禁可能导致用户无法访问政府服务。部分用户注意到 Antigravity 团队的澄清，但也指出初始措辞的模糊性本身已经损害了人们对谷歌 AI 产品的信任。

**标签**: `#Google`, `#Antigravity`, `#Terms of Service`, `#AI policy`, `#Account suspension`

---

<a id="item-6"></a>
## [美国政府支持 OpenAI：AI 训练属合理使用](https://www.reuters.com/legal/litigation/us-government-backs-openai-new-york-times-copyright-case-2026-09-02/) ⭐️ 8.0/10

美国政府向曼哈顿联邦法院提交一份法庭之友意见书，在《纽约时报》诉 OpenAI 的版权纠纷中支持 OpenAI，主张使用受版权保护的内容训练大语言模型通常属于合理使用。这是美国政府首次公开在此类 AI 训练版权案件中表明立场。 该意见书虽不具法律约束力，但可能增强 AI 企业在版权诉讼中的应诉底气，并影响法院与监管机构对 AI 训练行为的态度。此案已成为“未经许可使用受版权作品训练 AI 是否违法”的标志性争议，牵动 AI 开发者和内容创作者的切身利益。 《纽约时报》于 2023 年起诉 OpenAI 及微软，指控其未获许可使用该报数百万篇文章来训练 ChatGPT。《纽约时报》批评美国政府站在“万亿美元级 AI 公司”一边，以牺牲创作者权益为代价。

telegram · zaihuapd · 9月3日 05:45

**背景**: “合理使用”是美国法律中的一项原则，允许在批评、评论、新闻报道、教学或研究等情形下，未经许可有限度地使用受版权保护的作品。“法庭之友”意见书由非案件当事方提交，目的是为法院提供额外的法律视角；它虽不具约束力，但仍可能被法院参考。这起诉讼是对“大规模抓取受版权内容来构建生成式 AI 是否构成侵权”的一次重要检验，对 AI 产业的未来发展具有广泛影响。

**标签**: `#AI`, `#Copyright`, `#Legal`, `#OpenAI`, `#Fair Use`

---