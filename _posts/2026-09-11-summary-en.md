---
layout: default
title: "Horizon Summary: 2026-09-11 (EN)"
date: 2026-09-11
lang: en
---

> From 36 items, 5 important content pieces were selected

---

1. [Calif Research demos WeWorm, first zero-click worm via WeChat calls](#item-1) ⭐️ 9.0/10
2. [Shopify Abandons React Native for Native Swift and Kotlin](#item-2) ⭐️ 8.0/10
3. [Researchers question whether OpenAI can be trusted with unpublished math](#item-3) ⭐️ 8.0/10
4. [Microsoft Elevates Rust to Tier-1 Language Status](#item-4) ⭐️ 8.0/10
5. [trynix.dev boots any Nix package from 13 years in your browser](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Calif Research demos WeWorm, first zero-click worm via WeChat calls](https://simonwillison.net/2026/Sep/10/calif-research/) ⭐️ 9.0/10

Calif Research published a demo of WeWorm, which it claims is the first zero-click worm that spreads through WeChat calls on both iOS and Android. The team says it used AI to find the bug and write a first remote code execution \(RCE\) exploit in roughly two days, then spent about one more week turning that exploit into a self-spreading worm. It suggests AI can compress what used to be months of work by a large offensive-security team into about nine days for a small one, sharply lowering the cost of building wormable mobile exploits. If the claim holds up, it raises urgent questions for messaging platforms and mobile OS vendors about how quickly weaponized zero-click exploits can now be produced. According to the announcement, the victim does not need to answer the call or interact with the phone at all, and even if they do answer they hear nothing while the exploit still succeeds. The excerpt is brief and does not include a technical advisory, affected WeChat versions, or patch status, so the underlying bug class and real-world exploitability beyond the demo remain unverified.

rss · Simon Willison · Sep 10, 00:56

**Background**: A zero-click exploit compromises a device without any action from the user, typically by abusing software such as a messaging or calling stack that automatically processes incoming data. Remote code execution \(RCE\) is the ability to run arbitrary attacker-chosen code on a target machine over a network. WeChat is one of the world&\#x27;s most widely used messaging apps with well over a billion users, and a worm is malware that copies and spreads itself automatically from victim to victim. AI-assisted exploit development uses large language models to speed up tasks like reverse engineering, fuzzing and writing exploit code, a trend that security researchers have flagged as accelerating offensive work.

<details><summary>References</summary>
<ul>
<li><a href="https://grokipedia.com/page/Zero-click_exploit">Zero-click exploit</a></li>
<li><a href="https://en.wikipedia.org/wiki/Remote_code_execution">Remote code execution</a></li>
<li><a href="https://leanpub.com/ai-assistedexploitdevelopment">AI - Assisted Exploit Development [Leanpub PDF/iPad/Kindle]</a></li>

</ul>
</details>

**Tags**: `#ai-security-research`, `#cybersecurity`, `#zero-click-exploit`, `#wechat`, `#rce`

---

<a id="item-2"></a>
## [Shopify Abandons React Native for Native Swift and Kotlin](https://shopify.engineering/back-to-native) ⭐️ 8.0/10

Shopify Engineering published a post titled &quot;Native is now the future of mobile at Shopify,&quot; announcing that it is moving its mobile apps off React Native and back to fully native Swift for iOS and Kotlin for Android. The decision triggered a 497-comment Hacker News discussion in which mobile engineers debated whether shared codebases are worth the debugging and maintenance costs. Shopify is one of the largest and most visible companies to publicly reverse a React Native migration, directly challenging the &quot;write once, run anywhere&quot; pitch that has driven cross-platform adoption for years. For teams weighing React Native, Flutter, or native development, this case study shifts the default assumption that a shared codebase is always the economical choice. A recurring technical argument in the discussion is that debugging crashes spanning JavaScript, C++ and native threads costs more than maintaining two separate codebases, and that platform teams want engineers who can optimize specifically for iOS or Android. Commenters also debated whether AI coding assistants now make such migrations cheap enough to be routine, with at least one practitioner arguing their own React Native-to-native rewrite was mostly completed before LLM assistance was available.

hackernews · fnthawar2 · Sep 10, 14:09 · [Discussion](https://news.ycombinator.com/item?id=49643982)

**Background**: React Native, created by Meta, lets developers write mobile apps in JavaScript, but under the hood it must still communicate with platform-native code; the original architecture used an asynchronous JSON &quot;bridge,&quot; while the newer architecture replaces it with JavaScript Interface \(JSI\) so JavaScript can hold direct C++ references to native methods. Native development, by contrast, means writing separate Swift apps for iOS and Kotlin apps for Android, which gives better performance and platform integration at the cost of two codebases. The long-running tradeoff debate is whether the savings from a single shared codebase outweigh the extra friction of debugging across layers.

<details><summary>References</summary>
<ul>
<li><a href="https://reactnative.dev/architecture/landing-page">About the New Architecture · React Native</a></li>
<li><a href="https://apptitude.io/blog/cross-platform-vs-native/">Cross-Platform vs Native App Development: The Real Trade-Offs</a></li>
<li><a href="https://dev.to/subraatakumar/the-death-of-the-react-native-bridge-moving-from-json-to-jsi-in-2026-2614">The Death of the React Native Bridge: Moving from JSON to JSI in 2026 - DEV Community</a></li>

</ul>
</details>

**Discussion**: Sentiment is broadly sympathetic to Shopify, with commenters calling the move &quot;very validating&quot; after years of arguing against shared codebases pushed by management. The main disagreement concerns the role of AI: some see LLM-assisted migration \(one commenter described porting a 15–20 screen app to iOS and Android overnight using Codex and Maestro\) as the reason the switch is now viable, while another practitioner insists the LLM narrative is overstated since their own native rewrite predated such tooling. A common conclusion is that React Native made sense for startups leveraging web developers, but growing apps eventually want dedicated native engineers.

**Tags**: `#react-native`, `#mobile-development`, `#swift`, `#kotlin`, `#cross-platform`

---

<a id="item-3"></a>
## [Researchers question whether OpenAI can be trusted with unpublished math](https://mathstodon.xyz/@andreasthom/117240535270608201) ⭐️ 8.0/10

A Hacker News discussion \(636 points, 614 comments\) is debating whether mathematicians can still trust OpenAI with unpublished research, sparked by Mathstodon, X and Bluesky posts alleging that OpenAI used ideas from collaborative chats with researchers without attribution. The thread links directly to the Mastodon posts by @andreasthom on mathstodon.xyz that raised the concern. If substantiated, the allegations would undermine the informal trust that gives AI labs early access to cutting-edge mathematical work, potentially pushing mathematicians to withhold unpublished results. More broadly, it forces the research community to define attribution and credit norms now that AI systems increasingly participate in discovery. Commenters flag several unresolved specifics: it is unclear whether the model that produced the disputed result was even trained on the collaborative chats, OpenAI has reportedly given on the order of 100,000 researchers free access to its models, and one comment finds it suspicious that OpenAI generated roughly 300 billion output tokens from a still-in-training model soon after learning a major proof might be in its training data.

hackernews · pred\_ · Sep 10, 06:49 · [Discussion](https://news.ycombinator.com/item?id=49639408)

**Background**: Mathstodon.xyz is a Mastodon \(fediverse\) instance aimed at people who love mathematics, and the thread that ignited this debate was posted there; the linked X post can also be read through the Nitter-based frontend xcancel.com, and the Bluesky post uses a did:plc identifier rather than a plain handle. The technical backdrop is that large language models are usually pretrained on enormous text corpora and then further improved with reinforcement learning on tasks with verifiable answers such as math problems — two very different mechanisms that determine where a model&\#x27;s apparent &\#x27;insight&\#x27; actually came from. In mathematics, crediting whoever supplied an idea or a step of a proof is a core professional norm, which is why uncredited use of a conversation is treated so seriously.

<details><summary>References</summary>
<ul>
<li><a href="https://mathstodon.xyz/">About - Mathstodon</a></li>
<li><a href="https://en.wikipedia.org/wiki/Nitter">Nitter - Wikipedia</a></li>
<li><a href="https://atproto.wiki/en/wiki/reference/identifiers/did-plc">DID:PLC | AT Protocol Community Wiki</a></li>

</ul>
</details>

**Discussion**: Sentiment is largely skeptical of OpenAI. One prominent analogy compares OpenAI to a human collaborator who took researchers&\#x27; ideas and then published along those lines without credit, which would be plainly unethical if the collaborator were human; others argue both things can be true at once — pretraining on chats sharpens the model&\#x27;s intuition while RL on verifiable math genuinely discovers superhuman techniques; and some question whether reported rapid progress on open problems is real or an artifact of fresh, unpublished training data.

**Tags**: `#OpenAI`, `#AI ethics`, `#research integrity`, `#mathematics`, `#academia`

---

<a id="item-4"></a>
## [Microsoft Elevates Rust to Tier-1 Language Status](https://rustfoundation.org/media/guest-post-rust-is-tier-1-language-at-microsoft/) ⭐️ 8.0/10

In a guest post published on the Rust Foundation&\#x27;s website, Microsoft announced that Rust now holds &quot;tier-1 language&quot; engineering status internally, placing it alongside C++, C\#, and TypeScript as one of the company&\#x27;s best-supported languages for internal development. The post points to multiple core Microsoft projects already powered by Rust and follows earlier keynotes on the company&\#x27;s Rust adoption. The designation is a strong industry validation of Rust from one of the world&\#x27;s largest software vendors, and it signals that all major OS vendors with a stake in C and C++ tooling are now diversifying their systems-programming options for greenfield work. For developers and enterprises weighing a C/C++ successor, Microsoft&\#x27;s endorsement lowers the perceived risk of adopting Rust at scale. The post frames tier-1 status as an engineering-support commitment rather than a mandate, and commenters note it coincides with long-running rumors about Rust integration into the MSVC toolchain. Community members also point to Microsoft&\#x27;s stated ambition to convert 1 billion lines of C/C++ to Rust by 2030 using automated tooling, and to DARPA-funded research distributing C-to-Rust translation across six different teams.

hackernews · mmastrac · Sep 10, 13:39 · [Discussion](https://news.ycombinator.com/item?id=49643546)

**Background**: Rust was created by Graydon Hoare at Mozilla in 2006, reached its first stable release \(1.0\) in May 2015, and has been stewarded by the nonprofit Rust Foundation since February 2021. Its defining feature is compile-time memory safety enforced by the &quot;borrow checker&quot;, which prevents memory errors and data races without a garbage collector. That property matters to large vendors like Microsoft because memory-safety flaws account for a majority of the CVEs in their C and C++ codebases. Tier-1 language status at Microsoft means first-class internal tooling, training, and support, comparable to C++, C\#, and TypeScript.

<details><summary>References</summary>
<ul>
<li><a href="https://rustfoundation.org/media/guest-post-rust-is-tier-1-language-at-microsoft/">Guest Post: Rust Is Tier - 1 Language at Microsoft</a></li>
<li><a href="https://en.wikipedia.org/wiki/Rust_%28programming_language%29">Rust (programming language) - Wikipedia</a></li>
<li><a href="https://blog.jetbrains.com/rust/2026/07/27/cpp-to-rust-migration/">C++ to Rust Migration: By Luca Palmieri from Mainmatter</a></li>

</ul>
</details>

**Discussion**: Hacker News reaction was largely positive but nuanced: commenters welcomed the signal that Rust is a mature, serious competitor to C++ rather than a &quot;moves fast and breaks things&quot; newcomer, and several argued that newer alternatives like Zig and Odin still have more rough edges. Others highlighted the strategic logic of memory safety for reducing Microsoft&\#x27;s CVE load and linked related efforts such as the 1B-line conversion goal and DARPA&\#x27;s C-to-Rust translation program. The main caveats raised were practical gaps in native UI support across Windows, macOS, Android and iOS, plus lingering limitations of WASM.

**Tags**: `#rust`, `#microsoft`, `#programming-languages`, `#memory-safety`, `#software-engineering`

---

<a id="item-5"></a>
## [trynix.dev boots any Nix package from 13 years in your browser](https://simonwillison.net/2026/Sep/10/trynix/) ⭐️ 8.0/10

Farid Zakaria launched trynix.dev, a qemu-wasm powered x86\_64 Linux virtual machine that runs entirely in the browser via WebAssembly and can boot any Nix package built over the past 13 years. Packages are URL-addressable: visiting a link such as https://trynix.dev/?pkg=python3%403.6.2 and clicking &quot;Load&quot; drops you into an interactive shell running Python 3.6.2 from 2017. He also released trynix-preview, a GitHub Action that comments a link on a pull request so reviewers can boot that PR&\#x27;s build directly in the browser with no servers involved. It collapses the gap between a package&\#x27;s definition and actually running it, making decades-old or rarely-built Nix derivations instantly explorable from a URL instead of a local install. The trynix-preview action points at a broader shift toward browser-based, zero-infrastructure verification of code and reproducible builds, which could reshape how pull requests are reviewed and how historical software environments are reproduced for debugging, teaching, or supply-chain auditing. The whole environment is a real x86\_64 Linux VM emulated by QEMU compiled to WebAssembly \(ktock&\#x27;s qemu-wasm project\), so performance depends on the browser and the wasm JIT rather than native virtualization; qemu-wasm also supports TCG/JIT execution, networking through an in-browser proxy, and disk mounting. The 13-year range reflects how far back Nix binary caches and channel history still resolve, and booting a package means fetching a prebuilt closure from the Nix cache rather than rebuilding it locally.

rss · Simon Willison · Sep 10, 23:44

**Background**: Nix is a purely functional package manager, created by Eelco Dolstra in 2003, that installs every package into its own unique, content-addressed directory so builds are isolated and reproducible. This design makes each package version a self-contained, immutable artifact with a stable hash, which is exactly what allows a tool like trynix.dev to promise &quot;any package from the past 13 years&quot; and address it by URL. QEMU is a general-purpose machine emulator, and qemu-wasm is an experimental port that compiles it to WebAssembly so unmodified guest systems such as Linux can run inside a browser tab. Reproducible builds, the broader discipline Nix popularized, guarantee that compiling the same source yields bit-identical binaries, giving an independently verifiable chain of trust from source code to shipped binary.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Nix_%28package_manager%29">Nix (package manager) - Wikipedia</a></li>
<li><a href="https://github.com/ktock/qemu-wasm">GitHub - ktock/qemu-wasm: QEMU on browser · GitHub</a></li>
<li><a href="https://en.wikipedia.org/wiki/Reproducible_builds">Reproducible builds</a></li>

</ul>
</details>

**Tags**: `#nix`, `#webassembly`, `#qemu`, `#reproducible-builds`, `#browser-tools`

---