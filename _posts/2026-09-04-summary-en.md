---
layout: default
title: "Horizon Summary: 2026-09-04 (EN)"
date: 2026-09-04
lang: en
---

> From 33 items, 6 important content pieces were selected

---

1. [OpenAI Unveils GPT-6 Astra, Scoring 99.9% on ARC-AGI-3](#item-1) ⭐️ 10.0/10
2. [Developer Ports 1993 Amiga Assembly Game to Godot Using Claude LLM](#item-2) ⭐️ 8.0/10
3. [Go grandmaster Shin defeats AI KataGo with a two-stone handicap](#item-3) ⭐️ 8.0/10
4. [Audacity 4.0 Releases Qt6-Based Interface Amid Mixed Community Reactions](#item-4) ⭐️ 8.0/10
5. [Google Antigravity TOS Could Suspend Entire Accounts Over Third-Party AI Use](#item-5) ⭐️ 8.0/10
6. [US Government Backs OpenAI, Says AI Training Is Fair Use](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI Unveils GPT-6 Astra, Scoring 99.9% on ARC-AGI-3](https://openai.com/index/gpt-6-astra/) ⭐️ 10.0/10

OpenAI has announced GPT-6 Astra, a major new frontier model, reporting a 99.9% score on the ARC-AGI-3 benchmark and improvements across other evaluations. The company published a system card and began rolling out the model, with separate community discussions on the rollout, ARC-AGI-3 results, and coding-agent performance. A near-perfect ARC-AGI-3 score is significant because that benchmark tests agents&\#x27; ability to infer goals and learn rules in unfamiliar interactive environments, not just recall training data. If the result holds up, GPT-6 Astra could reset expectations for agentic AI rivalry among OpenAI, Google, Anthropic and other labs, and intensify debate over whether scaling still drives general intelligence. The 99.9% ARC-AGI-3 figure was measured with a Responses API harness, and commenters point out that applying the same harness to older models would considerably raise their reported scores. External trackers also highlighted GPT-6 Astra&\#x27;s gains on the Artificial Analysis Coding Agent Index, a composite of benchmarks such as DeepSWE, Terminal-Bench v2.1, and SWE-Atlas-QnA.

hackernews · kibae · Sep 3, 18:41 · [Discussion](https://news.ycombinator.com/item?id=49554643)

**Background**: ARC-AGI-3 is an interactive reasoning benchmark created by the ARC Prize community; agents must explore unfamiliar, abstract 2D game-like environments, infer goals, and learn from actions without explicit instructions, while older ARC versions measured passive fluid intelligence. Frontier models historically scored near zero or very low on ARC-AGI-3, while humans reliably solve the tasks. The related ongoing threads keep the model announcement separate from its evaluations, and the system card provides deployment details.

<details><summary>References</summary>
<ul>
<li><a href="https://arcprize.org/arc-agi/3">ARC-AGI-3</a></li>
<li><a href="https://arxiv.org/abs/2603.24621">ARC-AGI-3: A New Challenge for Frontier Agentic Intelligence ARC Prize - Leaderboard ARC-AGI-3 Leaderboard - llm-stats.com ARC-AGI-3: The New Interactive Reasoning Benchmark How enabling two settings tripled our scores on the ARC-AGI-3 ...</a></li>
<li><a href="https://artificialanalysis.ai/agents/coding-agents">AI Coding Agent Benchmarks &amp; Leaderboard | Artificial Analysis</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters were skeptical of the headline benchmark claim: intenex called the ARC-AGI-3 scorecard misleading because GPT-5.6 Sol&\#x27;s lower number was produced with a different harness, and abixb noted that aside from ARC-AGI-3, the gains resemble typical point-release improvements. Others questioned the framing of AI agents autonomously buying items in demos, and astrobiased argued the trajectory still resembles skill acquisition rather than the general intelligence François Chollet described.

**Tags**: `#OpenAI`, `#GPT-6`, `#AI research`, `#benchmarks`, `#large language models`

---

<a id="item-2"></a>
## [Developer Ports 1993 Amiga Assembly Game to Godot Using Claude LLM](https://babyloniantwins.com/blog/porting-a-1993-amiga-game-to-godot/) ⭐️ 8.0/10

A developer spent a single evening during a July holiday using Claude to port his 1993 Amiga game, written in MC68000 assembly, to the Godot engine. The LLM first reassembled the code with vasm until the binary was byte-identical to the original, then translated it into a working Godot port. This demonstrates a novel and powerful workflow: using LLMs to resurrect and modernize decades-old assembly-language games, preserving both gameplay and historical code. It suggests that retrocomputing preservation and porting projects can become dramatically faster and more accessible to original developers and hobbyists alike. The original shipped binaries were not clean assembler output but snapshots of already-running game memory saved by AsmOne, causing an initial 108-byte mismatch that the LLM had to account for. The developer spent several more weekends and evenings refining the game&\#x27;s feel, and is now releasing the original game for free.

hackernews · rabahs · Sep 3, 14:28 · [Discussion](https://news.ycombinator.com/item?id=49550375)

**Background**: The Amiga was a 1980s/90s personal computer known for custom graphics and sound, often programmed in assembly language to &\#x27;bang the hardware&\#x27; directly for speed. MC68000 assembly is the native instruction set of the Motorola 68000 CPU used in the Amiga. vasm is a portable and retargetable assembler commonly used to assemble 68000 code, while AsmOne was the original integrated assembler/editor environment the developer used in 1993. Godot is a modern open-source game engine, making this a translation from low-level legacy assembly to a high-level modern engine.

<details><summary>References</summary>
<ul>
<li><a href="http://sun.hasenbraten.de/vasm/">vasm portable and retargetable assembler</a></li>
<li><a href="https://aminet.net/package/dev/asm/ASM-One">Aminet - dev/asm/ASM-One.lha Asm One 1.02 Manual : Rune Gram-Madsen : Free Download ... Commodore Software - ASM-One v1.02 Manual Asm-One v1.20 by The Flame Arrows :: pouët.net ASM-One Macro Assembler - HandWiki Amiga Assembler Tutorial - Carl Henrik Asm One 1.02 Manual : Free Download, Borrow, and Streaming ...</a></li>
<li><a href="https://plugins.jetbrains.com/plugin/17268-mc68000-assembly-language-support">MC68000 Assembly Language Support - IntelliJ IDEs Plugin | Marketplace</a></li>

</ul>
</details>

**Discussion**: Commenters were enthusiastic and nostalgic: mattjoyce reported a similar success converting a ZX81 game binary to Go with Claude; btbuildem compared the game&\#x27;s aesthetic to &quot;Gods: Into the Wonderful&quot;; dannyobrien expressed awe at 1993 assembly development pre-Internet; hedgehog asked for an engineering guide from Claude Code; glimshe plans to port another forgotten game. Overall sentiment is admiration and excitement about LLM-assisted retro porting.

**Tags**: `#LLM`, `#Godot`, `#retrocomputing`, `#assembly`, `#code translation`

---

<a id="item-3"></a>
## [Go grandmaster Shin defeats AI KataGo with a two-stone handicap](https://www.kedglobal.com/artificial-intelligence/newsView/ked202607210007) ⭐️ 8.0/10

Go grandmaster Shin Jinse defeated AI KataGo despite a two-stone handicap, highlighting human strategic creativity against current AI systems.

hackernews · gmays · Sep 3, 01:11 · [Discussion](https://news.ycombinator.com/item?id=49544762)

**Tags**: `#Go`, `#Artificial Intelligence`, `#KataGo`, `#Human vs AI`, `#Game Strategy`

---

<a id="item-4"></a>
## [Audacity 4.0 Releases Qt6-Based Interface Amid Mixed Community Reactions](https://github.com/audacity/audacity/releases/tag/Audacity-4.0.0) ⭐️ 8.0/10

Audacity 4.0, a major release of the popular open-source audio editor, is now available, featuring a new Qt6-based interface and a range of fixes. The release marks a significant rewrite of the application&\#x27;s user interface after the version 3 series. Because Audacity is one of the most widely used free audio editors, this user-interface rewrite to Qt6 affects a large global user base and modernizes the aging codebase. The strong community reaction shows how important backend behavior, privacy, and workflow compatibility are to the project&\#x27;s future. The official release page highlights the new Qt6-based interface and various fixes, but the changelog does not address all long-standing complaints. Some users report that JACK/PipeWire backend integration remains awkward, and others express concern about cloud/telemetry features such as audio.com.

hackernews · ClydeN · Sep 3, 10:53 · [Discussion](https://news.ycombinator.com/item?id=49548395)

**Background**: Audacity is a long-established open-source audio editor used for recording and editing sound across Windows, macOS, and Linux. Qt is a cross-platform application framework used to build graphical interfaces; moving to Qt6 brings better performance, modern graphics, and improved hardware support. Audio backends are the low-level system APIs through which software actually plays and captures sound, such as JACK, PipeWire, PulseAudio, or WASAPI.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Qt_%28software%29">Qt (software) - Wikipedia</a></li>
<li><a href="https://extenly.com/2024/12/20/from-qtwidgets-to-qt6-and-beyond-what-is-qt-capable-of/">From QtWidgets to Qt6 and Beyond: What Is Qt Capable Of? – Extenly</a></li>
<li><a href="https://github.com/dechamps/FlexASIO/blob/master/BACKENDS.md">FlexASIO/BACKENDS.md at master · dechamps/FlexASIO</a></li>

</ul>
</details>

**Discussion**: Discussion is mixed: some users warmly recommend developer videos and praise the cleaner interface, while others say Audacity 4 still fails to address technical issues such as non-persistent JACK clients and awkward PipeWire behavior. Privacy-conscious commenters also ask about the post-telemetry forks Tenacity and Sneedacity, reflecting lingering distrust of Audacity&\#x27;s cloud and analytics features.

**Tags**: `#audacity`, `#open-source`, `#release`, `#qt6`, `#audio-editing`

---

<a id="item-5"></a>
## [Google Antigravity TOS Could Suspend Entire Accounts Over Third-Party AI Use](https://twitter.com/GergelyOrosz/status/2095453567955968398) ⭐️ 8.0/10

Google Antigravity&\#x27;s Terms of Service contain wording that suggests using the platform for third-party AI purposes could result in suspension of a user&\#x27;s entire Google account, not just the Antigravity service. A member of the Antigravity team, Varun Mohan, responded on X that the wording is confusing and will be updated to clarify that it refers only to the Antigravity account. This matters because many users rely on their Google accounts for email, calendars, government services, and other essential functions, so an account ban could have disproportionate consequences. The controversy highlights broader concerns about platform dependency, user-hostile account policies, and the importance of safe AI integration by major tech companies. The discussion originated from a tweet by Gergely Orosz, and community members noted that account bans are especially risky because users may be locked out of essential services and then have to battle automated support systems. Varun Mohan&\#x27;s response on X indicates that the official stance is that the terms refer to the Antigravity account, and the team plans to revise the ToS wording for clarity.

hackernews · tosh · Sep 3, 11:01 · [Discussion](https://news.ycombinator.com/item?id=49548452)

**Background**: Google Antigravity is a software development platform by Google that includes a chat-oriented development environment, an integrated development environment \(IDE\), a command-line interface \(CLI\), and a software development kit \(SDK\) for orchestrating autonomous AI agents in coding tasks. The concern emerges from the coupling of this new AI product to a broad Google identity, which means a violation of one product&\#x27;s terms could theoretically lead to suspension of unrelated services. This situation mirrors wider industry debates about how AI products interact with existing platform accounts and the need for clear, proportional enforcement policies.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Google_Antigravity">Google Antigravity</a></li>
<li><a href="https://antigravity.google/">Google Antigravity</a></li>

</ul>
</details>

**Discussion**: Commenters expressed strong disapproval, describing account-wide bans as &\#x27;wildly user hostile&\#x27; and warning about the difficulty of reaching human support or recovering years of emails and calendars. Some drew parallels to European eID systems requiring Apple/Google accounts, arguing that platform bans can lock users out of government services. A few acknowledged Antigravity team&\#x27;s clarification but maintained that the original ambiguity itself damages trust in Google AI products.

**Tags**: `#Google`, `#Antigravity`, `#Terms of Service`, `#AI policy`, `#Account suspension`

---

<a id="item-6"></a>
## [US Government Backs OpenAI, Says AI Training Is Fair Use](https://www.reuters.com/legal/litigation/us-government-backs-openai-new-york-times-copyright-case-2026-09-02/) ⭐️ 8.0/10

The U.S. government filed an amicus brief in a Manhattan federal court supporting OpenAI in its copyright dispute with The New York Times, arguing that using copyrighted material to train large language models generally qualifies as fair use. It is the first time the U.S. government has publicly taken a position in an AI-training copyright case. Although the brief is not legally binding, it may strengthen the confidence of AI companies defending against copyright lawsuits and influence how courts and regulators view AI training. The case has become a landmark battle over whether unlicensed use of copyrighted works to train AI violates the law, affecting both AI developers and content creators. The New York Times sued OpenAI and Microsoft in 2023, accusing them of using millions of its articles without permission to train ChatGPT. The Times criticized the U.S. government for siding with &\#x27;trillion-dollar AI companies&\#x27; at the expense of creators&\#x27; rights.

telegram · zaihuapd · Sep 3, 05:45

**Background**: Fair use is a U.S. legal doctrine that allows limited unlicensed use of copyrighted works for purposes such as criticism, commentary, news reporting, teaching, or research. An amicus curiae \(&\#x27;friend of the court&\#x27;\) brief is filed by someone who is not a party to the case to offer additional legal perspective, and courts may consider it even though it is not binding. This lawsuit is one of the most prominent tests of whether the massive ingestion of copyrighted content to build generative AI systems constitutes infringement, with broad implications for the future of AI development.

**Tags**: `#AI`, `#Copyright`, `#Legal`, `#OpenAI`, `#Fair Use`

---