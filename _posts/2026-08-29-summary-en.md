---
layout: default
title: "Horizon Summary: 2026-08-29 (EN)"
date: 2026-08-29
lang: en
---

> From 31 items, 10 important content pieces were selected

---

1. [Z.ai Launches Open-Weight GLM-5.3, Boosting Coding and Agent Skills](#item-1) ⭐️ 9.0/10
2. [Triton 3.8.0 Released with Aggregate Types and New tl.topk Options](#item-2) ⭐️ 8.0/10
3. [Keyboard-Driven GUIs: A Debate on Accessibility and Power Users](#item-3) ⭐️ 8.0/10
4. [Htmx 4.0 Released with New Features and Compatibility Improvements](#item-4) ⭐️ 8.0/10
5. [OpenAI Restricts Cursor After SpaceX Acquisition Over Model Distillation](#item-5) ⭐️ 8.0/10
6. [U.S. sanctions Italian hosting collective Autistici/Inventati as terrorist entity](#item-6) ⭐️ 8.0/10
7. [Bug Rumors Alone Now Trigger Exploit Discovery, Burdening Maintainers](#item-7) ⭐️ 8.0/10
8. [Inception-Style Curved Map for Turn-by-Turn Directions](#item-8) ⭐️ 8.0/10
9. [Tiny latent flow transformer generates 128x128 face images on RP2350 microcontroller](#item-9) ⭐️ 8.0/10
10. [Tencent Releases Hy4 Preview MoE, Slightly Beats Rivals in Blind Test](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Z.ai Launches Open-Weight GLM-5.3, Boosting Coding and Agent Skills](https://huggingface.co/zai-org/GLM-5.3) ⭐️ 9.0/10

GLM-5.3 is now released as an open-weight model, with weights available for download on Hugging Face. It delivers a 50% improvement over GLM-5.2 on Z.ai&\#x27;s in-house Code Bench and claims open-source state-of-the-art results on Terminal Bench 3.0 and Agents&\#x27; Last Exam. This is a major open-weight LLM release that strengthens the ecosystem of downloadable models capable of competing with leading closed models. It gives developers and researchers a high-performing, runnable alternative for coding and agentic tasks, and the community reaction suggests it may shift usage away from other open and commercial models. GLM-5.3 shares the same base model as GLM-5.2, with all improvements coming from post-training. The official license allows individuals and SMBs to freely use, fine-tune, and commercialize the model, but imposes restrictions for companies with over $10 billion in annual revenue over a rolling 12-month period if they offer certain external model services; API users migrating from earlier versions must also adjust their thinking/reasoning settings.

hackernews · jeudesprits · Aug 28, 15:20 · [Discussion](https://news.ycombinator.com/item?id=49479878)

**Background**: Open-weight models are large language models whose trained parameters are publicly released, allowing anyone to download, run, and modify them without going through a vendor&\#x27;s API. GLM is a series of LLMs developed by Z.ai \(Zhipu AI\), and GLM-5.3 is the newest open-weight release positioned as a strong coding and agentic model. The Hugging Face release notes say it achieves open-source state-of-the-art results on public benchmarks such as Terminal Bench 3.0 and Agents&\#x27; Last Exam.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/zai-org/GLM-5.3">zai-org/ GLM - 5 . 3 · Hugging Face</a></li>
<li><a href="https://docs.z.ai/guides/llm/glm-5.3">GLM - 5 . 3 - Overview - Z.AI DEVELOPER DOCUMENT</a></li>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>

</ul>
</details>

**Discussion**: Commenters are generally enthusiastic, with several reporting hands-on success: one calls it &quot;pretty amazing&quot; on two DGX Spark systems and says it has intuition that DeepSeek Flash 4 lacks, while another says it feels like Opus 4.8. Some see it as a practical middle ground between efficiency and capability, and one commenter raises a pointed question about whether past safety concerns still justify withholding older models like GPT-3.

**Tags**: `#LLM`, `#open-weights`, `#AI`, `#GLM`, `#model-release`

---

<a id="item-2"></a>
## [Triton 3.8.0 Released with Aggregate Types and New tl.topk Options](https://github.com/triton-lang/triton/releases/tag/v3.8.0) ⭐️ 8.0/10

Triton 3.8.0 was released, introducing public aggregate types via @triton.aggregate and @gluon.aggregate, a new descending argument for tl.topk, and numerous backend and compiler improvements across NVIDIA and AMD/HIP targets. The release also includes breaking changes and bug fixes for IEEE rounding, NaN handling, and block-pointer padding. Triton is a widely used GPU programming language and compiler in the ML/systems ecosystem, powering kernels for PyTorch and other frameworks. This release&\#x27;s aggregate types improve code readability and parameter passing, while tl.topk enhancements expand usability for sampling and search kernels, benefiting the broader GPU computing community. Aggregate types now support inherited fields, default values, generated constructors, immutable instances, and aggregate\_replace\(\). tl.topk gains a descending argument \(default True\) to return smallest values; tensor descriptors can now be passed inside tuple-valued kernel arguments, and the interpreter added tl.dot\_scaled support. Breaking changes and an LLVM pin update with GFX950 BF16 miscompilation fixes are also part of this release.

github · warrendeng · Aug 28, 18:25

**Background**: Triton is an open-source domain-specific language and compiler for writing GPU kernels, using a Python-like syntax that abstracts away low-level details like memory layout and synchronization. Gluon is a lower-level language built on the same compiler stack that gives users explicit control over layouts, complementing Triton&\#x27;s automatic optimizations. Aggregate types, previously internal, are now public APIs in both Triton and Gluon, simplifying the passing of structured data to JIT-compiled kernels. tl.topk is a standard operation for selecting the k largest or smallest elements along a dimension, commonly used in sampling and top-k decoding.

<details><summary>References</summary>
<ul>
<li><a href="https://triton-lang.org/main/python-api/generated/triton.language.topk.html">triton .language. topk — Triton documentation</a></li>
<li><a href="https://triton-lang.org/main/getting-started/tutorials/gluon/intro.html">Introduction to Gluon — Triton documentation</a></li>
<li><a href="https://www.lei.chat/posts/gluon-explicit-performance/">Gluon : Explicit Performance | Lei.Chat()</a></li>

</ul>
</details>

**Tags**: `#triton`, `#gpu`, `#compiler`, `#release`, `#ml`

---

<a id="item-3"></a>
## [Keyboard-Driven GUIs: A Debate on Accessibility and Power Users](https://ckardaris.com/blog/2026/08/28/keyboard-driven-guis.html) ⭐️ 8.0/10

A blog post argues that GUIs should be fully keyboard-driven, sparking a lively debate on Hacker News \(666 points, 324 comments\). The discussion focuses on accessibility, power users, and UX trade-offs. This debate highlights the tension between power-user efficiency and mainstream usability, pushing engineers and designers to treat keyboard support as a core requirement. The outcome influences how accessible software becomes for people with disabilities and for those who prefer keyboard-centric workflows. Commenters emphasize that keyboard navigation is critical for users with motor disabilities, but note that discoverability and learning curves remain challenges. One commenter distinguishes &quot;keyboard-driven&quot; from merely &quot;keyboard-compatible,&quot; suggesting that merely assigning shortcuts is insufficient.

hackernews · ckardaris · Aug 28, 15:17 · [Discussion](https://news.ycombinator.com/item?id=49479837)

**Background**: Keyboard-driven GUIs allow users to perform all interactions through keyboard shortcuts and focus navigation instead of a mouse or touchscreen. This is essential for accessibility compliance, such as the ADA, and is a common expectation among power users. Designing such interfaces requires careful attention to focus management, shortcut discoverability, and visual indicators. The Hacker News discussion reflects broader industry debates about whether accessibility features should be mandatory for all software.

**Discussion**: Commenters widely agree that keyboard accessibility matters, but disagree on whether every GUI must be fully keyboard-driven. Some argue that power-user needs differ from general user needs, and that forcing keyboard-driven design could harm mainstream usability.

**Tags**: `#accessibility`, `#keyboard-driven UI`, `#UX`, `#software design`, `#HN discussion`

---

<a id="item-4"></a>
## [Htmx 4.0 Released with New Features and Compatibility Improvements](https://four.htmx.org/announcements/2026-08-28-htmx-4.0.0-is-released) ⭐️ 8.0/10

Htmx 4.0.0 was released on August 28, 2026, introducing new features and compatibility improvements, including an hx-alpine-compat attribute to smooth over issues with Alpine.js. The release has generated significant community discussion, with 138 comments and 565 points. This major release of a widely-used hypermedia-oriented library reinforces the growing trend toward simpler server-side rendering approaches, offering an alternative to heavyweight JavaScript frameworks. The strong community response underscores htmx&\#x27;s influence in the frontend ecosystem and the ongoing debate about its role. Htmx remains small \(~16k min.gz&\#x27;d\), dependency-free, and extendable, using HTML attributes to provide AJAX, CSS transitions, WebSockets, and Server-Sent Events. The new hx-alpine-compat feature addresses compatibility issues between htmx and Alpine.js, while the library continues to support progressive enhancement.

hackernews · rmsaksida · Aug 28, 13:28 · [Discussion](https://news.ycombinator.com/item?id=49478178)

**Background**: Htmx is a JavaScript library that extends HTML with attributes, allowing developers to build modern user interfaces using the simplicity of hypertext without complex state management or hydration. It follows the hypermedia approach, where the server returns HTML fragments that update specific parts of the page without a full reload, making it a popular choice for developers who prefer server-side rendering. The library is known for being small, dependency-free, and extendable, and it supports techniques like progressive enhancement to degrade gracefully when JavaScript is disabled.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Htmx">htmx - Wikipedia</a></li>
<li><a href="https://htmx.org/">htmx - high power tools for html</a></li>
<li><a href="https://htmx.org/docs/">htmx ~ Documentation</a></li>

</ul>
</details>

**Discussion**: The community response is largely positive, with users expressing excitement and sharing practical use cases like Go, htmx, and SQLite together, while some also praise the library&\#x27;s simplicity and organic growth. However, there are contrarian views: one commenter noted that htmx could complicate things for developers accustomed to .NET API backends and Angular, while another mentioned alpine-ajax as a smaller alternative that met their needs. The CEO of HTMX also disclosed their role in the discussion, adding an element of transparency to the thread.

**Tags**: `#htmx`, `#javascript`, `#web development`, `#hypermedia`, `#release`

---

<a id="item-5"></a>
## [OpenAI Restricts Cursor After SpaceX Acquisition Over Model Distillation](https://openai.com/index/our-decision-on-cursor-following-its-acquisition-by-spacex/) ⭐️ 8.0/10

OpenAI has decided to restrict Cursor&\#x27;s access to its models following Cursor&\#x27;s acquisition by SpaceX, citing concerns about model distillation. The move effectively limits how Cursor, an AI coding assistant, can use OpenAI&\#x27;s proprietary models. This decision reshapes the competitive landscape for AI coding tools, as developers who rely on Cursor with OpenAI models may lose that integration. It also signals that major AI providers will actively enforce terms of service when a reseller is acquired by a rival model provider. OpenAI cited model distillation concerns, a practice in which outputs from a larger model are used to fine-tune smaller models. Cursor had been reselling access to third-party APIs, and its sale to SpaceX—a competing model provider—triggered the restriction.

hackernews · meetpateltech · Aug 29, 01:47 · [Discussion](https://news.ycombinator.com/item?id=49486172)

**Background**: Cursor is an AI-powered code editor and development environment founded in 2022, known for letting developers write code through natural-language instructions; it reached a $29.3 billion valuation and surpassed $3 billion in annual recurring revenue. Model distillation is the process of transferring knowledge from a large, capable model to a smaller, cheaper one by fine-tuning on the larger model&\#x27;s outputs, which many AI companies prohibit for competitive reasons.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cursor_%28code_editor%29">Cursor (company) - Wikipedia</a></li>
<li><a href="https://openai.com/index/api-model-distillation/">Model Distillation in the API - OpenAI</a></li>
<li><a href="https://cursor.com/">AI Coding Agent for Building Ambitious Software | Cursor</a></li>

</ul>
</details>

**Discussion**: Commenters largely said they saw this coming, noting that Cursor&\#x27;s business model of reselling others&\#x27; APIs was unsustainable. One pointed out that Anthropic had already banned xAI for similar terms-of-service violations, while another Cursor and Claude subscriber said the move would push them back to Anthropic. Some users said they were happy using Grok or Composer in Cursor and did not need OpenAI models.

**Tags**: `#AI`, `#OpenAI`, `#Cursor`, `#SpaceX`, `#Model Governance`

---

<a id="item-6"></a>
## [U.S. sanctions Italian hosting collective Autistici/Inventati as terrorist entity](https://www.inventati.org/) ⭐️ 8.0/10

In late August 2026, the U.S. State and Treasury Departments designated the Italy-based Autistici/Inventati \(A/I\) collective, which operates the noblogs.org blogging platform, as a Specially Designated Global Terrorist \(SDGT\), imposing sanctions on the infrastructure provider. This is a significant escalation because a nonviolent infrastructure provider has been labeled a terrorist entity, creating a chilling precedent for privacy tools, free speech platforms, and the broader internet ecosystem. It could deter hosting providers, developers, and users from offering or using privacy-preserving services for fear of similar sanctions. The designation specifically names the Autistici/Inventati Collective and prohibits U.S. persons from engaging in transactions with it; the group&\#x27;s websites, including autistici.org and noblogs.org, have become partially inaccessible or down. Critics point to the lack of transparent evidence tying A/I to terrorism, noting the designation appears to stem from its long history of hosting activist communications.

hackernews · exiguus · Aug 28, 12:58 · [Discussion](https://news.ycombinator.com/item?id=49477854)

**Background**: Autistici/Inventati \(A/I\) is a nonprofit collective founded in Milan in 2001 by individuals and collectives from the autonomous anticapitalist movement, providing email, web hosting, and blogging tools to activists and civil society groups. Noblogs.org, a blogging platform run by A/I, has hosted numerous independent media and social movement sites, including projects linked to Indymedia. This sanctions action treats the provision of communication infrastructure itself as terrorist support, a departure from past sanctions that typically targeted individuals or organizations with direct ties to violent groups.

<details><summary>References</summary>
<ul>
<li><a href="https://www.autistici.org/">autistici.org - Welcome to Autistici / Inventati</a></li>
<li><a href="https://crimethinc.com/2026/08/27/us-government-designates-host-of-noblogsorg-a-global-terrorist">US Government Designates Host of NoBlogs . org a &quot;Global Terrorist&quot;</a></li>
<li><a href="https://www.radiorebelde.cu/english/u-s-designates-palestine-action-masar-badil-and-autistici-inventati-as-terrorist-groups-26082026/">U.S. Designates Palestine Action, Masar Badil, and Autistici Inventati ...</a></li>

</ul>
</details>

**Discussion**: Commenters are largely alarmed, arguing that designating an infrastructure provider as a terrorist entity sets an unprecedented precedent that could threaten projects like I2P, Monero, Veilid, Tox, and Signal. Some question what A/I actually does and note the difficulty of verifying the alleged PKK connection, while others provide historical context about A/I&\#x27;s role in supporting protest movements such as the 2001 Genoa protests. The overall sentiment is critical of the government action and its potential chilling effect on privacy infrastructure.

**Tags**: `#sanctions`, `#privacy`, `#hosting`, `#civil liberties`, `#surveillance`

---

<a id="item-7"></a>
## [Bug Rumors Alone Now Trigger Exploit Discovery, Burdening Maintainers](https://anil.recoil.org/notes/rumour-is-the-exploit) ⭐️ 8.0/10

An article argues that mere rumors of a vulnerability are now sufficient to trigger exploit discovery, with AI-assisted tooling dramatically accelerating the process. This has led to a surge in security disclosures and a huge additional burden on open source maintainers. The combination of LLM-based code analysis and automated exploit generation means attackers can weaponize vague hints faster than ever. Open source maintainers face an unsustainable flood of reports, threatening the security ecosystem&\#x27;s ability to respond. In one example, the rclone project received over 40 security disclosures in a month after averaging about 20 in its first 10 years, with roughly 75% containing a real issue. AI models can now identify silent patches in routine commits and assist with patch diffing, lowering the skill barrier for exploitation.

hackernews · avsm · Aug 28, 15:58 · [Discussion](https://news.ycombinator.com/item?id=49480466)

**Background**: Vulnerability research historically included deriving exploits from patch diffs, commit messages, or offhand remarks, but this required significant skill. Large language models now make these techniques accessible to far more actors, enabling automated exploit generation and vulnerability discovery at scale. Tools like DeepBinDiff and ChatGPT are used for AI-assisted patch diffing to find silent fixes. This shifts the bottleneck from finding bugs to fixing them, and to rapid deployment of patches.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/html/2505.01065">Good News for Script Kiddies? Evaluating Large Language Models ...</a></li>
<li><a href="https://www.sans.org/cyber-security-courses/offensive-ai-attack-tools-techniques">SEC535: Offensive AI - Attack Tools and Techniques | SANS ...</a></li>
<li><a href="https://github.com/huhusmang/Awesome-LLMs-for-Vulnerability-Detection">GitHub - huhusmang/Awesome-LLMs-for- Vulnerability -Detection: The...</a></li>

</ul>
</details>

**Discussion**: Commenters broadly agree with the thesis, sharing maintainer experiences and varied perspectives. One open source maintainer reports a dramatic surge in disclosures—about 75% with real merit—that consumes enormous time, while others argue the real problems are organizational will to fix bugs and the impracticality of instant patching, with some noting the democratization of exploitation is new even if the technique is old.

**Tags**: `#security`, `#open source`, `#AI-assisted exploitation`, `#vulnerability disclosure`, `#maintainer burden`

---

<a id="item-8"></a>
## [Inception-Style Curved Map for Turn-by-Turn Directions](https://www.orbify.eu/demo/) ⭐️ 8.0/10

Orbify has released a demo of an Inception-style curved map for turn-by-turn navigation that bends the road ahead into a perspective curve. The visualization has generated significant discussion on Hacker News, with 147 comments and 447 points. This demo introduces a visually striking alternative to conventional 2D or 3D navigation maps, potentially changing how drivers perceive upcoming turns. Even as a proof of concept, it has sparked a lively debate about usability, highlighting an appetite for novel map visualizations. The demo is a proof of concept rather than a finished product, available at orbify.eu/demo. Critics point out that just before a turn, the view provides almost no information about the route ahead, making consecutive turns difficult to navigate; some suggest rotating the view or unwrapping sharp turns to compensate.

hackernews · smoser · Aug 28, 12:29 · [Discussion](https://news.ycombinator.com/item?id=49477564)

**Background**: The visual style echoes the folding-city scenes from the film Inception, and also has earlier roots in map-inspired art such as Berg London&\#x27;s &\#x27;Here and There&\#x27; poster from 2009. In typical turn-by-turn navigation, the map remains flat and follows the vehicle, whereas this demo projects the road ahead as a curved, perspective-bent surface, which is more cinematic but can obscure immediate next actions. The demo appears to use Gaussian-splat rendering for an interactive, photorealistic effect.

<details><summary>References</summary>
<ul>
<li><a href="https://lemmy.world/post/51241241">Inception - style curved map for turn-by-turn directions - Lemmy.World</a></li>
<li><a href="https://googlemapsmania.blogspot.com/2026/08/bending-maps-inception-style.html">Bending Maps , Inception Style</a></li>

</ul>
</details>

**Discussion**: Commenters praised the demo as &\#x27;pure Bret-Victorian magic&\#x27; and a beautiful proof of concept, but many questioned its practical usefulness. Key concerns included limited visibility before and after turns, unstable prediction distances, and potential motion sickness, summed up by one joke: &\#x27;Nausea as a Service.&\#x27;

**Tags**: `#UI/UX`, `#Maps`, `#Visualization`, `#Navigation`, `#Hacker News`

---

<a id="item-9"></a>
## [Tiny latent flow transformer generates 128x128 face images on RP2350 microcontroller](https://www.reddit.com/r/MachineLearning/comments/1w10tax/i_implemented_a_very_tiny_image_generation_model/) ⭐️ 8.0/10

A developer \(u/cpldcpu\) implemented a 2.4–4 million parameter latent flow transformer on an RP2350 microcontroller, generating 128×128 face images in about 20 seconds. The model runs fully on-device using int8 quantization and streams weights via DMA from flash while computing each layer. This shows that modern diffusion-style image generators can be compressed to run on a cheap ~$1 microcontroller, pushing edge-AI capabilities beyond classification into generative tasks. It is a notable proof-of-concept for on-device generation, privacy-preserving AI, and ultra-low-power ML. The model is a 12-layer latent flow transformer using AdaLN-Zero conditioning for class/timestep control and classifier-free guidance \(CFG\), which significantly improves quality. It uses ReLU² activations to increase sparsity, allowing the engine to skip computations, and supports displaying output on a monitor or transferring it via USB.

reddit · r/MachineLearning · /u/cpldcpu · Aug 28, 19:48

**Background**: Latent flow transformers \(LFT\) are a recent architecture that replaces a block of layers with a single learned transport operator trained via flow matching, enabling large compression of generative models. Flow matching and diffusion models learn to denoise/transport samples from noise to data, and AdaLN-Zero is a zero-initialized adaptive normalization technique commonly used in diffusion transformers like DiT for conditioning. The RP2350 is Raspberry Pi&\#x27;s dual-core microcontroller \(Cortex-M33 or Hazard3 RISC-V\) used on the Raspberry Pi Pico 2, with on-board flash and a very low cost.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2505.14513">Abstract page for arXiv paper 2505.14513: Latent Flow Transformer</a></li>
<li><a href="https://en.wikipedia.org/wiki/RP2350">RP2350</a></li>
<li><a href="https://openreview.net/forum?id=E4roJSM9RM">Unveiling the Secret of AdaLN-Zero in Diffusion Transformer</a></li>

</ul>
</details>

**Tags**: `#edge-ai`, `#microcontrollers`, `#image-generation`, `#model-compression`, `#efficient-inference`

---

<a id="item-10"></a>
## [Tencent Releases Hy4 Preview MoE, Slightly Beats Rivals in Blind Test](https://mp.weixin.qq.com/s/ymr3X878B8oa2XP15CH8TQ) ⭐️ 8.0/10

On August 28, 2026, Tencent released Hy4 preview, its strongest open-source model to date. The Mixture-of-Experts model has 770B total parameters, 49B active parameters, and a 1M-token context window, achieving a blind-test score of 2.99 on 203 engineering tasks, slightly ahead of GLM-5.3 \(2.92\) and Kimi K3 \(2.94\). This release intensifies competition among Chinese AI labs in the open-source LLM space, showing Tencent can match or slightly exceed peers such as Zhipu GLM and Moonshot Kimi. The 1M-token context and focus on long-horizon software engineering and scientific research target real-world productivity use cases. The model is hosted on Tencent Cloud, GitHub, Hugging Face, ModelScope, AtomGit, and OpenRouter, with API pricing of $0.834 per 1M input tokens and $2.501 per 1M output tokens. It is a preview release, so benchmark scores and availability may change before the final version.

telegram · zaihuapd · Aug 28, 06:11

**Background**: Mixture-of-Experts \(MoE\) is an architecture that activates only a subset of a model&\#x27;s parameters for each input token, allowing larger total parameter counts without proportional increases in compute cost. In Hy4 preview, only 49B of the 770B total parameters are active per token. Blind evaluation presents model outputs to human raters without revealing which model produced them, reducing brand bias; such tests are increasingly used for comparing LLM quality.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2507.11181">[2507.11181] Mixture of Experts in Large Language Models A Closer Look into Mixture-of-Experts in Large Language Models Mixture of Experts Explained - Hugging Face Applying Mixture of Experts in LLM Architectures | NVIDIA ... A Closer Look into Mixture-of-Experts in Large Language Models Understanding Mixture of Experts (MoE): The Architecture ...</a></li>
<li><a href="https://www.f22labs.com/blogs/active-vs-total-parameters-whats-the-difference/">Active vs Total Parameters: What’s the Difference?</a></li>
<li><a href="https://zylos.ai/research/2026-01-16-llm-evaluation-benchmarking/">LLM Evaluation and Benchmarking 2026 | Zylos Research</a></li>

</ul>
</details>

**Tags**: `#AI`, `#LLM`, `#Tencent`, `#open-source`, `#model release`

---