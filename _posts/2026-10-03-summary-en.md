---
layout: default
title: "Horizon Summary: 2026-10-03 (EN)"
date: 2026-10-03
lang: en
---

> From 31 items, 4 important content pieces were selected

---

1. [New AI Beats Top Human Stratego Player Using Far Less Training](#item-1) ⭐️ 8.0/10
2. [Greg Kroah-Hartman Critiques LLM-Generated Security Bug Reports in the LLM Age](#item-2) ⭐️ 8.0/10
3. [Zig v0.17.0 Release Notes Drop, With a Pragmatic Shift on LLMs](#item-3) ⭐️ 8.0/10
4. [arXiv caps submissions at two papers per month from October 1](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [New AI Beats Top Human Stratego Player Using Far Less Training](https://arstechnica.com/science/2026/10/ai-finally-beat-the-best-stratego-player-in-history-and-did-it-on-a-budget/) ⭐️ 8.0/10

A new AI system, described in a Nature paper with a corresponding arXiv preprint, has become the first to defeat the best human Stratego player in history, and it did so on a comparatively small budget. According to the report, the algorithm learned roughly 34 times more efficiently than DeepMind&\#x27;s DeepNash, playing far fewer games while ending up much stronger. Stratego is a classic hard case for AI because it is an imperfect-information game, where players cannot see the opponent&\#x27;s piece identities, so the brute-force lookahead search that conquered chess and Go breaks down. A method that learns this efficiently on a budget suggests more practical paths to decision-making under hidden information, which is closer to real-world problems like negotiation, security, and strategic planning than perfect-information board games. The reported efficiency gain is roughly 34x fewer games than DeepNash, which DeepMind introduced in a 2022 paper titled &\#x27;Mastering the Game of Stratego with Model-Free Multiagent Reinforcement Learning&\#x27;. The work therefore also reframes that earlier headline claim, since the 2022 system apparently did not yet clearly surpass top human play, whereas the new approach reportedly does.

hackernews · PaulHoule · Oct 2, 14:11 · [Discussion](https://news.ycombinator.com/item?id=49933740)

**Background**: In game theory, a game has &\#x27;perfect information&\#x27; when every player can see all relevant state — as in chess or Go. Stratego is instead an imperfect-information game: each side&\#x27;s 40 pieces look identical from the opponent&\#x27;s view, their ranks are hidden, and only combat outcomes gradually reveal information. This hidden state means a player cannot simply search ahead, because the value of a move depends on facts they cannot observe, which is why the problem resisted strong AI play for so long.

<details><summary>References</summary>
<ul>
<li><a href="https://www.deeplearning.ai/the-batch/deepnash-the-rl-system-that-plays-stratego-like-a-master">DeepNash, the RL System That Plays Stratego like a Master</a></li>
<li><a href="https://en.wikipedia.org/wiki/Perfect_information">Perfect information - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters largely agreed that hidden information is the crux: as one put it, you would like to search ahead with &\#x27;if I do this they will do that,&\#x27; but that is impossible when you don&\#x27;t even know what the opponent&\#x27;s pieces are, so the 34x learning efficiency is the key contribution. Others noted nostalgia for the physical board game, recalled the 2022 DeepNash paper and argued its &\#x27;mastering&\#x27; claim should now be seen as not quite there, and joked about cheating methods such as subtly marked pieces or asking a chatbot to disprove hard problems.

**Tags**: `#AI`, `#reinforcement-learning`, `#imperfect-information-games`, `#game-playing`, `#research`

---

<a id="item-2"></a>
## [Greg Kroah-Hartman Critiques LLM-Generated Security Bug Reports in the LLM Age](https://www.youtube.com/watch?v=NnV_cWeoo5Q) ⭐️ 8.0/10

In a Kernel Recipes 2026 talk titled &quot;Security in the LLM Age,&quot; Linux kernel maintainer Greg Kroah-Hartman dissected Anthropic&\#x27;s claim that its Mythos model &quot;found&quot; 79 kernel vulnerabilities, showing that 24 had no detail beyond &quot;something crashed,&quot; 14 were not bugs at all, 3 were based on made-up data, and 15 were already fixed in the latest release. Only about 20 required actual fixes, which he characterized as amounting to roughly one hour of kernel development work. This is one of the most direct public rebuttals of AI vendors&\#x27; security marketing by a top-tier open-source maintainer, and it matters because downstream distributions, security teams, and maintainers increasingly have to triage AI-generated vulnerability reports. It also raises broader questions about whether sensationalized &quot;AI finds zero-days&quot; claims are outrunning the evidence, and about credit and citation norms in open-source security work. According to the talk \(as summarized by attendees\), Mythos essentially pattern-matched decades of prior kernel patches and re-applied those patterns elsewhere to see whether the same class of fix had been applied universally, and among the fixes that were genuinely needed, several merely &quot;assume a malicious filesystem image&quot; or local injection privileges. Kroah-Hartman also noted that Anthropic did not cite the kernel developers who originally authored the patches for those issues, while the web coverage of Mythos focuses on separate claims such as autonomously finding a 27-year-old OpenBSD bug at a token cost of around $20,000.

hackernews · usernomdeguerre · Oct 2, 02:51 · [Discussion](https://news.ycombinator.com/item?id=49929391)

**Background**: Greg Kroah-Hartman is the long-time maintainer of the Linux kernel&\#x27;s stable branches and one of the most senior figures in kernel development, so his assessment of vulnerability reports carries unusual weight. &quot;Kernel Recipes&quot; is a French technical conference where kernel developers discuss low-level work. LLM-based vulnerability discovery is the emerging practice of prompting or fine-tuning large language models to scan source code and propose CVEs \(Common Vulnerabilities and Exposures, the standard identifiers for publicly disclosed security flaws\). The episode connects to the long-standing open-source argument that &quot;many eyes&quot; make bugs shallow — a claim that AI vendors now use to argue models can outperform human reviewers.

<details><summary>References</summary>
<ul>
<li><a href="https://venturebeat.com/security/mythos-detection-ceiling-security-teams-new-playbook">Anthropic&#x27;s Mythos finds 27-year-old bug | VentureBeat</a></li>
<li><a href="https://www.bymachine.news/anthropic-mythos-vulnerability-discovery-security-crisis">Mythos Found 27-Year-Old Bug Humans Missed Completely</a></li>
<li><a href="https://undercodetesting.com/mythos-ai-just-found-a-27-year-old-bsd-bug-why-human-researchers-kept-it-secret-for-decades-video/">Mythos AI Just Found a 27-Year-Old BSD Bug: Why Human ...</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters largely welcomed Kroah-Hartman&\#x27;s bluntness, with several quoting his slide breakdown and one noting that the whole &quot;79 bugs&quot; marketing push reduced to an hour of kernel work, calling the dissonance with AI-safety messaging &quot;stark.&quot; Others highlighted that Anthropic did not credit the kernel developers who originally fixed those CVEs — the same citation problem OpenAI has had. A more forward-looking view argued the criticism does not mean AI is useless here, and that specialized models trained on kernel specifics and coding standards could still make bug discovery and fixing much faster and more accurate.

**Tags**: `#LLM security`, `#Linux kernel`, `#AI vulnerability research`, `#open source`, `#Anthropic`

---

<a id="item-3"></a>
## [Zig v0.17.0 Release Notes Drop, With a Pragmatic Shift on LLMs](https://ziglang.org/download/0.17.0/release-notes.html) ⭐️ 8.0/10

The Zig project published the full release notes for version 0.17.0, a substantial documentation drop that hit 209 upvotes and 132 comments on Hacker News. The notes and surrounding discussion highlight a new pragmatic stance on using LLMs to discover compiler and language bugs — reportedly inspired by results from SQLite — alongside continued expansion of Zig&\#x27;s target and cross-compilation support. Zig is one of the fastest-rising systems programming languages, so each release shapes how low-level developers think about replacing C. The shift toward accepting LLM-assisted bug hunting is notable because the project had previously taken a hard line against AI-generated contributions, and that policy change could influence how other open-source language projects handle AI tooling. Zig is still pre-1.0, so 0.17.0 is a moving target with breaking changes and a relatively small ecosystem, even as its design and tooling mature. Community members singled out two features they most want next: a new stackless coroutine IO implementation and first-class fuzzer tooling.

hackernews · ErenayDev · Oct 2, 20:56 · [Discussion](https://news.ycombinator.com/item?id=49938521)

**Background**: Zig is a general-purpose systems programming language and toolchain designed as a general-purpose improvement on C, created by Andrew Kelley and first announced in 2016. It avoids macros and preprocessor directives, requires manual memory management, and adds compile-time generics and reflection over types, plus low-level features such as packed structs, arbitrary-width integers, and multiple pointer types. Development is funded by the Zig Software Foundation through corporate sponsorships and donations, and the language is released under an MIT license. Because Zig is pre-1.0, maintainers publish long, detailed release notes with each tagged version to document behavioral and toolchain changes.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Zig_%28programming_language%29">Zig (programming language)</a></li>
<li><a href="https://ziglang.org/">Home Zig Programming Language</a></li>

</ul>
</details>

**Discussion**: Sentiment was largely positive: one long-time polyglot developer called Zig the best-designed language they had tried, and another praised its target support as perhaps the only language that competes with C on that front. Commenters welcomed the pragmatic turn on LLMs while also raising a sharp counterpoint — one user said they left the Zig ecosystem for Odin because of hostile behavior from core team members toward humans, not just LLMs, and others asked how the project is doing overall given its earlier hard line against AI.

**Tags**: `#zig`, `#programming-languages`, `#systems-programming`, `#compilers`, `#release-notes`

---

<a id="item-4"></a>
## [arXiv caps submissions at two papers per month from October 1](https://www.huxiu.com/article/4895127.html) ⭐️ 8.0/10

arXiv, the world&\#x27;s largest preprint platform, will limit every submitter to a maximum of two papers per calendar month starting October 1, covering all disciplines including computer science, mathematics and physics, with rejected manuscripts still counting against the monthly quota. The change follows a record 40,363 submissions in September — a 35-year high — with AI-category papers growing more than sixfold in two years. The policy directly constrains how fast the global research community — especially AI and machine learning — can circulate new work, since arXiv has become the de facto first stop for pre-publication results. It is a strong signal that major academic infrastructure is being forced to ration access because of the flood of low-quality, AI-generated manuscripts straining human moderation. The cap applies per actual submitter rather than per paper, so co-authors of a multi-author paper are unaffected and can still submit their own work elsewhere in the same month. No discipline is exempt, and because rejected papers still consume quota, authors cannot simply re-submit repeatedly within a month.

telegram · zaihuapd · Oct 2, 06:21

**Background**: A preprint is a version of a scholarly paper that is posted publicly before formal peer review and journal publication, allowing researchers to share results early and claim priority. arXiv, launched 35 years ago and now run out of Cornell University, is the dominant preprint server for physics, mathematics and computer science. Unlike journals, arXiv performs only a light screening rather than full peer review, and that screening is done by a limited pool of human moderators. The rise of generative AI, alongside commercial &\#x27;paper mills&\#x27; that sell low-quality or fabricated manuscripts, has made it increasingly hard for such volunteer-based moderation to keep pace.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Preprint">Preprint - Wikipedia</a></li>
<li><a href="https://casrai.org/guides/preprint-servers-explained">Preprint Servers Explained: What &amp; How — CASRAI</a></li>
<li><a href="https://journals.plos.org/plosbiology/article/file?id=10.1371/journal.pbio.3002931&amp;type=printable">A call for research to address the threat of paper mills</a></li>

</ul>
</details>

**Tags**: `#arXiv`, `#academic-publishing`, `#AI-research`, `#preprints`, `#research-policy`

---