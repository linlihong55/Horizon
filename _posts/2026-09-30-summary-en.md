---
layout: default
title: "Horizon Summary: 2026-09-30 (EN)"
date: 2026-09-30
lang: en
---

> From 41 items, 4 important content pieces were selected

---

1. [OpenAI launches GPT-6.1 Sol: near-Astra smarts at one-fifth the price](#item-1) ⭐️ 9.0/10
2. [OpenAI DevDay 2026: Dots always-on agents plus 20+ launches](#item-2) ⭐️ 9.0/10
3. [Privacy Analysis Finds Web and Mobile AI Chat Agents Leak Data](#item-3) ⭐️ 8.0/10
4. [OpenAI launches Dots, always-on cloud agents for work](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI launches GPT-6.1 Sol: near-Astra smarts at one-fifth the price](https://openai.com/index/introducing-gpt-6-1-sol/) ⭐️ 9.0/10

OpenAI announced GPT-6.1 Sol, an upgrade to GPT-6 Sol that it says delivers near-GPT-6 Astra performance on agentic coding, computer use and professional work while costing only one-fifth of Astra&\#x27;s standard input and output price, with cached input at $0.10 per million tokens. The model is rolling out to Plus, Pro, Business, Enterprise and Edu users in ChatGPT. The release pushes near-frontier capability into a much cheaper tier, signaling that token price rather than raw benchmark scores is becoming the main competitive battleground among frontier labs. This pressures rivals such as Anthropic on cost and could accelerate the commoditization of high-end reasoning models for heavy agentic and coding workloads. OpenAI says GPT-6.1 Sol scores 2.2 percentage points above Opus 5.5 on AutomationBench, which measures whether agents correctly complete multi-step business workflows, at medium reasoning effort and roughly a third of the cost. Its cached input pricing is 95% below standard input pricing and 50% below GPT-6 Sol&\#x27;s cached input pricing.

hackernews · crorella · Sep 29, 17:06 · [Discussion](https://news.ycombinator.com/item?id=49896586)

**Background**: GPT-6 Astra is OpenAI&\#x27;s top-tier frontier model, released in September 2026 and described by company president Greg Brockman as a &quot;generational leap&quot; that could eventually be seen as the arrival of artificial general intelligence \(AGI\). Within that lineup, the Sol models form a cheaper tier aimed at complex coding and agentic workflows rather than maximum general capability. Cached input pricing refers to a discount applied when an LLM reuses previously processed prompt prefixes, which is common in coding agents that resend large, mostly unchanged contexts.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/introducing-gpt-6-1-sol/">Introducing GPT-6.1 Sol | OpenAI</a></li>
<li><a href="https://developers.openai.com/api/docs/models/gpt-6.1-sol">GPT-6.1 Sol Model | OpenAI API</a></li>
<li><a href="https://www.axios.com/2026/09/03/openai-astra-gpt-6-agi-brockman">OpenAI releases new model GPT-6 Astra, says it may represent AGI</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters were largely skeptical: several reported that GPT-6 Sol was a regression, with one long-time OpenAI/Codex fan saying they switched exclusively to Opus 5.5, and others speculated that GPT-6.1 Sol is a last-minute panic rename of a leaked &quot;Astra-Minor&quot; model released just days after Sol 6. One commenter argued the real headline is the 50% cheaper cache, while another worried that price becoming the main battleground is ominous for the industry and investors, and a third said DeepSeek is cheap and fast enough that being six months behind the frontier is acceptable on a bang-for-buck basis.

**Tags**: `#AI`, `#OpenAI`, `#LLM`, `#model-release`, `#pricing`

---

<a id="item-2"></a>
## [OpenAI DevDay 2026: Dots always-on agents plus 20+ launches](https://openai.com/zh-Hant/index/devday-2026-recap/) ⭐️ 9.0/10

At its 2026 DevDay, OpenAI unveiled more than 20 updates, headlined by Dots, an always-on companion agent that autonomously runs around the clock, learns user habits, and proactively takes over long-running complex work. Other releases include GPT-6.1 Sol for coding and computer control at roughly one-fifth the price with near-Astra intelligence, Astra Ultrafast running up to 8x faster \(6x via API\), Codex in the cloud with voice control and automatic debugging, an Agents API with native computer control and AWS Bedrock hosting, a lightweight Decisions API for real-time classification and routing, &quot;Sign in with ChatGPT&quot; subscription sharing with tools like Devin and Notion, and a new Pro 500 tier with 25x the compute of Plus. The launch signals that OpenAI is betting on persistent, always-on agents rather than chat sessions as the next interface for AI work, directly competing with rivals such as Meta&\#x27;s Muse. Bundling agent APIs, subscription portability, and tiered compute pricing into one event also reshapes how developers build and pay for agentic products on the OpenAI stack. GPT-6.1 Sol is positioned below the flagship GPT-6 Astra in OpenAI&\#x27;s model lineup, is not yet available in ChatGPT, and is reachable only through the API as gpt-6.1-sol; Astra Ultrafast in Codex is up to 8x faster than Astra Standard and 4x faster than Astra Fast. Dots can be provisioned with specific identities, credentials, and tools through existing systems, and OpenAI is already working with Microsoft to integrate them into Agent 365.

telegram · zaihuapd · Sep 29, 17:52

**Background**: OpenAI&\#x27;s GPT-6 family, launched in July 2026, comes in tiers ranked from least to most capable: Luna, Terra, Sol, and the flagship Astra, so &quot;Sol&quot; denotes a mid-tier model line that OpenAI iterates on with point releases like 6.1. &quot;Agents&quot; in this context means AI systems that can plan and execute multi-step tasks on their own, including controlling a computer, rather than just answering questions in a chat window. Dots are OpenAI&\#x27;s answer to that trend, positioned as always-on assistants rather than episodic chatbots, and they arrive weeks after Meta released its competing Muse agents.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/introducing-dots/">Introducing dots - OpenAI</a></li>
<li><a href="https://openai.com/index/introducing-gpt-6-1-sol/">Introducing GPT - 6 . 1 Sol | OpenAI</a></li>
<li><a href="https://techcrunch.com/2026/09/29/openai-launches-dots-its-bubbly-agentic-avatar/">OpenAI launches Dots, its bubbly agentic avatar - TechCrunch</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#AI Agents`, `#GPT-6.1`, `#Developer Conference`, `#API`

---

<a id="item-3"></a>
## [Privacy Analysis Finds Web and Mobile AI Chat Agents Leak Data](https://jorgegarciaherrero.com/wp-content/interactivos/20260916-Prompt-like-a-butterfly-sting-like-a-tracker-%28clean%29.pdf) ⭐️ 8.0/10

A new paper titled &quot;Prompt-like-a-butterfly, sting-like-a-tracker&quot; presents a privacy analysis of conversational AI agents on both web and mobile platforms, examining how these agents handle user data and tracking. The work was surfaced alongside a Hacker News discussion that reached 408 points and 130 comments, in which users reported concrete leakage behavior such as ChatGPT sending unfinished prompts to a \`conversation/prepare\` endpoint before the user hits send. Conversational AI agents are now used for sensitive drafting and research work, so evidence that prompts and partial prompts leak through tracking or pre-fetching undermines the assumption that these sessions are private. The findings matter to everyday users, enterprises evaluating AI assistants, and platform vendors who may face regulatory scrutiny over data collection in chat interfaces. The discussion highlights that prompt pre-fetching to endpoints such as \`conversation/prepare\` may let providers observe writing cadence, error-correction style, and half-formed ideas as they develop. Commenters also note that some services treat a UUID in the URL as sufficient privacy protection, even though sharing such a link can expose an entire conversation.

hackernews · damaru2 · Sep 29, 09:03 · [Discussion](https://news.ycombinator.com/item?id=49890226)

**Background**: Conversational AI agents are chat-based assistants, such as ChatGPT or Perplexity, that users reach through a web browser or a mobile app. Privacy researchers study what data these agents send to servers and when, including telemetry, trackers, and platform permissions on mobile devices. A UUID is a unique identifier often placed in a URL to reference a specific session, and it is frequently mistaken for an anonymity guarantee because it looks random.

**Discussion**: Commenters were broadly skeptical of current privacy practices: one described noticing ChatGPT pre-sending unfinished prompts, another argued that UUID-based links are wrongly equated with privacy \(citing Perplexity\), and a third questioned how much risk comes from the agent itself versus underlying platform APIs and permissions. A recurring theme was a preference for open, locally runnable models, with one commenter invoking a Simpsons joke to say users have become the character who tells all their secrets to an AI.

**Tags**: `#privacy`, `#AI agents`, `#security`, `#tracking`, `#web/mobile`

---

<a id="item-4"></a>
## [OpenAI launches Dots, always-on cloud agents for work](https://openai.com/index/introducing-dots/) ⭐️ 8.0/10

OpenAI introduced Dots, a product of &quot;always-on&quot; AI agents that run on their own cloud computers and are being rolled out to Pro, Business Premium, and Enterprise users in eligible markets. Each dot gets its own identity, credentials, and access to the systems it needs, can be messaged through Slack, Teams, and other organizational platforms, with text message support coming soon. Dots marks a shift from single-turn chatbots toward persistent, autonomous agents that live in the cloud and act on a user&\#x27;s behalf continuously, pushing OpenAI deeper into enterprise workflows. It also intensifies competition with Anthropic&\#x27;s Claude-based agents and Meta&\#x27;s Muse, and raises questions about how deeply users get locked into one vendor&\#x27;s platform. OpenAI says each dot adapts to new information and improves through feedback from a team, and it envisions &quot;specialist Dots&quot; that take on specific responsibilities; the product builds on lessons from internal testing across procurement, invoice processing, email marketing, customer support, and commercial contracting. Dots is a product launch rather than a technical breakthrough, and availability is limited to specified paid tiers and markets at launch.

hackernews · alvis · Sep 29, 17:07 · [Discussion](https://news.ycombinator.com/item?id=49896604)

**Background**: Chat assistants like ChatGPT are typically stateless: you open a session, ask something, and the session ends. &quot;Always-on agents&quot; instead keep running in a cloud sandbox or virtual machine, holding long-term memory and connected accounts so they can act on your behalf without you watching. This is where the whole industry is heading — Anthropic&\#x27;s Claude-based coding agents and Meta&\#x27;s reported Muse agent point the same way — but because such agents accumulate integrations and work history, switching vendors becomes much harder than swapping between underlying models.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/introducing-dots/">Introducing dots | OpenAI</a></li>
<li><a href="https://techcrunch.com/2026/09/29/openai-launches-dots-its-bubbly-agentic-avatar/">OpenAI launches Dots, its bubbly agentic avatar | TechCrunch</a></li>
<li><a href="https://www.technobezz.com/news/openai-launches-dots-always-on-ai-agents">OpenAI Launches dots, Always-On AI Agents That Work in the Cloud | Technobezz</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters focused on platform lock-in, arguing that always-on agents with integrations and work history are effectively &quot;your computer on the cloud&quot; and far harder to switch away from than swappable models. Several said OpenAI earned goodwill with a generous Codex subscription and efficient models, but is now pushing unnecessary products and tightening the very limits that attracted users, echoing what Anthropic did earlier; others called the boundaries between Codex, ChatGPT Work, and Dots blurry, said they are more bullish on Meta&\#x27;s Muse for consumer distribution, and predicted these cloud agents spell the end of the PC era for non-technical and AI-native users.

**Tags**: `#OpenAI`, `#AI agents`, `#always-on agents`, `#platform lock-in`, `#product announcement`

---