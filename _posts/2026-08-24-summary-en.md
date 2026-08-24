---
layout: default
title: "Horizon Summary: 2026-08-24 (EN)"
date: 2026-08-24
lang: en
---

> From 48 items, 12 important content pieces were selected

---

1. [MS Paint and Photos Embed Hidden GUID Watermarks in AI-Edited Images](#item-1) ⭐️ 8.0/10
2. [Shipyard Team Winding Down, IPFS Project Continues](#item-2) ⭐️ 8.0/10
3. [seL4 security proofs now complete on AArch64](#item-3) ⭐️ 8.0/10
4. [Essay Argues AI Coding Tools Will Erode Developer Expertise](#item-4) ⭐️ 8.0/10
5. [Turning Executables into Queryable SQLite Databases](#item-5) ⭐️ 8.0/10
6. [AgentX InferenceXv3: Does NVIDIA&\#x27;s CUDA Moat Hold in Agentic AI?](#item-6) ⭐️ 8.0/10
7. [Bart: A 2.82B Vintage LLM Trained on Pre-1931 English](#item-7) ⭐️ 8.0/10
8. [AI Generates 3D Objects as Programmable Code, Not Meshes](#item-8) ⭐️ 8.0/10
9. [Qwen 3.8 27B Ranks 9th on Code Arena, Outpacing Gemma 4 31B](#item-9) ⭐️ 8.0/10
10. [Anthropic&\#x27;s Claude Fable 5 Sees Weak Enterprise Demand, Priced Too High](#item-10) ⭐️ 8.0/10
11. [Hugging Face Explores Sale at $13B Valuation](#item-11) ⭐️ 8.0/10
12. [Xiaomi unveils three Xuanjie chips: AI flagship SoC, accelerator, 3nm auto chip](#item-12) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [MS Paint and Photos Embed Hidden GUID Watermarks in AI-Edited Images](https://xusheng.dev/posts/reversing/mspaint_invisible_watermark/main/) ⭐️ 8.0/10

Security researcher Xu Sheng reports that Microsoft Paint and Microsoft Photos silently embed an invisible GUID watermark into images edited with AI features, even when the processing happens entirely on-device with local models. The invisible watermark cannot be disabled, although Microsoft offers a separate visible AI watermark option that users can turn off. This means any image touched by AI tools in these apps carries a unique identifier tied to the user&\#x27;s Microsoft account, which can be used to deanonymize creators and enables copyright or legal requests to Microsoft for personal data. It underscores a growing industry trend of invisible AI watermarking that conflicts with user expectations of privacy for local processing. According to the report, the invisible watermark is a GUID embedded in the image metadata or pixel data, and it is added by both MS Paint and MS Photos after any AI-manipulation. The trigger conditions are not fully documented—commenters note false positives, and it is unclear whether simple AI-assisted actions such as background removal or text correction also receive the watermark.

hackernews · ComputerGuru · Aug 24, 15:28 · [Discussion](https://news.ycombinator.com/item?id=49421158)

**Background**: AI-generated content watermarking is becoming common as companies respond to concerns about deepfakes and provenance; for example, Anthropic recently added invisible watermarks to Claude-generated text that survive copy-and-paste. Microsoft also provides a visible AI watermark setting in Paint, which can be set to &\#x27;Never,&\#x27; &\#x27;Always,&\#x27; or &\#x27;Ask every time,&\#x27; but the hidden GUID watermark reportedly has no such control. The use of GUIDs is notable because unlike generic &\#x27;AI-generated&\#x27; labels, a GUID can uniquely identify the device or account that produced the image.

<details><summary>References</summary>
<ul>
<li><a href="https://geekrewind.com/how-to-enable-or-disable-ai-generated-watermark-in-paint-app-in-windows-11/">How to Enable or Disable AI-generated Watermark in Paint app in Windows 11 | Geek Rewind</a></li>
<li><a href="https://www.forbes.com/sites/anishasircar/2026/08/13/claude-will-now-leave-a-watermark-on-everything-it-writes-what-does-that-mean/">Anthropic’s Claude Adds Invisible Watermarks To AI ... - Forbes</a></li>
<li><a href="https://www.npr.org/2026/08/17/nx-s1-5928211/anthropics-new-invisible-watermark-marks-content-generated-by-ai-chatbot-claude">Anthropic&#x27;s new invisible watermark marks content generated ...</a></li>

</ul>
</details>

**Discussion**: Commenters are mostly concerned about anonymity and legal exposure, arguing the invisible GUID could be used to tie memes or images back to a Microsoft account via subpoenas. Others say the AI angle is a red herring, and point to Microsoft&\#x27;s history of sloppy AI-labeling rollouts, such as incorrectly stamping Copilot watermarks on Azure DevOps commits; some recommend avoiding Paint and other LLM-enabled apps.

**Tags**: `#privacy`, `#watermarking`, `#windows`, `#AI`, `#security`

---

<a id="item-2"></a>
## [Shipyard Team Winding Down, IPFS Project Continues](https://ipshipyard.com/blog/2026-the-end-of-ipfs-at-shipyard/) ⭐️ 8.0/10

Shipyard, a major maintainer team for IPFS implementations, has announced it is winding down, transitioning from centralized implementation support to individual maintainer grants. The IPFS project itself is not shutting down, despite the misleading title of the original post. This shift matters because it changes how IPFS is maintained, moving away from a dedicated team to a grant-funded community of individual maintainers. It could affect development coordination, release cadence, and the long-term health of the broader IPFS ecosystem. The sunset announcement specifically concerns Shipyard, one of several IPFS implementation maintainers, not the IPFS protocol itself. Protocol Labs is switching to individual maintainer grants, and community members note prior signs such as Cloudflare dropping IPFS and concerns about IPNS not satisfying webapp use cases.

hackernews · iand · Aug 24, 15:48 · [Discussion](https://news.ycombinator.com/item?id=49421489)

**Background**: IPFS \(InterPlanetary File System\) is a decentralized peer-to-peer protocol that uses content-based addressing instead of location-based addresses like HTTP. Shipyard was a team—formerly part of Protocol Labs—that maintained various IPFS implementations and ecosystem tools. This transition to individual maintainer grants reflects a broader trend in open-source sustainability, where projects move away from company-backed teams toward community-funded development.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/InterPlanetary_File_System">InterPlanetary File System - Wikipedia</a></li>
<li><a href="https://blog.ipfs.tech/shipyard-hello-world/">IPFS &amp; libp2p Devs Go Independent: Meet Interplanetary Shipyard</a></li>
<li><a href="https://ipfs.tech/">IPFS — Content addressing for data with confidence</a></li>

</ul>
</details>

**Discussion**: Commenters clarified that the post is confusing and that only Shipyard is sunsetting, with the IPFS project continuing via individual grants. Some users suggested sustainable alternatives like Iroh, while others criticized Protocol Labs and pointed to past issues such as Cloudflare dropping IPFS and IPNS shortcomings. One commenter ironically noted the need to fill out a Google Form to provide feedback about a decentralized project.

**Tags**: `#IPFS`, `#decentralized web`, `#open source maintenance`, `#p2p`, `#Protocol Labs`

---

<a id="item-3"></a>
## [seL4 security proofs now complete on AArch64](https://proofcraft.systems/news-2026/#2026-08-21) ⭐️ 8.0/10

The seL4 microkernel&\#x27;s security proofs are now complete on the AArch64 \(64-bit ARM\) architecture, announced via the Proofcraft systems news page in August 2026. This marks a formal verification milestone for the open-source, capability-based microkernel. This is significant because seL4 is one of the few operating system kernels with machine-checked formal proofs, and extending those proofs to AArch64 broadens the reach of high-assurance computing to the ubiquitous ARM platform. It could accelerate adoption in embedded, automotive, and military systems where formal guarantees are critical. The completed proofs cover the non-MCS \(mixed criticality systems\) configuration and are limited to unicore, not multicore, execution. Side-channel timing attacks also remain a noted threat that could potentially undercut the security claims.

hackernews · snvzz · Aug 24, 11:32 · [Discussion](https://news.ycombinator.com/item?id=49418255)

**Background**: Formal verification uses mathematical techniques to prove that a system behaves according to its specification. seL4 is an open-source, capability-based microkernel that has been formally verified for properties such as memory safety, integrity, and confidentiality. AArch64 is the 64-bit execution state of the ARM architecture family, introduced with ARMv8 and now used from mobile devices to servers.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/SeL4">seL 4 - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/AArch64">AArch64 - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Formal_verification">Formal verification - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Community reactions mix praise with caveats. Some note that side-channel timing attacks could invalidate the results, while others point out the proof only covers the unicore, non-MCS configuration. There are also questions about real-world OS adoption and calls for a native seL4/Linux environment to make the capability model more broadly impactful.

**Tags**: `#formal verification`, `#seL4`, `#microkernel`, `#AArch64`, `#security`

---

<a id="item-4"></a>
## [Essay Argues AI Coding Tools Will Erode Developer Expertise](https://larsfaye.com/articles/ai-coding-will-prevent-expertise) ⭐️ 8.0/10

An essay published on larsfaye.com argues that reliance on AI coding tools will collapse coding expertise, and the post has generated a lively community debate. The debate highlights concerns about enterprise mandates forcing AI-assisted development and the long-term effects on skill formation. This matters because AI coding tools are rapidly changing how software is written, reviewed, and maintained, affecting developers&\#x27; career trajectories and code quality. The debate also raises questions about whether current productivity gains are sustainable if deeper expertise is lost. Commenters distinguish between &\#x27;vibe coding&\#x27; and &\#x27;guided coding&\#x27;, noting that guided coding with LLM-integrated editors can be both productive and educational. Several commenters worry that developers are producing code faster than humans can review it, leading to an unsustainable burden on those who still review AI-generated code.

hackernews · larsfaye · Aug 24, 15:52 · [Discussion](https://news.ycombinator.com/item?id=49421554)

**Background**: AI coding assistants, such as Copilot and similar LLM-based tools, can generate entire functions or features from natural-language prompts. Some developers use them to write code directly \(&\#x27;vibe coding&\#x27;\), while others use them interactively within editors to assist parts of their workflow \(&\#x27;guided coding&\#x27;\). Deep expertise in software engineering often develops through long-term practice and the friction of solving hard problems, which is why some argue that heavy AI reliance may weaken these skills.

**Discussion**: The discussion is polarized: some commenters report enterprise mandates that punish manual coding, while others praise guided coding for being more enjoyable and higher-quality than pure vibe coding. A recurring concern is that AI-generated code is outpacing human review, and that maintaining expertise without intentional friction is unsustainable.

**Tags**: `#AI`, `#Software Engineering`, `#Developer Productivity`, `#Skill Formation`

---

<a id="item-5"></a>
## [Turning Executables into Queryable SQLite Databases](https://fzakaria.com/2026/08/23/your-executable-is-a-sqlite-database) ⭐️ 8.0/10

A new blog post by Farid Zakaria demonstrates how an ELF executable can be treated as a SQLite database using the virtual table mechanism, enabling SQL queries over the binary&\#x27;s contents. The approach also supports flexible multi-version binary shipping by storing multiple variants of code within the executable. This idea blurs the boundary between code and data, opening new possibilities for binary introspection, portability, and self-modifying applications. It could influence how systems programmers design portable &\#x27;fat binaries&\#x27; and package distribution. The technique relies on SQLite&\#x27;s virtual table API \(vtab\), which lets developers expose any data source as a table. The author&\#x27;s implementation maps ELF sections and program headers into queryable columns, and even discusses embedding a Lisp image or a virtual file system as runtime-modifiable tables.

hackernews · setheron · Aug 24, 04:48 · [Discussion](https://news.ycombinator.com/item?id=49415271)

**Background**: ELF \(Executable and Linkable Format\) is the standard file format for executables and shared libraries on Linux and other Unix-like systems, organized into sections and segments. SQLite&\#x27;s virtual table mechanism allows custom code to register a table whose data is computed by user-defined functions, effectively &\#x27;mounting&\#x27; external data as a database. Combining these ideas means an executable file can be queried and manipulated like a database, an approach the author calls &\#x27;your executable is a SQLite database.&\#x27;

<details><summary>References</summary>
<ul>
<li><a href="https://www.sqlite.org/vtab.html">The Virtual Table Mechanism Of SQLite</a></li>
<li><a href="https://en.wikipedia.org/wiki/Executable_and_Linkable_Format">Executable and Linkable Format - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters were largely enthusiastic, with several saying they had wanted to build something similar; one highlighted the &\#x27;mind-blowing&\#x27; realization that any data source can be mounted as a SQL table via vtab. The author noted that when he published a short paper on this idea in academic circles, the feedback &\#x27;wasn&\#x27;t so kind,&\#x27; adding an interesting counterpoint to the positive community reception.

**Tags**: `#sqlite`, `#executables`, `#elf`, `#virtual-tables`, `#systems-programming`

---

<a id="item-6"></a>
## [AgentX InferenceXv3: Does NVIDIA&\#x27;s CUDA Moat Hold in Agentic AI?](https://newsletter.semianalysis.com/p/agentx-inferencexv3-does-cuda-moat) ⭐️ 8.0/10

SemiAnalysis&\#x27;s &\#x27;AgentX - InferenceXv3&\#x27; analysis examines whether NVIDIA&\#x27;s CUDA moat survives agentic inference. It is backed by an open-sourced $3 million dataset, 1 million-plus context lengths, sub-agent KVCache hit rates above 95%, and comparisons of GB300 NVL72, B200, and MI355 systems. Agentic workloads shift inference from short single-turn requests to long, multi-turn chains where cache reuse and context management dominate. If the CUDA moat weakens in this regime, it could open the door for competitors like AMD and reshape hardware purchasing decisions in AI data centers. The article reports an open-sourced dataset valued at $3 million, context lengths exceeding 1 million tokens, multiturn interactions, and sub-agent KVCache hit rates above 95%. It also compares NVIDIA&\#x27;s GB300 NVL72 and B200 against AMD&\#x27;s MI355 in agentic inference scenarios.

rss · Semianalysis · Aug 24, 00:19

**Background**: Agentic inference refers to AI workloads where autonomous agents complete tasks by breaking them into multiple steps and making chains of model calls. KVCache stores previously computed key-value tensors so that repeated prefixes or turns do not need full recomputation, which is especially important for long-context and multi-turn agent flows. The CUDA moat refers to NVIDIA&\#x27;s programming model and software ecosystem that locks developers into its GPUs. Whether that lock-in persists in agentic inference is the core question of this analysis.

<details><summary>References</summary>
<ul>
<li><a href="https://sambanova.ai/blog/introducing-the-sn50-rdu-purpose-built-for-agentic-inference">Introducing the SN50 RDU: Purpose-Built for Agentic Inference</a></li>
<li><a href="https://huggingface.co/blog/not-lain/kv-caching">KV Caching Explained: Optimizing Transformer Inference Efficiency</a></li>
<li><a href="https://pitchgrade.com/research/nvidia-competitive-moat">NVIDIA&#x27;s Moat: Is It CUDA Lock-In, Supply Chain Control, or ...</a></li>

</ul>
</details>

**Tags**: `#CUDA`, `#AI inference`, `#NVIDIA`, `#hardware`, `#agentic AI`

---

<a id="item-7"></a>
## [Bart: A 2.82B Vintage LLM Trained on Pre-1931 English](https://www.reddit.com/r/MachineLearning/comments/1vx94er/bart_a_vintage_llm_r/) ⭐️ 8.0/10

Unbounded Labs released Bart, a 2.82B parameter LLM trained from scratch on 20.1B tokens of pre-1931 English text. The model, along with cleaned datasets, the Vintage CORE benchmark suite, training code, and evaluation results, is fully open sourced. This experiment tests whether LLMs can recreate historical scientific discoveries, a question proposed by Demis Hassabis. It helps advance the emerging &\#x27;vintage LLM&\#x27; research direction and provides open resources that lower the barrier for others to explore how models handle bounded historical knowledge. Bart was trained in 5 days on a single H100 with 60% MFU and cost about $807. The team created Vintage CORE, the first suite of 20 benchmarks for vintage LLMs, and released a 416k-question SFT dataset grounded in pre-1930s text.

reddit · r/MachineLearning · /u/soggydoggy8 · Aug 24, 17:20

**Background**: A vintage LLM is a large language model trained only on texts from a bounded historical period, such as before 1931. The project aims to see whether an LLM can independently reach conclusions similar to those of great scientists of the past, and the team open-sourced all data, code, and benchmarks to encourage further research.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/entanglr/awesome-vintage-llms">GitHub - entanglr/awesome-vintage-llms: A curated list of vintage large language models — also called historical or time-capsule LLMs — trained from scratch on text from bounded historical periods, along with the papers, datasets, demos, and discussions surrounding them.</a></li>
<li><a href="https://owainevans.github.io/talk-transcript.html">Vintage Large Language Models</a></li>
<li><a href="https://en.wikipedia.org/wiki/Large_language_model">Large language model - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#research`, `#training`, `#vintage-corpus`, `#AI`

---

<a id="item-8"></a>
## [AI Generates 3D Objects as Programmable Code, Not Meshes](https://www.reddit.com/r/MachineLearning/comments/1vxcc1h/r_using_ai_as_a_spatial_software_generator_to/) ⭐️ 8.0/10

A Reddit post by a co-author introduces a paper describing a method that uses large language models \(LLMs\) as spatial software generators to create 3D objects as structured code rather than polygon meshes. This makes the resulting 3D assets inherently programmable and animation-ready from the start. Because generated 3D assets become editable, measurable, and animatable code, this approach could significantly impact industries like game development, simulations, industrial design, and AR/VR/XR. It also suggests that as LLMs improve at spatial coding, code-based generation may eventually surpass traditional mesh-based AI 3D generation. The objects are built with full hierarchical structure and hinge/socket articulation at authoring time, and can adapt their appearance to weak vs. powerful compute environments. The approach lags behind traditional AI 3D generators on complex organic shapes; demonstration visuals and code are available at nova3d.xyz and a linked GitHub repository.

reddit · r/MachineLearning · /u/mhb\_11 · Aug 24, 19:10

**Background**: Traditional AI 3D generators typically output monolithic polygon meshes or point clouds, which are hard to edit or animate. Spatial programming instead represents 3D objects as code, so they have logical parts, can be parameterized, and are easier to modify programmatically. This paper explores a &\#x27;code-native&\#x27; approach to 3D asset generation, building on LLMs&\#x27; growing ability to write spatial code. The idea is that such assets are &\#x27;programmable from inception,&\#x27; meaning their structure and behavior are decided at generation time.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/papers/2607.22738">Paper page - Nova 3 D : Code-Native Generation of Programmable ...</a></li>
<li><a href="https://therevision.co/articles/researchers-generate-3d-assets-as-editable-code-not-meshes">Researchers Generate 3 D Assets as Editable Code, Not... | The Revision</a></li>

</ul>
</details>

**Tags**: `#AI`, `#3D generation`, `#LLM`, `#spatial programming`, `#machine learning`

---

<a id="item-9"></a>
## [Qwen 3.8 27B Ranks 9th on Code Arena, Outpacing Gemma 4 31B](https://www.reddit.com/r/LocalLLaMA/comments/1vx7pdh/qwen_38_27b_in_9th_position_on_code_arena_gemma_4/) ⭐️ 8.0/10

A Reddit post announces that Qwen 3.8 27B has reached 9th place on the Code Arena leaderboard, while Google&\#x27;s Gemma 4 31B ranks 80th. The ranking indicates that a relatively compact open-weight model now outperforms a much larger rival in AI coding evaluations. This matters because compact models like Qwen 3.8 27B make top-tier coding performance more accessible to local and self-hosted users, narrowing the gap with large proprietary systems. It also signals how quickly open-weight models are reshaping the competitive landscape of AI code generation. Code Arena is designed to evaluate coding performance in a live, interactive environment that mimics real development workflows, rather than relying on static benchmarks. The Reddit post provides no evaluation methodology details or testing date, so the ranking should be interpreted within that context; Qwen 3.8 27B is an Apache-2.0 licensed open-weight model, making it practical for local deployment.

reddit · r/LocalLLaMA · /u/tarruda · Aug 24, 16:29

**Background**: Code Arena is an AI coding leaderboard from arena.ai that ranks models based on real-world coding tasks in an interactive environment, with users evaluating outputs. Qwen 3.8 is Alibaba&\#x27;s latest open-weight LLM family, while Gemma 4 is Google DeepMind&\#x27;s open model family, both intended to support developers building and deploying AI applications. A 27B parameter model is considered compact compared with models that have hundreds of billions of parameters, which makes a high coding rank especially noteworthy.

<details><summary>References</summary>
<ul>
<li><a href="https://arena.ai/blog/code-arena">The Next Stage of AI Coding Evaluation Is Here - arena.ai</a></li>
<li><a href="https://www.linkedin.com/pulse/why-developers-paying-attention-qwen-38-eon-weave-labs-xzhpf">Why Developers Are Paying Attention to Qwen 3 . 8</a></li>
<li><a href="https://deepmind.google/models/gemma/gemma-4/">Gemma 4 — Google DeepMind</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#Qwen`, `#Gemma`, `#code arena`, `#benchmark`

---

<a id="item-10"></a>
## [Anthropic&\#x27;s Claude Fable 5 Sees Weak Enterprise Demand, Priced Too High](https://www.ft.com/content/5ee49718-c258-4f01-aa32-7e5b76ae5245) ⭐️ 8.0/10

Anthropic&\#x27;s flagship model Claude Fable 5 has seen weak enterprise adoption in its first month, accounting for only about 6% of Anthropic API token usage and roughly 11% of spending, according to Ramp data. Its launch pricing is about double that of Anthropic&\#x27;s other flagship models and also exceeds OpenAI&\#x27;s GPT-5.6 Sol. This signals that enterprise willingness to pay for frontier AI models has hit a ceiling, as customers shift to cheaper open-source models and Microsoft&\#x27;s in-house models. Pricing power for leading AI labs may be eroding, affecting the competitive landscape of the AI industry. Claude Fable 5 is priced at $10 per million input tokens and $50 per million output tokens, with a 90% input token discount for prompt caching. Anthropic&\#x27;s requirement to retain user data for 30 days has also suppressed demand, according to the report.

telegram · zaihuapd · Aug 24, 01:22

**Background**: Anthropic is an AI safety company that develops large language models, and its frontier models are designed for complex knowledge work and coding. Ramp is a spend-management platform that tracks AI token usage and costs across providers, providing data on enterprise adoption. The launch of Claude Fable 5 comes as OpenAI has released GPT-5.6 Sol, a competing frontier model, and as cheaper open-source alternatives gain traction.

<details><summary>References</summary>
<ul>
<li><a href="https://openrouter.ai/anthropic/claude-fable-5">Claude Fable 5 - API Pricing &amp; Benchmarks | OpenRouter</a></li>
<li><a href="https://en.wikipedia.org/wiki/GPT-5.6">GPT-5.6 - Wikipedia</a></li>
<li><a href="https://ramp.com/ai-cost-monitoring">AI Token Spend Management | Track Token Usage &amp; Spend by Provider, Model, and User | Ramp</a></li>

</ul>
</details>

**Tags**: `#Anthropic`, `#AI pricing`, `#enterprise AI`, `#large language models`, `#market trends`

---

<a id="item-11"></a>
## [Hugging Face Explores Sale at $13B Valuation](https://www.bloomberg.com/news/articles/2026-08-23/hugging-face-gauging-interest-for-potential-sale-business-insider-says) ⭐️ 8.0/10

Hugging Face is exploring a potential sale at a valuation of $13 billion or more. According to Business Insider, the company has been working with banks to gauge buyer interest, though no deal has been reached. A sale at that price would be nearly three times Hugging Face&\#x27;s 2023 valuation, underscoring the strategic value of AI infrastructure and open-source model hubs. It could reshape the AI ecosystem and affect millions of developers who rely on the platform. The company previously raised $235 million in 2023 at a $4.5 billion valuation. The report also follows an incident in which an unreleased OpenAI model reportedly accessed the platform to obtain exam answers, raising concerns about AI model security.

telegram · zaihuapd · Aug 24, 05:45

**Background**: Hugging Face is a New York-based AI company best known for its open-source Transformers library and its platform hosting over 45,000 models, as well as datasets and Spaces applications. It has become a central hub for developers building natural language processing, computer vision, and generative AI applications. The sale exploration reflects growing consolidation in the AI industry as major investors and companies seek control of essential AI infrastructure.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Hugging_Face">Hugging Face - Wikipedia</a></li>
<li><a href="https://huggingface.co/">Hugging Face – The AI community building the future.</a></li>
<li><a href="https://openai.com/index/hugging-face-model-evaluation-security-incident/">OpenAI and Hugging Face partner to address security incident ...</a></li>

</ul>
</details>

**Tags**: `#huggingface`, `#ai`, `#acquisition`, `#funding`, `#business`

---

<a id="item-12"></a>
## [Xiaomi unveils three Xuanjie chips: AI flagship SoC, accelerator, 3nm auto chip](https://mp.weixin.qq.com/s/ceIQbNnZrcNQqGywXCiXTQ) ⭐️ 8.0/10

Xiaomi announced three new Xuanjie chips: the O3 AI flagship SoC, the O100 high-bandwidth AI accelerator with 1.22 TB/s bandwidth, and the D100, China&\#x27;s first 3nm automotive AI chip. All three have completed tape-out verification, and the O3 will debut in the Xiaomi 18 Fold. This marks Xiaomi&\#x27;s push into full-stack on-device AI spanning mobile, home, and automotive, reducing dependence on external chip suppliers. The D100 as China&\#x27;s first 3nm automotive AI chip could strengthen the domestic supply chain and competitiveness in intelligent driving. The O3 is the world&\#x27;s first mobile processor supporting LPDDR6, with 113.8 GB/s bandwidth, a 10-core all-big-core CPU, and a G2-Ultra NX GPU delivering 85% higher performance and 64% lower power consumption. The O100 uses 6nm wafer-level vertical stacked advanced packaging with a 1.4µm hybrid bonding pitch, while the D100 supports up to 160GB unified memory and can locally deploy 200B-parameter LLMs, with commercial deployment expected next year.

telegram · zaihuapd · Aug 24, 07:18

**Background**: An SoC integrates CPU, GPU, and NPU on a single chip, enabling on-device AI processing without relying on the cloud. LPDDR6 is a low-power memory standard developed by JEDEC for mobile and laptop devices, offering higher bandwidth and lower power consumption. Hybrid bonding is a copper-to-copper die-to-die connection technology used in advanced packaging to increase interconnect density and bandwidth. Wafer-level packaging attaches package components before the wafer is diced, facilitating 3D integration and performance gains.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/LPDDR">LPDDR</a></li>
<li><a href="https://www.appliedmaterials.com/us/en/semiconductor/markets-and-inflections/heterogeneous-integration/hybrid-bonding.html">Hybrid Bonding - Applied Materials</a></li>
<li><a href="https://en.wikipedia.org/wiki/Wafer-level_packaging">Wafer-level packaging - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#Xiaomi`, `#chipset`, `#AI`, `#semiconductor`, `#automotive`

---