---
layout: default
title: "Horizon Summary: 2026-09-22 (EN)"
date: 2026-09-22
lang: en
---

> From 38 items, 5 important content pieces were selected

---

1. [Xiaomi Open-Sources MiMo-V2.6 Pro and Flash MoE Models](#item-1) ⭐️ 8.0/10
2. [NASA&\#x27;s Mars Sample Return Mission Effectively Cancelled](#item-2) ⭐️ 8.0/10
3. [Bryan Cantrill Dissects Sun Microsystems&\#x27; Fatal Mistakes](#item-3) ⭐️ 8.0/10
4. [TypeSafe AI unveils Jev, a &quot;System One&quot; decision model returning typed probabilities](#item-4) ⭐️ 8.0/10
5. [SemiAnalysis Deep-Dive: Mapping MoE Models onto Inference Hardware](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Xiaomi Open-Sources MiMo-V2.6 Pro and Flash MoE Models](https://mimo.xiaomi.com/mimo-v2-6) ⭐️ 8.0/10

On September 22, Xiaomi&\#x27;s MiMo team released and open-sourced the MiMo-V2.6 series, comprising the flagship MiMo-V2.6-Pro \(1.02T total parameters, 42B activated\) and the efficiency-focused MiMo-V2.6-Flash \(309B total, 15B activated\), both native multimodal models targeting coding, computer-use, 3D and audiovisual agent tasks. Alongside the weights, Xiaomi published an unusually detailed tech report, a realtime reinforcement-learning training dashboard, roughly 7,000 diverse environments, a full RL framework, and Qwen models distilled from MiMo training trajectories. The release raises the bar for what &quot;open&quot; means in open-weight AI: rather than shipping weights alone, Xiaomi exposed its reinforcement-learning process in public, making it both a practical tool and a teaching artifact. It also intensifies the debate about Chinese open models&\#x27; cost-performance advantage, since Flash pairs a 309B MoE with a claimed 73.4% SWE-Bench Verified score and fast inference, directly competing with Western frontier and open releases. MiMo-V2.6-Pro features a 1M-token context window, while Flash is ranked first on SWE-Bench Verified at 73.4% and reportedly runs at around 150 tokens/sec. Xiaomi says a Pro-UltraSpeed variant for high-throughput serving is rolling out with up to 20x faster output at equivalent quality, and the training recipe used MixRL to jointly train verifiable code and agent tasks of medium difficulty, with hard-to-verify or ultra-long tasks trained separately and merged via MOPD. MiMo lead Luo Fuli claims it may be one of the largest single RL training runs by compute for an open-model team, and that the engineering challenge exceeded her prior work on DeepSeek R1.

hackernews · volf\_ · Sep 21, 20:12 · [Discussion](https://news.ycombinator.com/item?id=49792730)

**Background**: Mixture-of-Experts \(MoE\) is an architecture in which a model contains many specialized sub-networks \(&quot;experts&quot;\) plus a routing mechanism that activates only a few of them per input, letting a model hold very large total parameter counts while using far fewer parameters — and less compute — for each token. That is why MiMo-V2.6-Pro can have 1.02T total parameters but activate only 42B, and Flash 309B total with 15B activated. Reinforcement learning \(RL\) is the post-training stage where a model is rewarded for better answers and agent behavior; &quot;open weights&quot; means the trained parameters are downloadable, though training data and code are often not released.

<details><summary>References</summary>
<ul>
<li><a href="https://mimo.xiaomi.com/mimo-v2-6">MiMo - V 2 . 6 | Xiaomi</a></li>
<li><a href="https://mimo.mi.com/docs/en-US/news/latest/v2-6">Xiaomi MiMo Home</a></li>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters were broadly impressed by the transparency rather than the benchmark numbers: one praised the realtime RL training dashboard as an &quot;incredible learning and teaching tool,&quot; while another said Chinese models now excite them more than American ones mainly because of affordability. Others focused on concrete specs \(Flash 309B/15B, Pro 1.02T/42B\) and lighter observations, such as a running joke that these models love the &quot;01 - UPPERCASE TEXT&quot; frontend design motif.

**Tags**: `#LLM`, `#open-source-models`, `#Mixture-of-Experts`, `#model-release`, `#AI-research`

---

<a id="item-2"></a>
## [NASA&\#x27;s Mars Sample Return Mission Effectively Cancelled](https://www.science.org/content/article/nasa-s-mars-sample-return-mission-dead) ⭐️ 8.0/10

NASA&\#x27;s Mars Sample Return \(MSR\) campaign — the joint NASA-ESA effort to retrieve samples cached by the Perseverance rover — has been effectively cancelled, with NASA concluding that the existing architecture had ballooned into a roughly $8–11 billion program that might not deliver samples to Earth until around 2040. The decision ends a flagship-class plan that was formally approved in 2022 and originally envisioned returning Martian material around 2033. Mars Sample Return was widely regarded as the highest-priority planetary science goal for the coming decade, and its cancellation reshapes the future of robotic planetary exploration and the institutional role of NASA&\#x27;s Jet Propulsion Laboratory, which led the mission. It also cedes potential first-mover advantage in Mars sample return to China&\#x27;s Tianwen-3, planned for the 2028–2029 launch window, at a time when NASA&\#x27;s own science budget is under pressure. The original plan involved three elements — Perseverance as the sample-collection rover, a Sample Retrieval Lander with a Mars Ascent Vehicle, and an Earth Return Orbiter — and critics argued JPL designed it around legacy launch vehicles such as Ariane 64 rather than leveraging lower-cost, higher-capacity commercial rockets like Starship or New Glenn that could have reduced cost and complexity. For scale, the Apollo missions returned 842 pounds \(about 382 kg\) of lunar rock, whereas MSR was intended to bring back only about 1.1 pounds \(roughly 0.5 kg\) of Martian material.

hackernews · Muhammad523 · Sep 21, 19:14 · [Discussion](https://news.ycombinator.com/item?id=49791939)

**Background**: Mars Sample Return is a proposed class of mission that would collect rock, soil and atmospheric samples on Mars and bring them to Earth, where laboratories can analyze them far more thoroughly than any onboard instrument — particularly to test whether Mars once hosted life. NASA and ESA jointly approved their MSR campaign in 2022, building on samples already sealed in tubes by the Perseverance rover, with the Jet Propulsion Laboratory \(a federally funded NASA center managed by Caltech\) as the lead implementer. Concerns about possible back-contamination of Earth&\#x27;s biosphere from returned Martian material are generally considered low-risk. Competing efforts include China&\#x27;s Tianwen-3 dual-launch mission, Roscosmos&\#x27;s Mars-Grunt, and JAXA&\#x27;s MMX mission to return samples from the Martian moon Phobos.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mars_sample-return_mission">Mars sample-return mission</a></li>
<li><a href="https://en.wikipedia.org/wiki/NASA-ESA_Mars_Sample_Return">NASA-ESA Mars Sample Return - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Jet_Propulsion_Laboratory">Jet Propulsion Laboratory - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters largely saw the cancellation as financially unavoidable, with one calling the mission &quot;financially unfeasible&quot; and another arguing NASA killed an $11B/2040 architecture that JPL leadership had inflated and tied to legacy rockets instead of Starship or New Glenn. Several pointed to parallel international efforts, notably China&\#x27;s Tianwen-3 \(launching 2028\) and the repeatedly delayed ExoMars Rosalind Franklin rover, now targeted for 2028 after its Russian launch was dropped. Others noted the modest scientific payload relative to Apollo&\#x27;s 842 pounds of lunar samples, and one dismissed the coverage as self-pity from institutions that benefited from the old NASA funding model.

**Tags**: `#NASA`, `#Mars Sample Return`, `#space exploration`, `#JPL`, `#science policy`

---

<a id="item-3"></a>
## [Bryan Cantrill Dissects Sun Microsystems&\#x27; Fatal Mistakes](https://bcantrill.dtrace.org/2026/09/20/what-sun-got-wrong/) ⭐️ 8.0/10

Bryan Cantrill, the creator of DTrace and co-founder of Oxide Computer, published an essay titled &quot;What Sun got wrong&quot; on his dtrace.org blog on September 20, 2026, dissecting the strategic and technical missteps that doomed Sun Microsystems. The post sparked a large Hacker News thread \(494 points, 283 comments\) in which former employees and customers traded firsthand anecdotes about Sun&\#x27;s decline. Sun was once the dominant vendor of Unix workstations and servers and the birthplace of Java, NFS, ZFS and DTrace, so its collapse into the 2010 Oracle acquisition is a widely cited cautionary tale about how a company with a commanding technical lead can lose the market. The discussion also preserves institutional memory that rarely makes it into official histories, since roughly 235,000 people can count themselves former Sun employees. Commenters point to concrete decisions such as Sun&\#x27;s brief 2002 cancellation of Solaris on x86, which pushed customers toward alternatives, and the failed 2002 deal with Google, which reportedly collapsed because Sun insisted on knowing how many servers Google operated. Others note the stark contrast between Sun&\#x27;s laborious quote-and-meeting sales process and Dell&\#x27;s next-day, shipped-to-your-door model.

hackernews · chmaynard · Sep 21, 14:03 · [Discussion](https://news.ycombinator.com/item?id=49787436)

**Background**: Sun Microsystems was founded in 1982 by Andreas Bechtolsheim, Bill Joy, Vinod Khosla and Scott McNealy to sell low-cost, high-performance Unix workstations, went public in 1986, and grew into a leading vendor of servers built around its SPARC processors and its Solaris operating system. Solaris superseded SunOS in 1993 and was known for scalability and innovations such as DTrace, ZFS and containers; Sun open-sourced most of it as OpenSolaris in 2005. After Oracle acquired Sun in 2010, Solaris was renamed Oracle Solaris, OpenSolaris was discontinued and forked into Illumos.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Sun_Microsystems">Sun Microsystems - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Solaris_operating_system">Solaris operating system</a></li>
<li><a href="https://spectrum.ieee.org/after-the-sun-microsystems-sets-the-real-stories-come-out">After the Sun (Microsystems) Sets, the Real Stories Come Out - IEEE Spectrum</a></li>

</ul>
</details>

**Discussion**: Overall sentiment is a mix of technical admiration and frustration with Sun&\#x27;s business culture: one buyer recalls that Alpha server rails and power cords alone cost more than a complete Dell server delivered the next day, while another lists the 2002 Solaris-on-x86 cancellation and the aborted Google deal as self-inflicted wounds. Others share nostalgic memories of fast, terminal-centric Sun thin clients at university, and one commenter argues Sun was never really interested in running a business at all, only in building great technology and tolerating sales to fund it.

**Tags**: `#sun-microsystems`, `#industry-history`, `#bryan-cantrill`, `#solaris`, `#business-strategy`

---

<a id="item-4"></a>
## [TypeSafe AI unveils Jev, a &quot;System One&quot; decision model returning typed probabilities](https://simonwillison.net/2026/Sep/21/jev/) ⭐️ 8.0/10

TypeSafe AI released Jev, its first &quot;System One model,&quot; which accepts unstructured text input as a &quot;state&quot; object and, instead of generating text, returns typed probabilistic outputs such as yes/no confidence scores, probability distributions over supplied options, and floating-point ratings. It is priced at $0.042 per million input tokens with output charged as free, making it cheaper than OpenAI&\#x27;s GPT-5 Nano \($0.05/million\). Jev suggests a new model category tuned for direct consumption by software rather than conversation, which could make AI-driven classification tasks like spam detection, labeling, prioritization, and search reranking dramatically cheaper and faster to deploy. At the same time, it pushes AI further toward opaque black-box behavior, since a system flagged as spam returns only a number and no explanation of which content signals drove the decision. Jev accepts a state containing a string, an array of strings, or a set of name-value pairs, and can evaluate as many questions as fit in the context window, with all questions processed in parallel so many queries take roughly the same time as one. The three question types are &quot;Noul&quot; yes/no questions \(a Bernoulli probability between 0 and 1\), choice questions returning a distribution over options, and score questions returning a value along a numeric range; the model is built on a new architecture, a parallel sampler, and a training method TypeSafe calls Reinforcement Learning for Calibrated Decisions \(RLCD\).

rss · Simon Willison · Sep 21, 23:09

**Background**: Traditional LLMs are text-in, text-out systems built for people to read, whereas System One models are designed to output decisions that other software can consume directly, echoing the &quot;System 1&quot; fast, intuitive mode of thinking described by Daniel Kahneman. The name TypeSafe AI borrows from type safety in programming languages, where values are constrained to a declared type so errors are caught early; Jev&\#x27;s outputs are similarly constrained to floats and categories rather than free-form prose. Simon Willison notes that he prefers the term &quot;decision models,&quot; a naming suggestion from Maggie Appleton, because it better describes what these models do.

<details><summary>References</summary>
<ul>
<li><a href="https://typesafe.ai/blog/introducing-system-one-models-and-jev">Introducing System One Models &amp; Jev - TypeSafe AI Blog</a></li>
<li><a href="https://en.wikipedia.org/wiki/Jev_%28AI_model%29">Jev (AI model) - Wikipedia</a></li>
<li><a href="https://docs.typesafe.ai/concepts/system-one">System One - TypeSafe AI</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#decision-models`, `#TypeSafe-AI`, `#Jev`, `#probabilistic-models`

---

<a id="item-5"></a>
## [SemiAnalysis Deep-Dive: Mapping MoE Models onto Inference Hardware](https://newsletter.semianalysis.com/p/computation-and-data-movement-for) ⭐️ 8.0/10

SemiAnalysis published a technical deep-dive titled &quot;Computation and Data Movement for Inference&quot; that analyzes how Mixture-of-Experts \(MoE\) models are mapped onto inference hardware, covering model structure, data flow, and efficient serving strategies. The piece focuses on the twin bottlenecks of compute and data movement that dominate MoE inference performance. MoE has become the dominant architecture for frontier open-weight models because it decouples total parameter count from per-token compute, but that same sparsity makes inference memory-bound and hard to serve efficiently. As more labs ship large MoE models, understanding how experts, routing, and weight movement interact with accelerators and interconnect directly determines serving cost, latency, and throughput for anyone deploying them. The analysis stresses that MoE inference shifts the bottleneck from raw FLOPs toward data movement: only a small subset of experts is activated per token, so weights must be gathered and exchanged across memory hierarchies and often across devices, making memory bandwidth, cache behavior, and inter-GPU communication the limiting factors. It also frames the trade-offs in serving strategies such as expert parallelism and batching, where larger batches improve efficiency but complicate routing and load balance across experts.

rss · Semianalysis · Sep 21, 18:14

**Background**: Mixture-of-Experts is a machine learning approach that divides a model into multiple &quot;expert&quot; sub-networks, each specializing in a subset of the input, with a routing mechanism deciding which experts handle each token. Because only a few experts fire per token, MoE models can be pretrained with far less compute than a dense model of comparable total size, letting researchers scale parameters or data within the same compute budget. The catch is inference: a model with, say, 132B total parameters but only a fraction active per token still has to hold and move all of its weights, making data movement — not arithmetic — the practical constraint, a problem long studied in ML systems research.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained</a></li>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://www.ibm.com/think/topics/mixture-of-experts">What is mixture of experts? | IBM</a></li>

</ul>
</details>

**Tags**: `#MoE`, `#inference`, `#hardware`, `#data movement`, `#ML systems`

---