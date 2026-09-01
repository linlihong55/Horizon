---
layout: default
title: "Horizon Summary: 2026-09-01 (ZH)"
date: 2026-09-01
lang: zh
---

> 从 37 条内容中筛选出 8 条重要资讯。

---

1. [谷歌从 Chrome 网上应用店移除 MV2 扩展，uBlock Origin 受影响](#item-1) ⭐️ 8.0/10
2. [ChatGPT Work 工具与技能参考网站引发社区热议](#item-2) ⭐️ 8.0/10
3. [NAT 被称为互联网中心化的“原罪”](#item-3) ⭐️ 8.0/10
4. [滑动窗口注意力在长上下文推理上胜过线性注意力](#item-4) ⭐️ 8.0/10
5. [GNN 时间泄漏问题暴露：SynthFin-AML 基准强制因果时间划分](#item-5) ⭐️ 8.0/10
6. [库克卸任苹果 CEO，特努斯接棒聚焦 AI](#item-6) ⭐️ 8.0/10
7. [DeepSeek 发布实验性多模态模型 V4-Flash-Vision-Exp 权重](#item-7) ⭐️ 8.0/10
8. [欧盟将 ChatGPT、Reddit、Roblox 认定为超大型服务，面临更严数字监管](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [谷歌从 Chrome 网上应用店移除 MV2 扩展，uBlock Origin 受影响](https://webiterate.dev/google-removed-extensions-ublock-origin-108/) ⭐️ 8.0/10

谷歌已将 Manifest V2（MV2）扩展从 Chrome 网上应用店中移除，包括 uBlock Origin，并开始在 Chrome 稳定版中禁用已安装的 MV2 扩展。这迫使用户转向内容过滤能力更受限的 Manifest V3（MV3）替代方案。 这是一项影响 Chrome 用户的重大平台变革，许多用户依赖广告拦截器保护隐私和安全。由于 MV3 的限制削弱了广告拦截能力，用户可能更容易遭遇恶意广告，部分用户可能会转向 Firefox 等其他浏览器。 MV3 用 declarativeNetRequest 取代了可拦截请求的 webRequest API，这限制了过滤规则数量并制约了动态请求拦截。广泛使用的开源拦截器 uBlock Origin 已公开批评这些限制，AdGuard 符合 MV3 的实验性拦截器在新规则下也面临困难。

hackernews · twapi · 8月31日 21:10 · [社区讨论](https://news.ycombinator.com/item?id=49514878)

**背景**: Manifest V2 长期以来是 Chrome 扩展所使用的扩展规范，uBlock Origin 是一款基于该规范拦截广告和跟踪器的免费开源内容拦截器。谷歌推出 MV3 声称为了提升安全性和性能，但 MV3 对 webRequest 的限制严重削弱了传统广告拦截技术。从 Chrome 网上应用店下架 MV2 扩展，是谷歌计划在 2025 年 6 月前淘汰 MV2 的一部分。Firefox 仍支持 MV2，用户如果想继续使用功能完整的 uBlock Origin，可以选择 Firefox。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/UBlock_Origin">uBlock Origin - Wikipedia</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/adguard-s-new-ad-blocker-struggles-with-google-s-manifest-v3-rules/">AdGuard’s new ad blocker struggles with Google’s Manifest v 3 rules</a></li>
<li><a href="https://tegufy.com/news/chrome-manifest-v3-kills-ad-blockers-june-2026">Chrome Manifest V 3 Is Finally Killing Ad Blockers — Here&#x27;s What...</a></li>

</ul>
</details>

**社区讨论**: 评论者强烈批评这一决定，认为广告拦截是安全必需品；一位用户提到年长的家人容易被恶意广告欺骗并安装诈骗软件。许多人建议改用 Firefox，称 uBlock Origin 在该浏览器上一直表现最佳。还有更广泛的情绪是对谷歌单方面控制互联网的不满，以及对 Chrome 早期良好声誉的怀念。

**标签**: `#Chrome`, `#Manifest V2`, `#ad-blocking`, `#browser extensions`, `#privacy`

---

<a id="item-2"></a>
## [ChatGPT Work 工具与技能参考网站引发社区热议](https://codex-tool-reference.simonw.chatgpt.site/) ⭐️ 8.0/10

一个新的参考网站\(codex-tool-reference.simonw.chatgpt.site\)收录了 ChatGPT Work 的工具与技能，其中包括一个引人注目的浏览器控制技能，可通过 Node.js 驱动 Playwright 实例。该网站在 Hacker News 上引发了活跃讨论，Simon Willison 特别提到了其浏览器控制方案。 这件事很重要，因为它整理并记录了可复用的 ChatGPT Work 技能——这是一种通过可编程工作流扩展 AI 助手的新方式。开发者对浏览器自动化的关注表明，人们希望从只能聊天的助手，转向能够与实时网页互动的智能体。 该浏览器控制技能指示 ChatGPT Work 通过其 Node.js REPL 启动 Playwright 实例，并运行 \`nodeRepl.write\(await browser.documentation\(\)\)\` 以获取进一步的使用说明。社区成员指出，有些 work 工具可能会拖慢响应并浪费大量 token，同时也质疑它与本就能完成类似操作的 Codex 有何区别。

hackernews · ijidak · 8月31日 14:07 · [社区讨论](https://news.ycombinator.com/item?id=49510000)

**背景**: ChatGPT Work 工具与技能是可供复用、共享的工作流，能让 ChatGPT 更稳定地完成特定任务；一个技能可以包含指令、示例和代码。Playwright 是微软推出的浏览器自动化库，用于测试和自动化网页浏览器，与 Selenium、Puppeteer 等工具竞争。该参考网站对这些技能进行了整理，方便开发者发现并复用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://help.openai.com/en/articles/20001066-skills-in-chatgpt">Skills in ChatGPT | OpenAI Help Center</a></li>
<li><a href="https://thecodeforge.io/python/playwright-python/">Playwright Python — Auto-wait Doesn&#x27;t Wait for... | TheCodeForge</a></li>

</ul>
</details>

**社区讨论**: Simon Willison 认为控制浏览器这一技能最有趣，并附上了相关文档与生成提示的链接。其他评论者则提出了 token 浪费和响应变慢等实际担忧，并询问这与 Codex 有何不同。还有一条元评论指出，AI 生成的网站往往具有相似的视觉风格。

**标签**: `#ChatGPT`, `#AI tools`, `#browser automation`, `#Playwright`, `#developer tools`

---

<a id="item-3"></a>
## [NAT 被称为互联网中心化的“原罪”](https://dreamstation.systems/personal/ntppost.html) ⭐️ 8.0/10

一篇散文认为，NAT（网络地址转换）通过让人们更难运行公共服务器，成为互联网中心化最早的推手之一。Linux 当前 NAT 系统的实现者 Rusty Russell 加入讨论并承认了他当时所做的权衡取舍，使这一讨论更具分量。 这一论点将一种日常网络技术重新定义为塑造当今以云为中心、客户端/服务器式互联网的结构性力量。它为工程师和历史学家提供了一个具体视角，帮助理解开放、对等互联网如何让位于中心化平台。 Rusty Russell 解释说，他当时避免端口预留，而倾向于只要远程地址允许区分，就把更多连接压缩进一个 IP 地址，这使得来自不同地址的入站流量无法路由。另一位评论者则认为，普通 NAT 可以接受，真正有害的是运营商级 NAT（CGNAT）。

hackernews · robinpie · 8月31日 02:23 · [社区讨论](https://news.ycombinator.com/item?id=49504905)

**背景**: 网络地址转换（NAT）为了应对 IPv4 地址枯竭而被广泛采用，它允许多个私有地址共享一个公共 IPv4 地址。它违背了端到端原则——该原则要求应用相关的功能应在端节点实现，而不是在网络内部实现。运营商级 NAT 将同样的转换推入 ISP 的基础设施中，造成了更深层次的服务共享与控制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/End-to-end_principle">End-to-end principle - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Carrier-grade_NAT">Carrier-grade NAT</a></li>

</ul>
</details>

**社区讨论**: 评论者的观点出现分歧：有人认为 NAT 让用户习惯了客户端—服务器模式是“自然的”，也有人认为“原罪”是夸大其词，并指出家庭网关的体验问题以及 CGNAT 的危害更大。Rusty Russell 给出了一个细致的辩护，表示他当时是解决具体问题的年轻工程师，但也承认 NAT 削弱了运行服务器的能力。另一位评论者则将根因归结为把现实世界规范套用到网络空间这一更根本的错误。

**标签**: `#NAT`, `#networking`, `#internet history`, `#centralization`, `#sysadmin`

---

<a id="item-4"></a>
## [滑动窗口注意力在长上下文推理上胜过线性注意力](https://www.reddit.com/r/MachineLearning/comments/1w3j1vw/slidingwindow_attention_beats_linear_on/) ⭐️ 8.0/10

Alexia Jolicoeur-Martineau 等人发布的新 arXiv 预印本指出，带注意力汇（sinks）的滑动窗口注意力在 Needle-in-a-Haystack 和 BABILong 等长上下文推理基准上，性能比线性注意力变体高 2 到 10 倍。作者建议改用这种更简单的基线，而不是后训练线性模型。 这一发现挑战了线性注意力这一重要研究方向，表明它可能没有与更简单的基线进行充分对比。这可能会让大语言模型效率研究重新关注滑动窗口注意力这类简单有效的方案。 论文特别点名 Needle-in-a-Haystack 和 BABILong 两个基准，认为差距很大且并不接近。作者承认线性注意力可能有一定潜力，但认为它可能需要从头训练或大量后训练才能赶上 SWA。

reddit · r/MachineLearning · /u/Justgototheeffinmoon · 8月31日 16:35

**背景**: 标准自注意力的复杂度随序列长度呈二次增长，导致长上下文处理成本很高。线性注意力变体试图通过近似或循环形式把复杂度降到线性，而滑动窗口注意力只是让每个 token 关注一个固定的局部窗口，同样能达到 O\(n\) 复杂度，Mistral 和 Longformer 等模型都采用了这种方法。注意力汇指在滑动窗口中保留早期 token 以稳定生成，因为一旦把位置 0 移除，输出质量会迅速下降。BABILong 是专门用于测试模型在超长文档中跨事实推理能力的基准。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2406.10149">BABILong: Testing the Limits of LLMs with Long Context Reasoning-in-a ...</a></li>
<li><a href="https://www.abhik.ai/concepts/transformers/sliding-window-attention">Sliding Window Attention | Abhik Sarkar</a></li>
<li><a href="https://mbrenndoerfer.com/writing/attention-sinks-streamingllm-infinite-generation">Attention Sinks and StreamingLLM for Long Generation - Interactive</a></li>

</ul>
</details>

**标签**: `#attention`, `#LLM`, `#long-context`, `#sliding-window`, `#linear-attention`

---

<a id="item-5"></a>
## [GNN 时间泄漏问题暴露：SynthFin-AML 基准强制因果时间划分](https://www.reddit.com/r/MachineLearning/comments/1w3imxy/your_gnn_is_probably_just_an_overcomplicated_mlp/) ⭐️ 8.0/10

这篇 Reddit 帖子发布了 SynthFin-AML v10.0，一个旨在消除 GNN 评估中时间泄漏的动态图基准。它表明在使用严格因果时间划分时，GraphSAGE（PR-AUC 0.881）仅略微优于调优的 LightGBM（0.848）。 这项工作揭露了动态 GNN 评估中一个关键缺陷——时间泄漏，它可能导致性能虚高和误导性的结论。通过强制因果边界，SynthFin-AML 为反洗钱和其他时序图应用提供了更严格的评估标准。 该数据集包含 10 万个节点和 120 万条边，采用 3 快照时点划分：训练边截至第 7 天，验证边截至第 8 天，测试边截至第 10 天。它还通过让欺诈和正常零售交易金额共享相同的对数正态分布（μ=8.517, σ=0.8）来修复表格泄漏。

reddit · r/MachineLearning · /u/Glabmayt2075 · 8月31日 16:21

**背景**: 图神经网络中的时间泄漏指模型在动态图的静态快照上训练时，可以看到未来的边，从而违反因果性。标准的转导随机划分不尊重时间方向，可能夸大结果。该帖子认为，使用时点图特征的 LightGBM 等树模型是强基线，GNN 必须通过基于时间的严格划分来证明其价值。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://kumo.ai/pyg/concepts/data-leakage/">Data Leakage in Graph ML: When Future Information Contaminates Training | Kumo.ai | Kumo.ai</a></li>
<li><a href="https://towardsdatascience.com/no-peeking-ahead-time-aware-graph-fraud-detection/">No Peeking Ahead: Time-Aware Graph Fraud Detection | Towards Data Science</a></li>
<li><a href="https://github.com/valiyevoktay-cmd/synthfin-aml-">GitHub - valiyevoktay-cmd/ synthfin - aml -: A graph-native Anti - Money ...</a></li>

</ul>
</details>

**标签**: `#GNN`, `#temporal leakage`, `#dynamic graphs`, `#benchmark`, `#anti-money laundering`

---

<a id="item-6"></a>
## [库克卸任苹果 CEO，特努斯接棒聚焦 AI](https://www.bloomberg.com/news/articles/2026-08-30/apple-s-new-ceo-john-ternus-takes-reins-from-tim-cook-focusing-on-ai) ⭐️ 8.0/10

蒂姆·库克于 2026 年 8 月 31 日卸任苹果 CEO，硬件工程老将约翰·特努斯于 9 月 1 日接任。新任 CEO 的首要任务是推进 AI 落地，苹果首款折叠屏 iPhone 预计于 9 月 9 日的秋季发布会上亮相。 此次 CEO 更替标志着苹果战略重心转向 AI，将影响其整个生态系统的产品方向。预计发布的折叠屏 iPhone 也意味着苹果首次进入快速增长的折叠屏设备市场。 现年 51 岁的特努斯此前负责硬件工程，库克将继续担任执行主席。9 月 9 日亮相的折叠屏 iPhone 据称配备 12GB RAM，并深度植入 Siri AI，可结合屏幕、日历与相机理解现实场景，以弥补 Siri 升级延期的问题。

telegram · zaihuapd · 8月31日 10:21

**背景**: 折叠屏手机依靠柔性 OLED 显示屏和铰链机构，使同一台设备能在手机与平板尺寸之间切换；目前市场分为横向折叠和竖向折叠两大类，但折痕、耐用性和重量问题使其尚未普及。Siri AI 是苹果 Apple Intelligence 设备端 AI 功能套件的一部分，仅支持 iPhone 15 Pro 及更新机型；苹果已确认将由 Google Gemini 为 Siri 提供 AI 核心能力。这些背景有助于理解新 CEO 推动 AI 落地以及折叠屏 iPhone 的功能定位。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://36kr.com/p/2789794675546496">5年了， 折 叠 屏 为 什 么 还 是 没能普及？ -36氪</a></li>
<li><a href="https://www.tmtpost.com/6070018.html">折 叠 屏 不 是 主力 机 的未来-钛媒体官方网站</a></li>
<li><a href="https://iphonenews.cc/2026/02/02/apple-siri-gemini-ai-privacy-strategy/">Apple 為何選擇 Google Gemini？ Siri AI 升 級背後的真相</a></li>

</ul>
</details>

**标签**: `#Apple`, `#CEO transition`, `#AI`, `#Tim Cook`, `#John Ternus`

---

<a id="item-7"></a>
## [DeepSeek 发布实验性多模态模型 V4-Flash-Vision-Exp 权重](https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash-Vision-Exp) ⭐️ 8.0/10

DeepSeek 发布了 DeepSeek-V4-Flash-Vision-Exp 的权重，这是一款在 V4-Flash 架构上加入视觉模块并继续训练的实验性多模态模型。其 ApexBench 分数从 26.2 跃升至 36.5，多模态 agent 性能显著提升。 此次发布意义重大，表明 DeepSeek 在多模态 agent 能力这一关键 AI 竞争领域取得了快速进展。基准测试的大幅提升说明面向 agent 的模型正在快速改进，并将影响依赖开源权重模型的开发者和研究人员。 该模型为实验性质，基于 V4-Flash 构建，与之前的 V4-Flash-0731 相比，文本 agent 任务表现基本持平。ApexBench 评估采用 Pass@1 分数，此次发布除基准结果外缺少详细的技术分析。

telegram · zaihuapd · 8月31日 11:41

**背景**: 多模态 AI 模型能在相互关联的任务中处理并生成多种类型的信息，例如文本、图像、音频和视频。ApexBench 是一个多模态 agent 基准，用于评估复杂的 agent 任务，DeepSeek 的视觉模型发布会在其上报告 Pass@1 分数。此次发布延续了 DeepSeek 开放权重模型的模式，在多模态性能上与 OpenAI 和 Anthropic 等实验室展开竞争。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.datalearner.com/en/benchmarks/apexbench">ApexBench : Multimodal Agent Benchmark and... | DataLearnerAI</a></li>
<li><a href="https://www.emergentmind.com/topics/apex-bench">APEX - Bench : High-Fidelity Benchmarking</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#multimodal`, `#AI`, `#model-release`

---

<a id="item-8"></a>
## [欧盟将 ChatGPT、Reddit、Roblox 认定为超大型服务，面临更严数字监管](https://www.euronews.com/next/2026/08/31/eu-places-chatgpt-reddit-and-roblox-under-strictest-digital-safety-rules) ⭐️ 8.0/10

2026 年 8 月 31 日，欧盟委员会依据《数字服务法》将 ChatGPT 认定为超大型在线搜索引擎，并将 Reddit 和 Roblox 列为超大型在线平台。这三项服务现在面临更严格的欧盟数字安全与透明度规则。 这是 AI 聊天机器人首次被认定为超大型在线搜索引擎，为欧盟数字监管下的人工智能服务开创了先例。该认定给大型平台带来了重大合规负担，影响数以亿计的欧盟用户在内容审核、风险管理和数据透明度方面的体验。 这三项服务在欧盟的月均活跃用户均超过《数字服务法》规定的 4500 万人门槛。它们有四个月过渡期，须开展年度系统性风险评估、接受独立审计，并向监管机构和经审核的研究人员共享涉及非法内容、未成年人保护和用户身心健康的数据。

telegram · zaihuapd · 8月31日 14:39

**背景**: 《数字服务法》是欧盟具有里程碑意义的法规，为在线中介服务建立了分级义务体系。超大型在线平台和超大型在线搜索引擎——即欧盟月活用户超过 4500 万的服务——需要遵守最严格的风险管理、透明度和问责要求。该认定工作仍在继续，欧盟委员会还会评估其他大型服务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Digital_Services_Act">Digital Services Act - Wikipedia</a></li>
<li><a href="https://digital-strategy.ec.europa.eu/en/policies/digital-services-act">The Digital Services Act | Shaping Europe’s digital future</a></li>
<li><a href="https://digital-strategy.ec.europa.eu/en/policies/dsa-vlops">DSA: Very large online platforms and search engines | Shaping Europe’s digital future</a></li>

</ul>
</details>

**标签**: `#EU`, `#Digital Services Act`, `#regulation`, `#ChatGPT`, `#Reddit`

---