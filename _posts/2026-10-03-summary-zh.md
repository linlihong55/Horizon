---
layout: default
title: "Horizon Summary: 2026-10-03 (ZH)"
date: 2026-10-03
lang: zh
---

> 从 31 条内容中筛选出 4 条重要资讯。

---

1. [新型 AI 以远低训练成本击败人类顶尖 Stratego 玩家](#item-1) ⭐️ 8.0/10
2. [Greg Kroah-Hartman 批评 LLM 时代的漏洞报告与 AI 营销](#item-2) ⭐️ 8.0/10
3. [Zig v0.17.0 发布说明出炉，对 LLM 态度转向务实](#item-3) ⭐️ 8.0/10
4. [arXiv 自 10 月 1 日起每人每月限投 2 篇论文](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [新型 AI 以远低训练成本击败人类顶尖 Stratego 玩家](https://arstechnica.com/science/2026/10/ai-finally-beat-the-best-stratego-player-in-history-and-did-it-on-a-budget/) ⭐️ 8.0/10

一篇发表于 Nature 的论文（并配有 arXiv 预印本）介绍了一个新的 AI 系统，它首次击败了人类历史上最强的 Stratego（斯特拉特戈）棋手，而且训练成本相对低廉。据报道，该算法的学习效率约为 DeepMind 的 DeepNash 的 34 倍，对局数量少得多，最终棋力却强得多。 Stratego 一直是 AI 的经典难题，因为它属于非完全信息博弈：玩家看不到对方棋子的具体身份，因此征服了国际象棋和围棋的暴力前瞻搜索方法在这里失效。一种能够低成本高效学习此类博弈的方法，为隐藏信息下的决策提供了更实用的路径，而这类问题比完全信息棋类更接近谈判、安全博弈和战略规划等现实场景。 报道中的效率提升约为 DeepNash 所需对局数的 1/34；DeepNash 是 DeepMind 在 2022 年论文《Mastering the Game of Stratego with Model-Free Multiagent Reinforcement Learning》中提出的方法。因此这项工作也重新审视了当年那个“已掌握”的宣称：2022 年的系统似乎尚未明显超越人类顶尖水平，而新方法据说做到了。

hackernews · PaulHoule · 10月2日 14:11 · [社区讨论](https://news.ycombinator.com/item?id=49933740)

**背景**: 在博弈论中，当所有玩家都能看到全部相关状态时，该游戏被称为“完全信息”博弈，例如国际象棋和围棋。Stratego 则属于非完全信息博弈：双方各 40 枚棋子从对手视角看外观完全相同，军衔是隐藏的，只有交战结果才会逐步揭示信息。这种隐藏状态意味着玩家无法直接进行前瞻搜索，因为一步棋的好坏取决于自己无法观测的事实，这正是该问题长期难以被 AI 攻克的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.deeplearning.ai/the-batch/deepnash-the-rl-system-that-plays-stratego-like-a-master">DeepNash, the RL System That Plays Stratego like a Master</a></li>
<li><a href="https://en.wikipedia.org/wiki/Perfect_information">Perfect information - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认同隐藏信息是关键所在：有人指出，你当然想用“我这样走、他就会那样走”的方式做前瞻搜索，但当你连对手的棋子是什么都不知道时，这就根本不可能，因此 34 倍的学习效率才是核心贡献。也有人回忆童年玩实体桌游的经历，并提及 2022 年的 DeepNash 论文，认为当年“已掌握”的说法现在看来还差得远；还有人开玩笑地谈到在棋子背面做记号作弊，或者直接让聊天机器人去推翻某个难题。

**标签**: `#AI`, `#reinforcement-learning`, `#imperfect-information-games`, `#game-playing`, `#research`

---

<a id="item-2"></a>
## [Greg Kroah-Hartman 批评 LLM 时代的漏洞报告与 AI 营销](https://www.youtube.com/watch?v=NnV_cWeoo5Q) ⭐️ 8.0/10

在 Kernel Recipes 2026 一场题为《Security in the LLM Age》的演讲中，Linux 内核维护者 Greg Kroah-Hartman 详细拆解了 Anthropic 关于其 Mythos 模型“发现”79 个内核漏洞的说法：其中 24 个除了“某个东西崩溃了”之外没有任何细节，14 个根本不是漏洞，3 个基于编造的数据，15 个已在最新版本中修复。真正需要修复的只有约 20 个，他形容这些工作量大致相当于一小时的内核开发。 这是一线开源维护者对 AI 厂商安全营销最直接的公开反驳之一，其意义在于：下游发行版、安全团队和维护者如今越来越需要处理 AI 生成的漏洞报告。它也引发了更广泛的质疑——那些耸动的“AI 发现零日漏洞”说法是否已经跑在了证据前面，以及开源安全工作中的署名与引用规范问题。 根据演讲内容（由参会者转述），Mythos 本质上是对过去几十年的内核补丁做模式匹配，再把这些模式套用到别处，看看同类修复是否已普遍应用；而在真正需要修复的问题中，有几个只是“假设存在恶意文件系统镜像”或需要本地注入权限。Kroah-Hartman 还指出，Anthropic 并未引用最初编写这些补丁的内核开发者；而网络上关于 Mythos 的报道则聚焦于另外一些说法，例如它以约 2 万美元的 token 成本自主发现了一个存在 27 年之久的 OpenBSD 漏洞。

hackernews · usernomdeguerre · 10月2日 02:51 · [社区讨论](https://news.ycombinator.com/item?id=49929391)

**背景**: Greg Kroah-Hartman 长期担任 Linux 内核 stable 分支的维护者，是内核开发领域资历最深的人物之一，因此他对漏洞报告的评估分量很重。“Kernel Recipes”是法国的技术会议，内核开发者会在此讨论底层工作。基于 LLM 的漏洞发现，是指通过提示或微调大语言模型来扫描源代码并提出 CVE（Common Vulnerabilities and Exposures，公开披露安全缺陷的标准编号）的新兴做法。此事还牵涉开源界长期以来的“多双眼睛让漏洞无处遁形”论调，而 AI 厂商如今正用这一论调来主张模型可以胜过人类审查者。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://venturebeat.com/security/mythos-detection-ceiling-security-teams-new-playbook">Anthropic&#x27;s Mythos finds 27-year-old bug | VentureBeat</a></li>
<li><a href="https://www.bymachine.news/anthropic-mythos-vulnerability-discovery-security-crisis">Mythos Found 27-Year-Old Bug Humans Missed Completely</a></li>
<li><a href="https://undercodetesting.com/mythos-ai-just-found-a-27-year-old-bsd-bug-why-human-researchers-kept-it-secret-for-decades-video/">Mythos AI Just Found a 27-Year-Old BSD Bug: Why Human ...</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者普遍赞赏 Kroah-Hartman 直言不讳，有人引用了他幻灯片中的分类数据，并指出整个“79 个漏洞”的营销宣传最终只相当于一小时的内核工作，认为这与 AI 安全宣传之间的落差“极其刺眼”。也有人强调，Anthropic 没有给最初修复这些 CVE 的内核开发者署名，这与 OpenAI 曾遇到的引用问题是同一类毛病。还有一种更前瞻的观点认为，这些批评并不意味着 AI 在此毫无用处——针对内核特性、代码规范和威胁模型训练的专业模型，仍有可能让漏洞发现与修复变得更快、更准。

**标签**: `#LLM security`, `#Linux kernel`, `#AI vulnerability research`, `#open source`, `#Anthropic`

---

<a id="item-3"></a>
## [Zig v0.17.0 发布说明出炉，对 LLM 态度转向务实](https://ziglang.org/download/0.17.0/release-notes.html) ⭐️ 8.0/10

Zig 项目发布了 0.17.0 版本的完整发布说明，这份内容详实的文档在 Hacker News 上获得 209 个赞和 132 条评论。发布说明及相关讨论显示，Zig 对使用 LLM 发现编译器与语言缺陷采取了新的务实态度——据称灵感来自 SQLite 的相关成果——同时继续扩展其目标平台与交叉编译支持。 Zig 是近年崛起最快的系统编程语言之一，每一次版本更新都会影响底层开发者对「取代 C」这件事的判断。此次开始接受 LLM 辅助的缺陷挖掘尤其值得关注，因为该项目此前对 AI 生成内容持强硬立场；这一政策转向可能影响其他开源语言项目对待 AI 工具的方式。 Zig 仍处于 1.0 之前阶段，因此 0.17.0 依旧是一个会带来破坏性变更、生态相对较小的移动目标，尽管其设计与工具链在不断成熟。社区成员特别点名了最期待的两项后续特性：新的无栈协程 IO 实现，以及一等公民级别的模糊测试工具。

hackernews · ErenayDev · 10月2日 20:56 · [社区讨论](https://news.ycombinator.com/item?id=49938521)

**背景**: Zig 是一门通用系统编程语言及其工具链，定位为对 C 语言的通用性改进，由 Andrew Kelley 创建并于 2016 年首次公布。它不使用宏和预处理器指令，采用手动内存管理，并引入编译期泛型与类型反射，还提供紧凑结构体、任意位宽整数和多种指针类型等底层特性。项目由 Zig 软件基金会通过企业赞助和个人捐赠提供资金，并以 MIT 许可证开源发布。由于尚未发布 1.0，维护者会在每个打标签的版本发布冗长而详尽的说明文档，以记录行为和工具链层面的变化。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Zig_%28programming_language%29">Zig (programming language)</a></li>
<li><a href="https://ziglang.org/">Home Zig Programming Language</a></li>

</ul>
</details>

**社区讨论**: 整体情绪偏正面：一位写过多门语言的老手称 Zig 是自己用过设计最好的语言，另一位则盛赞其目标平台支持，认为可能是唯一能在这一点上与 C 竞争的语言。评论者普遍欢迎 Zig 对 LLM 转向务实，但也提出了尖锐的反面观点——有用户表示自己因为核心团队成员不仅对 LLM、也对人态度敌意而离开 Zig 生态转向 Odin，还有人追问在早前对 AI 的强硬立场之后，项目整体进展如何。

**标签**: `#zig`, `#programming-languages`, `#systems-programming`, `#compilers`, `#release-notes`

---

<a id="item-4"></a>
## [arXiv 自 10 月 1 日起每人每月限投 2 篇论文](https://www.huxiu.com/article/4895127.html) ⭐️ 8.0/10

全球最大的预印本平台 arXiv 宣布，自 10 月 1 日起每位提交者每个自然月最多只能提交 2 篇论文，覆盖计算机、数学、物理等全部学科，且被拒稿件同样占用当月额度。这一新规出台的背景是 9 月投稿量达到 40363 篇、创下 35 年来新高，其中 AI 分类论文两年内增长超过 6 倍。 由于 arXiv 已成为科研成果首发的事实标准平台，这一政策直接限制了全球科研界——尤其是 AI 与机器学习领域——发布和传播新工作的速度。它也释放出一个强烈信号：面对大量低质量、AI 生成稿件的冲击，主流学术基础设施被迫通过限量提交来保护人工审核能力。 该上限按实际提交者而非按论文计算，因此多作者论文的其他合著者不受影响，仍可在同月提交自己的论文。所有学科均不豁免，而且由于被拒稿件同样占用额度，作者无法在同一月份内反复重投。

telegram · zaihuapd · 10月2日 06:21

**背景**: 预印本是指尚未经过正式同行评审和期刊发表、就先行公开的学术论文版本，它让研究者能够尽早分享成果并确立优先权。arXiv 创立于 35 年前，目前由康奈尔大学运营，是物理学、数学和计算机科学领域最主要的预印本平台。与期刊不同，arXiv 只做轻量级的形式筛查，而非完整的同行评审，而这项筛查由数量有限的人工审核员承担。生成式 AI 的普及，加上出售低质量或伪造稿件的商业化“论文工厂”，使这种依赖志愿者的审核机制越来越难以跟上投稿增长的速度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Preprint">Preprint - Wikipedia</a></li>
<li><a href="https://casrai.org/guides/preprint-servers-explained">Preprint Servers Explained: What &amp; How — CASRAI</a></li>
<li><a href="https://journals.plos.org/plosbiology/article/file?id=10.1371/journal.pbio.3002931&amp;type=printable">A call for research to address the threat of paper mills</a></li>

</ul>
</details>

**标签**: `#arXiv`, `#academic-publishing`, `#AI-research`, `#preprints`, `#research-policy`

---