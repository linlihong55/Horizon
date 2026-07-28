---
layout: default
title: "Horizon Summary: 2026-07-28 (EN)"
date: 2026-07-28
lang: en
---

> From 29 items, 10 important content pieces were selected

---

1. [Moonshot AI Open-Sources Kimi K3: 2.8 Trillion Parameters](#item-1) ⭐️ 10.0/10
2. [vLLM v0.26.0 Released: Inkling, DeepSeek-V4 Boosts, fp32 lm\_head](#item-2) ⭐️ 9.0/10
3. [Anthropic clarifies stance on open-weights AI models](#item-3) ⭐️ 8.0/10
4. [Judge Rejects Google&\#x27;s DMCA Argument Against Scraping](#item-4) ⭐️ 8.0/10
5. [Paged Out \#9: Free Technical Magazine Delights Hacker Community](#item-5) ⭐️ 8.0/10
6. [Pre-training data audit gate proposed for ML workflows](#item-6) ⭐️ 8.0/10
7. [Google Teases Gemini 4 as Most Ambitious Pretraining Yet](#item-7) ⭐️ 8.0/10
8. [Fastjson2 Critical RCE Vulnerability Disclosed, No Patch](#item-8) ⭐️ 8.0/10
9. [China Refutes US Sanctions Threat Over AI Model Distillation](#item-9) ⭐️ 8.0/10
10. [China Begins Mass Production of Domestic DUV Lithography Tools](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Moonshot AI Open-Sources Kimi K3: 2.8 Trillion Parameters](https://huggingface.co/moonshotai/Kimi-K3) ⭐️ 10.0/10

Moonshot AI has released the weights of Kimi K3, the first open-weight model with 2.8 trillion total parameters and 104 billion active parameters, using a novel Mixture-of-Experts \(MoE\) architecture with 896 experts. This marks a major milestone in open AI research, as K3 rivals proprietary frontier models like GPT-5.6 Sol and Claude Fable 5, while being freely available for download and deployment. The model uses Kimi Delta Attention \(KDA\) and Attention Residuals \(AttnRes\) for efficient linear attention, Stable LatentMoE framework with 16 of 896 experts active per token, and supports 1M token context window with MXFP4 quantization. The license imposes restrictions on large-scale commercial use.

telegram · zaihuapd · Jul 27, 15:15

**Background**: Large language models typically have billions of parameters, but K3 pushes to trillions. Mixture-of-Experts \(MoE\) models activate only a subset of parameters per token to balance scale and compute cost. KDA is a linear attention mechanism that reduces memory usage compared to standard softmax attention. MXFP4 is a 4-bit floating-point format that significantly reduces model size without major accuracy loss.

<details><summary>References</summary>
<ul>
<li><a href="https://www.kimi.com/blog/kimi-k3">Kimi K3 Tech Blog: Open Frontier Intelligence</a></li>
<li><a href="https://huggingface.co/blog/RakshitAralimatti/learn-ai-with-me">What’s MXFP4? The 4-Bit Secret Powering OpenAI’s GPT‑OSS Models on Modest Hardware</a></li>

</ul>
</details>

**Discussion**: Based on the provided RSS content and comments \(from Simon Willison\), the community notes that the K3 license is more restrictive than the K2 license, requiring a separate agreement for large &\#x27;Model as a Service&\#x27; businesses. Kimi does not call it &\#x27;open source&\#x27; but &\#x27;open weight&\#x27;. OpenRouter already offers K3 from multiple providers at competitive pricing.

**Tags**: `#open-source`, `#large language model`, `#Moonshot AI`, `#2.8 trillion parameters`, `#MoE`

---

<a id="item-2"></a>
## [vLLM v0.26.0 Released: Inkling, DeepSeek-V4 Boosts, fp32 lm\_head](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 9.0/10

vLLM v0.26.0 introduces support for the Inkling model family \(975B MoE, multimodal, 1M context\) and includes significant performance improvements for DeepSeek-V4, such as a specialized routing kernel and fused\_topk\_bias. It also adds fp32 lm\_head support for generation models via head\_dtype and allows flexible attention backend selection per KV-cache group. This release significantly expands vLLM&\#x27;s model support and inference performance, benefiting users of large-scale MoE models like Inkling and DeepSeek-V4. The fp32 lm\_head and flexible attention backends improve accuracy and adaptability for hybrid models, reinforcing vLLM&\#x27;s position as a leading LLM inference engine. The release includes 411 commits from 212 contributors, with 61 new contributors. New models added include the Inkling family, BertForMaskedLM, and RobertaForTokenClassification. KV offloading and tiered secondary storage saw substantial maturation, and the Rust frontend gained multimodal video and audio support.

github · khluu · Jul 27, 01:06

**Background**: vLLM is an open-source library for fast LLM inference and serving, supporting many model architectures and quantization methods. The Inkling model is a 975B parameter Mixture-of-Experts model developed by Thinking Machines Lab, featuring multimodal inputs and a 1M context window. DeepSeek-V4 is the latest iteration of the DeepSeek series, a large MoE model. FP32 lm\_head refers to using float32 precision for the language model head to improve generation accuracy.

<details><summary>References</summary>
<ul>
<li><a href="https://inkling-model.com/">Inkling Model : Architecture, Capabilities, Context &amp; Access</a></li>
<li><a href="https://www.digitalocean.com/community/tutorials/flashattention-4-llm-inference-optimization">FlashAttention 4: Faster, Memory-Efficient Attention for... | DigitalOcean</a></li>
<li><a href="https://www.spheron.network/blog/nvfp4-vs-mxfp4-gpu-cloud-4bit-quantization-guide/">NVFP 4 vs MXFP4: 4-Bit Quantization Format Decision... | Spheron Blog</a></li>

</ul>
</details>

**Tags**: `#vLLM`, `#LLM inference`, `#release`, `#performance optimization`, `#AI infrastructure`

---

<a id="item-3"></a>
## [Anthropic clarifies stance on open-weights AI models](https://www.anthropic.com/news/position-open-weights-models) ⭐️ 8.0/10

Anthropic published a position statement clarifying they do not advocate for banning open-weights models, but support mandatory safety testing for all sufficiently capable models, both open and closed. This position shapes the ongoing debate on AI regulation, as mandatory safety testing could effectively limit open-weights models if testing requirements become prohibitive or are selectively enforced, potentially setting a precedent for future regulation. The statement was authored by Anthropic CEO Dario Amodei and includes support for measures such as banning chip sales to China, which critics argue contradicts the claim of not advocating bans.

hackernews · surprisetalk · Jul 27, 22:03 · [Discussion](https://news.ycombinator.com/item?id=49076057)

**Background**: Open-weights models are AI models whose trained parameters \(weights\) are publicly released, allowing anyone to download, run, and fine-tune them on their own hardware. Unlike fully open-source AI, open-weights models may not include training data, code, or documentation. The debate centers on whether these models should be subject to safety testing before release to prevent misuse, with concerns that such testing could be used as a barrier to open access.

<details><summary>References</summary>
<ul>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>
<li><a href="https://opensource.org/ai/open-weights">Open Weights: not quite what you’ve been told</a></li>

</ul>
</details>

**Discussion**: Commenters largely criticized Anthropic&\#x27;s position, arguing that mandatory safety testing amounts to a de facto ban, citing historical examples where certification processes were used to restrict access. Others pointed out inconsistency with supporting hardware bans while opposing software bans, and questioned the credibility of Anthropic&\#x27;s motives given its commercial interests.

**Tags**: `#AI safety`, `#open-weights`, `#regulation`, `#Anthropic`, `#open source`

---

<a id="item-4"></a>
## [Judge Rejects Google&\#x27;s DMCA Argument Against Scraping](https://www.techdirt.com/2026/07/27/judge-rejects-googles-attempt-to-dmca-its-way-out-of-being-scraped/) ⭐️ 8.0/10

A judge ruled that Google&\#x27;s attempt to use the Digital Millennium Copyright Act \(DMCA\) to prevent scraping of its search results is invalid. This decision was in response to a lawsuit filed by Google against SerpAPI, a third-party service that scrapes Google&\#x27;s search results. This ruling sets an important legal precedent that DMCA does not shield search engines from scraping, potentially affecting how big tech companies protect their data. It also highlights the tension between Google&\#x27;s own web-crawling origins and its current efforts to limit access to its results. The judge found that Google&\#x27;s search results are not copyrightable compilations under DMCA, as they lack the required originality or creative selection. The case did not address other legal bases like breach of contract or trespass, leaving room for future litigation.

hackernews · cdrnsf · Jul 27, 18:15 · [Discussion](https://news.ycombinator.com/item?id=49073513)

**Background**: The Digital Millennium Copyright Act \(DMCA\) is a U.S. copyright law that provides protections against circumvention of technological measures controlling access to copyrighted works. Web scraping, the automated collection of data from websites, has been a legally contested area, with courts often ruling that scraping public data does not violate the Computer Fraud and Abuse Act \(CFAA\). However, the applicability of DMCA to search engine result pages has been less clear until this ruling.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Digital_Millennium_Copyright_Act">Digital Millennium Copyright Act - Wikipedia</a></li>
<li><a href="https://blog.apify.com/is-web-scraping-legal/">Is web scraping legal? Yes, if you know the rules.</a></li>

</ul>
</details>

**Discussion**: Community comments strongly criticized Google&\#x27;s behavior, with many noting the irony of Google, built on scraping the web, now trying to block scraping. Some highlighted the lack of good APIs as a driver for scraping, while others pointed to jurisdictional differences in copyright law. A comment also mentioned the importance of scraping for combating advertising scams.

**Tags**: `#web scraping`, `#DMCA`, `#Google`, `#legal`, `#APIs`

---

<a id="item-5"></a>
## [Paged Out \#9: Free Technical Magazine Delights Hacker Community](https://pagedout.institute/download/PagedOut_009.pdf) ⭐️ 8.0/10

Paged Out \#9 is a free, beautifully designed technical magazine that includes deep, hacker-curious articles on C programming, subpixel rendering, computable tilings, and more. It is released as a PDF and also offers print editions for purchase. This magazine revives the spirit of classic hacker zines like 2600 and Phrack, offering high-quality technical content for free, which is rare in today&\#x27;s publishing landscape. It fosters a community of curious programmers and engineers who appreciate deep dives into esoteric topics. The magazine is published by Paged Out Institute and is available for free download. Community comments highlight specific articles such as &\#x27;Baby Steps in C&\#x27;, &\#x27;The Subpixel Zoo&\#x27;, and a piece on computable tilings that rediscovers Wang&\#x27;s work from the 1960s.

hackernews · laurensr · Jul 27, 14:22 · [Discussion](https://news.ycombinator.com/item?id=49070138)

**Background**: Subpixel rendering is a technique that uses the individual red, green, and blue subpixels of a display to increase effective resolution, often used for text sharpness. Computable tilings, studied by Wang in the 1960s, link the domino problem \(whether a set of tiles can tile the plane\) to the halting problem, showing that tiling is computationally universal. These topics are explored in the magazine&\#x27;s articles.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Subpixel_rendering">Subpixel rendering</a></li>
<li><a href="https://dl.ifip.org/db/conf/ifipTCS/ifipTCS2008/LafitteW08.pdf">Computability of Tilings .</a></li>

</ul>
</details>

**Discussion**: Commenters express enthusiasm for the magazine&\#x27;s content and design, comparing it favorably to classic zines. One user notes a fun fact about the computable tilings article being an uncredited rediscovery of Wang&\#x27;s work, linking the domino problem to the halting problem. Others laugh at the &\#x27;Baby Steps in C&\#x27; article and plan to buy print editions.

**Tags**: `#magazine`, `#hacker`, `#technical`, `#free`, `#programming`

---

<a id="item-6"></a>
## [Pre-training data audit gate proposed for ML workflows](https://www.reddit.com/r/MachineLearning/comments/1v8a3nu/training_data_needs_a_real_gonogo_gate_before/) ⭐️ 8.0/10

A Reddit user proposed a formal, reproducible pre-training data audit system that gates training based on explicit evidence such as data leakage, contradictions, redundancy, and coverage, without relying on LLM verdicts. This concept addresses a critical gap in ML pipelines by adding a rigorous gate before training, potentially improving reproducibility, reducing failures, and increasing trust in model development. The system outputs verdicts of PASS, WARNING, FAIL, or FAIL\_SECURITY, and can generate a repair plan that applies only approved changes to a derived copy while preserving the original. It uses manifests and checksums for traceability.

reddit · r/MachineLearning · /u/jesusmjk · Jul 27, 19:13

**Background**: Data leakage in machine learning occurs when training data contains information that would not be available at prediction time, leading to overoptimistic performance estimates. Contradiction detection identifies conflicting data points within or across datasets. Data provenance tracks the origin and transformation of data throughout the ML lifecycle.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Leakage_%28machine_learning%29">Leakage (machine learning) - Wikipedia</a></li>
<li><a href="https://www.shadecoder.com/topics/contradiction-detection-a-comprehensive-guide-for-2025">Contradiction Detection: A Comprehensive Guide for 2025 - Shadecoder - 100% Invisibile AI Coding Interview Copilot</a></li>
<li><a href="https://mlip-cmu.github.io/s2023/slides/21_provenance/provenance.pdf">Versioning, Provenance</a></li>

</ul>
</details>

**Tags**: `#machine learning`, `#data quality`, `#training data`, `#MLOps`, `#reproducibility`

---

<a id="item-7"></a>
## [Google Teases Gemini 4 as Most Ambitious Pretraining Yet](https://9to5google.com/2026/07/26/google-gemini-4-teases/) ⭐️ 8.0/10

Google CEO Sundar Pichai announced during the Alphabet Q2 2026 earnings call that Gemini 4, the next-generation large language model, is now in training, calling it the company&\#x27;s most ambitious pretraining project to date. The model is expected to launch in late 2026, likely November or December. This signals Google&\#x27;s continued commitment to leading the AI frontier, with Gemini 4 targeting significant advances over previous models. The release could impact the competitive landscape of large language models and accelerate progress toward AGI. Pichai emphasized that compute resources will be prioritized for frontier AGI research to ensure Gemini 4 remains cutting-edge upon release. Additionally, the Gemini 3.x Flash series will maintain nearly monthly updates focusing on improved coding abilities.

telegram · zaihuapd · Jul 27, 04:06

**Background**: Gemini is Google&\#x27;s family of large language models, competing with OpenAI&\#x27;s GPT series. Pretraining involves training a model on vast amounts of unlabeled data to learn general language patterns before fine-tuning for specific tasks. Google aims to achieve artificial general intelligence \(AGI\), where AI can perform any intellectual task a human can.

**Tags**: `#Gemini`, `#AI`, `#Google`, `#Large Language Model`, `#AGI`

---

<a id="item-8"></a>
## [Fastjson2 Critical RCE Vulnerability Disclosed, No Patch](https://mp.weixin.qq.com/s/LJaul1jNjK9pXRAkoUiMEA) ⭐️ 8.0/10

On July 27, 2024, Chaitin Technology disclosed a remote code execution \(RCE\) vulnerability in Fastjson2, affecting all versions up to 2.0.62. Attackers can bypass AutoType validation via crafted JSON data to execute arbitrary code. Fastjson2 is widely used in Java applications, especially in Alibaba ecosystem projects like Dubbo. This high-severity vulnerability puts a large number of applications at risk of remote compromise, and developers must urgently disable AutoType or apply interim mitigations until an official patch is available. The vulnerability details and exploit code have not been publicly released. This is the second critical vulnerability in the Fastjson series this month, following one in Fastjson1. The maintainer acknowledged the issue but the PR \#7695 fix was not merged into the main branch, leaving all released versions vulnerable.

telegram · zaihuapd · Jul 27, 10:31

**Background**: Fastjson2 is a high-performance JSON library for Java developed by Alibaba, designed as the successor to Fastjson. It supports the AutoType feature, which allows JSON to specify types during deserialization, but this has historically been a source of deserialization vulnerabilities. Previous Fastjson versions have faced multiple similar RCE vulnerabilities, requiring developers to understand the risks of enabling AutoType.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/alibaba/fastjson2">GitHub - alibaba/fastjson2: 🚄 FASTJSON2 is a Java JSON library with excellent performance.</a></li>
<li><a href="https://www.alphabot.com/security/blog/2020/java/Fastjson-exceptional-deserialization-vulnerabilities.html">Fastjson: exceptional deserialization vulnerabilities - Alphabot Security</a></li>

</ul>
</details>

**Tags**: `#security`, `#vulnerability`, `#Fastjson2`, `#RCE`, `#Java`

---

<a id="item-9"></a>
## [China Refutes US Sanctions Threat Over AI Model Distillation](https://www.mofcom.gov.cn/syxwfb/art/2026/art_7f1622463a7c48ef9fad600ce0ef702f.html) ⭐️ 8.0/10

On July 27, China&\#x27;s Ministry of Commerce issued a statement rejecting US plans to investigate and sanction Chinese AI firms over alleged model distillation of US frontier models, calling the accusations unfounded and warning of retaliatory measures. This marks a significant escalation in US-China tech tensions, as model distillation is a common industry practice, and the US move could disrupt global AI collaboration and open-source ecosystem. The Ministry noted that nearly 200 US startups have urged the US government not to restrict access to Chinese open-source models, highlighting that US companies also distill Chinese models.

telegram · zaihuapd · Jul 27, 11:01

**Background**: Model distillation \(knowledge distillation\) is a machine learning technique where a smaller &\#x27;student&\#x27; model learns from a larger &\#x27;teacher&\#x27; model to achieve similar performance with lower computational cost. It is widely used in AI development to reduce model size and inference time. The US has been increasingly concerned about China&\#x27;s AI advances, leading to export controls and sanctions aimed at limiting China&\#x27;s access to cutting-edge AI technologies.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Knowledge_distillation">Knowledge distillation - Wikipedia</a></li>
<li><a href="https://labelbox.com/guides/model-distillation/">What is Model Distillation?</a></li>

</ul>
</details>

**Tags**: `#AI`, `#China`, `#US`, `#regulation`, `#trade`

---

<a id="item-10"></a>
## [China Begins Mass Production of Domestic DUV Lithography Tools](https://www.theinformation.com/articles/china-starts-mass-producing-homegrown-duv-chipmaking-tools-advance-local-chip-industry) ⭐️ 8.0/10

China has started mass-producing domestic immersion DUV lithography machines, with plans to manufacture about 5 units this year and 20 by 2027, targeting domestic chipmakers like SMIC and Hua Hong Semiconductor. This milestone advances China&\#x27;s semiconductor self-sufficiency and could gradually erode ASML&\#x27;s market share in China, especially if Western export restrictions tighten. The domestic DUV tools still lag behind ASML in performance and reliability, requiring months of testing by chipmakers. Some key components are sourced from Japan, and local supply chain delays have affected progress.

telegram · zaihuapd · Jul 27, 14:10

**Background**: DUV lithography uses deep ultraviolet light \(e.g., 193nm ArF lasers\) to pattern circuits on silicon wafers. Immersion lithography uses a liquid layer between the lens and wafer to improve resolution, enabling nodes down to 7nm. ASML dominates the high-end lithography market, but export controls have spurred Chinese efforts to develop domestic alternatives.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DUV_lithography">DUV lithography</a></li>
<li><a href="https://en.wikipedia.org/wiki/Immersion_lithography">Immersion lithography</a></li>

</ul>
</details>

**Tags**: `#semiconductor`, `#lithography`, `#China`, `#ASML`, `#chip manufacturing`

---