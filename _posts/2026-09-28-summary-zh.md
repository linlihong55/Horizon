---
layout: default
title: "Horizon Summary: 2026-09-28 (ZH)"
date: 2026-09-28
lang: zh
---

> 从 23 条内容中筛选出 1 条重要资讯。

---

1. [「无法解释的失败」正在被常态化](#item-1) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [「无法解释的失败」正在被常态化](https://www.ihatethefuture.com/2026/09/the-normalization-of-inexplicable.html) ⭐️ 8.0/10

ihatethefuture.com 上一篇题为《无法解释的失败的常态化》的文章认为，软件行业正越来越习惯于容忍没人能解释的失败，而智能体与 LLM 辅助开发正在加速这一趋势。该文获得 246 分和约 100 条评论，成为近期讨论最热烈的可靠性批评之一。 如果无法解释的失败在面向用户的应用中被接受，这种容忍就可能蔓延到库、编译器和基础设施层，那里的不确定性会让每一次下游修复的成本都更高。这会侵蚀责任归属，拖慢整个生态，影响工程师、运维人员和最终用户。 文章区分了「无法解释」与「暂时未知」：核心问题在于「总有人为这个失败负责」这一预期正在消失，即便责任归属在制度上仍然明确。评论者补充说，LLM 的「置信度分数」是一种拟人化错觉，海森堡 bug 式的不可复现性让借助智能体的调试格外棘手，而 Nix 等可复现性工具加上严格的确定性，被提出作为应对手段。

hackernews · pxx · 9月27日 15:26 · [社区讨论](https://news.ycombinator.com/item?id=49867486)

**背景**: 智能体软件开发（agentic software development）指 AI 智能体在软件生命周期中自主地规划、生成、测试和修改代码；而 LLM 辅助开发（常被称为「氛围编程」vibe coding）则是开发者用自然语言描述任务、由模型生成代码。在这种模式下，可复现性与确定性——即相同输入得到相同结果的能力，通常借助 Nix 等工具强制执行——是缺陷可被调试的前提。所谓「海森堡 bug」（heisenbug）指的是在被观察时行为改变甚至消失的缺陷，名称借自海森堡不确定性原理，它正是文章所警告的那类不透明、无人负责的失败的典型代表。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Vibe_coding">Vibe coding - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Heisenbug">Heisenbug</a></li>
<li><a href="https://agenticse-book.github.io/pdf/AgenticSE_Book.pdf">Agentic</a></li>

</ul>
</details>

**社区讨论**: 评论者总体上认同文章观点。pmarreck 表示自己重视可复现性、确定性、测试和 Elixir 式的九个 9 可靠性，但在把该做的检查全做齐的前提下，仍觉得智能体辅助开发很有效率；adamddev1 则警告，一旦在库、基础设施和编译器层面把失败常态化，就会拖慢所有人和所有事。其他人指出失败的归属虽明确、对用户却是黑箱，并把「无法解释」的常态化与「无人负责」的常态化联系起来，还认为「置信度分数」暗示了一种算法根本不具备的拟人化含义。

**标签**: `#software reliability`, `#AI-assisted development`, `#debugging`, `#software engineering culture`, `#reproducibility`

---