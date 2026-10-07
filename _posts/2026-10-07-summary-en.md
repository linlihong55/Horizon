---
layout: default
title: "Horizon Summary: 2026-10-07 (EN)"
date: 2026-10-07
lang: en
---

> From 41 items, 5 important content pieces were selected

---

1. [OpenAI Releases AI-Generated Proofs for Dozens of Open Math Problems](#item-1) ⭐️ 10.0/10
2. [Francis Halzen Wins 2026 Nobel Prize in Physics for IceCube Neutrino Detector](#item-2) ⭐️ 9.0/10
3. [Mistral Large 4 preview: 1T-parameter MoE with promised open weights](#item-3) ⭐️ 9.0/10
4. [Google Releases EmbeddingGemma 2, an Apache 2.0 Multimodal Embedding Model](#item-4) ⭐️ 8.0/10
5. [Apple Opens App Store Submissions for Foldable iPhone Duo Apps](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI Releases AI-Generated Proofs for Dozens of Open Math Problems](https://openai.com/index/sharing-ai-progress-in-mathematics/) ⭐️ 10.0/10

OpenAI published a GitHub repository \(openai/math\) containing AI-generated mathematical proofs and preprints that claim progress on numerous long-standing open problems in mathematics. Community members quickly noted that the list appears to claim full solutions to 90 of the top 500 open problems tracked by proofatlas.ai, including high-ranked entries such as Hilbert&\#x27;s tenth problem over ℚ, the Unique Games Conjecture and the Baum–Connes Conjecture. If even a fraction of these results hold up, it would mark a paradigm shift in how mathematics is done, potentially resolving problems that have shaped pure mathematics and theoretical computer science for decades. It would also intensify the debate over whether AI systems can genuinely contribute original mathematical insight rather than merely recombining existing human knowledge. The claims span a wide range of fields, including a proof of Barnette&\#x27;s Conjecture in graph theory, results on the Unique Games Conjecture, a polynomial-time algorithm for three-machine unit-job scheduling \(open since Garey and Johnson&\#x27;s 1979 book\), and a claimed solution to Hilbert&\#x27;s tenth problem over ℚ. A key caveat is that these are AI-produced preprints that have not necessarily been peer-reviewed or formally verified in a proof assistant such as Lean.

hackernews · OfficialTurkey · Oct 6, 22:17 · [Discussion](https://news.ycombinator.com/item?id=49984923)

**Background**: Automated theorem proving is a subfield of automated reasoning in which computer programs attempt to prove mathematical statements — an idea that helped motivate the development of computer science itself. In recent years, large language models fine-tuned for mathematical reasoning have begun producing candidate proofs, while proof assistants like Lean allow proofs to be checked mechanically. The Unique Games Conjecture, mentioned prominently here, is a foundational conjecture in complexity theory that underpins many known inapproximability results.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Automated_theorem_proving">Automated theorem proving</a></li>
<li><a href="https://www.wolframcloud.com/obj/jayantap/AIMath2025-26">AI for Mathematics : 2025–2026 Digest</a></li>

</ul>
</details>

**Discussion**: The Hacker News discussion is highly engaged and substantive, with domain experts flagging specific ambitious claims such as the Barnette&\#x27;s Conjecture proof, the Unique Games Conjecture and the scheduling result, while one commenter quotes Kevin Buzzard&\#x27;s 2020 question about what a single mind grasping all of modern pure mathematics could see. Sentiment mixes excitement about the scale of the claims with caution: several commenters stress verification, and others debate the relative importance of individual results.

**Tags**: `#AI`, `#mathematics`, `#OpenAI`, `#theorem-proving`, `#research`

---

<a id="item-2"></a>
## [Francis Halzen Wins 2026 Nobel Prize in Physics for IceCube Neutrino Detector](https://www.nobelprize.org/prizes/physics/2026/) ⭐️ 9.0/10

The 2026 Nobel Prize in Physics was awarded to Francis Halzen, the principal investigator of the IceCube Neutrino Observatory, for conceiving the cubic-kilometer neutrino detector built in the Antarctic ice at the Amundsen–Scott South Pole Station. The citation recognizes his decisive contributions to IceCube and to the discovery of high-energy neutrinos of astrophysical origin. The award confirms neutrino astronomy as a mature observational window, complementing light-based and gravitational-wave astronomy and enabling multi-messenger studies of the most energetic processes in the universe. It also validates a decades-long, high-risk engineering bet on an international facility that many initially considered impractical. IceCube consists of thousands of spherical digital optical modules \(DOMs\) — each containing a photomultiplier tube and data-acquisition electronics — deployed on strings of 60 at depths between 1,450 and 2,450 meters in holes melted with hot-water drills, and it was completed on 18 December 2010. The detector works by catching the faint blue Cherenkov radiation emitted by charged particles produced when a neutrino interacts with the ice; an upgrade approved in 2019 was announced on 12 February 2026 to have been successfully deployed, its first major expansion in 15 years.

hackernews · solarist · Oct 6, 09:48 · [Discussion](https://news.ycombinator.com/item?id=49976265)

**Background**: Neutrinos are nearly massless, electrically neutral elementary particles produced in nuclear reactions inside stars, in supernovae and in radioactive decay; they interact only through the weak nuclear force and gravity, so trillions can pass through the entire planet unnoticed. Because they are so hard to catch, neutrino detectors must be enormous and shielded from cosmic rays, which is why IceCube uses a cubic kilometer of Antarctic ice as both the target material and the detection medium, studied by its predecessor AMANDA and joined by facilities such as Super-Kamiokande in Japan and ANTARES and KM3NeT in the Mediterranean. Unlike photons, neutrinos travel in straight lines without being absorbed or deflected by magnetic fields, making them a uniquely clean messenger from otherwise inaccessible sources such as the cores of stars and violent cosmic accelerators.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/IceCube_Neutrino_Observatory">IceCube Neutrino Observatory</a></li>
<li><a href="https://en.wikipedia.org/wiki/Neutrino_astronomy">Neutrino astronomy</a></li>
<li><a href="https://icecube.wisc.edu/">IceCube Neutrino Observatory</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters were enthusiastic and explanatory: one long breakdown described neutrinos as abundant “ghost particles” that pass through planets unimpeded, while another explained the detection chain of neutrino-to-charged-particle conversion and Cherenkov radiation. Several people shared personal connections — one said he helped with construction at the South Pole in 2009, another recalled a colleague who flew there just to install Debian on the data-processing systems — and many praised the sheer boldness of the project as something out of science fiction.

**Tags**: `#Nobel Prize`, `#Physics`, `#Neutrino Astronomy`, `#IceCube`, `#Science`

---

<a id="item-3"></a>
## [Mistral Large 4 preview: 1T-parameter MoE with promised open weights](https://simonwillison.net/2026/Oct/6/le-chonk/) ⭐️ 9.0/10

Mistral released a preview of Mistral Large 4, nicknamed &quot;Le chonk&quot;, a 1-trillion-parameter mixture-of-experts model with 49 billion active parameters, trained from scratch on Mistral&\#x27;s own cluster of 3,800 NVIDIA Grace Blackwell GPUs in Europe. The preview is available now through the Mistral API, with Mistral promising to release the open-weight version by the end of the month. This marks Mistral&\#x27;s return to competitiveness in the open-weight LLM race after a weak Mistral Large 3 release, and the promise of open weights for a trillion-parameter model matters for the whole ecosystem of developers and companies that cannot or will not rely on closed US and Chinese frontier APIs. The fact that it was trained entirely on European soil on a relatively modest 3,800-GPU cluster also makes it a notable data point for EU AI sovereignty and for debates about how much compute is really needed at the frontier. On Artificial Analysis the model scores 38, just behind the 552B DeepSeek 4.1 Flash, a huge jump from Mistral Large 3&\#x27;s score of 9 last December — though Simon Willison notes it still appears to be roughly six months behind the frontier, and not a &quot;Fable-class&quot; model. The API exposes only two reasoning levels, &quot;none&quot; and &quot;high&quot;, and in Willison&\#x27;s test the &quot;high&quot; setting barely changed behavior, even producing fewer output tokens \(2,717\) than &quot;none&quot; \(3,275\).

rss · Simon Willison · Oct 6, 20:18

**Background**: A mixture-of-experts \(MoE\) model splits its parameters into many specialized &quot;expert&quot; sub-networks and only activates a small fraction of them for each token, which lets a model have a very large total parameter count while keeping inference and training costs closer to those of a much smaller dense model — hence 1T total but only 49B active parameters here. NVIDIA&\#x27;s Grace Blackwell \(GB200\) is Nvidia&\#x27;s current-generation GPU platform, successor to Hopper, in which Grace CPUs and Blackwell GPUs are combined and linked via NVLink so a rack can act as one large accelerator, which is why a cluster of a few thousand such GPUs is enough to train a trillion-parameter model. &quot;Open weights&quot; means the trained model parameters are published for anyone to download and run themselves, as opposed to only being accessible through a vendor&\#x27;s API.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Blackwell_%28microarchitecture%29">Blackwell (microarchitecture) - Wikipedia</a></li>
<li><a href="https://www.nvidia.com/en-us/data-center/gb200-nvl72/">GB200 NVL72 | NVIDIA</a></li>
<li><a href="https://arxiv.org/html/2507.11181v1">Mixture of Experts in Large Language Models</a></li>

</ul>
</details>

**Discussion**: Commenters were broadly positive: one noted the reasoning &quot;none&quot;/&quot;high&quot; switch made little practical difference, while others praised strong vision and cybersecurity benchmarks and reported that on a Plotly analytics benchmark it went from 58% to 74% correct at roughly 10x lower cost than Mistral Medium 3.5. Several saw strategic value beyond raw capability, arguing the EU-trained, EU-hosted inference makes it important for European sovereignty even if it is not the best model overall, and one asked how a mere ~4,000-GPU run can nearly match far larger Chinese-labs&\#x27; efforts — implying efficiency gains deserve more attention.

**Tags**: `#Mistral`, `#large language models`, `#open weights`, `#mixture-of-experts`, `#AI model release`

---

<a id="item-4"></a>
## [Google Releases EmbeddingGemma 2, an Apache 2.0 Multimodal Embedding Model](https://blog.google/innovation-and-ai/technology/developers-tools/embeddinggemma-2/) ⭐️ 8.0/10

Google released EmbeddingGemma 2, a lightweight embedding model that handles both text and vision and is published under the commercially permissive Apache 2.0 license. Community members highlight a roughly 270M-parameter text-only configuration and a roughly 440M-parameter text-plus-vision configuration, positioning it among the strongest multimodal embedding models under 1B parameters. Embedding models are used at scale — applications often compute and store thousands to millions of vectors — so a permissively licensed model removes the risk that a vendor eventually retires a proprietary hosted embedding endpoint and invalidates stored vectors. It also fills a widely felt gap: despite rapid progress in LLMs and agents, there had been few good open, moderate-sized embedding models, and this one covers vision too. According to the model card, EmbeddingGemma 2 natively produces 768-dimensional embeddings that can be truncated to 128, 256, and 512 dimensions via Matryoshka Representation Learning \(MRL\) and re-normalized, which lets developers trade accuracy for storage and latency. Its lightweight footprint makes it suitable for local and on-device use rather than only GPU-backed server deployment.

hackernews · ilreb · Oct 6, 16:03 · [Discussion](https://news.ycombinator.com/item?id=49980487)

**Background**: An embedding model converts text, images, or other data into numeric vectors so that semantically similar items end up close together in a shared vector space; this is the foundation of semantic search, retrieval-augmented generation \(RAG\), recommendation, and deduplication. Multimodal embedding models place text and images in the same space, so a text query can retrieve relevant images and vice versa. Matryoshka Representation Learning trains the model so that a prefix of the vector is itself a usable, smaller embedding, enabling flexible dimensionality. Gemma is Google DeepMind&\#x27;s family of lightweight open models built from the same technology behind Gemini.

<details><summary>References</summary>
<ul>
<li><a href="https://ai.google.dev/gemma/docs/embeddinggemma/model_card_2">EmbeddingGemma 2 model card | Google AI for Developers</a></li>
<li><a href="https://huggingface.co/google/embeddinggemma-2">google/ embeddinggemma - 2 · Hugging Face</a></li>
<li><a href="https://blog.google/innovation-and-ai/technology/developers-tools/embeddinggemma-2/">EmbeddingGemma 2 is a best-in-class open model for natively...</a></li>

</ul>
</details>

**Discussion**: Sentiment on Hacker News was strongly positive \(224 points, 29 comments\). simonw praised the Apache 2.0 license, arguing that hosted-only proprietary embedding models are risky because stored vectors break when a vendor retires a model, while minimaxir welcomed finally having a good moderate-size embedding model that is also multimodal. kaycebasques raised a technical question about whether binary quantization could be used instead of MRL, and flockonus noted the release is likely close to what Google ships on Android phones.

**Tags**: `#embeddings`, `#machine-learning`, `#multimodal`, `#open-source`, `#gemma`

---

<a id="item-5"></a>
## [Apple Opens App Store Submissions for Foldable iPhone Duo Apps](https://www.macrumors.com/2026/10/05/apple-opens-iphone-duo-app-submissions/) ⭐️ 8.0/10

Apple announced that apps optimized for the iPhone Duo, its first foldable iPhone, can now be submitted to the App Store for review ahead of the device&\#x27;s October 23, 2026 launch. To take full advantage of the inner display with dynamic resizing, apps must be built with the iOS 27.1 SDK or later, which developers can prepare using Xcode 27.1. This is the starting gun for iOS developers to prepare for Apple&\#x27;s first foldable form factor, and apps that ship without SDK 27.1 support will run in a letterboxed or non-adaptive mode on the larger inner screen. It signals the beginning of a broader shift toward adaptive, resizable iOS layouts across Apple&\#x27;s lineup, likely well beyond the Duo itself. Apple notes that most existing iPhone apps will run on the Duo without modification, but hardcoded screen sizes, fixed orientations, and device assumptions can break layouts, causing stretched or clipped interfaces. Apps built with SDK 26 can still be submitted for now; Apple is expected to mandate SDK 27 around April 2027.

telegram · zaihuapd · Oct 6, 03:36

**Background**: The iPhone Duo is Apple&\#x27;s first foldable iPhone, unveiled at an Apple Park event on September 9, 2026 alongside the iPhone 18 Pro and iPhone 18 Pro Max. When opened, it offers a 7.6-inch inner display with a nano-texture finish that reduces glare, and its dual-display system supports new poses and orientations. &quot;Dynamic resizing&quot; means an app expands to fill the inner screen when unfolded and contracts to the outer display when folded, which is why the SDK version determines whether an app can adapt cleanly or must fall back to a fixed layout.

<details><summary>References</summary>
<ul>
<li><a href="https://www.apple.com/newsroom/2026/09/apple-unveils-iphone-duo/">Apple unveils iPhone Duo</a></li>
<li><a href="https://developer.apple.com/iphone-duo/prepare/">Prepare - iPhone Duo - Apple Developer</a></li>
<li><a href="https://en.wikipedia.org/wiki/IPhone_Duo">iPhone Duo - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#Apple`, `#iPhone Duo`, `#foldable devices`, `#App Store`, `#iOS development`

---