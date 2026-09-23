---
layout: default
title: "Horizon Summary: 2026-09-23 (EN)"
date: 2026-09-23
lang: en
---

> From 42 items, 10 important content pieces were selected

---

1. [OpenAI Releases GPT-6 Sol and Luna With Sharper Pricing](#item-1) ⭐️ 10.0/10
2. [Anthropic Releases Claude Opus 5.5 With Lower Pricing](#item-2) ⭐️ 9.0/10
3. [Pentagon: AI Overreliance Blamed in Strike on Iranian School](#item-3) ⭐️ 9.0/10
4. [Claude Opus 5.5 and GPT-6 Sol/Luna Launch, Sparking a Price War](#item-4) ⭐️ 9.0/10
5. [vLLM v0.30.0 ships 762 commits, new models, and Fast Start weight cache](#item-5) ⭐️ 8.0/10
6. [Hackers claim to hold data on all FBI employees, threaten coercion](#item-6) ⭐️ 8.0/10
7. [Artificial Analysis Benchmarks Claude Opus 5.5 at Max Reasoning Setting](#item-7) ⭐️ 8.0/10
8. [WordPress patches unauthenticated path traversal flaw enabling conditional RCE](#item-8) ⭐️ 8.0/10
9. [DeepSeek and Tsinghua publish DSec sandbox platform report: 3M sandboxes per day for agent training](#item-9) ⭐️ 8.0/10
10. [China Probes DeepSeek and Moonshot Over Alleged Claude Data Leaks](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI Releases GPT-6 Sol and Luna With Sharper Pricing](https://openai.com/index/introducing-gpt-6-sol-and-luna/) ⭐️ 10.0/10

OpenAI introduced GPT-6 Sol and Luna, two new models in its flagship GPT-6 series, available through the API as gpt-6-sol and gpt-6-luna. According to OpenAI and early coverage, Sol makes roughly half as many mistakes as GPT-5.6, while Luna matches the performance of previously higher-tier models at a far lower cost — including being priced at about half of GPT-5.6 Luna. The release shifts the competitive conversation from raw capability to price-performance: if a cheaper tier can match last generation&\#x27;s top-end accuracy, developers can run far more agentic, high-volume workloads for the same budget. It also raises the stakes in the ongoing rivalry with rival coding and agent offerings, since per-token cost and usage limits increasingly decide which model teams standardize on. Sol is positioned as the higher-accuracy flagship that halves GPT-5.6&\#x27;s error rate, while Luna is the fast, cost-efficient tier aimed at high-volume and latency-sensitive work such as chat, classification, and lightweight agentic tasks. Practically, the lower input/output prices feed directly into subscription usage limits, which is the dimension users say they feel most in day-to-day work.

hackernews · OfficialTurkey · Sep 22, 18:00 · [Discussion](https://news.ycombinator.com/item?id=49805509)

**Background**: GPT models are large language models \(LLMs\) — neural networks, typically based on the transformer architecture, trained on massive text corpora to predict and generate language, then fine-tuned to act as assistants such as ChatGPT. OpenAI has historically split its lineup into a stronger but pricier flagship and a cheaper, faster sibling, so GPT-6 Sol and Luna continue that two-tier pattern as successors to the GPT-5.6 generation. Because these models are accessed mainly through paid APIs and subscription plans, pricing and usage limits matter as much to developers as benchmark scores do.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/introducing-gpt-6-sol-and-luna/">Introducing GPT - 6 Sol and Luna | OpenAI</a></li>
<li><a href="https://www.zdnet.com/innovation/openai-gpt-6-sol-luna-release/">OpenAI &#x27;s GPT - 6 Sol doubles its accuracy rate - for half the... - ZDNET</a></li>
<li><a href="https://openrouter.ai/openai/gpt-6-luna">GPT - 6 Luna - API Pricing &amp; Benchmarks | OpenRouter</a></li>

</ul>
</details>

**Discussion**: The Hacker News thread \(1149 points, 595 comments\) is broadly enthusiastic, with Simon Willison calling Luna&\#x27;s half-price positioning &\#x27;a really big deal&\#x27; and sharing side-by-side &\#x27;pelican&\#x27; SVG generation tests across models. Other commenters are more ambivalent: one describes an almost colleague-like attachment to GPT-5.6 Sol and worries a technically better successor may feel less natural, while another weighs Codex Pro 20x against Claude Code 20x and concludes Codex wins largely on usage limits and unmetered ChatGPT access, and a third argues that for average users ChatGPT Plus has felt essentially limitless since 5.6.

**Tags**: `#OpenAI`, `#GPT-6`, `#LLM`, `#AI models`, `#release`

---

<a id="item-2"></a>
## [Anthropic Releases Claude Opus 5.5 With Lower Pricing](https://www.anthropic.com/claude-opus-5-5) ⭐️ 9.0/10

Anthropic released Claude Opus 5.5, the first model in its Claude 5.5 series, with significant price reductions across every token category: input tokens drop from $5 to $4 per million, output tokens from $25 to $20, cache reads from $0.50 to $0.20, and cache writes from $6.25 to $5. Anthropic also claims the model communicates more naturally and writes more clearly than Opus 5, with early testers saying its writing is clearer and easier to follow. A price cut on a top-tier frontier model signals that even the leading labs are now competing on cost, not just raw capability, as cheap open-weight alternatives such as DeepSeek squeeze margins from below. For developers and enterprises that route large volumes of traffic through APIs, the lower token and cache pricing directly reduces operating costs and could shift model-selection decisions across the industry. The announcement frames the improved communication style as a safety benefit as well as a practical one, arguing that clearer, front-loaded output is easier for users to follow and check. Context for the pricing move: Opus 5 was reportedly the highest-spend model on OpenRouter&\#x27;s rankings, suggesting a large existing base of paying users that Anthropic is trying to retain as rivals undercut it.

hackernews · km144 · Sep 22, 16:29 · [Discussion](https://news.ycombinator.com/item?id=49803892)

**Background**: Frontier models are the most advanced general-purpose AI systems available at a given time, typically large language models trained on massive datasets at costs that can reach hundreds of millions of dollars, and they represent the leading edge of AI capability. API access to such models is usually billed per token — a token being a small chunk of text — with separate rates for input \(what you send\), output \(what the model generates\), and cached context, where previously processed text is stored so it can be reused more cheaply on subsequent calls. OpenRouter is a marketplace that routes requests across many models and publishes usage and spending rankings, which is why its data is often cited as a proxy for real-world model adoption.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Frontier_model">Frontier model</a></li>
<li><a href="https://www.nvidia.com/en-us/glossary/frontier-models/">What Are Frontier AI Models and How They Work - NVIDIA</a></li>

</ul>
</details>

**Discussion**: The Hacker News thread is highly engaged and broadly positive about the price cut, with one commenter cataloguing the exact drops in cache reads, input, output, and cache writes. A notable critique points out the irony that Anthropic&\#x27;s post opens by referencing its recent call to &quot;pace the frontier&quot; and then spends the rest of the announcement demonstrating with specific numbers that it is not pacing at all. Others say they are content with cheaper alternatives such as DeepSeek v4.1 for heavy agentic work, citing its low cost and willingness to spawn sub-agents and write its own tooling.

**Tags**: `#Anthropic`, `#Claude`, `#large language models`, `#AI pricing`, `#frontier AI`

---

<a id="item-3"></a>
## [Pentagon: AI Overreliance Blamed in Strike on Iranian School](https://www.bloomberg.com/graphics/2026-iran-school-attack/) ⭐️ 9.0/10

A Pentagon report concluded that overreliance on an AI targeting system contributed to a U.S. missile strike on a school in Minab, Iran, finding that the United States &quot;failed in its obligation to do everything feasible to verify&quot; that the school was a military objective and that the failure &quot;went beyond mere negligence.&quot; The report states the U.S. &quot;directed the strikes at the building of the school while being aware of a substantial risk of striking a civilian object and acting recklessly as regards the possibility that this would happen.&quot; This is one of the most concrete public cases of an AI-assisted targeting pipeline being linked to civilian casualties, putting pressure on how militaries govern human review, data freshness, and accountability for machine-recommended targets. It feeds directly into the ongoing international debate over lethal autonomous weapons, &quot;human-in-the-loop&quot; doctrine, and who is legally and morally responsible when an algorithm&\#x27;s recommendation leads to a wrongful strike. According to the reporting, the Minab site had been cataloged as an Islamic Revolutionary Guard Corps facility based on outdated data, was fed into the Maven targeting system alongside other candidates, and emerged as a recommended day-one target — compressing target-list work that once took hours into minutes. Commenters point out that the system preserves a human decision point, and that the broader 2026 campaign reportedly struck roughly 13,000 targets with only a handful of acknowledged errors, which raises the question of whether accuracy metrics are being optimized at the expense of verification.

hackernews · devonnull · Sep 22, 19:03 · [Discussion](https://news.ycombinator.com/item?id=49806430)

**Background**: The Maven Smart System is an AI-enabled targeting and intelligence-analysis platform that grew out of a decade of collaboration between the U.S. Department of Defense and major tech companies, used to speed up identification of potential targets from sensor and intelligence data. Most military doctrines that use such tools promise a &quot;human in the loop,&quot; meaning a person retains final authority to approve a strike and therefore bears legal and moral responsibility for it. Critics argue this safeguard is often illusory, because operators cannot fully understand how machine-learning models reach their recommendations and may defer to them under time pressure. International discussions on lethal autonomous weapons systems \(LAWS\) — weapons that can select and engage targets without direct human intervention — provide the broader legal and ethical context for this debate.

<details><summary>References</summary>
<ul>
<li><a href="https://www.brennancenter.org/our-work/research-reports/militarys-use-ai-explained">The Military’s Use of AI, Explained | Brennan Center for Justice</a></li>
<li><a href="https://smallwarsjournal.com/2026/03/11/human-in-the-loop/">Human-in-the-Loop or Loophole? Targeting AI and Legal ...</a></li>
<li><a href="https://www.technologyreview.com/2026/04/16/1136029/humans-in-the-loop-ai-war-illusion/">Why having “humans in the loop” in an AI war is an illusion</a></li>

</ul>
</details>

**Discussion**: Commenters are divided: several argue the AI is not really the culprit and that the failure lies with human decisions and outdated data, while others insist that no accuracy ratio justifies a strike on a school and ask pointedly &quot;who&\#x27;s going to jail?&quot; One widely echoed view holds that compressing hours of target-list work into minutes is &quot;optimizing the wrong metric,&quot; and another commenter notes a related incident in which AI incorrectly flagged a Chinese vessel as carrying nuclear-weapons material.

**Tags**: `#AI ethics`, `#military AI`, `#autonomous weapons`, `#AI safety`, `#accountability`

---

<a id="item-4"></a>
## [Claude Opus 5.5 and GPT-6 Sol/Luna Launch, Sparking a Price War](https://simonwillison.net/2026/Sep/22/opus-and-sol-and-luna/) ⭐️ 9.0/10

Anthropic released Claude Opus 5.5, and roughly an hour later OpenAI released GPT-6 Sol and GPT-6 Luna, according to Simon Willison&\#x27;s first impressions published on September 22, 2026. GPT-6 Luna is priced at $0.10 per million input tokens and $0.50 per million output tokens — half the price of GPT-5.6 Luna — while GPT-6 Sol also saw a similar price reduction versus GPT-5.6 Sol. Two frontier labs shipping flagship models within an hour of each other, with OpenAI halving its prices again, signals an intensifying price war that directly benefits developers building applications on top of these APIs. It also puts pressure on rivals such as xAI&\#x27;s Grok 4.7, which now looks expensive relative to GPT-6 Sol and no cheaper than it on input pricing. The comparison is measured against promotional pricing: GPT-5.6 has a scheduled 25% price increase for November, so GPT-6 is effectively half the price of those models&\#x27; promotional rates. GPT-6 Luna is among the cheapest models OpenAI has ever released, beaten only by the weaker GPT-4.1 Nano \($0.10/$0.40\) and GPT-5 Nano \($0.05/$0.40\), and GPT-5.6 Terra now costs the same as GPT-6 Sol, removing any remaining reason to use it.

rss · Simon Willison · Sep 22, 23:46

**Background**: Simon Willison is a well-known developer and commentator who has tracked large language model releases closely since 2024, and this post is his early reaction rather than a full benchmark. The releases came amid a dense cluster of model launches: xAI&\#x27;s Grok 4.7 and Xiaomi&\#x27;s open-weight MiMo v2.6 Flash/Pro arrived the day before, alongside the pelican benchmark Willison popularized. Model API pricing is normally quoted per million tokens, split between input, cached input, and output, which is why small per-token figures translate into large differences at application scale.

<details><summary>References</summary>
<ul>
<li><a href="https://grokipedia.com/page/Pelican_on_a_bicycle_AI_benchmark">Pelican on a bicycle (AI benchmark) — Grokipedia</a></li>
<li><a href="https://x.ai/news/grok-4-7">Introducing Grok 4.7 | SpaceXAI</a></li>
<li><a href="https://mimo.xiaomi.com/mimo-v2-6">MiMo-V2.6 | Xiaomi</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#AI`, `#OpenAI`, `#Anthropic`, `#Pricing`

---

<a id="item-5"></a>
## [vLLM v0.30.0 ships 762 commits, new models, and Fast Start weight cache](https://github.com/vllm-project/vllm/releases/tag/v0.30.0) ⭐️ 8.0/10

vLLM released v0.30.0, a large update containing 762 commits from 315 contributors \(104 of them first-time\), which adds many new model architectures \(DeepSeek-V4.1-Flash, GLM-5.3-Flash, K2-Horizon, Cohere Compass, Bailing V3 VL, Nanbeige4.2 and more\), a range of new quantization and backend kernels \(MXFP8 KV cache, an AVX512/AMX CPU backend for DeepSeek sparse MLA\), HiSparse host-tier decode, Gumbel-max watermarking, and the persistent per-GPU weight-cache feature named &\#x27;Fast Start&\#x27;. The release notes also describe substantial performance work on Qwen3.8-Flash-Next and Kimi K3, plus a wide set of large-scale serving improvements such as PCP+DCP on sparse-MLA models and Elastic EP CUDA-graph reuse. vLLM is one of the most widely used open-source frameworks for LLM inference and serving, so changes here propagate quickly into production deployments across the industry. The Fast Start weight cache directly attacks a long-standing operational pain point — the minutes-long engine startup and restart time on large models — while the new quantization formats and CPU backend widen the range of hardware and checkpoints that teams can serve efficiently. The Fast Start daemon keeps post-quantized, tensor-parallel-sharded weights resident in GPU memory so that a restarting engine can map them over CUDA IPC using \`--load-format ipc\_cache\` instead of reloading from disk, and it now covers FP4 checkpoints and multi-node tensor parallelism. On the performance side, freezing Python garbage collection during CUDA graph capture reportedly cut capture time from 12s to 2s and engine initialization from 28.9s to 8.2s on an H200, while new kernels such as grouped FP8 MLA cache insertion gave a 4-6x kernel speedup at small batch sizes.

github · khluu · Sep 22, 05:20

**Background**: vLLM is an open-source engine for serving large language models, built around memory-efficient attention and batched decoding so that a single GPU or cluster can handle many concurrent requests. Quantization is the practice of storing weights and activations at lower numeric precision — formats mentioned in this release include FP8, MXFP8 and NVFP4 — which reduces memory footprint and memory bandwidth pressure at some cost in accuracy; MXFP8 is a microscaling format from the Open Compute Project specification in which a group of 32 elements shares a single FP8 exponent scale. CUDA IPC \(inter-process communication\) is an NVIDIA API that lets separate processes share the same GPU memory handles, which is what makes the Fast Start cache reusable across engine restarts, and FlashMLA is DeepSeek&\#x27;s optimized library of Multi-head Latent Attention kernels for DeepSeek-style models.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.vllm.ai/projects/vllm-omni/en/latest/user_guide/quantization/mxfp8/">MXFP8 W8A8 - vLLM-Omni</a></li>
<li><a href="https://github.com/deepseek-ai/FlashMLA">GitHub - deepseek-ai/FlashMLA: FlashMLA: Efficient Multi-head ...</a></li>
<li><a href="https://docs.nvidia.com/cuda/cuda-programming-guide/04-special-topics/inter-process-communication.html">4.15. Interprocess Communication — CUDA Programming Guide</a></li>

</ul>
</details>

**Tags**: `#vllm`, `#LLM inference`, `#model serving`, `#GPU optimization`, `#open-source release`

---

<a id="item-6"></a>
## [Hackers claim to hold data on all FBI employees, threaten coercion](https://www.404media.co/we-hacked-the-fbi-hackers-say-they-have-data-on-all-fbi-employees/) ⭐️ 8.0/10

A group of hackers claims to have breached the FBI and says it now possesses data on all of the bureau&\#x27;s employees, according to a 404 Media report. In a quoted exchange, a representative said the group does not intend to extort the agency financially but is planning something they would call &quot;coercion&quot; instead. If the claim is verified, it would rank among the most sensitive breaches of US federal personnel data and could expose agents, analysts and support staff to targeting or blackmail. Even unverified, the claim amplifies ongoing concern about whether large government databases can be protected at all, and it raises questions about how agencies should respond to non-financial extortion. The hackers, referred to in the quoted exchange as ShinyHunters, framed their plan as &quot;not financially motivated,&quot; which is unusual for a criminal group typically associated with data theft and sale. The claim has not been independently verified, and no sample data or technical evidence demonstrating the breach has been publicly confirmed.

hackernews · spenvo · Sep 22, 17:46 · [Discussion](https://news.ycombinator.com/item?id=49805278)

**Background**: The FBI is the principal federal law enforcement agency of the United States, and its internal personnel records include biographical details, job roles and, in many cases, information tied to security clearance processes. The 2015 breach of the Office of Personnel Management \(OPM\) exposed records on roughly 22.1 million current and former federal employees and contractors, and it remains the benchmark for how damaging a government personnel-data compromise can be. &quot;Extortion&quot; in cybercrime usually means demanding payment in exchange for not leaking stolen data; &quot;coercion&quot; implies pressuring an organization into an action rather than a payment. ShinyHunters is a handle associated with a series of high-profile data thefts and leak-site operations in recent years.

**Discussion**: The Hacker News discussion was largely fatalistic about database security, with one commenter arguing that no one can keep a large database safe and pointing to China&\#x27;s theft of 22.1 million US government employee records in the 2015 OPM breach. Others treated the claim with dark humor — joking about the hackers being accidentally added to a Signal group chat sharing a Google Drive of employee data, and citing Battlestar Galactica&\#x27;s deliberately unnetworked warship as a security model. Several commenters also mocked the &quot;coercion, not extortion&quot; framing and speculated about what non-financial demands the group might make.

**Tags**: `#cybersecurity`, `#data breach`, `#FBI`, `#hacking`, `#privacy`

---

<a id="item-7"></a>
## [Artificial Analysis Benchmarks Claude Opus 5.5 at Max Reasoning Setting](https://artificialanalysis.ai/models/claude-opus-5-5) ⭐️ 8.0/10

Artificial Analysis published an evaluation page for Claude Opus 5.5 run at the &quot;max&quot; reasoning setting, tracking its intelligence, performance and price, with separate pages for the xhigh and medium \(default\) effort levels. The item sparked a Hacker News discussion that reached 232 points and 69 comments covering reasoning-budget limits, possible post-launch benchmark regression, and cost comparisons against cheaper alternatives. Because reasoning-effort settings change both accuracy and token spend, benchmarking a flagship model only at a non-default &quot;max&quot; level can mislead developers who run the cheaper default in production. The headline claim of roughly half the cost per task versus Opus 5 at comparable high effort, if it holds, would directly affect which models teams choose for agentic and coding workloads. Commenter simonw noted that at max effort he failed twice to get the model to generate an SVG of a pelican riding a bicycle because it exhausted its 128,000-token reasoning budget while still reasoning. Community members also raised whether these evaluations are re-run weeks after launch, citing an internal case where one model&\#x27;s measured performance reportedly regressed to match another&\#x27;s after a single run, and debated whether the small quality gap over open-weight models justifies a roughly 100x price difference.

hackernews · theanonymousone · Sep 22, 16:51 · [Discussion](https://news.ycombinator.com/item?id=49804316)

**Background**: Artificial Analysis is an independent organization that benchmarks large language models on intelligence, output speed, latency and price, publishing side-by-side comparisons across vendors. Modern reasoning models such as Claude can be given a &quot;thinking&quot; budget — a maximum number of tokens spent on internal reasoning before the final answer — and separate effort settings \(here medium, xhigh and max\) control how aggressively that budget is used. Larger reasoning budgets generally improve accuracy on hard tasks but increase latency and token cost, which is why the choice of setting matters when interpreting any benchmark or price figure.

<details><summary>References</summary>
<ul>
<li><a href="https://artificialanalysis.ai/methodology/intelligence-benchmarking">Artificial Analysis Intelligence Benchmarking Methodology</a></li>
<li><a href="https://platform.claude.com/docs/en/build-with-claude/extended-thinking">Extended thinking - Claude Platform Docs</a></li>
<li><a href="https://aisuperior.com/llm-token-cost/">LLM Inference Cost 2026: Complete Pricing Guide</a></li>

</ul>
</details>

**Discussion**: Overall sentiment mixed admiration for the pricing improvement with skepticism about benchmark reliability: simonw flagged the different effort-level pages and the max setting burning through its 128k reasoning budget on a trivial SVG task, hglaser highlighted roughly half the cost per task versus Opus 5 at equal effort, and breckenedge worried that providers may peak at launch and &quot;pull the rug&quot; afterward. cmiles8 argued that closed models are only marginally better than open-weight ones at around 100x the price, making &quot;good enough&quot; the more likely winner.

**Tags**: `#AI/ML`, `#LLM benchmarks`, `#Claude Opus`, `#model pricing`, `#reasoning models`

---

<a id="item-8"></a>
## [WordPress patches unauthenticated path traversal flaw enabling conditional RCE](https://github.com/WordPress/wordpress-develop/security/advisories/GHSA-7hp8-65ch-5whp) ⭐️ 8.0/10

WordPress released version 7.1.2 containing a fix for a critical unauthenticated path traversal vulnerability that can lead to conditional remote code execution, and as a courtesy to users on older versions the patch was backported to every branch back to 4.7. The upstream fix commit was identified publicly through the 7.1.1-to-7.1.2 comparison on the wordpress-develop repository. WordPress is one of the most widely deployed content management systems on the web, so an unauthenticated flaw — one that requires no login or credentials — puts an enormous number of sites at risk and makes rapid patching urgent. Because roughly one third of installations are not on the current 7.x branch, the backports to branches as old as 4.7 are what keep a large share of the installed base fixable. The RCE is described as conditional, meaning exploitation depends on specific configuration or deployment conditions rather than being universally achievable, though the underlying path traversal itself is unauthenticated. The flaw centers on template handling: documentation for the affected function, locate\_template\(\), explicitly warns that it does not prevent directory traversal when a user-provided template name is passed in, which is exactly the pattern this advisory addresses.

hackernews · vntok · Sep 22, 16:33 · [Discussion](https://news.ycombinator.com/item?id=49803959)

**Background**: WordPress is an open-source content management system that powers a very large fraction of all websites, which makes any unauthenticated vulnerability in it broadly consequential. A path traversal \(or directory traversal\) attack exploits insufficient validation of user-supplied file names so that sequences like &quot;../&quot; escape the intended directory and reach files elsewhere on the file system. Remote code execution is a more severe escalation: an attacker can run arbitrary code on the target server from a remote location, typically by abusing insecure handling of input. In this case a traversal in template-name handling can, under certain conditions, be chained into code execution, which is why the advisory is rated critical and patched across all supported branches.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Path_traversal_vulnerability">Path traversal vulnerability</a></li>
<li><a href="https://grokipedia.com/page/rce_remote_code_execution">RCE - Remote Code Execution</a></li>

</ul>
</details>

**Discussion**: Commenters noted the backport to branches as old as 4.7 was done &quot;as a courtesy&quot; while pointing out that about a third of installs still are not on the recent 7 branch, so many sites remain exposed until administrators act. Several argued WordPress is among the most-exploited software in web history, and one developer celebrated having migrated their site to statically hosted Hugo templates to escape the constant patching. Others added concrete value by pinpointing the upstream patch commit and surfacing a nine-year-old comment on the locate\_template\(\) documentation page that had already described both the nature of this directory traversal and its remediation.

**Tags**: `#security`, `#wordpress`, `#vulnerability`, `#rce`, `#path-traversal`

---

<a id="item-9"></a>
## [DeepSeek and Tsinghua publish DSec sandbox platform report: 3M sandboxes per day for agent training](https://arxiv.org/abs/2609.22978) ⭐️ 8.0/10

DeepSeek-AI and Tsinghua University jointly released a technical report on DeepSeek Elastic Compute \(DSec\), a sandbox infrastructure built to support large-scale agent training and evaluation. The platform provides four backends through a unified SDK — FnCall, containers, Firecracker microVMs, and full VMs — and in production a single unit of roughly 160 nodes serves about 3 million sandbox instances per day, with peak concurrency above 380,000 and creation rates exceeding 5,000 per second. Agent training and evaluation are increasingly bottlenecked not by model capacity but by the throughput and isolation quality of the execution environment, so a production-grade sandbox platform with published metrics gives the community a concrete reference architecture. It also signals that DeepSeek is investing in the systems layer behind its agent and reinforcement-learning work, not just in model weights, which matters for anyone building agent training pipelines or code-execution services. DSec decouples stateful rollout execution from preemptible GPU training and works tightly with reinforcement-learning frameworks; a single node can densely host 3,200 containers or 800 microVMs. It loads EROFS images on demand via the 3FS distributed file system, which reportedly cuts task completion time by 1.7x and disk writes by 57% versus traditional full Docker pulls, while memory sharing and reclamation reduce peak memory usage by roughly 40%.

telegram · zaihuapd · Sep 22, 04:45

**Background**: Sandboxes are isolated execution environments where an AI agent can run code, operate a computer, or complete software-engineering and security tasks without harming the host system. Firecracker is AWS&\#x27;s open-source microVM technology that combines hardware-virtualization isolation with fast startup and a minimal device model, while EROFS is a lightweight read-only Linux file system and 3FS is DeepSeek&\#x27;s own high-performance distributed file system for AI workloads. Combining these lets DSec spin up very large numbers of isolated environments cheaply, which is the prerequisite for large-scale agent training and benchmarking.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/deepseek-ai/3FS">GitHub - deepseek-ai/3FS: A high-performance distributed file ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/EROFS">EROFS - Wikipedia</a></li>
<li><a href="https://github.com/firecracker-microvm/firecracker">GitHub - firecracker - microvm / firecracker : Secure and fast microVMs...</a></li>

</ul>
</details>

**Tags**: `#AI infrastructure`, `#agent training`, `#sandboxing`, `#DeepSeek`, `#systems research`

---

<a id="item-10"></a>
## [China Probes DeepSeek and Moonshot Over Alleged Claude Data Leaks](https://www.theinformation.com/articles/china-probes-deepseek-moonshot-potential-data-leaks-anthropic) ⭐️ 8.0/10

According to people familiar with the matter, China&\#x27;s internet regulator is investigating DeepSeek and Moonshot AI \(月之暗面\) after Anthropic published a 154-page report on September 10 accusing seven Chinese companies of large-scale misuse of Claude, including an example in which DeepSeek allegedly forwarded requests from an engineer working on police surveillance systems to the Claude model. The probe is reportedly focused on whether sensitive user data was improperly routed to the US-based model. The investigation turns an accusation from a US AI lab into a regulatory matter inside China, signaling that cross-border model API usage and data flows are becoming a governance battleground between the two countries&\#x27; AI ecosystems. It could push Chinese labs to tighten how they handle user prompts and third-party model access, and raise compliance risk for any company whose products route data to overseas models. Anthropic&\#x27;s allegations are laid out in a 154-page report published September 10 that names seven Chinese companies and singles out DeepSeek for forwarding a request tied to police surveillance work; the Chinese investigation is based on unnamed sources and no formal charges or findings have been announced. The Information reported the probe, and neither regulator nor the companies have publicly confirmed its scope or status.

telegram · zaihuapd · Sep 22, 14:37

**Background**: DeepSeek is a Chinese AI research company that develops and open-sources frontier large language models such as DeepSeek-R1, and its chatbot became a global phenomenon after launching in early 2025. Moonshot AI, known in Chinese as 月之暗面 \(literally &quot;dark side of the moon&quot;\), is a Beijing-based AI company counted among China&\#x27;s &quot;AI Tigers&quot; and best known for its Kimi assistant. Claude is the AI assistant product family built by Anthropic, a US AI safety and research company; Chinese developers typically reach such US models through APIs or intermediary services rather than an officially available domestic offering. China&\#x27;s internet regulator oversees domestic internet services and data handling, which is why an allegation about routing user data to an overseas model falls within its remit.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Moonshot_AI">Moonshot AI - Wikipedia</a></li>
<li><a href="https://www.anthropic.com/">Home \ Anthropic</a></li>

</ul>
</details>

**Tags**: `#AI regulation`, `#DeepSeek`, `#Anthropic/Claude`, `#data privacy`, `#China AI`

---