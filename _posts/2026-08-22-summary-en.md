---
layout: default
title: "Horizon Summary: 2026-08-22 (EN)"
date: 2026-08-22
lang: en
---

> From 30 items, 3 important content pieces were selected

---

1. [SGLang v0.5.18 Released with 710 PRs and New Model Support](#item-1) ⭐️ 8.0/10
2. [MCP Roadmap Moves Remote Servers to HTTP, Adds Agent Identity](#item-2) ⭐️ 8.0/10
3. [DelveRL: An Open-Source Roguelike for Training Game-Playing Agents](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [SGLang v0.5.18 Released with 710 PRs and New Model Support](https://github.com/sgl-project/sglang/releases/tag/v0.5.18) ⭐️ 8.0/10

SGLang v0.5.18 was released with 710 pull requests from 212 contributors. It adds support for new models including Muse Glimmer, SANA-Video, LTX-2.5, and others, plus performance optimizations like overlapped checkpoint staging and TP LMHead with all-to-all. This release is significant for the LLM inference community because it brings major performance improvements and broadens support for both autoregressive and diffusion models. The optimizations can reduce startup time by up to 2.38x and improve decode latency, benefiting production deployments. Key details include overlapped checkpoint staging that speeds Qwen3-32B startup by 8.6-11.7% on H100, and TP LMHead with all-to-all reducing LMHead time from 320us to 169us on DeepSeek-V4-Pro B200. The release also consolidates all compiled-kernel caches under SGLANG\_CACHE\_DIR and upgrades dependencies to torch 2.13.0, flashinfer 0.6.17, and sgl-kernel 0.4.6.post1.

github · Fridge003 · Aug 22, 00:09

**Background**: SGLang is a high-performance open-source serving framework for large language models and multimodal models, developed by UC Berkeley and hosted by LMSYS. It uses RadixAttention for automatic KV cache reuse, achieving up to 6x higher throughput. The framework supports both autoregressive models like LLaVA and diffusion models, and this release adds cookbook recipes for several new families including Qwen3.8, Ling-3.0, Nemotron 3.5 Lightning, and DeepSeek-V4-Pro.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/sgl-project/sglang">GitHub - sgl-project/sglang: SGLang is a high-performance serving framework for large language models and multimodal models. · GitHub</a></li>
<li><a href="https://research.meta.ai/blog/introducing-muse-glimmer-open-agentic-model">Introducing Muse Glimmer: An Open Agentic Model That Runs on Your Device | Meta AI Research</a></li>
<li><a href="https://sanavideo.org/">Efficient Video Generation With Block Linear Diffusion Transformer</a></li>

</ul>
</details>

**Tags**: `#LLM inference`, `#SGLang`, `#AI infrastructure`, `#open source`, `#release`

---

<a id="item-2"></a>
## [MCP Roadmap Moves Remote Servers to HTTP, Adds Agent Identity](https://blog.modelcontextprotocol.io/posts/mcp-roadmap/) ⭐️ 8.0/10

The Model Context Protocol announced a new roadmap that simplifies remote MCP servers to standard HTTP workloads and standardizes agent identity and authorization. The changes are targeted for the 2026-07-28 release. MCP is widely adopted by major AI providers, so this update could reshape how agents authenticate and integrate with remote tools. Treating remote servers as ordinary HTTP workloads lowers the barrier to building and deploying MCP endpoints. The roadmap moves away from the bespoke protocol MCP initially used for remote servers, and proposes a standardized way for servers to recognize and trust agent identities, likely built on existing standards such as OAuth 2.0. It also notes that current authorization, which relies on a person approving access in a browser, does not fit agents running as cloud workloads or sub-agents with delegated authority.

hackernews · pentagrama · Aug 22, 13:31 · [Discussion](https://news.ycombinator.com/item?id=49399591)

**Background**: The Model Context Protocol \(MCP\) is an open standard introduced by Anthropic in November 2024 to standardize how AI systems connect to external tools and data sources. Think of MCP as a USB-C port for AI: it gives large language models a common way to read files, call functions, and access context. The protocol was quickly adopted by providers such as OpenAI and Google DeepMind. This roadmap addresses growing pains around remote deployment and non-interactive agent callers.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol</a></li>
<li><a href="https://modelcontextprotocol.io/docs/2026-07-28/getting-started/intro">What is the Model Context Protocol (MCP)?</a></li>
<li><a href="https://www.ietf.org/archive/id/draft-klrc-aiagent-auth-00.html">AI Agent Authentication and Authorization - ietf.org</a></li>

</ul>
</details>

**Discussion**: Community reaction is mixed. One commenter welcomes the move off a bespoke protocol, calling the original approach &\#x27;bone-headed,&\#x27; while others question how many servers will actually implement the new identity standards or argue that REST plus a skills.md file is simpler. There is also lingering frustration from early adopters over pivoting standards, plus a joke about MCP recalling the &\#x27;Master Control Program.&\#x27;

**Tags**: `#MCP`, `#AI`, `#Protocol`, `#Agents`, `#Developer Tools`

---

<a id="item-3"></a>
## [DelveRL: An Open-Source Roguelike for Training Game-Playing Agents](https://www.reddit.com/r/MachineLearning/comments/1vvii1j/i_built_an_opensource_roguelike_specifically_for/) ⭐️ 8.0/10

DelveRL, a deterministic, procedurally generated roguelike built specifically for reinforcement learning, has been open-sourced. It includes a structured API, batched renderer-free environments, and a recurrent PPO baseline that reaches a median floor of 18. DelveRL addresses the common pain point of integrating games with agent training harnesses, providing a human-playable but agent-friendly environment. This could lower the barrier for RL researchers to experiment with partially observable, procedurally generated tasks. The game is an endless turn-based roguelike where agents must explore, manage resources and risk, fight enemies, and escape each floor. All components run locally, including batched renderer-free environments, a recurrent PPO trainer, checkpoints, bridge documentation, and raw benchmarks.

reddit · r/MachineLearning · /u/SnyderConsulting · Aug 22, 17:32

**Background**: Roguelikes are a game genre characterized by procedural level generation and permanent death, making them natural testbeds for reinforcement learning. Standardized RL environments, such as those based on Gymnasium, help integrate games with training pipelines, but many commercial games are difficult to interface with. DelveRL was designed from the ground up to be agent-friendly, with deterministic simulation and a structured API.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Delver">Delver - Wikipedia</a></li>
<li><a href="https://arxiv.org/html/2407.17032v4">Gymnasium: A Standardized Interface for Reinforcement ...</a></li>
<li><a href="https://github.com/pat-jj/harness-1">GitHub - pat-jj/harness-1: 🚀 Ultra Recipe for Training Long-Horizon Search Agents - matching frontier AI&#x27;s search capability with a 20B model + stateful harness</a></li>

</ul>
</details>

**Tags**: `#Reinforcement Learning`, `#Open Source`, `#Game Environment`, `#Benchmark`, `#AI Agents`

---