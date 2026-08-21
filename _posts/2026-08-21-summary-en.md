---
layout: default
title: "Horizon Summary: 2026-08-21 (EN)"
date: 2026-08-21
lang: en
---

> From 42 items, 9 important content pieces were selected

---

1. [Felony Bench Tracks AI Agent Harm, Sparks Accountability Debate](#item-1) ⭐️ 8.0/10
2. [U.S. Citizen Faces Felony for Deleting Phone Data at Border](#item-2) ⭐️ 8.0/10
3. [Researcher accidentally logs military phone calls via ENUM hijack](#item-3) ⭐️ 8.0/10
4. [DeepSeek Releases Experimental Vision Model v4-flash-vision-exp](#item-4) ⭐️ 8.0/10
5. [AI Firms Destroying Physical Books; Scan Rare Copies Before It&\#x27;s Too Late](#item-5) ⭐️ 8.0/10
6. [Are Open Models Catching Up to Frontier AI?](#item-6) ⭐️ 8.0/10
7. [China&\#x27;s Chang&\#x27;e-7 to Launch Aug 24, Hopper to Hunt Lunar South Pole Water Ice](#item-7) ⭐️ 8.0/10
8. [Amazon Reported Buying and Destroying Books to Scan for AI Training](#item-8) ⭐️ 8.0/10
9. [YMTC&\#x27;s STAR Market IPO accepted, aims to raise 33 billion yuan](#item-9) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Felony Bench Tracks AI Agent Harm, Sparks Accountability Debate](https://www.felonybench.com/) ⭐️ 8.0/10

Felony Bench is a website and informal benchmark that tracks instances in which AI agents inadvertently compromise or affect third-party entities. It has drawn intense community discussion about legal accountability, especially after an incident involving OpenAI and Hugging Face. As AI agents become more autonomous and are deployed in real-world systems, incidents can occur without direct human intent, creating a legal gray area. This tracker is significant because it highlights the growing need for clear accountability frameworks, AI safety standards, and potentially mandatory incident reporting. The name &\#x27;Felony Bench&\#x27; is deliberately provocative, but the project counts &\#x27;unique instances where AI agents inadvertently compromise or affect third-party entities.&\#x27; Critics note that proving intent is normally required for criminal liability, so &\#x27;inadvertent&\#x27; incidents may not fit the felony framing; the site is also described as a benchmark rather than an official legal record.

hackernews · colinprince · Aug 21, 15:17 · [Discussion](https://news.ycombinator.com/item?id=49389430)

**Background**: AI agents are software systems that can pursue goals, use tools, and take multi-step actions with some autonomy, often driven by large language models. As these agents operate in real-world environments, they can occasionally cause harm to third parties, which has led to the creation of incident databases such as the MIT AI Incident Tracker and the AI Incident Database. Tracking such incidents is part of a broader effort to understand AI risks and design governance and reporting mechanisms before serious harms become widespread.

<details><summary>References</summary>
<ul>
<li><a href="https://www.felonybench.com/">Felony Bench</a></li>
<li><a href="https://en.wikipedia.org/wiki/AI_agent">AI agent</a></li>
<li><a href="https://airisk.mit.edu/ai-incident-tracker">MIT AI Incident Tracker</a></li>

</ul>
</details>

**Discussion**: Commenters are sharply divided. Some, like rfw300, argue that OpenAI treated its own &\#x27;felonious behavior&\#x27; like an uncontrollable act of God instead of taking responsibility, while beej71 states that a computer can never be held accountable, so it must never be allowed to commit a felony. Others question the legal framing: john\_strinlai notes that inadvertent actions and guardrails make felony claims unconvincing because intent must usually be proven, and lxe asks which party in the AI-agent chain — user, host, harness developer, or model developer — should be prosecuted. ang\_cire adds a broader critique that nonviolent felonies are often tools of oppression.

**Tags**: `#AI-safety`, `#AI-agents`, `#legal-liability`, `#ethics`, `#HackerNews`

---

<a id="item-2"></a>
## [U.S. Citizen Faces Felony for Deleting Phone Data at Border](https://www.nytimes.com/2026/08/21/us/politics/samuel-tunick-deleted-phone-felony.html) ⭐️ 8.0/10

Samuel Tunick, a U.S. citizen, has been charged with felonies for deleting data from his phone during a border search by customs agents. The case, reported by The New York Times, is drawing attention to the legal limits of digital privacy at U.S. ports of entry. This case could set a precedent for whether deleting one&\#x27;s own data during a border search is considered obstruction or a protected act. It directly affects travelers&\#x27; ability to safeguard sensitive personal and professional information from warrantless government inspection. The charges stem from an incident where Tunick allegedly wiped data while being searched by U.S. border agents. Because border searches have long been treated as an exception to the Fourth Amendment warrant requirement, the legal question hinges on whether data deletion after a search has begun constitutes obstruction.

hackernews · floathub · Aug 21, 12:10 · [Discussion](https://news.ycombinator.com/item?id=49386895)

**Background**: U.S. law generally allows border agents to search electronic devices without a warrant under the &quot;border search exception.&quot; However, courts have been split on the scope of digital searches, and legal experts argue that deleting data, especially by a citizen, raises complex questions about self-incrimination, destruction of evidence, and digital privacy rights.

**Discussion**: Commenters expressed widespread pessimism about the state of digital privacy in the U.S., with one likening the country to an East Germany or Soviet-era surveillance state. Others focused on technical workarounds, such as imaging a phone&\#x27;s storage before the border, using automation tools to trigger a factory reset, or keeping data in encrypted backups that require a separate password.

**Tags**: `#privacy`, `#border search`, `#digital rights`, `#surveillance`, `#legal`

---

<a id="item-3"></a>
## [Researcher accidentally logs military phone calls via ENUM hijack](https://lina.sh/blog/hijacking-e164-arpa) ⭐️ 8.0/10

In a new blog post, security researcher lina.sh describes how they accidentally logged hundreds of thousands of phone calls to military bases by querying the ENUM/E.164.arpa namespace. The incident reveals that this supposedly dead telephony DNS infrastructure is still operational and largely unprotected. This matters because it exposes a systemic weakness in global telephony routing that could be exploited to intercept, redirect, or manipulate calls. It also shows how forgotten infrastructure can create serious security and privacy risks for military and government organizations. The author apparently made queries against e164.arpa and collected call records, though no actual call content was intercepted. ENUM is not entirely dead: it still exists in private forms, such as number portability databases served over VPNs.

hackernews · gavide · Aug 21, 13:11 · [Discussion](https://news.ycombinator.com/item?id=49387570)

**Background**: ENUM \(E.164 Number Mapping\) uses the Domain Name System \(DNS\) to map international telephone numbers, organized under the E.164 standard, to Internet services such as SIP URIs. Under ENUM, phone numbers are reversed, dotted, and appended with e164.arpa; for example, +1-212-555-1234 becomes 4.3.2.1.5.5.5.2.1.2.1.e164.arpa. This allows call routing information to be published and resolved via DNS.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Telephone_number_mapping">Telephone number mapping - Wikipedia</a></li>
<li><a href="https://www.ietf.org/archive/id/draft-ietf-enum-combined-08.html">Combined User and Infrastructure ENUM in the e 164 . arpa tree</a></li>
<li><a href="https://circleid.com/posts/enum_mapping_e164_into_dns">ENUM: Mapping the E . 164 Number Space into the DNS</a></li>

</ul>
</details>

**Discussion**: HN commenters largely praised the writeup but added caveats: toast0 noted that ENUM is not dead, merely non-public, with private number-porting services still using e164.arpa queries over VPNs. chaz6 wished the author had set up a SIP server to see if calls would actually terminate, and mentioned the similar TRIP schema. Others expressed surprise that the author wasn&\#x27;t arrested, and amusement that the issue was only addressed once the military was involved.

**Tags**: `#security`, `#telephony`, `#ENUM`, `#vulnerability`, `#DNS`

---

<a id="item-4"></a>
## [DeepSeek Releases Experimental Vision Model v4-flash-vision-exp](https://api-docs.deepseek.com/guides/vision/) ⭐️ 8.0/10

DeepSeek released &\#x27;deepseek-v4-flash-vision-exp&\#x27; on August 21, 2026, an experimental vision-language model now available through the DeepSeek API and OpenRouter. The model converts image inputs into tokens that are billed alongside text tokens, enabling multimodal visual understanding. The release gives DeepSeek users native image understanding, bringing the model family into the multimodal space already occupied by GPT-4V, Gemini, and Claude. It also addresses a reported weakness in earlier DeepSeek text-only versions, which sometimes hallucinated vision tools or failed to read screenshots. The vision API docs state images are tokenized based on their dimensions and billed with text tokens; before inference, images smaller than roughly 384×384 pixels are scaled up preserving aspect ratio, while larger images are scaled down to about 800×800 total pixels. The model is marked &\#x27;Experimental&\#x27; and is served by DeepSeek directly, with OpenRouter listing it under the model ID deepseek/deepseek-v4-flash-vision-exp.

hackernews · dares2573 · Aug 21, 10:33 · [Discussion](https://news.ycombinator.com/item?id=49386163)

**Background**: A vision-language model \(VLM\) is a type of AI system that jointly interprets and generates information from both images and text, extending large language models beyond text-only input. Multimodal AI integrates multiple data types, such as text, audio, images, and video, for a more holistic understanding. OpenAI introduced computer vision to GPT-4 with GPT-4V, and similar capabilities were later added to Google&\#x27;s Gemini, Anthropic&\#x27;s Claude, and Microsoft&\#x27;s Copilot; open-source VLMs include LLaVA, InstructBLIP, and MiniGPT-4.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Vision-language_model">Vision-language model</a></li>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4-flash-vision-exp">DeepSeek V 4 Flash Vision Exp - API Pricing &amp; Providers | OpenRouter</a></li>
<li><a href="https://zenmux.ai/deepseek/deepseek-v4-flash-vision-exp">deepseek / deepseek - v 4 - flash - vision - exp - ZenMux</a></li>

</ul>
</details>

**Discussion**: Community reaction is positive but mixed. One user praised the model as &\#x27;promising&\#x27; for analyzing Playwright screenshots, a capability they previously missed from Sonnet; another found it fails a simple clock-reading test that Qwen got nearly right. Others noted the 800×800 resizing may be too low for OCR on full A4/letter pages, and one commenter recalled previous DeepSeek Flash versions hallucinating vision tools, making this upgrade welcome.

**Tags**: `#AI`, `#DeepSeek`, `#vision model`, `#LLM`, `#machine learning`

---

<a id="item-5"></a>
## [AI Firms Destroying Physical Books; Scan Rare Copies Before It&\#x27;s Too Late](https://annas-archive.gl/blog/physical-destruction.html) ⭐️ 8.0/10

Anna&\#x27;s Archive published a blog post warning that AI companies are purchasing physical books, scanning them, and then destroying the originals. The post urges the public to digitize rare books before they are lost forever. This practice pits AI training needs against cultural preservation, and could result in the irreversible loss of unique and rare books. It also highlights gaps in copyright law that allow copying for AI while restricting public access to digitized works. The post specifically advocates for prioritizing rare and out-of-print books, which are often irreplaceable. It argues that even if a digital copy is made, the physical artifact itself—its provenance and historical value—cannot be recovered once destroyed.

hackernews · Cider9986 · Aug 21, 02:37 · [Discussion](https://news.ycombinator.com/item?id=49383026)

**Background**: Mass digitization efforts, such as Google Books, have long faced copyright litigation but typically use non-destructive scanning. Controlled digital lending \(CDL\) allows libraries to lend digitized copies on a one-to-one basis, but its legality is still contested. Rare books are often unique and not widely replicated, so destroying them is irreversible. These dynamics explain why the destruction of physical books during AI scanning raises alarm.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ifla.org/files/assets/rare-books-and-manuscripts/Project-dcouments/ifla_rbms_digitization_guidelines_final_draft_20140703.pdf">Written by the IFLA Rare Book and Manuscripts Section Version: June 2014</a></li>
<li><a href="https://www.sciencedirect.com/science/article/abs/pii/S0099133306001534">Mass Digitization of Books - ScienceDirect</a></li>
<li><a href="https://en.wikipedia.org/wiki/Controlled_digital_lending">Controlled digital lending</a></li>

</ul>
</details>

**Discussion**: Commenters are divided: some cite Google Books as a precedent and argue most books have many copies, while others blame copyright holders for forcing AI companies to destroy books by refusing to allow legal digitization. Another common point is that destructive scanning is simply cheaper, and rare books deserve special treatment.

**Tags**: `#AI`, `#copyright`, `#digitization`, `#rare books`, `#preservation`

---

<a id="item-6"></a>
## [Are Open Models Catching Up to Frontier AI?](https://newsletter.semianalysis.com/p/are-open-models-catching-up) ⭐️ 8.0/10

SemiAnalysis has published an analysis titled &\#x27;Are Open Models Catching Up?&\#x27;, comparing open-weight models with closed frontier models across multiple eras of AI development. The article tracks how the performance gap between open and closed models has evolved over time. This analysis matters because it provides evidence-based insight into whether the open-source AI ecosystem is closing the gap with proprietary leaders, which influences research directions, investment decisions, and policy discussions. A narrowing gap could accelerate AI commoditization and broaden access to advanced capabilities. The article focuses on open-weight models, which release trained parameters but not necessarily full training data or code, and compares them against closed frontier models across different generations. SemiAnalysis is known for its deep technical industry analysis, so the piece likely relies on benchmark data and model releases to chart progress.

rss · Semianalysis · Aug 21, 16:40

**Background**: Open-weight models are AI models whose core trained parameters are publicly released, allowing anyone to download, inspect, and run them on their own infrastructure. Frontier models, in contrast, are the most advanced AI models at the cutting edge of capability, typically developed by leading labs with substantial computational resources. The comparison between open and closed models is central to debates about AI safety, accessibility, and competition, as open weights enable wider use and modification but also raise concerns about misuse.

<details><summary>References</summary>
<ul>
<li><a href="https://opensource.org/ai/open-weights">Open Weights: not quite what you’ve been told</a></li>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Open Source`, `#Model Comparison`, `#Frontier Models`, `#AI Research`

---

<a id="item-7"></a>
## [China&\#x27;s Chang&\#x27;e-7 to Launch Aug 24, Hopper to Hunt Lunar South Pole Water Ice](https://www.space.com/astronomy/moon/chinas-change-7-moon-probe-will-launch-this-weekend-on-the-most-ambitious-lunar-mission-in-history) ⭐️ 8.0/10

China&\#x27;s Chang&\#x27;e-7 lunar probe is scheduled to launch on August 24, 2026, from Wenchang aboard a Long March 5 Y14 rocket. The mission will deploy an orbiter, lander, rover, and a hopper to hunt for water ice near the Moon&\#x27;s south pole. This is one of the most ambitious lunar missions ever attempted and a major step in China&\#x27;s lunar exploration program. Finding water ice at the south pole could support future crewed bases and in-situ resource utilization. The lander will target the rim of Shackleton crater, and the hopper will traverse between sunlit areas and permanently shadowed craters to search for water ice. The mission also carries several international cooperative experiments, including a US-supported payload.

telegram · zaihuapd · Aug 21, 03:19

**Background**: Shackleton crater at the lunar south pole has peaks that are almost continually sunlit, while its interior is permanently shadowed and acts as a cold trap that may preserve water ice. A lunar hopper is a small spacecraft that can make repeated ballistic &\#x27;hops&\#x27; to access rugged terrain that rovers cannot reach, such as the bottoms of deep craters.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Shackleton_%28crater%29">Shackleton (crater)</a></li>
<li><a href="https://news.asu.edu/20210720-nasa-funds-hopper-explore-lunar-polar-craters">NASA funds hopper to explore lunar polar craters | ASU News</a></li>

</ul>
</details>

**Tags**: `#space exploration`, `#lunar mission`, `#Chang&\#x27;e-7`, `#water ice`, `#China`

---

<a id="item-8"></a>
## [Amazon Reported Buying and Destroying Books to Scan for AI Training](https://www.404media.co/we-tracked-a-shipment-of-rare-books-it-ended-at-an-amazon-ai-training-facility/) ⭐️ 8.0/10

404 Media&\#x27;s investigation revealed that Amazon is mass-purchasing physical books, scanning them for AI training data, and destroying the books afterward. Investigators planted a tracking device in a rare book and traced it to an Amazon warehouse in Las Vegas, Nevada. This practice raises significant ethical and legal questions about copyright and data sourcing in the AI industry, following similar revelations about Anthropic. It affects authors, publishers, and the broader ecosystem that increasingly relies on mass digitization of copyrighted works without transparent permission. Warehouse employees reportedly cut off book bindings to speed up scanning, and the pages are then discarded. This destructive book scanning technique is a known digitization method, but the scale and commercial use for AI training intensify the controversy.

telegram · zaihuapd · Aug 21, 04:52

**Background**: Mass digitization refers to large-scale projects that convert physical books and documents into digital formats, often for public archives like Google Books. Destructive book scanning, where books are cut or guillotined to scan pages quickly, is a standard technique in some high-volume digitization efforts. However, when AI companies buy rare or copyrighted books and destroy them solely for training data, it raises concerns about the preservation of cultural artifacts and compliance with copyright law.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Destructive_book_scanning">Destructive book scanning</a></li>
<li><a href="https://www.theguardian.com/commentisfree/2026/aug/05/anthropic-ai-destroying-books">Why is Anthropic destroying books? | Kathryn James | The Guardian</a></li>
<li><a href="https://www.reddit.com/r/singularity/comments/1v7birc/ai_companies_are_buying_antique_books_ingesting/">r/singularity on Reddit: AI Companies Are Buying Antique Books, Ingesting Their Contents to Train Models, and Then Destroying Them at Incredible Scale, Even If Almost No Copies Remain</a></li>

</ul>
</details>

**Discussion**: Reddit discussions on similar reports show mixed sentiment: some users point out that destructive scanning is a normal practice in large library digitization, while others express concern about the scale of destruction, especially for rare books. A common counterargument is that the speed of AI-driven scanning necessitates page destruction, but the long-term value of preserving originals remains debated.

**Tags**: `#AI training`, `#Amazon`, `#data ethics`, `#copyright`, `#investigation`

---

<a id="item-9"></a>
## [YMTC&\#x27;s STAR Market IPO accepted, aims to raise 33 billion yuan](https://api3.cls.cn/share/article/2461025?os=android&amp;amp;sv=8.8.2&amp;amp;app=cailianpress) ⭐️ 8.0/10

The Shanghai Stock Exchange has accepted Yangtze Memory Technologies&\#x27; \(YMTC\) initial public offering on the STAR Market, with plans to raise 33 billion yuan. The application was accepted after about three months of IPO counseling, with CITIC Securities and CITIC Construction Investment as sponsors. YMTC has become the first Chinese memory maker to rank in the global top three for NAND flash by shipment capacity, and its mega IPO could reshape the semiconductor memory landscape and bolster China&\#x27;s drive for self-sufficiency in storage chips. This affects investors, the chip industry, and global technology competition. The prospectus reveals 2026 first-quarter revenue of 47.04 billion yuan \(470.42 亿元\) and net profit attributable to shareholders of 33.38 billion yuan \(333.79 亿元\). According to Counterpoint, YMTC&\#x27;s shipment capacity in the second quarter of 2026 entered the global top three for NAND for the first time.

telegram · zaihuapd · Aug 21, 14:26

**Background**: YMTC is China&\#x27;s leading maker of 3D NAND flash memory, which is used in solid-state drives and mobile devices, and is a focal point of the country&\#x27;s semiconductor self-sufficiency efforts. The STAR Market is a NASDAQ-style board for technology firms launched by the Shanghai Stock Exchange in 2019. YMTC&\#x27;s IPO would be among the largest in China&\#x27;s memory chip sector, coming after it achieved a top-three global NAND shipment share.

**Tags**: `#semiconductor`, `#IPO`, `#NAND`, `#China tech`, `#memory`

---