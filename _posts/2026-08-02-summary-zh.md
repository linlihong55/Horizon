---
layout: default
title: "Horizon Summary: 2026-08-02 (ZH)"
date: 2026-08-02
lang: zh
---

> 从 29 条内容中筛选出 3 条重要资讯。

---

1. [卡帕西提议用 3D 场景生成作为 AI 基准引发争论](#item-1) ⭐️ 8.0/10
2. [eBay 高管因骚扰批评者被判刑，赔付 5600 万美元](#item-2) ⭐️ 8.0/10
3. [微软牵头公开信反对限制开放权重 AI 模型](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [卡帕西提议用 3D 场景生成作为 AI 基准引发争论](https://twitter.com/karpathy/status/2083749667410727319) ⭐️ 8.0/10

Andrej Karpathy 发布推文称，像“生成一个自行车上鹈鹕的 SVG”这类简单 LLM 测试正在过时，并提出了一个更难的测试：给 Opus 5《指环王》第一段文本、100 万 token 预算（约 10 美元），要求生成一个 three.js 渲染场景。该推文迅速引发社区讨论，争论 3D 场景生成是否能作为衡量 AI 对物理世界理解的有意义基准。 作为 AI 领域最具影响力的人物之一，卡帕西的建议将关注点从静态图像生成转向具有空间和物理感知的场景生成这一新的评估前沿。这场争论可能影响未来模型的基准测试方式，尤其是在能力超越聊天机器人和 2D 图像生成之后。 卡帕西特意用“自行车上的鹈鹕”来代表过去较简单的测试，并提出用《指环王》作为输入、100 万 token 预算（约 10 美元）来完成一个 three.js 代码生成任务。多位评论者提醒，模型能生成好的 three.js 代码可能只是因为训练数据中包含大量此类代码，并不代表普遍物理理解；同时，像 3DGen-Bench 这样的现有基准已经在尝试将 3D 生成评估系统化。

hackernews · delichon · 8月2日 04:05 · [社区讨论](https://news.ycombinator.com/item?id=49140998)

**背景**: LLM 基准测试长期以来包含生成 SVG 等简单任务，这些任务只考验基本的指令遵循能力，而非深层的世界建模能力。相比之下，3D 场景生成要求模型推理空间关系、物体恒存性和物理合理性，因此是更丰富的潜在基准。卡帕西的推文是社区寻找下一代基准、更好衡量 AI 对真实世界理解的一部分；最近的学术工作如 3DGen-Bench 也通过大规模人类偏好评估文本到 3D 和图像到 3D 模型，与这一方向不谋而合。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://x.com/karpathy/status/2083749667410727319">Andrej Karpathy on X: &quot;We&#x27;re starting to leave the territory where you ...</a></li>
<li><a href="https://arxiv.org/abs/2503.21745">[2503.21745] 3DGen-Bench: Comprehensive Benchmark Suite for 3D Generative Models</a></li>
<li><a href="https://arxiv.org/html/2503.21745v3">3DGen-Bench: Comprehensive Benchmark Suite for 3D Generative Models</a></li>

</ul>
</details>

**社区讨论**: 评论者观点明显分化：像 jmugan 这样的用户支持这一想法，认为不完美的 3D 输出恰恰能比图像更好地暴露对物理世界的理解。另一些人如 YmiYugy 担心长期接触 AI 内容已经拉低了公众对质量的预期；HarHarVeryFunny 则警告说，出色的 three.js 输出可能只是训练痕迹。bredren 则分享了自己用 LLM 从电影场景描述构建 3D 动画的实际项目。

**标签**: `#AI`, `#Machine Learning`, `#Benchmarking`, `#3D Generation`, `#Karpathy`

---

<a id="item-2"></a>
## [eBay 高管因骚扰批评者被判刑，赔付 5600 万美元](https://www.ft.com/content/06ec1b03-d4af-40cf-b12a-4ba5a410f6d2) ⭐️ 8.0/10

联邦法官判处七名前 eBay 安全高管参与针对戴维和伊娜·施泰纳的骚扰行动，这对夫妇曾发布批评 eBay 的通讯稿。eBay 公司同意支付 5600 万美元以了结相关民事索赔。 此案是高管因针对网络批评者而面临刑事指控的罕见案例，凸显了科技公司内部安全团队的法律责任。它向企业发出警告：对记者和博主的骚扰将带来严重后果。 在判决中，前安全与安保高级总监吉姆·鲍获得 57 个月监禁；前全球复原力总监戴维·哈维尔获较轻刑期；布赖恩·吉尔伯特被判服刑期满、一年监督释放及 2 万美元罚款。包括前警察队长在内的七名 eBay 安全团队成员参与了此次行动。

hackernews · JumpCrisscross · 8月2日 19:19 · [社区讨论](https://news.ycombinator.com/item?id=49147435)

**背景**: 此案源于 2019 年 eBay 安全团队的一项计划，旨在让戴维和伊娜·施泰纳闭嘴，这对夫妇出版一份报道 eBay 卖家并经常批评公司的在线通讯。员工向这对夫妇在马萨诸塞州的家中寄送威胁性和令人不安的包裹，包括一盒活蟑螂、一个带血猪面具和葬礼花圈。骚扰还升级为 GPS 跟踪、监视，甚至使用\#Crushthislady 标签的社交媒体运动。肇事者意图恐吓施泰纳夫妇让他们停止报道。

**社区讨论**: 评论者对骚扰是否仅限于一对夫妇表示怀疑，暗示 eBay 可能还针对其他批评者。还有人质疑涉案前警察队长的职业生涯，并询问是否进行了更广泛的调查。

**标签**: `#eBay`, `#corporate accountability`, `#harassment`, `#legal`, `#tech ethics`

---

<a id="item-3"></a>
## [微软牵头公开信反对限制开放权重 AI 模型](https://simonwillison.net/2026/Aug/2/open-letters/#atom-everything) ⭐️ 8.0/10

2026 年 7 月 24 日，微软牵头发布公开信《开放权重与美国 AI 领导力》，获 NVIDIA、亚马逊、Y Combinator、Linux 基金会以及后来加入的 OpenAI 等 235 家 AI 相关公司联署，反对限制开放权重 AI 模型。7 月 28 日，另一封公开信《Pacing the Frontier》发布，由 1324 名前沿 AI 公司员工签署，呼吁美国政府支持国际合作，审慎把控自动化 AI 开发的节奏。 这标志着美国 AI 政策辩论中一次重大的行业联合，多家领先企业公开反对以“安全”为由限制开放权重模型。微软联盟与 Anthropic 较谨慎立场之间的分歧，加上数量空前的 AI 员工呼吁“有节奏地”推进开发，表明开源与前沿 AI 的监管将成为该行业的关键议题。 微软的公开信特别支持“蒸馏”——即使用其他模型的输出来训练或改进模型——并敦促政策制定者不要将其与不当挪用混为一谈。Anthropic 未签署该信，并于三天后发布自身立场，反对全面禁令，但警告威权政府滥用以及工业规模的蒸馏操作；其 CEO Dario Amodei 也签署了《Pacing the Frontier》。

rss · Simon Willison · 8月2日 04:16

**背景**: 开放权重 AI 模型是指已训练好的神经网络模型公开其学习到的权重和偏置，任何人都可以下载和运行，但能否修改或再分发取决于其许可证。支持者认为这种透明性有助于审查和广泛使用，而批评者则担心无限制使用可能导致滥用，或失去闭源模型所规避的集中风险。蒸馏是一种常见技术，即用一个模型的输出来训练另一个模型，它已成为开放权重争论中的一个争议点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Open-weight_model">Open-weight model</a></li>
<li><a href="https://www.microsoft.com/en-us/corporate-responsibility/topics/open-weight/">Open Weights and American AI Leadership</a></li>

</ul>
</details>

**标签**: `#AI policy`, `#Open weights`, `#Microsoft`, `#AI regulation`, `#Open source`

---