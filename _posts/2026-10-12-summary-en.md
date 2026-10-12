---
layout: default
title: "Horizon Summary: 2026-10-12 (EN)"
date: 2026-10-12
lang: en
---

> From 33 items, 2 important content pieces were selected

---

1. [Terence Tao&\#x27;s &\#x27;Math 2.0&\#x27; Slides on AI Reshaping Mathematics](#item-1) ⭐️ 8.0/10
2. [Passkeys Are a Trap: Attestation Lock-In and Privacy Risks](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Terence Tao&\#x27;s &\#x27;Math 2.0&\#x27; Slides on AI Reshaping Mathematics](https://teorth.github.io/tao-web/slides/math-2-0-caltech-2026.pdf) ⭐️ 8.0/10

Terence Tao released the slide deck for a Caltech talk titled &\#x27;Math 2.0&\#x27;, in which he lays out a historical &\#x27;Math 1.0&\#x27; state of mathematics, the current state induced by excessive emphasis on AI automatically solving open problems, and his vision of a future &\#x27;Math 2.0&\#x27; where AI tools sustain both the internal mathematical community and the role of mathematical understanding. The accompanying blog post and slides frame this as a response to the wave of AI results in late 2025 and 2026, and the deck quickly became a major discussion topic with roughly 323 points and 372 comments on Hacker News. As one of the most influential working mathematicians, Tao&\#x27;s framing shapes how the field, funders and tool-builders think about what AI should be for in mathematics, shifting the goal from an &\#x27;answer machine&\#x27; that closes open problems toward AI as infrastructure that organizes, verifies and preserves mathematical knowledge. The debate it triggered also highlights tensions that will affect hiring, grant writing and research culture across mathematics and adjacent AI-for-science fields. The slides are a conceptual talk rather than a new theorem or model release, and they explicitly push back on the current emphasis on automated solving of open problems, describing open problems as &\#x27;lighthouses not destinations&\#x27;. A frequently cited portion uses a cancer-medicine analogy to ask whether one would trust a cure whose mechanism no human understands, a point that drew substantial criticism from commenters working in drug discovery.

hackernews · Anon84 · Oct 11, 13:16 · [Discussion](https://news.ycombinator.com/item?id=50043026)

**Background**: Research on AI for mathematics has accelerated through proof assistants such as Lean 4, which let mathematicians write proofs in a formal language that software can mechanically verify, alongside automated theorem provers and neural models that solve competition-style problems. Terence Tao is a Fields Medalist at UCLA whose widely read blog posts have made him a leading commentator on how AI and formalization are changing mathematical practice. His &\#x27;Math 2.0&\#x27; talk sits at the intersection of these two threads, asking how the community should adapt when machines can produce correct answers faster than humans can understand them.

<details><summary>References</summary>
<ul>
<li><a href="https://terrytao.wordpress.com/2026/10/10/math-2-0/">Math 2.0 | What&#x27;s new</a></li>
<li><a href="https://en.wikipedia.org/wiki/Proof_assistant">Proof assistant - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Automated_theorem_proving">Automated theorem proving - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters broadly welcomed the framing but pushed back on specific points, with drug-discovery researcher dekhn and others arguing that many medicines work without fully understood mechanisms, so Tao was &\#x27;out of his lane&\#x27; with the cancer analogy. samuelknight summarized reactions to an October 8 wave of AI solutions, describing researchers grieving problems they had worked on for years and rewriting grant proposals, while thomasahle translated Tao&\#x27;s argument into software terms, saying current math AI is not a &\#x27;good citizen&\#x27; because it does not try to make the most elegant additions to the theory &\#x27;codebase&\#x27;.

**Tags**: `#Terence Tao`, `#Math 2.0`, `#AI for mathematics`, `#formalization`, `#Hacker News discussion`

---

<a id="item-2"></a>
## [Passkeys Are a Trap: Attestation Lock-In and Privacy Risks](https://nonfunctional.substack.com/p/passkeys-are-a-trap-do-not-use-them) ⭐️ 8.0/10

A critical Substack article titled &quot;Passkeys are a trap&quot; argues that passkeys, particularly when relying parties require remote attestation, introduce vendor lock-in, portability limits and privacy risks for users. The piece sparked a lengthy Hacker News discussion in which commenters debated whether attestation is actually demanded at registration time, how much control users retain over their credentials, and whether the article understates passkeys&\#x27; security benefits. Passkeys are being pushed by Apple, Google, Microsoft and Yahoo as the eventual replacement for passwords, so questions about attestation-based lock-in and credential portability affect hundreds of millions of everyday logins. If platforms can demand attested, device-bound credentials, users may lose the ability to back up, export or migrate their identity material between vendors. Attestation in WebAuthn is an optional field in the registration response that proves the authenticator&\#x27;s identity — such as its AAGUID, attestation format \(packed, tpm, none\) and certificate chain — and browsers display a permission prompt when a site requests it. Commenters noted that attestation can only be enforced at credential registration, not retroactively at login, so the practical scope of the concern depends on whether large services actually reject registrations when users decline the prompt.

hackernews · laurex · Oct 11, 21:59 · [Discussion](https://news.ycombinator.com/item?id=50048312)

**Background**: Passkeys are built on the FIDO2/WebAuthn standards and use origin-bound public-key cryptography: the private key stays on the user&\#x27;s device or syncs through a platform keychain, while the public key is registered with the website, making phishing and credential replay much harder. Remote attestation is a separate, optional mechanism that lets a device cryptographically prove what kind of authenticator it is, which enterprises use to restrict logins to approved hardware keys but which can also be used to fingerprint users or force them onto a specific vendor&\#x27;s ecosystem.

<details><summary>References</summary>
<ul>
<li><a href="https://developers.yubico.com/Passkeys/Passkey_relying_party_implementation_guidance/Attestation/">Attestation</a></li>
<li><a href="https://developers.yubico.com/WebAuthn/Concepts/Enterprise_Attestation/">Enterprise Attestation</a></li>
<li><a href="https://support.microsoft.com/en-us/accounts-billing/security/passkeys-frequently-asked-questions-faq">Passkeys frequently asked questions (FAQ) | Microsoft Support</a></li>

</ul>
</details>

**Discussion**: The Hacker News thread was largely sympathetic but pushed back on specifics: one commenter stressed that attestation can only be required at registration and that browsers show a permission prompt, doubting that Netflix or Twitter currently enforce it, while another said they avoid passkeys entirely because they want portability, offline backup and control over credential strength, trusting a long password manager entry more than a phone thumbprint. Others praised the writing while noting the article concedes legitimate uses of attestation \(rejecting a scammer&\#x27;s fake passkey app\), and one pointed out that its final footnote admits passkeys are domain-bound and thus resistant to man-in-the-middle attacks — arguably their most important security feature.

**Tags**: `#passkeys`, `#authentication`, `#security`, `#privacy`, `#web-standards`

---