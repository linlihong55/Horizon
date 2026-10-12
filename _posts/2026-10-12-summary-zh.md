---
layout: default
title: "Horizon Summary: 2026-10-12 (ZH)"
date: 2026-10-12
lang: zh
---

> 从 33 条内容中筛选出 2 条重要资讯。

---

1. [陶哲轩《Math 2.0》幻灯片探讨 AI 如何重塑数学研究](#item-1) ⭐️ 8.0/10
2. [通行密钥是陷阱：远程认证带来的锁定与隐私风险](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [陶哲轩《Math 2.0》幻灯片探讨 AI 如何重塑数学研究](https://teorth.github.io/tao-web/slides/math-2-0-caltech-2026.pdf) ⭐️ 8.0/10

陶哲轩发布了他加州理工演讲《Math 2.0》的幻灯片，梳理了数学的“Math 1.0”历史状态、当前因 AI 过度聚焦自动求解未解难题而形成的现状，以及他设想的未来“Math 2.0”——让 AI 工具既维系数学共同体内部生态，又维护数学理解本身的价值。配套博文与幻灯片被视为对 2025 年底至 2026 年 AI 数学成果浪潮的回应，并以约 323 分、372 条评论成为 Hacker News 上的热门讨论话题。 作为最有影响力的在世数学家之一，陶哲轩的论述会影响数学界、资助方和工具开发者对“AI 在数学中该干什么”的判断，把目标从“关掉未解难题的答题机”转向“组织、验证并保存数学知识的基础设施”。由此引发的争论也凸显出将影响数学及 AI for Science 相邻领域的招聘、基金申请与研究文化的深层张力。 这份幻灯片是概念性演讲，而非新定理或新模型发布，其中明确批评当前过度强调用 AI 自动求解未解难题的做法，并把未解问题描述为“灯塔而非终点”。被频繁引用的一段用癌症药物作类比，追问人们是否愿意接受一种没有任何人类理解其机理的疗法，这一点招致了从事药物研发的评论者的强烈批评。

hackernews · Anon84 · 10月11日 13:16 · [社区讨论](https://news.ycombinator.com/item?id=50043026)

**背景**: AI 用于数学的研究近年来快速推进：Lean 4 等证明助手让数学家可以用形式化语言书写证明并由软件机械验证，同时自动定理证明器和神经模型在竞赛类题目上也有不俗表现。陶哲轩是 UCLA 的菲尔兹奖得主，其广受阅读的博文使他成为观察 AI 与形式化如何改变数学实践的核心评论者。他的《Math 2.0》演讲正处于这两条脉络的交汇处，追问当机器给出的正确答案快于人类理解速度时，数学共同体应如何应对。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://terrytao.wordpress.com/2026/10/10/math-2-0/">Math 2.0 | What&#x27;s new</a></li>
<li><a href="https://en.wikipedia.org/wiki/Proof_assistant">Proof assistant - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Automated_theorem_proving">Automated theorem proving - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者总体认可这一框架，但对具体论点提出反驳：从事药物研发的 dekhn 等人指出许多药物在机理尚未被完全理解的情况下同样有效，因此陶哲轩的癌症类比属于“越界发言”。samuelknight 总结了人们对 10 月 8 日一批 AI 解答的反应，形容研究者像失去老朋友一样为钻研多年的问题被解决而哀伤，并被迫重写已提交的基金申请；thomasahle 则用软件术语转述陶哲轩的观点，称当前的数学 AI 还不是“好公民”，因为它并不追求对理论“代码库”做出最优雅的扩展。

**标签**: `#Terence Tao`, `#Math 2.0`, `#AI for mathematics`, `#formalization`, `#Hacker News discussion`

---

<a id="item-2"></a>
## [通行密钥是陷阱：远程认证带来的锁定与隐私风险](https://nonfunctional.substack.com/p/passkeys-are-a-trap-do-not-use-them) ⭐️ 8.0/10

一篇题为《Passkeys are a trap》的 Substack 批评文章指出，通行密钥（passkeys）在依赖方要求远程认证（remote attestation）时，会给用户带来厂商锁定、可移植性受限和隐私风险。该文在 Hacker News 上引发了长篇讨论，评论者就注册环节是否真的会强制要求认证、用户对凭证还剩多少控制权，以及文章是否低估了通行密钥的安全优势展开了争论。 苹果、谷歌、微软和雅虎都在力推通行密钥，将其视为密码的最终替代方案，因此围绕基于认证的锁定和凭证可移植性的问题，会影响数以亿计的日常登录。如果平台能够要求经过认证且绑定设备的凭证，用户就可能失去备份、导出或在不同厂商之间迁移身份凭据的能力。 WebAuthn 中的认证是注册响应里的一个可选字段，用于证明认证器的身份，例如其 AAGUID、认证格式（packed、tpm、none）以及证书链；当网站请求认证时，浏览器会弹出权限提示。评论者指出，认证只能在凭证注册时强制，无法在登录时追溯要求，因此这一担忧的实际影响范围取决于大型服务是否真的会在用户拒绝授权提示时拒绝注册。

hackernews · laurex · 10月11日 21:59 · [社区讨论](https://news.ycombinator.com/item?id=50048312)

**背景**: 通行密钥基于 FIDO2/WebAuthn 标准，采用与来源绑定的公钥加密：私钥保存在用户设备上或通过平台钥匙串同步，公钥则注册到网站，这让钓鱼和凭证重放变得困难得多。远程认证是一项独立的可选机制，让设备能够以密码学方式证明自己属于哪类认证器；企业借此把登录限制在获批的硬件密钥上，但它同样可以被用来对用户进行指纹识别，或迫使用户进入某一特定厂商的生态。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developers.yubico.com/Passkeys/Passkey_relying_party_implementation_guidance/Attestation/">Attestation</a></li>
<li><a href="https://developers.yubico.com/WebAuthn/Concepts/Enterprise_Attestation/">Enterprise Attestation</a></li>
<li><a href="https://support.microsoft.com/en-us/accounts-billing/security/passkeys-frequently-asked-questions-faq">Passkeys frequently asked questions (FAQ) | Microsoft Support</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论总体偏向认同，但对具体论点提出了反驳：一位评论者强调认证只能在注册时要求，且浏览器会弹出权限提示，因此他怀疑 Netflix 或 Twitter 目前并未强制认证；另一位则表示完全不启用通行密钥，因为他需要可移植性、离线备份和对凭证强度的控制，而且比起手机指纹，他更信任密码管理器中的长密码。也有人赞赏文章的行文，同时指出作者承认远程认证有其正当用途（可拒绝诈骗者伪造的通行密钥应用）；还有人提到文末脚注承认通行密钥与域名绑定、因此能抵御中间人攻击——这可以说是它们最重要的安全特性。

**标签**: `#passkeys`, `#authentication`, `#security`, `#privacy`, `#web-standards`

---