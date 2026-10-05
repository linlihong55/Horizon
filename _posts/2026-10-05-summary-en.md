---
layout: default
title: "Horizon Summary: 2026-10-05 (EN)"
date: 2026-10-05
lang: en
---

> From 22 items, 1 important content pieces were selected

---

1. [ARC-AGI-3 Kaggle Scores Reportedly Jump From 7% to 56% in 30 Days](#item-1) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [ARC-AGI-3 Kaggle Scores Reportedly Jump From 7% to 56% in 30 Days](https://www.reddit.com/r/MachineLearning/comments/1wxcd4k/top_arc%CE%B1gi3_scores_on_kaggle_just_went_from_7_to/) ⭐️ 8.0/10

A Reddit post on r/MachineLearning claims that the top score on the ARC-AGI-3 Kaggle competition rose from roughly 7% to 56% over the past 30 days, apparently achieved by small local models running inside a harness rather than by frontier-scale systems. The poster notes that the leaderboard graphic they shared is slightly out of date. ARC-AGI-3 is deliberately designed to resist memorization and to expose the gap between current AI and human fluid reasoning, so a jump past average human performance would be a strong signal of rapid progress in interactive, agentic reasoning. That it reportedly came from small local models rather than giant frontier systems makes the result more surprising and more relevant to cost-sensitive and privacy-sensitive deployments. Kaggle rules for this competition restrict entrants to small local models, so much of the gain likely reflects harness and scaffolding engineering — search, retries, tool use and environment interaction — rather than raw model capability. A score of 100% on ARC-AGI-3 means an agent can beat every game as efficiently as humans, and the figure cited is from a Kaggle leaderboard rather than the officially verified ARC Prize leaderboard.

reddit · r/MachineLearning · /u/we\_are\_mammals · Oct 4, 10:24 · [Discussion](https://www.reddit.com/r/MachineLearning/comments/1wxcd4k/top_arc%CE%B1gi3_scores_on_kaggle_just_went_from_7_to/)

**Background**: ARC-AGI is a benchmark suite created under the ARC Prize effort \(associated with François Chollet\) that tests abstraction and reasoning on novel puzzles rather than learned knowledge. Its first two versions measured passive, single-shot reasoning, while ARC-AGI-3 is interactive: an agent must explore unfamiliar environments, infer goals on the fly, build adaptable world models and learn continuously — closer to how a human plays an unfamiliar video game. Kaggle hosts the competition with compute limits, which is why participants use small local models, and an &\#x27;eval harness&\#x27; is the scaffolding that lets a model act, observe feedback and iterate.

<details><summary>References</summary>
<ul>
<li><a href="https://arcprize.org/arc-agi/3">ARC-AGI-3</a></li>
<li><a href="https://arcprize.org/leaderboard">ARC-AGI-3 Leaderboard - ARC Prize</a></li>
<li><a href="https://deepeval.com/blog/what-is-an-eval-harness">Eval harness: What it is, how to use it, and why you should ...</a></li>

</ul>
</details>

**Tags**: `#ARC-AGI`, `#AI benchmarks`, `#Kaggle`, `#LLM reasoning`, `#AGI`

---