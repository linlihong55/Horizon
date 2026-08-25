---
layout: default
title: "Horizon Summary: 2026-08-25 (ZH)"
date: 2026-08-25
lang: zh
---

> 从 41 条内容中筛选出 11 条重要资讯。

---

1. [苹果推出 M6 和 M5 Ultra 芯片，性能和 AI 算力大幅跃升](#item-1) ⭐️ 9.0/10
2. [OpenAI 自研芯片 Jalapeño 推理性能超越英伟达 Blackwell](#item-2) ⭐️ 9.0/10
3. [Vera Rubin NVL72 首测：AI 推理吞吐提升 30 倍](#item-3) ⭐️ 9.0/10
4. [FDA 批准首款可同时监测血糖和酮体的可穿戴设备](#item-4) ⭐️ 8.0/10
5. [苹果推出搭载 M5 Max 和 M5 Ultra 的新款 Mac Studio，主打本地 AI](#item-5) ⭐️ 8.0/10
6. [Nitter 项目收到停止函，实例暂停服务](#item-6) ⭐️ 8.0/10
7. [火狐 157 将默认在所有平台启用 JPEG XL](#item-7) ⭐️ 8.0/10
8. [SpaceX 宣布在路易斯安那州建设耗资 1000 亿美元的 Starbase LA 航天港](#item-8) ⭐️ 8.0/10
9. [EVE Online 启动向 Python 3 的长期迁移](#item-9) ⭐️ 8.0/10
10. [SpaceX 计划 2027 年将英伟达 Vera Rubin NVL72 送入轨道](#item-10) ⭐️ 8.0/10
11. [GPT-5.6 Sol 设计定制 CPU 成功运行《毁灭战士》](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [苹果推出 M6 和 M5 Ultra 芯片，性能和 AI 算力大幅跃升](https://www.apple.com/newsroom/2026/08/apple-introduces-m6-and-m5-ultra-for-a-big-leap-in-performance-and-ai-compute/) ⭐️ 9.0/10

苹果于 2026 年 8 月 25 日发布 M6 和 M5 Ultra 芯片。M6 是苹果首款 2nm 芯片，配备 12 核 CPU、12 核 GPU 和双 16 核神经引擎；M5 Ultra 则是苹果史上最强芯片，采用四晶粒（quad-die）架构。 这标志着 Apple Silicon 在代际上的重大飞跃，尤其是在 AI 算力方面，并将驱动新款 Mac mini 和 Mac Studio。这些芯片可能会为端侧 AI 和专业工作负载树立新标杆，巩固苹果相对于高通、AMD 等竞争对手的地位。 M6 是苹果首款 2nm 芯片，由台积电代工；M5 Ultra 则是苹果首款四晶粒芯片，通过 UltraFusion 连接两颗 M5 Max 双晶粒芯片。苹果将 M5 Ultra 定位用于极端专业工作负载，如复杂 3D 渲染、科学分析以及在设备端运行计算密集型前沿 AI 模型。

hackernews · interpol\_p · 8月25日 13:01 · [社区讨论](https://news.ycombinator.com/item?id=49433292)

**背景**: Apple Silicon 是苹果为 Mac 打造的基于 ARM 架构的系统级芯片产品线，具有统一内存，并集成了 CPU、GPU 和神经引擎。苹果持续改进这些芯片，M5 系列于 2025 年底推出，而 M6 和 M5 Ultra 于 2026 年 8 月发布。M6 采用的 2nm 工艺节点相比此前的 3nm 芯片是一大进步，能在芯片上容纳更多晶体管，并有更好的能效。AI 算力已成为重点，Apple Intelligence 等功能需要较新的芯片支持。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.apple.com/newsroom/2026/08/apple-introduces-m6-and-m5-ultra-for-a-big-leap-in-performance-and-ai-compute/">Apple introduces M6 and M5 Ultra for a big leap in performance and AI compute - Apple</a></li>
<li><a href="https://en.wikipedia.org/wiki/Apple_M6">Apple M 6 - Wikipedia</a></li>
<li><a href="https://9to5mac.com/2026/08/25/apple-launches-next-gen-apple-silicon-chips-m6-and-m5-ultra/">Apple launches next-gen Apple Silicon chips : M 6 and... - 9to5Mac</a></li>

</ul>
</details>

**社区讨论**: 社区反应不一：有人对性能飞跃感到兴奋，也有人注意到价格大幅上涨，不过有评论者指出，经通胀调整后价格与 Mac SE/30 时代大致相当。还有传言称，苹果可能会跳过 M6 Pro/Max/Ultra 版本，全力开发面向 AI 的 M7 芯片，据称消息来自 Bloomberg。

**标签**: `#Apple Silicon`, `#M6`, `#M5 Ultra`, `#AI compute`, `#Hardware`

---

<a id="item-2"></a>
## [OpenAI 自研芯片 Jalapeño 推理性能超越英伟达 Blackwell](https://newsletter.semianalysis.com/p/openai-jalapeno-better-than-nvidia) ⭐️ 9.0/10

OpenAI 公布了其首款自研推理 ASIC“Jalapeño”的首批测试结果，在 GPT-OSS 120B、DeepSeek R1 670B 和 Kimi K2.5 1T 等模型上，相比英伟达 GB300（Blackwell），单位功耗 AI 工作量提升 1.5–1.9 倍，端到端延迟降低 1.7–3.6 倍，高交互场景性能提升 2.1–4.1 倍。该芯片与博通合作开发，计划年底前部署于 OpenAI 自有数据中心。 这一成果动摇了英伟达在 AI 推理硬件领域的主导地位，表明定制 ASIC 在性能和总拥有成本（TCO）上可以超越顶级 GPU。它预示着大型 AI 实验室可能越来越多地自研芯片，从而重塑 AI 硬件市场，并可能整体降低推理成本。 该芯片额定功耗 700 瓦，实测持续功耗不高于 550 瓦。基准测试对标的是英伟达 GB300（Blackwell），未与刚开始出货的 Vera Rubin 比较，且 Jalapeño 不用于模型训练。OpenAI 表示第二代芯片已在深入开发，第三代正在设计。

hackernews · Semianalysis · 8月25日 14:06 · [社区讨论](https://news.ycombinator.com/item?id=49434378)

**背景**: ASIC（专用集成电路）是为特定工作负载定制设计的芯片，不同于通用 GPU。TCO（总拥有成本）不仅包括采购成本，还涵盖能耗、维护等全生命周期费用，因此每瓦效率至关重要。Nvidia 的 Blackwell 架构是用于 GB300 等数据中心加速器的 GPU 微架构，是 Hopper 的继任者，也是当前 AI 推理和训练硬件的基准。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Application-specific_integrated_circuit">Application-specific integrated circuit - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Blackwell_%28microarchitecture%29">Blackwell (microarchitecture) - Wikipedia</a></li>
<li><a href="https://www.ibm.com/think/topics/total-cost-of-ownership">What Is Total Cost of Ownership (TCO)? | IBM</a></li>

</ul>
</details>

**社区讨论**: 评论区讨论了这类芯片是否会让 GPU 更普及，并类比了早期 3dfx/Riva 等图形芯片的竞争格局；有评论指出各家芯片厂商普遍以 DeepSeek 和 Kimi 作为基准，反映了行业方向。还有人表示，按 token/焦耳计算，人类语音仍然比这些芯片节能约 22 倍；也有人推测 OpenAI 未来可能直接将模型权重固化到芯片中。

**标签**: `#AI hardware`, `#OpenAI`, `#ASIC`, `#Nvidia`, `#inference`

---

<a id="item-3"></a>
## [Vera Rubin NVL72 首测：AI 推理吞吐提升 30 倍](https://blogs.nvidia.com/blog/vera-rubin-nvl72-efficiency-ai-agents/) ⭐️ 9.0/10

英伟达首次公布下一代机柜级系统 Vera Rubin NVL72 的实测成绩：在运行 DeepSeek-V4-Pro 的智能体编码任务时，每兆瓦吞吐量较 GB300 最高提升 30 倍，每百万 Token 成本最高下降 35 倍。 这标志着 AI 基础设施正从独立 GPU 卡转向机柜级超级计算机，整个机柜如同一个巨型 GPU。这将大幅降低智能体 AI 的推理成本和延迟，并加剧 AI 基础设施领域的竞争。 Vera Rubin NVL72 在单个机柜中集成了 72 颗 Rubin GPU、36 颗 Vera CPU、NVLink 6 交换、ConnectX-9 SuperNIC、BlueField-4 DPU 以及液冷散热。英伟达还发布了 Groq 3 LPX 推理加速芯片（在 Gemma 4 31B 上实现每秒 3400 输出 Token）和专为智能体 AI 设计的 Vera CPU，其能效是传统机柜级 CPU 的两倍。

telegram · zaihuapd · 8月25日 14:48

**背景**: 传统 AI 服务器依赖通过网络连接的独立 GPU 加速器，这在智能体 AI 等需要计算、内存和网络紧密耦合的大规模负载中容易形成瓶颈。英伟达 Vera Rubin NVL72 将整个机柜视为一个巨型 GPU，集成了 72 颗 Rubin GPU 和 36 颗 Vera CPU，并采用 NVLink 6 和液冷散热。Vera CPU 负责代码执行、工具调用、沙箱和编排等 CPU 端工作，而 Groq 3 LPX 则是结合 GPU 与 LPU 优势的推理加速器，用于低延迟 Token 生成。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://benquan.hk/article-vera-rubin-nvl72.html">NVIDIA Vera Rubin NVL 72 Deep Dive 2026 | BENQUAN Global</a></li>
<li><a href="https://blogs.nvidia.com/blog/vera-rubin-lpx-spectrum-x-nvlink-fusion/">NVIDIA Advances Vera Rubin Inference With New LPX ... | NVIDIA Blog</a></li>
<li><a href="https://nvidianews.nvidia.com/news/nvidia-launches-vera-cpu-purpose-built-for-agentic-ai">NVIDIA Launches Vera CPU, Purpose-Built for Agentic AI | NVIDIA Newsroom</a></li>

</ul>
</details>

**标签**: `#NVIDIA`, `#AI hardware`, `#inference optimization`, `#data center`, `#Vera Rubin`

---

<a id="item-4"></a>
## [FDA 批准首款可同时监测血糖和酮体的可穿戴设备](https://www.fda.gov/news-events/press-announcements/fda-authorizes-first-wearable-device-continuously-monitors-both-ketone-levels-and-blood-sugar) ⭐️ 8.0/10

美国 FDA 批准了首款能同时持续监测血糖和酮体水平的可穿戴设备。这款设备让糖尿病患者通过一枚传感器即可跟踪两项指标，取代了以往分开的指尖采血检测。 这一里程碑意义重大，因为酮体监测对于预防糖尿病酮症酸中毒\(DKA\)这一危险并发症至关重要。血糖与酮体的联合传感可提供更早的预警，并简化数百万人的糖尿病管理，尤其是 1 型糖尿病患者。这也标志着连续代谢健康监测这一趋势正在兴起。 该设备在美国属首创，但类似的双传感技术已在欧洲获得 CE 标志\(例如 Abbott 的 Libre Duo 系统\)。与传统的尿酮试纸不同，连续酮体监测通过组织间液提供实时读数。报销和可及性仍是有待解决的问题。

hackernews · sunnynagra · 8月25日 19:07 · [社区讨论](https://news.ycombinator.com/item?id=49439017)

**背景**: 酮体是身体燃烧脂肪供能时产生的物质，水平过高可能预示着危及生命的糖尿病酮症酸中毒。此前，血糖通过连续血糖监测\(CGM\)设备持续监测，而酮体通常用尿酮试纸或指血检测。将两种传感器集成到一枚贴片上的可穿戴设备能提供更全面的代谢追踪。此前已有研究强调可穿戴酮体传感器在早期诊断 DKA 和指导个性化营养方面的潜力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://abbott.mediaroom.com/2026-05-27-Abbott-secures-CE-Mark-for-worlds-first-dual-glucose-ketone-sensing-technology-for-people-with-diabetes">Abbott secures CE Mark for world&#x27;s first dual glucose-ketone ...</a></li>
<li><a href="https://www.sciencedirect.com/science/article/pii/S0165993623000250">Ketone bodies detection: Wearable and mobile sensors for ...</a></li>
<li><a href="https://beyondtype1.org/ketone-monitoring-timeline/">From Urine Strips to Continuous Monitoring : The Evolution of Ketone ...</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍欢迎该设备，有人分享了因 DKA 失去亲友的经历，并对 1 型糖尿病儿童拥有更有效的工具表示期待。另一些人对无创传感的准确性表示怀疑，并质疑酮体数据对一般糖尿病患者的实用价值。还有人询问现有替代传感器及该技术已存在多长时间。

**标签**: `#FDA`, `#wearable`, `#health-tech`, `#diabetes`, `#ketone-monitoring`

---

<a id="item-5"></a>
## [苹果推出搭载 M5 Max 和 M5 Ultra 的新款 Mac Studio，主打本地 AI](https://www.apple.com/newsroom/2026/08/apple-introduces-new-mac-studio-with-m5-max-and-m5-ultra/) ⭐️ 8.0/10

苹果推出了搭载 M5 Max 和 M5 Ultra 芯片的全新 Mac Studio，这是迄今最强悍的桌面芯片。该机型提供最高 1.2 TB/s 的统一内存带宽，并被定位为一台‘本地 AI 性能猛兽’。 这次发布标志着苹果大举进军端侧 AI，可能让原本依赖云端 GPU 的工作负载转移到桌面端。开发者、研究人员和 AI 从业人员将获得一个高带宽、多核心的平台，用于在本地运行大语言模型及其他 AI 任务。 M5 Ultra 采用新一代 UltraFusion 技术，将两颗 M5 Max 芯片组合成四裸片架构；M5 Max 则提供 18 核 CPU 和最多 40 核 GPU。两款芯片都在每个 GPU 核心中集成了神经加速器以提升 AI 性能，内存配置预计最高可达 256GB 甚至更高。

hackernews · interpol\_p · 8月25日 13:03 · [社区讨论](https://news.ycombinator.com/item?id=49433316)

**背景**: Mac Studio 是介于 Mac mini 和 Mac Pro 之间的桌面工作站，面向创作者和专业用户设计。M5 系列是苹果下一代的 ARM 架构自研芯片，采用全新的 GPU 架构，并在每个核心中集成了专用的神经加速器；M 系列还使用统一内存，让 CPU 和 GPU 共享一个高带宽内存池。自 M1 Ultra 起，苹果就通过 UltraFusion 以低延迟、高吞吐的互连把多颗芯片连在一起，从而突破单芯片性能上限。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Apple_M5">Apple M5 - Wikipedia</a></li>
<li><a href="https://www.apple.com/newsroom/2026/08/apple-introduces-m6-and-m5-ultra-for-a-big-leap-in-performance-and-ai-compute/">Apple introduces M6 and M5 Ultra for a big leap in performance and AI compute - Apple</a></li>
<li><a href="https://www.macworld.com/article/2973459/2026-mac-studio-m5-release-date-specs-price-rumors.html">New Mac Studio M5 Max and M5 Ultra: Everything you need to know | Macworld</a></li>

</ul>
</details>

**社区讨论**: 评论者们持谨慎乐观态度，但也批评其定价，指出新闻稿中‘最高/高达’出现 46 次，而 256GB 内存版可能花费约 1 万美元。一些评论分析了超大模型的内存带宽上限，还有用户估算在 Ultra 上运行未量化的 DeepSeek V4 可达到每秒 1000+ token 的预填充和 50+ token 的生成速度。还有人希望苹果能预装并优化一个前沿开放权重模型，正好适配新硬件。

**标签**: `#Apple`, `#Mac Studio`, `#AI`, `#Hardware`, `#M5`

---

<a id="item-6"></a>
## [Nitter 项目收到停止函，实例暂停服务](https://github.com/zedeus/nitter/issues/1442) ⭐️ 8.0/10

Nitter 项目已收到停止与终止函，所有 Nitter 实例预计将在可预见的未来保持下线，团队正在等待法律建议。官方声明未提供关于发函方或法律依据的更多细节。 Nitter 是广泛使用的保护隐私的 X/Twitter 替代前端，此次法律行动威胁到用户在没有追踪、广告或账号的情况下自由访问 Twitter 内容的权利。这可能为其他替代前端树立先例，并加剧关于过度依赖 X 平台的争论。 官方声明称：“我们已收到停止与终止函。目前正在等待法律建议，但预计所有 Nitter 实例将在可预见的未来保持下线。”目前未透露法律依据或发函方的任何信息。

hackernews · Banditoz · 8月25日 17:08 · [社区讨论](https://news.ycombinator.com/item?id=49437283)

**背景**: Nitter 是一个免费开源的 Twitter/X 替代前端，注重隐私和性能，允许用户在没有追踪、广告或账号的情况下浏览主页、推文、搜索和 RSS 订阅。它旨在提供一种轻量且私密的方式来查看 Twitter 内容，但不支持登录或与帖子互动。这些背景解释了为什么 Nitter 对注重隐私的用户和记者很有价值，以及法律威胁为何意义重大。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Nitter">Nitter</a></li>
<li><a href="https://nitter.tiekoetter.com/about">nitter .tiekoetter.com</a></li>

</ul>
</details>

**社区讨论**: 社区评论表达了对许多机构仍依赖 X 进行沟通的不满，认为这让 Nitter 变得不可或缺，并希望这能推动人们离开 X。也有人建议中等强国应为这类项目提供法律保护，讨论将 X 上有价值的内容迁移到替代平台，并指出目前细节不足，同时猜测哪些司法管辖区可使停止函失效。

**标签**: `#nitter`, `#legal`, `#privacy`, `#open-source`, `#twitter`

---

<a id="item-7"></a>
## [火狐 157 将默认在所有平台启用 JPEG XL](https://groups.google.com/a/mozilla.org/g/dev-platform/c/3YMV4MS34KA?pli=1) ⭐️ 8.0/10

Firefox 157 将默认在所有平台上启用 JPEG XL 图像支持，这是面向下一代图像格式的重要一步。这一改动使 Firefox 成为最早默认提供该格式的主要浏览器之一。 浏览器采用 JPEG XL 可能推动该格式在 Web 上的广泛使用，由于 Chromium 也在采用该格式，这会带来跨浏览器的影响。网页开发者、摄影师和最终用户都将因这一更高效图像编解码器得到更广泛支持而受益。 该实现基于 Rust 语言的 jxl-rs 库，Chromium 也采用了该库，而 Apple 此前已经内置了 C++ 版 libjxl。一些用户还询问 Windows 7/8 等旧平台能否通过 Firefox 115 获得支持。

hackernews · yboris · 8月25日 17:55 · [社区讨论](https://news.ycombinator.com/item?id=49437946)

**背景**: JPEG XL 是由 JPEG 委员会、Google 和 Cloudinary 联合开发的下一代图像编码系统，被标准化为 ISO/IEC 18181。它同时支持有损与无损压缩，压缩效率明显优于传统 JPEG，并支持广色域、高动态范围和动画。该格式旨在成为 JPEG/JFIF 的长期继任者。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/JPEG_XL">JPEG XL</a></li>
<li><a href="https://jpeg.org/jpegxl/">JPEG - JPEG XL</a></li>

</ul>
</details>

**社区讨论**: 社区成员注意到 Firefox 和 Chromium 都使用了基于 Rust 的 jxl-rs，并好奇 Apple 的 C++ libjxl 及两者性能对比。一些用户希望浏览器在网站不支持 JXL 时提供便捷的自动转换方案，也有人询问 Windows 7/8 等旧平台能否获得支持。

**标签**: `#JPEG XL`, `#Firefox`, `#Web Standards`, `#Image Formats`, `#Browser`

---

<a id="item-8"></a>
## [SpaceX 宣布在路易斯安那州建设耗资 1000 亿美元的 Starbase LA 航天港](https://www.spacex.com/sites/starbase-la) ⭐️ 8.0/10

SpaceX 已正式确认将在路易斯安那州弗米利恩堂区（Vermilion Parish）建造 Starbase LA，这是一个自给自足的航天港，计划建设 10 个发射台。据报该项目投资达 1000 亿美元，将成为路易斯安那州历史上最大的资本投资。 这标志着 SpaceX 将发射基础设施从得克萨斯州和佛罗里达州大幅扩展，重点支持太阳同步轨道（SSO）发射和下一代星链（Starlink）卫星。该项目可能重塑当地经济和美国商业发射市场，同时也引发环境方面的担忧。 Starbase Louisiana 的 10 个发射台不仅用于推进剂输送，还将支持星舰（Starship）任务，包括发射 SpaceX 下一代星链卫星星座。该地点的发射角度相对赤道约为 98 度（向南发射），因此能高效进入太阳同步轨道。

hackernews · bilsbie · 8月25日 16:37 · [社区讨论](https://news.ycombinator.com/item?id=49436822)

**背景**: SpaceX Starbase 目前指该公司位于得克萨斯州布朗斯维尔附近的发射与生产基地，是星舰（Starship）火箭的主要开发中心，并于 2025 年正式成为得克萨斯州 Starbase 市。路易斯安那州的选址位于墨西哥湾沿岸弗米利恩堂区，是 SpaceX 扩大星舰发射能力的一部分；星舰是该公司火星殖民计划和大规模卫星部署的核心。环保组织此前曾就 Boca Chica 的星舰开发提起诉讼，如今类似的野生动植物与沿海栖息地问题也在路易斯安那引发关注。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/SpaceX_Starbase_%28spaceport%29">SpaceX Starbase (spaceport)</a></li>
<li><a href="https://www.space.com/space-exploration/private-spaceflight/spacex-announces-enormous-usd100-billion-starbase-louisiana-starship-launch-site">Starbase Louisiana: SpaceX announces enormous $100 billion ...</a></li>
<li><a href="https://lailluminator.com/2026/08/25/spacex-louisiana-2/">Musk plans $100 billion SpaceX launch site in coastal Louisiana</a></li>

</ul>
</details>

**社区讨论**: 评论者对新工作岗位和务实的工程雄心表示兴奋，有评论指出该建设项目可能为当地贫困的沿海地区带来 10 至 20 年的建筑行业工作机会。也有人对时间表和环境后果持怀疑态度，预测海岸会遭到破坏；还有评论者指出官方网页的部分段落几乎完全相同，疑似由大语言模型生成。

**标签**: `#SpaceX`, `#Starbase`, `#aerospace`, `#economic-development`, `#Louisiana`

---

<a id="item-9"></a>
## [EVE Online 启动向 Python 3 的长期迁移](https://simonwillison.net/2026/Aug/25/eve-online-move-to-python-3/) ⭐️ 8.0/10

EVE Online 宣布开始从 Stackless Python 2.7 迁移到 Python 3，该过程将对其 240 万行代码应用 futurize 脚本，随后手动审查行为差异。 这是有史以来规模最大、最复杂的 Python 2 到 3 迁移之一，将为其他仍在运行遗留 Python 代码的组织提供宝贵的实际案例。其结果可能影响社区处理大规模迁移的方式，以及依赖 Stackless 的项目如何规划未来。 迁移将依靠 futurize 来自动完成初步转换，但开发人员需要手动检查大约 2 万个 Python 2 与 Python 3 行为不同的位置，例如 &\#x27;/&\#x27; 运算符从整除变为真除法。该公告未说明将如何替代 Stackless，但此前的一次会议演讲描述了在 EVE Frontier 的 Carbon 引擎中用自定义调度器替代 Stackless 的做法。

rss · Simon Willison · 8月25日 22:59

**背景**: Stackless Python 是一个增强版解释器，通过微线程、tasklet 和 channel 提供轻量级并发；自 2003 年发布以来，它一直是 EVE Online 的核心组成部分。该游戏上一次升级运行时是在 2010 年，升级到 Stackless Python 2.7，而这一版本早已停止维护。Futurize 是一种广泛使用的自动化工具，它应用 2to3 修复器并添加兼容性导入，帮助代码库从 Python 2 迁移到 Python 3。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/stackless-dev/stackless/wiki/">Home · stackless-dev/stackless Wiki · GitHub</a></li>
<li><a href="https://python-future.org/futurize.html">futurize: Py2 to Py2/3 — Python-Future documentation</a></li>
<li><a href="https://en.wikipedia.org/wiki/Stackless_Python">Stackless Python</a></li>

</ul>
</details>

**标签**: `#Python`, `#Python 3`, `#EVE Online`, `#Migration`, `#Stackless Python`

---

<a id="item-10"></a>
## [SpaceX 计划 2027 年将英伟达 Vera Rubin NVL72 送入轨道](https://www.theregister.com/off-prem/2026/08/25/spacex-claims-it-will-put-a-vera-rubin-nvl72-rack-scale-system-into-orbit-next-year/5292067) ⭐️ 8.0/10

SpaceX 宣布计划于 2027 年将英伟达 Vera Rubin NVL72 机架级 AI 系统送入轨道，以验证太空数据中心技术。该系统包含 72 颗 Rubin GPU 和 36 颗 Vera CPU，功耗超过 100 千瓦。 这可能为太空数据中心和边缘 AI 铺平道路，有潜力实现卫星和航天器的在轨处理。此举标志着 SpaceX 与英伟达的重大合作，表明大规模 AI 计算在太空中或将成为可能。 SpaceX 尚未公布具体发射时间、轨道高度以及系统在太空中的供电和冷却方案。NVL72 通常需要复杂的液冷和供电基础设施，在轨道上还需解决辐射防护和通信等挑战。

telegram · zaihuapd · 8月25日 08:03

**背景**: 英伟达 Vera Rubin NVL72 是一款机架级 AI 超级计算机，将 72 颗新一代 Rubin GPU 和 36 颗 Vera CPU 集成在单台液冷机架中，通过 NVLink 6 互联。它专为高性能 AI 训练和推理设计，能提供显著的每瓦性能。将这样的系统送入太空，将测试地球级 AI 计算硬件能否在严苛的太空环境中运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nvidia.com/en-us/data-center/vera-rubin-nvl72/">Rack-Scale Agentic AI Supercomputer | NVIDIA Vera Rubin NVL72</a></li>
<li><a href="https://grokipedia.com/page/nvidia-vera-rubin-nvl72">NVIDIA Vera Rubin NVL72</a></li>

</ul>
</details>

**标签**: `#Space`, `#AI`, `#NVIDIA`, `#SpaceX`, `#Data Center`

---

<a id="item-11"></a>
## [GPT-5.6 Sol 设计定制 CPU 成功运行《毁灭战士》](https://www.tomshardware.com/tech-industry/artificial-intelligence/ai-coder-gets-doom-running-on-a-custom-cpu-designed-by-gpt-5-6-sol-game-viewport-is-overlaid-on-a-pulsing-schematic-of-the-cpu-in-turing-completes-sandbox-environment) ⭐️ 8.0/10

AI 爱好者 Angel 展示了 GPT-5.6 Sol 设计的定制 CPU「Codex-R32」，它在教育解谜游戏 Turing Complete 的沙盒模式中成功启动并运行了 1993 年的经典游戏《毁灭战士》。该 CPU 完全由基础逻辑门搭建，运行被编译为 RV32IM 机器码的 PureDOOM 移植版。 这一演示表明 AI 在硬件设计方面的能力正在增长，不再局限于生成代码，而是能从逻辑门出发构造可工作的处理器架构。它也提示 AI 辅助芯片设计可能会变得更加平民化，不过这仍只是小规模仿真，而非硅片制造层面的突破。 该 CPU 名为「Codex-R32」，面向 RV32IM 指令集，包含整数运算、乘法和内存访问指令。游戏画面叠加在处理器门级电路的实时脉冲示意图上；当网友调侃“下一步跑《孤岛危机》”时，AI 回答说需要先给它一块 GPU、几 GB 内存，再画一张从太空可见的电路图。

telegram · zaihuapd · 8月25日 15:23

**背景**: Turing Complete 是一款教育解谜游戏，玩家像从零组装硬件一样，用基础逻辑门搭建出一台可工作的计算机。PureDOOM 是一个单头文件（single-header）的《毁灭战士》C 语言移植版，设计目标就是方便移植到各种非主流平台。RV32IM 是 RISC-V 32 位基础指令集加上整数乘除扩展，指令集紧凑，很适合作为自定义 CPU 的实现目标。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/Daivuk/PureDOOM">GitHub - Daivuk/PureDOOM: Pure DOOM - Single Header Doom ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/RISC-V">RISC-V - Wikipedia</a></li>
<li><a href="https://steamcommunity.com/sharedfiles/filedetails/?id=3058316651">Steam Community :: Guide :: Turing Complete: All-level walkthrough</a></li>

</ul>
</details>

**标签**: `#AI`, `#Hardware Design`, `#GPT-5`, `#Turing Complete`, `#Doom`

---