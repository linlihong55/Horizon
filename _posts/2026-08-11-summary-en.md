---
layout: default
title: "Horizon Summary: 2026-08-11 (EN)"
date: 2026-08-11
lang: en
---

> From 37 items, 9 important content pieces were selected

---

1. [Meta introduces Muse Glimmer, an open 30B agentic model](#item-1) ⭐️ 9.0/10
2. [Nvidia Unveils Nemotron 3.5 Lightning and NeMo Switchyard](#item-2) ⭐️ 8.0/10
3. [Compression Is Prediction: An Exploration of Information Theory and ML](#item-3) ⭐️ 8.0/10
4. [Mojo 1.0 Launches, Aiming to Combine Python Usability with C-Level Speed](#item-4) ⭐️ 8.0/10
5. [Researchers Steal Hidden Reasoning Traces from Proprietary LLM APIs](#item-5) ⭐️ 8.0/10
6. [Stratechery Analyzes Risks to Nvidia&\#x27;s AI Infrastructure Dominance](#item-6) ⭐️ 8.0/10
7. [London Underground Trials Live Facial Recognition During Policing Expansion](#item-7) ⭐️ 8.0/10
8. [Decoupled Descent: New Training Method Tracks Train-Test Error via AMP Onsager Corrections](#item-8) ⭐️ 8.0/10
9. [HyperSAE: Poincaré Geometry for Sparse Autoencoders Reduces MSE by 9.8%](#item-9) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Meta introduces Muse Glimmer, an open 30B agentic model](https://simonwillison.net/2026/Aug/10/introducing-muse-glimmer/#atom-everything) ⭐️ 9.0/10

Meta released Muse Glimmer, a 30-billion-parameter open-weights model under the Apache 2.0 license, optimized for end-to-end agentic tasks, reliable tool use, and multi-step reasoning. It is designed to run locally on a single consumer GPU, and Simon Willison quickly tested it via LM Studio. This is significant because Meta shifted to a permissive Apache 2.0 license, a departure from the more restrictive Llama licenses, and targeted exactly the local-agent, tool-use niche that many developers and researchers care about. It could accelerate on-device agentic AI and provide a strong open alternative to larger closed models. The model is multimodal \(vision-capable\), and Meta highlights its performance on full-task benchmarks including DeepSearch QA, MCP-Atlas, τ-Bench, and SWE-Bench. Simon Willison ran an 18.16 GB quantized version in LM Studio and also tested it with his llm-coding-agent plugin against a Datasette checkout.

rss · Simon Willison · Aug 10, 23:56

**Background**: Open-weights models let developers download and run the model locally, avoiding cloud API costs and privacy concerns. Apache 2.0 is a permissive license that allows broad commercial and research use with few restrictions, unlike Meta&\#x27;s earlier Llama licenses. Agentic tasks require a model to autonomously use external tools, follow multi-step plans, and recover from errors; benchmarks like MCP-Atlas \(based on the Model Context Protocol\) and τ-Bench evaluate these abilities. Muse Glimmer is part of a broader trend toward capable local models optimized for agent workflows.

<details><summary>References</summary>
<ul>
<li><a href="https://research.meta.ai/blog/introducing-muse-glimmer-open-agentic-model">Introducing Muse Glimmer: An Open Agentic Model That Runs on Your Device | Meta AI Research</a></li>
<li><a href="https://huggingface.co/meta-models/Muse-Glimmer-30B">meta-models/Muse-Glimmer-30B · Hugging Face</a></li>
<li><a href="https://github.com/scaleapi/mcp-atlas">GitHub - scaleapi/mcp-atlas: MCP Atlas</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Meta`, `#open-weights`, `#agentic`, `#LLM`

---

<a id="item-2"></a>
## [Nvidia Unveils Nemotron 3.5 Lightning and NeMo Switchyard](https://blogs.nvidia.com/blog/nemotron-lightning-switchyard-rtx-dgx/) ⭐️ 8.0/10

NVIDIA announced Nemotron 3.5 Lightning, an open 30B-parameter Mixture-of-Experts small language model with 3B active parameters optimized for agentic workloads. It also released NeMo Switchyard, an open-source Rust proxy and library for intelligently routing requests across LLMs. This release signals growing industry momentum toward smaller, efficient models that can deliver strong task-specific accuracy at lower cost and latency. Switchyard could also become a standard building block for agentic AI systems that need to balance capability, cost, and latency across multiple models. The model delivers up to 4x faster output speed and 30% faster agentic task completion, and was released alongside speculative decoding methods; an NVFP4 version is available on Hugging Face for commercial use. Switchyard is a Rust proxy and library that supports tuning-free and tunable routers to route agent workflows across models.

hackernews · droidjj · Aug 11, 19:35 · [Discussion](https://news.ycombinator.com/item?id=49263340)

**Background**: Small language models \(SLMs\) are compact LLMs that trade some raw capability for lower compute cost and faster inference, often using Mixture-of-Experts designs that activate only a subset of parameters per token. Model routing is an emerging pattern where a dispatcher sends each request to the most suitable model based on task, cost, or latency targets. NeMo Switchyard is part of the NVIDIA NeMo ecosystem, and Nemotron 3.5 Lightning can be post-trained on proprietary data with NeMo to improve domain-specific accuracy.

<details><summary>References</summary>
<ul>
<li><a href="https://blogs.nvidia.com/blog/nemotron-lightning-switchyard-rtx-dgx/">NVIDIA Nemotron 3.5 Lightning and NeMo Switchyard Deliver Faster, Smarter, More Efficient Agentic AI | NVIDIA Blog</a></li>
<li><a href="https://developer.nvidia.com/blog/nvidia-nemotron-3-5-lightning-delivers-fast-accurate-specialized-task-execution-for-long-running-agents/">NVIDIA Nemotron 3.5 Lightning Delivers Fast, Accurate Specialized Task Execution for Long-Running Agents | NVIDIA Technical Blog</a></li>
<li><a href="https://developer.nvidia.com/blog/route-ai-agent-workloads-across-models-with-nvidia-nemo-switchyard/">Route AI Agents Across Models with NVIDIA NeMo Switchyard | NVIDIA Technical Blog</a></li>

</ul>
</details>

**Discussion**: Commenters were generally positive, especially about the trend toward small, efficient models and the fact that a Nemotron model runs well on Apple Silicon via MLX. However, one person raised concerns about how routers handle prompt caching for multi-turn sessions, and another criticized the benchmarks for omitting most Qwen models, suggesting a lack of fairness.

**Tags**: `#NVIDIA`, `#LLM`, `#model routing`, `#AI`, `#open source`

---

<a id="item-3"></a>
## [Compression Is Prediction: An Exploration of Information Theory and ML](https://ngrok.com/blog/compression-is-prediction) ⭐️ 8.0/10

The ngrok blog published an article, &\#x27;Compression is prediction,&\#x27; exploring the theoretical equivalence between data compression and prediction, drawing on information theory and machine learning. The post frames compression not just as a storage technique but as a fundamental principle underlying intelligent prediction. This discussion is significant because it connects foundational ideas in algorithmic information theory—such as Kolmogorov complexity and Solomonoff induction—to modern machine learning practice. It offers a principled lens for model selection and generalization, relevant to researchers and practitioners building predictive systems. The article reportedly equates compression with prediction under the assumption that the data distribution exactly represents all future problems; commenters note that the equivalence becomes subtle when generalization is required, since test distributions may differ arbitrarily. Community responses also point to earlier work by Schmidhuber and to resources like Grant Sanderson&\#x27;s &\#x27;Compression is Intelligence&\#x27; video series.

hackernews · nikolay · Aug 11, 19:49 · [Discussion](https://news.ycombinator.com/item?id=49263497)

**Background**: The idea that compression and prediction are linked comes from algorithmic information theory. Kolmogorov complexity measures the length of the shortest program that produces a given object, while Solomonoff induction formalizes Occam&\#x27;s razor by assigning higher prior probability to theories with shorter algorithmic descriptions. The minimum description length \(MDL\) principle applies this to model selection, choosing models that compress data best. These concepts provide a theoretical foundation for understanding why compression can be seen as a form of prediction.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kolmogorov_complexity">Kolmogorov complexity</a></li>
<li><a href="https://en.wikipedia.org/wiki/Solomonoff_induction">Solomonoff induction</a></li>
<li><a href="https://en.wikipedia.org/wiki/Minimum_description_length">Minimum description length</a></li>

</ul>
</details>

**Discussion**: Commenters engaged deeply with the topic: one referenced a Cambridge course on &\#x27;Information Theory, Inference, and Learning Algorithms&\#x27; and noted that information theory and machine learning belong together; another pointed to Grant Sanderson&\#x27;s video series. Some added nuance—ssivark argued that compression and prediction are equivalent only when the data distribution exactly matches future problems, otherwise generalization makes the story more complicated. Others noted prior art, with rrherr citing Schmidhuber&\#x27;s work on compression progress and QuadrupleA referencing Ted Chiang&\#x27;s analogy of ChatGPT as a &\#x27;blurry JPEG of the web.&\#x27;

**Tags**: `#compression`, `#prediction`, `#machine learning`, `#information theory`, `#ngrok`

---

<a id="item-4"></a>
## [Mojo 1.0 Launches, Aiming to Combine Python Usability with C-Level Speed](https://www.modular.com/blog/modular-26-5-mojo-1-0-is-here) ⭐️ 8.0/10

Modular has released Mojo 1.0, marking a major milestone for its AI-focused programming language, and launched a dedicated language website at mojolang.org. The release emphasizes combining Python-like usability with C/C++-level performance and targets diverse hardware from CPUs to GPUs. Mojo 1.0 matters because it offers a potential alternative for AI developers who want Python&\#x27;s productivity and systems-level speed in one language, reducing the need to write low-level extensions in C, C++ or Rust. If it gains traction, it could reshape how AI infrastructure and model-serving code are written. Mojo is built on the MLIR compiler framework rather than directly on LLVM, which allows it to generate code for CPUs, GPUs, TPUs, ASICs and other accelerators. The standard library is open source under Apache 2.0, but the compiler remains closed-source until Modular&\#x27;s promised open-sourcing in fall 2026; the roadmap also now says Mojo &\#x27;may or may not&\#x27; evolve into a full Python superset.

hackernews · dayanruben · Aug 11, 16:56 · [Discussion](https://news.ycombinator.com/item?id=49261128)

**Background**: Mojo is an in-development systems programming language created by Modular, with syntax designed to resemble Python and semantics inspired by Rust, including static typing and a borrow checker. It was originally conceived as a superset of Python, but that goal has been softened and may not be fully realized. The language aims to let developers write fast, memory-safe code for heterogeneous hardware without vendor lock-in.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mojo_%28programming_language%29">Mojo (programming language) - Wikipedia</a></li>
<li><a href="https://mojolang.org/">Mojo - Modular</a></li>

</ul>
</details>

**Discussion**: Community reaction is cautiously optimistic but marked by healthy skepticism. Several commenters question the value of a closed-source compiler when Rust- or C-based Python libraries already offer performance, ask whether Mojo is still meant to be a Python superset, and criticize AI-generated imagery in the announcement; others also point out that the roadmap says Mojo &\#x27;may or may not&\#x27; fully superset Python. Overall, many remain hopeful but want clearer positioning and faster open-sourcing.

**Tags**: `#Mojo`, `#programming-language`, `#AI`, `#compiler`, `#release`

---

<a id="item-5"></a>
## [Researchers Steal Hidden Reasoning Traces from Proprietary LLM APIs](https://stolen-thoughts.com/) ⭐️ 8.0/10

Researchers demonstrated a method to extract hidden chain-of-thought reasoning from proprietary LLM APIs by replaying a frontier model&\#x27;s trace into a weaker sibling model and jailbreaking it. The technique, detailed in the paper “Stealing Reasoning Traces from Proprietary LLM APIs” \(arXiv:2608.09867\), bypasses encryption and system-level filters. This matters because proprietary LLM providers hide chain-of-thought to protect intellectual property and limit information leakage, and this attack shows those defenses can be circumvented. It raises urgent questions about model security, user privacy, and the ethics of training on other models&\#x27; outputs. The attack works by replaying a trace produced by a frontier model into a weaker sibling model, then jailbreaking the weaker model to reveal the encrypted reasoning text. The paper notes that a direct extraction attack on a more capable model would require bypassing both model-level alignment and system-level defenses such as input filters and output substring-matching filters.

hackernews · quantumgarbage · Aug 11, 13:22 · [Discussion](https://news.ycombinator.com/item?id=49257876)

**Background**: Leading large language model providers now conceal their models&\#x27; step-by-step reasoning, or chain-of-thought, to protect intellectual property and limit information leakage. Rather than storing these traces server-side, providers return them to the client as encrypted text blocks that the client passes back with each subsequent request. Previous research on model extraction attacks has focused on replicating model behavior, recovering training data, or stealing prompts; this work extends that line of research specifically to encrypted reasoning traces. The broader context includes ongoing debate about whether “stealing” is the right term when the output is generated from user-paid tokens.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2608.09867">Stealing Reasoning Traces from Proprietary LLM APIs</a></li>
<li><a href="https://arxiv.org/pdf/2608.09867">Stealing Reasoning Traces from Proprietary LLM APIs - arXiv.org</a></li>
<li><a href="https://stolen-thoughts.com/paper.pdf">Stealing Reasoning Traces from Proprietary LLM APIs</a></li>

</ul>
</details>

**Discussion**: Commenters were divided: some argued that “stealing” is a misleading, morally charged term because users already paid for the tokens, while others suggested the extraction could be done more simply, for example by disabling thinking and providing a “deep\_think” tool. One commenter noted they had achieved a similar result with Codex by auto-injecting a developer prompt, and another wondered whether the attack was intentionally allowed by the provider. A further commenter pointed out that API summaries can make reasoning appear cleaner than it actually is, a distortion that the paper confirms.

**Tags**: `#LLM`, `#security`, `#interpretability`, `#AI safety`, `#reverse engineering`

---

<a id="item-6"></a>
## [Stratechery Analyzes Risks to Nvidia&\#x27;s AI Infrastructure Dominance](https://stratechery.com/2026/nvidias-risky-business/) ⭐️ 8.0/10

Stratechery published a strategic analysis of the risks threatening Nvidia&\#x27;s dominance in AI infrastructure, focusing on challenges to its CUDA software ecosystem and the sustainability of demand growth for AI compute. The piece drew substantial community debate on both technical and economic assumptions. Nvidia&\#x27;s position is central to the AI industry, so any erosion of its dominance would ripple through hardware supply chains, cloud providers, and AI startups. This analysis matters for investors and technologists assessing whether Nvidia&\#x27;s CUDA moat and growth expectations are durable. The article scored 8.0/10 for its high-value strategic perspective, with community comments debating whether CUDA&\#x27;s entrenchment offsets its poor developer experience. A key economic caveat raised is that while demand for compute is certainly growing, the expected rate of growth may be exaggerated.

hackernews · jonbaer · Aug 11, 10:02 · [Discussion](https://news.ycombinator.com/item?id=49255710)

**Background**: CUDA \(Compute Unified Device Architecture\) is Nvidia&\#x27;s proprietary parallel computing platform and API, first released in 2007, that allows software to use GPUs for general-purpose processing. It is deeply embedded in machine learning research, giving Nvidia a software moat that complements its hardware. This entrenchment is why many view Nvidia&\#x27;s position as difficult to attack, even as competitors develop alternatives. The Stratechery analysis examines whether that moat and the growth assumptions built around AI infrastructure demand are as solid as they appear.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/CUDA">CUDA</a></li>

</ul>
</details>

**Discussion**: Commenters offered mixed views: one argued CUDA&\#x27;s entrenchment masks a poor developer experience with C++ footguns, while another noted that although demand for compute is real, growth expectations are likely exaggerated. A third expressed skepticism about AI reaching a singularity given biological efficiency, while another countered that Nvidia is expanding into robotics and remains dominant in the West, apart from China.

**Tags**: `#Nvidia`, `#AI infrastructure`, `#business strategy`, `#CUDA`, `#investment analysis`

---

<a id="item-7"></a>
## [London Underground Trials Live Facial Recognition During Policing Expansion](https://www.btp.police.uk/news/btp/news/england/btp-expands-live-facial-recognition-lfr-trial-into-london-underground-stations/) ⭐️ 8.0/10

British Transport Police are expanding their live facial recognition \(LFR\) trial into London Underground stations, extending the technology from earlier deployments at public events and other locations. The move follows the Metropolitan Police&\#x27;s broader push to intensify LFR use across London despite ongoing legal challenges. This marks a significant step in embedding facial recognition into everyday public transit, where millions of people move through the network daily. It intensifies the debate over mass surveillance, privacy rights, and whether such technology delivers public safety gains worth the civil liberties cost. The LFR system uses CCTV cameras to scan faces in real time and match them against a police watchlist of wanted or suspected individuals. Critics point to risks of false positives, racial bias, and the lack of independent oversight, while police claim the technology has proven effective in identifying suspects and reducing violent crime.

hackernews · BlueBerry2001 · Aug 11, 09:40 · [Discussion](https://news.ycombinator.com/item?id=49255496)

**Background**: Live facial recognition \(LFR\) is a surveillance tool that captures faces from camera feeds and instantly compares them against a database of known individuals. The Metropolitan Police has been trialing LFR for several years at public events and in specific areas, and its expansion into transport hubs like the Underground represents a new frontier for the technology. Supporters argue it helps catch serious criminals, but civil liberties groups warn that it normalizes mass surveillance and undermines anonymous movement in public spaces.

<details><summary>References</summary>
<ul>
<li><a href="https://www.met.police.uk/advice/advice-and-information/facial-recognition/live-facial-recognition-trial/">Live Facial Recognition | Metropolitan Police</a></li>
<li><a href="https://www.biometricupdate.com/202511/metropolitan-police-to-expand-live-facial-recognition-use-even-amid-legal-challenge">Metropolitan Police to expand live facial recognition use ...</a></li>
<li><a href="https://www.theguardian.com/technology/2026/jun/23/met-to-expand-live-facial-recognition-central-london">Met to expand use of live facial recognition into central ...</a></li>

</ul>
</details>

**Discussion**: Community comments were overwhelmingly critical, with many users expressing anger over the intrusion into privacy and civil liberties. Some argued that anonymous travel on the Underground had already been lost through contactless payment systems, while others questioned the trial&\#x27;s purpose, noting that no outcome would likely reverse the rollout; a few compared the situation unfavorably to other countries or invoked Orwellian imagery.

**Tags**: `#facial recognition`, `#privacy`, `#surveillance`, `#London`, `#civil liberties`

---

<a id="item-8"></a>
## [Decoupled Descent: New Training Method Tracks Train-Test Error via AMP Onsager Corrections](https://www.reddit.com/r/MachineLearning/comments/1vlu1se/decoupled_descent_enforcing_exact_traintest_error/) ⭐️ 8.0/10

The author introduces Decoupled Descent \(DD\), a training algorithm that uses approximate message passing \(AMP\) Onsager corrections to guarantee that the training error asymptotically equals the test error at each parameter iterate. The paper studies full-batch gradient descent on stylized Gaussian mixture models and reports 100 simulations on a two-layer XOR model. This work offers a fresh theoretical angle on the train-test error gap, framing it as data reuse bias that can be provably controlled during training. If it scales, it could enable principled optimal stopping and hyperparameter tuning for neural networks, and may inspire new training rules beyond gradient descent. A key limitation is that the result is asymptotic and currently restricted to stylized Gaussian mixture models and full-batch gradient descent; the author notes that large-scale models remain a long way off. The author plans to release a PyTorch-compatible package and invites feature suggestions.

reddit · r/MachineLearning · /u/mlovik1 · Aug 11, 21:06

**Background**: Approximate message passing \(AMP\) is a family of iterative algorithms for high-dimensional statistical problems such as compressed sensing, where each step adds a memory/Onsager correction term that allows the algorithm&\#x27;s behavior to be tracked by a scalar state evolution. The Onsager correction, named after Lars Onsager, removes correlations between iterates and past noise, which is what lets AMP-based methods give exact predictions for train and test error. Decoupled Descent applies this idea to neural network training so that a certificate of train-test matching can be provided at each iterate.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2201.07487">A Concise Tutorial on Approximate Message Passing A unifying tutorial on Approximate Message Passing Lecture 19: Approximate message passing algorithms Approximate Message Passing Tutorial - GitHub Pages Message-passing algorithms for compressed sensing A unifying tutorial on Approximate Message Passing Note on Approximate Message Passing - Peng Xu</a></li>
<li><a href="https://arxiv.org/abs/2105.02180">A unifying tutorial on Approximate Message Passing Lecture 19: Approximate message passing algorithms Approximate Message Passing Tutorial - GitHub Pages Message-passing algorithms for compressed sensing A unifying tutorial on Approximate Message Passing Note on Approximate Message Passing - Peng Xu</a></li>
<li><a href="https://arxiv.org/abs/2601.07095">Score-Based VAMP with Fisher-Information-Based Onsager Correction</a></li>

</ul>
</details>

**Tags**: `#approximate-message-passing`, `#generalization`, `#training theory`, `#neural networks`, `#high-dimensional statistics`

---

<a id="item-9"></a>
## [HyperSAE: Poincaré Geometry for Sparse Autoencoders Reduces MSE by 9.8%](https://www.reddit.com/r/MachineLearning/comments/1vlpyh2/hypersae_decoupled_poincar%C3%A9_geometry_for_sparse/) ⭐️ 8.0/10

HyperSAE is a new PyTorch library that applies Poincaré hyperbolic geometry to sparse autoencoders \(SAEs\) for mechanistic interpretability. On Gemma-2-2B Layer 13 with 20M tokens, it achieves a 9.8% reduction in reconstruction MSE, cuts dead latents from 3.8% to 0.2%, and improves CE loss recovery by 3.4 percentage points. This work addresses two known pain points in SAE training—feature collisions and dead latents—by using hyperbolic geometry that matches the branching hierarchical structure of concepts in LLMs. Because HyperSAE keeps the forward pass Euclidean, it adds zero inference overhead and could make SAE-based interpretability tools more reliable and scalable for large models. HyperSAE uses a decoupled dual-speed design: the forward pass and causal steering remain Euclidean \(single vector addition\), while dictionary weights are projected into the Poincaré ball during training. An entailment cone loss places parent concepts near the origin and child concepts near the boundary; the TriPartite loss combines reconstruction, L1 sparsity, and entailment terms, and the library includes co-activation queue tracking and a single-class trainer.

reddit · r/MachineLearning · /u/visha1v · Aug 11, 18:37 · [Discussion](https://www.reddit.com/r/MachineLearning/comments/1vlpyh2/hypersae_decoupled_poincar%C3%A9_geometry_for_sparse/)

**Background**: Sparse autoencoders \(SAEs\) are used in mechanistic interpretability to decompose neural network activations into sparse, interpretable features. Standard SAEs embed dictionary atoms in Euclidean space, whose volume grows polynomially, whereas concepts learned by LLMs often form hierarchies that grow exponentially, causing collisions and dead features at large dictionary sizes. Poincaré models are a standard representation of hyperbolic geometry, where distances expand exponentially toward the boundary, making them natural for tree-like hierarchies. Entailment cones are a technique for embedding hierarchical relations in such spaces.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2406.04093">[2406.04093] Scaling and evaluating sparse autoencoders Scaling and evaluating sparse autoencoders - OpenAI ICLR Poster Scaling and evaluating sparse autoencoders (PDF) Scaling and evaluating sparse autoencoders - ResearchGate Dead Feature Counts in Sparse Autoencoders Predict Underlying ... Beyond Input Activations: Identifying Influential Latents by ...</a></li>
<li><a href="https://openaccess.thecvf.com/content_CVPRW_2020/papers/w50/Dhall_Hierarchical_Image_Classification_Using_Entailment_Cone_Embeddings_CVPRW_2020_paper.pdf">Hierarchical Image Classiﬁcation using Entailment Cone Embeddings</a></li>

</ul>
</details>

**Tags**: `#sparse autoencoders`, `#mechanistic interpretability`, `#hyperbolic geometry`, `#representation learning`, `#LLM interpretability`

---