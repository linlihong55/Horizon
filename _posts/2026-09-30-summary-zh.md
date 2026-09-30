---
layout: default
title: "Horizon Summary: 2026-09-30 (ZH)"
date: 2026-09-30
lang: zh
---

> 从 41 条内容中筛选出 4 条重要资讯。

---

1. [OpenAI 发布 GPT-6.1 Sol：接近 Astra 的智能，价格仅为其五分之一](#item-1) ⭐️ 9.0/10
2. [OpenAI 开发者大会 2026：常驻智能体 Dots 及 20 余项更新](#item-2) ⭐️ 9.0/10
3. [隐私分析发现网页与移动端 AI 对话代理存在数据泄露](#item-3) ⭐️ 8.0/10
4. [OpenAI 发布 Dots：常驻云端的 AI 智能体](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI 发布 GPT-6.1 Sol：接近 Astra 的智能，价格仅为其五分之一](https://openai.com/index/introducing-gpt-6-1-sol/) ⭐️ 9.0/10

OpenAI 发布了 GPT-6 Sol 的升级版本 GPT-6.1 Sol，声称其在智能体编程、计算机操作和专业任务上接近 GPT-6 Astra 的水平，而输入输出价格仅为 Astra 标准价的五分之一，缓存输入价格更是低至每百万 token 0.10 美元。该模型已向 ChatGPT 的 Plus、Pro、Business、Enterprise 和 Edu 用户推出。 此次发布把接近前沿的能力下放到更便宜的价位，说明 token 价格而非单纯的基准分数正在成为前沿实验室之间竞争的主战场。这会在成本层面对 Anthropic 等竞争对手形成压力，并可能加速高端推理模型在重度智能体与编程工作负载上的商品化。 OpenAI 表示，在衡量智能体能否正确完成多步骤业务流程的 AutomationBench 上，GPT-6.1 Sol 在中等推理强度下比 Opus 5.5 高出 2.2 个百分点，而成本约为后者的三分之一。其缓存输入价格比标准输入价格低 95%，也比 GPT-6 Sol 的缓存输入价格低 50%。

hackernews · crorella · 9月29日 17:06 · [社区讨论](https://news.ycombinator.com/item?id=49896586)

**背景**: GPT-6 Astra 是 OpenAI 的顶级前沿模型，于 2026 年 9 月发布，公司总裁 Greg Brockman 称其为“代际跃升”，甚至可能被视为通用人工智能（AGI）的到来。在这一产品序列中，Sol 系列定位为更便宜的档位，主打复杂编程与智能体工作流，而不是追求最高的通用能力。缓存输入价格是指模型复用此前已处理过的提示词前缀时享受的折扣，这在反复发送大量基本不变上下文的编程智能体中非常常见。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/introducing-gpt-6-1-sol/">Introducing GPT-6.1 Sol | OpenAI</a></li>
<li><a href="https://developers.openai.com/api/docs/models/gpt-6.1-sol">GPT-6.1 Sol Model | OpenAI API</a></li>
<li><a href="https://www.axios.com/2026/09/03/openai-astra-gpt-6-agi-brockman">OpenAI releases new model GPT-6 Astra, says it may represent AGI</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论整体偏怀疑：多人称 GPT-6 Sol 相比 Sol 5.6 出现明显退步，一位长期支持 OpenAI/Codex 的用户表示已完全转用 Opus 5.5，也有人猜测 GPT-6.1 Sol 其实是几天前泄露的“Astra-Minor”模型的临时紧急改名。有评论认为真正的重磅是缓存价格便宜了 50%，另有评论担心价格成为主战场对整个行业和投资者而言是凶兆，还有人表示 DeepSeek 又便宜又快，从性价比出发落后前沿半年也可以接受。

**标签**: `#AI`, `#OpenAI`, `#LLM`, `#model-release`, `#pricing`

---

<a id="item-2"></a>
## [OpenAI 开发者大会 2026：常驻智能体 Dots 及 20 余项更新](https://openai.com/zh-Hant/index/devday-2026-recap/) ⭐️ 9.0/10

在 2026 年开发者大会上，OpenAI 发布了 20 余项更新，其中最重要的是常驻智能体 Dots——一款可全天候自主运转的伴生 Agent，能深入学习用户习惯并主动接管长线复杂工作。其他发布包括：专精编程与电脑操控的 GPT-6.1 Sol，以约五分之一的价格获得接近 Astra 的智能水平；速度最高提升 8 倍的 Astra Ultrafast（API 提升 6 倍）；登陆云端并支持语音操控与自动修障的 Codex；原生开放电脑操控并支持 AWS Bedrock 托管的 Agents API；面向实时分类与路由的轻量 Decisions API；可与 Devin、Notion 等第三方工具共享订阅额度的“Sign in with ChatGPT”；以及算力额度为 Plus 25 倍的全新 Pro 500 档位。 这次发布表明 OpenAI 押注“常驻、全天候运行的智能体”而非对话式会话，将其视为 AI 工作的下一代界面，并直接与 Meta 的 Muse 等竞品展开竞争。把智能体 API、订阅额度互通与分层算力定价集中在一次大会中发布，也重新定义了开发者构建智能体产品并在 OpenAI 技术栈上付费的方式。 在 OpenAI 的模型序列中，GPT-6.1 Sol 定位低于旗舰的 GPT-6 Astra，目前尚未在 ChatGPT 中提供，只能通过 API 以 gpt-6.1-sol 的名称调用；Codex 中的 Astra Ultrafast 比 Astra Standard 快最多 8 倍，比 Astra Fast 快 4 倍。Dots 可通过现有系统被赋予特定身份、凭证与工具权限，OpenAI 已在与微软合作，将其集成到 Agent 365 中。

telegram · zaihuapd · 9月29日 17:52

**背景**: OpenAI 于 2026 年 7 月推出的 GPT-6 系列按能力从低到高分为 Luna、Terra、Sol 以及旗舰 Astra，因此“Sol”代表的是中端模型线，OpenAI 通过 6.1 这样的版本迭代持续升级它。这里的“智能体（Agent）”指能够自主规划并执行多步任务（包括操作电脑）的 AI 系统，而不只是在聊天窗口中回答问题。Dots 正是 OpenAI 对这一趋势的回应，定位为常驻助手而非一问一答的聊天机器人，其发布时间比 Meta 推出竞品 Muse 智能体仅晚数周。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/introducing-dots/">Introducing dots - OpenAI</a></li>
<li><a href="https://openai.com/index/introducing-gpt-6-1-sol/">Introducing GPT - 6 . 1 Sol | OpenAI</a></li>
<li><a href="https://techcrunch.com/2026/09/29/openai-launches-dots-its-bubbly-agentic-avatar/">OpenAI launches Dots, its bubbly agentic avatar - TechCrunch</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#AI Agents`, `#GPT-6.1`, `#Developer Conference`, `#API`

---

<a id="item-3"></a>
## [隐私分析发现网页与移动端 AI 对话代理存在数据泄露](https://jorgegarciaherrero.com/wp-content/interactivos/20260916-Prompt-like-a-butterfly-sting-like-a-tracker-%28clean%29.pdf) ⭐️ 8.0/10

一篇题为《Prompt-like-a-butterfly, sting-like-a-tracker》的新论文对网页端和移动端的对话式 AI 代理进行了隐私分析，考察这些代理如何处理用户数据与追踪行为。该研究在 Hacker News 上引发讨论，帖子获得 408 分、130 条评论，用户在其中报告了具体泄露现象，例如 ChatGPT 会在用户点击发送之前，就把尚未写完的提示词发送到 \`conversation/prepare\` 接口。 对话式 AI 代理如今被用于撰写敏感内容和资料研究，因此提示词乃至未写完的提示词通过追踪或预取机制泄露的证据，动摇了“这些会话是私密的”这一假设。这一发现对普通用户、正在评估 AI 助手的企业，以及可能因聊天界面数据收集而面临监管审查的平台厂商都具有重要意义。 讨论指出，向 \`conversation/prepare\` 这类接口预取提示词，可能让服务商观察到用户的写作节奏、纠错习惯以及尚在成形中的半成品想法。评论者还指出，一些服务把 URL 中带一个 UUID 就当作足够的隐私保护，但实际上分享这样的链接会暴露整段对话内容。

hackernews · damaru2 · 9月29日 09:03 · [社区讨论](https://news.ycombinator.com/item?id=49890226)

**背景**: 对话式 AI 代理是用户通过网页浏览器或移动应用访问的聊天型助手，例如 ChatGPT 或 Perplexity。隐私研究者会考察这些代理向服务器发送了哪些数据、在什么时机发送，包括遥测信息、追踪器以及移动端的平台权限。UUID 是一种常被放进 URL 中用于引用特定会话的唯一标识符，由于看起来随机，常被误认为能保证匿名性。

**社区讨论**: 评论者普遍对当前隐私实践持怀疑态度：有人描述自己发现 ChatGPT 会预先发送未写完的提示词，有人认为基于 UUID 的链接被错误地等同于隐私保护（并以 Perplexity 为例），还有人质疑风险究竟来自代理本身，还是来自底层的平台 API 与权限。一个反复出现的主题是倾向于使用开放、可本地运行的模型；有评论者借用《辛普森一家》的桥段调侃，称用户如今已变成那个把所有秘密都告诉 AI 的角色。

**标签**: `#privacy`, `#AI agents`, `#security`, `#tracking`, `#web/mobile`

---

<a id="item-4"></a>
## [OpenAI 发布 Dots：常驻云端的 AI 智能体](https://openai.com/index/introducing-dots/) ⭐️ 8.0/10

OpenAI 正式推出 Dots，这是一款“常驻在线”（always-on）的 AI 智能体产品，每个 dot 都运行在属于自己的云端计算机上，并率先面向符合条件市场的 Pro、Business Premium 和 Enterprise 用户开放。每个 dot 拥有独立身份、凭据以及完成工作所需的系统访问权限，用户可以通过 Slack、Teams 等组织协作平台与它交互，短信（text message）支持也即将上线。 Dots 标志着行业从单轮对话式聊天机器人转向常驻云端、可持续代用户执行任务的自主智能体，也让 OpenAI 更深地介入企业工作流。它同时加剧了与 Anthropic 旗下 Claude 智能体以及 Meta 的 Muse 之间的竞争，并引发用户会被单一厂商平台锁定到何种程度的讨论。 OpenAI 表示，每个 dot 都能适应新信息，并通过团队反馈不断改进，同时设想让“专家型 Dots”（specialist Dots）承担特定职责；该产品借鉴了 OpenAI 内部在采购、发票处理、邮件营销、客户支持和商业合同等场景的测试经验。Dots 目前属于产品发布而非技术突破，首发阶段仅面向特定付费档位和特定市场开放。

hackernews · alvis · 9月29日 17:07 · [社区讨论](https://news.ycombinator.com/item?id=49896604)

**背景**: 像 ChatGPT 这类聊天助手通常是无状态的：你打开一次会话、提出请求、会话结束。而“常驻智能体”则持续运行在云端沙盒或虚拟机上，具备长期记忆与已连接账户，因此可以在无人盯着的情况下代你行动。这已成为整个行业的方向——Anthropic 基于 Claude 的编程智能体和 Meta 传闻中的 Muse 智能体都指向同一条路；但由于这类智能体会不断累积集成关系和工作历史，用户更换供应商的难度远高于单纯替换底层模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/introducing-dots/">Introducing dots | OpenAI</a></li>
<li><a href="https://techcrunch.com/2026/09/29/openai-launches-dots-its-bubbly-agentic-avatar/">OpenAI launches Dots, its bubbly agentic avatar | TechCrunch</a></li>
<li><a href="https://www.technobezz.com/news/openai-launches-dots-always-on-ai-agents">OpenAI Launches dots, Always-On AI Agents That Work in the Cloud | Technobezz</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者主要担忧平台锁定问题，认为带有各类集成和工作历史的常驻智能体本质上就是“你在云端的电脑”，比可随时替换的模型难以割舍得多。一些人表示 OpenAI 凭借慷慨的 Codex 订阅和高效的模型赢得了口碑，如今却在推销不必要的产品，并收紧当初吸引用户的那套宽松额度，这与 Anthropic 早前的做法如出一辙；也有人认为 Codex、ChatGPT Work 与 Dots 之间的界限越来越模糊，更看好 Meta 的 Muse 在消费级市场的分发优势，并预测这类云端智能体将宣告面向非技术用户和 AI 原住民的新时代、终结 PC 时代。

**标签**: `#OpenAI`, `#AI agents`, `#always-on agents`, `#platform lock-in`, `#product announcement`

---