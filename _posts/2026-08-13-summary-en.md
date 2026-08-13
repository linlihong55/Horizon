---
layout: default
title: "Horizon Summary: 2026-08-13 (EN)"
date: 2026-08-13
lang: en
---

> From 34 items, 11 important content pieces were selected

---

1. [New Tool &\#x27;Spaghettifying DRAM&\#x27; Reverse-Engineers Memory Addressing via Rowhammer](#item-1) ⭐️ 9.0/10
2. [Choose Boring Technology: Budget Your Innovation Tokens](#item-2) ⭐️ 9.0/10
3. [DeepMind SL2T Brings Sign Language-to-Text AI to Pixel 11](#item-3) ⭐️ 9.0/10
4. [DeepSeek-V4-Pro launches with Agent upgrades and time-based pricing](#item-4) ⭐️ 9.0/10
5. [Google Unveils Gemini 3.7 Flash with Vision and Price Hike](#item-5) ⭐️ 8.0/10
6. [Cerebras and OpenAI Accelerate GPT-5.6 Sol Ultrafast Mode](#item-6) ⭐️ 8.0/10
7. [DeepSeek releases open-source AI harness developer preview](#item-7) ⭐️ 8.0/10
8. [Gloomberb brings an open-source tiling terminal to financial data.](#item-8) ⭐️ 8.0/10
9. [DeepSeek V4 Pro 0813 Released with Open Weights on Hugging Face](#item-9) ⭐️ 8.0/10
10. [Trump Signs Memo to Enlist Private Firms in Overseas Cyber Operations](#item-10) ⭐️ 8.0/10
11. [DeepSeek Launches Open-Source Harness and V4-Pro-0813 Weights](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [New Tool &\#x27;Spaghettifying DRAM&\#x27; Reverse-Engineers Memory Addressing via Rowhammer](https://github.com/xoreaxeaxeax/skitter-creek-bath-salts) ⭐️ 9.0/10

Christopher Domas has released &\#x27;Spaghettifying DRAM&\#x27;, a tool that reverse-engineers DRAM row/bank/column address mappings by exploiting the row hammer effect. The tool is available on GitHub under the repository &\#x27;skitter-creek-bath-salts&\#x27;. This research exposes a large and largely hidden attack surface in modern DRAM, potentially allowing attackers with ring-0 access to reach data normally protected in negative-ring territory. It also raises concerns for console security, such as Xbox and PlayStation, where hardware isolation was previously considered strong. The tool works on the AMD Jaguar architecture from 2013; the README notes that Zen 3 uses a different base address for memory controller registers, leaving newer CPU compatibility unclear. By deriving the physical address bit assignments for row, bank, and column, it enables targeted rowhammer attacks and deeper memory introspection.

hackernews · matt\_d · Aug 13, 14:17 · [Discussion](https://news.ycombinator.com/item?id=49286341)

**Background**: DRAM chips are organized into banks, rows, and columns, and a memory controller maps physical addresses to these structures using often-proprietary bit assignments. The row hammer effect is a DRAM reliability side effect where rapidly accessing one row can cause bit flips in neighboring rows, and it has become a known security vulnerability. Understanding the exact address mapping improves an attacker&\#x27;s ability to target flips, which is what this tool automates.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Row_hammer">Row hammer - Wikipedia</a></li>
<li><a href="https://www.mdpi.com/1424-8220/24/2/592">Rowhammer Attacks in Dynamic Random-Access Memory and ... - MDPI</a></li>
<li><a href="https://people.inf.ethz.ch/omutlu/pub/onur-Bogazici-June-13-2013-lecture2-1-dram-basics-and-scaling-afterlecture.pptx">Memory Systems in the Multi-Core EraLecture 1: DRAM Basics and...</a></li>

</ul>
</details>

**Discussion**: Commenters are enthusiastic about Christopher Domas&\#x27;s upcoming Black Hat talk, praising his ability to explain complex research. Some express concern about the implications for console security, while others ask which newer CPUs are affected beyond the old AMD Jaguar architecture.

**Tags**: `#DRAM`, `#security`, `#reverse-engineering`, `#hardware`, `#rowhammer`

---

<a id="item-2"></a>
## [Choose Boring Technology: Budget Your Innovation Tokens](https://mcfunley.com/choose-boring-technology) ⭐️ 9.0/10

Dan McKinley’s 2015 essay &\#x27;Choose Boring Technology&\#x27; argues that companies have a fixed budget of roughly three &\#x27;innovation tokens&\#x27; and should spend them only on technology that directly differentiates their product. The essay recently resurfaced on Hacker News, earning 212 points and 116 comments. The &\#x27;innovation tokens&\#x27; framework gives engineers and managers a simple, memorable way to justify pragmatic technology choices and push back against hype-driven adoption. It remains highly relevant as teams evaluate new tools, AI agents, and infrastructure decisions. McKinley originally published the essay in 2015, drawing on his experience building scalable systems; he argues that adding any new technology carries maintenance and integration costs. In the Hacker News thread, commenters note that a sensible modern application is to spend all of your innovation tokens on an AI agent layer while keeping the surrounding stack boring.

hackernews · tosh · Aug 13, 17:48 · [Discussion](https://news.ycombinator.com/item?id=49289512)

**Background**: The essay popularized the term &\#x27;innovation tokens&\#x27;: a finite budget for deviating from standard practice. Boring technology means mature, well-understood tools whose failure modes are known, rather than tools that are merely unexciting. The concept echoes earlier engineering ideas such as Gunpei Yokoi&\#x27;s &\#x27;lateral thinking with withered technology,&\#x27; and has become a touchstone in debates about pragmatism versus novelty in software engineering.

<details><summary>References</summary>
<ul>
<li><a href="https://mcfunley.com/choose-boring-technology">Dan McKinley :: Choose Boring Technology</a></li>
<li><a href="https://www.lessannoyingbusiness.com/post/innovation-tokens">Innovation Tokens - When to break from the status quo</a></li>
<li><a href="https://xebia.com/blog/how-innovation-tokens-can-change-your-life/">How Innovation Tokens Can Change Your Life | Xebia</a></li>

</ul>
</details>

**Discussion**: Commenters largely praised the essay: one called it a favorite and said the token idea helps explain tradeoffs to colleagues at all levels, while another wished for a jobs board that vets for pragmatic engineering culture. A commenter suggested that, in the age of AI agents, teams should push all their innovation tokens into agents and use &\#x27;in-distribution&\#x27; boring tech around them. However, one dissenter argued that &\#x27;innovation tokens&\#x27; are arbitrary and that &\#x27;novel&\#x27; is a weak proxy for risk and value.

**Tags**: `#technology-choice`, `#innovation-tokens`, `#software-engineering`, `#pragmatism`, `#engineering-culture`

---

<a id="item-3"></a>
## [DeepMind SL2T Brings Sign Language-to-Text AI to Pixel 11](https://deepmind.google/blog/putting-sign-language-ai-into-users-hands/) ⭐️ 9.0/10

Google DeepMind unveiled SL2T, a multilingual sign language-to-text model, and deployed it in Pixel 11&\#x27;s Gboard and Live Transcribe, initially supporting American Sign Language to English translation. This marks the first time sign language AI has been integrated into mainstream consumer products, potentially improving accessibility for deaf and hard-of-hearing users. It sets a precedent for future accessibility features across devices. SL2T was trained on over 100,000 hours of sign language video spanning 50+ languages, and achieves a zero-shot BLEURT score of 70 on the FLEURS-ASL benchmark. For privacy, it processes only hand and body pose keypoints rather than raw video frames.

telegram · zaihuapd · Aug 13, 08:55

**Background**: BLEURT is a learned evaluation metric for natural language generation that measures how well a candidate text matches a reference in fluency and meaning. FLEURS-ASL is an extension of the FLORES/FLEURS benchmarks that adds American Sign Language video, enabling evaluation of sign language translation. Pose keypoint detection is a computer vision technique that tracks meaningful points on a person&\#x27;s body, which allows models to understand sign language without storing or processing identifiable video.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2004.04696">BLEURT: Learning Robust Metrics for Text Generation BLEURT: Learning Robust Metrics for Text Generation BLEURT Explained: A Learned Metric for AI Text Quality Bleurt Metric: A Comprehensive Guide for 2025 - Shadecoder ... bleurt/README.md at master · google-research/bleurt · GitHub bleurt.py · evaluate-metric/bleurt at main - Hugging Face</a></li>
<li><a href="https://aclanthology.org/2025.naacl-long.314/">FLEURS-ASL: Including American Sign Language in Massively Multilingual Multitask Evaluation - ACL Anthology</a></li>
<li><a href="https://viso.ai/deep-learning/pose-estimation-ultimate-overview/">Real-Time Pose Estimation in Computer Vision</a></li>

</ul>
</details>

**Tags**: `#sign language`, `#accessibility`, `#DeepMind`, `#AI model`, `#Pixel`

---

<a id="item-4"></a>
## [DeepSeek-V4-Pro launches with Agent upgrades and time-based pricing](https://api-docs.deepseek.com/zh-cn/updates) ⭐️ 9.0/10

DeepSeek-V4-Pro is now officially available on the app, web, and API under the model name deepseek-v4-pro. The new version enhances agent capabilities, natively supports the Responses API format for Codex compatibility, and introduces peak/off-peak API pricing effective August 17, 2026, with off-peak rates at half the peak price. DeepSeek is a widely adopted model family, so this major update strengthens its position among developers building agentic applications. The compatibility with OpenAI&\#x27;s Responses API and Codex lowers the barrier for teams that want to switch or use DeepSeek within existing toolchains, while time-based pricing offers a new lever for cost optimization. The API calling method remains unchanged, and the model is set to deepseek-v4-pro. The V4-Pro and V4-Flash thinking modes now support three levels — low, high, and max — and the new pricing applies to the API starting at 0:00 on August 17, 2026.

telegram · zaihuapd · Aug 13, 11:12

**Background**: DeepSeek is a Chinese AI company that offers large language models via API. The Responses API is a developer tool originally released by OpenAI in March 2025 to simplify building agentic applications, and Codex is OpenAI&\#x27;s AI coding agent that integrates with various IDEs. By natively supporting the Responses API format, DeepSeek makes its models usable in tools and workflows built around that standard, including Codex-compatible environments.

<details><summary>References</summary>
<ul>
<li><a href="https://grokipedia.com/page/OpenAI_Responses_API">OpenAI Responses API</a></li>
<li><a href="https://en.wikipedia.org/wiki/Codex_%28AI_agent%29">Codex (AI agent)</a></li>
<li><a href="https://developers.openai.com/api/reference/responses/overview">Responses Overview | OpenAI API Reference</a></li>

</ul>
</details>

**Tags**: `#DeepSeek`, `#AI`, `#API`, `#LLM`, `#Pricing`

---

<a id="item-5"></a>
## [Google Unveils Gemini 3.7 Flash with Vision and Price Hike](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-3-7-flash/) ⭐️ 8.0/10

Google introduced Gemini 3.7 Flash, a vision-capable model built on Gemini 3.6 Flash, with introductory pricing scheduled to double on December 31, 2026. It delivers notable gains on document and automation benchmarks, and now powers Gemini Spark for AI Pro and Ultra subscribers. Gemini 3.7 Flash strengthens Google&\#x27;s low-cost, high-volume &\#x27;workhorse&\#x27; model tier, making advanced reasoning and multimodal capabilities more accessible for developers and enterprises. The release also intensifies competition with other fast, cheap models like GPT-5.6 Luna and Terra, as pricing and real-world performance become key battlegrounds. The model is based on Gemini 3.6 Flash and supports a 1M token context window with text, image, audio, and video inputs. It improves over 3.6 Flash on GDP.pdf \(34.0% vs 22.0%\) and AutomationBench \(30.4% vs 17.0%\), and with high reasoning it is 40% faster than GPT-5.6 Terra \(max\) per task, while costing just $1.50/1M input and $7.50/1M output tokens during the intro period.

hackernews · thisisauserid · Aug 13, 17:23 · [Discussion](https://news.ycombinator.com/item?id=49289112)

**Background**: Gemini Flash is Google&\#x27;s cost-efficient model family designed for high-volume, latency-sensitive tasks such as summarization, parsing, and coding agents, complementing the larger Pro models. Gemini 3.7 Flash continues this line, adding adjustable reasoning levels \(high, medium, low\) and multimodal support. Hybrid reasoning models like this often attract significant community testing around price-to-performance and benchmark results.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-3-7-flash/">Gemini 3 . 7 Flash : our most intelligent workhorse model</a></li>
<li><a href="https://deepmind.google/models/model-cards/gemini-3-7-flash/">Gemini 3 . 7 Flash - Model Card — Google DeepMind</a></li>
<li><a href="https://artificialanalysis.ai/articles/gemini-3-7-time-frontier">Gemini 3 . 7 Flash : On the Intelligence vs . Time per Task Pareto frontier</a></li>

</ul>
</details>

**Discussion**: Commenters shared hands-on tests and mixed reactions: one found Gemini 3.7 Flash strong at image-to-HTML but still behind Opus 5, while another praised its price-performance but questioned the planned price doubling only months after 3.6 Flash&\#x27;s release. Several compared it to GPT-5.6 Luna and Terra, arguing Luna is cheaper and stronger on DeepSWE, potentially undercutting the Flash lineup&\#x27;s value.

**Tags**: `#AI`, `#Google`, `#Gemini`, `#LLM`, `#Model Release`

---

<a id="item-6"></a>
## [Cerebras and OpenAI Accelerate GPT-5.6 Sol Ultrafast Mode](https://www.cerebras.ai/blog/accelerating-gpt-5-6-sol-ultrafast-with-openai) ⭐️ 8.0/10

OpenAI and Cerebras announced that GPT-5.6 Sol&\#x27;s Ultrafast mode answered all 2,500 Humanity&\#x27;s Last Exam questions in 11 hours and 11 minutes, roughly 7 times faster than competitor Claude Fable 5&\#x27;s 78 hours, while achieving comparable accuracy. The result marks a major milestone in the collaboration between the two companies. This speedup matters because frontier reasoning tasks—like solving Humanity&\#x27;s Last Exam—currently require hours of continuous compute; making them 7x faster can unlock broader practical applications and lower deployment costs. It also signals that specialized hardware such as Cerebras&\#x27;s wafer-scale engines can meaningfully compete with GPU-based clouds for cutting-edge inference workloads. Despite the headline speedup, neither Cerebras nor OpenAI explicitly stated that Ultrafast mode matches the standard GPT-5.6 Sol&\#x27;s performance on all benchmarks—the post refers to &quot;comparable accuracy&quot; on HLE only. OpenAI&\#x27;s companion post also did not list pricing for the new mode, and reported output speeds vary across independent leaderboards \(e.g., Artificial Analysis counts GPT-5.6 Sol Ultrafast as 11x faster than Fable 5 and 5x faster than Opus 4.8 Fast\).

hackernews · pr337h4m · Aug 13, 18:10 · [Discussion](https://news.ycombinator.com/item?id=49289844)

**Background**: Humanity&\#x27;s Last Exam \(HLE\) is a frontier AI benchmark containing 2,500 expert-written questions across mathematics, sciences, and humanities, designed to measure the upper bounds of LLM knowledge. Cerebras Systems is a Silicon Valley company known for its Wafer-Scale Engine, the world&\#x27;s largest AI processor, which it sells as part of CS-3 supercomputers and an AI inference/training cloud. GPT-5.6 Sol is OpenAI&\#x27;s flagship model in the GPT-5.6 series, oriented toward complex reasoning, coding, and agentic workflows. The collaboration aims to show that Cerebras&\#x27;s wafer-scale hardware can run such models far faster than conventional GPU clusters for long-horizon inference tasks.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cerebras_Systems">Cerebras Systems - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Humanity&#x27;s_Last_Exam">Humanity&#x27;s Last Exam - Wikipedia</a></li>
<li><a href="https://openrouter.ai/openai/gpt-5.6-sol">GPT - 5 . 6 Sol - API Pricing &amp; Benchmarks | OpenRouter</a></li>

</ul>
</details>

**Discussion**: Community reaction is a mix of enthusiasm and skepticism. Some commenters are excited that the OpenAI–Cerebras collaboration finally produced a headline speedup, and argue that faster inference enables iterative thinking and better outputs; others, however, point out that neither company explicitly confirmed that Ultrafast mode is behaviorally identical to standard GPT-5.6 Sol, and that the absence of pricing information suggests it may be aimed at a niche, expensive segment.

**Tags**: `#AI`, `#LLM`, `#inference speed`, `#OpenAI`, `#Cerebras`

---

<a id="item-7"></a>
## [DeepSeek releases open-source AI harness developer preview](https://deepseek.com/harness/en/) ⭐️ 8.0/10

DeepSeek has published an early developer preview of DeepSeek Harness on GitHub under the MIT license, featuring full run traceability and a plugin-based architecture. The preview includes documentation and is positioned as a rough, compatibility-breaking early release. This matters because a major AI lab is open-sourcing a core agent infrastructure tool, which could accelerate community innovation in AI agent development. The full traceability feature is particularly notable, as it offers an auditable event stream that commenters say US models do not provide. The harness uses Cordis v4, a hot-reload plugin system that can unload plugins and revert their side effects without restarting. Every run writes to an append-only session log covering system prompts, reasoning, tool calls, and subagent scheduling, enabling resume, fork, search, and replay operations.

hackernews · bjin · Aug 13, 12:58 · [Discussion](https://news.ycombinator.com/item?id=49285244)

**Background**: An AI agent harness is the software scaffolding around a language model that manages tools, memory, sandboxes, and feedback loops, turning a model into an agent. AI traceability refers to the ability to reconstruct how a model output was produced by linking data sources, prompts, model versions, and deployment context, which supports auditing and accountability. DeepSeek Harness appears to combine these concepts by providing a transparent, plugin-based runtime for agent workloads.

<details><summary>References</summary>
<ul>
<li><a href="https://harness-engineering.ai/blog/agent-harness-complete-guide/">The Complete Guide to Agent Harness: What It Is and Why It ...</a></li>
<li><a href="https://www.databricks.com/blog/ai-harness">What is an AI Agent Harness? | Databricks Blog</a></li>
<li><a href="https://data.world/blog/what-is-ai-traceability-benefits-tools-best-practices/">What is AI traceability? Benefits, tools &amp; best practices</a></li>

</ul>
</details>

**Discussion**: One author confirmed it is an early developer preview under MIT license and welcomed feedback. Commenters highlighted full traceability as a killer feature, especially compared to encrypted or obfuscated traces from US models, while others noted the plugin system resembles Cordis/Koishi and some expressed concern about plugin fatigue.

**Tags**: `#DeepSeek`, `#AI tools`, `#open-source`, `#developer tools`, `#tracing`

---

<a id="item-8"></a>
## [Gloomberb brings an open-source tiling terminal to financial data.](https://gloom.sh/) ⭐️ 8.0/10

Gloomberb, an open-source terminal-based financial terminal, has launched with a command-bar-first tiling UI that lets users type tickers or shortcuts like DES AAPL to jump directly into market views. It provides market data through an open-source stack but does not include Bloomberg&\#x27;s proprietary data connections. This matters because it brings a Bloomberg-like terminal experience into the open-source ecosystem, potentially lowering the barrier to sophisticated financial data tools for developers and retail traders. It reflects a growing demand for alternative terminal UIs in finance, even though it cannot replace Bloomberg&\#x27;s proprietary data. The tiling UI organizes panes into a non-overlapping layout, and the interface is command-bar first with shortcuts such as TOP. Some users have reported difficulty setting one pane to follow the ticker selected in another pane, and installation currently uses a curl script rather than a standard package manager.

hackernews · rbanffy · Aug 13, 13:52 · [Discussion](https://news.ycombinator.com/item?id=49285982)

**Background**: Gloomberb is a finance terminal that runs inside a user&\#x27;s terminal, inspired by the Bloomberg Terminal, a subscription-based financial software widely used by professionals. Bloomberg Terminal provides real-time market data, news, and analytics at a cost of about $31,980 per user per year. Gloomberb offers a similar command-driven, tiled interface using non-proprietary data sources, though it lacks Bloomberg&\#x27;s proprietary feeds. Tiling window managers, the design concept behind Gloomberb&\#x27;s UI, organize windows into a non-overlapping frame.

<details><summary>References</summary>
<ul>
<li><a href="https://gloom.sh/">Gloomberb</a></li>
<li><a href="https://github.com/gloom-sh/gloomberb">GitHub - gloom-sh/gloomberb: Finance terminal, in your ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Tiling_window_manager">Tiling window manager</a></li>

</ul>
</details>

**Discussion**: Commenters were generally intrigued but pointed out limitations: some questioned the curl-based installation and dependency handling, while others noted that Bloomberg&\#x27;s real value is its proprietary data, not the terminal UI. Several users found the tiling interface practical and easy to learn, though one struggled to link pane tickers, and another mentioned alternative terminals such as Godel Terminal.

**Tags**: `#terminal`, `#finance`, `#TUI`, `#open-source`, `#bloomberg`

---

<a id="item-9"></a>
## [DeepSeek V4 Pro 0813 Released with Open Weights on Hugging Face](https://simonwillison.net/2026/Aug/12/deepseek-v4-pro-0813/) ⭐️ 8.0/10

DeepSeek V4 Pro 0813 is now available via API on OpenRouter, and its open weights have been posted on Hugging Face with 1.7 trillion parameters \(893 GB\). The release arrived without an official announcement page from DeepSeek, making the OpenRouter listing and Hugging Face upload the primary access points. This is a major new open-weights release from DeepSeek, one of the most influential model developers in the open-weight space. The 1.7T-parameter model is likely to drive broad adoption in both API-based products and self-hosted deployments, continuing the industry trend of powerful open-weight models challenging closed offerings. The Hugging Face repository lists 1.7 trillion parameters and a 893 GB file size, making it one of the largest open-weight models yet. Benchmarks were initially shared in the official DeepSeek WeChat group, then copied to a Reddit post that moderators deleted for being low-effort, and finally reposted as an ASCII-art table on Hacker News; Simon Willison also noted unusually large output differences across low, medium, and high reasoning levels in his pelican rendering test.

rss · Simon Willison · Aug 12, 23:59

**Background**: Open-weight models allow anyone to download the trained weights and run inference locally, but they usually do not include the full training data and pipeline that true open-source AI would provide. DeepSeek has historically released its models with open weights, making them widely used by developers and researchers. OpenRouter is a unified API platform that lets users access hundreds of large language models from different providers through a single endpoint, which is why it often becomes the first practical way to try a new model before official documentation appears.

<details><summary>References</summary>
<ul>
<li><a href="https://openrouter.ai/models">Compare AI Models : Pricing, Context &amp; Benchmarks | OpenRouter</a></li>
<li><a href="https://www.pbs.org/newshour/science/whats-the-difference-between-closed-open%E2%80%91source-and-open-weight-ai-a-researcher-explains">What&#x27;s the difference between closed, open‑source and open-weight AI? A researcher explains | PBS News</a></li>
<li><a href="https://neysa.ai/blog/open-weights-open-source/">AI Models: Why Open Weights ≠ Open Source</a></li>

</ul>
</details>

**Discussion**: The community discussion is limited: the benchmark table was initially deleted from Reddit by moderators as low-effort, then shared on Hacker News as an ASCII-art table. Overall sentiment highlights the high impact of the release itself, though the lack of an official announcement and the scattered benchmark circulation drew some criticism.

**Tags**: `#AI`, `#DeepSeek`, `#model release`, `#open weights`, `#LLM`

---

<a id="item-10"></a>
## [Trump Signs Memo to Enlist Private Firms in Overseas Cyber Operations](https://www.bloomberg.com/news/articles/2026-08-13/trump-enlists-private-sector-to-boost-cyber-offensive-arsenal) ⭐️ 8.0/10

President Trump signed a memorandum that allows federally supervised private companies to conduct overseas surveillance and cyber attacks against foreign criminal networks targeting Americans. The Department of Homeland Security will administer the program in coordination with the Department of Justice. This is a significant policy shift that brings the private sector into US government-backed offensive cyber operations and surveillance, potentially expanding the nation&\#x27;s cyber arsenal while raising concerns about oversight and accountability. It could set a precedent for other countries and deepen the role of private companies in national security. Participating firms must maintain a performance bond or escrow of at least $1 million, which will be seized if they fail to meet contract terms. The program is directly controlled and supervised by the federal government, with DHS leading and the Justice Department coordinating oversight.

telegram · zaihuapd · Aug 13, 05:10

**Background**: Historically, offensive cyber operations and surveillance have been the domain of government agencies such as the National Security Agency and US Cyber Command. This memorandum marks a departure by authorizing private companies to act with federal endorsement, reflecting a broader trend of leveraging private-sector expertise in cybersecurity. However, it also raises novel legal and ethical questions about the boundaries of corporate participation in military-style operations.

**Tags**: `#cybersecurity`, `#government policy`, `#surveillance`, `#cyber warfare`, `#private sector`

---

<a id="item-11"></a>
## [DeepSeek Launches Open-Source Harness and V4-Pro-0813 Weights](https://mp.weixin.qq.com/s/mANdGRI4fO_sEbC1ECEoZQ) ⭐️ 8.0/10

DeepSeek released the open-source DeepSeek Harness application under the MIT license and made the DeepSeek-V4-Pro-0813 model weights available on Hugging Face. The harness adopts an &\#x27;everything is a plugin&\#x27; architecture and provides four operation modes: Standard, PTC, Minimal, and Creative. This release offers an open-source, model-agnostic alternative to the agent infrastructure behind tools like Claude Code and Codex, lowering barriers for developers to build custom agent harnesses. Open-sourcing the V4-Pro-0813 weights also advances model accessibility for the broader AI/ML community. DeepSeek Harness \(dsh\) is powered by Cordis, whose design is described in &\#x27;A Programming Paradigm for Spatiotemporal Composability.&\#x27; DeepSeek-V4-Pro-0813 is a mixture-of-experts model with a 1,048,576-token context window and a maximum output of 384,000 tokens; the Hugging Face page briefly returned a 404 before being restored.

telegram · zaihuapd · Aug 13, 12:39

**Background**: An agent harness is a software framework that orchestrates models, tools, and UI for building AI agents, similar to how a test harness orchestrates test execution. DeepSeek&\#x27;s approach treats every capability—models, tools, skills, sessions, sandboxes, storage, scheduling, and UI—as swappable plugins, enabling flexible recomposition. Mixture-of-experts \(MoE\) is an LLM architecture where different specialized sub-networks \(experts\) are activated per token, allowing large models to be more computationally efficient than dense models.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/deepseek-ai/deepseek-harness/tree/master">DeepSeek Harness - GitHub</a></li>
<li><a href="https://huggingface.co/multimodalart/DeepSeek-V4-Pro-0813">multimodalart/ DeepSeek - V 4 - Pro - 0813 · Hugging Face</a></li>
<li><a href="https://venturebeat.com/technology/deepseek-harness-launches-as-open-source-rival-to-claude-code-alongside-v4-pro-on-api-with-higher-prices">DeepSeek Harness launches as open source rival to Claude Code ...</a></li>

</ul>
</details>

**Tags**: `#DeepSeek`, `#LLM`, `#open-source`, `#AI`, `#model-release`

---