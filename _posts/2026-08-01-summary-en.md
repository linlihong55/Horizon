---
layout: default
title: "Horizon Summary: 2026-08-01 (EN)"
date: 2026-08-01
lang: en
---

> From 36 items, 7 important content pieces were selected

---

1. [DeepSeek V4 Flash 0731 Launches: Frontier-Level AI at Ultra-Low Price](#item-1) ⭐️ 9.0/10
2. [Huawei Open-Sources 505B-Parameter MoE Model openPangu-2.0-Pro](#item-2) ⭐️ 9.0/10
3. [Elevator Scheduling Algorithms: A Simulation-Based Analysis](#item-3) ⭐️ 8.0/10
4. [YC-Backed qm Launches Multiplayer Agent Harness for Work](#item-4) ⭐️ 8.0/10
5. [Stateless MCP 2.0 Reignites Interest, Inspires mcp-explorer and datasette-mcp](#item-5) ⭐️ 8.0/10
6. [Simon Willison Joins Oxide and Friends to Discuss Open-Weight AI Revolution](#item-6) ⭐️ 8.0/10
7. [German Court Rules AI Music Firm Suno Violated Copyright](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [DeepSeek V4 Flash 0731 Launches: Frontier-Level AI at Ultra-Low Price](https://artificialanalysis.ai/models/deepseek-v4-flash) ⭐️ 9.0/10

DeepSeek officially released V4 Flash 0731, the successor to its V4 Flash preview, scoring 50 on the Artificial Analysis Intelligence Index — 10 points higher than the previous version. Agentic performance jumped as well, with an Elo of 1559 on GDPval-AA v2, up from 1189. The release shows that an efficiency-optimized, low-cost model can now sit at the frontier of AI intelligence, challenging the economics of larger proprietary systems. With API pricing at just $0.14 per million input tokens and $0.28 per million output tokens, DeepSeek makes advanced agentic AI affordable for a much wider range of developers and applications. V4 Flash 0731 is a sparse mixture-of-experts model with 284B total parameters, 13B activated per token, and a 1M-token context window. It keeps the same architecture as the preview and only revises post-training, while natively supporting the Responses API format and including targeted adaptation for OpenAI&\#x27;s Codex.

hackernews · theanonymousone · Jul 31, 07:59 · [Discussion](https://news.ycombinator.com/item?id=49120299)

**Background**: DeepSeek is a Chinese AI lab that openly releases model weights, and its V4 series uses a Mixture-of-Experts design in which only a fraction of parameters are active per token, cutting inference cost while keeping capability high. The Artificial Analysis Intelligence Index aggregates public and private evaluations to rank models, and a score of 50 places V4 Flash 0731 on the frontier alongside systems that are far more expensive to run.

<details><summary>References</summary>
<ul>
<li><a href="https://artificialanalysis.ai/articles/deepseek-v4-flash-0731-scores-50-on-the-artificial-analysis-intelligence-index-10-points-above-previous-deepseek-v4-flash">DeepSeek V4 Flash 0731 scores 50 on the Artificial Analysis Intelligence Index, 10 points above previous DeepSeek V4 Flash</a></li>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4-flash-0731">DeepSeek V4 Flash 0731 - API Pricing &amp; Benchmarks | OpenRouter</a></li>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash-0731">deepseek-ai/DeepSeek-V4-Flash-0731 · Hugging Face</a></li>

</ul>
</details>

**Discussion**: Comments are largely enthusiastic, celebrating frontier-level intelligence at an extremely low price and noting that the model works well as a daily coding driver. Some users wonder whether an upcoming V4 Pro could surpass it, while others debate the sustainability of large-scale open model hosting and approximate cost comparisons with other frontier models.

**Tags**: `#AI`, `#DeepSeek`, `#LLM`, `#model release`, `#cost analysis`

---

<a id="item-2"></a>
## [Huawei Open-Sources 505B-Parameter MoE Model openPangu-2.0-Pro](https://huggingface.co/openpangu/openPangu-2.0-Pro) ⭐️ 9.0/10

Huawei has open-sourced openPangu-2.0-Pro on Hugging Face, a Mixture-of-Experts LLM with about 505B total parameters and about 18B active per token, supporting a 512k context window. The Thinking variant scores 95.4 on AIME 2026 and 87.9 on GPQA-Diamond. This is one of the largest open-source MoE releases from Huawei, trained on Ascend NPUs, demonstrating a viable non-NVIDIA AI stack. It could strengthen the open-weight LLM ecosystem and provide researchers with an advanced long-context reasoning model. The architecture uses Multi-head Latent Attention \(MLA\), a hybrid DSA+SWA layered attention design, and a 3-head Multi-Token Prediction \(MTP\) module for self-speculative decoding. Training used roughly 34T tokens, with post-training combining fast/slow integrated fine-tuning and multi-task reinforcement learning.

telegram · zaihuapd · Jul 31, 06:50

**Background**: OpenPangu-2.0-Pro is a Mixture-of-Experts \(MoE\) model, where a large set of parameters is split into experts and only a subset is activated per token, balancing quality and inference cost. MLA compresses key-value cache to reduce memory overhead, while DSA+SWA hybrid attention mixes sliding-window and content-selected attention for efficient long context. MTP enables faster decoding by predicting several future tokens at once. Ascend NPUs are Huawei&\#x27;s AI accelerators, making this release notable for AI hardware diversity.

<details><summary>References</summary>
<ul>
<li><a href="https://sebastianraschka.com/llms-from-scratch/ch04/05_mla/">MLA Chapter 4 Guide | Sebastian Raschka, PhD</a></li>
<li><a href="https://sebastianraschka.com/llm-architecture-gallery/mtp/">Multi-Token Prediction (MTP) | Sebastian Raschka, PhD</a></li>
<li><a href="https://www.pythonalchemist.com/llm-architectures/attention-variants">Attention Variants Explained: MHA, GQA, MQA, MLA, SWA , DSA</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#MoE`, `#Huawei`, `#Open Source`, `#AI`

---

<a id="item-3"></a>
## [Elevator Scheduling Algorithms: A Simulation-Based Analysis](https://john.fun/elevators) ⭐️ 8.0/10

The article &\#x27;Elevators&\#x27; by john.fun presents an analysis of elevator scheduling algorithms using simulations, comparing approaches such as FCFS, SCAN, and LOOK under different conditions. It highlights the trade-offs between efficiency and fairness for each algorithm. Elevator scheduling is a classic real-world optimization problem that directly affects user experience in buildings. This analysis connects elevator algorithms to disk-scheduling concepts, showing how ideas from one domain transfer to another, and has sparked a rich community discussion about real-world behavior. The simulations compare multiple algorithms, including FCFS, SSTF, SCAN, and LOOK, each with different trade-offs in response time and fairness. Community members noted that real-world travel patterns, such as destination dispatch usage in office buildings, can make some algorithms perform differently than random simulations suggest.

hackernews · Jrh0203 · Jul 31, 15:17 · [Discussion](https://news.ycombinator.com/item?id=49124218)

**Background**: The elevator algorithm, also known as SCAN, is a disk-scheduling algorithm that determines the motion of a disk arm while servicing read and write requests. In elevator scheduling, the elevator car moves in one direction until no more requests are ahead, then reverses direction, similar to how a disk head sweeps across tracks. LOOK is a variant that only goes as far as the last request in each direction, saving unnecessary travel. These algorithms are widely taught in computer science courses and are also used in game simulations like Elevator Saga.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Elevator_algorithm">Elevator algorithm - Wikipedia</a></li>
<li><a href="https://dev.to/thesaltree/elevator-scheduling-algorithms-fcfs-sstf-scan-and-look-2pae">Elevator Scheduling Algorithms: FCFS, SSTF, SCAN, and LOOK - DEV Community</a></li>
<li><a href="https://www.geeksforgeeks.org/dsa/scan-elevator-disk-scheduling-algorithms/">SCAN (Elevator) Disk Scheduling Algorithms - GeeksforGeeks</a></li>

</ul>
</details>

**Discussion**: Commenters connected elevator scheduling to disk scheduling, noting that HDDs behave like &\#x27;one really long elevator&\#x27; and that SCAN is a true disk-scheduling algorithm. Several shared practical experiences: destination dispatch in real buildings often has skewed travel patterns \(e.g., everyone going to the ground floor\), which may make it worse than random simulations suggest, while one developer of the elevator game Sky Lobby said they chose LOOK because it matched player expectations.

**Tags**: `#algorithms`, `#simulation`, `#elevators`, `#systems`, `#scheduling`

---

<a id="item-4"></a>
## [YC-Backed qm Launches Multiplayer Agent Harness for Work](https://github.com/yc-software/qm) ⭐️ 8.0/10

qm, a YC-backed multiplayer agent harness for work, has been published on GitHub at github.com/yc-software/qm. It uses per-person scopes and shared rooms to coordinate company-wide AI assistants, following the pattern of local coding agents like OpenCode, Codex, and Claude Code. qm directly tackles scoping, which practitioners call the hardest problem in multiplayer agents, by pairing per-person scopes with shared rooms for company-wide coordination. As a YC-backed project in the fast-moving LLM agent space, it signals a shift from single-agent loops toward orchestrating AI assistants across entire teams. In qm, the agent acts as the person it works for, using that person&\#x27;s credentials and permissions, with every action audited. An organization sets one overall security posture, and narrower per-person scopes can only tighten it further.

hackernews · tosh · Jul 31, 18:04 · [Discussion](https://news.ycombinator.com/item?id=49126604)

**Background**: An agent harness is the complete software infrastructure wrapping an LLM, including the orchestration loop, tools, and memory; the term was formalized around early 2026, though the concept predates it. In harness engineering, developers treat this scaffolding as a real artifact and tighten it whenever an agent makes a mistake. For multiplayer coordination, tools like Agent Room let AI coding agents on different machines collaborate in persistent shared rooms, often over the Model Context Protocol \(MCP\).

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/yc-software/qm">GitHub - yc-software/ qm : Multiplayer agent harness for work · GitHub</a></li>
<li><a href="https://habr.com/ru/articles/1023316/">Что такое Harness ? Полный разбор на примере Claude... / Хабр</a></li>
<li><a href="https://www.agent-room.com/">Agent Room — Multi-agent collaboration for Claude Code, Codex, Cursor &amp; Gemini</a></li>

</ul>
</details>

**Discussion**: Commenters largely welcomed the direction: one builder called per-person scopes plus shared rooms &\#x27;a sane answer for a company-wide assistant&\#x27; and found YC shipping this &\#x27;validating and a little surreal.&\#x27; A humorous anecdote described an agent scheduling meetings with other agents without human involvement, while another commenter asked for a &quot;QM vs Cowork&quot; comparison and questioned qm&\#x27;s advantage over Claude Cowork. Others noted the difficulty of understanding new LLM-era apps and pointed to related tools like Garry Tan&\#x27;s gstack.

**Tags**: `#AI agents`, `#multiplayer`, `#LLM tools`, `#YC`, `#developer tools`

---

<a id="item-5"></a>
## [Stateless MCP 2.0 Reignites Interest, Inspires mcp-explorer and datasette-mcp](https://simonwillison.net/2026/Jul/31/stateless-mcp/#atom-everything) ⭐️ 8.0/10

MCP 2.0, the 2026-07-28 Model Context Protocol specification, introduces stateless MCP, eliminating the need for session IDs. Simon Willison built three new tools this week, including mcp-explorer and datasette-mcp. This is the most significant change to MCP since its launch, greatly simplifying client and server implementation and enabling horizontal scaling for remote servers. It may reignite adoption of MCP among AI agent developers, especially for smaller models and auditable workflows. Stateless MCP uses a single HTTP request with MCP-Protocol-Version and Mcp-Method headers instead of two round-trips with a Mcp-Session-Id. mcp-explorer is a CLI for interactively probing MCP servers, while datasette-mcp provides read-only access to Datasette instances.

rss · Simon Willison · Jul 31, 23:13

**Background**: MCP \(Model Context Protocol\) is an open standard introduced by Anthropic in November 2024 to standardize how LLM-powered agents connect to external tools and data. Earlier stateful MCP required a two-step initialization to create a session, which complicated scaling. The new stateless design sends all needed context in each request, making it easier to build and deploy servers. This shift comes after MCP&\#x27;s popularity waned somewhat in 2025 amid competition from approaches like Claude Skills.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol - Wikipedia</a></li>
<li><a href="https://stackpicks.dev/blog/mcp-2-0-explained-2026">MCP 2 . 0 Explained — Stateless Core, OAuth Login... — StackPicks</a></li>
<li><a href="https://www.anthropic.com/news/model-context-protocol">Introducing the Model Context Protocol \ Anthropic</a></li>

</ul>
</details>

**Tags**: `#MCP`, `#AI agents`, `#Model Context Protocol`, `#software engineering`, `#developer tools`

---

<a id="item-6"></a>
## [Simon Willison Joins Oxide and Friends to Discuss Open-Weight AI Revolution](https://simonwillison.net/2026/Jul/31/oxide-and-friends/#atom-everything) ⭐️ 8.0/10

Simon Willison appeared on the Oxide and Friends podcast on July 31, 2026 to discuss the open-weight AI model revolution, including Kimi K3&\#x27;s parity with proprietary frontier models, recent AI security incidents, and industry letters on open weights. He also noted that DeepSeek V4 Flash and Anthropic&\#x27;s own cyber incident occurred just days after the recording, quickly making the episode out-of-date. This expert discussion highlights a pivotal moment in AI: open-weight models like Kimi K3 are now competing head-to-head with proprietary models, challenging the assumption that frontier AI must remain closed. The industry letters and the notable absence of Anthropic&\#x27;s signature underscore a deepening debate over openness, security, and American AI leadership. Kimi K3 is a 2.8-trillion-parameter open-source model built on Kimi Delta Attention and Attention Residuals, with native vision and a 1-million-token context window, released under a Modified MIT license. The episode also covered Golden Gate Claude, the Zizians case, Soviet Marburg virus research, and the lead-crime hypothesis, and Simon added a new prediction that the Pope will say something about open models by the end of the year.

rss · Simon Willison · Jul 31, 21:33

**Background**: Open-weight models are AI models whose core components, including the trained parameters or &\#x27;weights&\#x27;, are publicly released so that anyone can download and run them. Kimi K3, from Moonshot AI, is one of the latest flagships in this category, while DeepSeek simultaneously released DeepSeek V4 Flash on July 31, 2026. This rapid succession of releases has intensified discussions about whether open-weight models can safely match or even surpass closed proprietary systems.

<details><summary>References</summary>
<ul>
<li><a href="https://www.kimi.com/blog/kimi-k3">Kimi K 3 Tech Blog: Open Frontier Intelligence</a></li>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash">deepseek -ai/ DeepSeek - V 4 - Flash · Hugging Face</a></li>

</ul>
</details>

**Tags**: `#open-weight models`, `#AI`, `#podcast`, `#Simon Willison`, `#Kimi K3`

---

<a id="item-7"></a>
## [German Court Rules AI Music Firm Suno Violated Copyright](https://www.dw.com/en/german-court-rules-that-ai-music-firm-suno-violated-copyrights/a-78152227) ⭐️ 8.0/10

The Munich Regional Court ruled against AI music company Suno, finding that it infringed copyright by using protected music to train its models. The court ordered Suno to disclose illegal gains and pay unspecified damages, and Suno says it will consider an appeal. This is one of the first major cases testing how copyright law applies to AI music training, so the ruling could set a precedent for the AI industry worldwide. It strengthens the hand of rights holders like GEMA in seeking licensing agreements and may push AI companies toward greater transparency about training data. The lawsuit, filed by GEMA in January 2025, represents more than 95,000 German musicians and over 2 million rights holders worldwide; GEMA demonstrated that Suno-generated songs were highly similar to original works. GEMA&\#x27;s stated goal is to achieve equal licensing negotiations.

telegram · zaihuapd · Jul 31, 13:11

**Background**: Suno is a generative AI music creation platform that produces songs with vocals and instrumentation from text prompts. GEMA is a German collective management organization that manages the rights of over 90,000 members and more than 2 million rights holders globally. This case tests whether using copyrighted works to train AI models without licensing constitutes infringement.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Suno_%28platform%29">Suno (platform) - Wikipedia</a></li>
<li><a href="https://www.gema.de/en/w/help/gema/organisation/questions-and-answers/what-is-gema">What is GEMA and what is its purpose?</a></li>

</ul>
</details>

**Tags**: `#AI`, `#copyright`, `#legal`, `#music`, `#Suno`

---