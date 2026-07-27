---
layout: default
title: "Horizon Summary: 2026-07-26 (EN)"
date: 2026-07-26
lang: en
---

> From 31 items, 11 important content pieces were selected

---

1. [GrapheneOS Shields Locked Devices from Data Extraction](#item-1) ⭐️ 8.0/10
2. [EU Proposes Browser-Level Privacy to Kill Cookie Banners](#item-2) ⭐️ 8.0/10
3. [Delegating details to AI may not be empowering](#item-3) ⭐️ 8.0/10
4. [LLM Token Relay Market: Pooling APIs and Fraud](#item-4) ⭐️ 8.0/10
5. [ARM64 Assembly Implementation of YOLO26n Inference from Scratch](#item-5) ⭐️ 8.0/10
6. [Small 4B Open-Weight Models Reach o3-Level on Swedish Medical QA](#item-6) ⭐️ 8.0/10
7. [LLMs Benchmarked on IMO 2026: Frontier Models Nearly Perfect](#item-7) ⭐️ 8.0/10
8. [DeepSeek Pauses Funding Round After Founder&\#x27;s Leaked Remarks](#item-8) ⭐️ 8.0/10
9. [CXMT IPO on Shanghai Stock Exchange could become highest market cap in A-shares](#item-9) ⭐️ 8.0/10
10. [Claude share links indexed by search engines, exposing user privacy](#item-10) ⭐️ 8.0/10
11. [SpaceX rejects Falcon 9 orders from 2028, bets on Starship](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [GrapheneOS Shields Locked Devices from Data Extraction](https://discuss.grapheneos.org/d/40700-grapheneos-protections-against-data-extraction-from-locked-devices) ⭐️ 8.0/10

GrapheneOS implements strong protections against data extraction from locked devices, including an auto-reboot feature that returns the device to Before First Unlock \(BFU\) mode after 18 hours of inactivity. This significantly enhances user privacy and security, especially for journalists, activists, and individuals at risk of device seizure, by ensuring encryption keys are inaccessible when the device is locked. The auto-reboot to BFU mode is complemented by PIN entropy analysis and other hardening measures, making GrapheneOS one of the most secure mobile operating systems available.

hackernews · Cider9986 · Jul 26, 05:57 · [Discussion](https://news.ycombinator.com/item?id=49055169)

**Background**: Before First Unlock \(BFU\) is a state where a device has been powered off or rebooted and has not been unlocked since; in this state, all data remains encrypted and inaccessible. GrapheneOS is an open-source Android-based OS focused on security and privacy, with features like sandboxed Google services and attack surface reduction.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GrapheneOS">GrapheneOS</a></li>
<li><a href="https://blogs.dsu.edu/digforce/2023/08/23/bfu-and-afu-lock-states/">BFU and AFU Lock States – Blog | DigForCE Lab - DSU</a></li>

</ul>
</details>

**Discussion**: Commenters noted that these features rival Apple&\#x27;s offerings, with some praising GrapheneOS for providing strong protection even without a duress password. Others discussed the entropy of different lock methods and the need for a complete backup solution to allow safe device wiping before border crossings.

**Tags**: `#security`, `#mobile`, `#grapheneos`, `#privacy`, `#android`

---

<a id="item-2"></a>
## [EU Proposes Browser-Level Privacy to Kill Cookie Banners](https://killthecookiebanner.eu/) ⭐️ 8.0/10

The European Commission has proposed a new regulation that would allow users to set their privacy preferences directly in their web browser, eliminating the need for repetitive cookie consent banners on every website. This could dramatically improve user experience by reducing intrusive pop-ups and could set a global standard for privacy consent that simplifies compliance for websites. The proposal still requires formal adoption by EU institutions. It builds on existing browser settings like those in Chrome and Edge but aims to make them legally binding for consent under GDPR.

hackernews · rapnie · Jul 26, 11:53 · [Discussion](https://news.ycombinator.com/item?id=49057175)

**Background**: Cookie banners are a result of the EU&\#x27;s ePrivacy Directive and GDPR, which require websites to obtain user consent before placing non-essential cookies. However, many users find these banners annoying and often click without reading. The proposed solution would let users set a global preference in the browser, which websites would then respect.

<details><summary>References</summary>
<ul>
<li><a href="https://support.microsoft.com/en-us/edge/adjust-privacy-settings-in-microsoft-edge">Adjust privacy settings in Microsoft Edge</a></li>
<li><a href="https://secureprivacy.ai/blog/cookie-consent-automation">Cookie Consent Automation: A Complete Guide for Businesses | Secure Privacy Blog</a></li>

</ul>
</details>

**Discussion**: Commenters express mixed feelings: some support the idea but suggest making all non-essential cookies illegal, while others note that a similar approach is already being implemented in California. A few point out that the real solution is to stop tracking altogether.

**Tags**: `#privacy`, `#cookie banners`, `#EU regulation`, `#web standards`, `#user experience`

---

<a id="item-3"></a>
## [Delegating details to AI may not be empowering](https://davidnicholaswilliams.com/its-not-empowering-to-hand-off-the-details/) ⭐️ 8.0/10

David Nicholas Williams argues that handing off details to AI reduces personal understanding and control, challenging the notion that delegation is empowering. This debate highlights a critical tension in AI-assisted development: the trade-off between efficiency gains and the loss of deep knowledge, affecting developer skill growth and code quality. The author focuses on the act of delegating details—not just tasks—and argues it leads to superficial understanding, while commenters note that verification can occur without full comprehension.

hackernews · davnicwil · Jul 26, 17:58 · [Discussion](https://news.ycombinator.com/item?id=49060592)

**Background**: Vibecoding is a term for loosely directing AI to generate code without deep involvement. The article taps into ongoing discussions about how much developers should rely on AI versus maintain hands-on expertise.

**Discussion**: Commenters are divided: some agree that delegating details reduces empowerment \(e.g., RGS1811’s fatigue with AI output\), while others find it liberating \(e.g., chungusamongus using AI for game development\). The dialogue emphasizes the need for judgement over which details to keep or hand off.

**Tags**: `#AI-assisted coding`, `#developer productivity`, `#software engineering`, `#knowledge work`, `#delegation`

---

<a id="item-4"></a>
## [LLM Token Relay Market: Pooling APIs and Fraud](https://simonwillison.net/2026/Jul/26/relay-market/#atom-everything) ⭐️ 8.0/10

An investigation by Matt Lenhard reveals a market where resellers offer discounted LLM tokens by pooling API keys from various sources, including abusing free trials and using stolen credit cards, primarily operating in China using open-source proxy tools like one-api and new-api. This highlights a significant security and fraud issue in the LLM ecosystem, where abusers can profit from unprotected endpoints, leading to large token bills for legitimate API users and vendors. It underscores the need for better API key caps and monitoring from LLM providers. The proxy software used, one-api and its fork new-api, are legitimate open-source API proxy products designed for load balancing across multiple API credentials. Buyers seek cheap tokens, avoid geo-restrictions, or collect data for model distillation.

rss · Simon Willison · Jul 26, 19:30

**Background**: LLM tokens are units used by language models to process text, and API keys grant access to these models on a pay-per-token basis. Resellers create proxy services that pool many API keys, often obtained through illicit means, to offer discounted rates. The open-source tools one-api and new-api allow users to set up such proxies easily, but they can be misused for fraudulent activities.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/songquanpeng/one-api/blob/main/README.en.md">one-api/README.en.md at main · songquanpeng/one-api</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#security`, `#fraud`, `#API`, `#AI`

---

<a id="item-5"></a>
## [ARM64 Assembly Implementation of YOLO26n Inference from Scratch](https://www.reddit.com/r/MachineLearning/comments/1v6w394/i_implemented_the_yolo26n_model_inference_from/) ⭐️ 8.0/10

A bachelor&\#x27;s thesis project implemented YOLO26n object detection inference entirely from scratch using ARM64 assembly language and C, without relying on any existing deep learning frameworks. The implementation incorporates advanced optimizations such as NEON SIMD, Winograd convolution, cache-aware tiling, and custom ARM64 micro-kernels. This project demonstrates a deep understanding of low-level systems programming and neural network optimization, which is crucial for deploying efficient AI on edge devices like the Raspberry Pi. It shows that even without massive frameworks, one can achieve functional inference with careful manual optimization, pushing the boundaries of edge AI performance. The implementation includes custom binary format for model parameters, operator fusion, attention mechanisms, and all YOLO26n components \(Conv, C3K2, SPPF, C2PSA, PSA, BottleNeck, Detect\). Performance improvement was lower than expected, indicating the complexity of optimizing for ARM NEON and memory hierarchy.

reddit · r/MachineLearning · /u/Forward\_Confusion902 · Jul 26, 06:43

**Background**: YOLO \(You Only Look Once\) is a popular family of real-time object detection models, with YOLO26n being the latest nano version optimized for edge devices. Winograd convolution is a fast algorithm that reduces the number of multiplications in convolutional layers, and NEON SIMD \(Single Instruction Multiple Data\) allows parallel processing on ARM processors. C2PSA is a dual-branch attention module used in YOLO26n to enhance feature extraction for small objects.

<details><summary>References</summary>
<ul>
<li><a href="https://platform.ultralytics.com/ultralytics/yolo26">YOLO 26 Models by Ultralytics</a></li>
<li><a href="https://arxiv.org/abs/2201.10369">[2201.10369] Winograd Convolution for Deep Neural Networks: Efficient ...</a></li>
<li><a href="https://www.emergentmind.com/topics/c2psa-module">C2PSA Module: Dual-Branch Attention</a></li>

</ul>
</details>

**Tags**: `#ARM64`, `#YOLO`, `#Edge AI`, `#Optimization`, `#Assembly`

---

<a id="item-6"></a>
## [Small 4B Open-Weight Models Reach o3-Level on Swedish Medical QA](https://www.reddit.com/r/MachineLearning/comments/1v71wds/openweight_4b_models_approach_o3level_medical/) ⭐️ 8.0/10

The post demonstrates that open-weight 4B models, specifically Qwen3.5-4B with reasoning enabled, achieve 87% accuracy on the MedQA-SWE Swedish medical licensing exam dataset, approaching the 88% score of OpenAI&\#x27;s o3 model. The author used supervised fine-tuning \(SFT\) on earlier exam years and an early-exit thinking intervention to prevent reasoning loops. This result shows that small open-weight models can rival much larger proprietary systems on domain-specific medical QA, lowering the barrier for clinical AI in low-resource languages. It highlights the effectiveness of post-training techniques like SFT and reasoning intervention for improving small model performance. The best result \(87%\) was achieved by Qwen3.5-4B with reasoning and an early-exit intervention that caps the thinking trace length, preventing repetitive loops. Without any post-training, Qwen3.5-4B already scores 77%, while older MedGemma-1.5-4B reached only 60% after SFT.

reddit · r/MachineLearning · /u/AccomplishedCat4770 · Jul 26, 11:58

**Background**: MedQA-SWE is a multiple-choice clinical question-answering dataset in Swedish, comprising 3,180 questions from exams for foreign doctors. The early-exit intervention is inspired by the S-GRPO reinforcement learning paper, which injects a phrase to close the thinking trace at a predetermined length. Small language models \(4B parameters\) are often used for efficient deployment due to lower compute requirements.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/datasets/nicher92/medqa-swe">nicher92/medqa-swe · Datasets at Hugging Face</a></li>
<li><a href="https://aclanthology.org/2024.lrec-main.975/">MedQA-SWE - a Clinical Question &amp; Answer Dataset for Swedish</a></li>
<li><a href="https://arxiv.org/pdf/2505.07686">S - GRPO : Early Exit via Reinforcement Learning in Reasoning Models</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#medical QA`, `#reasoning`, `#open-weight models`, `#Swedish`

---

<a id="item-7"></a>
## [LLMs Benchmarked on IMO 2026: Frontier Models Nearly Perfect](https://www.reddit.com/r/MachineLearning/comments/1v6wskz/we_compared_different_llms_on_imo_2026_r/) ⭐️ 8.0/10

A team of former IMO medalists evaluated multiple LLMs on the novel IMO 2026 problems, finding that frontier models &\#x27;sol&\#x27; and &\#x27;fable&\#x27; achieved nearly perfect scores, while their custom multi-agent harness AutoFyn significantly boosted performance of other models like Claude Sonnet and open-weight GLM. This comparison demonstrates that even on novel, high-difficulty math reasoning tasks, frontier models are approaching human expert-level performance, while orchestration harnesses can substantially bridge the gap for weaker models, highlighting the importance of engineering alongside model scale. Grading combined automated evaluation by a frontier model and manual verification by former IMO medalists; the hardest problem \(P3\) eluded all sub-frontier models regardless of harness, and hallucination issues still appeared in verifiable math domains.

reddit · r/MachineLearning · /u/pequalnp92 · Jul 26, 07:21

**Background**: International Mathematical Olympiad \(IMO\) problems are designed for high school students but require deep reasoning and are rarely seen in training data, making them a rigorous benchmark for LLM reasoning ability. An orchestration harness like AutoFyn coordinates multiple LLM calls, retrieval, and verification steps to improve performance on complex multi-step tasks, beyond what a single model call can achieve.

<details><summary>References</summary>
<ul>
<li><a href="https://opace.agency/blog/gpt-5-6-sol-vs-fable-5-expensive-llms/">GPT-5.6 Sol vs Fable 5 | Do More Expensive LLMs Provide Better Results?</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#benchmark`, `#reasoning`, `#math`, `#evaluation`

---

<a id="item-8"></a>
## [DeepSeek Pauses Funding Round After Founder&\#x27;s Leaked Remarks](https://www.bloomberg.com/news/articles/2026-07-25/deepseek-said-to-tell-backers-of-funding-pause-after-viral-posts) ⭐️ 8.0/10

DeepSeek has paused a new funding round due to founder Liang Wenfeng&\#x27;s dissatisfaction with leaked internal remarks. The company is also preparing for an IPO, which could be filed as early as 2026. This pause signals potential internal governance challenges at a major Chinese AI startup, and may affect its near-term capital raising and IPO timeline. It also highlights the sensitivity of communications in the competitive AI industry. The funding round was expected to raise at least 10 billion yuan at a pre-money valuation of no less than 480 billion yuan. DeepSeek raised $7 billion in its first round in June 2026, including investors like Tencent, CATL, and a national AI investment fund.

telegram · zaihuapd · Jul 26, 01:17

**Background**: DeepSeek is a Chinese AI company based in Hangzhou, focused on developing large language models. Its DeepSeek-V3 model uses a Mixture-of-Experts architecture with 671 billion total parameters. The company is owned by hedge fund High-Flyer, and its models are known for strong reasoning and efficient inference.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek - Wikipedia</a></li>
<li><a href="https://www.deepseek.com/en/">DeepSeek</a></li>

</ul>
</details>

**Tags**: `#AI`, `#DeepSeek`, `#funding`, `#business`, `#IPO`

---

<a id="item-9"></a>
## [CXMT IPO on Shanghai Stock Exchange could become highest market cap in A-shares](https://www.bloomberg.com/news/articles/2026-07-26/memory-frenzy-primes-china-champion-cxmt-for-historic-debut?srnd=phx-technology) ⭐️ 8.0/10

CXMT, China&\#x27;s largest DRAM manufacturer, will debut on the Shanghai Stock Exchange after raising 66.6 billion yuan \($9.8 billion\) in the biggest A-share IPO since 2010. This IPO signals China&\#x27;s push for semiconductor self-sufficiency and could make CXMT the most valuable A-share company, impacting the global DRAM market and semiconductor industry. The IPO priced at 8.66 yuan per share, with an initial market cap of about 580 billion yuan. Retail tranche was oversubscribed 212 times, with 9.4 million orders freezing approximately 7.07 trillion yuan.

telegram · zaihuapd · Jul 26, 07:31

**Background**: DRAM \(Dynamic Random Access Memory\) is a type of volatile memory used in computers and devices. CXMT operates as an IDM \(Integrated Device Manufacturer\), meaning it designs and manufactures its own chips. The company is China&\#x27;s most advanced DRAM producer and a key player in the country&\#x27;s semiconductor self-sufficiency goals.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Random-access_memory">Random - access memory - Wikipedia</a></li>
<li><a href="https://www.techtarget.com/searchstorage/definition/DRAM">What is DRAM ( Dynamic Random Access Memory )? How Does it...</a></li>

</ul>
</details>

**Tags**: `#DRAM`, `#Semiconductor`, `#IPO`, `#CXMT`, `#A-shares`

---

<a id="item-10"></a>
## [Claude share links indexed by search engines, exposing user privacy](https://search.brave.com/search?q=site%3Aclaude.ai%2Fshare&amp;amp;source=android) ⭐️ 8.0/10

A privacy vulnerability in Anthropic&\#x27;s Claude AI assistant allows publicly shared conversation links to be indexed by search engines like Google, exposing sensitive user data such as API keys, cryptocurrency wallet details, and personal information. Unlike ChatGPT, which fixed a similar issue a year ago, Anthropic has not yet addressed this flaw. This vulnerability compromises user privacy on a large scale, as anyone can access private conversations by searching indexed links. It undermines trust in AI assistants that handle sensitive information and highlights the need for default privacy safeguards in AI products. Exposed data includes API keys, cryptocurrency wallets, resumes, legal consultations, internal company projects, and Social Security numbers. Google has blocked indexing of these links, but Brave and Bing still index them. Anthropic recommends manually deleting shared conversations via settings.

telegram · zaihuapd · Jul 26, 11:16

**Background**: Claude is an AI assistant developed by Anthropic, designed for safe and accurate interactions. The &\#x27;share&\#x27; feature allows users to create public links to conversations. However, these links lack a &\#x27;noindex&\#x27; robots meta tag, which instructs search engines not to index a page. Without this tag, search engines automatically index the links, making them publicly discoverable.

<details><summary>References</summary>
<ul>
<li><a href="https://claude.com/">Claude</a></li>
<li><a href="https://en.wikipedia.org/wiki/Noindex">noindex - Wikipedia</a></li>
<li><a href="https://developers.google.com/search/docs/crawling-indexing/block-indexing">Block Search Indexing with noindex | Google Search Central</a></li>

</ul>
</details>

**Discussion**: The community discussion highlights the severity of the issue, with many users expressing concern over the exposure of highly sensitive data. A notable comment from Om Patel \(@om\_patel5\) notes that while Google has blocked indexing, Brave and Bing still index the links.

**Tags**: `#privacy`, `#security`, `#Claude`, `#AI`, `#vulnerability`

---

<a id="item-11"></a>
## [SpaceX rejects Falcon 9 orders from 2028, bets on Starship](https://www.bloomberg.com/news/articles/2026-07-23/spacex-is-turning-away-falcon-customers-in-major-bet-on-starship) ⭐️ 8.0/10

SpaceX has begun rejecting sole-use Falcon 9 launch requests from satellite operators for missions beyond 2028 and is no longer accepting future reservations for its Falcon 9 rideshare program, while scaling back production of non-reusable Falcon parts to accelerate transition to Starship. This strategic shift could reshape the commercial launch market, as many satellite operators rely on Falcon 9 for affordable access to orbit; if Starship fails to achieve operational readiness by 2028, a significant launch capacity gap may emerge. SpaceX may still retain Falcon 9 missions for the U.S. Department of Defense and NASA, but its stock has dropped about 25% since its June 2026 IPO due to Starship delays; as of July 2026, Starship has launched 13 times with 8 successes and 5 failures.

telegram · zaihuapd · Jul 26, 12:42

**Background**: Starship is a two-stage fully reusable super heavy-lift launch vehicle under development by SpaceX, intended to succeed Falcon 9 and Falcon Heavy. It is powered by Raptor engines burning liquid methane and liquid oxygen, and aims to reduce launch costs through reuse. The Falcon 9 has been SpaceX&\#x27;s workhorse, offering dedicated and rideshare launches for commercial and government customers. SpaceX&\#x27;s transition to Starship involves phasing out Falcon 9 production, but Starship has not yet entered commercial service.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Starship_rocket">Starship rocket</a></li>
<li><a href="https://www.spacex.com/rideshare">Smallsat Rideshare Program - SpaceX</a></li>
<li><a href="https://rideshare.spacex.com/">SpaceX Satellite Rideshare</a></li>

</ul>
</details>

**Tags**: `#SpaceX`, `#Starship`, `#Falcon 9`, `#space launch`, `#commercial space`

---