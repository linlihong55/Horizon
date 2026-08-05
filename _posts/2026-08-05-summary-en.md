---
layout: default
title: "Horizon Summary: 2026-08-05 (EN)"
date: 2026-08-05
lang: en
---

> From 38 items, 14 important content pieces were selected

---

1. [Keyv and friends compromised in active Shai-Hulud supply chain attack](#item-1) ⭐️ 9.0/10
2. [Google Builds $200 Billion Financing Machine to Deliver AI Chips to Anthropic](#item-2) ⭐️ 9.0/10
3. [Mistral Launches Shieldstral, a 3B Open-Weights Multimodal Moderation Model](#item-3) ⭐️ 8.0/10
4. [Custom Color Space and Algorithm Generate Diverse Skin Tones](#item-4) ⭐️ 8.0/10
5. [Waymo Brings Driverless Ride-Hailing to Dallas](#item-5) ⭐️ 8.0/10
6. [DeepSeek V4 Flash Runs on a Single AMD MI300X](#item-6) ⭐️ 8.0/10
7. [FedEx Case Shows Legit Emails Look Just Like Phishing](#item-7) ⭐️ 8.0/10
8. [Oxide Computer Raises $445M Series D, SEC Filing Shows](#item-8) ⭐️ 8.0/10
9. [Xbox Outage Blocks Disc-Based Games, Igniting DRM Ownership Debate](#item-9) ⭐️ 8.0/10
10. [MiniMax-H3 Omni-Modal Model Now Runs on Apple Silicon via MLX Port](#item-10) ⭐️ 8.0/10
11. [Huawei Chief Scientist Warns Nvidia Chips Will Hit Physical Limits](#item-11) ⭐️ 8.0/10
12. [Trump administration drafts ban on Chinese optical modules](#item-12) ⭐️ 8.0/10
13. [China Releases First Mandatory National Standard for L3/L4 Autonomous Driving, Effective July 2027](#item-13) ⭐️ 8.0/10
14. [White House Reverses Course on Open Source AI Regulation Amid Silicon Valley Rift](#item-14) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Keyv and friends compromised in active Shai-Hulud supply chain attack](https://www.aikido.dev/blog/keyv-and-friends-compromised-in-npm-supply-chain-attack) ⭐️ 9.0/10

Security researchers at JFrog identified a new wave of the Shai-Hulud worm spreading through the npm registry via compromised packages, starting with keyv and cacheable. The active attack has affected over 400 packages, including the widely used keyv key-value storage library. Keyv is a widely used npm library with over 1,700 dependent projects, so this compromise can ripple broadly across the JavaScript ecosystem. The attack demonstrates how a self-replicating worm can exploit npm&\#x27;s trust model and underscores the urgent need for stronger supply-chain security measures. The worm harvests credentials, automatically publishes itself to writable npm packages, and plants execution hooks in GitHub repositories. JFrog&\#x27;s analysis indicates the campaign is still active, and developers should check for suspicious versions of keyv, cacheable, and any packages that depend on them.

hackernews · cimi\_ · Aug 4, 11:01 · [Discussion](https://news.ycombinator.com/item?id=49166874)

**Background**: Shai-Hulud is a self-replicating worm that targets the npm ecosystem, the world&\#x27;s largest JavaScript package registry. It spreads by compromising maintainer accounts or packages, harvesting credentials, and then using those credentials to publish malicious updates to other writable packages. Unlike typical single-use supply-chain payloads, Shai-Hulud automates its spread, enabling it to compromise hundreds of packages quickly and making cleanup difficult.

<details><summary>References</summary>
<ul>
<li><a href="https://research.jfrog.com/post/shai-hulud-is-back-august/">Major Shai Hulud campaign strikes npm again, affecting keyv and 400+ packages - JFrog Security Research</a></li>
<li><a href="https://www.cisa.gov/news-events/alerts/2025/09/23/widespread-supply-chain-compromise-impacting-npm-ecosystem">Widespread Supply Chain Compromise Impacting npm Ecosystem | CISA</a></li>
<li><a href="https://unit42.paloaltonetworks.com/npm-supply-chain-attack/">&quot;Shai-Hulud&quot; Worm Compromises npm Ecosystem in Supply Chain Attack (Updated November 26)</a></li>

</ul>
</details>

**Discussion**: Commenters expressed concern about the fragility of the npm dependency chain and the difficulty of cleaning up after such attacks. Suggestions included banning or restricting pre-install/post-install hooks, adopting devcontainers for isolation, and using static/dynamic analysis tools like Packj to detect compromises.

**Tags**: `#security`, `#supply-chain`, `#npm`, `#malware`, `#cybersecurity`

---

<a id="item-2"></a>
## [Google Builds $200 Billion Financing Machine to Deliver AI Chips to Anthropic](https://www.ft.com/content/549f2e23-5aa2-49c7-9ea6-a9784ab7087c) ⭐️ 9.0/10

According to a Financial Times investigation, Google has quietly created a roughly $200 billion asset-backed financing structure to deliver more than $150 billion in AI chips to Anthropic. The structure involves Broadcom, Apollo, Blackstone, Morgan Stanley, and several crypto-mining firms, with a special purpose vehicle called Compute SPV closing its first ~$35 billion hardware purchase in June. This is one of the largest infrastructure financing structures ever built for AI, representing a paradigm shift in how AI compute capacity is funded and deployed. It allows Anthropic, which lacks a credit rating, to access hundreds of billions of dollars in chips without burdening any single company&\#x27;s balance sheet, and could set a template for future AI infrastructure deals. The contracts total about $200 billion, with roughly 80% directly tied to chips. Risk is shared: Google guarantees data centers, Broadcom buys and helps finance chips, while Apollo and Blackstone purchase hardware and lease it back to Anthropic; the June Compute SPV deal covered about 1 gigawatt of compute and 1 million TPUs.

telegram · zaihuapd · Aug 4, 10:52

**Background**: The structure borrows from vendor financing, a model used by companies like Boeing and GE to sell planes and engines by partnering with financiers to help customers overcome upfront costs. A special purpose vehicle \(SPV\) is a bankruptcy-remote entity set up to isolate financial risk for a specific transaction, which is why Compute SPV was created. Tensor Processing Units \(TPUs\) are Google&\#x27;s custom application-specific integrated circuits \(ASICs\) designed for neural network machine learning, and they power Anthropic&\#x27;s computation needs.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Tensor_Processing_Unit">Tensor Processing Unit - Wikipedia</a></li>
<li><a href="https://corporatefinanceinstitute.com/resources/management/special-purpose-vehicle-spv/">Special Purpose Vehicle ( SPV ) - Guide, Examples, What You Need...</a></li>
<li><a href="https://www.pnc.com/insights/corporate-institutional/raise-capital/vendor-financing-what-it-is-and-how-it-works.html">Vendor Financing: What It Is and How It Works | PNC Insights</a></li>

</ul>
</details>

**Tags**: `#Google`, `#Anthropic`, `#AI Infrastructure`, `#Financing`, `#AI Chips`

---

<a id="item-3"></a>
## [Mistral Launches Shieldstral, a 3B Open-Weights Multimodal Moderation Model](https://mistral.ai/news/shieldstral/) ⭐️ 8.0/10

Mistral has released Shieldstral-1.0-3B, an open-weights 3B parameter multimodal content moderation model, now available on Hugging Face. It offers a cost-effective, customizable alternative to existing moderation APIs. Content moderation is a critical challenge for online platforms, and an open-weights model allows developers to fine-tune and deploy it locally, reducing dependence on proprietary APIs. This could lower entry barriers for smaller platforms and accelerate the adoption of multimodal safety tools. Shieldstral handles both text and image inputs, making it suitable for policy-based moderation across multiple content types. With only 3B parameters, it can run on edge devices with modest compute, though its non-deterministic nature may still require human review as a safety net.

hackernews · riadsila · Aug 4, 16:36 · [Discussion](https://news.ycombinator.com/item?id=49171268)

**Background**: Open-weights models are AI models whose trained parameters are publicly released, enabling anyone to download and customize them. Multimodal content moderation uses AI to simultaneously analyze text, images, and other content forms for policy violations. The 3B parameter size falls into a &\#x27;Goldilocks zone&\#x27; — small enough for local deployment, yet capable enough for many real-world tasks.

<details><summary>References</summary>
<ul>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>
<li><a href="https://arxiv.org/html/2508.05527v1">AI vs. Human Moderators: A Comparative Evaluation of Multimodal LLMs in Content Moderation for Brand Safety Accepted to the Computer Vision in Advertising and Marketing (CVAM) workshop at ICCV 2025.</a></li>
<li><a href="https://quadric.ai/blog/on-device-llm-revolution">The On-Device LLM Revolution: Why 3B-30B Models Are Moving to the Edge | Quadric Blog</a></li>

</ul>
</details>

**Discussion**: Commenters asked whether Shieldstral supports arbitrary rulesets or just a fixed moderation style, and one playfully suggested the name &\#x27;Safestral&\#x27;. Several praised Mistral&\#x27;s pivot to smaller fine-tuned models, while others compared it to OpenAI&\#x27;s omni-moderation API and noted its potential as a cost-effective first line of defense, albeit with human review still necessary for sensitive cases.

**Tags**: `#AI`, `#moderation`, `#Mistral`, `#open-weights`, `#safety`

---

<a id="item-4"></a>
## [Custom Color Space and Algorithm Generate Diverse Skin Tones](https://toneyalexander.github.io/inclusive-color-space/) ⭐️ 8.0/10

The author has created a custom color space, a JavaScript color picker, and procedural generation algorithms in Python and JavaScript that make it easy to sample plausible but diverse skin tones for digital art and game development. The project page includes interactive demos and detailed explanations of how the space was built. This addresses a practical gap in creative tools: conventional color pickers make it tedious to select a broad, inclusive range of skin tones. A simple, equation-based skin-tone space could improve character customization and procedural generation in games and digital art, and help creators avoid defaulting to a narrow set of skin colors. The color space is built by fitting equations to skin-tone data derived from a PCA-based 2D basis, resulting in a compact region shaped roughly like a crescent. The author notes the methodology is &quot;a bit shaky&quot; and includes a Future Work section, acknowledging room for improvement.

hackernews · automatoney · Aug 4, 15:16 · [Discussion](https://news.ycombinator.com/item?id=49170165)

**Background**: A color space is a system for representing colors numerically, such as RGB or HSV, but generic spaces are not designed for representing human skin accurately. Skin color is affected by melanin, blood flow, lighting, and human perception, so plausible skin tones form a limited, curved region inside a full color space. Existing data such as Pantone SkinTones and foundation shade datasets also show this crescent-like pattern, and color scientists have observed that skin at 100% saturation tends to look orange.

<details><summary>References</summary>
<ul>
<li><a href="https://toneyalexander.github.io/inclusive-color-space/">What Colors Are We? Constructing A Color Space For Skin Tones</a></li>
<li><a href="https://news.ycombinator.com/item?id=49170165">Show HN: Simple algorithm and color space to generate diverse skin tones | Hacker News</a></li>

</ul>
</details>

**Discussion**: Commenters were largely appreciative, praising the presentation and the hand-fitted function idea, and noting that the resulting colors match the crescent shape seen in foundation-shade data in Oklab. Others pointed out caveats: some generated colors appear green, blue, or purple, and one commenter wondered why Pantone SkinTones was not referenced. A commenter also shared the fact that skin at full saturation tends to look orange.

**Tags**: `#color-space`, `#computer-graphics`, `#procedural-generation`, `#skin-tones`, `#game-development`

---

<a id="item-5"></a>
## [Waymo Brings Driverless Ride-Hailing to Dallas](https://waymo.com/blog/shorts/dallas-open-to-all/) ⭐️ 8.0/10

Waymo has launched its autonomous ride-hailing service in Dallas, making the service open to all users. This marks the company&\#x27;s expansion into a new major Texas metroplex. The Dallas launch is a significant milestone in the wider deployment of autonomous vehicles, bringing robotaxis to a sprawling, car-dependent region. It also highlights ongoing public debates about safety, urban planning, and the local economic effects of driverless fleets. The Dallas–Fort Worth metroplex is extremely low-density and has limited public transit, making it a testing ground for robotaxis in car-centric environments. User comments also point to operational details such as the need for local maintenance labor and occasional vehicles getting stuck.

hackernews · xnx · Aug 4, 18:29 · [Discussion](https://news.ycombinator.com/item?id=49172836)

**Background**: Waymo is an autonomous vehicle company and subsidiary of Alphabet that began as Google&\#x27;s self-driving car project. It is the leading commercial operator of robotaxis in the United States, and the &\#x27;open to all&\#x27; designation means the Dallas service is now available to the general public rather than just a waitlist. Robotaxis are self-driving vehicles that can be hailed via an app, similar to ride-hailing services but without a human driver.

<details><summary>References</summary>
<ul>
<li><a href="https://waymo.com/">Waymo - Self-Driving Cars - Autonomous Vehicles - Ride-Hail</a></li>
<li><a href="https://builtin.com/articles/waymo-robotaxis">Waymo Explained: Alphabet’s Autonomous Vehicle Company | Built In</a></li>
<li><a href="https://en.wikipedia.org/wiki/Robotaxi">Robotaxi - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Comments are broadly positive, with users praising Waymo&\#x27;s safety and predictability compared to human drivers. A few raise economic concerns, such as money leaving the local economy, while another commenter argues driverless cars could serve as an affordable housing policy by reducing the need for parking and cars.

**Tags**: `#autonomous vehicles`, `#Waymo`, `#Dallas`, `#urban planning`, `#mobility`

---

<a id="item-6"></a>
## [DeepSeek V4 Flash Runs on a Single AMD MI300X](https://github.com/ryanzhou/deepseek-v4-flash-mi300x) ⭐️ 8.0/10

A practical guide demonstrates running DeepSeek V4 Flash on a single AMD MI300X, achieving about 150 tokens per second. The setup reduces the context window from the model&\#x27;s native 1M tokens to 256k to fit in the GPU&\#x27;s 192GB HBM3 memory. This lowers the hardware barrier for self-hosting a frontier-level MoE model, showing a single MI300X can serve it at practical speeds. It also strengthens AMD&\#x27;s case in AI inference, where Nvidia GPUs have dominated, and gives developers a reference path for single-GPU deployment. DeepSeek V4 Flash is a Mixture-of-Experts model with 284B total parameters and 13B activated parameters, and it ships with native MXFP4 quantized weights. The MI300X offers 192GB of HBM3, which is central to fitting the model; however, MI300X accelerators are OAM modules typically sold in 8-GPU boards, not as single units.

hackernews · zhoutong · Aug 4, 10:00 · [Discussion](https://news.ycombinator.com/item?id=49166386)

**Background**: DeepSeek V4 Flash is an efficiency-optimized preview of the DeepSeek V4 series, designed for fast reasoning across a 1M-token context. The AMD MI300X is an Instinct data-center GPU with 192GB HBM3 memory and 304 compute units. Quantization compresses model weights to lower precision, enabling large models to run on a single accelerator with faster inference, though often with tradeoffs such as reduced context length.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash">deepseek -ai/ DeepSeek - V 4 - Flash · Hugging Face</a></li>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4-flash">DeepSeek V 4 Flash - API Pricing &amp; Benchmarks | OpenRouter</a></li>
<li><a href="https://www.amd.com/en/products/accelerators/instinct/mi300/mi300x.html">AMD Instinct™ MI300X Accelerators</a></li>

</ul>
</details>

**Discussion**: Commenters raised practical caveats: you cannot easily buy a single MI300X — it is only sold as an 8-GPU box costing around €250K. Others noted alternative approaches like DoubleWord&\#x27;s 2xMI300X work, the DwarfStar project, and the upcoming MI350P PCIe card with 144GB memory, which can also run the model due to native MXFP4 quantization. One commenter highlighted the context-length tradeoff as acceptable, comparing it to OpenAI Codex&\#x27;s range.

**Tags**: `#DeepSeek`, `#AMD MI300X`, `#LLM inference`, `#quantization`, `#hardware`

---

<a id="item-7"></a>
## [FedEx Case Shows Legit Emails Look Just Like Phishing](https://www.troyhunt.com/thanks-fedex-this-is-why-we-keep-getting-phished/) ⭐️ 8.0/10

Troy Hunt published a 2024 blog post dissecting a real FedEx notification email that is nearly indistinguishable from a phishing message. The post shows how legitimate shipping alerts copy the same formatting, links, and urgency that scammers use. When legitimate companies send emails that look like phishing, users are trained to ignore warning signs, making real phishing attacks more successful. This case highlights a systemic security and UX problem that affects everyone who relies on email. The post generated 46 community comments and a score of 195, with readers sharing similar experiences from FedEx, Google, and the IRS. Commenters noted that even technical users were unsure whether certain official emails or shortened domains like c.gle were legitimate.

hackernews · stymaar · Aug 4, 21:09 · [Discussion](https://news.ycombinator.com/item?id=49175192)

**Background**: Phishing is a social engineering attack in which attackers impersonate trusted organizations to trick people into revealing sensitive information. Technical standards such as SPF, DKIM, and DMARC help verify that an email genuinely comes from a domain, but they cannot prevent legitimate senders from crafting messages that mimic phishing patterns. This means even authenticated emails can confuse users, as Troy Hunt&\#x27;s FedEx example demonstrates.

<details><summary>References</summary>
<ul>
<li><a href="https://www.validity.com/email-authentication/dmarc/">What is DMARC ? How Does DMARC Work? - Validity</a></li>
<li><a href="https://www.csoonline.com/article/567357/3-email-security-protocols-that-help-prevent-address-spoofing-how-to-use-them.html">Preventing address spoofing with DMARC, DKIM and SPF | CSO Online</a></li>

</ul>
</details>

**Discussion**: Commenters largely agreed with Hunt, sharing their own examples of legitimate messages looking like scams: a real FedEx customs notice sent by a person with a PDF attachment, a Google storage alert using a c.gle link, and an IRS IVR that sounds identical to scam callers. Several readers pointed out that the proliferation of gTLDs such as .xyz makes phishing detection even harder for non-technical users. One comment additionally cited Australia blocking 336 million scam SMS messages, reinforcing the scale of the problem.

**Tags**: `#phishing`, `#cybersecurity`, `#email`, `#social engineering`, `#human factors`

---

<a id="item-8"></a>
## [Oxide Computer Raises $445M Series D, SEC Filing Shows](https://www.sec.gov/Archives/edgar/data/1795071/000179507126000002/xslFormDX01/primary_doc.xml) ⭐️ 8.0/10

Oxide Computer has raised $445 million in a Series D funding round, according to a new SEC Form D filing. The round follows the company&\#x27;s earlier Series A \($44M\), Series B \($100M\), and Series C \($200M\) rounds. This large funding round signals strong investor confidence in Oxide&\#x27;s vision of an integrated on-premises cloud computer that can challenge public clouds like AWS. It could accelerate the company&\#x27;s growth and push the broader industry toward rack-scale, software-defined infrastructure. SEC Form D is a notice of an exempt securities offering and contains limited operating details, so the filing does not disclose valuation or investor names. Oxide sells a rack-scale &\#x27;Cloud Computer&\#x27; that integrates compute, storage, networking, and software into a single platform.

hackernews · depr · Aug 4, 20:13 · [Discussion](https://news.ycombinator.com/item?id=49174407)

**Background**: Oxide Computer Company, founded by former Sun and Joyent engineers, aims to deliver the public cloud experience on-premises with a single integrated rack. The company describes its product as &\#x27;the public cloud built this way — Oxide is, too.&\#x27; A Form D filing is how private companies report certain securities offerings to the SEC, often used for Reg D exemptions.

<details><summary>References</summary>
<ul>
<li><a href="https://oxide.computer/">Oxide Computer Company</a></li>
<li><a href="https://research.aerarium.app/filings/form-d">SEC Form D : exempt offering notice | Aerarium Research</a></li>
<li><a href="https://tracxn.com/d/companies/oxide-computer/__kI0jT50BQRv4YWhfboq9Wp2wCfHm6iQWJODTcCX-grc">Oxide Computer - 2026 Company Profile, Team, Funding... - Tracxn</a></li>

</ul>
</details>

**Discussion**: Community reaction is a mix of excitement and skepticism. Many praise the product concept and the team — especially Jessie Frazelle — but some question whether Oxide actually ships hardware, and one engineer \(VP of Eng\) says his sales inquiry was never answered despite his company spending $900k/year on AWS.

**Tags**: `#funding`, `#hardware`, `#cloud-computing`, `#infrastructure`, `#oxide-computer`

---

<a id="item-9"></a>
## [Xbox Outage Blocks Disc-Based Games, Igniting DRM Ownership Debate](https://birchtree.me/blog/xbox-goes-down-you-cant-play-games-you-own-on-disc/) ⭐️ 8.0/10

A widespread Xbox outage prevented users from playing games they owned on physical discs, because the console could not complete required online DRM verification. Even disc-based games were rendered unplayable until Microsoft&\#x27;s servers recovered. This incident exposes a key reality of modern gaming: even physical game discs are tied to online DRM checks, meaning consumers do not truly own their games. It has reignited the debate over digital ownership and consumer rights, affecting all Xbox players and raising concerns about game preservation. The outage shows that Xbox consoles perform online license verification even for disc-based titles, requiring a connection to Microsoft&\#x27;s servers. The original article notes the discussion drew 613 comments, indicating strong community engagement on the topic.

hackernews · surprisetalk · Aug 4, 12:01 · [Discussion](https://news.ycombinator.com/item?id=49167448)

**Background**: DRM \(Digital Rights Management\) refers to technologies that restrict how digital content is used, often requiring online verification to prove ownership or licensing. Many modern consoles and PCs apply DRM checks even to physical media, so if the relevant servers go offline or shut down permanently, legally purchased games can become unplayable. This has raised concerns among consumers about long-term access and the true nature of &\#x27;owning&\#x27; a game.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Digital_rights_management">Digital rights management - Wikipedia</a></li>
<li><a href="https://business.adobe.com/blog/basics/digital-rights-management">Digital Rights Management ( DRM ) | What It Is, How It Works &amp; Why It...</a></li>
<li><a href="https://www.youtube.com/watch?v=lZ2LhcsvyDQ">You Don&#x27;t Really Own Your Digital Games - YouTube</a></li>

</ul>
</details>

**Discussion**: Commenters expressed frustration that gaming is moving toward a licensing model similar to TV, movies, and music, where consumers own little. One user argued the real issue is ownership, not the physical vs. digital format, and listed rights like permanent access, offline use, and the ability to resell or pass games on. Others pointed out that older consoles like the PS3 ran matchmaking on free servers and supported offline play, contrasting sharply with today&\#x27;s always-online dependence.

**Tags**: `#DRM`, `#digital ownership`, `#gaming`, `#Xbox outage`, `#consumer rights`

---

<a id="item-10"></a>
## [MiniMax-H3 Omni-Modal Model Now Runs on Apple Silicon via MLX Port](https://simonwillison.net/2026/Aug/4/minimax-h3-mlx/#atom-everything) ⭐️ 8.0/10

MiniMax released MiniMax-H3, an omni-modal generative system that accepts text, images, audio, and video to generate up to 15-second video clips with audio. A new Python package, PipeNetwork/minimax-h3-mlx, ports the model to MLX for running on Apple Silicon, and the author successfully ran it on an M5 Max MacBook Pro. This makes a powerful state-of-the-art multimodal generation model accessible to Apple Silicon users without requiring cloud GPUs. It demonstrates the growing ecosystem of MLX ports and the trend toward running large generative models locally on consumer hardware. The model downloads roughly 115 GB of files, and generating a single 15-second video took just under 45 minutes on an M5 Max MacBook Pro. Audio output may be poor without following the prompting guide, as the author noted that unguided audio produced &quot;weird speech-like garbage&quot;.

rss · Simon Willison · Aug 4, 19:10

**Background**: MLX is an array framework developed by Apple for efficient machine learning on Apple silicon, leveraging the unified memory architecture with a NumPy-like Python API. An omni-modal generative system is a unified model capable of understanding and generating across text, image, audio, and video modalities, moving beyond single-task text-to-video models. The MLX port enables these models to run locally on Macs using Metal, rather than relying on remote cloud services.

<details><summary>References</summary>
<ul>
<li><a href="https://mlx-framework.org/">MLX</a></li>
<li><a href="https://github.com/ml-explore/mlx">GitHub - ml-explore/ mlx : MLX : An array framework for Apple silicon</a></li>
<li><a href="https://opensource.apple.com/projects/mlx/">Apple Open Source</a></li>

</ul>
</details>

**Tags**: `#MiniMax-H3`, `#MLX`, `#multimodal generation`, `#video generation`, `#Apple Silicon`

---

<a id="item-11"></a>
## [Huawei Chief Scientist Warns Nvidia Chips Will Hit Physical Limits](https://www.bloomberg.com/news/articles/2026-08-04/huawei-s-top-scientist-warns-of-chip-limit-nvidia-will-soon-face) ⭐️ 8.0/10

In a rare four-hour public interview in late July, Huawei chief semiconductor scientist Liao Heng warned that Nvidia-style scaling via more compute chips and high-bandwidth memory will soon hit physical limits, and proposed Huawei&\#x27;s LogicFolding framework and Tau Law as an alternative path. The first phone chip using LogicFolding is expected to launch later this year. This is significant because it challenges the dominant industry assumption that simply adding more silicon and memory can sustain AI compute growth. If the physical limit is real, the entire semiconductor ecosystem — from Nvidia to TSMC to hyperscalers — will need alternative approaches like 3D logic stacking and new scaling laws. Liao disclosed that Huawei has designed and manufactured 381 chips over the past six years using LogicFolding, a 3D logic-stacking framework that optimizes for signal delay rather than transistor pitch. The first product will be the Kirin 2026 SoC in the Mate 90 series, with Ascend AI accelerators expected to follow around 2030, targeting 1.4nm-class equivalent density by 2031 without EUV lithography.

telegram · zaihuapd · Aug 4, 08:04

**Background**: Traditional semiconductor scaling, often described by Moore&\#x27;s Law, relies on shrinking transistor dimensions to improve performance. Huawei&\#x27;s Tau Law \(also translated as Tao&\#x27;s Law\) is pitched as an alternative scaling theory for an industry stuck at the limits of transistor miniaturization, emphasizing system-level integration and 3D stacking. The approach is highly consistent with the broader industry direction that chip performance can no longer rely solely on making transistors smaller, though unresolved challenges remain in EDA toolchains and energy consumption control.

<details><summary>References</summary>
<ul>
<li><a href="https://abhs.in/blog/huawei-tau-scaling-law-logicfolding-55-percent-density-kirin-ascend-2026">Huawei Tau Scaling Law: 55% Density Gain on Kirin and Ascend Chips</a></li>
<li><a href="https://min.news/en/tech/a6f179218a21e70ccdde040590dd609d.html">A detailed explanation of Huawei&#x27; s &quot; Tao Law &quot;: What does it really...</a></li>
<li><a href="https://gizmoindo.com/news/huawei-tao-law-semiconductor-news/">Huawei Tao Law : New Hope or Chip Industry Mirage?</a></li>

</ul>
</details>

**Tags**: `#semiconductors`, `#Huawei`, `#Nvidia`, `#chip design`, `#physical limits`

---

<a id="item-12"></a>
## [Trump administration drafts ban on Chinese optical modules](https://www.reuters.com/world/trump-administration-drafting-ban-chinese-data-center-devices-sources-say-2026-08-04/) ⭐️ 8.0/10

The Trump administration is drafting a ban on importing new Chinese optical modules and other data center components, with the FCC reportedly advancing the measure. Officials aim to publish and enforce the rule within the year to protect AI infrastructure from espionage and sabotage. This ban would significantly disrupt the global data center and AI supply chain, directly hitting major vendors such as Zhongji Innolight, which holds about 27% of the optical module market. It also escalates U.S.-China trade tensions in a critical technology sector. Sources caution that the ban might still be modified or shelved, and China&\#x27;s embassy in Washington has vowed to take all necessary actions to protect Chinese interests. The FCC has previously imposed similar import restrictions on Chinese drones, routers, robots, and inverters.

telegram · zaihuapd · Aug 4, 11:29

**Background**: Optical modules are key components in data center networks, enabling high-speed data transmission over fiber optic cables by converting electrical signals to light signals. They connect servers, switches, and other network equipment, and are essential for the high-bandwidth infrastructure that supports AI workloads.

<details><summary>References</summary>
<ul>
<li><a href="https://ascentoptics.com/blog/everything-you-need-to-know-about-optical-modules/">Everything You Need to Know About Optical Modules</a></li>
<li><a href="https://www.baudcom.com.cn/blog/understand-the-optical-module">What is Optical Module ？ A Simple Guide for Beginners - Baudcom</a></li>

</ul>
</details>

**Tags**: `#policy`, `#trade`, `#AI infrastructure`, `#China`, `#supply chain`

---

<a id="item-13"></a>
## [China Releases First Mandatory National Standard for L3/L4 Autonomous Driving, Effective July 2027](https://wap.miit.gov.cn/jgsj/zbys/qcgy/art/2026/art_a1d2072374884287b67048a77560014e.html) ⭐️ 8.0/10

The Ministry of Industry and Information Technology \(MIIT\) officially issued GB 44721—2026, the mandatory national standard for safety requirements of intelligent connected vehicle autonomous driving systems, scheduled to take effect on July 1, 2027. This is China&\#x27;s first mandatory national standard specifically targeting L3 conditional and L4 highly automated driving systems. This standard marks a major regulatory milestone for China&\#x27;s autonomous driving industry, shifting safety requirements from recommended to mandatory and creating a unified compliance baseline. It will significantly affect automakers, suppliers, and technology companies, potentially accelerating the large-scale deployment of L3/L4 vehicles while clarifying legal and technical expectations. The standard applies to M-class \(passenger\) and N-class \(cargo\) vehicles equipped with L3 or L4 systems, but explicitly excludes automatic parking systems. It builds on the 2024 recommended national standard and constructs a safety requirement framework covering four dimensions: enterprise full-lifecycle safety assurance, system dynamic driving capability, human-machine interaction and user notification, and multi-dimensional inspection and testing.

telegram · zaihuapd · Aug 4, 13:06

**Background**: According to China&\#x27;s national standard GB/T 40429-2021 on driving automation classification, autonomous driving is divided into six levels from L0 to L5, where L3 is conditional automation and L4 is high automation. M-class and N-class vehicles refer to passenger and cargo vehicles respectively under Chinese vehicle classification, while the 2024 recommended standard laid the groundwork for this mandatory version.

<details><summary>References</summary>
<ul>
<li><a href="https://www.autohome.com.cn/news/202608/1316205.html">autohome.com.cn/news/202608/1316205.html</a></li>
<li><a href="https://www.donews.com/tag/58673.html">GB 44721 — 2026 - DoNews - 创新无边界</a></li>
<li><a href="https://m.jrj.com.cn/madapter/24h/2026/06/16174957490090.shtml">m.jrj.com.cn/madapter/24h/ 2026 /06/16174957490090.shtml</a></li>

</ul>
</details>

**Tags**: `#autonomous driving`, `#regulation`, `#China`, `#L3/L4`, `#standards`

---

<a id="item-14"></a>
## [White House Reverses Course on Open Source AI Regulation Amid Silicon Valley Rift](https://www.nytimes.com/2026/08/04/technology/ai-washington-regulation-whiplash.html) ⭐️ 8.0/10

The White House has abruptly reversed its position on restricting Chinese open-source AI models, dropping earlier consideration of sanctions and trade blacklists in favor of a strategy centered on boosting U.S. AI competitiveness. On August 4, the White House convened tech companies to discuss a new framework that would require cybersecurity reviews before model releases. This reversal determines whether the U.S. treats open-source AI as a security threat or a strategic asset in its competition with China. The decision will shape how major AI labs, open-source communities, and American companies operate globally, with tech leaders openly split on the issue. The trigger was the Chinese open-source model Kimi, developed by Moonshot AI, which reportedly rivals OpenAI&\#x27;s top models on some tasks. OpenAI and Anthropic lobbied for restrictions on Chinese competitors, while Nvidia and Meta defended open ecosystems; Jensen Huang recently made his first X post advocating open source and helped form a security alliance with over 230 member companies.

telegram · zaihuapd · Aug 4, 15:22

**Background**: Open-source AI models publish their weights publicly, allowing anyone to study, modify, and deploy them. This openness can accelerate innovation but also raises concerns about misuse and national security. Kimi is a series of large language models and a chatbot by Moonshot AI, a Beijing-based startup founded in 2023 by Tsinghua University alumni, known for long context windows and performance rivaling Western models. The U.S. government has been weighing how to balance AI competitiveness with security restrictions, and this reversal reflects intense lobbying from both sides of the tech industry.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kimi_%28chatbot%29">Kimi (chatbot) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Moonshot_AI">Moonshot AI</a></li>

</ul>
</details>

**Tags**: `#AI regulation`, `#open source`, `#policy`, `#national security`, `#Silicon Valley`

---