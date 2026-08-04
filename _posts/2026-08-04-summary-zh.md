---
layout: default
title: "Horizon Summary: 2026-08-04 (ZH)"
date: 2026-08-04
lang: zh
---

> 从 33 条内容中筛选出 12 条重要资讯。

---

1. [Qwen 3.8-Max：2.4 万亿参数，首款开源 Max 级模型](#item-1) ⭐️ 9.0/10
2. [OpenAI 重点介绍人工智能驱动的数学与理论计算机科学十大进展](#item-2) ⭐️ 8.0/10
3. [开发工具必须开源：LLM 让这一理想更可行](#item-3) ⭐️ 8.0/10
4. [ComfyUI 首发支持 MiniMax H3：开放权重、原生音频与 2K 视频](#item-4) ⭐️ 8.0/10
5. [安迪·帕夫洛加入 ClickHouse，创立 ClickHouse 实验室](#item-5) ⭐️ 8.0/10
6. [Jane Street 的 Bonsai：用 OCaml 构建 Web UI](#item-6) ⭐️ 8.0/10
7. [Kimi K3 架构深度解析：压缩记忆与潜在路由](#item-7) ⭐️ 8.0/10
8. [审稿人呼吁：论文不附可复现代码应直接拒稿](#item-8) ⭐️ 8.0/10
9. [DNA 分析设备漏洞或致 30 年法医证据面临篡改风险](#item-9) ⭐️ 8.0/10
10. [美至少 50 名警员被控滥用车牌摄像头窥探前任](#item-10) ⭐️ 8.0/10
11. [英伟达 170HX 矿卡破解：解锁 80GB 显存，二手价暴涨](#item-11) ⭐️ 8.0/10
12. [苹果就英国政府 iCloud 后门要求提起法律诉讼](#item-12) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Qwen 3.8-Max：2.4 万亿参数，首款开源 Max 级模型](https://qwen.ai/blog?id=qwen3.8) ⭐️ 9.0/10

通义千问团队发布了 Qwen 3.8-Max，参数量达 2.4 万亿（活跃参数 95B），基于 Qwen 3.5 架构，并宣布模型权重将于下周开源。这是 Qwen 首次开放 Max 级别模型的权重。 这是开源大语言模型领域的一个里程碑，因为一款顶级的 Max 级别模型即将向社区免费开放。它可能重塑开源 AI 生态，让开发者和研究人员在编程、工作、研究和长周期任务方面获得最先进的能力。 该模型总参数量为 2.4 万亿，但每个 token 仅激活 95B 参数，表明其采用混合专家（MoE）设计，内存占用与每 token 计算量、服务成本是分离的。在测试中，Qwen 3.8-Max 可自主运行编码项目超过 10 天，并在 WWW2025 多模态对话意图识别竞赛中击败了 526 支队伍中的 458 支；目前可通过 QwenCloud 使用 API。

telegram · zaihuapd · 8月3日 02:31

**背景**: 大语言模型通常采用混合专家（MoE）架构，每次输入只激活一部分“专家”子网络。总参数量决定模型的存储和内存占用，而活跃参数量决定每个 token 的计算量，进而影响延迟和服务成本。这个区别解释了为什么一个 2.4 万亿参数的模型可以仅用 95B 活跃参数来提供推理服务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://qainsights.com/qwen-3-8s-hidden-cost-problem-total-parameters-vs-active-parameters-explained/">Qwen 3.8&#x27;s Hidden Cost Problem: Total Parameters vs Active ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://www.ibm.com/think/topics/mixture-of-experts">What is mixture of experts? | IBM</a></li>

</ul>
</details>

**标签**: `#AI`, `#LLM`, `#Qwen`, `#open-source`, `#model release`

---

<a id="item-2"></a>
## [OpenAI 重点介绍人工智能驱动的数学与理论计算机科学十大进展](https://openai.com/index/ten-advances-in-mathematics/) ⭐️ 8.0/10

OpenAI 发布了一份由人工智能驱动的数学与理论计算机科学十项进展的总结。该文强调了大语言模型（LLM）在数学发现与证明中日益重要的作用。 这标志着人工智能正在成为纯数学和理论计算机科学领域可靠的研究工具，可能加速发现并自动化部分证明过程。这些进展还可能改变数学家的研究方式：由人工智能处理计算性繁重工作，而人类专注于直觉与猜想。 根据社区讨论，该列表包括高维球填充和多色拉姆齐数方面的研究。评论指出，虽然当前的模型尚不能凭直觉提出猜想，但它们可以通过蛮力计算快速反驳一些假设。

hackernews · milkshakes · 8月3日 16:27 · [社区讨论](https://news.ycombinator.com/item?id=49157930)

**背景**: 大型语言模型（LLM）是在海量文本语料上训练的人工智能系统，在数学问题求解方面展现出新兴能力。在数学领域，研究者传统上依赖创造力和严谨的逻辑；如今 LLM 被用于生成潜在解并验证其正确性，使某些类型的证明探索变得更加容易。这一领域备受关注，因为数学是推理能力的清晰基准，这里的 AI 进展可能推广到其他科学领域。

**社区讨论**: 评论普遍持积极态度，有些人认为这是指数级的、变革性的进展。另一些人则提醒，AI 在提出猜想方面仍无法匹敌人类直觉，但它擅长否定假设。少数评论者附上了具体问题的直观解释链接，也有人担心一些数学家近年来的研究可能因此被颠覆。

**标签**: `#AI`, `#mathematics`, `#theoretical computer science`, `#LLM`, `#research`

---

<a id="item-3"></a>
## [开发工具必须开源：LLM 让这一理想更可行](https://blog.exe.dev/devtools-must-be-open-source) ⭐️ 8.0/10

exe.dev 博客上的一篇观点文章主张开发工具必须开源，认为 LLM 从根本上改变了修改和维护本地工具源代码的可行性。文章提出一种工作流：用户在 AI 帮助下直接修改代码，并通过夜间自动化任务将本地修改变基到上游更新之上。 这篇文章在 LLM 时代重新点燃了关于开源开发工具的长期争论，影响开发者如何定制编辑器、命令行工具和构建工具。维护者、工具厂商以及高级用户可能需要在配置系统与直接修改源码之间做出选择。 文章据称反对配置文件、选项和插件系统，主张让 LLM 修改硬编码值并重新构建工具。它还建议设置一个夜间 cron 任务：获取上游更改、将本地修改变基，并验证软件仍能正常工作。

hackernews · bryanmikaelian · 8月3日 14:15 · [社区讨论](https://news.ycombinator.com/item?id=49156111)

**背景**: 开源软件赋予用户检查和修改源代码的自由，但实际上很少有程序员有时间维护个人分支。LLM 降低了阅读和编辑陌生代码的成本，使直接修改源码有可能成为配置系统的现实替代方案。文章将这个想法专门应用于文本编辑器等开发工具——这类工具的传统定制方式一直依赖配置文件和插件。

**社区讨论**: 评论者总体上认同开源，但对激进提议持怀疑态度：simonw 认为 LLM 让“自由修改”这一原始理想更可行，而 kelnos 称用 LLM 重新构建替代配置/插件系统既低效又浪费。theamk 警告说，夜间 AI 驱动的变基是“地狱”，因为不可靠的行动者随时可能破坏正常运行的工作流；身为开发工具维护者的 lalitmaganti 则认为，考虑到真实的维护负担，这个愿景过于理想化。

**标签**: `#open source`, `#devtools`, `#LLM`, `#software engineering`, `#community discussion`

---

<a id="item-4"></a>
## [ComfyUI 首发支持 MiniMax H3：开放权重、原生音频与 2K 视频](https://blog.comfy.org/p/minimax-h3-day-0-support-in-comfyui) ⭐️ 8.0/10

ComfyUI 宣布对 MiniMax H3 提供首日支持，这是一款开放权重的全模态模型，能够生成带原生音频的 2K 视频。该集成实现了在消费级 GPU 上本地生成，并将内存占用从 123.6 GB 降至 42.5 GB。 此次发布是开放权重多模态 AI 的重要一步，创作者和研究人员无需依赖专有云端 API 即可在本地运行高质量视频与音频生成。它也标志着更小内存占用趋势的形成，使高级模型能够在 RTX 3060 等更易获得的硬件上运行。 该模型的调制权重（约占总参数的 40%）被剪枝并替换为功能等价的查找表，大幅缩减内存且据称不影响输出质量。动态 VRAM 卸载技术进一步使 2K 视频模型能够在 RTX 3060 等 GPU 上本地运行。

hackernews · vblanco · 8月3日 13:34 · [社区讨论](https://news.ycombinator.com/item?id=49155629)

**背景**: ComfyUI 是一个开源、基于节点的图形界面和后端，用于构建扩散模型工作流，被 AI 艺术创作者和开发者广泛用于生成图像、视频和音频。MiniMax H3 是上海 AI 公司 MiniMax Group 推出的全模态生成系统，支持对文本、图像、视频和音频的统一理解与生成。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/MiniMaxAI/MiniMax-H3">MiniMaxAI/ MiniMax - H 3 · Hugging Face</a></li>
<li><a href="https://en.wikipedia.org/wiki/MiniMax_Group">MiniMax Group</a></li>
<li><a href="https://github.com/comfy-org/comfyui">GitHub - Comfy-Org/ComfyUI: The most powerful and modular diffusion model GUI, api and backend with a graph/nodes interface. · GitHub</a></li>

</ul>
</details>

**社区讨论**: 社区评价总体积极，用户对输出质量和速度感到满意，但也有人指出在非常规或创意场景下仍存在不够流畅的问题。vblanco 在 4070 Ti Super 上生成 10 秒 480p 视频耗时 10 分钟，称效果惊艳；还有人对剪枝 40% 参数而无质量损失的做法表示怀疑，并思考该技术是否能应用于大语言模型。

**标签**: `#AI/ML`, `#Video Generation`, `#Open Weights`, `#ComfyUI`, `#MiniMax`

---

<a id="item-5"></a>
## [安迪·帕夫洛加入 ClickHouse，创立 ClickHouse 实验室](https://clickhouse.com/blog/andy-pavlo-joins-clickhouse) ⭐️ 8.0/10

知名数据库研究者、卡内基梅隆大学教授安迪·帕夫洛（Andy Pavlo）加入 ClickHouse，创立新的研究机构 ClickHouse 实验室。这一公告标志着学术界与领先的开源 OLAP 数据库公司之间的一次重要合作。 此举将学术数据库研究与顶尖商业 OLAP 数据库连接起来，有望加速列式存储、查询处理和实时分析等领域的创新。这也反映了数据库领域产学研合作的更广泛趋势，让真实世界挑战与前沿研究相结合。 ClickHouse 实验室预计将专注于推进 OLAP 数据库技术，但具体研究方向尚未公布。帕夫洛以在卡内基梅隆大学广受欢迎的数据库系统系列讲座而闻名，社区许多人希望该系列能以赞助形式继续。

hackernews · nikolay\_sivko · 8月3日 14:09 · [社区讨论](https://news.ycombinator.com/item?id=49156011)

**背景**: ClickHouse 是一个开源的面向列式存储的数据库管理系统，专为在线分析处理（OLAP）设计，可使用 SQL 实时生成分析报告。安迪·帕夫洛是卡内基梅隆大学专注数据库系统的教授，以数据库教学和研究闻名。此类合作是数据库公司设立研究实验室或与学术界合作以衔接理论与实践的日益增长趋势的一部分。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/ClickHouse">ClickHouse - Wikipedia</a></li>
<li><a href="https://clickhouse.com/">Fast Open-Source OLAP DBMS | ClickHouse</a></li>
<li><a href="https://en.wikipedia.org/wiki/Online_analytical_processing">Online analytical processing - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 社区反应积极，许多人向帕夫洛和 ClickHouse 表示祝贺。多位评论者称赞帕夫洛在 CMU 的系列讲座，并希望其继续；还有人建议 ClickHouse 可以资助学术数据库研究，另有人讨论了计算与存储分离以及 Trino 等 OLAP 引擎的行业趋势。

**标签**: `#databases`, `#clickhouse`, `#olap`, `#research`, `#industry-academia`

---

<a id="item-6"></a>
## [Jane Street 的 Bonsai：用 OCaml 构建 Web UI](https://github.com/janestreet/bonsai) ⭐️ 8.0/10

Jane Street 开源的 Bonsai 是一个基于 OCaml 的 UI 库，借助 js\_of\_ocaml 和受 Elm 启发的架构来构建动态 Web 应用。该项目近期在 Hacker News 上引发热议，获得了 292 分和 113 条评论。 它的意义在于让 OCaml 开发者在前端和后端使用同一种语言与类型系统，减少样板代码并提升安全性。这也表明函数式编程可以用于大规模生产级 UI——Jane Street 几乎所有内部 Web 应用都在使用 Bonsai，这可能影响 OCaml 社区在 ReasonML/Melange 等方案之间的选择。 Bonsai 基于 js\_of\_ocaml 构建，而不是绑定 React，因此在与 JavaScript 生态（如 React、GraphQL 客户端）互操作时会有取舍。它部分受 Elm 启发，采用增量计算来保证性能；有评论者认为默认样式不好看，但也承认性能很好。

hackernews · KolmogorovComp · 8月3日 08:29 · [社区讨论](https://news.ycombinator.com/item?id=49152842)

**背景**: Bonsai 是 Jane Street 内部开发的 UI 库，用于在 OCaml 中构建高性能、响应式的 Web 应用，覆盖从公司目录到监控工具等几乎所有内部 Web 应用。它通过 js\_of\_ocaml 把 OCaml 编译成 JavaScript，采用受 Elm 启发的架构，而不是像 Melange 那样提供 React 绑定。Jane Street 还曾在 Signals &amp; Threads 播客中专门介绍过这个框架。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/janestreet/bonsai">GitHub - janestreet/bonsai: A library for building dynamic webapps, using Js_of_ocaml · GitHub</a></li>
<li><a href="https://github.com/janestreet/bonsai_web">GitHub - janestreet/bonsai_web: A library for building dynamic webapps, using Js_of_ocaml · GitHub</a></li>
<li><a href="https://blog.janestreet.com/strace-ui-bonsai-term-and-the-tui-renaissance/">Jane Street Blog - strace-ui, Bonsai_term, and the TUI renaissance</a></li>

</ul>
</details>

**社区讨论**: 社区讨论整体积极，但也带有观望态度。有人询问 Bonsai 在 Jane Street 之外是否已用于生产环境，以及它与 Melange 相比有何优劣，尤其是会否牺牲 React 等 JS 生态；还有评论认为默认界面样式不好看，但性能不错。也有人推荐 Signals &amp; Threads 播客上关于该框架的深入介绍。

**标签**: `#OCaml`, `#UI framework`, `#functional programming`, `#Jane Street`, `#web development`

---

<a id="item-7"></a>
## [Kimi K3 架构深度解析：压缩记忆与潜在路由](https://newsletter.semianalysis.com/p/kimi-k3-the-manos-the-mythos-the) ⭐️ 8.0/10

这篇文章深入分析了 Kimi K3 的新颖架构，重点关注压缩记忆、深度间注意力和潜在专家路由，以及这些技术如何影响推理性能。 这一分析对 AI/ML 系统研究具有重要意义，因为它详细介绍了可能提升 LLM 推理效率和内存使用的新兴架构技术。理解这些方法可能有助于研究人员设计更高效的模型。 文章重点介绍了三项关键技术：压缩记忆以减少 KV 缓存开销、深度间注意力以捕捉跨层依赖，以及潜在专家路由以改善 MoE 负载均衡。这些创新旨在解决长上下文模型中的推理瓶颈。

rss · Semianalysis · 8月3日 19:42

**背景**: 大语言模型（LLM）使用注意力机制，需要存储键值（KV）缓存，这会占用大量内存。混合专家（MoE）架构每个 token 只激活部分参数，但依赖路由网络来选择专家。压缩记忆技术可以减小这些缓存的内存占用，而潜在专家路由则将专家重构到共享潜在空间中。这些方法属于当前提升 LLM 效率和可扩展性的研究热点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://arxiv.org/abs/2502.15443">[2502.15443] When Compression Meets Model Compression: Memory-Efficient Double Compression for Large Language Models</a></li>
<li><a href="https://arxiv.org/html/2506.21328v1">Latent Prototype Routing: Achieving Near-Perfect Load Balancing in Mixture-of-Experts Preprint - Work in Progress. Code: Here</a></li>

</ul>
</details>

**标签**: `#AI`, `#LLM`, `#architecture`, `#inference`, `#memory`

---

<a id="item-8"></a>
## [审稿人呼吁：论文不附可复现代码应直接拒稿](https://www.reddit.com/r/MachineLearning/comments/1vei12v/its_time_to_desk_reject_papers_that_dont_include/) ⭐️ 8.0/10

一位为三场机器学习顶会审稿的研究者报告称，12 篇论文中仅 1 篇提供了完整可复现代码，并建议对不提供代码的论文直接拒稿（desk reject）。 这一提议可能促使 ML 顶会强制执行代码提交政策，从而提升可复现性，减少因隐藏 bug 导致结果失效的问题。 在 5 篇提供部分代码的论文中，3 篇存在使结果失效的 bug，另有 7 篇未提供代码；作者认为当前激励机制反而惩罚公开代码，因为审稿人可能发现 bug。

reddit · r/MachineLearning · /u/Flaky-Ambition5900 · 8月3日 16:17

**背景**: Desk rejection 指稿件未经同行评审就直接被编辑拒稿，常见原因包括不符合期刊范围或未满足基本要求。AUROC 是 ML 论文中常用的指标，用于衡量模型区分正负样本的能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://authorservices.taylorandfrancis.com/blog/get-published/5-reasons-for-desk-rejection-and-how-to-avoid-them/">5 top reasons for desk rejection – and how to avoid them - Author Services</a></li>
<li><a href="https://www.letpub.com/How-to-Avoid-Desk-Rejection-in-Academic-Publishing">How to Avoid Desk Rejection in Academic Publishing - LetPub</a></li>
<li><a href="https://glassboxmedicine.com/2019/02/23/measuring-performance-auc-auroc/">Measuring Performance: AUC ( AUROC ) – Glass Box Medicine</a></li>

</ul>
</details>

**标签**: `#machine learning`, `#reproducibility`, `#research practices`, `#peer review`

---

<a id="item-9"></a>
## [DNA 分析设备漏洞或致 30 年法医证据面临篡改风险](https://www.wsj.com/tech/cybersecurity/security-flaw-placed-30-years-of-dna-evidence-at-risk-of-hacking-1932775a) ⭐️ 8.0/10

研究人员发现，美国多数犯罪实验室使用的 Thermo Fisher Scientific DNA 分析设备存在安全漏洞。他们借助 Anthropic 的 Claude 生成的 AI 代码，在大约 45 分钟内不留痕迹地修改了 DNA 扫描文件，促使 Thermo Fisher 于上周五发布了加入数字签名的补丁。 该漏洞可能危及约 30 年来刑事案件中使用的法医 DNA 证据，进而削弱公众对司法系统的信任。同时，它也暴露了法医实验室网络安全防护薄弱的现状，这些实验室缺乏统一监管，安全措施参差不齐。 该漏洞影响的是 Thermo Fisher 分析软件加载前的 .fsa 和 .hid 法医 DNA 文件，攻击者可在几乎不被察觉的情况下修改这些文件。Thermo Fisher 正与美国网络安全和基础设施安全局（CISA）协作，目前尚无该漏洞被实际利用的报告。

telegram · zaihuapd · 8月3日 05:15

**背景**: 犯罪实验室使用毛细管电泳仪等 DNA 分析设备生成电泳图谱文件，并将其与嫌疑人档案比对，这些数字文件在法庭上被当作证据使用。常规的法医分析软件不会用数字签名验证这些文件的完整性，因此容易遭受篡改。这正是 Thermo Fisher 新软件更新加入数字签名校验的原因，数字签名是确保数据真实性和完整性的常用机制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://suriq.io/blog/thermo-fisher-dna-file-tampering-cve-2026-17583">DNA analysis software flaw let evidence files be altered</a></li>
<li><a href="https://www.techtimes.com/articles/322771/20260803/ai-assisted-code-can-alter-forensic-dna-scan-files-without-any-detectable-trace.htm">AI-Assisted Code Can Alter Forensic DNA Scan Files Without Any...</a></li>
<li><a href="https://blog.cybernexora.com/dna-test-software-vulnerability/">DNA Test Software Vulnerability: Critical Evidence Risk</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#forensics`, `#DNA analysis`, `#vulnerability`, `#Thermo Fisher`

---

<a id="item-10"></a>
## [美至少 50 名警员被控滥用车牌摄像头窥探前任](https://www.washingtonpost.com/technology/2026/08/02/how-police-officers-used-vast-network-cameras-spy-their-exes/) ⭐️ 8.0/10

《华盛顿邮报》2026 年 8 月 2 日发布的调查发现，美国至少有 50 名执法人员被指控或起诉滥用 Flock 等自动车牌识别系统。其中 26 起案件涉及窥探妻子、女友、前任或心仪女性，46 起使用了 Flock 系统。 这项调查暴露了监控技术部署中存在的系统性监管漏洞，显示大规模数据采集很容易被变成个人跟踪工具。这给 Flock 等公司和各州立法机构施加了压力，要求他们实施更严格的访问控制和审计，也为更广泛的隐私争论添了一把火。 Flock 声称其在 6000 多个社区运营超过 12 万台摄像头，每月记录 200 亿次车牌扫描。该公司表示滥用行为很难完全避免，并推出了可选的「审计辅助」功能，而隐私倡导者指出，目前只有 13 个州要求审计，至少 8 个州将滥用定为犯罪。

telegram · zaihuapd · 8月3日 09:03

**背景**: 自动车牌识别（ALPR）系统利用摄像头和软件来捕获并存储车牌号码和位置信息，通常无需搜查令。Flock Safety 是这类系统的主要私人供应商，向社区和警察局销售联网摄像头，并在不同辖区之间共享数据。由于系统持续记录数百万个车牌，形成了可搜索的车辆行踪数据库，拥有权限的员工可能会滥用这些数据。该调查凸显了在犯罪调查效率与隐私保护、监管之间取得平衡的难度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Flock_Safety">Flock Safety - Wikipedia</a></li>
<li><a href="https://sls.eff.org/technologies/automated-license-plate-readers-alprs">Automated License Plate Readers</a></li>

</ul>
</details>

**标签**: `#privacy`, `#surveillance`, `#law enforcement`, `#license plate cameras`, `#ethics`

---

<a id="item-11"></a>
## [英伟达 170HX 矿卡破解：解锁 80GB 显存，二手价暴涨](https://finance.sina.com.cn/tech/roll/2026-08-03/doc-inikzqsf4659769.shtml) ⭐️ 8.0/10

亚利桑那州立大学研究人员公开了英伟达 CMP 170HX 矿卡的破解方案，通过 GPU 安全协处理器的栈溢出漏洞绕过 OTP 熔丝锁定，将显存解锁至最高 80GB，FP32 算力从 0.39 TFLOPS 暴增至 94 TFLOPS。消息传出后，该卡二手价从 300–500 元飙升至 3000–4000 元，海外叫价甚至达到 1500 美元。 这一破解意义重大：它将一块廉价矿卡变成高显存 AI 加速器，让本地大语言模型推理和 AI 图像生成的门槛大幅降低。同时，它也暴露了英伟达 GPU 安全协处理器中的严重漏洞，动摇了基于 OTP 熔丝的硬件锁信任，可能影响二手 GPU 市场。 该漏洞是 Falcon 安全协处理器中的 DMA 无界溢出，可劫持权限并逐一修改寄存器来解除显存与算力限制。国内社区已跟进验证，解锁卡可在 Windows 和 Linux 下运行 AI 图像生成及大语言模型推理，但长期稳定性和不同批次的解锁上限仍存风险。

telegram · zaihuapd · 8月3日 11:29

**背景**: CMP 170HX 是英伟达 2021 年推出的专用加密货币矿卡，搭载与 A100 数据中心 GPU 相同的 GA100 核心，但出厂时通过 OTP 熔丝永久限制了 PCIe 带宽、显存和算力，使其无法用于通用计算。OTP（一次性可编程）熔丝是一种物理硬件锁，正常情况下不可逆转。Falcon 协处理器是负责固件管理与可信执行的安全处理器，本次发现的漏洞让研究人员得以绕过这些保护。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://kentino.com/products/nvidia-cmp-170hx-64-gb-hbm2e-modified-ex-mining">NVIDIA CMP 170 HX 64 GB HBM2e (Modified, Ex- Mining ) – Kentino</a></li>
<li><a href="https://electronics.stackexchange.com/questions/455756/how-are-otp-fuses-in-ics-implemented">integrated circuit - How are OTP fuses in ICs implemented? - Electrical...</a></li>

</ul>
</details>

**标签**: `#GPU`, `#hardware security`, `#NVIDIA`, `#AI inference`, `#exploit`

---

<a id="item-12"></a>
## [苹果就英国政府 iCloud 后门要求提起法律诉讼](https://www.ft.com/content/2cc9c96a-0e5b-4c33-a95a-3d11072a145c?syn-25a6b1a6=1) ⭐️ 8.0/10

苹果已向英国调查权力法庭提起法律申诉，挑战政府要求其提供英国用户 iCloud 加密备份访问能力的技术能力通知。该申诉质疑政府签发此类通知的权力。 此案可能为政府强制科技公司设置加密后门确立重要先例，直接影响用户隐私与全球加密标准。此前苹果已在英国下架高级数据保护功能，显示科技企业与政府之间的冲突正在升级。 该技术能力通知依据英国《2016 年调查权力法》签发，要求苹果维持或开发访问 iCloud 备份的技术能力。苹果于 2025 年 2 月在英国停用了高级数据保护功能；法庭已定于下月举行案件管理听证，隐私组织也已提出类似申诉。

telegram · zaihuapd · 8月3日 15:40

**背景**: iCloud 高级数据保护功能为大多数 iCloud 数据提供端到端加密，使苹果无法访问用户内容。英国法律下的技术能力通知强制服务提供商构建监控能力。调查权力法庭是英国专门审理公共机构监控投诉的特别法庭。苹果一直主张任何后门都会削弱所有用户的系统安全性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Investigatory_Powers_Tribunal">Investigatory Powers Tribunal</a></li>
<li><a href="https://factually.co/fact-checks/technology/uk-technical-capability-notice-to-apple-demands-legal-challenges-f8051c">What exactly did the UK Technical Capability Notice to...</a></li>
<li><a href="https://support.apple.com/en-us/102651">iCloud data security overview - Apple Support</a></li>

</ul>
</details>

**标签**: `#Apple`, `#Encryption`, `#Privacy`, `#UK Government`, `#Legal`

---