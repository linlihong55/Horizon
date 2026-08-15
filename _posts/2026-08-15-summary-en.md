---
layout: default
title: "Horizon Summary: 2026-08-15 (EN)"
date: 2026-08-15
lang: en
---

> From 23 items, 4 important content pieces were selected

---

1. [BDH-CQ: Recurrent Latent Reasoning Hits Low-Cost ARC-AGI-1 Breakthrough](#item-1) ⭐️ 9.0/10
2. [AI&\#x27;s Math Edge: Bigger Working Memory, Not Better Reasoning](#item-2) ⭐️ 8.0/10
3. [Developer Achieves 232x Kernel Speedup Using OpenAI Codex](#item-3) ⭐️ 8.0/10
4. [Jacobian Lens Fitted to Qwen3.6 Transfers to Qwen3.8 Without Refitting](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [BDH-CQ: Recurrent Latent Reasoning Hits Low-Cost ARC-AGI-1 Breakthrough](https://www.reddit.com/r/MachineLearning/comments/1vov5r5/bdhcq_incontext_learning_with_recurrent_latent/) ⭐️ 9.0/10

The paper introduces BDH-CQ, a reasoning system that merges in-context learning with recurrent latent reasoning. A 150M-parameter configuration reaches 29.5% pass@2 on ARC-AGI-1 at an estimated $0.00070 per task, surpassing the previous cost–accuracy Pareto frontier. This result suggests that compact models can achieve strong abstract reasoning by iterating in a latent workspace rather than generating long chains of thought. It could lower inference costs and influence future in-context learning and test-time compute architectures. Demonstrations at inference time continuously update the model&\#x27;s recurrent memory, and queries are solved through iterative computation in a high-dimensional latent space without verbalizing intermediate states. Neither task identifiers nor evaluation-task demonstration pairs are used in training, and no parameters are updated at inference time.

reddit · r/MachineLearning · /u/moschles · Aug 15, 06:18

**Background**: ARC-AGI-1 is a benchmark designed to measure abstract reasoning capability in AI systems, often requiring generalization to unfamiliar tasks. Mainstream reasoning models typically scale test-time compute by producing more tokens, while latent-reasoning approaches like BDH-CQ iterate a recurrent block internally to &\#x27;think&\#x27; without explicit chain-of-thought. BDH-CQ builds on a post-Transformer recurrent architecture and keeps memory, adaptation, and inference in the same computational fabric.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2608.09888">[2608.09888] BDH-CQ: In-Context Learning with Recurrent Latent Reasoning</a></li>
<li><a href="https://arxiv.org/pdf/2608.09888">BDH-CQ: IN-CONTEXT LEARNING WITH RECURRENT LATENT REASONING</a></li>
<li><a href="https://arcprize.org/arc-agi/1">ARC - AGI - 1</a></li>

</ul>
</details>

**Tags**: `#in-context learning`, `#recurrent reasoning`, `#ARC-AGI`, `#latent reasoning`, `#efficient AI`

---

<a id="item-2"></a>
## [AI&\#x27;s Math Edge: Bigger Working Memory, Not Better Reasoning](https://davidepiffer.com/p/ai-isnt-outthinking-mathematicians) ⭐️ 8.0/10

A new essay argues that AI&\#x27;s edge in mathematics comes from access to vastly larger working memory and tireless brute-force exploration, not from superior reasoning. The piece has sparked a rich discussion among 313 commenters about what this means for AI cognition and mathematical research. This distinction matters because it reframes debates about whether AI truly &\#x27;thinks&\#x27; or &\#x27;reasons&\#x27; like humans, separating raw computational advantages from human-like insight. It could shape how researchers interpret AI results in mathematics, how they design evaluation benchmarks, and what kind of AI-assisted math tools are prioritized. The essay draws on the concept of the context window as an LLM&\#x27;s working memory, while community members point to projects such as theoremdb.org that archive negative results for AI reuse. Commenters also note that AI never tires or gets discouraged, so it can pursue research directions a human mathematician would abandon after a week.

hackernews · rzk · Aug 15, 18:13 · [Discussion](https://news.ycombinator.com/item?id=49312845)

**Background**: In human cognition, working memory refers to the small amount of information one can actively hold and manipulate at once, often estimated at only a few items. For transformer-based large language models, the context window acts as a kind of working memory: the maximum number of tokens the model can process in a single inference pass. Brute-force search, a classic computer science technique, systematically exhausts all possibilities and has been used to prove mathematical theorems and solve hard combinatorial problems. The essay builds on these ideas to argue that AI&\#x27;s mathematical progress may come more from scaling memory and tireless search than from human-like reasoning.

<details><summary>References</summary>
<ul>
<li><a href="https://towardsdatascience.com/de-coded-understanding-context-windows-for-transformer-models-cd1baca6427e/">De-Coded: Understanding Context Windows for Transformer ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Brute-force_search">Brute-force search - Wikipedia</a></li>
<li><a href="https://cacm.acm.org/research/the-science-of-brute-force/">The Science of Brute Force – Communications of the ACM</a></li>

</ul>
</details>

**Discussion**: The discussion is largely supportive of the essay&\#x27;s nuance, adding that &\#x27;intelligence&\#x27; often looks like out-remembering others and that human mathematicians rarely publish negative results while AI can reuse them. Some commenters cite Michael Nielsen&\#x27;s &\#x27;Augmenting Long-Term Memory&\#x27; and emphasize AI&\#x27;s tireless brute-force persistence as a key factor. Overall, the thread enriches the essay by connecting it to concrete projects and personal research experience rather than merely defending or attacking AI.

**Tags**: `#AI`, `#mathematics`, `#working memory`, `#cognition`, `#research`

---

<a id="item-3"></a>
## [Developer Achieves 232x Kernel Speedup Using OpenAI Codex](https://sankalp.bearblog.dev/autoresearch/) ⭐️ 8.0/10

A developer used OpenAI&\#x27;s Codex agent to autonomously research and optimize a GPU kernel, achieving a 232x speedup. The result was shared in a blog post that has gained traction on Hacker News. This demonstrates the potential of LLM agents to autonomously perform complex performance engineering, which could accelerate optimization work across industries. However, community discussion cautions that such AI-driven solutions may overfit to specific inputs and require expert oversight. The 232x speedup was achieved through an autonomous research loop likely involving profiling, iteration, and kernel rewriting by Codex. Discussion notes that in a related competition, 8 of 10 top AI-optimized solutions failed on out-of-distribution inputs, underlining robustness concerns.

hackernews · tosh · Aug 15, 11:00 · [Discussion](https://news.ycombinator.com/item?id=49309549)

**Background**: OpenAI Codex is an AI coding agent released in April 2025, available via CLI, desktop, and IDE integrations. LLM agents use a large language model as a central engine to reason, plan, and execute tasks. GPU kernel optimization often involves techniques like profiling and handwritten PTX to approach theoretical performance limits.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenAI_Codex_%28AI_agent%29">OpenAI Codex (AI agent) - Wikipedia</a></li>
<li><a href="https://openai.com/codex/">Codex in ChatGPT | AI Coding Agents for Software Engineering | OpenAI</a></li>
<li><a href="https://developer.nvidia.com/blog/advanced-nvidia-cuda-kernel-optimization-techniques-handwritten-ptx/">Advanced NVIDIA CUDA Kernel Optimization Techniques: Handwritten PTX | NVIDIA Technical Blog</a></li>

</ul>
</details>

**Discussion**: Commenters shared mixed experiences: one praised the novelty of non-AI-generated writing, while another tested DeepSeek v4 on a video codec and noted the verifier helped. A key concern was that AI-optimized solutions often overfit to benchmark inputs, with expert adjustments remaining necessary.

**Tags**: `#AI-assisted development`, `#GPU kernels`, `#performance optimization`, `#Codex`, `#LLM agents`

---

<a id="item-4"></a>
## [Jacobian Lens Fitted to Qwen3.6 Transfers to Qwen3.8 Without Refitting](https://www.reddit.com/r/MachineLearning/comments/1vpa5cv/survival_of_the_fitted_qwen3627bs_jacobian_lens/) ⭐️ 8.0/10

A Reddit user tested whether the Jacobian lens published for Qwen3.6-27B remains effective when applied unchanged to the newer Qwen3.8-27B. The transferred lens kept latent entities near the top of the vocabulary on two-hop prompts, and steering directions derived from the old checkpoint suppressed &\#x27;paradox&\#x27; in generated text on the new model. This is the first empirical investigation into whether interpretability lenses survive model version updates, an open question for the practicality of mechanistic interpretability. If lenses transfer across checkpoints, monitoring pipelines can validate their instruments instead of assuming a refit is required for every release. Both models share 64 layers, hidden dimension, and tokenizer, but their training relationship is undocumented. The transferred lens showed median rank 4 \(home\) vs 17 \(transferred\) at layer 48, while the successor did better at layer 24 \(121 vs 38\); WikiText transfer costs were 1.2–1.3x mid-network and ~2x by layer 48.

reddit · r/MachineLearning · /u/imstilllearningthis · Aug 15, 18:24

**Background**: The Jacobian lens \(J-lens\) is a technique introduced in Anthropic&\#x27;s paper &\#x27;Verbalizable Representations Form a Global Workspace in Language Models&\#x27; that reads out what an internal activation is disposed to make the model say. The logit lens, an earlier interpretability method, examines pre-softmax activations to track how predictions converge across layers. Neuronpedia is an open-source platform that publishes and hosts such lenses for models like Qwen.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/anthropics/jacobian-lens">GitHub - anthropics/jacobian-lens: Companion code for the global workspace interpretability paper · GitHub</a></li>
<li><a href="https://transformer-circuits.pub/2026/workspace/index.html">Verbalizable Representations Form a Global Workspace in Language Models</a></li>
<li><a href="https://www.lesswrong.com/posts/AcKRB8wDpdaN6v6ru/interpreting-gpt-the-logit-lens">interpreting GPT: the logit lens</a></li>

</ul>
</details>

**Tags**: `#interpretability`, `#mechanistic interpretability`, `#Jacobian lens`, `#language models`, `#Qwen`

---