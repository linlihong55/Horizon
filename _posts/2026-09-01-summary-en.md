---
layout: default
title: "Horizon Summary: 2026-09-01 (EN)"
date: 2026-09-01
lang: en
---

> From 37 items, 8 important content pieces were selected

---

1. [Google Removes MV2 Extensions From Chrome Web Store, Affecting uBlock Origin](#item-1) ⭐️ 8.0/10
2. [ChatGPT Work Tools and Skills Reference Site Draws Community Interest](#item-2) ⭐️ 8.0/10
3. [NAT Called the &\#x27;Original Sin&\#x27; Behind Internet Centralization](#item-3) ⭐️ 8.0/10
4. [Sliding-Window Attention Outperforms Linear Attention on Long-Context Reasoning](#item-4) ⭐️ 8.0/10
5. [Temporal Leakage in GNNs Exposed; SynthFin-AML Benchmark Enforces Causal Splits](#item-5) ⭐️ 8.0/10
6. [Tim Cook Steps Down as Apple CEO; John Ternus Takes Reins Focused on AI](#item-6) ⭐️ 8.0/10
7. [DeepSeek Releases Experimental Multimodal Model V4-Flash-Vision-Exp Weights](#item-7) ⭐️ 8.0/10
8. [EU Designates ChatGPT, Reddit, Roblox as &\#x27;Very Large&\#x27; Services Under DSA](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Google Removes MV2 Extensions From Chrome Web Store, Affecting uBlock Origin](https://webiterate.dev/google-removed-extensions-ublock-origin-108/) ⭐️ 8.0/10

Google has removed Manifest V2 \(MV2\) extensions from the Chrome Web Store, including uBlock Origin, and has begun disabling existing MV2 extensions in Chrome&\#x27;s stable channel. This pushes users toward Manifest V3 \(MV3\) alternatives with more limited content-filtering abilities. This is a major platform change that affects Chrome users who depend on ad blockers for privacy and security. Because MV3&\#x27;s restrictions weaken ad-blocking, users could become more exposed to malicious ads, and some are likely to switch to Firefox or other browsers. MV3 replaces the blocking webRequest API with declarativeNetRequest, which imposes caps on filter rules and restricts dynamic request blocking. uBlock Origin, a widely used open-source blocker, has publicly criticized these limits, and AdGuard&\#x27;s experimental MV3-compliant blocker also struggles under the new rules.

hackernews · twapi · Aug 31, 21:10 · [Discussion](https://news.ycombinator.com/item?id=49514878)

**Background**: Manifest V2 has long been the extension specification used by Chrome extensions, and uBlock Origin is a free, open-source content blocker that leverages it to block ads and trackers. Google announced MV3 as a migration for improved security and performance, but MV3&\#x27;s webRequest constraints severely limit traditional ad-blocking techniques. The removal from the Chrome Web Store is part of Google&\#x27;s planned phase-out of MV2, which was targeted for June 2025. Firefox still supports MV2 and remains an option for users who want full-featured uBlock Origin.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/UBlock_Origin">uBlock Origin - Wikipedia</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/adguard-s-new-ad-blocker-struggles-with-google-s-manifest-v3-rules/">AdGuard’s new ad blocker struggles with Google’s Manifest v 3 rules</a></li>
<li><a href="https://tegufy.com/news/chrome-manifest-v3-kills-ad-blockers-june-2026">Chrome Manifest V 3 Is Finally Killing Ad Blockers — Here&#x27;s What...</a></li>

</ul>
</details>

**Discussion**: Commenters strongly criticize the move, framing ad blocking as a safety necessity; one user noted that older family members can be tricked by malicious ads into installing scam software. Many recommend switching to Firefox, saying uBlock Origin has always worked best there. There is also broader frustration with Google&\#x27;s unilateral control over the web and nostalgia for Chrome&\#x27;s earlier positive reputation.

**Tags**: `#Chrome`, `#Manifest V2`, `#ad-blocking`, `#browser extensions`, `#privacy`

---

<a id="item-2"></a>
## [ChatGPT Work Tools and Skills Reference Site Draws Community Interest](https://codex-tool-reference.simonw.chatgpt.site/) ⭐️ 8.0/10

A new reference site at codex-tool-reference.simonw.chatgpt.site catalogs ChatGPT Work tools and skills, including a standout browser-control skill that drives a Playwright instance through Node.js. The site has attracted active Hacker News discussion, with Simon Willison highlighting its browser-control approach. This is significant because it curates and documents reusable ChatGPT Work skills, a new way to extend AI assistants with programmable workflows. Developer interest in browser automation suggests demand for moving from chat-only assistants to agents that can interact with live web pages. The browser-control skill instructs ChatGPT Work to launch a Playwright instance via its Node.js REPL and run \`nodeRepl.write\(await browser.documentation\(\)\)\` to fetch further usage instructions. Community members note that some work tools may slow down responses and waste tokens, and question how this differs from Codex, which can already perform similar actions.

hackernews · ijidak · Aug 31, 14:07 · [Discussion](https://news.ycombinator.com/item?id=49510000)

**Background**: ChatGPT Work tools and skills are reusable, shareable workflows that let ChatGPT handle specific tasks more consistently; a skill can contain instructions, examples, and code. Playwright is a browser automation library from Microsoft used for testing and automating web browsers, competing with tools like Selenium and Puppeteer. This reference site documents such skills so developers can discover and reuse them.

<details><summary>References</summary>
<ul>
<li><a href="https://help.openai.com/en/articles/20001066-skills-in-chatgpt">Skills in ChatGPT | OpenAI Help Center</a></li>
<li><a href="https://thecodeforge.io/python/playwright-python/">Playwright Python — Auto-wait Doesn&#x27;t Wait for... | TheCodeForge</a></li>

</ul>
</details>

**Discussion**: Simon Willison calls the control-browser skill the most interesting and links to the site&\#x27;s documentation and creation prompt. Other commenters raise practical concerns about token waste and slowness, and ask how this differs from Codex. A meta comment observes that AI-generated websites tend to share a similar visual style.

**Tags**: `#ChatGPT`, `#AI tools`, `#browser automation`, `#Playwright`, `#developer tools`

---

<a id="item-3"></a>
## [NAT Called the &\#x27;Original Sin&\#x27; Behind Internet Centralization](https://dreamstation.systems/personal/ntppost.html) ⭐️ 8.0/10

An essay argues that NAT \(Network Address Translation\) was one of the earliest contributors to internet centralization by making it harder to run a public server. The discussion was amplified by a comment from Rusty Russell, the implementer of the current NAT system in Linux, who acknowledged the trade-offs he made. This reframes a mundane networking technology as a structural force that shaped today&\#x27;s cloud-centric, client-server internet. It gives engineers and historians a concrete lens for understanding how the open, peer-to-peer internet gave way to centralized platforms. Rusty Russell explained that he avoided port reservation in favor of squeezing more connections into one IP address as long as the remote address allowed differentiation, which made incoming traffic from a different address unroutable. Another commenter argued that ordinary NAT is acceptable, while Carrier-Grade NAT \(CGNAT\) is the truly harmful concept.

hackernews · robinpie · Aug 31, 02:23 · [Discussion](https://news.ycombinator.com/item?id=49504905)

**Background**: Network Address Translation \(NAT\) was widely adopted to cope with IPv4 address exhaustion, allowing many private addresses to share one public IPv4 address. It violates the end-to-end principle, which holds that application-specific features should be implemented in the end nodes, not inside the network. Carrier-grade NAT pushes the same translation into the ISP&\#x27;s infrastructure, creating further layers of sharing and control.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/End-to-end_principle">End-to-end principle - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Carrier-grade_NAT">Carrier-grade NAT</a></li>

</ul>
</details>

**Discussion**: Commenters were split: some agreed that NAT trained users to accept a client-server model as natural, while others called &\#x27;original sin&\#x27; an exaggeration and pointed to UX problems in home gateways and the greater harm of CGNAT. Rusty Russell offered a nuanced defense, noting he was a young engineer solving a specific problem, but admitted NAT eroded the ability to run a server. Another commenter blamed a deeper design mistake in applying meatspace norms to cyberspace.

**Tags**: `#NAT`, `#networking`, `#internet history`, `#centralization`, `#sysadmin`

---

<a id="item-4"></a>
## [Sliding-Window Attention Outperforms Linear Attention on Long-Context Reasoning](https://www.reddit.com/r/MachineLearning/comments/1w3j1vw/slidingwindow_attention_beats_linear_on/) ⭐️ 8.0/10

A new arXiv preprint by Alexia Jolicoeur-Martineau and colleagues reports that sliding-window attention with sinks delivers 2 to 10 times higher performance than linear attention variants on long-context reasoning benchmarks such as Needle-in-a-Haystack and BABILong. The authors recommend switching to this simpler baseline instead of post-training linear models. This finding challenges a major research direction, suggesting that linear attention has not been properly compared against simpler baselines. It could shift focus in LLM efficiency research toward straightforward fixes like sliding-window attention. The paper specifically highlights Needle-in-a-Haystack and BABILong, where the reported gap is large and not close. The authors concede that linear attention may show promise, but argue it likely needs to be trained from scratch or heavily post-trained to even match SWA.

reddit · r/MachineLearning · /u/Justgototheeffinmoon · Aug 31, 16:35

**Background**: Standard self-attention has quadratic complexity in sequence length, making long-context processing expensive. Linear attention variants aim to reduce this to linear cost via approximations or recurrent forms, while sliding-window attention simply lets each token attend to a fixed local window, also achieving O\(n\) complexity and used by models like Mistral and Longformer. Attention sinks refer to keeping early tokens in the window to stabilize generation, since removing position 0 causes output quality to degrade rapidly. BABILong is a benchmark designed to test reasoning across facts distributed in extremely long documents.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2406.10149">BABILong: Testing the Limits of LLMs with Long Context Reasoning-in-a ...</a></li>
<li><a href="https://www.abhik.ai/concepts/transformers/sliding-window-attention">Sliding Window Attention | Abhik Sarkar</a></li>
<li><a href="https://mbrenndoerfer.com/writing/attention-sinks-streamingllm-infinite-generation">Attention Sinks and StreamingLLM for Long Generation - Interactive</a></li>

</ul>
</details>

**Tags**: `#attention`, `#LLM`, `#long-context`, `#sliding-window`, `#linear-attention`

---

<a id="item-5"></a>
## [Temporal Leakage in GNNs Exposed; SynthFin-AML Benchmark Enforces Causal Splits](https://www.reddit.com/r/MachineLearning/comments/1w3imxy/your_gnn_is_probably_just_an_overcomplicated_mlp/) ⭐️ 8.0/10

The Reddit post introduces SynthFin-AML v10.0, a dynamic graph benchmark designed to eliminate temporal leakage in GNN evaluation. It demonstrates that GraphSAGE \(PR-AUC 0.881\) only marginally outperforms a tuned LightGBM \(0.848\) when strict causal time-based splits are used. The work exposes a critical flaw in many dynamic GNN evaluations—temporal leakage—which can produce inflated performance and misleading conclusions. By enforcing causal boundaries, SynthFin-AML provides a more rigorous evaluation standard for AML and other temporal graph applications. The dataset contains 100k nodes and 1.2M edges, with a 3-snapshot point-in-time split: train edges up to Day 7, validation up to Day 8, and test up to Day 10. It also fixes tabular leakage by making fraud and retail transaction amounts share the same lognormal distribution \(μ=8.517, σ=0.8\).

reddit · r/MachineLearning · /u/Glabmayt2075 · Aug 31, 16:21

**Background**: Temporal leakage in graph neural networks occurs when a model trained on static snapshots of a dynamic graph can see future edges during training, violating causality. Standard transductive random splits do not respect the arrow of time and can inflate results. The post argues that tree-based models like LightGBM with point-in-time graph features are a strong baseline, and that GNNs must be evaluated with strict time-based splits to prove their value.

<details><summary>References</summary>
<ul>
<li><a href="https://kumo.ai/pyg/concepts/data-leakage/">Data Leakage in Graph ML: When Future Information Contaminates Training | Kumo.ai | Kumo.ai</a></li>
<li><a href="https://towardsdatascience.com/no-peeking-ahead-time-aware-graph-fraud-detection/">No Peeking Ahead: Time-Aware Graph Fraud Detection | Towards Data Science</a></li>
<li><a href="https://github.com/valiyevoktay-cmd/synthfin-aml-">GitHub - valiyevoktay-cmd/ synthfin - aml -: A graph-native Anti - Money ...</a></li>

</ul>
</details>

**Tags**: `#GNN`, `#temporal leakage`, `#dynamic graphs`, `#benchmark`, `#anti-money laundering`

---

<a id="item-6"></a>
## [Tim Cook Steps Down as Apple CEO; John Ternus Takes Reins Focused on AI](https://www.bloomberg.com/news/articles/2026-08-30/apple-s-new-ceo-john-ternus-takes-reins-from-tim-cook-focusing-on-ai) ⭐️ 8.0/10

Tim Cook stepped down as Apple CEO on August 31, 2026, with hardware engineering veteran John Ternus taking over on September 1. Ternus&\#x27;s top priority is accelerating AI, and Apple&\#x27;s first foldable iPhone is expected to debut at the September 9 event. The CEO change marks a strategic pivot at Apple, putting AI at the center of its roadmap and affecting product decisions for the entire ecosystem. The anticipated foldable iPhone also represents Apple&\#x27;s entry into the fast-growing foldable device market. John Ternus, 51, takes over after leading hardware engineering, while Tim Cook remains as executive chairman. The September 9 foldable iPhone is said to include 12GB RAM and deeply integrated Siri AI that can interpret real-world scenes through the display, calendar, and camera, addressing the delayed Siri upgrade.

telegram · zaihuapd · Aug 31, 10:21

**Background**: Foldable phones rely on flexible OLED displays and hinge mechanisms to switch between phone and tablet sizes; the market currently splits into horizontal and vertical folding designs, but creasing, durability, and weight have kept them from becoming mainstream. Siri AI is part of Apple Intelligence, Apple&\#x27;s on-device AI features, and is only available on iPhone 15 Pro and later; Apple has confirmed it will use Google&\#x27;s Gemini to power Siri&\#x27;s AI capabilities. These details give context to the new CEO&\#x27;s AI push and the foldable iPhone&\#x27;s feature set.

<details><summary>References</summary>
<ul>
<li><a href="https://36kr.com/p/2789794675546496">5年了， 折 叠 屏 为 什 么 还 是 没能普及？ -36氪</a></li>
<li><a href="https://www.tmtpost.com/6070018.html">折 叠 屏 不 是 主力 机 的未来-钛媒体官方网站</a></li>
<li><a href="https://iphonenews.cc/2026/02/02/apple-siri-gemini-ai-privacy-strategy/">Apple 為何選擇 Google Gemini？ Siri AI 升 級背後的真相</a></li>

</ul>
</details>

**Tags**: `#Apple`, `#CEO transition`, `#AI`, `#Tim Cook`, `#John Ternus`

---

<a id="item-7"></a>
## [DeepSeek Releases Experimental Multimodal Model V4-Flash-Vision-Exp Weights](https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash-Vision-Exp) ⭐️ 8.0/10

DeepSeek released the weights for DeepSeek-V4-Flash-Vision-Exp, an experimental multimodal model that adds a vision module to the V4-Flash architecture and continues training. Its ApexBench score jumped from 26.2 to 36.5, marking a major improvement in multimodal agent performance. The release is significant because it shows DeepSeek making rapid progress in multimodal agent capabilities, a key competitive area in AI development. The large benchmark gain suggests agent-focused models are improving quickly and will affect developers and researchers who rely on open-weight models. The model is experimental and builds on V4-Flash, with text agent task performance staying roughly flat compared to the previous V4-Flash-0731 release. The ApexBench measurement uses Pass@1 scores, and the release lacks detailed technical analysis beyond the benchmark results.

telegram · zaihuapd · Aug 31, 11:41

**Background**: Multimodal AI models process and generate multiple types of information, such as text, images, audio, and video, within connected tasks. ApexBench is a multimodal agent benchmark that evaluates complex agent tasks, and DeepSeek&\#x27;s vision-model releases report Pass@1 scores on it. This release continues DeepSeek&\#x27;s pattern of open-weight model releases, competing with labs like OpenAI and Anthropic in multimodal performance.

<details><summary>References</summary>
<ul>
<li><a href="https://www.datalearner.com/en/benchmarks/apexbench">ApexBench : Multimodal Agent Benchmark and... | DataLearnerAI</a></li>
<li><a href="https://www.emergentmind.com/topics/apex-bench">APEX - Bench : High-Fidelity Benchmarking</a></li>

</ul>
</details>

**Tags**: `#DeepSeek`, `#multimodal`, `#AI`, `#model-release`

---

<a id="item-8"></a>
## [EU Designates ChatGPT, Reddit, Roblox as &\#x27;Very Large&\#x27; Services Under DSA](https://www.euronews.com/next/2026/08/31/eu-places-chatgpt-reddit-and-roblox-under-strictest-digital-safety-rules) ⭐️ 8.0/10

On August 31, 2026, the European Commission designated ChatGPT as a Very Large Online Search Engine and Reddit and Roblox as Very Large Online Platforms under the Digital Services Act \(DSA\). The three services now face stricter EU digital safety and transparency rules. This is the first time an AI chatbot has been classified as a VLOSE, setting a precedent for AI services under EU digital regulation. The designation imposes significant compliance burdens on major platforms, affecting content moderation, risk management, and data transparency for hundreds of millions of EU users. All three services exceed the DSA threshold of 45 million monthly active users in the EU. They have a four-month transition period to conduct annual systemic risk assessments, undergo independent audits, and share data with regulators and vetted researchers on illegal content, child protection, and user well-being.

telegram · zaihuapd · Aug 31, 14:39

**Background**: The Digital Services Act is a landmark EU regulation that creates a tiered set of obligations for online intermediaries. Very Large Online Platforms and Very Large Online Search Engines—those with over 45 million EU monthly active users—face the strictest requirements on risk management, transparency, and accountability. The designation process is ongoing, and the Commission continues to assess other large services.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Digital_Services_Act">Digital Services Act - Wikipedia</a></li>
<li><a href="https://digital-strategy.ec.europa.eu/en/policies/digital-services-act">The Digital Services Act | Shaping Europe’s digital future</a></li>
<li><a href="https://digital-strategy.ec.europa.eu/en/policies/dsa-vlops">DSA: Very large online platforms and search engines | Shaping Europe’s digital future</a></li>

</ul>
</details>

**Tags**: `#EU`, `#Digital Services Act`, `#regulation`, `#ChatGPT`, `#Reddit`

---