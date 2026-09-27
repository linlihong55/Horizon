---
layout: default
title: "Horizon Summary: 2026-09-27 (EN)"
date: 2026-09-27
lang: en
---

> From 27 items, 2 important content pieces were selected

---

1. [Conversations XMPP Client Leaves Google Play, Becomes Free](#item-1) ⭐️ 8.0/10
2. [SemiAnalysis Tears Down Intel Panther Lake and the 18A Node](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Conversations XMPP Client Leaves Google Play, Becomes Free](https://gultsch.de/posts/breaking-up-with-google-play/) ⭐️ 8.0/10

Daniel Gultsch, the developer of the open-source Android XMPP client Conversations, announced that the app is now free of charge and will no longer be distributed through Google Play, citing poor platform support and unfair treatment of developers. Users are instead directed to obtain the app through other channels such as the project&\#x27;s own website or alternative Android app stores. A well-known open-source developer publicly walking away from the world&\#x27;s largest Android app store is a concrete data point in the ongoing debate over app store monopolies, developer fees and platform governance. It signals that even established, widely used apps can find Google Play&\#x27;s support and review processes too costly and unpredictable to justify staying, which may push more projects toward direct distribution or alternative stores. The post is framed as a first-hand account rather than a technical release, so the practical change for users is simply that Conversations must now be downloaded outside Google Play while the app itself remains free. Commenters noted that the revenue cut Google takes is not the core grievance — the lack of responsive developer support and unpredictable review or account verification steps are what pushed the decision.

hackernews · ezst · Sep 26, 10:55 · [Discussion](https://news.ycombinator.com/item?id=49855315)

**Background**: Conversations is a free and open-source instant messaging client for Android built on XMPP \(Extensible Messaging and Presence Protocol, originally called Jabber\), an open standard for instant messaging, presence and contact lists that uses XML for near-real-time data exchange. Unlike most commercial messaging services, XMPP is federated much like email: anyone can run a server, there is no central master server, and users on different servers can interoperate. Conversations, developed by Daniel Gultsch, is one of the best-known mobile XMPP clients, and Android has historically allowed users to install apps from outside Google Play.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Conversations_%28software%29">Conversations (software) - Wikipedia</a></li>
<li><a href="https://conversations.im/">Conversations - Jabber/XMPP client for Android</a></li>
<li><a href="https://en.wikipedia.org/wiki/XMPP">XMPP - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters broadly agreed with the developer&\#x27;s critique, arguing that the problem is not Google&\#x27;s revenue cut but the terrible and unaccountable support that a monopoly can afford to provide. Several shared their own frustrations: one described a year-long failure to list a product because Google&\#x27;s phone-number verification assumed individual developers, and another noted that Play has shifted from a home for hobbyist projects to a business platform requiring a business address and documents, while increasingly discouraging users from installing apps outside the store.

**Tags**: `#Google Play`, `#Android`, `#Open Source`, `#App Distribution`, `#Developer Experience`

---

<a id="item-2"></a>
## [SemiAnalysis Tears Down Intel Panther Lake and the 18A Node](https://newsletter.semianalysis.com/p/intel-panther-lake-teardown) ⭐️ 8.0/10

SemiAnalysis published a free physical teardown of Intel&\#x27;s Panther Lake client SoC, using its STEEL \(Teardown Engineering &amp; Evaluation Lab\) facility to examine the silicon built on Intel&\#x27;s 18A process node. The analysis looks directly inside the chip, covering structures such as backside power delivery \(BSPD\) and gate-all-around \(GAAFET\) transistors rather than relying on vendor disclosures. Intel 18A is the company&\#x27;s most advanced node and the centerpiece of its foundry strategy, so independent physical verification of its features matters for the whole chip industry. Panther Lake is the first product to put 18A into high-volume client silicon, making this teardown an early real-world check on whether Intel&\#x27;s process claims hold up. The teardown is published as a free SemiAnalysis STEEL analysis, with the lab specifically built to break down advanced datacenter, AI, and client hardware at the physical level. It focuses on 18A-specific innovations such as backside power delivery and gate-all-around transistors, which are the differentiating features Intel is betting its manufacturing roadmap on.

rss · Semianalysis · Sep 26, 13:36

**Background**: Intel 18A is the name of Intel&\#x27;s most advanced chip manufacturing process; by its naming convention, 18A refers to a 1.8-nanometer-class node, notably smaller than the previous Intel 3 generation. Two headline technologies define it: RibbonFET, Intel&\#x27;s implementation of gate-all-around transistors, and PowerVia, its backside power delivery scheme. Panther Lake is the client processor family \(Intel Core Ultra Series 3\) that serves as the first product built on 18A, and teardown labs like SemiAnalysis STEEL physically de-layer chips to inspect transistor and interconnect structures that vendors otherwise only describe in slides.

<details><summary>References</summary>
<ul>
<li><a href="https://newsletter.semianalysis.com/p/intel-panther-lake-teardown">Intel Panther Lake Teardown, 18A, BSPD, GAAFET, SemiAnalysis STEEL</a></li>
<li><a href="https://www.intel.com/content/www/us/en/foundry/process/18a.html">Intel 18A | See Our Biggest Process Innovation</a></li>

</ul>
</details>

**Tags**: `#semiconductors`, `#Intel 18A`, `#Panther Lake`, `#chip fabrication`, `#hardware analysis`

---