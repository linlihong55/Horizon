---
layout: default
title: "Horizon Summary: 2026-10-05 (ZH)"
date: 2026-10-05
lang: zh
---

> 从 22 条内容中筛选出 1 条重要资讯。

---

1. [ARC-AGI-3 Kaggle 分数据称在 30 天内从 7% 跃升至 56%](#item-1) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [ARC-AGI-3 Kaggle 分数据称在 30 天内从 7% 跃升至 56%](https://www.reddit.com/r/MachineLearning/comments/1wxcd4k/top_arc%CE%B1gi3_scores_on_kaggle_just_went_from_7_to/) ⭐️ 8.0/10

Reddit 机器学习版块的一篇帖子声称，ARC-AGI-3 Kaggle 竞赛的最高分在过去 30 天内从约 7% 上升到了 56%，且据称这是由小型本地模型在某种 harness（评测框架）中运行实现的，而非依赖前沿规模的大模型。发帖人同时说明，他附上的排行榜截图略有滞后。 ARC-AGI-3 被刻意设计成难以靠记忆刷分，用来暴露当前 AI 与人类流体推理能力之间的差距，因此一旦分数超过人类平均水平，就意味着交互式、智能体式推理取得了快速进展。而据称这一成绩来自小型本地模型而非巨型前沿系统，更令人意外，也对关注成本与隐私的部署场景更具参考价值。 该 Kaggle 竞赛的规则限制参赛者只能使用小型本地模型，因此分数的提升很可能主要来自 harness 与脚手架工程（搜索、重试、工具调用和环境交互），而不是模型本身能力的提升。ARC-AGI-3 的 100% 分数意味着智能体能在每一款游戏上都以与人类相当甚至更高的效率通关，而帖子中引用的数字来自 Kaggle 排行榜，并非 ARC Prize 官方验证榜。

reddit · r/MachineLearning · /u/we\_are\_mammals · 10月4日 10:24 · [社区讨论](https://www.reddit.com/r/MachineLearning/comments/1wxcd4k/top_arc%CE%B1gi3_scores_on_kaggle_just_went_from_7_to/)

**背景**: ARC-AGI 是由 ARC Prize（与 François Chollet 相关）推出的基准测试系列，用全新的谜题考察抽象与推理能力，而不是考察模型记住的知识。前两个版本衡量的是被动的单次推理，而 ARC-AGI-3 是交互式的：智能体必须探索陌生环境、边玩边推断目标、构建可适应的世界模型并持续学习，更接近人类玩一款陌生电子游戏的过程。Kaggle 承办该竞赛并设有算力限制，因此参赛者只能使用小型本地模型；而所谓 harness（评测框架）就是让模型能够行动、观察反馈并反复迭代的脚手架代码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arcprize.org/arc-agi/3">ARC-AGI-3</a></li>
<li><a href="https://arcprize.org/leaderboard">ARC-AGI-3 Leaderboard - ARC Prize</a></li>
<li><a href="https://deepeval.com/blog/what-is-an-eval-harness">Eval harness: What it is, how to use it, and why you should ...</a></li>

</ul>
</details>

**标签**: `#ARC-AGI`, `#AI benchmarks`, `#Kaggle`, `#LLM reasoning`, `#AGI`

---