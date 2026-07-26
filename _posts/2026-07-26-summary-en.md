---
layout: default
title: "Horizon Summary: 2026-07-26 (EN)"
date: 2026-07-26
lang: en
---

> From 28 items, 7 important content pieces were selected

---

1. [vLLM v0.26.0 adds Inkling model, boosts DeepSeek-V4](#item-1) ⭐️ 9.0/10
2. [SGLang v0.5.16: DSpark Speculative Decoding and Inkling Support](#item-2) ⭐️ 9.0/10
3. [Open-weight AI is having its Kubernetes moment](#item-3) ⭐️ 8.0/10
4. [Grassroots movement disables Flock surveillance cameras](#item-4) ⭐️ 8.0/10
5. [Ruff v0.16.0 Expands Default Rules from 59 to 413](#item-5) ⭐️ 8.0/10
6. [Claude Opus 5 Shows Strong Prompt Injection Resistance](#item-6) ⭐️ 8.0/10
7. [AMD&\#x27;s Strategy to Break Nvidia&\#x27;s CUDA Moat](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [vLLM v0.26.0 adds Inkling model, boosts DeepSeek-V4](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 9.0/10

vLLM v0.26.0 introduces support for the Inkling model family, delivers performance improvements for DeepSeek-V4, and adds features like fp32 lm\_head via head\_dtype, flexible attention backends, and matured KV offloading. This release strengthens vLLM as a versatile inference engine for cutting-edge open-weight models like Inkling \(975B parameters\) and optimizes performance for widely-used DeepSeek models, benefiting both researchers and production deployments. Inkling support includes base modeling, piecewise CUDA graphs, Hopper FA4 relative attention, MTP=1 speculative decoding, LoRA, and NVFP4 quantization. DeepSeek-V4 gains a specialized routing kernel \(2.94% E2E TPOT improvement\) and fused\_topk\_bias \(1.5–2x kernel speedup\).

github · khluu · Jul 25, 10:38

**Background**: vLLM is a high-performance open-source library for LLM inference, supporting various models and hardware. The Inkling model is a 975B-parameter mixture-of-experts transformer with 41B active parameters, pretrained on 45 trillion tokens and supporting up to 1M context tokens. NVFP4 is a 4-bit floating-point quantization format that retains higher dynamic range than INT4.

<details><summary>References</summary>
<ul>
<li><a href="https://thinkingmachines.ai/news/introducing-inkling/">Inkling: Our Open-Weights Model - Thinking Machines Lab</a></li>
<li><a href="https://www.technology.org/2026/07/16/thinking-machines-inkling-open-weights-model/">Thinking Machines Releases Inkling, Its First Open-Weights Model, Trained From Scratch</a></li>
<li><a href="https://developer.nvidia.com/blog/introducing-nvfp4-for-efficient-and-accurate-low-precision-inference/">Introducing NVFP4 for Efficient and Accurate Low-Precision Inference | NVIDIA Technical Blog</a></li>

</ul>
</details>

**Tags**: `#vLLM`, `#LLM inference`, `#release`, `#DeepSeek`, `#performance`

---

<a id="item-2"></a>
## [SGLang v0.5.16: DSpark Speculative Decoding and Inkling Support](https://github.com/sgl-project/sglang/releases/tag/v0.5.16) ⭐️ 9.0/10

SGLang v0.5.16 introduces DSpark speculative decoding, achieving 383.7 tok/s on DeepSeek-V4-Pro, and adds support for the 975B-parameter Inkling multimodal MoE model. The release includes 574 pull requests from 169 contributors, marking a major update. This release significantly boosts LLM inference performance with adaptive speculative decoding, and extends SGLang&\#x27;s support to cutting-edge multimodal MoE models, benefiting both researchers and production deployments. DSpark uses semi-autoregressive drafting and confidence-based verification, reaching up to 383.7 tok/s with an accept length of ~5 on Blackwell B300 TP8. Inkling combines sliding-window, full, and Mamba2 linear attention with NVFP4 MoE and native MTP, achieving up to 71.7k tok/s input and 171.0 tok/s per-user decode.

github · Qiaolin-Yu · Jul 25, 00:13

**Background**: Speculative decoding is a technique that uses a smaller draft model to generate multiple tokens, then verifies them with the larger target model, achieving speedup without quality loss. SGLang is an open-source serving framework for large language models, optimized for fast inference. DSpark, originally released by DeepSeek, reduces inference latency by up to 85% by scheduling verification based on confidence.

<details><summary>References</summary>
<ul>
<li><a href="https://www.techtimes.com/articles/319236/20260628/deepseek-releases-dspark-speculative-decoding-makes-v4-85-percent-faster.htm">DeepSeek Releases DSpark: Speculative Decoding Makes V4 Up to 85 Percent Faster</a></li>
<li><a href="https://thinkingmachines.ai/news/introducing-inkling/">Inkling: Our Open-Weights Model - Thinking Machines Lab</a></li>
<li><a href="https://www.marktechpost.com/2026/07/15/thinking-machines-lab-releases-inkling-a-975b-parameter-open-weights-multimodal-moe-with-41b-active-parameters-and-controllable-thinking-effort/">Thinking Machines Lab Releases Inkling: A 975B-Parameter Open ...</a></li>

</ul>
</details>

**Tags**: `#speculative decoding`, `#LLM serving`, `#SGLang`, `#multimodal MoE`, `#high performance`

---

<a id="item-3"></a>
## [Open-weight AI is having its Kubernetes moment](https://tobi.knaup.me/2026-07-25-open-weight-ai-is-having-its-kubernetes-moment/) ⭐️ 8.0/10

An article argues that open-weight AI models are becoming the standard infrastructure layer, similar to how Kubernetes became the standard for container orchestration in cloud computing. This analogy suggests open-weight models could become indispensable infrastructure, reshaping competition, regulation, and startup viability, with implications for how American labs need to compete against Chinese models. Open-weight models release the trained parameters \(weights\) but not necessarily the training data or full source code, enabling anyone to host, fine-tune, or build on them while lacking full open-source transparency.

hackernews · tknaup · Jul 25, 14:49 · [Discussion](https://news.ycombinator.com/item?id=49048034)

**Background**: Kubernetes is an open-source system that automates deployment, scaling, and management of containerized applications, becoming the de facto standard cloud infrastructure layer. Similarly, open-weight AI models release the learned weights of a neural network, allowing users to run inference or fine-tune the model, but they differ from fully open-source AI \(which also includes training data and code\). The article draws a parallel between the two as standardized, widely adopted infrastructure that enables innovation on top.

<details><summary>References</summary>
<ul>
<li><a href="https://www.linkedin.com/pulse/open-weight-ai-what-we-finally-opened-bonnet-nicolas-pistorio-n3ulf">Open - weight AI : what if we finally opened the bonnet ?</a></li>
<li><a href="https://openai.com/index/introducing-gpt-oss/">Introducing gpt-oss | OpenAI</a></li>

</ul>
</details>

**Discussion**: Community comments highlight several key points: some argue that banning models by country of origin is technically infeasible since weights are just numbers \(ozgung\); others find &\#x27;tokenomics&\#x27; pricing confusing \(firasd\); there is support for a collaborative, Linux-like AI model built by many companies \(pianopatrick\); and some note that OpenAI has released older open-weight models but rarely updates them \(drnick1\). Overall sentiment is positive about the analogy but concerned about practical and regulatory challenges.

**Tags**: `#open-weight models`, `#AI infrastructure`, `#Kubernetes`, `#open source AI`, `#AI regulation`

---

<a id="item-4"></a>
## [Grassroots movement disables Flock surveillance cameras](https://www.theguardian.com/us-news/ng-interactive/2026/jul/25/flock-surveillance-cameras) ⭐️ 8.0/10

A Guardian article reports that citizens are increasingly disabling Flock surveillance cameras through direct action, citing privacy violations and distrust in authorities. 这种草根反抗凸显了公众对无处不在的监控技术日益增长的抵制，并引发了关于公共安全与公民自由平衡的质疑。 Flock cameras are license plate readers used by law enforcement, but a 2021 study found a 10% error rate in their output. The disabling movement includes acts like using pool skimmers with cardboard to block cameras.

hackernews · bookofjoe · Jul 25, 19:02 · [Discussion](https://news.ycombinator.com/item?id=49050538)

**Background**: Flock Safety is a company that sells automated license plate recognition cameras to police departments and private entities. The cameras are mounted in public spaces to record every passing vehicle, which has raised significant privacy concerns. Critics argue that such surveillance can be misused and erode public trust.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Flock_Safety">Flock Safety - Wikipedia</a></li>
<li><a href="https://trafficvision.live/blog/flock-cameras">Flock Cameras : What They Are &amp; Can You Watch... | TrafficVision.Live</a></li>

</ul>
</details>

**Discussion**: Comments express strong support for the grassroots actions, with some noting that extreme criminality at high political levels undermines the stated purpose of the cameras. Others suggest counter-measures like pointing cameras at politicians&\#x27; homes. The sentiment is that when people feel unheard, vigilantism is inevitable.

**Tags**: `#surveillance`, `#privacy`, `#civil liberties`, `#vigilantism`, `#technology`

---

<a id="item-5"></a>
## [Ruff v0.16.0 Expands Default Rules from 59 to 413](https://simonwillison.net/2026/Jul/25/ruff/#atom-everything) ⭐️ 8.0/10

Astral released Ruff v0.16.0 on July 23rd, which increases the default lint rule set from 59 to 413 rules, enabling many previously opt-in checks by default. This change will affect virtually all Ruff users and CI pipelines, as existing projects may suddenly see hundreds of new warnings or errors. Developers with unpinned dependencies may experience broken CI builds until they update their code or pin the old Ruff version. The default rule set had not been updated since Ruff v0.1.0, despite the total number of available rules growing from 708 to 968. The release includes &\#x27;unsafe-fixes&\#x27; for automated resolution, and the author of the news post successfully applied automatic fixes to three major projects, fixing up to 1,538 errors per project.

rss · Simon Willison · Jul 25, 22:44

**Background**: Ruff is an extremely fast Python linter and code formatter written in Rust, designed as a drop-in replacement for tools like Flake8, isort, and pyupgrade. It re-implements over 900 lint rules from dozens of existing tools and runs 10-100x faster than its predecessors. The default rule set previously only enabled a small subset \(59 rules\) to minimize false positives for new users, but this release flips many more rules on by default to catch more issues early.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.astral.sh/ruff/linter/">The Ruff Linter | Ruff - Astral</a></li>
<li><a href="https://github.com/astral-sh/ruff">GitHub - astral-sh/ruff: An extremely fast Python linter and ... ruff · PyPI Ruff - Astral Ruff: Complete Guide to Python&#x27;s Fastest Linter | pydevtools GitHub - sartcod/ruff: An extremely fast Python linter and ... Ruff: A Modern Python Linter for Error-Free and Maintainable ...</a></li>

</ul>
</details>

**Tags**: `#Python`, `#linting`, `#Ruff`, `#tooling`

---

<a id="item-6"></a>
## [Claude Opus 5 Shows Strong Prompt Injection Resistance](https://simonwillison.net/2026/Jul/25/boris-cherny/#atom-everything) ⭐️ 8.0/10

Boris Cherny highlighted that Anthropic&\#x27;s Claude Opus 5 model is the least prompt injectable model yet, as detailed in its system card. This marks a significant safety improvement for large language models, addressing a critical vulnerability that can bypass model safeguards. Enhanced prompt injection resistance is vital for deploying AI in sensitive applications. The claim is based on prompt injection evaluations and red teaming, with details buried on page 73 of the Claude Opus 5 System Card. The model appears very hard to prompt inject successfully.

rss · Simon Willison · Jul 25, 00:42

**Background**: Prompt injection is a cybersecurity exploit where malicious inputs cause LLMs to ignore developer instructions or perform unintended actions. It can be direct or indirect, e.g., via web content. Red teaming involves adversarial testing to uncover vulnerabilities. These evaluations are crucial for AI safety.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection">Prompt injection</a></li>
<li><a href="https://en.wikipedia.org/wiki/Red_teaming">Red teaming</a></li>
<li><a href="https://owasp.org/www-community/attacks/PromptInjection">Prompt Injection - OWASP Foundation</a></li>

</ul>
</details>

**Tags**: `#prompt-injection`, `#anthropic`, `#claude`, `#ai-safety`, `#generative-ai`

---

<a id="item-7"></a>
## [AMD&\#x27;s Strategy to Break Nvidia&\#x27;s CUDA Moat](https://newsletter.semianalysis.com/p/can-amd-break-the-cuda-moat-amd-advancing) ⭐️ 8.0/10

A detailed analysis from SemiAnalysis reveals AMD&\#x27;s multifaceted approach to challenge Nvidia&\#x27;s CUDA dominance, including agentic kernel generation, software quality improvements, aggressive pricing with up to 105% discounts, and the Helios MI455X rack-scale system facing production ramp challenges. If successful, AMD&\#x27;s efforts could erode Nvidia&\#x27;s near-monopoly in AI training and inference, potentially lowering costs and increasing hardware options for AI developers. The analysis highlights both technical and financial tactics that could shift the competitive landscape. AMD&\#x27;s agentic kernel generation \(e.g., GEAK\) aims to automate kernel optimization, addressing a key weakness in software quality. However, internal development clusters remain unstable, and the Helios MI455X production ramp is described as &\#x27;hell,&\#x27; while finance engineering offers up to 105% equity rebate discounts to attract customers like OpenAI.

rss · Semianalysis · Jul 25, 00:33

**Background**: Nvidia&\#x27;s CUDA ecosystem has long been a formidable barrier to entry for competitors, as many AI frameworks and optimized libraries are built specifically for CUDA. AMD&\#x27;s ROCm software stack aims to provide compatibility and performance, but historically has lagged in quality and developer adoption. Agentic kernel generation uses AI to automatically create optimized GPU kernels, potentially reducing the manual effort required to match Nvidia&\#x27;s performance.

<details><summary>References</summary>
<ul>
<li><a href="https://newsletter.semianalysis.com/p/can-amd-break-the-cuda-moat-amd-advancing">Can AMD break the CUDA Moat? AMD Advancing AI 2026</a></li>
<li><a href="https://www.tomshardware.com/pc-components/gpus/amd-takes-the-wraps-off-its-instinct-mi455x-ai-accelerator-cdna-5-and-helios-rack-scale-architecture-combine-to-take-the-fight-to-nvidia-in-the-data-center">AMD takes the wraps off its Instinct MI455X AI accelerator — CDNA 5 and Helios rack-scale architecture combine to take the fight to Nvidia in the data center | Tom&#x27;s Hardware</a></li>
<li><a href="https://www.amd.com/en/products/rackscale-solutions/helios.html">AMD Helios Rackscale Solution – Powering Frontier AI</a></li>

</ul>
</details>

**Tags**: `#AMD`, `#CUDA`, `#GPU Computing`, `#AI Hardware`, `#Software Ecosystem`

---