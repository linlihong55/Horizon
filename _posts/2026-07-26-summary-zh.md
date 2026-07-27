---
layout: default
title: "Horizon Summary: 2026-07-26 (ZH)"
date: 2026-07-26
lang: zh
---

> 从 31 条内容中筛选出 11 条重要资讯。

---

1. [GrapheneOS 保护锁定设备免受数据提取](#item-1) ⭐️ 8.0/10
2. [欧盟提议浏览器级隐私设置取代 Cookie 横幅](#item-2) ⭐️ 8.0/10
3. [将细节委托给 AI 可能并不赋能](#item-3) ⭐️ 8.0/10
4. [LLM Token 转售市场：聚合 API 与欺诈](#item-4) ⭐️ 8.0/10
5. [从头用 ARM64 汇编实现 YOLO26n 推理](#item-5) ⭐️ 8.0/10
6. [小规模 4B 开放权重模型在瑞典医学问答中达到 o3 级水平](#item-6) ⭐️ 8.0/10
7. [LLM 在 IMO 2026 基准测试：前沿模型接近满分](#item-7) ⭐️ 8.0/10
8. [DeepSeek 因创始人言论泄露暂停新一轮融资](#item-8) ⭐️ 8.0/10
9. [长鑫科技登陆上交所，有望成 A 股市值最高公司](#item-9) ⭐️ 8.0/10
10. [Claude 共享链接被搜索引擎索引，用户隐私泄露](#item-10) ⭐️ 8.0/10
11. [SpaceX 拒接 2028 年后猎鹰 9 订单，全力押注星舰](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [GrapheneOS 保护锁定设备免受数据提取](https://discuss.grapheneos.org/d/40700-grapheneos-protections-against-data-extraction-from-locked-devices) ⭐️ 8.0/10

GrapheneOS 实施了强大的保护措施，防止从锁定设备中提取数据，其中包括一项自动重启功能，可在设备闲置 18 小时后将其恢复到首次解锁前（BFU）模式。 这极大地增强了用户隐私和安全性，尤其是对记者、活动人士以及面临设备扣押风险的个人，通过确保在设备锁定时加密密钥不可访问。 自动重启到 BFU 模式与 PIN 熵分析及其他强化措施相辅相成，使 GrapheneOS 成为目前最安全的移动操作系统之一。

hackernews · Cider9986 · 7月26日 05:57 · [社区讨论](https://news.ycombinator.com/item?id=49055169)

**背景**: 首次解锁前（BFU）是指设备已关机或重启后尚未解锁的状态；在此状态下，所有数据保持加密且不可访问。GrapheneOS 是一个基于 Android 的开源操作系统，专注于安全与隐私，具有沙盒化 Google 服务和攻击面减少等功能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GrapheneOS">GrapheneOS</a></li>
<li><a href="https://blogs.dsu.edu/digforce/2023/08/23/bfu-and-afu-lock-states/">BFU and AFU Lock States – Blog | DigForCE Lab - DSU</a></li>

</ul>
</details>

**社区讨论**: 评论者指出这些功能可与苹果的产品相媲美，一些人称赞 GrapheneOS 即使在没有胁迫密码的情况下也能提供强力保护。其他人讨论了不同锁定方法的熵以及需要完整的备份解决方案，以便在过境前安全擦除设备。

**标签**: `#security`, `#mobile`, `#grapheneos`, `#privacy`, `#android`

---

<a id="item-2"></a>
## [欧盟提议浏览器级隐私设置取代 Cookie 横幅](https://killthecookiebanner.eu/) ⭐️ 8.0/10

欧盟委员会提出一项新法规，允许用户直接在浏览器中设置隐私偏好，从而消除在每个网站上重复出现的 Cookie 同意横幅。 这可以大幅改善用户体验，减少侵入性弹窗，并可能为隐私同意设定一个全球标准，简化网站的合规要求。 该提案仍需欧盟机构正式通过。它基于 Chrome 和 Edge 等现有浏览器设置，但旨在使其在 GDPR 下具有法律约束力的同意效力。

hackernews · rapnie · 7月26日 11:53 · [社区讨论](https://news.ycombinator.com/item?id=49057175)

**背景**: Cookie 横幅是欧盟《电子隐私指令》和 GDPR 的产物，要求网站在放置非必要 Cookie 前获得用户同意。然而，许多用户觉得这些横幅很烦人，常常不阅读就点击。拟议的解决方案将允许用户在浏览器中设置全局偏好，网站必须遵守该偏好。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://support.microsoft.com/en-us/edge/adjust-privacy-settings-in-microsoft-edge">Adjust privacy settings in Microsoft Edge</a></li>
<li><a href="https://secureprivacy.ai/blog/cookie-consent-automation">Cookie Consent Automation: A Complete Guide for Businesses | Secure Privacy Blog</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了不同看法：一些人支持这个想法，但建议直接让所有非必要 Cookie 非法，另一些人指出加州已经在实施类似方法。还有少数人认为真正的解决方案是彻底停止追踪。

**标签**: `#privacy`, `#cookie banners`, `#EU regulation`, `#web standards`, `#user experience`

---

<a id="item-3"></a>
## [将细节委托给 AI 可能并不赋能](https://davidnicholaswilliams.com/its-not-empowering-to-hand-off-the-details/) ⭐️ 8.0/10

David Nicholas Williams 认为，将细节交给 AI 会降低个人的理解与控制力，对“委托即赋能”的观点提出质疑。 这场辩论凸显了 AI 辅助开发中的一个关键矛盾：效率提升与深层知识流失之间的权衡，影响开发者技能成长和代码质量。 作者聚焦于“委托细节”（而非仅委托任务），认为这会导致理解肤浅；评论区指出，验证可以在不完全理解的情况下进行。

hackernews · davnicwil · 7月26日 17:58 · [社区讨论](https://news.ycombinator.com/item?id=49060592)

**背景**: “Vibecoding”指松散地指导 AI 生成代码而不深入参与。该文章切入关于开发者应多大程度依赖 AI、保留多少动手经验的持续讨论。

**社区讨论**: 评论区意见不一：有人赞同委托细节会削弱自主性（如 RGS1811 对 AI 输出的厌倦），也有人认为这带来解放（如 chungusamongus 用 AI 进行游戏开发）。讨论强调需判断哪些细节应保留或委托。

**标签**: `#AI-assisted coding`, `#developer productivity`, `#software engineering`, `#knowledge work`, `#delegation`

---

<a id="item-4"></a>
## [LLM Token 转售市场：聚合 API 与欺诈](https://simonwillison.net/2026/Jul/26/relay-market/#atom-everything) ⭐️ 8.0/10

Matt Lenhard 的一项调查揭示了一个转售市场：转售商通过聚合多种来源的 API 密钥，包括滥用免费试用和盗用信用卡，提供打折的 LLM Token 服务，该市场主要在中国运营，并使用 one-api 和 new-api 等开源代理工具。 这突显了 LLM 生态系统中一个重大的安全和欺诈问题：滥用者可以通过未受保护的端点获利，导致合法 API 用户和供应商面临巨额 Token 账单。这强调了 LLM 提供商需要更好的 API 密钥限额和监控。 所使用的代理软件 one-api 及其分支 new-api 是合法的开源 API 代理产品，旨在跨多个 API 凭证进行负载均衡。买家寻求低价 Token、绕过地域限制或收集数据用于模型蒸馏。

rss · Simon Willison · 7月26日 19:30

**背景**: LLM Token 是语言模型处理文本的计量单位，API 密钥按 Token 计费提供模型访问权限。转售商创建代理服务，聚合大量通常通过非法手段获得的 API 密钥，以提供折扣费率。开源工具 one-api 和 new-api 允许用户轻松设置此类代理，但可能被滥用于欺诈活动。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/songquanpeng/one-api/blob/main/README.en.md">one-api/README.en.md at main · songquanpeng/one-api</a></li>

</ul>
</details>

**标签**: `#LLM`, `#security`, `#fraud`, `#API`, `#AI`

---

<a id="item-5"></a>
## [从头用 ARM64 汇编实现 YOLO26n 推理](https://www.reddit.com/r/MachineLearning/comments/1v6w394/i_implemented_the_yolo26n_model_inference_from/) ⭐️ 8.0/10

一个本科毕业设计项目完全从零开始，使用 ARM64 汇编语言和 C 语言实现了 YOLO26n 目标检测推理，不依赖任何现有深度学习框架。该实现包含了 NEON SIMD、Winograd 卷积、缓存感知分块和自定义 ARM64 微内核等高级优化技术。 该项目展示了低层系统编程和神经网络优化的深刻理解，这对在树莓派等边缘设备上部署高效 AI 至关重要。它表明即使没有大型框架，通过精心手动优化也能实现功能性的推理，从而推动边缘 AI 性能的极限。 该实现包括自定义二进制格式的模型参数、算子融合、注意力机制以及 YOLO26n 的所有组件（Conv、C3K2、SPPF、C2PSA、PSA、BottleNeck、Detect）。性能提升低于预期，表明针对 ARM NEON 和内存层次结构进行优化的复杂性。

reddit · r/MachineLearning · /u/Forward\_Confusion902 · 7月26日 06:43

**背景**: YOLO（You Only Look Once）是一个流行的实时目标检测模型家族，YOLO26n 是最新的针对边缘设备优化的纳米版本。Winograd 卷积是一种快速算法，可减少卷积层中的乘法次数，而 NEON SIMD（单指令多数据）允许在 ARM 处理器上进行并行处理。C2PSA 是 YOLO26n 中使用的双分支注意力模块，用于增强小目标的特征提取。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://platform.ultralytics.com/ultralytics/yolo26">YOLO 26 Models by Ultralytics</a></li>
<li><a href="https://arxiv.org/abs/2201.10369">[2201.10369] Winograd Convolution for Deep Neural Networks: Efficient ...</a></li>
<li><a href="https://www.emergentmind.com/topics/c2psa-module">C2PSA Module: Dual-Branch Attention</a></li>

</ul>
</details>

**标签**: `#ARM64`, `#YOLO`, `#Edge AI`, `#Optimization`, `#Assembly`

---

<a id="item-6"></a>
## [小规模 4B 开放权重模型在瑞典医学问答中达到 o3 级水平](https://www.reddit.com/r/MachineLearning/comments/1v71wds/openweight_4b_models_approach_o3level_medical/) ⭐️ 8.0/10

该帖子展示，开放权重的 4B 模型（特别是启用了推理的 Qwen3.5-4B）在 MedQA-SWE 瑞典医学执照考试数据集上达到了 87%的准确率，接近 OpenAI o3 模型的 88%。作者使用了基于往年考试数据的监督微调（SFT）以及一种提前退出思考干预来防止推理循环。 这一结果表明，小型开放权重模型可以在特定领域的医学问答上与大型专有系统匹敌，从而降低了在低资源语言中应用临床 AI 的门槛。它突显了监督微调和推理干预等后训练技术在提升小型模型性能方面的有效性。 最佳结果（87%）由 Qwen3.5-4B 结合推理和提前退出干预实现，该干预限制思考轨迹长度，防止重复循环。无后训练时，Qwen3.5-4B 已得 77%，而旧的 MedGemma-1.5-4B 经过微调后仅达 60%。

reddit · r/MachineLearning · /u/AccomplishedCat4770 · 7月26日 11:58

**背景**: MedQA-SWE 是一个瑞典语的多选题临床问答数据集，包含来自外国医生考试的 3180 道题。提前退出干预受 S-GRPO 强化学习论文启发，通过注入短语在预定长度关闭思考轨迹。小型语言模型（4B 参数）因计算需求低常被用于高效部署。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/datasets/nicher92/medqa-swe">nicher92/medqa-swe · Datasets at Hugging Face</a></li>
<li><a href="https://aclanthology.org/2024.lrec-main.975/">MedQA-SWE - a Clinical Question &amp; Answer Dataset for Swedish</a></li>
<li><a href="https://arxiv.org/pdf/2505.07686">S - GRPO : Early Exit via Reinforcement Learning in Reasoning Models</a></li>

</ul>
</details>

**标签**: `#LLM`, `#medical QA`, `#reasoning`, `#open-weight models`, `#Swedish`

---

<a id="item-7"></a>
## [LLM 在 IMO 2026 基准测试：前沿模型接近满分](https://www.reddit.com/r/MachineLearning/comments/1v6wskz/we_compared_different_llms_on_imo_2026_r/) ⭐️ 8.0/10

一个由前 IMO 奖牌获得者组成的团队在全新的 2026 年国际数学奥林匹克竞赛题目上评估了多个 LLM，发现前沿模型 &\#x27;sol&\#x27; 和 &\#x27;fable&\#x27; 获得了近乎满分的成绩，而他们定制的多智能体编排工具 AutoFyn 显著提升了其他模型（如 Claude Sonnet 和开放权重模型 GLM）的表现。 这项比较表明，即使在全新的高难度数学推理任务上，前沿模型也正在接近人类专家水平的表现，而编排工具可以显著缩小较弱模型与前沿模型之间的差距，凸显了工程优化与模型规模同等重要。 评分结合了前沿模型的自动评估和前 IMO 奖牌获得者的人工验证；最难题目（P3）在所有非前沿模型上均未被解决，无论是否使用编排工具，且幻觉问题在可验证的数学领域仍然存在。

reddit · r/MachineLearning · /u/pequalnp92 · 7月26日 07:21

**背景**: 国际数学奥林匹克竞赛（IMO）题目面向高中生，但需要深度推理，且很少出现在训练数据中，因此成为衡量 LLM 推理能力的严格基准。像 AutoFyn 这样的编排工具通过协调多次 LLM 调用、检索和验证步骤，在复杂多步骤任务上提升性能，超越单次模型调用的能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://opace.agency/blog/gpt-5-6-sol-vs-fable-5-expensive-llms/">GPT-5.6 Sol vs Fable 5 | Do More Expensive LLMs Provide Better Results?</a></li>

</ul>
</details>

**标签**: `#LLM`, `#benchmark`, `#reasoning`, `#math`, `#evaluation`

---

<a id="item-8"></a>
## [DeepSeek 因创始人言论泄露暂停新一轮融资](https://www.bloomberg.com/news/articles/2026-07-25/deepseek-said-to-tell-backers-of-funding-pause-after-viral-posts) ⭐️ 8.0/10

DeepSeek 因创始人梁文锋对内部言论泄露不满，暂停了新一轮融资。该公司同时正在筹备首次公开募股，最快或于 2026 年递交申请。 此次暂停表明这家中国 AI 初创公司可能面临内部治理挑战，可能影响其短期融资和 IPO 进程。这也凸显了在竞争激烈的 AI 行业中沟通的敏感性。 此轮融资原计划募资至少 100 亿元人民币，投前估值不低于 4800 亿元。DeepSeek 在 2026 年 6 月完成的首轮融资中筹集了 70 亿美元，投资者包括腾讯、宁德时代及国家人工智能产业投资基金等。

telegram · zaihuapd · 7月26日 01:17

**背景**: DeepSeek 是一家位于杭州的中国人工智能公司，专注于开发大型语言模型。其 DeepSeek-V3 模型采用混合专家架构，总参数达 6710 亿。该公司由对冲基金 High-Flyer 全资拥有，其模型以强大的推理能力和高效推理著称。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek - Wikipedia</a></li>
<li><a href="https://www.deepseek.com/en/">DeepSeek</a></li>

</ul>
</details>

**标签**: `#AI`, `#DeepSeek`, `#funding`, `#business`, `#IPO`

---

<a id="item-9"></a>
## [长鑫科技登陆上交所，有望成 A 股市值最高公司](https://www.bloomberg.com/news/articles/2026-07-26/memory-frenzy-primes-china-champion-cxmt-for-historic-debut?srnd=phx-technology) ⭐️ 8.0/10

长鑫科技（CXMT），中国最大的 DRAM 制造商，将在上海证券交易所上市，此次 IPO 募集资金 666 亿元人民币（约 98 亿美元），是 2010 年以来 A 股最大规模 IPO。 此次 IPO 标志着中国推动半导体自主化，并可能使长鑫科技成为 A 股市值最高的公司，对全球 DRAM 市场和半导体行业产生重大影响。 发行价为每股 8.66 元，初始市值约 5800 亿元。散户认购部分超额 212 倍，940 万个订单共冻结约 7.07 万亿元资金。

telegram · zaihuapd · 7月26日 07:31

**背景**: DRAM（动态随机存取存储器）是一种用于计算机和设备的易失性存储器。长鑫科技以 IDM（设计制造一体化）模式运营，即自行设计和制造芯片。该公司是中国最先进的 DRAM 生产商，也是中国半导体自主化目标的关键参与者。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Random-access_memory">Random - access memory - Wikipedia</a></li>
<li><a href="https://www.techtarget.com/searchstorage/definition/DRAM">What is DRAM ( Dynamic Random Access Memory )? How Does it...</a></li>

</ul>
</details>

**标签**: `#DRAM`, `#Semiconductor`, `#IPO`, `#CXMT`, `#A-shares`

---

<a id="item-10"></a>
## [Claude 共享链接被搜索引擎索引，用户隐私泄露](https://search.brave.com/search?q=site%3Aclaude.ai%2Fshare&amp;amp;source=android) ⭐️ 8.0/10

Anthropic 的 Claude AI 助手的共享对话功能存在隐私漏洞，公开的共享链接被 Google 等搜索引擎索引，导致 API 密钥、加密货币钱包、个人简历等敏感数据泄露。与一年前修复了类似问题的 ChatGPT 不同，Anthropic 尚未解决此漏洞。 该漏洞大规模侵犯用户隐私，任何人通过搜索索引链接即可查看私人对话。这削弱了用户对处理敏感信息的 AI 助手的信任，并凸显了 AI 产品默认采取隐私保护措施的必要性。 泄露的数据包括 API 密钥、加密货币钱包、简历、法律咨询记录、公司内部项目和社会安全号码。谷歌已屏蔽索引，但 Brave 和 Bing 仍在索引。Anthropic 建议用户手动在设置中删除共享对话。

telegram · zaihuapd · 7月26日 11:16

**背景**: Claude 是 Anthropic 开发的 AI 助手，旨在提供安全准确的交互。其共享功能允许用户生成对话的公开链接。但这些链接缺少禁止搜索引擎索引的&\#x27;noindex&\#x27; robots 元标签。没有此标签，搜索引擎会自动索引这些链接，使其可公开发现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://claude.com/">Claude</a></li>
<li><a href="https://en.wikipedia.org/wiki/Noindex">noindex - Wikipedia</a></li>
<li><a href="https://developers.google.com/search/docs/crawling-indexing/block-indexing">Block Search Indexing with noindex | Google Search Central</a></li>

</ul>
</details>

**社区讨论**: 社区讨论强调了问题的严重性，许多用户对高度敏感数据的泄露表示担忧。Om Patel \(@om\_patel5\) 指出，谷歌已屏蔽索引，但 Brave 和 Bing 仍在索引这些链接。

**标签**: `#privacy`, `#security`, `#Claude`, `#AI`, `#vulnerability`

---

<a id="item-11"></a>
## [SpaceX 拒接 2028 年后猎鹰 9 订单，全力押注星舰](https://www.bloomberg.com/news/articles/2026-07-23/spacex-is-turning-away-falcon-customers-in-major-bet-on-starship) ⭐️ 8.0/10

SpaceX 开始拒绝卫星运营商 2028 年后使用猎鹰 9 的专属发射请求，并不再接受该火箭拼单项目的未来预订，同时缩减猎鹰系列非重复使用部件生产，以加速向星舰过渡。 这一战略转变可能重塑商业发射市场，因为许多卫星运营商依赖猎鹰 9 获得经济实惠的入轨途径；如果星舰未能在 2028 年底前投入商业运营，可能会产生巨大的发射能力缺口。 SpaceX 可能仍为美国国防部和 NASA 保留猎鹰 9 任务，但自 2026 年 6 月 IPO 以来，因星舰延误其股价已下跌约 25%；截至 2026 年 7 月，星舰已发射 13 次，8 次成功、5 次失败。

telegram · zaihuapd · 7月26日 12:42

**背景**: 星舰是 SpaceX 正在开发的两级完全可重复使用超重型运载火箭，旨在取代猎鹰 9 和猎鹰重型。它采用以液甲烷和液氧为燃料的猛禽发动机，目标是通过复用降低发射成本。猎鹰 9 一直是 SpaceX 的主力火箭，为商业和政府客户提供专属和拼单发射。SpaceX 向星舰的过渡涉及逐步停产猎鹰 9，但星舰尚未投入商业运营。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Starship_rocket">Starship rocket</a></li>
<li><a href="https://www.spacex.com/rideshare">Smallsat Rideshare Program - SpaceX</a></li>
<li><a href="https://rideshare.spacex.com/">SpaceX Satellite Rideshare</a></li>

</ul>
</details>

**标签**: `#SpaceX`, `#Starship`, `#Falcon 9`, `#space launch`, `#commercial space`

---