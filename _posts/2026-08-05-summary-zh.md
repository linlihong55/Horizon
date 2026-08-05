---
layout: default
title: "Horizon Summary: 2026-08-05 (ZH)"
date: 2026-08-05
lang: zh
---

> 从 38 条内容中筛选出 14 条重要资讯。

---

1. [Keyv 及相关 npm 包遭 Shai-Hulud 供应链攻击入侵](#item-1) ⭐️ 9.0/10
2. [谷歌搭建 2000 亿美元融资机器，向 Anthropic 交付 AI 芯片](#item-2) ⭐️ 9.0/10
3. [Mistral 发布 Shieldstral：3B 开放权重多模态审核模型](#item-3) ⭐️ 8.0/10
4. [自定义色彩空间与算法生成多元肤色](#item-4) ⭐️ 8.0/10
5. [Waymo 在达拉斯推出无人驾驶打车服务](#item-5) ⭐️ 8.0/10
6. [DeepSeek V4 Flash 在单块 AMD MI300X 上成功运行](#item-6) ⭐️ 8.0/10
7. [联邦快递合法邮件酷似钓鱼邮件](#item-7) ⭐️ 8.0/10
8. [Oxide Computer 完成 4.45 亿美元 D 轮融资，SEC 文件确认](#item-8) ⭐️ 8.0/10
9. [Xbox 宕机导致光盘游戏无法游玩，引发 DRM 所有权之争](#item-9) ⭐️ 8.0/10
10. [MiniMax-H3 全模态模型现可通过 MLX 移植在 Apple Silicon 上运行](#item-10) ⭐️ 8.0/10
11. [华为首席科学家警告英伟达芯片将触及物理极限](#item-11) ⭐️ 8.0/10
12. [特朗普政府拟起草禁令限制中国光模块](#item-12) ⭐️ 8.0/10
13. [我国首部 L3/L4 自动驾驶强制性国标发布，2027 年 7 月起实施](#item-13) ⭐️ 8.0/10
14. [白宫开源 AI 监管转向，硅谷分裂](#item-14) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Keyv 及相关 npm 包遭 Shai-Hulud 供应链攻击入侵](https://www.aikido.dev/blog/keyv-and-friends-compromised-in-npm-supply-chain-attack) ⭐️ 9.0/10

JFrog 的安全研究人员发现新一轮 Shai-Hulud 蠕虫通过 npm 仓库中遭入侵的软件包传播，首先波及 keyv 和 cacheable。这次主动攻击已影响超过 400 个软件包，包括广泛使用的键值存储库 keyv。 Keyv 是一个被广泛使用的 npm 库，有超过 1700 个下游项目依赖它，因此此次入侵可能波及整个 JavaScript 生态系统。该攻击表明自复制蠕虫能够利用 npm 的信任模型，凸显了加强供应链安全措施的迫切性。 该蠕虫会窃取凭据、自动向所有可写的 npm 软件包发布自身，并在 GitHub 仓库中植入执行钩子。JFrog 的分析表明攻击仍在进行中，开发者应检查 keyv、cacheable 及其依赖包是否存在可疑版本。

hackernews · cimi\_ · 8月4日 11:01 · [社区讨论](https://news.ycombinator.com/item?id=49166874)

**背景**: Shai-Hulud 是一种自我复制的蠕虫，针对世界上最大的 JavaScript 软件包注册表 npm 生态系统。它通过入侵维护者账户或软件包来传播，窃取凭据，然后利用这些凭据向其他可写软件包发布恶意更新。与典型的单次供应链攻击载荷不同，Shai-Hulud 实现了传播自动化，因此能迅速入侵数百个软件包，并使得清理工作十分困难。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://research.jfrog.com/post/shai-hulud-is-back-august/">Major Shai Hulud campaign strikes npm again, affecting keyv and 400+ packages - JFrog Security Research</a></li>
<li><a href="https://www.cisa.gov/news-events/alerts/2025/09/23/widespread-supply-chain-compromise-impacting-npm-ecosystem">Widespread Supply Chain Compromise Impacting npm Ecosystem | CISA</a></li>
<li><a href="https://unit42.paloaltonetworks.com/npm-supply-chain-attack/">&quot;Shai-Hulud&quot; Worm Compromises npm Ecosystem in Supply Chain Attack (Updated November 26)</a></li>

</ul>
</details>

**社区讨论**: 评论者对 npm 依赖链的脆弱性以及攻击后清理的困难表示担忧。有人建议限制或禁止安装前后的钩子脚本、采用开发容器进行隔离，以及使用 Packj 等静态和动态分析工具来检测此类入侵。

**标签**: `#security`, `#supply-chain`, `#npm`, `#malware`, `#cybersecurity`

---

<a id="item-2"></a>
## [谷歌搭建 2000 亿美元融资机器，向 Anthropic 交付 AI 芯片](https://www.ft.com/content/549f2e23-5aa2-49c7-9ea6-a9784ab7087c) ⭐️ 9.0/10

据《金融时报》调查，谷歌悄然搭建了约 2000 亿美元的资产支持融资架构，向 Anthropic 交付超过 1500 亿美元的 AI 芯片。该架构涉及博通、阿波罗、黑石、摩根士丹利及多家加密矿企，其中名为 Compute SPV 的特殊目的载体已于 6 月完成首批约 350 亿美元的硬件采购。 这是有史以来规模最大的 AI 基础设施融资架构之一，代表了 AI 算力资金筹措和部署方式的范式转变。该模式让没有信用评级的 Anthropic 能够获得数千亿美元的芯片，同时不使任何单一公司的资产负债表承压，并可能为未来 AI 基础设施交易树立模板。 相关合同总额约 2000 亿美元，约八成与芯片直接挂钩。各方分担风险：谷歌担保数据中心，博通购买并协助融资芯片，阿波罗与黑石购买硬件后回租给 Anthropic；6 月 Compute SPV 交易涵盖约 1 吉瓦算力和 100 万颗 TPU。

telegram · zaihuapd · 8月4日 10:52

**背景**: 该架构借鉴了厂商融资（vendor financing）模式——波音、GE 等公司通过与金融机构合作，帮助客户克服高昂的前期采购成本来推销飞机和发动机。特殊目的载体（SPV）是为隔离特定交易财务风险而设立的破产隔离实体，Compute SPV 正是为此成立。张量处理单元（TPU）是谷歌为神经网络机器学习设计的定制专用集成电路（ASIC），为 Anthropic 提供算力支撑。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Tensor_Processing_Unit">Tensor Processing Unit - Wikipedia</a></li>
<li><a href="https://corporatefinanceinstitute.com/resources/management/special-purpose-vehicle-spv/">Special Purpose Vehicle ( SPV ) - Guide, Examples, What You Need...</a></li>
<li><a href="https://www.pnc.com/insights/corporate-institutional/raise-capital/vendor-financing-what-it-is-and-how-it-works.html">Vendor Financing: What It Is and How It Works | PNC Insights</a></li>

</ul>
</details>

**标签**: `#Google`, `#Anthropic`, `#AI Infrastructure`, `#Financing`, `#AI Chips`

---

<a id="item-3"></a>
## [Mistral 发布 Shieldstral：3B 开放权重多模态审核模型](https://mistral.ai/news/shieldstral/) ⭐️ 8.0/10

Mistral 已发布 Shieldstral-1.0-3B，一个开放权重的 3B 参数多模态内容审核模型，现已在 Hugging Face 上提供。它提供了一种经济高效、可定制化的替代方案，以取代现有的审核 API。 内容审核是在线平台面临的关键挑战，而开放权重模型允许开发者微调并本地部署，减少对专有 API 的依赖。这可能降低小型平台的进入门槛，并加速多模态安全工具的采用。 Shieldstral 支持文本和图像输入，适用于跨多种内容类型的基于策略的审核。由于仅有 3B 参数，它可以在中等算力的边缘设备上运行，但其非确定性特性可能仍需要人工审核作为安全网。

hackernews · riadsila · 8月4日 16:36 · [社区讨论](https://news.ycombinator.com/item?id=49171268)

**背景**: 开放权重模型是公开发布其训练参数的 AI 模型，允许任何人下载和定制。多模态内容审核使用 AI 同时分析文本、图像及其他内容形式以识别违规。3B 参数规模处于“金发姑娘区”——小到足以本地部署，又强大到能胜任许多实际任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>
<li><a href="https://arxiv.org/html/2508.05527v1">AI vs. Human Moderators: A Comparative Evaluation of Multimodal LLMs in Content Moderation for Brand Safety Accepted to the Computer Vision in Advertising and Marketing (CVAM) workshop at ICCV 2025.</a></li>
<li><a href="https://quadric.ai/blog/on-device-llm-revolution">The On-Device LLM Revolution: Why 3B-30B Models Are Moving to the Edge | Quadric Blog</a></li>

</ul>
</details>

**社区讨论**: 评论者询问 Shieldstral 是否支持任意规则集，还是仅支持固定的审核风格，还有人戏称其应命名为“Safestral”。一些人赞赏 Mistral 转向小型微调模型的策略，另一些人则将其与 OpenAI 的 omni-moderation API 进行比较，并指出它可能作为一种经济高效的初步防线，但敏感场景仍需人工审核。

**标签**: `#AI`, `#moderation`, `#Mistral`, `#open-weights`, `#safety`

---

<a id="item-4"></a>
## [自定义色彩空间与算法生成多元肤色](https://toneyalexander.github.io/inclusive-color-space/) ⭐️ 8.0/10

作者构建了一个自定义色彩空间，并提供了 JavaScript 取色器以及 Python 和 JavaScript 版本的程序化生成算法，让数字艺术和游戏开发中采样合理且多样的肤色变得容易。项目页面包含交互式演示和关于该色彩空间构建过程的详细说明。 这填补了创意工具中的一个实际缺口：传统取色器难以便捷地选择广泛而包容的肤色范围。基于简单方程的肤色色彩空间可以改进游戏和数字艺术中的角色自定义与程序化生成，帮助创作者避免局限于狭窄的肤色集合。 该色彩空间基于 PCA（主成分分析）导出的二维基向量，通过对肤色数据手工拟合方程而构建，最终形成一个近似新月形的紧凑区域。作者也表示方法学上“有点不严谨”，并提供了“未来工作”部分，承认仍有改进空间。

hackernews · automatoney · 8月4日 15:16 · [社区讨论](https://news.ycombinator.com/item?id=49170165)

**背景**: 色彩空间是用数字表示颜色的系统，例如 RGB 或 HSV，但通用色彩空间并非为准确表示人类肤色而设计。肤色受黑色素、血流、光照和人类感知等多重因素影响，因此合理的肤色在完整色彩空间中只形成一个有限且弯曲的区域。现有的 Pantone SkinTones 和粉底色号数据也呈现出这种新月形分布，而色彩科学家也观察到将肤色饱和度调到 100% 时颜色会偏向橙色。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://toneyalexander.github.io/inclusive-color-space/">What Colors Are We? Constructing A Color Space For Skin Tones</a></li>
<li><a href="https://news.ycombinator.com/item?id=49170165">Show HN: Simple algorithm and color space to generate diverse skin tones | Hacker News</a></li>

</ul>
</details>

**社区讨论**: 评论区整体反响积极，称赞了演示效果和手工拟合函数的思路，并指出所得颜色与 Oklab 色彩空间中粉底色号数据呈现的新月形分布一致。也有用户提出注意事项：部分生成的颜色看起来带绿、蓝或紫色，还有人问为什么没有参考 Pantone SkinTones。另有评论者分享了一个事实：当饱和度调到 100% 时，任何种族肤色看起来都偏向橙色。

**标签**: `#color-space`, `#computer-graphics`, `#procedural-generation`, `#skin-tones`, `#game-development`

---

<a id="item-5"></a>
## [Waymo 在达拉斯推出无人驾驶打车服务](https://waymo.com/blog/shorts/dallas-open-to-all/) ⭐️ 8.0/10

Waymo 已在达拉斯推出其自动驾驶打车服务，向所有用户开放。这标志着公司向得州新的主要都会区扩张。 达拉斯的推出是自动驾驶汽车更广泛部署中的一座重要里程碑，将自动驾驶出租车带到一个低密度、高度依赖汽车的地区。这也引发了关于安全、城市规划以及无人驾驶车队对地方经济影响的持续公众讨论。 达拉斯-沃斯堡都会区密度极低，公共交通有限，是自动驾驶出租车在以汽车为中心的环境中的一个试验场。用户评论还提到一些运营细节，如需要本地维护人员，以及偶尔出现车辆卡住的情况。

hackernews · xnx · 8月4日 18:29 · [社区讨论](https://news.ycombinator.com/item?id=49172836)

**背景**: Waymo 是一家自动驾驶汽车公司，是 Alphabet 的子公司，起源于谷歌的自动驾驶汽车项目。它是美国领先的自动驾驶出租车商业运营商，“向所有人开放”意味着达拉斯服务现已面向普通公众，而不是仅限等待名单。自动驾驶出租车是一种可以通过应用程序叫车的自动驾驶车辆，类似于网约车服务，但没有人类司机。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://waymo.com/">Waymo - Self-Driving Cars - Autonomous Vehicles - Ride-Hail</a></li>
<li><a href="https://builtin.com/articles/waymo-robotaxis">Waymo Explained: Alphabet’s Autonomous Vehicle Company | Built In</a></li>
<li><a href="https://en.wikipedia.org/wiki/Robotaxi">Robotaxi - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论总体上是积极的，用户称赞 Waymo 比人类驾驶员更安全、更可预测。也有少数人提出经济方面的担忧，比如资金流出当地经济，而另一位评论者认为，无人驾驶汽车可以减少对停车位和汽车的需求，从而成为一种可负担住房政策。

**标签**: `#autonomous vehicles`, `#Waymo`, `#Dallas`, `#urban planning`, `#mobility`

---

<a id="item-6"></a>
## [DeepSeek V4 Flash 在单块 AMD MI300X 上成功运行](https://github.com/ryanzhou/deepseek-v4-flash-mi300x) ⭐️ 8.0/10

一份实用指南展示了如何在单块 AMD MI300X 上运行 DeepSeek V4 Flash，实现约每秒 150 个 token 的推理速度。该方案将上下文窗口从模型原生的 1M token 缩减到 256k，以适配 GPU 的 192GB HBM3 显存。 这降低了自托管前沿级 MoE 模型的硬件门槛，表明一块 MI300X 就能以实用速度提供服务。同时也有力支持了 AMD 在 AI 推理领域与 NVIDIA 竞争的地位，为开发者提供了一条单卡部署的参考路径。 DeepSeek V4 Flash 是混合专家（MoE）模型，总参数 284B、激活参数 13B，并提供原生 MXFP4 量化权重。MI300X 拥有 192GB HBM3 显存，是模型能否装下的关键，但 MI300X 是 OAM 模块，通常以 8 卡整机形式销售，无法单独购买。

hackernews · zhoutong · 8月4日 10:00 · [社区讨论](https://news.ycombinator.com/item?id=49166386)

**背景**: DeepSeek V4 Flash 是 DeepSeek V4 系列的效率优化预览版，设计用于在 1M token 上下文下进行高效推理。AMD MI300X 是 Instinct 数据中心 GPU，配备 192GB HBM3 显存和 304 个计算单元。量化是将模型权重压缩为更低精度的技术，能让大模型在单块加速器上运行并加快推理，但通常需要做出一些取舍，比如缩短上下文长度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash">deepseek -ai/ DeepSeek - V 4 - Flash · Hugging Face</a></li>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4-flash">DeepSeek V 4 Flash - API Pricing &amp; Benchmarks | OpenRouter</a></li>
<li><a href="https://www.amd.com/en/products/accelerators/instinct/mi300/mi300x.html">AMD Instinct™ MI300X Accelerators</a></li>

</ul>
</details>

**社区讨论**: 评论者提出了实际注意事项：用户无法轻易买到单块 MI300X，它只以约 25 万欧元的 8 卡整机形式销售。还有人提到其他方案，如 DoubleWord 的双卡 MI300X 工作、DwarfStar 项目，以及显存 144GB 的 PCIe 版 MI350P——由于原生 MXFP4 量化，该卡也能运行此模型。一位评论者认为上下文窗口的取舍可以接受，并类比了 OpenAI Codex 的范围。

**标签**: `#DeepSeek`, `#AMD MI300X`, `#LLM inference`, `#quantization`, `#hardware`

---

<a id="item-7"></a>
## [联邦快递合法邮件酷似钓鱼邮件](https://www.troyhunt.com/thanks-fedex-this-is-why-we-keep-getting-phished/) ⭐️ 8.0/10

特洛伊·亨特（Troy Hunt）在 2024 年发布博文，剖析了一封真实的联邦快递通知邮件，它与钓鱼邮件几乎无法区分。文章展示了合法的物流提醒如何采用与骗子相同的格式、链接和紧迫感。 当合法企业发送看起来像钓鱼邮件的邮件时，用户会被训练得无视危险信号，从而使真正的钓鱼攻击更容易得逞。这一案例突显了一个影响所有电子邮件用户的系统性安全与用户体验问题。 该博文引发 46 条社区评论，评分达到 195，读者分享了来自联邦快递、谷歌和美国国税局（IRS）的类似经历。评论者指出，即使是技术用户也不确定某些官方邮件或如 c.gle 这样的短域名是否合法。

hackernews · stymaar · 8月4日 21:09 · [社区讨论](https://news.ycombinator.com/item?id=49175192)

**背景**: 网络钓鱼是一种社会工程学攻击，攻击者冒充可信机构来诱骗人们泄露敏感信息。SPF、DKIM 和 DMARC 等技术标准可以帮助验证邮件确实来自某个域名，但无法阻止合法发件人编写带有钓鱼特征的邮件。正如特洛伊·亨特的联邦快递案例所示，即使是经过身份验证的邮件也可能让用户感到困惑。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.validity.com/email-authentication/dmarc/">What is DMARC ? How Does DMARC Work? - Validity</a></li>
<li><a href="https://www.csoonline.com/article/567357/3-email-security-protocols-that-help-prevent-address-spoofing-how-to-use-them.html">Preventing address spoofing with DMARC, DKIM and SPF | CSO Online</a></li>

</ul>
</details>

**社区讨论**: 评论者大多赞同亨特的观点，并分享了各自经历的“合法信息看起来像诈骗”的例子：联邦快递由真人发送的包含 PDF 附件的真实海关通知、使用 c.gle 链接的谷歌存储提醒，以及声音与诈骗来电完全相同的 IRS 自动语音系统。有读者指出，.xyz 等新通用顶级域（gTLD）的泛滥让非技术用户更难识别钓鱼。还有评论提到澳大利亚拦截了 3.36 亿条诈骗短信，印证了问题的普遍性。

**标签**: `#phishing`, `#cybersecurity`, `#email`, `#social engineering`, `#human factors`

---

<a id="item-8"></a>
## [Oxide Computer 完成 4.45 亿美元 D 轮融资，SEC 文件确认](https://www.sec.gov/Archives/edgar/data/1795071/000179507126000002/xslFormDX01/primary_doc.xml) ⭐️ 8.0/10

根据新的 SEC Form D 文件，Oxide Computer 已在 D 轮融资中筹集 4.45 亿美元。此前该公司已完成 A 轮（4400 万美元）、B 轮（1 亿美元）和 C 轮（2 亿美元）融资。 这笔巨额融资表明投资者对 Oxide 的愿景——用一体化本地云计算机挑战 AWS 等公有云——充满信心。这可能加速公司发展，并推动整个行业向机架级、软件定义的基础设施迈进。 SEC Form D 是豁免证券发行的通知，包含的运营细节有限，因此文件未披露估值或投资者名单。Oxide 销售的是机架级“云计算机”，将计算、存储、网络和软件集成到单一平台中。

hackernews · depr · 8月4日 20:13 · [社区讨论](https://news.ycombinator.com/item?id=49174407)

**背景**: Oxide Computer Company 由前 Sun 和 Joyent 工程师创立，旨在通过单个集成机架在本地提供公有云体验。该公司将其产品描述为“公有云就是这样构建的，Oxide 也是如此”。Form D 文件是私营公司向 SEC 报告某些证券发行（通常是 Reg D 豁免）的方式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://oxide.computer/">Oxide Computer Company</a></li>
<li><a href="https://research.aerarium.app/filings/form-d">SEC Form D : exempt offering notice | Aerarium Research</a></li>
<li><a href="https://tracxn.com/d/companies/oxide-computer/__kI0jT50BQRv4YWhfboq9Wp2wCfHm6iQWJODTcCX-grc">Oxide Computer - 2026 Company Profile, Team, Funding... - Tracxn</a></li>

</ul>
</details>

**社区讨论**: 社区反应既兴奋又怀疑。许多人称赞产品理念和团队——尤其是 Jessie Frazelle——但有人质疑 Oxide 是否真的出货硬件，还有一位工程副总裁表示，尽管他的公司每年在 AWS 上花费 90 万美元，他提交的销售问询却一直没有得到回复。

**标签**: `#funding`, `#hardware`, `#cloud-computing`, `#infrastructure`, `#oxide-computer`

---

<a id="item-9"></a>
## [Xbox 宕机导致光盘游戏无法游玩，引发 DRM 所有权之争](https://birchtree.me/blog/xbox-goes-down-you-cant-play-games-you-own-on-disc/) ⭐️ 8.0/10

一次大规模的 Xbox 宕机导致用户无法游玩自己拥有的实体光盘游戏，因为主机无法完成所需的在线 DRM 验证。在微软服务器恢复之前，即使是光盘版游戏也无法运行。 这起事件揭示了现代游戏的一个关键现实：即使是实体游戏光盘也受限于在线 DRM 验证，意味着消费者并未真正拥有自己的游戏。它重新点燃了关于数字所有权和消费者权利的争论，影响所有 Xbox 玩家，并引发对游戏保存问题的担忧。 这次宕机表明，即使是光盘版游戏，Xbox 主机也会执行在线许可证验证，需要连接微软服务器。原文提到该讨论吸引了 613 条评论，显示出社区对此话题的强烈关注。

hackernews · surprisetalk · 8月4日 12:01 · [社区讨论](https://news.ycombinator.com/item?id=49167448)

**背景**: DRM（数字版权管理）指限制数字内容使用方式的技术，通常需要在线验证以证明所有权或许可。许多现代主机和 PC 即使对实体介质也会执行 DRM 验证，因此如果相关服务器离线或永久关闭，合法购买的游戏可能变得无法游玩。这引发了消费者对长期使用权以及&\#x27;拥有&\#x27;游戏真正含义的担忧。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Digital_rights_management">Digital rights management - Wikipedia</a></li>
<li><a href="https://business.adobe.com/blog/basics/digital-rights-management">Digital Rights Management ( DRM ) | What It Is, How It Works &amp; Why It...</a></li>
<li><a href="https://www.youtube.com/watch?v=lZ2LhcsvyDQ">You Don&#x27;t Really Own Your Digital Games - YouTube</a></li>

</ul>
</details>

**社区讨论**: 评论者对游戏行业正走向类似电视、电影和音乐的授权模式表示失望，消费者几乎什么都不拥有。一位用户认为真正的问题在于所有权，而非实体与数字格式之争，并列出了永久访问、离线使用、转售和传给后代等权利。还有用户指出，像 PS3 这样的旧主机使用免费服务器进行匹配，并支持离线游玩，与如今对在线的依赖形成鲜明对比。

**标签**: `#DRM`, `#digital ownership`, `#gaming`, `#Xbox outage`, `#consumer rights`

---

<a id="item-10"></a>
## [MiniMax-H3 全模态模型现可通过 MLX 移植在 Apple Silicon 上运行](https://simonwillison.net/2026/Aug/4/minimax-h3-mlx/#atom-everything) ⭐️ 8.0/10

MiniMax 发布了 MiniMax-H3，这是一个全模态生成系统，可接受文本、图像、音频和视频，并生成最长 15 秒、含音频的视频片段。新的 Python 包 PipeNetwork/minimax-h3-mlx 将该模型移植到 MLX，可在 Apple Silicon 上运行，作者已在 M5 Max MacBook Pro 上成功运行。 这使 Apple Silicon 用户无需云端 GPU 即可使用强大的尖端多模态生成模型。这体现了 MLX 移植生态的不断壮大，以及在消费级硬件上本地运行大型生成模型的趋势。 该模型需下载约 115 GB 文件，在 M5 Max MacBook Pro 上生成单个 15 秒视频耗时近 45 分钟。音频输出若不遵循提示指南可能效果不佳，作者指出在未加引导时生成的音频是&quot;奇怪的类似语音的垃圾内容&quot;。

rss · Simon Willison · 8月4日 19:10

**背景**: MLX 是 Apple 开发的数组框架，面向 Apple silicon 的高效机器学习，利用统一内存架构并提供类似 NumPy 的 Python API。全模态生成系统是一种统一模型，能够跨文本、图像、音频和视频模态进行理解和生成，超越了单一任务的文本转视频模型。MLX 移植使得这些模型可以借助 Metal 在 Mac 上本地运行，而无需依赖远程云服务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mlx-framework.org/">MLX</a></li>
<li><a href="https://github.com/ml-explore/mlx">GitHub - ml-explore/ mlx : MLX : An array framework for Apple silicon</a></li>
<li><a href="https://opensource.apple.com/projects/mlx/">Apple Open Source</a></li>

</ul>
</details>

**标签**: `#MiniMax-H3`, `#MLX`, `#multimodal generation`, `#video generation`, `#Apple Silicon`

---

<a id="item-11"></a>
## [华为首席科学家警告英伟达芯片将触及物理极限](https://www.bloomberg.com/news/articles/2026-08-04/huawei-s-top-scientist-warns-of-chip-limit-nvidia-will-soon-face) ⭐️ 8.0/10

华为首席半导体科学家廖恒在 7 月底一次罕见的四小时公开采访中警告，英伟达式通过增加计算芯片和高带宽内存来扩展规模的做法终将触及物理极限，并提出了华为的 LogicFolding 技术框架与韬定律作为替代路径。首款采用 LogicFolding 的手机芯片预计今年晚些时候亮相。 这一表态意义重大，因为它挑战了行业主流假设，即单纯增加硅片和内存就能维持 AI 算力增长。如果物理极限真实存在，从英伟达到台积电再到云服务商的整个半导体生态都将需要 3D 逻辑堆叠和新的缩放定律等替代路径。 廖恒透露，华为过去六年间已采用 LogicFolding（一种以信号延迟而非晶体管间距为优化目标的 3D 逻辑堆叠框架）设计并制造了 381 款芯片。首款产品将是 Mate 90 系列中的 Kirin 2026 SoC，Ascend AI 加速器预计约在 2030 年跟进，目标是在 2031 年前在不使用 EUV 光刻的情况下实现等效 1.4nm 级密度。

telegram · zaihuapd · 8月4日 08:04

**背景**: 传统半导体缩放通常以摩尔定律描述，依靠缩小晶体管尺寸来提升性能。华为的韬定律（也译作 Tao&\#x27;s Law）被定位为在晶体管小型化触顶的行业中替代性缩放理论，强调系统级集成与 3D 堆叠。这一方向与整个行业“芯片性能不能再只靠缩小晶体管”的演进趋势高度一致，但在 EDA 工具链和能耗控制等方面仍有关键挑战待解决。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://abhs.in/blog/huawei-tau-scaling-law-logicfolding-55-percent-density-kirin-ascend-2026">Huawei Tau Scaling Law: 55% Density Gain on Kirin and Ascend Chips</a></li>
<li><a href="https://min.news/en/tech/a6f179218a21e70ccdde040590dd609d.html">A detailed explanation of Huawei&#x27; s &quot; Tao Law &quot;: What does it really...</a></li>
<li><a href="https://gizmoindo.com/news/huawei-tao-law-semiconductor-news/">Huawei Tao Law : New Hope or Chip Industry Mirage?</a></li>

</ul>
</details>

**标签**: `#semiconductors`, `#Huawei`, `#Nvidia`, `#chip design`, `#physical limits`

---

<a id="item-12"></a>
## [特朗普政府拟起草禁令限制中国光模块](https://www.reuters.com/world/trump-administration-drafting-ban-chinese-data-center-devices-sources-say-2026-08-04/) ⭐️ 8.0/10

特朗普政府正在起草一项禁令，拟禁止进口新型中国光模块及其他数据中心组件，据报美国联邦通信委员会（FCC）正在推进该措施。官员们希望在今年内发布并实施该规定，以保护 AI 基础设施免受间谍活动和破坏。 该禁令将严重扰乱全球数据中心和 AI 供应链，直接冲击中际旭创等主要供应商——该公司占据约 27%的光模块市场份额。此举也使中美在关键科技领域的贸易紧张进一步升级。 知情人士提醒称，禁令仍可能被修改或搁置；中国驻美使馆则表示将采取一切必要措施维护中国利益。此前 FCC 已对中国无人机、路由器、机器人和逆变器实施过类似的进口限制。

telegram · zaihuapd · 8月4日 11:29

**背景**: 光模块是数据中心网络中的关键组件，通过光纤电缆将电信号转换为光信号，实现高速数据传输。它们连接服务器、交换机等网络设备，是支撑 AI 工作负载所需高带宽基础设施的重要组成部分。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ascentoptics.com/blog/everything-you-need-to-know-about-optical-modules/">Everything You Need to Know About Optical Modules</a></li>
<li><a href="https://www.baudcom.com.cn/blog/understand-the-optical-module">What is Optical Module ？ A Simple Guide for Beginners - Baudcom</a></li>

</ul>
</details>

**标签**: `#policy`, `#trade`, `#AI infrastructure`, `#China`, `#supply chain`

---

<a id="item-13"></a>
## [我国首部 L3/L4 自动驾驶强制性国标发布，2027 年 7 月起实施](https://wap.miit.gov.cn/jgsj/zbys/qcgy/art/2026/art_a1d2072374884287b67048a77560014e.html) ⭐️ 8.0/10

工业和信息化部组织制定的《智能网联汽车 自动驾驶系统安全要求》（GB 44721—2026）强制性国家标准正式发布，拟于 2027 年 7 月 1 日起实施。这是我国首部专门针对 L3 级有条件自动驾驶和 L4 级高度自动驾驶系统的强制性国标。 该标准将自动驾驶安全要求从推荐性转为强制性，标志着我国智能网联汽车监管进入新阶段，为行业划定了统一的合规底线。它将深刻影响整车企业、零部件供应商和科技公司，有望加速 L3/L4 级自动驾驶的大规模落地，同时明确法律与技术预期。 该标准适用于搭载 L3、L4 级系统的 M 类（载客）和 N 类（载货）车辆，但不适用于自动泊车系统。它是对 2024 年推荐性国标的系统性升级，从企业全生命周期安全保障、系统动态驾驶能力、人机交互与用户告知、多维度检验检测四个维度构建安全要求体系。

telegram · zaihuapd · 8月4日 13:06

**背景**: 根据中国国家标准《汽车驾驶自动化分级》（GB/T40429-2021），自动驾驶技术分为 L0 至 L5 共 6 个等级，其中 L3 为有条件自动驾驶，L4 为高度自动驾驶。M 类和 N 类车辆分别指载客和载货车辆，是中国车辆分类标准中的类型。2024 年发布的推荐性国标为本次强制性国标的制定奠定了基础。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.autohome.com.cn/news/202608/1316205.html">autohome.com.cn/news/202608/1316205.html</a></li>
<li><a href="https://www.donews.com/tag/58673.html">GB 44721 — 2026 - DoNews - 创新无边界</a></li>
<li><a href="https://m.jrj.com.cn/madapter/24h/2026/06/16174957490090.shtml">m.jrj.com.cn/madapter/24h/ 2026 /06/16174957490090.shtml</a></li>

</ul>
</details>

**标签**: `#autonomous driving`, `#regulation`, `#China`, `#L3/L4`, `#standards`

---

<a id="item-14"></a>
## [白宫开源 AI 监管转向，硅谷分裂](https://www.nytimes.com/2026/08/04/technology/ai-washington-regulation-whiplash.html) ⭐️ 8.0/10

白宫突然逆转了限制中国开源 AI 模型的立场，放弃了此前考虑制裁和贸易黑名单的做法，转而聚焦提升美国 AI 竞争力。8 月 4 日，白宫召集科技公司商议新框架，拟在模型发布前进行网络安全审查。 这一逆转将决定美国在对华竞争中把开源 AI 视为安全威胁还是战略资产。该决定将影响主要 AI 实验室、开源社区和美国企业的全球运营方式，科技领袖在这一问题上公开分裂。 导火索是月之暗面（Moonshot AI）开发的中国开源模型 Kimi，据报道其在部分任务上可与 OpenAI 的顶级模型匹敌。OpenAI 和 Anthropic 主张对中国竞争对手设限，而 Nvidia 和 Meta 则捍卫开放生态；黄仁勋最近首次在 X 上发帖为开源辩护，并组建了有 230 多家成员公司的安全联盟。

telegram · zaihuapd · 8月4日 15:22

**背景**: 开源 AI 模型会公开其权重，允许任何人研究、修改和部署。这种开放性可加速创新，但也引发滥用和国家安全方面的担忧。Kimi 是总部位于北京的初创公司月之暗面（Moonshot AI）推出的系列大语言模型和聊天机器人，该公司由清华大学校友于 2023 年创立，以长上下文窗口和媲美西方模型的性能著称。美国政府一直在权衡如何平衡 AI 竞争力与安全限制，此次急转弯反映了科技行业两派的密集游说。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kimi_%28chatbot%29">Kimi (chatbot) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Moonshot_AI">Moonshot AI</a></li>

</ul>
</details>

**标签**: `#AI regulation`, `#open source`, `#policy`, `#national security`, `#Silicon Valley`

---