---
layout: default
title: "Horizon Summary: 2026-09-17 (EN)"
date: 2026-09-17
lang: en
---

> From 36 items, 3 important content pieces were selected

---

1. [Nvidia launches two official Rust tracks for CUDA GPU kernels](#item-1) ⭐️ 8.0/10
2. [Flock License Plate Cameras Found Riddled With Hardcoded Credentials](#item-2) ⭐️ 8.0/10
3. [TMLR probes 10 desk-rejected papers; authors mostly can&\#x27;t explain them](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Nvidia launches two official Rust tracks for CUDA GPU kernels](https://developer.nvidia.com/blog/introducing-cuda-rust-two-tracks-for-writing-gpu-kernels/) ⭐️ 8.0/10

Nvidia announced two official tracks for writing native CUDA GPU kernels in Rust: cuda-oxide, a custom rustc codegen backend that compiles SIMT-style Rust kernels directly to PTX using the Pliron IR framework and LLVM, and cutile-rs, which enables tile-based GPU programming in stable Rust through CUDA Tile IR JIT compilation. Both approaches enforce memory safety at compile time rather than at runtime. This is the first time Nvidia has offered first-class, officially supported pathways for Rust GPU kernel development, which could shift how a growing share of GPU code is written and reduce the friction that has kept Rust workloads tied to C++ CUDA. It also strengthens the wider Rust machine-learning stack, particularly inference frameworks such as HuggingFace&\#x27;s Candle. cuda-oxide relies on DisjointSlice and launch contracts to prevent aliasing, while cutile-rs uses tensor partitioning and ownership to guarantee exclusive access to memory regions. A notable design choice is that kernel launches are checked rather than trusted, meaning the host-side compiler verifies the safety preconditions of each launch instead of assuming the programmer got them right.

hackernews · nonmaskable · Sep 16, 11:15 · [Discussion](https://news.ycombinator.com/item?id=49724881)

**Background**: A CUDA kernel is a function executed in parallel across many GPU threads; in traditional CUDA C++ it is marked with the \_\_global\_\_ specifier, receives pointers to global device memory, and typically mutates that memory rather than returning values. Rust is a systems programming language whose borrow checker and ownership rules give compile-time memory-safety guarantees, which is appealing for GPU code where data races and aliasing are common failure modes. Candle is HuggingFace&\#x27;s minimalist Rust ML framework focused on performance and GPU support, and it is a key piece of Rust-based inference tooling that native CUDA kernels could accelerate.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/introducing-cuda-rust-two-tracks-for-writing-gpu-kernels/">Introducing CUDA Rust: Two Tracks for Writing GPU Kernels | NVIDIA Technical Blog</a></li>
<li><a href="https://github.com/huggingface/candle">GitHub - huggingface / candle : Minimalist ML framework for Rust</a></li>
<li><a href="https://cvw.cac.cornell.edu/gpu-architecture/gpu-characteristics/kernel_sm">Cornell Virtual Workshop &gt; Understanding GPU Architecture &gt; GPU Characteristics &gt; Kernels and SMs</a></li>

</ul>
</details>

**Discussion**: The Hacker News thread \(221 points, 75 comments\) is broadly enthusiastic but skeptical of Nvidia&\#x27;s proprietary ecosystem: one commenter \(jacobgorm\) argues that once CUDA enters a codebase it is hard to remove and leads to vendor lock-in or \#ifdef hell, recommending explicit kernel files and manual launches as in Metal, OpenCL or D3D12. Others \(Driftbench\) welcome Rust&\#x27;s safety as a potential game changer for kernel programming, while dllu ties the news to HuggingFace&\#x27;s Candle inference crate, and several commenters \(claiir, LarsDu88\) note with irony that even Nvidia&\#x27;s announcement appears heavily LLM-written — though one says it has revived their interest in learning Rust since LLMs have not yet been trained on it.

**Tags**: `#Rust`, `#CUDA`, `#GPU Programming`, `#Nvidia`, `#Systems Programming`

---

<a id="item-2"></a>
## [Flock License Plate Cameras Found Riddled With Hardcoded Credentials](https://www.wired.com/story/hackers-flock-camera-data-shows-how-system-works/) ⭐️ 8.0/10

Security researcher Micah Lee reported that Flock Safety&\#x27;s license-plate-reading surveillance cameras are riddled with security vulnerabilities, including a hardcoded API key that can be used to request plaintext-stored credentials for Flock&\#x27;s servers. The reporting, done in collaboration with 404 Media, was accompanied by Distributed Denial of Secrets publishing partition images of the cameras&\#x27; firmware. The case has become a flashpoint in the broader debate over IoT and surveillance-device security, since cameras deployed in public spaces carry a threat model that explicitly includes physical access by attackers. It also highlights how companies can adopt vulnerability disclosure policies that create the appearance of a responsible security posture while discouraging meaningful reports. The hardcoded credential in question is an API key rather than an admin password, and it can be used to retrieve credentials stored in plaintext; it remains unclear exactly what an attacker could do after authenticating as a camera. Flock&\#x27;s vulnerability disclosure policy welcomes reports except in cases where a researcher must &quot;interact&quot; with the device or service, or download its data — carve-outs that exclude nearly all meaningful hardware testing.

hackernews · driverdan · Sep 16, 13:18 · [Discussion](https://news.ycombinator.com/item?id=49726586)

**Background**: Flock Safety makes automated license plate readers \(ALPRs\), AI-powered cameras that scan every passing vehicle&\#x27;s plate and characteristics and cross-reference the data against watchlists such as stolen-vehicle databases and AMBER alerts. Hardcoded credentials are a classic vulnerability class \(CWE-798\): because the secret is baked into firmware, it cannot be rotated without redeploying or reflashing the device. A vulnerability disclosure policy is the formal process by which researchers report flaws to a vendor, and its scope determines whether legitimate security research is welcomed or legally discouraged.

<details><summary>References</summary>
<ul>
<li><a href="https://trafficvision.live/blog/flock-cameras">Flock Cameras : What They Are &amp; Can You Watch... | TrafficVision.Live</a></li>
<li><a href="https://cwe.mitre.org/data/definitions/798.html">CWE - CWE-798: Use of Hard - coded Credentials (4.20)</a></li>
<li><a href="https://www.bugcrowd.com/blog/vulnerability-disclosure-policy-what-is-it-why-is-it-important/">Vulnerability Disclosure Policy : What is It &amp; Why is it... | @Bugcrowd</a></li>

</ul>
</details>

**Discussion**: Commenters were largely harsh: one called hardcoded credentials &quot;a sign of total incompetence,&quot; another described Flock&\#x27;s VDP as existing mainly to create the appearance of responsible security, and a third attributed the flaws to laziness and &quot;reduced time to market&quot; that ignored the reality that public-space hardware faces local physical access. Others noted the collaboration with 404 Media and that Distributed Denial of Secrets had published the camera partition images, with one commenter observing the data is &quot;literally there for any unauthorized person to walk up and take.&quot;

**Tags**: `#security`, `#IoT`, `#surveillance`, `#vulnerabilities`, `#privacy`

---

<a id="item-3"></a>
## [TMLR probes 10 desk-rejected papers; authors mostly can&\#x27;t explain them](https://www.reddit.com/r/MachineLearning/comments/1wid67h/tmlr_reached_out_to_the_authors_of_10_papers/) ⭐️ 8.0/10

TMLR&\#x27;s Co-Editor-in-Chief contacted the authors of 10 submissions that were slated for desk rejection and asked them to explain their own work. Of the ten: one withdrew, one cited other commitments, one scheduled a meeting but never showed up, three could not answer basic questions about the paper, three handled high-level ideas but stumbled on technical details, and only one answered all questions — though the interviewer still identified a major flaw in that paper. This is direct, first-hand evidence that a substantial share of submissions reaching ML peer review may be LLM-generated or produced by paper mills, which threatens the integrity of the review pipeline that the whole research community depends on. It gives journals a concrete, low-cost screening technique and puts author accountability at the center of the debate over how AI-assisted writing should be policed. The test used was simply a conversation about the submission, so it requires editorial time rather than any technical tooling, and it cannot by itself prove LLM authorship — it mainly exposes authors who lack genuine familiarity with their own claims. Notably, even the single author who answered everything competently had a major flaw found in the paper, showing that passing this interview is not a proxy for scientific quality.

reddit · r/MachineLearning · /u/hihey54 · Sep 16, 23:20

**Background**: TMLR is a machine learning journal founded in late 2021 as a complement to JMLR, using OpenReview and a rolling review process; a desk rejection means an editor rejects a submission outright before sending it out for peer review, typically for scope, formatting, or quality reasons. Paper mills are companies or operations that mass-produce and sell scientific manuscripts, often fabricated or plagiarized, to researchers under pressure to publish. As generative models have become cheap and capable, editors have grown concerned that such manuscripts — or wholly LLM-written papers — are increasingly slipping past initial screening.

<details><summary>References</summary>
<ul>
<li><a href="https://jmlr.org/tmlr/">Transactions on Machine Learning Research (TMLR)</a></li>
<li><a href="https://en.wikipedia.org/wiki/Research_paper_mill">Research paper mill - Wikipedia</a></li>
<li><a href="https://www.aischolar.com/news/article/is-desk-rejection-common">Is Desk Rejection Common?</a></li>

</ul>
</details>

**Tags**: `#peer-review`, `#research-integrity`, `#LLM-generated-papers`, `#machine-learning`, `#academic-publishing`

---