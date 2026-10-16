---
layout: default
title: "Horizon Summary: 2026-10-16 (EN)"
date: 2026-10-16
lang: en
---

> From 42 items, 5 important content pieces were selected

---

1. [Citizen Lab: Targeted Ads Used as Pipeline for Zero-Click Mercenary Spyware](#item-1) ⭐️ 9.0/10
2. [Meta Releases Muse Spark Open, an 816B-Parameter Open-Weight MoE Model](#item-2) ⭐️ 8.0/10
3. [Goodfire&\#x27;s Nick Cammarata argues neural networks learn clean, separable features](#item-3) ⭐️ 8.0/10
4. [ASML Reportedly Developing a Hybrid Bonding Tool](#item-4) ⭐️ 8.0/10
5. [Random Neural Networks Self-Assemble Learning Motifs, Match Backprop](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Citizen Lab: Targeted Ads Used as Pipeline for Zero-Click Mercenary Spyware](https://citizenlab.ca/research/how-discover-tech-turned-targeted-ads-into-a-pipeline-for-spyware/) ⭐️ 9.0/10

Citizen Lab published a report on October 15, 2026 titled &quot;Exposing AdFection: How Discover-Tech Turned Targeted Ads Into a Pipeline for Zero-Click Mercenary Spyware,&quot; alleging that the Israeli advertising firm Discover-Tech served targeted ads that silently installed mercenary spyware on victims&\#x27; devices without any user interaction. According to coverage of the report, the ad infrastructure reached more than 70,000 apps and over 120,000 websites. This is reportedly the first confirmed case of mercenary spyware being delivered through targeted advertising, moving the zero-click threat from messaging apps into the advertising layer that is embedded in a large share of everyday apps and websites. It raises hard questions about who is accountable in the adtech supply chain, since ads and the SDKs behind them are a near-universal and largely unaudited attack surface. Coverage notes that the report documents the ad-based distribution and command-and-control infrastructure in some detail but is vaguer about the exact mechanism that triggered the zero-click activation, and no specific ad network or vulnerability was publicly named as the sole vector. The ads reportedly allowed spyware to be used against specific targets, indicating selective rather than mass targeting, and the affected apps and sites were counted in the tens of thousands.

hackernews · jcomp · Oct 15, 10:43 · [Discussion](https://news.ycombinator.com/item?id=50101813)

**Background**: Mercenary spyware is commercial surveillance software sold to governments and other clients, typically designed to remotely compromise phones and extract messages, location and other data; Apple and others periodically send threat notifications to users targeted by such tools. &quot;Zero-click&quot; means the compromise requires no tap, download or link click from the victim, historically achieved through vulnerabilities in messaging or communication apps. Adtech is the ecosystem of networks, exchanges and software development kits \(SDKs\) that place ads inside apps and websites, gathering targeting data about users in the process.

<details><summary>References</summary>
<ul>
<li><a href="https://citizenlab.ca/research/exposing-adfection-executive-summary/">Exposing AdFection Executive Summary - The Citizen Lab</a></li>
<li><a href="https://arstechnica.com/security/2026/10/targeted-ads-delivered-0-click-exploits-to-install-mercenary-malware/">Targeted ads delivered 0-click exploits to install mercenary ...</a></li>
<li><a href="https://www.theguardian.com/technology/2026/oct/15/israeli-firm-digital-ads-enabling-installation-of-zero-click-spyware-researchers-say">Online ads weaponised to deliver ‘zero-click’ spyware ...</a></li>

</ul>
</details>

**Discussion**: The Hacker News discussion was highly engaged and split: a self-described 13-year adtech engineer argued the &quot;zero-click&quot; framing is sensationalist and that the report is vague about the actual activation mechanism, while also stressing that there is no single accountable &quot;ad provider&quot; in the fragmented adtech ecosystem. Other commenters focused on geopolitics, arguing that Israeli cybersecurity firms should be viewed as tied to the state and questioning why Israel has become such a dominant cyber power, while some simply shared the original Citizen Lab report link.

**Tags**: `#security`, `#spyware`, `#adtech`, `#privacy`, `#surveillance`

---

<a id="item-2"></a>
## [Meta Releases Muse Spark Open, an 816B-Parameter Open-Weight MoE Model](https://research.meta.ai/blog/muse-spark-open) ⭐️ 8.0/10

Meta launched Muse Spark Open, an 816B-parameter mixture-of-experts open-weight model listed on Hugging Face as Muse-Spark-Open-816B-A42B, meaning 816B total parameters with roughly 42B active per token. Meta published build and deployment documentation and is marketing the model as optimized to run on local hardware such as a Mac Studio. A new 816B-scale open-weight release from Meta is a major event for the open-weight LLM ecosystem, since it gives developers a large, locally deployable option without relying on a hosted API. At the same time, the model reportedly trails rivals such as Qwen3.8 Flash Next and GLM 5.3 Flash on Artificial Analysis, so the release is as much a statement about Meta&\#x27;s open-weight strategy as it is a technical leap. The model&\#x27;s naming indicates a sparse MoE design with 816B total and about 42B active parameters, and Meta has invested in broad runner support including Unsloth and MLX, according to community reports and Meta&\#x27;s deploy docs. The license is permissive for most uses but contains a &quot;Model as a Service&quot; clause restricting third parties from reselling model outputs via API if the licensee and its affiliates exceed $20M in aggregate gross revenue.

hackernews · bigwheels · Oct 15, 17:47 · [Discussion](https://news.ycombinator.com/item?id=50107379)

**Background**: Mixture-of-experts \(MoE\) models split a network into specialized sub-networks called experts and use a router to activate only the most relevant ones for each token, letting models scale to very large parameter counts without paying the full compute cost per token. This is why parameter counts come in two numbers: total parameters determine the memory needed to hold the weights, while active parameters determine the compute spent per token. &quot;Open-weight&quot; means the trained weights are published, but the license may still restrict commercial uses — a spectrum that ranges from permissive licenses like Apache 2.0 to custom licenses with revenue thresholds and field-of-use limits.

<details><summary>References</summary>
<ul>
<li><a href="https://www.f22labs.com/blogs/active-vs-total-parameters-whats-the-difference/">Active vs Total Parameters: What’s the Difference?</a></li>
<li><a href="https://researchaudio.io/p/mixture-of-experts-moe-in-large-language-models">Mixture of Experts ( MoE ) in Large Language Models</a></li>
<li><a href="https://intuitionlabs.ai/articles/open-weight-ai-model-licenses">Open-Weight AI Model Licenses: Commercial Use Rules Explained</a></li>

</ul>
</details>

**Discussion**: Commenters were largely measured rather than impressed: one noted the model underperforms Qwen3.8 Flash Next and GLM 5.3 Flash \(both runnable on a single B300\) and criticized Artificial Analysis for only comparing models at the highest, production-impractical reasoning level. Others scrutinized the license&\#x27;s &quot;Model as a Service&quot; revenue clause to argue the release is not truly open weight, praised the wide runner support \(Unsloth, MLX\), and debated whether Meta&\#x27;s open-weight push is a genuine community contribution or a moat-building play around a sticky product.

**Tags**: `#open-weight-models`, `#meta-ai`, `#large-language-models`, `#model-release`, `#licensing`

---

<a id="item-3"></a>
## [Goodfire&\#x27;s Nick Cammarata argues neural networks learn clean, separable features](https://already-clean.goodfire.com/) ⭐️ 8.0/10

Nick Cammarata, a Goodfire co-founder and early co-author of mechanistic interpretability work at OpenAI, published a new essay titled &quot;Neural networks are clean&quot; \(already-clean.goodfire.com\) arguing that neural networks learn surprisingly clean, separable features rather than the messy, heavily superposed representations the field has long assumed. The essay quickly rose to 489 points on Hacker News with 187 largely technical comments. If the claim holds, it would substantially lower the difficulty of mechanistic interpretability, since much of the field&\#x27;s pessimism rests on the assumption that features are deeply entangled and hard to isolate. That matters for AI alignment, where researchers argue we cannot steer or trust systems we cannot understand. The essay functions as a large evidentiary brief: it revisits famously polysemantic neurons, catalogues cases where interpretability tooling failed, and maps out where messiness still hides in networks. Critiques in the discussion note that the evidence may not rule out parameter overloading, pointing to older results such as the Lottery Ticket Hypothesis and the Multimodal Gap paper \(arXiv:2203.02053\), which suggests networks tend toward condensed representations.

hackernews · themgt · Oct 15, 16:04 · [Discussion](https://news.ycombinator.com/item?id=50105647)

**Background**: Mechanistic interpretability is a subfield of explainable AI that tries to reverse-engineer neural networks into human-understandable features, circuits, and algorithms. A central obstacle has been superposition and polysemanticity: because models pack more concepts than they have neurons, a single neuron often fires for many unrelated ideas, making clean feature extraction hard. Cammarata co-authored early interpretability work at OpenAI \(including circuit-style analyses of vision models\) and later co-founded Goodfire, a startup focused on interpretability tooling, so his reversal from pessimism to optimism carries weight in the community.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mechanistic_interpretability">Mechanistic interpretability - Wikipedia</a></li>
<li><a href="https://arxiv.org/abs/2404.14082">[2404.14082] Mechanistic Interpretability for AI Safety -- A ... Mechanistic Interpretability for Neural Networks: Circuits ... Mechanistic Interpretability: Peeking Inside an LLM Mechanistic Interpretability Explained (2026) | Taskade Blog Mechanistic Interpretability in Neural Networks</a></li>

</ul>
</details>

**Discussion**: Sentiment is engaged but contested: sebmellen calls Cammarata &quot;a force of nature&quot; and points to his launch post framing interpretability as possibly the most important scientific problem today, while bluejay2387 argues the claims overreach what is proven, citing the Lottery Ticket Hypothesis and the Multimodal Gap work as compatible with parameter overloading. dleeftink raises a philosophical objection that a neuron&\#x27;s external context and genesis may matter more than its weights, and antics summarizes the essay as an evidentiary brief arguing it is easier than expected to &quot;sequence the AI genome.&quot;

**Tags**: `#mechanistic-interpretability`, `#AI-alignment`, `#neural-networks`, `#deep-learning`, `#research-discussion`

---

<a id="item-4"></a>
## [ASML Reportedly Developing a Hybrid Bonding Tool](https://newsletter.semianalysis.com/p/asml-is-building-a-hybrid-bonding) ⭐️ 8.0/10

According to a SemiAnalysis report, ASML is building a hybrid bonding tool, an entry into advanced packaging equipment that the company has not officially announced. The claim is based on ASML&\#x27;s own patent filings, a news report, and its published technology roadmap, all of which point toward a hybrid bonding product. Hybrid bonding is a cornerstone of advanced packaging and 3D chip stacking, an area where demand has surged with AI accelerators and where TSMC&\#x27;s CoWoS and SoIC capacity is strained. If ASML — the dominant supplier of EUV lithography — enters this space, it could reshape the competitive landscape of advanced packaging tooling and give the company a new growth vector beyond lithography. The evidence is currently indirect: no product name, specifications, timeline, or customer commitments have been disclosed. Notably, hybrid bonding requires extremely flat dielectric surfaces and ultra-fine interconnect pitch so that copper pads on two dies make direct contact, a process discipline closer to wafer-level deposition and CMP than to lithography and overlay.

rss · Semianalysis · Oct 15, 19:27

**Background**: Hybrid bonding is an advanced packaging technique in which copper pads are embedded in an extremely flat dielectric surface, allowing two wafers or dies to bond directly at very fine interconnect pitch without solder bumps. It is central to 3D IC stacking and heterogeneous integration, where multiple dies or chiplets are combined in one package to gain performance without relying on further transistor scaling. Advanced packaging has become a key way to extend Moore&\#x27;s Law, and demand has grown sharply with AI, machine learning and 5G applications. ASML is best known for its lithography systems, so a move into bonding equipment would mark an expansion of its equipment portfolio.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Advanced_packaging_%28semiconductors%29">Advanced packaging (semiconductors)</a></li>
<li><a href="https://www.linkedin.com/posts/asmpt-semi-solutions_??-???-????-???-??-??-activity-7460607355387281408-2YHp">What is Hybrid Bonding in Semiconductor Technology | LinkedIn</a></li>

</ul>
</details>

**Tags**: `#ASML`, `#hybrid bonding`, `#semiconductor manufacturing`, `#advanced packaging`, `#lithography`

---

<a id="item-5"></a>
## [Random Neural Networks Self-Assemble Learning Motifs, Match Backprop](https://www.reddit.com/r/MachineLearning/comments/1x6hmyg/how_artificial_neural_networks_build_their_own/) ⭐️ 8.0/10

A PNAS paper published on 9 October 2026, &quot;How Biological Synapses Self-Assemble Gradient Learning,&quot; introduces Self-Assembling Learning \(SAM\), in which randomly interconnected neuron-like units governed by shared local plasticity rules organise themselves into learning motifs, and networks built from those motifs learn pattern recognition and image classification at accuracy similar to the backpropagation-trained networks tested. MIT&\#x27;s McGovern Institute publicised the result on 13 October 2026, framing it as a demonstration that machine-learning networks can acquire learning machinery without a detailed designer blueprint. The result shifts the question from hand-designing a learning circuit to specifying local rules out of which learning machinery can organise itself, which is central to the long-standing debate about whether the brain&\#x27;s local synaptic processes can ever account for global credit assignment. If such self-assembly is robust, it could inform biologically plausible learning theories and energy-efficient hardware that learns through local updates rather than global gradient transport, though the authors present it as a plausibility argument rather than a replacement for backpropagation. According to the paper, SAM self-assembles at two scales: an individual motif emerges from initially random connectivity under heterosynaptic plasticity rules, and hierarchically composed networks of SAMs self-organise into dynamics that provably approximate a generalized form of stochastic gradient descent, matching backpropagation-level performance. The authors explicitly caution that self-organisation does not establish that the brain actually uses this mechanism, and open questions include the stability of the motifs under different initial connectivity and whether the approach extends beyond the demonstrated simple tasks.

reddit · r/MachineLearning · /u/Dorian182 · Oct 15, 10:01

**Background**: Backpropagation, the algorithm behind most modern deep learning, requires a global error signal to be propagated backwards through the whole network, which is widely considered biologically implausible because real synapses only have access to local information. Neuroscience instead describes learning through local plasticity rules such as Hebbian learning, where a synapse changes strength based on the activity of the neurons it connects, though simple Hebbian rules are known to be unstable and are often replaced by variants like BCM theory or Oja&\#x27;s rule. The credit assignment problem — how local changes add up to globally useful learning — has motivated a body of work that meta-learns plasticity rules or searches for interpretable local rules in spiking networks. The self-assembly framing adds the further step of asking how the learning circuitry itself, not just the weights, can emerge from random initial connectivity.

<details><summary>References</summary>
<ul>
<li><a href="https://www.pnas.org/doi/10.1073/pnas.2606245123">How biological synapses self-assemble gradient learning | PNAS</a></li>
<li><a href="https://news.mit.edu/2026/how-artificial-neural-networks-build-their-own-learning-machinery-1013">How artificial neural networks build their own learning machinery</a></li>
<li><a href="https://en.wikipedia.org/wiki/Hebbian_theory">Hebbian theory - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#neuroscience`, `#machine-learning`, `#self-organization`, `#plasticity`, `#backpropagation`

---