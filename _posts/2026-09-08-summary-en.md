---
layout: default
title: "Horizon Summary: 2026-09-08 (EN)"
date: 2026-09-08
lang: en
---

> From 32 items, 5 important content pieces were selected

---

1. [LLM-guided evolution improves 10 circle-packing benchmarks](#item-1) ⭐️ 9.0/10
2. [TPU Inference Externalization Accelerates: InferenceX Shows Ironwood Up to 50% Better Per Dollar](#item-2) ⭐️ 8.0/10
3. [Measuring LLM Performance Drift with 31,352 Repeated Benchmark Runs](#item-3) ⭐️ 8.0/10
4. [Huawei Unveils Kirin 9050 Pro, Its First Logic-Folding Chip in Six Years](#item-4) ⭐️ 8.0/10
5. [China&\#x27;s Supreme Court Clarifies Liability in AI Disputes, Including Deepfakes](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [LLM-guided evolution improves 10 circle-packing benchmarks](https://www.reddit.com/r/MachineLearning/comments/1w9xlyi/llmguided_program_evolution_improves_10_bestknown/) ⭐️ 9.0/10

A system called Discovery Loop used LLM-guided program evolution to iteratively improve an optimization algorithm rather than solve circle packing directly. On the Packomania csqv benchmark, it improved the best-known sum-of-radii solutions for 10 values of N between 101 and 114 by 2.4% to 5.4%, within 15 iterations, at a total LLM cost of $27.72. This work demonstrates that LLMs can do more than generate code; they can autonomously discover algorithmic improvements that beat established benchmarks. Since Packomania independently verified and accepted the results, it offers a credible, low-cost path for AI-driven algorithm discovery and optimization. The system starts from a simple seed solver, and the LLM proposes algorithmic changes guided by a scoreboard of results and a history of prior attempts. Each candidate is scored by an independent verifier so improvements are kept and failures discarded; the author highlights the plateau-detection stopping rule as the piece they most want critiqued.

reddit · r/MachineLearning · /u/SIGH\_I\_CALL · Sep 7, 16:54

**Background**: The Packomania csqv benchmark is a classic circle-packing problem: maximize the sum of radii of N variable-radius circles packed in a unit square, often referred to as the sum-of-radii variant. LLM-guided program evolution is an emerging approach where large language models directly modify and propose code, guided by fitness feedback from scoring systems. Similar ideas, such as those in the LLM Guided Evolution framework, have been cited by DeepMind&\#x27;s AlphaEvolve and used to evolve neural network architectures with improved accuracy.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2609.05093">[2609.05093] LLM-Guided Program Evolution for Circle Packing: Breaking 10 Packomania Records for $28</a></li>
<li><a href="https://arxiv.org/html/2609.05093">LLM-Guided Program Evolution for Circle Packing:Breaking 10 Packomania Records for $28</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#program evolution`, `#optimization`, `#circle-packing`, `#benchmark`

---

<a id="item-2"></a>
## [TPU Inference Externalization Accelerates: InferenceX Shows Ironwood Up to 50% Better Per Dollar](https://newsletter.semianalysis.com/p/tpu-inferencex-full-steam) ⭐️ 8.0/10

SemiAnalysis published the first third-party inference benchmark results for Google&\#x27;s TPUv7 Ironwood through the InferenceX Official Preview. In apples-to-apples comparisons against NVIDIA B200/B300, Ironwood delivered up to 50% better performance per dollar, based on both Google&\#x27;s internal TCO and an external customer&\#x27;s TCO. This marks a rapid externalization of Google&\#x27;s TPU stack: Ironwood is the first TPU generation Google is actively selling or renting for others&\#x27; inference workloads, not just internal use. Such cost-performance gains could meaningfully reduce NVIDIA CUDA&\#x27;s competitive moat in the AI hardware ecosystem. The InferenceX benchmark spans much of the Pareto curve and evaluates economics from two perspectives: Google&\#x27;s internal total cost of ownership and the external TCO an actual customer pays. Note that the news tag says &\#x27;TPUv8i,&\#x27; but official documentation identifies Ironwood as the seventh-generation TPU, TPUv7.

rss · Semianalysis · Sep 7, 20:00

**Background**: TPUs are Google&\#x27;s custom application-specific integrated circuits \(ASICs\) designed for neural network workloads and are often used for inference with transformer-based LLMs. InferenceX is an open, reproducible benchmark suite from SemiAnalysis that continuously tracks GPUs, TPUs, LPUs, and software stacks as they evolve. Ironwood is purpose-built for high-volume, low-latency inference and is composed of two distinct chiplets, each with its own dedicated memory space. Google has said Ironwood will be generally available on Google Cloud and can also be purchased outright.

<details><summary>References</summary>
<ul>
<li><a href="https://newsletter.semianalysis.com/p/tpu-inferencex-full-steam">TPU Inference Externalization Full Steam Ahead - InferenceX</a></li>
<li><a href="https://docs.cloud.google.com/tpu/docs/tpu7x">TPU7x (Ironwood) | Google Cloud Documentation</a></li>
<li><a href="https://cloud.google.com/blog/products/compute/ironwood-tpus-and-new-axion-based-vms-for-your-ai-workloads">Ironwood TPUs and new Axion-based VMs for your AI workloads | Google Cloud Blog</a></li>

</ul>
</details>

**Tags**: `#TPU`, `#Inference`, `#AI Hardware`, `#CUDA`, `#Cloud Computing`

---

<a id="item-3"></a>
## [Measuring LLM Performance Drift with 31,352 Repeated Benchmark Runs](https://www.reddit.com/r/MachineLearning/comments/1w9llr4/measuring_llm_performance_drift_observations_and/) ⭐️ 8.0/10

The AI Stupid Level team conducted 31,352 repeated benchmark observations across 49 LLMs and found that between-day variance \(8.43 points\) is roughly three times within-day variance \(2.80 points\), suggesting models behind the same name change in ways static leaderboards miss. The work treats benchmarks as longitudinal time-series measurements rather than one-time rankings. This matters because API-served LLMs can silently change across versions, infrastructure, or configurations, so relying on static benchmark scores for model selection or production systems can be misleading. Longitudinal benchmarking offers a more trustworthy way to monitor drift, detect regressions, and validate behavior over time. The methodology keeps benchmark configurations versioned and only compares observations from compatible measurement conditions, using execution-based evaluation where possible rather than an LLM judge. It also separates availability and infrastructure failures from valid task outcomes and runs change detection over the resulting time series to flag genuine model drift.

reddit · r/MachineLearning · /u/ionutvi · Sep 7, 07:44

**Background**: Traditional LLM benchmarks are often snapshots: a model is evaluated once, a score is published, and that score is treated as a stable property. However, API-served models can change behind the same model name due to infrastructure, configuration, or version updates, so static leaderboard numbers may not reflect actual behavior over time. Longitudinal benchmarking instead tracks the same models repeatedly under versioned conditions and compares results against each model&\#x27;s own baseline. A related concern discussed in the post is benchmark contamination: publishing every live task, prompt transformation, or hidden test can change what the benchmark is actually measuring.

<details><summary>References</summary>
<ul>
<li><a href="https://data-today.net/llm-performance-drift-benchmark-variance/">LLM performance drift : why your benchmark scores... | Data Today</a></li>
<li><a href="https://www.logicmonitor.com/blog/llms-dont-stand-still-how-to-monitor-and-trust-the-models-powering-your-ai">How to Monitor and Trust the LLMs Powering Your AI | LogicMonitor</a></li>
<li><a href="https://arxiv.org/html/2508.05452v1">LLMEval-3: A Large-Scale Longitudinal Study on Robust and ...</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#benchmarking`, `#performance drift`, `#evaluation`, `#MLOps`

---

<a id="item-4"></a>
## [Huawei Unveils Kirin 9050 Pro, Its First Logic-Folding Chip in Six Years](https://www.news.cn/20260907/adf46c5c003240d28cc3cf6de54f9b5f/c.html) ⭐️ 8.0/10

On September 7, Huawei released the Mate XT 2 tri-fold phone, powered by the new Kirin 9050 Pro chip. This is the first high-performance chip to adopt logic folding technology and Huawei&\#x27;s first new flagship Kirin processor since the Mate 40 launch six years ago. This launch ends Huawei&\#x27;s six-year hiatus in flagship chip releases and marks a major step beyond traditional planar chip design. It could reshape expectations for post-Moore&\#x27;s-law semiconductor progress and strengthen Huawei&\#x27;s position against competitors in premium smartphones and advanced packaging. The Kirin 9050 Pro stacks logic cells in layers within a single chip and adds vertical interconnect channels, which shorten signal paths and reduce latency. The Mate XT 2 achieves a 42% performance improvement over the Mate XTs, thanks in part to wafer-to-wafer hybrid bonding that creates a dual-layer vertical architecture.

telegram · zaihuapd · Sep 7, 08:20

**Background**: Logic folding, introduced by Huawei at ISCAS 2026 alongside the Tao \(τ\) Law, falls under 3D integrated circuits and advanced packaging. It uses fine-grained dynamic reconfiguration and time multiplexing of hardware resources to address area-efficiency demands in the post-Moore era. Traditional chips place logic units on a single flat plane, while logic folding rearranges them vertically in a chip, similar to turning a one-story flat into a duplex with elevators connecting floors.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ithome.com/0/999/300.htm">华为继 Mate 40 后时隔六年再次发布高性能芯片，麒麟 9050 Pro 首发逻辑折叠技术 - IT之家</a></li>
<li><a href="https://i.ifeng.com/c/8w8hG82QYNl">全球首款逻辑折叠芯片！麒麟9050 Pro本月登场：华为三折叠首发_凤凰网</a></li>
<li><a href="https://zhuanlan.zhihu.com/p/2042626173432328269">陈巍：一文看懂逻辑折叠（logic folding）背后的关键技术和产业玩家</a></li>

</ul>
</details>

**Tags**: `#Huawei`, `#semiconductor`, `#Kirin`, `#smartphone`, `#technology`

---

<a id="item-5"></a>
## [China&\#x27;s Supreme Court Clarifies Liability in AI Disputes, Including Deepfakes](https://www.cnr.cn/news/20260907/t20260907_527806795.shtml) ⭐️ 8.0/10

On September 7, China&\#x27;s Supreme People&\#x27;s Court issued a judicial interpretation on AI dispute cases, comprising 24 articles in 5 parts that cover AI face-swapping, algorithmic price discrimination, unauthorized AI impersonation, autonomous driving, and intellectual property. The interpretation clarifies that using AI to create identifiable faces or voices without consent may constitute infringement of personality rights, and platforms engaging in algorithmic price discrimination that harms consumer rights must bear liability. This judicial interpretation establishes legal accountability for AI-related harms in China, setting influential precedents for deepfakes, algorithmic fairness, and AI impersonation. It will directly affect AI developers, tech platforms, and companies operating in or with China, and may shape global AI governance debates by demonstrating a top-down regulatory approach. The interpretation explicitly supports punitive damages when AI impersonates a person for endorsement and induces consumption. It also regulates the use of AI to commit privacy violations such as &\#x27;kaihe&\#x27; \(online doxxing\) and &\#x27;human flesh search&\#x27;, applying existing legal principles to AI-driven misconduct.

telegram · zaihuapd · Sep 7, 09:32

**Background**: Chinese law already addresses algorithmic price discrimination, which refers to platforms charging loyal or existing customers higher prices than new users, and &\#x27;kaihe&\#x27;, a form of cyberviolence where personal information is illegally obtained and publicly exposed, evolving from the older practice of &\#x27;human flesh search&\#x27;. Punitive damages are compensation awarded beyond actual losses to punish especially egregious conduct. This interpretation updates these existing legal concepts to cover AI-specific scenarios such as deepfakes, AI impersonation, and biased algorithmic pricing, filling gaps in a fast-evolving technological landscape.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bswxw.org.cn/web/article/1493984301637644288/web/content_1493984301637644288.html">莫让 算 法 “ 杀 熟 ”寒了人心-璧山网</a></li>
<li><a href="https://baike.baidu.com/item/%E5%BC%80%E7%9B%92/58943997">开盒（网络热词）_百度百科</a></li>
<li><a href="https://zh.wikipedia.org/zh-hans/%E6%87%B2%E7%BD%B0%E6%80%A7%E8%B3%A0%E5%84%9F">惩罚性赔偿 - 维基百科，自由的百科全书</a></li>

</ul>
</details>

**Tags**: `#AI governance`, `#legal regulation`, `#deepfake`, `#algorithmic fairness`, `#privacy`

---