---
layout: default
title: "Horizon Summary: 2026-08-18 (EN)"
date: 2026-08-18
lang: en
---

> From 31 items, 6 important content pieces were selected

---

1. [Mojo programming language open-sourced under Apache 2.0](#item-1) ⭐️ 9.0/10
2. [Qwen 3.8 27B scores 52 on AI Index, matching GPT-5.6 Luna](#item-2) ⭐️ 9.0/10
3. [Seth Godin: Amazon&\#x27;s ad-driven search imposes a &\#x27;tax&\#x27; on consumers](#item-3) ⭐️ 8.0/10
4. [Linux 7.3 Improves Performance When VRAM Runs Out](#item-4) ⭐️ 8.0/10
5. [China Orders Early Removal of Custom Windows 10 from State Agencies](#item-5) ⭐️ 8.0/10
6. [China&\#x27;s Homegrown AI Chips to Take ~90% of Domestic Market by 2026](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Mojo programming language open-sourced under Apache 2.0](https://simonwillison.net/2026/Aug/18/mojo-is-now-open-source/) ⭐️ 9.0/10

On August 18, 2026, Modular released Mojo&\#x27;s compiler and toolchain under the Apache 2.0 license, following the release of Mojo 1.0 the previous week. The language is now fully open source on Linux and macOS. This fulfills the long-standing open source promise made when Mojo launched in May 2023, making it a credible open alternative for high-performance, Python-adjacent computing. It could reshape AI/ML systems programming by offering a Rust-inspired language with Python-like syntax, built on MLIR for GPU and TPU acceleration. Mojo was originally intended to be a superset of Python, but around August 2025 the project changed direction, and Mojo is now its own language with Python-inspired syntax rather than full compatibility. It builds on the MLIR compiler framework, allowing it to target CPUs, GPUs, TPUs, and other accelerators, and includes features like static typing and a borrow checker inspired by Rust.

rss · Simon Willison · Aug 18, 21:39

**Background**: Mojo is a programming language created by Modular, designed to combine Python&\#x27;s ease of use with systems-level performance. It was announced in May 2023 with a commitment to eventually open source the compiler. The language uses syntax reminiscent of Python while incorporating systems programming concepts such as ownership and borrow checking, similar to Rust. By building on MLIR instead of directly on LLVM, Mojo can generate highly optimized code for a variety of hardware accelerators.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mojo_%28programming_language%29">Mojo (programming language)</a></li>
<li><a href="https://mojolang.org/">Mojo</a></li>

</ul>
</details>

**Tags**: `#Mojo`, `#programming language`, `#open source`, `#compiler`, `#AI/ML`

---

<a id="item-2"></a>
## [Qwen 3.8 27B scores 52 on AI Index, matching GPT-5.6 Luna](https://simonwillison.net/2026/Aug/17/qwen-38-27b-scores-52/) ⭐️ 9.0/10

Qwen 3.8 27B, a 27-billion-parameter model, scored 52 on the Artificial Analysis Intelligence Index, the same score as GPT-5.6 Luna \(max\) and just one point behind GLM-5.2 \(753B\) and DeepSeek V4 Pro \(1.7T\). The result highlights a dramatic efficiency breakthrough for a relatively small open-weights model. This is a major efficiency breakthrough: a 27B model rivaling models with hundreds of billions or even 1.7 trillion parameters suggests that scale is not the only path to intelligence. It could lower deployment costs, democratize access to frontier-level AI, and reshape assumptions about model development. The Artificial Analysis Intelligence Index is a weighted average of production benchmark scores scaled from 0 to 100, with v4.1 assigning 34% weight to agents, 24% to coding, 24% to scientific reasoning, and 18% to general tasks. Qwen 3.8 27B&\#x27;s exact score of 52 ties with GPT-5.6 Luna, whose parameter count is undisclosed but presumably far larger.

rss · Simon Willison · Aug 17, 23:58

**Background**: The Artificial Analysis Intelligence Index evaluates AI models on a 0–100 scale by combining scores on benchmarks such as agents, coding, scientific reasoning, and general knowledge. Historically, higher intelligence scores have strongly correlated with model scale, so small models typically underperform large frontier systems. Qwen 3.8 27B&\#x27;s near-top score with a fraction of the parameters breaks this pattern and suggests that efficient architectures and training methods are advancing rapidly.

<details><summary>References</summary>
<ul>
<li><a href="https://artificialanalysis.ai/evaluations/artificial-analysis-intelligence-index">Artificial Analysis Intelligence Index | Artificial Analysis</a></li>
<li><a href="https://artificialanalysis.ai/">AI Model &amp; API Providers Analysis | Artificial Analysis</a></li>

</ul>
</details>

**Tags**: `#AI`, `#LLM`, `#Qwen`, `#benchmark`, `#model efficiency`

---

<a id="item-3"></a>
## [Seth Godin: Amazon&\#x27;s ad-driven search imposes a &\#x27;tax&\#x27; on consumers](https://seths.blog/2026/08/the-amazon-tax/) ⭐️ 8.0/10

Seth Godin&\#x27;s blog post &\#x27;The Amazon tax&\#x27; argues that Amazon&\#x27;s search results are increasingly distorted by advertising and the platform&\#x27;s own commercial interests, costing consumers time and freedom of choice. This matters because Amazon is a dominant shopping search engine, and its shift from relevance to ad-driven rankings affects millions of buyers daily. It also highlights broader concerns about platform self-preferencing and the degradation of search quality across big tech. Seth Godin uses the metaphor of a &\#x27;tax&\#x27; to describe the hidden cost of wading through sponsored and irrelevant results. The post has generated 503 comments, reflecting strong reader engagement with the issue.

hackernews · herbertl · Aug 18, 13:22 · [Discussion](https://news.ycombinator.com/item?id=49345263)

**Background**: Amazon&\#x27;s product search is powered by the A9 algorithm, whose primary goal is to match customers with products they are most likely to buy. However, ranking factors include sponsored placements and sales performance, which can push organic relevance aside. Regulators and researchers have also examined &\#x27;self-preferencing&\#x27; by dual-role platforms, where a platform that also sells its own products may favor them in recommendations over third-party offers.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/A9.com">A9.com - Wikipedia</a></li>
<li><a href="https://myamazonguy.com/seo/amazon-a9-search-engine/">Amazon A9 Algorithm | What It Is and How It Works</a></li>
<li><a href="https://arxiv.org/pdf/2303.14947">Measuring Self-Preferencing on Digital Platforms - arXiv.org</a></li>

</ul>
</details>

**Discussion**: Commenters largely agree with Godin, noting that search has shifted from finding exact items to surfacing platform-chosen results. Some share personal experiences of shifting purchases to local shops or other platforms due to declining quality, while one commenter sees potential value in relevant ads, comparing them to Google search ads.

**Tags**: `#Amazon`, `#search`, `#advertising`, `#platform economics`, `#consumer behavior`

---

<a id="item-4"></a>
## [Linux 7.3 Improves Performance When VRAM Runs Out](https://pixelcluster.dev/VRAM-Overcommit/) ⭐️ 8.0/10

The article reports that Linux 7.3 introduces performance improvements for VRAM overcommit scenarios, aiming to reduce stutters and improve frametimes when GPU memory is exhausted. It also discusses possible kernel-side strategies such as better memory allocation hints and virtual memory defragmentation. As GPU memory becomes a bottleneck for AI training, gaming, and rendering, better VRAM overcommit handling can significantly improve user experience on systems with limited video memory. This is especially relevant for Linux users who rely on open-source drivers and want to push their hardware further. The article, titled &\#x27;VRAM Management Part 2: Beyond the Limits&\#x27;, notes that the experience under VRAM overcommit can still be hit-or-miss, with frametimes varying depending on the objects in the scene. The author suggests that applications are best positioned to inform the kernel about which memory allocations should remain resident in VRAM.

hackernews · flaburgan · Aug 18, 07:51 · [Discussion](https://news.ycombinator.com/item?id=49342719)

**Background**: VRAM overcommit allows GPU applications to use more video memory than physically present by moving pages between VRAM and system RAM. This paging process is traditionally slow and can cause stutters, especially in games and ML workloads. The Linux kernel has been evolving its memory management and GPU paging algorithms to make this process more seamless, and the article examines what Linux 7.3 brings to this area.

<details><summary>References</summary>
<ul>
<li><a href="https://pixelcluster.dev/VRAM-Overcommit/">VRAM Management Part 2: Beyond the Limits... | pixelcluster&#x27;s GPU blog</a></li>
<li><a href="https://www.cs.unc.edu/~anderson/papers/rtss22c.pdf">Enabling GPU Memory Oversubscription via</a></li>

</ul>
</details>

**Discussion**: Commenters are generally enthusiastic about the improvements, with one calling the article &\#x27;well written and very informative&\#x27; and another eagerly awaiting the 7.3 release after being impressed by 7.2. Some express frustration that Nvidia drivers still lack proper GPU paging support, while one commenter argues that applications themselves should provide memory residency hints to the kernel. There is also a remark expressing gratitude for contributions from young trans people to low-level performance engineering.

**Tags**: `#Linux`, `#kernel`, `#VRAM`, `#performance`, `#memory-management`

---

<a id="item-5"></a>
## [China Orders Early Removal of Custom Windows 10 from State Agencies](https://www.bloomberg.com/news/articles/2026-08-18/china-axing-microsoft-windows-from-state-agencies-ahead-of-plan) ⭐️ 8.0/10

China&\#x27;s Ministry of State Security has ordered some government agencies to uninstall customized Windows 10 months ahead of the scheduled February 2027 phase-out, citing data security concerns. Microsoft said it has found no security incidents affecting the product and that it still receives regular security updates. This acceleration signals rising cybersecurity distrust toward foreign software in China&\#x27;s state sector, with implications for Microsoft&\#x27;s government business and global tech supply chains. It also reflects broader efforts to promote domestic alternatives in critical infrastructure. The customized Windows 10 is the China Government Edition developed via the CMIT joint venture with CETC in 2017, designed to give government customers more control over security and telemetry. The order came from the Ministry of State Security, but the specific vulnerabilities or reasons were not disclosed.

telegram · zaihuapd · Aug 18, 06:22

**Background**: Windows 10 China Government Edition was announced in 2017 and preinstalled by Lenovo and others for Chinese government customers, with features tailored to local security and compliance requirements. Microsoft Windows 10 reached end of support in October 2025, but the Chinese government had planned a separate phase-out by February 2027. The new order instructs some agencies to remove it earlier than planned.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Windows_10_China_Government_edition">Windows 10 China Government edition</a></li>
<li><a href="https://blogs.windows.com/windowsexperience/2017/05/23/announcing-windows-10-china-government-edition-new-surface-pro/">Announcing Windows 10 China Government Edition and the new Surface Pro | Windows Experience Blog</a></li>

</ul>
</details>

**Tags**: `#China`, `#Microsoft`, `#Cybersecurity`, `#Government Policy`, `#Windows 10`

---

<a id="item-6"></a>
## [China&\#x27;s Homegrown AI Chips to Take ~90% of Domestic Market by 2026](https://www.tomshardware.com/tech-industry/artificial-intelligence/chinas-homegrown-ai-accelerators-to-supply-90-percent-of-the-countrys-domestic-market-analysts-suggest-cambricon-and-huawei-expected-to-be-the-biggest-winners-in-the-shift-away-from-nvidia-and-amd) ⭐️ 8.0/10

TrendForce predicts Chinese domestic AI accelerators will supply nearly 90% of China&\#x27;s market by 2026, up from 45% last year. Cambricon and Huawei are expected to be the biggest winners in this shift away from Nvidia and AMD. This marks a major strategic shift in China&\#x27;s AI chip supply, driven by US export controls and geopolitical tensions. It could reshape the global AI chip market and accelerate China&\#x27;s push for semiconductor self-sufficiency. In 2025, Nvidia held a 55% share of China&\#x27;s market with 2.2 million units shipped, while Huawei shipped 812,000 units, a 20.3% share. China would need to boost high-end AI chip production by 2.2 times to about 1.96 million units within a year, though capacity remains uncertain.

telegram · zaihuapd · Aug 18, 13:03

**Background**: An AI accelerator, also known as a neural processing unit, is specialized hardware designed to speed up AI and machine learning tasks such as deep learning and computer vision. Cambricon is a partially state-owned Chinese company headquartered in Beijing that designs AI chips for cloud and edge computing. The forecast reflects the impact of US export restrictions on advanced chips, prompting China to cultivate domestic suppliers like Cambricon and Huawei.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cambricon_Technologies">Cambricon Technologies - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/AI_accelerator">Neural processing unit - Wikipedia</a></li>
<li><a href="https://www.ibm.com/think/topics/ai-accelerator">What is an AI accelerator? | IBM</a></li>

</ul>
</details>

**Tags**: `#AI chips`, `#China`, `#Huawei`, `#Cambricon`, `#semiconductors`

---