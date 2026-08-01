---
layout: default
title: "Horizon Summary: 2026-08-01 (ZH)"
date: 2026-08-01
lang: zh
---

> 从 36 条内容中筛选出 7 条重要资讯。

---

1. [DeepSeek V4 Flash 0731 发布：前沿级 AI 性能，超低价格](#item-1) ⭐️ 9.0/10
2. [华为开源 505B 参数 MoE 大模型 openPangu-2.0-Pro](#item-2) ⭐️ 9.0/10
3. [电梯调度算法：基于模拟的分析](#item-3) ⭐️ 8.0/10
4. [YC 支持的 qm 发布多人智能体协作框架，面向工作场景](#item-4) ⭐️ 8.0/10
5. [无状态 MCP 2.0 重燃兴趣，催生 mcp-explorer 与 datasette-mcp](#item-5) ⭐️ 8.0/10
6. [西蒙·威利森做客 Oxide and Friends：畅谈开放权重 AI 革命](#item-6) ⭐️ 8.0/10
7. [德国法院裁定 AI 音乐公司 Suno 侵犯版权](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [DeepSeek V4 Flash 0731 发布：前沿级 AI 性能，超低价格](https://artificialanalysis.ai/models/deepseek-v4-flash) ⭐️ 9.0/10

DeepSeek 正式发布 V4 Flash 0731，作为 V4 Flash 预览版的正式后续版本，在 Artificial Analysis 智能指数上拿下 50 分，比上一版本高出 10 分。Agent 性能同样大幅跃升，GDPval-AA v2 的 Elo 评分从 1189 涨到 1559。 该发布表明，一个面向效率优化、成本极低的模型如今也能跻身 AI 智能前沿，挑战更大规模专有系统的经济性。API 定价仅为每百万输入 token 0.14 美元、每百万输出 token 0.28 美元，DeepSeek 让更广泛的开发者和应用场景都用得起先进的智能体 AI。 V4 Flash 0731 是一个稀疏混合专家（MoE）模型，总参数 284B，每次推理激活 13B 参数，支持 100 万 token 上下文窗口。它沿用预览版的架构，只对后训练环节做了调整，并原生支持 Responses API 格式，还针对 OpenAI 的 Codex 做了专门适配。

hackernews · theanonymousone · 7月31日 07:59 · [社区讨论](https://news.ycombinator.com/item?id=49120299)

**背景**: DeepSeek 是一家开源模型权重的中国 AI 实验室，其 V4 系列采用混合专家（MoE）架构，每个 token 只激活少量参数，在保持高能力的同时显著降低推理成本。Artificial Analysis 智能指数综合公开与非公开评测结果来给模型排名，V4 Flash 0731 拿到 50 分，意味着它与许多运行成本高得多的系统一样，处于行业前沿。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://artificialanalysis.ai/articles/deepseek-v4-flash-0731-scores-50-on-the-artificial-analysis-intelligence-index-10-points-above-previous-deepseek-v4-flash">DeepSeek V4 Flash 0731 scores 50 on the Artificial Analysis Intelligence Index, 10 points above previous DeepSeek V4 Flash</a></li>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4-flash-0731">DeepSeek V4 Flash 0731 - API Pricing &amp; Benchmarks | OpenRouter</a></li>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash-0731">deepseek-ai/DeepSeek-V4-Flash-0731 · Hugging Face</a></li>

</ul>
</details>

**社区讨论**: 评论普遍热情高涨，称赞该模型以极低价格提供前沿级智能，并适合作为日常编码开发的主力模型。也有用户猜测即将推出的 V4 Pro 是否会超越它，还有人讨论大规模开源模型托管的可持续性，以及与其他前沿模型的价格比较。

**标签**: `#AI`, `#DeepSeek`, `#LLM`, `#model release`, `#cost analysis`

---

<a id="item-2"></a>
## [华为开源 505B 参数 MoE 大模型 openPangu-2.0-Pro](https://huggingface.co/openpangu/openPangu-2.0-Pro) ⭐️ 9.0/10

华为在 Hugging Face 上开源了 openPangu-2.0-Pro，这是一个混合专家（MoE）大语言模型，总参数约 505B，每 token 激活约 18B，支持 512k 上下文长度。其 Thinking 版本在 AIME 2026 数学测评中得分 95.4，在 GPQA-Diamond 上得分 87.9。 这是华为发布的最大开源 MoE 模型之一，基于昇腾 NPU 训练，展示了非 NVIDIA AI 技术栈的可行性。该发布有望增强开放权重大模型生态，并为研究人员提供一个先进的长上下文推理模型。 该模型采用了 MLA（多头潜在注意力）、DSA+SWA 独立分层混合注意力设计，以及用于自投机解码的 3 头 MTP（多 token 预测）模块。训练数据约为 34T tokens，后训练阶段完成了快慢合一微调与多专项强化学习。

telegram · zaihuapd · 7月31日 06:50

**背景**: openPangu-2.0-Pro 是一个混合专家（MoE）模型，将大量参数拆分为多个专家，每个 token 只激活部分专家，从而在效果和推理成本之间取得平衡。MLA 通过压缩 KV 缓存来降低显存开销；DSA+SWA 混合注意力将滑窗注意力与基于内容的稀疏注意力结合，以高效支持长上下文。MTP 通过同时预测多个未来 token 来加速解码。昇腾 NPU 是华为的 AI 加速芯片，因此这次开源也体现了 AI 硬件的多样性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://sebastianraschka.com/llms-from-scratch/ch04/05_mla/">MLA Chapter 4 Guide | Sebastian Raschka, PhD</a></li>
<li><a href="https://sebastianraschka.com/llm-architecture-gallery/mtp/">Multi-Token Prediction (MTP) | Sebastian Raschka, PhD</a></li>
<li><a href="https://www.pythonalchemist.com/llm-architectures/attention-variants">Attention Variants Explained: MHA, GQA, MQA, MLA, SWA , DSA</a></li>

</ul>
</details>

**标签**: `#LLM`, `#MoE`, `#Huawei`, `#Open Source`, `#AI`

---

<a id="item-3"></a>
## [电梯调度算法：基于模拟的分析](https://john.fun/elevators) ⭐️ 8.0/10

文章《Elevators》通过模拟分析比较了 FCFS、SCAN、LOOK 等电梯调度算法在不同条件下的表现，重点说明了每种算法在效率与公平性之间的权衡。 电梯调度是直接影响楼宇用户体验的经典现实优化问题。该分析将电梯算法与磁盘调度概念联系起来，展示了思想如何在领域间迁移，并引发了关于真实世界行为的丰富社区讨论。 模拟比较了 FCFS、SSTF、SCAN 和 LOOK 等多种算法，它们在响应时间和公平性上各有取舍。社区成员指出，真实世界中的出行模式（如办公楼中的目的地派梯系统）会使某些算法的表现不同于随机模拟的结果。

hackernews · Jrh0203 · 7月31日 15:17 · [社区讨论](https://news.ycombinator.com/item?id=49124218)

**背景**: 电梯算法，也称 SCAN，是一种磁盘调度算法，用于决定磁盘臂在服务读写请求时的运动方式。在电梯调度中，轿厢沿一个方向移动直到前方没有更多请求，然后反向运行，这类似于磁盘头在磁道上的扫描。LOOK 是 SCAN 的一种变体，只运行到每个方向最远的请求点，避免不必要的行程。这些算法在计算机科学课程中广泛教授，也被用于 Elevator Saga 等模拟游戏中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Elevator_algorithm">Elevator algorithm - Wikipedia</a></li>
<li><a href="https://dev.to/thesaltree/elevator-scheduling-algorithms-fcfs-sstf-scan-and-look-2pae">Elevator Scheduling Algorithms: FCFS, SSTF, SCAN, and LOOK - DEV Community</a></li>
<li><a href="https://www.geeksforgeeks.org/dsa/scan-elevator-disk-scheduling-algorithms/">SCAN (Elevator) Disk Scheduling Algorithms - GeeksforGeeks</a></li>

</ul>
</details>

**社区讨论**: 评论者将电梯调度与磁盘调度联系起来，指出 HDD 就像“一部很长的电梯”，而 SCAN 本身就是磁盘调度算法。还有人分享了实际经验：真实建筑中的目的地派梯常呈现偏斜的出行模式（例如大家都去一楼），这可能使其表现比随机模拟更差；开发电梯游戏 Sky Lobby 的开发者则表示他们选择了 LOOK，因为它更符合玩家预期。

**标签**: `#algorithms`, `#simulation`, `#elevators`, `#systems`, `#scheduling`

---

<a id="item-4"></a>
## [YC 支持的 qm 发布多人智能体协作框架，面向工作场景](https://github.com/yc-software/qm) ⭐️ 8.0/10

qm 是一个由 YC 支持的多人智能体协作框架（agent harness），现已发布并托管在 GitHub（github.com/yc-software/qm）上。它通过按人划分的权限范围（per-person scopes）和共享房间（shared rooms）来协调公司级的 AI 助手，延续了 OpenCode、Codex 和 Claude Code 等本地编码智能体的模式。 qm 直面多人智能体领域最棘手的「作用域」（scoping）问题：以按人作用域搭配共享房间的方式实现公司级协调。作为 YC 支持的项目，它在快速演进的 LLM 智能体生态中具有指标意义，标志着行业正从单一智能体循环走向跨团队调度 AI 助手的新阶段。 在 qm 中，智能体会以所服务人员的身份行动，使用该人员的凭据与权限，且所有操作都会被审计。组织只需设定一个整体安全基线，更窄的个人作用域只能在此基础上进一步收紧。

hackernews · tosh · 7月31日 18:04 · [社区讨论](https://news.ycombinator.com/item?id=49126604)

**背景**: 智能体框架（agent harness）是包裹 LLM 的完整软件基础设施，涵盖编排循环、工具与记忆；该术语在 2026 年初被正式定义，但相关概念早已存在。在 harness 工程实践中，开发者把这些脚手架当作真正的工件来维护，每当智能体出错就着手加固。在多人协作方面，Agent Room 等工具允许不同机器上的 AI 编码智能体在持久化共享房间中协作，通常基于模型上下文协议（MCP）。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/yc-software/qm">GitHub - yc-software/ qm : Multiplayer agent harness for work · GitHub</a></li>
<li><a href="https://habr.com/ru/articles/1023316/">Что такое Harness ? Полный разбор на примере Claude... / Хабр</a></li>
<li><a href="https://www.agent-room.com/">Agent Room — Multi-agent collaboration for Claude Code, Codex, Cursor &amp; Gemini</a></li>

</ul>
</details>

**社区讨论**: 评论者总体上欢迎这一方向：一位从业者称赞「按人作用域加共享房间」是公司级助手的合理答案，并认为 YC 推出该项目「令人鼓舞，也有点超现实」。一则幽默轶事提到，智能体会自己与其他智能体安排会议，让人感觉像中层管理者；另有评论者要求做「QM vs Cowork」的对比，质疑其相比 Claude Cowork 有何优势。还有人感慨 LLM 时代的新应用难以理解，并关联到 Garry Tan 的 gstack 等相关工具。

**标签**: `#AI agents`, `#multiplayer`, `#LLM tools`, `#YC`, `#developer tools`

---

<a id="item-5"></a>
## [无状态 MCP 2.0 重燃兴趣，催生 mcp-explorer 与 datasette-mcp](https://simonwillison.net/2026/Jul/31/stateless-mcp/#atom-everything) ⭐️ 8.0/10

MCP 2.0（即 2026-07-28 版 Model Context Protocol 规范）引入了无状态 MCP，取消了会话 ID 的需求。Simon Willison 本周构建了三个新工具，包括 mcp-explorer 和 datasette-mcp。 这是 MCP 自发布以来最重大的变化，大幅简化了客户端和服务端的实现，并让远程服务器能够水平扩展。这可能会重新点燃 AI 智能体开发者对 MCP 的采用，尤其是对于较小模型和可审计的工作流程。 无状态 MCP 使用单个 HTTP 请求，携带 MCP-Protocol-Version 和 Mcp-Method 头，替代了原来需要 Mcp-Session-Id 的两次往返。mcp-explorer 是一个用于交互式探查 MCP 服务器的 CLI 工具，而 datasette-mcp 则提供对 Datasette 实例的只读访问。

rss · Simon Willison · 7月31日 23:13

**背景**: MCP（Model Context Protocol）是 Anthropic 于 2024 年 11 月推出的开放标准，旨在标准化 LLM 驱动的智能体连接外部工具和数据的方式。早期的有状态 MCP 需要通过两步初始化来创建会话，这使得扩展变得复杂。新的无状态设计在每个请求中携带所有所需上下文，使构建和部署服务器更加容易。这一转变发生在 MCP 在 2025 年因 Claude Skills 等方法的竞争而热度有所下降之后。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol - Wikipedia</a></li>
<li><a href="https://stackpicks.dev/blog/mcp-2-0-explained-2026">MCP 2 . 0 Explained — Stateless Core, OAuth Login... — StackPicks</a></li>
<li><a href="https://www.anthropic.com/news/model-context-protocol">Introducing the Model Context Protocol \ Anthropic</a></li>

</ul>
</details>

**标签**: `#MCP`, `#AI agents`, `#Model Context Protocol`, `#software engineering`, `#developer tools`

---

<a id="item-6"></a>
## [西蒙·威利森做客 Oxide and Friends：畅谈开放权重 AI 革命](https://simonwillison.net/2026/Jul/31/oxide-and-friends/#atom-everything) ⭐️ 8.0/10

西蒙·威利森于 2026 年 7 月 31 日做客 Oxide and Friends 播客，讨论开放权重 AI 模型革命，内容包括 Kimi K3 与专有前沿模型看齐、最近的 AI 安全事件，以及关于开放权重的业界公开信。他还提到，就在录制后没几天，DeepSeek V4 Flash 发布、Anthropic 自身也发生网络安全事件，让这期节目迅速“过时”。 这场专家对话凸显了 AI 行业的一个关键时刻：以 Kimi K3 为代表的开放权重模型已能与专有模型正面竞争，动摇了“前沿 AI 必须闭源”的固有观念。业界公开信以及 Anthropic 的“缺席签名”也反映出围绕开放、安全与美国 AI 领导地位的争论日益激烈。 Kimi K3 是一个 2.8 万亿参数的开源模型，基于 Kimi Delta Attention 和 Attention Residuals 构建，具备原生视觉能力、100 万 token 上下文窗口，并以修改版 MIT 许可证发布。节目中还聊到了 Golden Gate Claude、Zizians 事件、苏联马尔堡病毒研究和铅犯罪假说等话题；威利森还新增了一个预测：教宗会在今年年底前就开放模型发表言论。

rss · Simon Willison · 7月31日 21:33

**背景**: 开放权重模型是指核心组件（包括训练后的参数即“权重”）被公开发布的 AI 模型，任何人都可以下载并运行。月之暗面推出的 Kimi K3 是此类模型的最新旗舰之一，而 DeepSeek 也在 2026 年 7 月 31 日发布了 DeepSeek V4 Flash。这种密集发布加剧了业界对开放权重模型能否在安全情况下比肩甚至超越闭源专有系统的讨论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.kimi.com/blog/kimi-k3">Kimi K 3 Tech Blog: Open Frontier Intelligence</a></li>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash">deepseek -ai/ DeepSeek - V 4 - Flash · Hugging Face</a></li>

</ul>
</details>

**标签**: `#open-weight models`, `#AI`, `#podcast`, `#Simon Willison`, `#Kimi K3`

---

<a id="item-7"></a>
## [德国法院裁定 AI 音乐公司 Suno 侵犯版权](https://www.dw.com/en/german-court-rules-that-ai-music-firm-suno-violated-copyrights/a-78152227) ⭐️ 8.0/10

慕尼黑地区法院裁定 AI 音乐公司 Suno 侵犯版权，因其使用受版权保护的音乐训练模型，须披露非法所得并支付数额待定的赔偿。Suno 表示不认同判决，将评估包括上诉在内的所有选项。 这是全球首批检验版权法如何适用于 AI 音乐训练的重大案件之一，判决可能为 AI 行业树立全球性先例。它加强了 GEMA 等权利方推动平等许可谈判的地位，并可能促使 AI 公司更透明地披露训练数据。 该诉讼由 GEMA 于 2025 年 1 月提起，代表超过 9.5 万名德国音乐人及全球逾 200 万权利持有人；GEMA 在庭审中演示了用 Suno 生成的歌曲与原作高度相似。GEMA 表示其目标是推动平等的许可谈判。

telegram · zaihuapd · 7月31日 13:11

**背景**: Suno 是一个生成式 AI 音乐创作平台，用户只需输入文字描述即可生成包含人声和乐器的完整歌曲。GEMA 是德国音乐版权集体管理组织，管理逾 9 万名会员及全球超 200 万权利持有人的权利。本案的核心问题是：未经许可使用受版权保护的作品训练 AI 模型是否构成侵权。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Suno_%28platform%29">Suno (platform) - Wikipedia</a></li>
<li><a href="https://www.gema.de/en/w/help/gema/organisation/questions-and-answers/what-is-gema">What is GEMA and what is its purpose?</a></li>

</ul>
</details>

**标签**: `#AI`, `#copyright`, `#legal`, `#music`, `#Suno`

---