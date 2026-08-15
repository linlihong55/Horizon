---
layout: default
title: "Horizon Summary: 2026-08-15 (ZH)"
date: 2026-08-15
lang: zh
---

> 从 23 条内容中筛选出 4 条重要资讯。

---

1. [BDH-CQ：以循环潜在推理实现低成本 ARC-AGI-1 突破](#item-1) ⭐️ 9.0/10
2. [AI 数学优势来自更大工作记忆而非更强的推理](#item-2) ⭐️ 8.0/10
3. [开发者利用 OpenAI Codex 实现内核 232 倍加速](#item-3) ⭐️ 8.0/10
4. [无需重新拟合：Qwen3.6 的 Jacobian 透镜可迁移至 Qwen3.8](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [BDH-CQ：以循环潜在推理实现低成本 ARC-AGI-1 突破](https://www.reddit.com/r/MachineLearning/comments/1vov5r5/bdhcq_incontext_learning_with_recurrent_latent/) ⭐️ 9.0/10

论文提出了 BDH-CQ，一个将上下文学习与循环潜在推理相结合的新型推理系统。其 150M 参数配置在 ARC-AGI-1 上达到 29.5%的 pass@2，每个任务的估算成本仅为 0.00070 美元，突破了此前的成本-准确率帕累托前沿。 这一结果表明，紧凑型模型可以通过在潜在工作区中迭代来获得强大的抽象推理能力，而无需生成长思维链。这可能降低推理成本，并影响未来的上下文学习与测试时计算架构。 推理时，演示样本会持续更新模型的循环记忆，查询则通过高维潜在空间中的迭代计算来求解，且不会将中间推理状态翻译成语言。训练中不使用任务标识符或评估任务的演示对，推理时也不更新任何参数。

reddit · r/MachineLearning · /u/moschles · 8月15日 06:18

**背景**: ARC-AGI-1 是一个旨在衡量 AI 系统抽象推理能力的基准测试，通常要求模型对不熟悉的任务进行泛化。主流推理模型通常通过生成更多令牌来扩展测试时计算，而 BDH-CQ 等潜在推理方法则在内部迭代一个循环模块来“思考”，无需显式的思维链。BDH-CQ 基于一种后 Transformer 循环架构，将记忆、适应与推理置于同一计算框架之中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2608.09888">[2608.09888] BDH-CQ: In-Context Learning with Recurrent Latent Reasoning</a></li>
<li><a href="https://arxiv.org/pdf/2608.09888">BDH-CQ: IN-CONTEXT LEARNING WITH RECURRENT LATENT REASONING</a></li>
<li><a href="https://arcprize.org/arc-agi/1">ARC - AGI - 1</a></li>

</ul>
</details>

**标签**: `#in-context learning`, `#recurrent reasoning`, `#ARC-AGI`, `#latent reasoning`, `#efficient AI`

---

<a id="item-2"></a>
## [AI 数学优势来自更大工作记忆而非更强的推理](https://davidepiffer.com/p/ai-isnt-outthinking-mathematicians) ⭐️ 8.0/10

一篇新文章提出，AI 在数学上的优势来自它拥有比人脑大得多的工作记忆，以及不知疲倦的暴力搜索，而不是更优越的推理能力。这篇文章引发了 313 位评论者的热烈讨论，话题涉及 AI 认知的本质及其对数学研究的意义。 这种区分很重要，因为它把“原始计算优势”和“类人洞察力”分开，重新定义了 AI 是否真的像人类一样“思考”或“推理”的争论。它可能影响研究人员如何解读 AI 在数学中的成果、如何设计评估基准，以及优先开发哪类 AI 辅助数学工具。 该文章借用了“上下文窗口相当于大语言模型工作记忆”的概念；社区成员则提到 theoremdb.org 等项目，它们将研究中的负结果（失败路径）存档供 AI 复用。评论者还指出，AI 永不疲倦、不会气馁，因此可以持续探索人类数学家可能一周后就放弃的研究方向。

hackernews · rzk · 8月15日 18:13 · [社区讨论](https://news.ycombinator.com/item?id=49312845)

**背景**: 在人脑认知中，工作记忆指我们在一瞬间能主动保存和操作的少量信息，通常只能记住几个项目。对于基于 Transformer 的大语言模型来说，“上下文窗口”就相当于一种工作记忆：它决定了模型单次推理能同时处理的 token 数量上限。暴力搜索是计算机科学中的经典技术，通过系统地穷举所有可能来求解问题，已被用于证明数学定理和解决困难组合问题。这篇评论正是基于这些概念，认为 AI 在数学上的进展更多来自记忆规模与不知疲倦的搜索，而不是类人推理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://towardsdatascience.com/de-coded-understanding-context-windows-for-transformer-models-cd1baca6427e/">De-Coded: Understanding Context Windows for Transformer ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Brute-force_search">Brute-force search - Wikipedia</a></li>
<li><a href="https://cacm.acm.org/research/the-science-of-brute-force/">The Science of Brute Force – Communications of the ACM</a></li>

</ul>
</details>

**社区讨论**: 讨论在很大程度上赞同文章的细致分析，并补充说“聪明”往往表现为比别人记得更多，而人类数学家很少发表负结果，AI 却可以复用它。一些评论者引用 Michael Nielsen 的《Augmenting Long-Term Memory》，并强调 AI 不知疲倦的暴力搜索是其关键因素。总体而言，评论不是简单地支持或攻击 AI，而是将其与具体项目和亲身研究经历联系起来，进一步丰富了文章。

**标签**: `#AI`, `#mathematics`, `#working memory`, `#cognition`, `#research`

---

<a id="item-3"></a>
## [开发者利用 OpenAI Codex 实现内核 232 倍加速](https://sankalp.bearblog.dev/autoresearch/) ⭐️ 8.0/10

一位开发者使用 OpenAI 的 Codex 智能体自主研究和优化 GPU 内核，实现了 232 倍的加速。这一成果发布在博客上，并在 Hacker News 上引发热议。 这表明 LLM 智能体在自主执行复杂性能工程方面具有潜力，可能加速各行业的优化工作。但社区讨论也提醒，这类 AI 驱动的解决方案可能过拟合特定输入，需要专家监督。 232 倍的加速是通过 Codex 自主研究循环实现的，可能涉及性能分析、迭代和内核重写。讨论指出，在相关比赛中，10 个 AI 优化顶级方案中有 8 个在分布外输入上失效，凸显了鲁棒性问题。

hackernews · tosh · 8月15日 11:00 · [社区讨论](https://news.ycombinator.com/item?id=49309549)

**背景**: OpenAI Codex 是 OpenAI 于 2025 年 4 月发布的 AI 编程智能体，可通过 CLI、桌面应用和 IDE 集成使用。LLM 智能体以大语言模型为核心引擎进行推理、规划和执行任务。GPU 内核优化通常涉及性能分析和手写 PTX 等技术，以接近理论性能极限。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenAI_Codex_%28AI_agent%29">OpenAI Codex (AI agent) - Wikipedia</a></li>
<li><a href="https://openai.com/codex/">Codex in ChatGPT | AI Coding Agents for Software Engineering | OpenAI</a></li>
<li><a href="https://developer.nvidia.com/blog/advanced-nvidia-cuda-kernel-optimization-techniques-handwritten-ptx/">Advanced NVIDIA CUDA Kernel Optimization Techniques: Handwritten PTX | NVIDIA Technical Blog</a></li>

</ul>
</details>

**社区讨论**: 评论者分享了不同体验：有人称赞非 AI 生成的文字更有新鲜感，也有人用 DeepSeek v4 测试视频编解码器并指出验证器有助于保证正确性。一个核心担忧是 AI 优化方案常过拟合基准输入，仍需专家进行调整。

**标签**: `#AI-assisted development`, `#GPU kernels`, `#performance optimization`, `#Codex`, `#LLM agents`

---

<a id="item-4"></a>
## [无需重新拟合：Qwen3.6 的 Jacobian 透镜可迁移至 Qwen3.8](https://www.reddit.com/r/MachineLearning/comments/1vpa5cv/survival_of_the_fitted_qwen3627bs_jacobian_lens/) ⭐️ 8.0/10

一位 Reddit 用户测试了为 Qwen3.6-27B 发布的 Jacobian lens 在未经修改地应用于新版 Qwen3.8-27B 时是否仍然有效。结果表明，迁移后的透镜在二跳提示上仍能将潜在实体保持在词表前列，并且从旧检查点导出的转向方向在新模型上成功抑制了生成文本中的“悖论”一词。 这是首次实证研究解释性透镜能否在模型版本更新后继续有效，而这一问题此前一直悬而未决，直接影响机械可解释性的实用价值。如果透镜可以跨检查点迁移，监控管线就可以验证其工具而不必假设每个版本都必须重新拟合。 两个模型共享 64 层、隐藏维度和分词器，但训练关系未公开。迁移透镜在第 48 层的中位排名为 4（原模型）对 17（迁移后），而第 24 层时新模型表现反而更好（121 对 38）；在 WikiText 上的迁移成本为网络中部 1.2–1.3 倍、第 48 层约 2 倍。

reddit · r/MachineLearning · /u/imstilllearningthis · 8月15日 18:24

**背景**: Jacobian lens（J-lens）是 Anthropic 论文《Verbalizable Representations Form a Global Workspace in Language Models》中引入的一种技术，用于解读内部激活状态倾向于让模型说出什么。Logit lens 是一种更早的解释性方法，通过检查 softmax 前的激活来追踪预测在各层之间的收敛过程。Neuronpedia 是一个开源平台，公开发布并托管诸如 Qwen 等模型的此类透镜。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/anthropics/jacobian-lens">GitHub - anthropics/jacobian-lens: Companion code for the global workspace interpretability paper · GitHub</a></li>
<li><a href="https://transformer-circuits.pub/2026/workspace/index.html">Verbalizable Representations Form a Global Workspace in Language Models</a></li>
<li><a href="https://www.lesswrong.com/posts/AcKRB8wDpdaN6v6ru/interpreting-gpt-the-logit-lens">interpreting GPT: the logit lens</a></li>

</ul>
</details>

**标签**: `#interpretability`, `#mechanistic interpretability`, `#Jacobian lens`, `#language models`, `#Qwen`

---