---
layout: default
title: "Horizon Summary: 2026-08-02 (EN)"
date: 2026-08-02
lang: en
---

> From 29 items, 3 important content pieces were selected

---

1. [Karpathy&\#x27;s 3D Scene Generation Benchmark Idea Sparks Debate](#item-1) ⭐️ 8.0/10
2. [eBay executives sentenced for harassment campaign, $56M payout](#item-2) ⭐️ 8.0/10
3. [Microsoft-led open letter defends open-weight AI models from restrictions](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Karpathy&\#x27;s 3D Scene Generation Benchmark Idea Sparks Debate](https://twitter.com/karpathy/status/2083749667410727319) ⭐️ 8.0/10

Andrej Karpathy tweeted that simple LLM tests like &\#x27;create an SVG of a pelican on a bicycle&\#x27; are being left behind, and proposed a tougher test: give Opus 5 the first paragraph of The Lord of the Rings with a 1M token budget \(~$10\) and ask for a three.js render. The tweet quickly ignited a community debate about whether 3D scene generation can serve as a meaningful benchmark for AI&\#x27;s understanding of the physical world. As one of the most influential voices in AI, Karpathy&\#x27;s suggestion shifts attention from static image generation to spatial, physics-aware scene generation as a new evaluation frontier. This debate could shape how future models are benchmarked, especially as capabilities progress beyond chatbots and 2D art. Karpathy specifically used the example of &\#x27;pelican on a bicycle&\#x27; to represent older, simpler tests, and proposed a 1M token budget \(about $10\) for a three.js code-generation task using The Lord of the Rings as input. Several commenters warned that a model producing good three.js code may simply reflect training on such code, not general physical understanding, and existing benchmarks like 3DGen-Bench are already attempting to formalize 3D generation evaluation.

hackernews · delichon · Aug 2, 04:05 · [Discussion](https://news.ycombinator.com/item?id=49140998)

**Background**: LLM benchmarking has long included simple generation tasks like creating SVGs, which test basic instruction-following but not deep world modeling. 3D scene generation, by contrast, requires a model to reason about spatial relationships, object permanence, and physical plausibility, making it a richer potential benchmark. Karpathy&\#x27;s tweet is part of a broader community search for next-generation benchmarks that better measure AI&\#x27;s understanding of the real world, and recent academic work like 3DGen-Bench is converging on similar ideas by evaluating text-to-3D and image-to-3D models with large-scale human preferences.

<details><summary>References</summary>
<ul>
<li><a href="https://x.com/karpathy/status/2083749667410727319">Andrej Karpathy on X: &quot;We&#x27;re starting to leave the territory where you ...</a></li>
<li><a href="https://arxiv.org/abs/2503.21745">[2503.21745] 3DGen-Bench: Comprehensive Benchmark Suite for 3D Generative Models</a></li>
<li><a href="https://arxiv.org/html/2503.21745v3">3DGen-Bench: Comprehensive Benchmark Suite for 3D Generative Models</a></li>

</ul>
</details>

**Discussion**: Commenters were broadly divided: some like jmugan defended the idea, arguing that imperfect 3D outputs are exactly the point because they expose physical-world understanding better than images. Others, like YmiYugy, worried that society&\#x27;s quality expectations have been lowered by AI content, and HarHarVeryFunny cautioned that strong three.js output may just be a training artifact, while bredren shared a concrete project using LLMs to build 3D animations from film scene descriptions.

**Tags**: `#AI`, `#Machine Learning`, `#Benchmarking`, `#3D Generation`, `#Karpathy`

---

<a id="item-2"></a>
## [eBay executives sentenced for harassment campaign, $56M payout](https://www.ft.com/content/06ec1b03-d4af-40cf-b12a-4ba5a410f6d2) ⭐️ 8.0/10

Federal judges sentenced seven former eBay security executives for orchestrating a harassment campaign against David and Ina Steiner, a couple who published a newsletter critical of eBay. The company agreed to pay $56 million to resolve related civil claims. This case marks a rare instance of corporate executives facing criminal charges for targeting online critics, underscoring the legal accountability of tech companies&\#x27; internal security teams. It sends a warning to companies that harassment of journalists and bloggers will have serious consequences. Among the sentences, Jim Baugh, former Senior Director of Safety and Security, received 57 months in prison; David Harville, former Director of Global Resiliency, received a lesser sentence; Brian Gilbert was sentenced to time served, one year supervised release, and a $20,000 fine. Seven members of eBay&\#x27;s security team, including former police captains, were involved in the campaign.

hackernews · JumpCrisscross · Aug 2, 19:19 · [Discussion](https://news.ycombinator.com/item?id=49147435)

**Background**: The case stems from a 2019 plot by eBay&\#x27;s security team to silence David and Ina Steiner, who published an online newsletter covering eBay sellers and often criticizing the company. Employees sent threatening and disturbing packages to the couple&\#x27;s home in Massachusetts, including a box of live cockroaches, a bloodied pig mask, and a funeral wreath. The harassment escalated to GPS tracking, surveillance, and even a social media campaign using the hashtag &\#x27;\#Crushthislady.&\#x27; The perpetrators intended to intimidate the Steiners into stopping their coverage.

**Discussion**: Commenters expressed skepticism that the harassment was limited to one couple, suggesting eBay may have targeted other critics. Some also wondered about the careers of the former police captains involved and whether broader investigations were conducted.

**Tags**: `#eBay`, `#corporate accountability`, `#harassment`, `#legal`, `#tech ethics`

---

<a id="item-3"></a>
## [Microsoft-led open letter defends open-weight AI models from restrictions](https://simonwillison.net/2026/Aug/2/open-letters/#atom-everything) ⭐️ 8.0/10

On July 24, 2026, Microsoft shepherded an open letter titled &quot;Open Weights and American AI Leadership,&quot; signed by 235 AI-adjacent companies including NVIDIA, Amazon, Y Combinator, The Linux Foundation, and later OpenAI, arguing against restrictions on open-weight AI models. On July 28, a separate letter, &quot;Pacing the Frontier,&quot; was published with signatures from 1,324 employees of frontier AI companies, requesting U.S. government support for international efforts to deliberately pace automated AI development. This marks a major industry alignment in the U.S. AI policy debate, with leading companies publicly opposing safety-driven restrictions on open-weight models. The split between Microsoft&\#x27;s coalition and Anthropic&\#x27;s more cautious stance, plus the unprecedented number of frontier AI employees calling for paced development, signals that regulation of open-source and frontier AI will be a defining issue for the industry. The Microsoft letter notably endorses distillation — training a model on outputs from other models — urging policymakers not to conflate it with misappropriation. Anthropic did not sign and three days later published its own position opposing bans but warning about authoritarian misuse and industrial-scale distillation; its CEO Dario Amodei also signed &quot;Pacing the Frontier.&quot;

rss · Simon Willison · Aug 2, 04:16

**Background**: Open-weight AI models are trained neural networks whose learned weights and biases are publicly released, allowing anyone to download and run them, though modification and redistribution depend on the license. Proponents argue this transparency enables scrutiny and broad access, while critics warn that unrestricted access could lead to misuse or concentration risks avoided by closed models. Distillation is a common technique in which one model is trained on the outputs of another, and it has become a contentious point in the open-weight debate.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Open-weight_model">Open-weight model</a></li>
<li><a href="https://www.microsoft.com/en-us/corporate-responsibility/topics/open-weight/">Open Weights and American AI Leadership</a></li>

</ul>
</details>

**Tags**: `#AI policy`, `#Open weights`, `#Microsoft`, `#AI regulation`, `#Open source`

---