---
layout: default
title: "Horizon Summary: 2026-08-22 (ZH)"
date: 2026-08-22
lang: zh
---

> 从 30 条内容中筛选出 3 条重要资讯。

---

1. [SGLang v0.5.18 发布：710 个 PR 与新模型支持](#item-1) ⭐️ 8.0/10
2. [MCP 路线图：远程服务器转向 HTTP 并标准化智能体身份](#item-2) ⭐️ 8.0/10
3. [DelveRL：开源 Roguelike 游戏，专为训练游戏智能体设计](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [SGLang v0.5.18 发布：710 个 PR 与新模型支持](https://github.com/sgl-project/sglang/releases/tag/v0.5.18) ⭐️ 8.0/10

SGLang v0.5.18 已发布，包含来自 212 位贡献者的 710 个拉取请求。该版本新增了对 Muse Glimmer、SANA-Video、LTX-2.5 等模型的支持，并引入了重叠检查点暂存和 TP LMHead 全对全等性能优化。 此版本对 LLM 推理社区意义重大，因为它带来了重大性能提升并扩大了对自回归和扩散模型的支持。这些优化可将启动时间最多缩短 2.38 倍，并改善解码延迟，从而使生产部署受益。 关键细节包括：重叠检查点暂存使 Qwen3-32B 在 H100 上的启动速度提升 8.6%-11.7%；TP LMHead 全对全使得 DeepSeek-V4-Pro B200 上的 LMHead 时间从 320 微秒降至 169 微秒。该版本还将所有编译内核缓存整合到 SGLANG\_CACHE\_DIR 下，并将依赖升级至 torch 2.13.0、flashinfer 0.6.17 和 sgl-kernel 0.4.6.post1。

github · Fridge003 · 8月22日 00:09

**背景**: SGLang 是一个高性能的开源服务框架，用于大型语言模型和多模态模型的推理，由加州大学伯克利分校开发并由 LMSYS 托管。它利用 RadixAttention 实现 KV 缓存的自动重用，吞吐量最高可提升 6 倍。该框架同时支持自回归模型（如 LLaVA）和扩散模型，此版本还为 Qwen3.8、Ling-3.0、Nemotron 3.5 Lightning 和 DeepSeek-V4-Pro 等多个新系列添加了 cookbook 配方。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/sgl-project/sglang">GitHub - sgl-project/sglang: SGLang is a high-performance serving framework for large language models and multimodal models. · GitHub</a></li>
<li><a href="https://research.meta.ai/blog/introducing-muse-glimmer-open-agentic-model">Introducing Muse Glimmer: An Open Agentic Model That Runs on Your Device | Meta AI Research</a></li>
<li><a href="https://sanavideo.org/">Efficient Video Generation With Block Linear Diffusion Transformer</a></li>

</ul>
</details>

**标签**: `#LLM inference`, `#SGLang`, `#AI infrastructure`, `#open source`, `#release`

---

<a id="item-2"></a>
## [MCP 路线图：远程服务器转向 HTTP 并标准化智能体身份](https://blog.modelcontextprotocol.io/posts/mcp-roadmap/) ⭐️ 8.0/10

模型上下文协议（MCP）发布新路线图，将远程 MCP 服务器简化为标准 HTTP 工作负载，并标准化智能体身份与授权。这些变更计划在 2026-07-28 版本中落地。 MCP 已被主流 AI 提供商广泛采用，因此这次更新可能重塑智能体在远程工具上的身份验证与集成方式。将远程服务器视为普通 HTTP 工作负载，可降低构建和部署 MCP 端点的门槛。 该路线图摒弃了 MCP 最初用于远程服务器的专有协议，并提出一种标准化机制，让服务器能够识别和信任智能体身份，可能基于 OAuth 2.0 等现有标准构建。它还指出，当前依赖用户在浏览器中批准访问的授权方式，并不适合以云工作负载运行、或由子智能体代理行使的智能体。

hackernews · pentagrama · 8月22日 13:31 · [社区讨论](https://news.ycombinator.com/item?id=49399591)

**背景**: 模型上下文协议（MCP）是 Anthropic 于 2024 年 11 月推出的开放标准，旨在规范化 AI 系统连接外部工具和数据源的方式。可以把 MCP 想象成 AI 界的 USB-C 接口：它为大型语言模型提供了读取文件、调用函数和获取上下文的通用方式。该协议很快被 OpenAI、Google DeepMind 等提供商采纳。本路线图旨在解决远程部署和非交互式智能体调用者带来的发展痛点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol</a></li>
<li><a href="https://modelcontextprotocol.io/docs/2026-07-28/getting-started/intro">What is the Model Context Protocol (MCP)?</a></li>
<li><a href="https://www.ietf.org/archive/id/draft-klrc-aiagent-auth-00.html">AI Agent Authentication and Authorization - ietf.org</a></li>

</ul>
</details>

**社区讨论**: 社区反应不一。有评论者欢迎放弃专有协议，称最初的做法“愚蠢”；也有人质疑有多少服务器会真正实现新的身份标准，或认为 REST 加 skills.md 文件更简单。早期采用者对标准反复变动仍有不满，还有人开玩笑说 MCP 让人想起“主控制程序”（Master Control Program）。

**标签**: `#MCP`, `#AI`, `#Protocol`, `#Agents`, `#Developer Tools`

---

<a id="item-3"></a>
## [DelveRL：开源 Roguelike 游戏，专为训练游戏智能体设计](https://www.reddit.com/r/MachineLearning/comments/1vvii1j/i_built_an_opensource_roguelike_specifically_for/) ⭐️ 8.0/10

DelveRL 已开源，这是一款专为强化学习设计的确定性、程序生成的 roguelike 游戏。它包含结构化 API、批处理无渲染器环境，以及一个循环 PPO 基线，中位数可到达第 18 层。 DelveRL 解决了游戏与智能体训练框架集成这一常见痛点，提供了既可人类游玩又对智能体友好的环境。这有望降低 RL 研究人员在部分可观测、程序生成任务上做实验的门槛。 该游戏是一款无尽回合制 roguelike，智能体必须探索、管理资源与风险、战斗并逃离每层。所有组件均在本地运行，包括批处理无渲染器环境、循环 PPO 训练器、检查点、桥接文档和原始基准测试。

reddit · r/MachineLearning · /u/SnyderConsulting · 8月22日 17:32

**背景**: Roguelike 是一种以程序化关卡生成和永久死亡为特征的游戏类型，因此天然适合作为强化学习的试验场。基于 Gymnasium 等标准化的 RL 环境有助于将游戏与训练流程集成，但许多商业游戏难以对接。DelveRL 从一开始就被设计为对智能体友好，具有确定性模拟和结构化 API。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Delver">Delver - Wikipedia</a></li>
<li><a href="https://arxiv.org/html/2407.17032v4">Gymnasium: A Standardized Interface for Reinforcement ...</a></li>
<li><a href="https://github.com/pat-jj/harness-1">GitHub - pat-jj/harness-1: 🚀 Ultra Recipe for Training Long-Horizon Search Agents - matching frontier AI&#x27;s search capability with a 20B model + stateful harness</a></li>

</ul>
</details>

**标签**: `#Reinforcement Learning`, `#Open Source`, `#Game Environment`, `#Benchmark`, `#AI Agents`

---