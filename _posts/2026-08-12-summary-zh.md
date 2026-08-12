---
layout: default
title: "Horizon Summary: 2026-08-12 (ZH)"
date: 2026-08-12
lang: zh
---

> 从 37 条内容中筛选出 10 条重要资讯。

---

1. [Qwen 开源发布 2.4T 参数 MoE 模型 Qwen3.8-2.4T-A95B](#item-1) ⭐️ 9.0/10
2. [DeepSeek V4 Pro 0813 上线 OpenRouter，用户将其与 Grok 4.6 对比测试](#item-2) ⭐️ 8.0/10
3. [Tailscale 将数据库损坏追溯到 16 年前的 SQLite WAL 重置 Bug](#item-3) ⭐️ 8.0/10
4. [xAI 发布 Grok 4.6，引发 API 与基准测试争议](#item-4) ⭐️ 8.0/10
5. [Chrome 的 JPEG 缩放算法导致小图像渲染不同](#item-5) ⭐️ 8.0/10
6. [uBlock Origin 放弃过滤 Facebook 广告](#item-6) ⭐️ 8.0/10
7. [文章称 AI 冲击中级软件工程师阶层](#item-7) ⭐️ 8.0/10
8. [车牌读取器搜索应需搜查令](#item-8) ⭐️ 8.0/10
9. [Adam 破坏基不变性，失去 GD 在分解模型中的低秩偏差](#item-9) ⭐️ 8.0/10
10. [LTX 发布开源视频模型 LTX-2.5，单张 RTX 5090 即可运行](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Qwen 开源发布 2.4T 参数 MoE 模型 Qwen3.8-2.4T-A95B](https://huggingface.co/Qwen/Qwen3.8-2.4T-A95B) ⭐️ 9.0/10

阿里巴巴 Qwen 团队在 Hugging Face 上开放了 Qwen3.8-2.4T-A95B 的权重，这是一个混合专家（MoE）大语言模型，总参数量 2.4 万亿，每个 token 激活 950 亿参数。此次发布提供 bf16 和 FP8 检查点，原生上下文长度为 262,144 个 token，可扩展至超过 100 万个 token。 这使接近前沿的模型能力进入开放权重生态，研究人员和企业可以自行部署一个与领先闭源系统竞争的大模型。然而，其庞大的规模意味着只有拥有大规模多 GPU 或多节点基础设施的机构才实际部署得起。 BF16 检查点约为 4.9TB，FP8 版本约为其一半；社区估计 4 比特量化版可降至约 1.3TB，但官方未发布 QAT（量化感知训练）的 q4 权重。开放权重模型缺少 Qwen3.8-Max 的部分功能，如视觉输入、非思考模式和内置工具，其许可证对超过一定营收门槛的商业用途有所限制。

hackernews · Philpax · 8月12日 15:01 · [社区讨论](https://news.ycombinator.com/item?id=49273478)

**背景**: 混合专家（MoE）是一种将计算分散到多个“专家”子网络、每个 token 只激活其中少数的架构，从而在推理成本不按比例增加的情况下实现很大的参数量。量化通过 FP8 或 INT4 等低精度格式存储权重来减少模型内存占用，通常质量损失很小。此类开放权重发布让社区可以在 API 之外自行运行、微调并基于前沿规模模型进行开发。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/serve-qwen3-8-2-4t-a95b-a-2-4t-parameter-model-with-configurable-reasoning-on-nvidia-gb300-nvl72/">Serve Qwen 3 . 8 - 2 . 4 T - A 95 B , a 2 . 4 T -Parameter Model , with...</a></li>
<li><a href="https://huggingface.co/Qwen/Qwen3.8-2.4T-A95B">Qwen/ Qwen 3 . 8 - 2 . 4 T - A 95 B · Hugging Face</a></li>
<li><a href="https://arxiv.org/abs/2507.11181">[2507.11181] Mixture of Experts in Large Language Models</a></li>

</ul>
</details>

**社区讨论**: 社区讨论既热情又务实：用户对 1 比特量化版可压缩到约 397GB、能在普通可购买机器上达到高端性能感到惊讶，但也指出 BF16/FP8 版本比 Kimi k3 更难部署，且没有 QAT q4 权重。还有人失望地表示开放权重模型缺少 Qwen3.8-Max 的视觉输入、100 万上下文和内置工具；也有用户对小硬件运行此模型表达了嘲讽式怀疑。

**标签**: `#AI`, `#LLM`, `#Qwen`, `#MoE`, `#open-source`

---

<a id="item-2"></a>
## [DeepSeek V4 Pro 0813 上线 OpenRouter，用户将其与 Grok 4.6 对比测试](https://openrouter.ai/deepseek/deepseek-v4-pro-0813) ⭐️ 8.0/10

DeepSeek V4 Pro 0813（DeepSeek V4 Pro 模型的新版本）已在 OpenRouter 上出现。早期社区测试显示，在编码代理任务上它的价格远低于 Grok 4.6，但在一次直接对比测试中速度更慢且产生了 bug。 这次发布延续了 DeepSeek 以极低 API 价格提供开源权重模型的策略，迫使竞争对手在成本与能力上同时竞争。早期的对比为开发者选择“极便宜”还是“更快更可靠”的替代方案提供了真实世界信号。 在社区针对 Codex CLI 的测试中，DeepSeek V4 Pro 0813 用 12 分 02 秒、花费 0.12 美元完成任务，但引入了 bug；而 Grok 4.6 用 3 分 18 秒、花费 1.41 美元且无 bug。该模型属于 DeepSeek V4 系列，该系列还有一个更轻量、更便宜的“Flash”预览版。

hackernews · explosion-s · 8月12日 16:04 · [社区讨论](https://news.ycombinator.com/item?id=49274600)

**背景**: DeepSeek 是一家中国生成式 AI 公司，其开源权重模型（如 R1）以较低成本媲美更昂贵的竞争对手而广受国际关注。DeepSeek V4-Pro 是其旗舰大语言模型，公司已发布更轻量的“Flash”预览版，在简单代理任务上接近 V4-Pro 的水平。Grok 是 SpaceXAI 开发的竞争性 LLM 系列，以与 X 平台集成及代理式编程工具著称。OpenRouter 是一个中立的 API 网关，让开发者通过一个接口比较和调用多种模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek_%28product%29">DeepSeek (product)</a></li>
<li><a href="https://api-docs.deepseek.com/news/news260424/">DeepSeek V 4 Preview Release | DeepSeek API Docs</a></li>
<li><a href="https://en.wikipedia.org/wiki/Grok_4">Grok 4</a></li>

</ul>
</details>

**社区讨论**: 评论者大多对 DeepSeek 的性价比表示肯定，有用户称赞此前 Flash 更新能“用极低的成本处理重型开发”。在 Codex CLI 上的直接对比测试显示，DeepSeek 比 Grok 4.6 便宜得多但更慢且存在 bug；另有用户表示，大多数任务并不需要顶级智能，只需要最便宜且能完成工作的模型。也有人批评新闻链接到 OpenRouter 而非官方 API 文档或基准测试。

**标签**: `#AI`, `#DeepSeek`, `#language models`, `#ML`, `#API`

---

<a id="item-3"></a>
## [Tailscale 将数据库损坏追溯到 16 年前的 SQLite WAL 重置 Bug](https://tailscale.com/blog/sqlite-wal-reset-bug) ⭐️ 8.0/10

Tailscale 发布了一份事后分析报告，将数据库损坏问题追溯到 16 年前的一个 SQLite WAL 重置 Bug。他们还资助了一个开源的 VFS 垫片，该垫片帮助快速隔离了导致问题的竞态条件。 这份事后分析很有价值，因为它展示了公司如何直接资助开源调试工具，从而使更广泛的生态系统受益。它还提高了人们对一个细微的 SQLite WAL 竞态条件的认识，该竞态条件会影响任何在 WAL 模式下使用多个连接的应用程序。 该 Bug 是写事务与 WAL 重置之间的竞态条件，已在 SQLite 3.51.3 中修复。VFS 垫片（虚拟文件系统垫片）提供了一个拦截和记录操作的层，有助于隔离此类并发问题。

hackernews · ropbear · 8月12日 14:22 · [社区讨论](https://news.ycombinator.com/item?id=49272832)

**背景**: SQLite 是一种常用的嵌入式数据库，它可以通过可选的 Write-Ahead Logging（WAL）模式获得更好的并发性和崩溃安全性。在 WAL 模式下，写入被追加到日志文件中，然后检查点回主数据库。自 2010 年以来就存在的一个长期 Bug 允许写事务与 WAL 重置之间发生冲突，从而导致数据库损坏。SQLite 团队此前并未意识到这个 Bug，直到它被报告后才在 3.51.3 版本中修复。Tailscale 资助了一个开源的 VFS 垫片——一个用于拦截 SQLite 操作系统接口调用的层——以帮助诊断此问题以及将来类似的 Bug。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tailscale.com/blog/sqlite-wal-reset-bug">How Tailscale helped find the SQLite WAL-Reset bug</a></li>
<li><a href="https://antithesis.com/blog/2026/wal-reset-bug/">Breaking the WAL | Antithesis</a></li>
<li><a href="https://www.sqlite.org/vfs.html">The SQLite OS Interface or &quot; VFS &quot;</a></li>

</ul>
</details>

**社区讨论**: 社区成员对这篇详细的文章表示赞赏，称赞 Tailscale 资助开源调试工具并与 SQLite 签订支持合同的做法。有人对单写者设计下竞态条件的具体触发方式感到好奇，还有人引用了 Dijkstra 的名言：测试只能证明 Bug 的存在，而不能证明其不存在。

**标签**: `#sqlite`, `#postmortem`, `#debugging`, `#open-source`, `#wal`

---

<a id="item-4"></a>
## [xAI 发布 Grok 4.6，引发 API 与基准测试争议](https://x.ai/news/grok-4-6) ⭐️ 8.0/10

xAI 发布了 Grok 4.6，这是其前沿 AI 模型的新版本，可通过 xAI API 使用。该发布迅速引发了社区关于 API 默认系统提示词处理方式以及其基准测试成绩真实性的讨论。 Grok 4.6 之所以重要，因为它代表着 xAI 在竞争激烈的前沿模型领域的持续发力，用户在某些任务上将其与 GPT-5.6-Sol 和 Claude 4.8/5 等模型进行对比并给予好评。然而，社区对基准测试污染和系统提示词干扰的担忧，可能会影响人们对该模型报告能力与 API 行为的信任。 根据官方文档，Grok 4.6 通过 xAI API 中的模型 ID &\#x27;grok-4.6&\#x27;访问。GitHub 仓库&\#x27;grok-prompts&\#x27;显示，xAI 会为模型注入系统提示词前缀，社区成员报告称，其中一条指示模型不要提及这些准则的内容会覆盖用户提供的系统提示词。

hackernews · iLuddite · 8月12日 15:32 · [社区讨论](https://news.ycombinator.com/item?id=49274027)

**背景**: Grok 是 xAI 开发的一系列大语言模型，旨在提供有帮助、真实且略带不羁的回答。在 API 使用中，系统提示词是一组指导模型行为的指令，xAI 似乎会注入一个用户无法完全覆盖的默认提示词。基准测试污染指的是模型训练数据中包含测试答案，导致基准成绩虚高的情况；社区讨论认为这可能是各大实验室模型迅速进步的一种解释。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/xai-org/grok-prompts">GitHub - xai-org/grok-prompts: Prompts for our Grok chat assistant and the `@grok` bot on X. · GitHub</a></li>
<li><a href="https://docs.x.ai/developers/grok-4-6">Grok 4.6 - Docs - SpaceXAI</a></li>
<li><a href="https://www.mindstudio.ai/blog/ai-benchmark-contamination-swebench-pro-deepswe">AI Benchmark Contamination : Why SWEBench Pro... | MindStudio</a></li>

</ul>
</details>

**社区讨论**: 社区反应不一：一些用户称赞 Grok 4.6 的速度、简洁性和相较于竞争对手的强劲基准成绩，另一些用户则批评 API 默认系统提示词的行为，指出它可能覆盖用户指令并拒绝讨论系统提示词。还有评论者质疑多个实验室如何在两个月内发布&\#x27;Fable 级别&\#x27;的模型，提出可能是技术传播或基准测试造假所致，但目前尚无定论。

**标签**: `#AI`, `#Grok`, `#xAI`, `#Machine Learning`, `#Model Release`

---

<a id="item-5"></a>
## [Chrome 的 JPEG 缩放算法导致小图像渲染不同](https://guillaumetech.github.io/posts/jpg-scaling-chrome/) ⭐️ 8.0/10

一篇新的技术博客文章解释称，Chrome 渲染缩小后的 JPEG 图像与其他浏览器不同，原因是 Chrome 使用了基于 Lanczos 的特定缩放算法。这种差异在图标和缩略图等小图像上尤为明显。 这很重要，因为 Web 开发人员希望图像在不同浏览器中渲染一致，尤其是图标和缩略图。理解 Chrome 的行为可帮助开发者选择合适的图像格式和分辨率，以避免视觉差异。 Chrome 在将图像缩小超过 2.5% 时可能使用 Lanczos 滤波器，而其他浏览器使用双线性等不同算法。CSS 的 \`image-rendering\` 属性可以部分控制缩放方式，评论中也提到类似问题也影响 PNG 图像。

hackernews · gutechh · 8月12日 14:00 · [社区讨论](https://news.ycombinator.com/item?id=49272549)

**背景**: 数字图像通常需要缩小以适应屏幕显示。浏览器使用图像重采样算法（如双线性、双三次或 Lanczos）在缩放时插值像素。Lanczos 重采样以保持清晰度著称，但可能引入振铃伪影，而双线性滤波结果更平滑但更模糊。这些算法差异导致同一图像在不同浏览器中显示略有不同。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://entropymine.com/resamplescope/notes/browsers/">How web browsers resize images - entropymine.com</a></li>
<li><a href="https://en.wikipedia.org/wiki/Lanczos_resampling">Lanczos resampling</a></li>
<li><a href="https://css-tricks.com/almanac/properties/i/image-rendering/">image-rendering | CSS-Tricks</a></li>

</ul>
</details>

**社区讨论**: 评论者指出，同样的缩放问题也影响 PNG，并可能破坏 Electron 应用中的图标；有人链接到 Firefox 中低比例解码的相关工作。还有人指出 Chrome 和 Firefox 只是使用了不同的缩放算法，对 Chrome 的模糊效果和 Firefox 的更清晰但略带振铃的效果各有偏好。也有人提到可以通过 CSS 的 \`image-rendering\` 属性进行部分修复，但各浏览器行为不一。

**标签**: `#jpeg`, `#chrome`, `#image-scaling`, `#web-development`, `#rendering`

---

<a id="item-6"></a>
## [uBlock Origin 放弃过滤 Facebook 广告](https://digitalescapetools.com/2026/08/ublock-origin-stops-chasing-facebook-ads.html) ⭐️ 8.0/10

uBlock Origin 宣布停止维护针对 Facebook 广告的专用过滤规则，承认 Facebook 激进的对抗措施已使这一努力徒劳。这一消息在 Reddit 上迅速引来 358 条评论，反映了广告拦截军备竞赛的最新进展。 作为最广泛使用的开源广告拦截器之一，uBlock Origin 的退却表明，即使专注的客户端拦截器也可能无法跟上 Facebook 等大型平台的步伐。数百万用户将不得不忍受广告或另寻解决方案，这一事件也凸显了对基于计算机视觉的新拦截方法的需求。 Facebook 以其频繁更新广告投放代码（有时每小时一次）来绕过静态过滤规则而闻名，这使得规则维护成为一场必败之战。uBlock Origin 团队如今将把资源转向维护其他网站的过滤规则，同时社区成员正在讨论技术变通方案能否提供永久解决方案。

hackernews · Markoff · 8月12日 11:28 · [社区讨论](https://news.ycombinator.com/item?id=49270726)

**背景**: uBlock Origin 是一款免费开源的浏览器扩展，通过 EasyList 以及自己的 uAssets 仓库等过滤规则集来屏蔽广告、跟踪器和其他不需要的内容。Facebook 的大部分收入来自广告，多年来一直部署强有力的反广告拦截手段；例如，2016 年它开始向广告拦截用户展示广告。广告拦截器与内容发布者之间的‘军备竞赛’已持续数十年，双方不断更新代码和过滤规则。一些安全研究人员提出了类似计算机视觉的面向未来的方案，通过视觉识别广告，以绕开需要不断更新的过滤规则。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://support.adblockultimate.net/en/articles/9240458-anti-adblock-techniques">Anti - adblock techniques | AdBlocker Ultimate Help Center</a></li>
<li><a href="https://github.com/uBlockOrigin/uAssets">GitHub - uBlockOrigin/uAssets: Filter lists for uBlock Origin &amp; uBlock Origin Lite · GitHub</a></li>

</ul>
</details>

**社区讨论**: Reddit 上的讨论大多支持这一决定，许多评论者认为 Facebook 的广告确实难以被可靠拦截。有人认为唯一真正的办法是完全离开 Facebook，而另一些人则半开玩笑地预测，未来会出现一个计算机视觉模型，把屏幕上任何看起来像广告的元素框起来。也有少数人质疑其中的经济学，指出安装了广告拦截器的用户本来也不太可能去点击广告。

**标签**: `#adblocking`, `#privacy`, `#facebook`, `#ublock-origin`, `#web`

---

<a id="item-7"></a>
## [文章称 AI 冲击中级软件工程师阶层](https://blog.florianherrengt.com/ai-removing-middle-class-software-engineering.html) ⭐️ 8.0/10

一篇博文认为，AI 编程工具正在不成比例地冲击中级软件工程师岗位，同时放大优秀与平庸工程师各自的影响。这篇文章在 Hacker News 上引发了关于职业前景与工程质量的广泛讨论。 这一点很重要，因为 AI 辅助开发已经在改变软件行业的招聘与团队结构。这场讨论反映出人们对职业发展、工作稳定性以及 AI 工具普及后如何管理工程质量的真实担忧。 文章的核心观点是“糟糕的工程师从来都是隐患”，而 AI 现在让能力较弱的工程师能把不良实践放大到整个组织。评论者还提到“StackOverflow 式工程师的自动化”，即高级工程师不再需要把编码任务交给初级或中级员工。

hackernews · florianherrengt · 8月12日 13:20 · [社区讨论](https://news.ycombinator.com/item?id=49271994)

**背景**: AI 编程助手和基于大语言模型的智能体发展迅速，使开发者能更快地生成和修改代码。这导致人们预测，传统上分配给初级和中级工程师的常规编码工作将会缩减，而高级工程师则更多地专注于架构、代码审查和产品决策。软件工程中的“中间阶层”指的是主要实现明确定义任务的工程师，而这正是 AI 工具最擅长自动化的部分。

**社区讨论**: 评论者大体赞同这篇文章，但提出了更多细节。有人警告说，缺乏热情的资深工程师可以用 AI 大规模交付劣质代码；也有人把这种变化称为“StackOverflow 式工程师的自动化”，而非消灭所有初级岗位。还有少数人质疑，目前是否已出现由 LLM 编程代理直接导致大规模软件岗位流失的具体证据。

**标签**: `#AI`, `#software-engineering`, `#careers`, `#LLM`, `#industry-impact`

---

<a id="item-8"></a>
## [车牌读取器搜索应需搜查令](https://andrewpwheeler.com/2026/08/12/license-plate-reader-searches-should-require-a-warrant/) ⭐️ 8.0/10

这篇文章认为，警方在无搜查令情况下访问自动车牌读取器（ALPR）数据属于侵犯隐私，应需司法监督。该文章引发了关于监控风险和替代技术的大规模社区讨论。 ALPR 系统越来越多地部署在公共空间，能够对车辆位置进行大规模追踪。确立搜查令要求将为保护公民自由免受普遍监控树立重要先例。 ALPR 利用光学字符识别读取车牌，并可存储图像、车牌文本甚至驾驶员照片，从而形成全面的移动记录。评论者指出这些摄像头是通用的联网设备，可能被重新利用，还有人提议使用可改变标识符的加密车牌来防止追踪。

hackernews · apwheele · 8月12日 14:43 · [社区讨论](https://news.ycombinator.com/item?id=49273165)

**背景**: 自动车牌读取器（ALPR，也称 ANPR）是使用光学字符识别技术拍摄车辆牌照并生成位置数据的摄像头。执法部门利用它来核查车辆注册和调查犯罪，但隐私倡导者警告说，它可能实现大规模监控和追踪公民行踪。电子前沿基金会（EFF）指出，ALPR 让警方比传统手段更容易追踪所有人。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Automatic_number-plate_recognition">Automatic number-plate recognition - Wikipedia</a></li>
<li><a href="https://www.eff.org/pages/what-alpr">Data Driven: What Is ALPR? | Electronic Frontier Foundation</a></li>

</ul>
</details>

**社区讨论**: 评论者大体同意无需搜查令的 ALPR 访问令人担忧，但多人认为仅要求搜查令并不足够。他们指出这些摄像头是通用设备，可能被重新用于更广泛的监控，并提出用加密替代方案来防止追踪；还有人提到警方曾滥用数据（如跟踪他人），认为根本不应大规模收集这些数据。

**标签**: `#privacy`, `#surveillance`, `#law-enforcement`, `#ALPR`, `#policy`

---

<a id="item-9"></a>
## [Adam 破坏基不变性，失去 GD 在分解模型中的低秩偏差](https://www.reddit.com/r/MachineLearning/comments/1vmjb3p/the_loss_does_not_see_the_basis_but_adam_does_r/) ⭐️ 8.0/10

一项新研究表明，Adam 的逐坐标预处理破坏了分解模型 W=UVᵀ的旋转不变性，使其失去梯度下降隐式持有的低秩偏差。在欠定矩阵感知上对九种更新规则的实验中，只有 GD、共享标量 Adam、Muon 和 Shampoo 保留了该偏差，而 Adam、RMSProp、Lion、signum 和 Adafactor 则失去了它。 这为深度学习中选择优化器为何会改变泛化性能提供了机制性解释，并将罪魁祸首从自适应性本身区分出来，指向逐坐标非均匀缩放（各向异性）。它可能引导研究者和从业者使用能保留低秩等有益归纳偏置的优化器（如 Muon 或共享标量变体）进行训练。 作者引入了一个单参数族，将 Adam 的分母从逐坐标插值到单一共享标量，恢复误差沿该参数族单调改善。他们还给出一个限制：高光谱数据上 43–44%的留出误差降低使用了仅基于训练集的学习率规则，而该规则恰好给 Adam 在其网格上最差的学习率；此外理论只覆盖无记忆（memoryless）规则，动量部分是经验性结论。

reddit · r/MachineLearning · /u/EtherealGlyph · 8月12日 16:39

**背景**: 在分解模型 W=UVᵀ中，用一个正交矩阵 Q 旋转因子（U→UQ, V→VQ）不会改变损失值，因此损失具有基不变性（旋转不变性）。梯度下降尊重这种不变性，并自然会收敛到低秩解，这一性质被称为隐式低秩偏差；而 Adam 的逐坐标二阶矩估计依赖于因子所处的基，从而破坏了该不变性。Muon 是一种较新的优化器，它对动量更新施加牛顿-舒尔茨（Newton–Schulz）正交化步骤，似乎能够保留这一偏差。这些概念与深度学习的理论和实践都相关，因为隐式偏差有助于解释模型为何能在欠定问题上泛化。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://grokipedia.com/page/muon-optimizer">Muon optimizer</a></li>
<li><a href="https://en.papernotes.org/ICLR2026/llm_pretraining/implicit_bias_and_loss_of_plasticity_in_matrix_completion_depth_promotes_low-ran/">[Paper Note] Implicit Bias and Loss of Plasticity in Matrix Completion...</a></li>
<li><a href="https://www.math.fsu.edu/~gallivan/talks/BakerNADay12.pdf">Recent Work at the Intersection of Optimization and Linear Algebra</a></li>

</ul>
</details>

**标签**: `#optimization`, `#Adam`, `#low-rank bias`, `#matrix sensing`, `#deep learning theory`

---

<a id="item-10"></a>
## [LTX 发布开源视频模型 LTX-2.5，单张 RTX 5090 即可运行](https://ltx.io/model/ltx-2-5) ⭐️ 8.0/10

LTX 发布了开源视频生成基础模型 LTX-2.5，权重、训练代码和推理管线全部开放。该模型可在单张 RTX 5090 上本地运行，年收入低于 1000 万美元的公司可免费商用。 此次发布大幅降低了研究人员和开发者使用前沿视频生成模型的门槛，开放权重和训练代码使其可以在消费级硬件上本地部署和完全定制。同时，这也加剧了开源视频生成领域的竞争，而该领域此前主要由体积更大、闭源的模型主导。 LTX-2.5 支持文生视频和图生视频，并改进了多镜头连贯性和提示词遵循能力。它引入了新的扩散视频解码器，并使用 Google 的 Gemma 4 12B 作为文本编码器；在 98 个提示词的视频瑕疵评测中，LTX 2.5 Pro 在十个模型中排名第一。

telegram · zaihuapd · 8月12日 02:15

**背景**: LTX-2.5 是一种基于扩散的视频生成模型，通过学习帧之间的时间结构来生成连贯、高质量的视频。其前代模型 LTX-2.3 已经开放权重，而 LTX-2.5 进一步加入了原生多镜头场景和编辑真实视频的能力。该模型使用了扩散视频解码器和 Google 的 Gemma 4 12B 文本编码器，后者是一种面向笔记本级硬件优化的无编码器多模态模型。RTX 5090 是 NVIDIA 最新的高端消费级 GPU，LTX-2.5 针对单卡本地推理进行了优化。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ltx.io/model/open-source">LTX-2.5 Model Open Source: AI Video Generator</a></li>
<li><a href="https://ltx.io/model">Multimodal Model For Generative Creation | LTX Model</a></li>
<li><a href="https://blog.google/innovation-and-ai/technology/developers-tools/introducing-gemma-4-12b/">Introducing Gemma 4 12 B</a></li>

</ul>
</details>

**标签**: `#video generation`, `#open-source`, `#AI model`, `#text-to-video`, `#diffusion`

---