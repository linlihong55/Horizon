---
layout: default
title: "Horizon Summary: 2026-10-17 (EN)"
date: 2026-10-17
lang: en
---

> From 37 items, 7 important content pieces were selected

---

1. [Claude Solves Origins of NIST ECDSA Curve Seeds](#item-1) ⭐️ 8.0/10
2. [Jake Archibald compares JPEG XL and AVIF for web images](#item-2) ⭐️ 8.0/10
3. [How the Claude Code team does code review](#item-3) ⭐️ 8.0/10
4. [Mercor: 90% of US Work Hours Lack AI Benchmark Coverage](#item-4) ⭐️ 8.0/10
5. [Big Fish: Exploiting a 37-Year-Old OpenBSD Kernel Bug](#item-5) ⭐️ 8.0/10
6. [ORL Accelerates Diffusion LLMs to 2,788 Tokens/s on a Single RTX 5090](#item-6) ⭐️ 8.0/10
7. [Investors Cut Anthropic IPO Valuation Expectations to About $1.5 Trillion](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Claude Solves Origins of NIST ECDSA Curve Seeds](https://www.anthropic.com/research/ecdsa-curve-origins) ⭐️ 8.0/10

Anthropic&\#x27;s Frontier Red Team reported that Claude discovered the origins of the NIST P-192, P-224, P-256, P-384 and P-521 curve seeds in under half an hour, finding they were not the output of any hash algorithm but the output of the C library&\#x27;s lrand48 random-number generator seeded with a Unix timestamp. This resolves a decades-old cryptographic mystery about how the seeds behind the most widely deployed elliptic-curve standard were generated, and it undercuts a long-running conspiracy theory that the NSA deliberately manipulated the NIST curves to embed a backdoor. It also serves as a striking demonstration of AI-assisted research against long-standing open problems in cryptography. The fifth binary-field seed, B-163, fits nothing Claude has tried and remains unexplained. Crucially, the result only confirms the method of production, not the selection process: because discarded candidate timestamps are invisible, it remains conceivable that the curves were chosen to have a specific property by searching over timestamps fed to the RNG.

hackernews · ahlCVA · Oct 16, 18:55 · [Discussion](https://news.ycombinator.com/item?id=50122800)

**Background**: ECDSA is the most widely used elliptic-curve cryptography standard; NIST adopted it in 2000 as part of the FIPS 186-2 Digital Signature Standard, which lists standard curves of varying sizes and security levels. To make the curves &quot;verifiably random&quot;, the standard specified that a seed be hashed to derive the curve parameters, so anyone could re-run the computation and confirm no hidden backdoor — but the origin of the seeds themselves was never published. Suspicion grew after the Snowden revelations and the discovery of the NSA-linked Dual\_EC\_DRBG backdoor, which led many to assume the NIST curves had similarly been engineered with a secret weakness.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/research/ecdsa-curve-origins">Claude reveals ECDSA curve origins \ Anthropic</a></li>
<li><a href="https://www.unite.ai/anthropic-says-claude-traced-nist-ecdsa-curve-seeds-to-a-1990s-rng/">Anthropic Says Claude Traced NIST ECDSA Curve Seeds to a ...</a></li>
<li><a href="https://www.explainx.ai/blog/claude-ecdsa-nist-curve-seeds-lrand48-anthropic-frontier-red-team-backdoor-question-2026">ECDSA Curve Seeds Solved: Claude Found lrand48 (2026 ...</a></li>

</ul>
</details>

**Discussion**: Sentiment was a mix of amusement and caution: one commenter joked about &quot;13 years of tinfoil hats for srand48\(time\(NULL\)&quot; and another called it &quot;devastating news... for an entire generation of NIST cryptography conspiracy theories.&quot; The main counterargument, however, was that confirming the generation method says nothing about selection — since discarded candidates are invisible, the curves could still have been chosen deliberately by searching over timestamps — while others suggested the unexplained B-163 seed may simply be a mistyped digit in the original publication.

**Tags**: `#cryptography`, `#ECDSA`, `#NIST curves`, `#AI-assisted research`, `#security`

---

<a id="item-2"></a>
## [Jake Archibald compares JPEG XL and AVIF for web images](https://jakearchibald.com/2026/jpeg-xl-vs-avif/) ⭐️ 8.0/10

Web performance expert Jake Archibald published a technical comparison of JPEG XL and AVIF for web image delivery, pairing benchmark-style analysis with practitioner-tested encoding settings. The post drew heavy community engagement \(194 points, 143 comments\) in which developers shared concrete encoder configurations and debated which codec will ultimately win. Image bytes are typically the largest part of a page&\#x27;s payload, so the choice between JPEG XL and AVIF directly affects load times, bandwidth costs, and Core Web Vitals for sites at scale. The comparison matters because the two formats currently trade off against each other: AVIF already ships in most major browsers while JPEG XL offers stronger compression and features but lacks broad native support. JPEG XL is a lossy-and-lossless format designed for efficient software-based encoding and decoding without hardware acceleration, while AVIF derives from the AV1 video codec and is backed by the Alliance for Open Media. Community members noted that libjxl&\#x27;s highest effort levels are extremely slow—producing files only 2–7% smaller than the default for photos yet taking 9–46 seconds—largely because of an iterative optimization loop over the perceptual metric Butteraugli, with the alternative encoder jixel achieving similar results in a couple of seconds.

hackernews · farlight · Oct 16, 16:12 · [Discussion](https://news.ycombinator.com/item?id=50120224)

**Background**: JPEG XL is a next-generation image format developed by the Joint Photographic Experts Group together with Google and Cloudinary, offering both lossy and lossless compression and significantly better quality-per-byte than legacy JPEG. AVIF is the AV1 Image File Format from the Alliance for Open Media, using the AV1 video codec to compress still images, and it has already been adopted by most major browsers. Both formats exist to solve the same problem: replacing the decades-old JPEG with smaller files at equal or better visual quality.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/JPEG_XL">JPEG XL - Wikipedia</a></li>
<li><a href="https://shortpixel.com/blog/what-is-avif-and-why-is-it-good/">What is AVIF and why is it good? - ShortPixel Blog</a></li>
<li><a href="https://jpeg.org/jpegxl/">JPEG - JPEG XL</a></li>

</ul>
</details>

**Discussion**: Commenters largely agreed that the technical trade-offs are real but that codec wars take years to settle: one explained that libjxl&\#x27;s slowest modes stem from its Butteraugli-driven evaluation loop \(and that jixel is far faster\), while another shared a tested ffmpeg AVIF command that preserves PNG alpha transparency. A more cautious voice recalled the MP3/LAME and WebP eras, warning against treating any early &\#x27;winner&\#x27; declaration as gospel, and one commenter criticized AVIF for visibly erasing highlight detail in the article&\#x27;s F1 example image.

**Tags**: `#image-compression`, `#jpeg-xl`, `#avif`, `#web-performance`, `#codecs`

---

<a id="item-3"></a>
## [How the Claude Code team does code review](https://claude.dev/blog/solving-code-review-at-anthropic/) ⭐️ 8.0/10

Anthropic&\#x27;s Claude Code team describes an automated, eval-driven code review pipeline with at most one human reviewer, sparking critical HN debate over compliance, insider risk, and AI-generated prose.

hackernews · pretext · Oct 16, 19:04 · [Discussion](https://news.ycombinator.com/item?id=50122951)

**Tags**: `#AI-assisted-code-review`, `#software-engineering-practices`, `#Anthropic`, `#SOC2-compliance`, `#developer-tooling`

---

<a id="item-4"></a>
## [Mercor: 90% of US Work Hours Lack AI Benchmark Coverage](https://www.mercor.com/research/labor-index/benchmark-map/) ⭐️ 8.0/10

Mercor published a &quot;Labor Index: Benchmark Map&quot; analysis finding that roughly 90% of American working hours are spent on tasks that existing AI benchmarks cover little or not at all. The study further reports that, even after controlling for AI exposure, O\*NET tasks from occupations with larger wage bills are significantly overrepresented among benchmark prompts. If benchmarks mostly measure work that is not representative of what Americans actually do, then leaderboard scores and capability claims may say little about real economic impact or automation risk. This undermines how enterprises, policymakers, and labs judge AI readiness, and it means the benchmark-driven narrative about which jobs are &quot;at risk&quot; may be systematically skewed toward high-wage knowledge work. A key methodological caveat raised by readers is that the paper appears to use &quot;covered well&quot; loosely, treating a task as covered if only a handful of prompts exist — one commenter notes a social-work counseling category was labeled &quot;well covered&quot; on the basis of just 13 prompts. The analysis is also based on O\*NET occupational task taxonomies and wage-bill weighting, so its conclusions depend heavily on how coverage thresholds and exposure controls are defined.

hackernews · speckx · Oct 16, 17:08 · [Discussion](https://news.ycombinator.com/item?id=50121179)

**Background**: AI benchmarks are standardized test suites — such as question sets or task prompts — used to compare model capabilities and produce leaderboards. O\*NET is the US Department of Labor&\#x27;s occupational database that breaks jobs down into granular tasks, which researchers use to map AI exposure onto the labor market. Mercor is a San Francisco-based AI data startup founded in 2023 that supplies domain experts to frontier AI labs for post-training work including RLHF, supervised fine-tuning, model evaluation, and benchmark construction — meaning it has a direct commercial interest in where benchmarks fall short.

<details><summary>References</summary>
<ul>
<li><a href="https://www.mercor.com/">Mercor | Organizing human intelligence to power the AI economy</a></li>
<li><a href="https://en.wikipedia.org/wiki/Mercor">Mercor - Wikipedia</a></li>
<li><a href="https://arxiv.org/html/2607.01254">The Benchmark Ceiling: Human Judgment, Evaluation Scarcity, and...</a></li>

</ul>
</details>

**Discussion**: Commenters broadly agreed the finding is meaningful but challenged its framing: one invoked the Doorman Fallacy \(automating an obvious task destroys hidden value the worker also provided\), and another argued &quot;covered well&quot; is being used as a synonym for &quot;covered at all.&quot; Others connected it to Baumol&\#x27;s Cost Disease — individual productivity gains get absorbed by surrounding low-automation work like presentations, Jira, and QA — and to Karpathy&\#x27;s claim that AI currently tackles only 2-5% of work, with the gap between heavy and light AI users widening.

**Tags**: `#AI benchmarks`, `#labor economics`, `#AI evaluation`, `#future of work`, `#research analysis`

---

<a id="item-5"></a>
## [Big Fish: Exploiting a 37-Year-Old OpenBSD Kernel Bug](https://calif.io/research/big-fish) ⭐️ 8.0/10

A technical write-up titled &quot;Big Fish&quot; published at calif.io/research/big-fish describes exploiting a 37-year-old kernel bug in OpenBSD and discusses how such a long-lived vulnerability evaded code review. The post includes an exploit and argues that the flaw survived in one of the most heavily audited codebases. OpenBSD is widely regarded as a security-focused operating system, so a 37-year-old kernel bug challenges assumptions about what code review alone can catch. The finding highlights the need for fuzzing, static analysis, and human reasoning about exploit primitives when hunting deep kernel flaws, and it could affect confidence in OpenBSD and downstream projects that reuse its code. Community discussion points out that the same code was accidentally fixed in NetBSD during a rewrite in August 1999, which helps explain why the bug persisted in OpenBSD but not in its sibling BSD. The write-up is an exploit analysis rather than just a bug report, and commenters question whether fuzzing or static analysis could realistically have found this class of bug.

hackernews · rs\_rs\_rs\_rs\_rs · Oct 16, 14:44 · [Discussion](https://news.ycombinator.com/item?id=50118977)

**Background**: OpenBSD is a security-focused, Unix-like operating system based on BSD, created in 1995 by Theo de Raadt as a fork of NetBSD 1.0. Its project emphasizes proactive security, correctness, and code auditing, and its code has been reused in macOS&\#x27;s PF firewall, Android&\#x27;s Bionic libc, LLVM&\#x27;s regular expression library, and Windows&\#x27; OpenSSH. Kernel bugs are flaws in the core of the operating system that can sometimes be exploited to crash the system or gain elevated privileges. A 37-year-old bug means the vulnerable code predates OpenBSD itself and was inherited from earlier BSD source, surviving multiple audits and rewrites.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenBSD">OpenBSD</a></li>
<li><a href="https://www.openbsd.org/">OpenBSD</a></li>

</ul>
</details>

**Discussion**: Commenters were impressed that the bug survived 37 years in one of the most heavily audited codebases and noted it was accidentally fixed in NetBSD during a 1999 rewrite. They debated whether fuzzing or static analysis could realistically have found this class of bug or whether it required a human reasoning about the exploit primitive. There was also lighthearted praise for the write-up&\#x27;s OpenBSD Release-style graphics and anticipation of a theme song.

**Tags**: `#security`, `#openbsd`, `#kernel`, `#vulnerability`, `#exploit`

---

<a id="item-6"></a>
## [ORL Accelerates Diffusion LLMs to 2,788 Tokens/s on a Single RTX 5090](https://www.reddit.com/r/MachineLearning/comments/1x7qgr0/research_2788_tokenss_on_a_single_rtx_5090_with_a/) ⭐️ 8.0/10

Researchers released ORL \(On-Policy Residual Learning\), a post-training method for diffusion language models that teaches them to finalize more tokens per denoising pass, together with dlmrt, a custom inference engine, and reported 2,788 tokens/s for LLaDA-2.1-mini + ORL on a single RTX 5090 and up to 7,708 tokens/s for DiffusionGemma 26B MoE + ORL in NVFP4 on 8× B200. On their converted QwenDLM-4B model, ORL raised end-to-end throughput by roughly 6.9x while lifting HumanEval pass@1 from 82.9% to 89.6%, and the team open-sourced the models, training code, evaluation pipeline, and inference engine. Diffusion language models have long promised parallel token generation but have struggled to convert that parallelism into real wall-clock speedups, so a method that cuts the number of forward passes while improving accuracy could make dLLMs a practical alternative to autoregressive decoding. The comparison against speculative decoding baselines \(1,298 tokens/s for QwenDLM-4B + ORL versus 746 tokens/s for DFlash and 405 tokens/s for EAGLE3 on a single H100 at matched accuracy\) directly targets the incumbent acceleration technique used in production serving stacks like vLLM. All reported numbers are for single-request decoding at batch size 1 and represent peak results on specific benchmarks rather than averages, and they are end-to-end system comparisons in which ORL uses dlmrt while the speculative decoders run on vLLM. Training efficiency is also notable: LLaDA-2.1-mini needed only 4.2M self-generated training tokens and 36 H100 GPU-hours of post-training, and the team co-designed the training stack with efficient residual-state capture, specialized attention kernels, and compute-balanced packing for up to 5.2x faster training steps.

reddit · r/MachineLearning · /u/arty\_photography · Oct 16, 20:03

**Background**: Autoregressive LLMs generate text one token at a time, so each token costs a full forward pass. Diffusion language models instead start from noise or masks and iteratively denoise a whole block of tokens in parallel, refining many positions at once — but they only become faster if the model can converge in fewer denoising steps. ORL addresses two problems in that setting: residual states carried across denoising steps are produced by the model itself and drift during training \(so the authors train on fresh on-policy trajectories rather than stale offline ones\), and simply supervising the final output does not teach faster convergence, which their Adjacent Entropy Contraction loss targets by rewarding each step that reduces uncertainty. dlmrt complements the algorithm on the systems side by capturing the entire denoising loop in a CUDA graph so it executes on the GPU without per-step CPU launch and synchronization overhead, and it supports NVFP4 inference on Blackwell GPUs including the consumer RTX 5090.

**Tags**: `#diffusion-language-models`, `#llm-inference`, `#model-optimization`, `#open-source`, `#machine-learning-research`

---

<a id="item-7"></a>
## [Investors Cut Anthropic IPO Valuation Expectations to About $1.5 Trillion](https://www.reuters.com/business/finance/investors-temper-anthropic-ipo-valuation-expectations-over-revenue-growth-2026-10-15/) ⭐️ 8.0/10

Anthropic reported third-quarter revenue of $16.8 billion, up 45% quarter-over-quarter, and reached adjusted profitability with positive quarterly cash flow, yet some investors lowered their IPO valuation expectations for the company from $2 trillion to roughly $1.5 trillion. The downgrade reflects slowing growth, intensifying price competition among frontier models, and mounting pressure from compute spending. The revision signals that public-market investors are applying stricter scrutiny to AI companies&\#x27; growth quality, margins, and capital efficiency rather than rewarding revenue growth alone. It could act as a valuation stress test for other AI firms, including Zhipu, MiniMax, Kimi and DeepSeek, as markets shift their focus toward revenue durability, gross margins and capital efficiency. Even with 45% quarter-over-quarter revenue growth and positive cash flow, the cut in expected valuation suggests investors are discounting future growth rates rather than current results. The cited drivers — decelerating growth, aggressive model price competition, and heavy compute capital expenditure — are the same pressures facing most large-model developers.

telegram · zaihuapd · Oct 16, 15:46

**Background**: Anthropic is an AI company best known as the developer of the Claude family of large language models, and an IPO would mean listing its shares on a public stock exchange for the first time. Valuation expectations during a pre-IPO period reflect how much investors believe the company is worth, and they can rise or fall as new financial data and market sentiment emerge. Training and running frontier AI models requires enormous amounts of computing power, so compute spending is a central factor in whether such companies can turn revenue growth into sustainable profit.

**Tags**: `#Anthropic`, `#IPO`, `#AI industry`, `#valuation`, `#AI investment`

---