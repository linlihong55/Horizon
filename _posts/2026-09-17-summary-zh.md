---
layout: default
title: "Horizon Summary: 2026-09-17 (ZH)"
date: 2026-09-17
lang: zh
---

> 从 36 条内容中筛选出 3 条重要资讯。

---

1. [Nvidia 推出两条官方 Rust 编写 CUDA GPU 内核的路径](#item-1) ⭐️ 8.0/10
2. [Flock 车牌识别摄像头被曝存在硬编码凭证等严重漏洞](#item-2) ⭐️ 8.0/10
3. [TMLR 约谈 10 篇拟被直接拒稿论文的作者，多数人无法解释自己的论文](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Nvidia 推出两条官方 Rust 编写 CUDA GPU 内核的路径](https://developer.nvidia.com/blog/introducing-cuda-rust-two-tracks-for-writing-gpu-kernels/) ⭐️ 8.0/10

Nvidia 宣布了两条用 Rust 编写原生 CUDA GPU 内核的官方路径：一是 cuda-oxide，它通过自定义的 rustc 代码生成后端，借助 Pliron IR 框架和 LLVM 将 SIMT 风格的 Rust 内核直接编译为 PTX；二是 cutile-rs，它在稳定版 Rust 中通过 CUDA Tile IR 的即时编译实现基于 tile 的 GPU 编程。这两种方案都在编译期而非运行期强制保证内存安全。 这是 Nvidia 首次为 Rust 的 GPU 内核开发提供一等公民式的官方支持路径，可能改变相当一部分 GPU 代码的编写方式，并降低长期以来把 Rust 工作负载束缚在 C++ CUDA 上的阻力。这也会增强整个 Rust 机器学习技术栈，尤其是 HuggingFace 的 Candle 等推理框架。 cuda-oxide 依靠 DisjointSlice 和启动契约（launch contracts）来防止别名问题，cutile-rs 则通过张量分区和所有权来保证对内存区域的独占访问。一个值得注意的设计选择是内核启动是「被检查」而非「被信任」的，也就是说宿主端编译器会验证每次启动的安全前提，而不是默认程序员已经处理正确。

hackernews · nonmaskable · 9月16日 11:15 · [社区讨论](https://news.ycombinator.com/item?id=49724881)

**背景**: CUDA 内核是在大量 GPU 线程上并行执行的函数；在传统的 CUDA C++ 中它用 \_\_global\_\_ 修饰符标记，接收指向设备全局内存的指针，通常直接修改内存而不返回值。Rust 是一门系统编程语言，其借用检查器和所有权规则能在编译期提供内存安全保证，这对容易出现数据竞争和别名问题的 GPU 代码很有吸引力。Candle 是 HuggingFace 推出的极简 Rust 机器学习框架，主打性能和 GPU 支持，是 Rust 推理工具链的关键一环，而原生 CUDA 内核有望为其加速。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/introducing-cuda-rust-two-tracks-for-writing-gpu-kernels/">Introducing CUDA Rust: Two Tracks for Writing GPU Kernels | NVIDIA Technical Blog</a></li>
<li><a href="https://github.com/huggingface/candle">GitHub - huggingface / candle : Minimalist ML framework for Rust</a></li>
<li><a href="https://cvw.cac.cornell.edu/gpu-architecture/gpu-characteristics/kernel_sm">Cornell Virtual Workshop &gt; Understanding GPU Architecture &gt; GPU Characteristics &gt; Kernels and SMs</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论（221 分、75 条评论）总体热情高涨，但对 Nvidia 的专有生态持怀疑态度：有评论者（jacobgorm）认为一旦 CUDA 进入代码库就很难清除，最终要么被单一厂商锁定，要么陷入 \#ifdef 地狱，因此主张像 Metal、OpenCL、D3D12 那样把内核写在独立文件中并手动启动。也有人（Driftbench）看好 Rust 的安全性能为内核编程带来变革，dllu 则把这条新闻与 HuggingFace 的 Candle 推理库联系起来；此外，claiir 和 LarsDu88 等评论者略带讽刺地指出，连 Nvidia 的公告似乎也大量由大语言模型撰写，不过其中一位表示这反而重新激起了自己学习 Rust 的兴趣，因为 LLM 尚未针对这些新内容训练过。

**标签**: `#Rust`, `#CUDA`, `#GPU Programming`, `#Nvidia`, `#Systems Programming`

---

<a id="item-2"></a>
## [Flock 车牌识别摄像头被曝存在硬编码凭证等严重漏洞](https://www.wired.com/story/hackers-flock-camera-data-shows-how-system-works/) ⭐️ 8.0/10

安全研究员 Micah Lee 报告称，Flock Safety 的车牌识别监控摄像头存在大量安全漏洞，其中包括一个硬编码的 API 密钥，攻击者可借此请求到以明文存储的凭证，从而有可能访问 Flock 的服务器。该报道与 404 Media 合作完成，同时 Distributed Denial of Secrets 公布了摄像头的分区镜像。 这一事件已成为物联网与监控设备安全争论的焦点，因为部署在公共空间的摄像头，其威胁模型本就明确包含攻击者的物理接触。它也凸显出：企业可以通过制定漏洞披露政策来营造&quot;负责任安全姿态&quot;的表象，却在实际上抑制有价值的漏洞报告。 涉事的硬编码凭证是一个 API 密钥，而非管理员密码，它可被用来获取以明文存储的凭证；目前尚不清楚攻击者以摄像头身份成功认证后究竟能做什么。Flock 的漏洞披露政策虽表示欢迎漏洞报告，但排除了需要与设备或服务&quot;交互&quot;或下载其数据的情形——这一豁免几乎把真正有意义的硬件测试全部排除在外。

hackernews · driverdan · 9月16日 13:18 · [社区讨论](https://news.ycombinator.com/item?id=49726586)

**背景**: Flock Safety 生产自动车牌识别摄像头（ALPR），这类 AI 摄像头会扫描每一辆经过车辆的车牌与特征，并将数据与失窃车辆数据库、AMBER 警报等名单比对。硬编码凭证是典型的漏洞类型（CWE-798）：由于密钥被写死在固件中，除非重新部署或重新刷写设备，否则无法轮换。漏洞披露政策是研究人员向厂商报告缺陷的正式流程，其覆盖范围决定了正当的安全研究是被欢迎还是被法律手段劝阻。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://trafficvision.live/blog/flock-cameras">Flock Cameras : What They Are &amp; Can You Watch... | TrafficVision.Live</a></li>
<li><a href="https://cwe.mitre.org/data/definitions/798.html">CWE - CWE-798: Use of Hard - coded Credentials (4.20)</a></li>
<li><a href="https://www.bugcrowd.com/blog/vulnerability-disclosure-policy-what-is-it-why-is-it-important/">Vulnerability Disclosure Policy : What is It &amp; Why is it... | @Bugcrowd</a></li>

</ul>
</details>

**社区讨论**: 评论区整体态度严厉：有人称硬编码凭证是&quot;完全无能的标志&quot;；有人批评 Flock 的漏洞披露政策主要是为了营造负责任安全的表象；还有人把问题归咎于懒惰和&quot;缩短上市时间&quot;，忽视了公共空间硬件必然面临本地物理接触这一现实。也有人提到此次与 404 Media 的合作，以及 Distributed Denial of Secrets 已公开摄像头分区镜像，一位评论者感叹这些数据&quot;简直就摆在那里，任何未经授权的人走过去就能拿走&quot;。

**标签**: `#security`, `#IoT`, `#surveillance`, `#vulnerabilities`, `#privacy`

---

<a id="item-3"></a>
## [TMLR 约谈 10 篇拟被直接拒稿论文的作者，多数人无法解释自己的论文](https://www.reddit.com/r/MachineLearning/comments/1wid67h/tmlr_reached_out_to_the_authors_of_10_papers/) ⭐️ 8.0/10

TMLR（Transactions on Machine Learning Research）的联席主编联系了 10 篇原本将被直接拒稿（desk rejection）的投稿作者，要求他们解释自己提交的论文。结果是：1 篇作者主动撤稿，1 篇以其他事务为由表示无法参加，1 篇约好了会议却未出席，3 篇作者无法回答关于论文的基本问题，3 篇作者能谈高层思路但在被追问技术细节时出现困难，只有 1 篇作者回答了全部问题——但访谈者仍在该论文中发现了一处重大缺陷。 这是第一手证据，表明进入机器学习同行评审环节的投稿中有相当比例可能由大语言模型生成或出自论文工厂，直接威胁到整个研究界赖以运转的评审体系的可信度。它也为期刊提供了一种具体且低成本的筛查手段，并把“作者责任”推到如何监管 AI 辅助写作这一争论的中心。 所用的方法只是围绕投稿进行一次对话，因此依赖的是编辑的时间投入而非任何技术工具，并且它本身并不能证明论文由大语言模型撰写——它主要暴露的是那些对自己论文主张并不真正熟悉的作者。值得注意的是，即便是唯一一位对答如流的作者，其论文仍被发现存在重大缺陷，这说明通过这种访谈并不能等同于论文具备科学质量。

reddit · r/MachineLearning · /u/hihey54 · 9月16日 23:20

**背景**: TMLR 是 2021 年底为补充 JMLR 而创办的机器学习期刊，采用 OpenReview 平台与滚动评审流程；所谓“直接拒稿（desk rejection）”是指编辑在送交同行评审之前就直接拒掉投稿，通常出于范围、格式或质量方面的原因。论文工厂（paper mill）是指批量生产并出售科学手稿（往往数据造假或抄袭）的机构，客户是那些面临“不发表就淘汰”压力的研究者。随着生成模型变得廉价且强大，编辑们越来越担心这类手稿——乃至完全由大语言模型撰写的论文——正越来越多地绕过初审。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://jmlr.org/tmlr/">Transactions on Machine Learning Research (TMLR)</a></li>
<li><a href="https://en.wikipedia.org/wiki/Research_paper_mill">Research paper mill - Wikipedia</a></li>
<li><a href="https://www.aischolar.com/news/article/is-desk-rejection-common">Is Desk Rejection Common?</a></li>

</ul>
</details>

**标签**: `#peer-review`, `#research-integrity`, `#LLM-generated-papers`, `#machine-learning`, `#academic-publishing`

---