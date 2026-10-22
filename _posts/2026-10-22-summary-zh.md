---
layout: default
title: "Horizon Summary: 2026-10-22 (ZH)"
date: 2026-10-22
lang: zh
---

> 从 40 条内容中筛选出 8 条重要资讯。

---

1. [PyPI 上的 LiteLLM 1.107.0 被植入凭据窃取程序与后门](#item-1) ⭐️ 9.0/10
2. [DuckDB 2.0.0 LTS“Cinnamon Teal”发布，新增客户端-服务器模式与触发器](#item-2) ⭐️ 9.0/10
3. [PHP 8.2.35 紧急发布，修复 PHP2Shell 远程代码执行漏洞](#item-3) ⭐️ 9.0/10
4. [Railway 披露安全事件：用户密钥与环境变量疑似泄露](#item-4) ⭐️ 8.0/10
5. [新墨西哥州在剑桥分析案中赢得对 Meta 的 250 亿美元罚单](#item-5) ⭐️ 8.0/10
6. [eMudhra 中间证书私钥熵值过低，毫秒级被破解，各大平台紧急停止信任](#item-6) ⭐️ 8.0/10
7. [SemiAnalysis 实测华为昇腾 950PR 与 DeepSeek DSv4.1 Flash](#item-7) ⭐️ 8.0/10
8. [SpaceX 下月将首次尝试完整回收星舰飞船与超级重型助推器](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [PyPI 上的 LiteLLM 1.107.0 被植入凭据窃取程序与后门](https://safedep.io/litellm-pypi-compromise-credential-stealer-backdoor/) ⭐️ 9.0/10

发布在 PyPI 上的 LiteLLM 1.107.0 版本被篡改，其中被植入了凭据窃取程序和后门，任何安装该版本的用户都会直接从官方包索引下载到恶意代码。SafeDep 的安全研究人员记录了这一事件，并呼吁各团队审计依赖、排查环境里是否装有 1.107.0。 LiteLLM 是被广泛使用的 LLM 网关和 Python SDK，拥有数以万计的下游依赖项目，因此一个被投毒的版本就可能悄无声息地让 OpenAI、Anthropic、云厂商和数据库的凭据在整个生态中泄露。这还动摇了“从官方仓库安装固定版本就是安全的”这一核心假设，而这是每个软件团队都要面对的问题。 受影响的是具体的 1.107.0 版本，因此当务之急是锁定到已知安全的版本、轮换在安装过该版本的机器上可访问的所有密钥，并检查 lockfile 与 CI 缓存，而不是依赖版本范围。由于 LiteLLM 常常作为其他工具的传递依赖被间接引入，团队可能从未直接安装过它却仍然暴露在风险之中。

hackernews · abhisek · 10月21日 14:00 · [社区讨论](https://news.ycombinator.com/item?id=50181114)

**背景**: LiteLLM 由 BerriAI 开发，是一个开源 AI 网关与 Python SDK，为应用提供统一的、兼容 OpenAI 的接口，用于调用 OpenAI、Anthropic、Gemini、Bedrock、Azure 等 100 多家 LLM 提供商，并提供成本追踪、预算和限流功能。由于它持有各家提供商的 API 密钥以便应用转发请求，因此是高价值攻击目标：被篡改的版本恰好把那些它本该安全保管的密钥交给了攻击者。这并非首次事件——2025 年早些时候就曾报道过一次类似的 LiteLLM PyPI 供应链攻击。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/LiteLLM">LiteLLM</a></li>
<li><a href="https://github.com/BerriAI/litellm">GitHub - BerriAI/litellm: The fastest, litest AI Gateway ...</a></li>
<li><a href="https://grokipedia.com/page/LiteLLM">LiteLLM</a></li>

</ul>
</details>

**社区讨论**: 评论者强调，sandbox-exec、LuLu 这类终端沙箱和防火墙工具无法真正阻止此类攻击，而权限弹窗疲劳以及习惯性地执行 \`brew\`/\`npm\` 升级会让开发者对安装内容逐渐麻木。多人指出这是大约一年内 LiteLLM 第二次重大被利用事件，有人建议对新版本设置 8 天的“时间门槛”再安装，也有人质疑一个三年内提交了 5.5 万次的项目怎么会发生这种事；此外还有人建议用 canary token 作为检测手段。

**标签**: `#supply-chain-security`, `#pypi`, `#litellm`, `#malware`, `#dependency-management`

---

<a id="item-2"></a>
## [DuckDB 2.0.0 LTS“Cinnamon Teal”发布，新增客户端-服务器模式与触发器](https://duckdb.org/2026/10/21/announcing-duckdb-200) ⭐️ 9.0/10

DuckDB 于 2026 年 10 月 21 日发布 2.0.0 LTS 版本，代号“Cinnamon Teal”，承诺长期支持至少延续到 2027 年 10 月。该版本通过 quack 扩展提供稳定的客户端-服务器模式（用 CALL quack\_serve\(token = &\#x27;my\_token&\#x27;\) 启动服务端），并引入触发器、一等公民的半结构化 VARIANT 数据类型、异步 I/O、全新的 SQL 解析器，以及大幅的查询与存储性能改进。 DuckDB 一直以“没有服务器”的嵌入式分析引擎著称，而新增客户端-服务器模式使其成为可用于集中式分析服务的可信方案，有望替代小型组织中运行在多台服务器上的数据技术栈。再加上触发器和显著改善的多核扩展能力，这一版本让 DuckDB 更接近开箱即用的“一体化数据仓库”，影响所有在大型云主机上运行分析负载的用户。 新的服务器模式通过 quack 扩展提供，但官方指出目前对 DuckDB 原生 Quack 协议的客户端支持仍然非常有限，因此大多数工具会改用 Postgres 线协议或 Arrow Flight/ADBC 连接。社区测试显示，CPU 利用率现在可扩展到约 128–192 个 vCPU，而 2.0 之前的版本在约 64 个 vCPU 就达到上限，不过超过约 192 个 vCPU 后收益仍会趋平；上一个 LTS 版本 1.4 将支持到 2026 年 11 月下旬，以便用户平滑迁移。

hackernews · nnx · 10月21日 14:01 · [社区讨论](https://news.ycombinator.com/item?id=50181136)

**背景**: DuckDB 是一个开源的分析型（OLAP）数据库，像 SQLite 一样以进程内方式运行，但它针对 Parquet、CSV 等文件的快速列式查询处理进行了优化，而非事务型负载。这种嵌入式设计使其在本地分析和数据管道中极受欢迎，但过去没有服务器模式，多个用户或应用无法共享同一个中心实例。LTS（长期支持）版本是 DuckDB 的一项惯例，为企业提供带有安全更新和缺陷修复的稳定分支，而不必追逐快速迭代的功能版本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://duckdb.org/2026/10/21/announcing-duckdb-200">Announcing DuckDB 2.0.0 LTS “Cinnamon Teal” – DuckDB</a></li>
<li><a href="https://tldr.tech/data/2026-08-20">Inside DuckDB 2 . 0 , ACID for AI Agents , Variant Lands in Iceberg</a></li>
<li><a href="https://motherduck.com/duckdb-book-summary-chapter1/">What Is DuckDB ? Introduction, Use Cases &amp; Architecture | MotherDuck</a></li>

</ul>
</details>

**社区讨论**: 社区反应非常积极，评论者称客户端-服务器能力是“改变游戏规则”的功能，可能取代多服务器的数据栈，并认为触发器让 DuckDB 真正接近“一体化数据仓库”。一位用户表示已将 2.0 alpha 投入生产，作为小型组织的集中式分析服务器，并因为原生 Quack 客户端支持有限而自行开发了支持 Postgres 线协议和 Arrow Flight 连接的扩展。另有人报告在 EC2 高核数机器上获得了显著的加速——在 128–192 个 vCPU 下接近 100% 利用率，而此前上限约为 64 个 vCPU——这也让其 Splink 记录链接工具得以进一步扩展。

**标签**: `#duckdb`, `#databases`, `#analytics`, `#release`, `#performance`

---

<a id="item-3"></a>
## [PHP 8.2.35 紧急发布，修复 PHP2Shell 远程代码执行漏洞](https://github.com/php/php-src/releases/tag/php-8.2.35) ⭐️ 9.0/10

PHP 8.2.35 已作为 PHP2Shell 的紧急安全更新发布；PHP2Shell 是一个被追踪为 CVE-2026-109618 和 CVE-2026-109619 的严重远程代码执行问题，由 Wiz、Calif 和 OpenAI 协调披露。它是在该漏洞公开宣布后发布的多个已修复 PHP 分支之一。 PHP 驱动着互联网上很大一部分网站，因此一个影响 5.4 至 8.5 版本的未认证远程代码执行漏洞会使大量面向互联网的服务器立即面临风险，补丁更新十分紧迫。此次披露还因漏洞据称是在 AI 辅助下发现而格外引人注目，这可能预示着高危漏洞的发现方式正在发生变化。 PHP2Shell 由两个高危漏洞组成，分别追踪为 CVE-2026-109618 和 CVE-2026-109619，影响 PHP 5.4 至 8.5；已修复版本为 PHP 8.5.12、8.4.27、8.3.36 和 8.2.35。CVE-2026-109619 被描述为允许攻击者无需登录即可在 Web 服务器上执行自己的代码，社区报告还将其与 session.upload\_progress 堆释放后使用（use-after-free）问题联系起来。

hackernews · tuyuri · 10月21日 13:45 · [社区讨论](https://news.ycombinator.com/item?id=50180873)

**背景**: PHP 是一种广泛使用的服务器端脚本语言，支撑着许多内容管理系统和 Web 应用，包括 WordPress。远程代码执行漏洞允许攻击者在服务器上运行任意命令，通常会导致服务器被完全攻陷。PHP2Shell 于 2026 年 10 月 20 日公开宣布，紧急补丁和技术细节于 10 月 21 日发布；此次协调披露涉及 PHP 项目以及 Wiz、Calif 和 OpenAI。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/PHP2Shell">PHP2Shell - Wikipedia</a></li>
<li><a href="https://sansec.io/research/php2shell">PHP2Shell: Critical PHP RCE (CVE-2026-109618, CVE-2026-109619)</a></li>
<li><a href="https://watchtowr.com/intelligence/php-remote-code-execution-php2shell/">PHP2Shell: PHP Remote Code Execution Exploited</a></li>

</ul>
</details>

**社区讨论**: 评论者贴出了来自 php2shell.com、Wiz、Calif 和 OpenAI 的协调披露文章，还有人指出可能存在第二个漏洞。整体情绪既严肃又对发布过程感到沮丧：一位拥有 20 年 PHP 托管经验的用户质疑项目的处理方式，另一位则指出公告发布数小时后发布产物仍未真正可用，这促使他们重新考虑自己的部署流程。

**标签**: `#PHP`, `#security`, `#RCE`, `#vulnerability-disclosure`, `#AI-security`

---

<a id="item-4"></a>
## [Railway 披露安全事件：用户密钥与环境变量疑似泄露](https://blog.railway.com/p/security-disclosure-wednesday-october-21st) ⭐️ 8.0/10

广受欢迎的 PaaS 部署平台 Railway 于 10 月 21 日（周三）发布安全披露公告，承认发生了一起安全事件，可能导致用户的环境变量与密钥被解密泄露。官方敦促用户立即轮换凭据，社区成员也报告称已有第三方在真实环境中使用了泄露的密钥。 PaaS 平台上的环境变量通常存放数据库密码、API 密钥和云凭据，一旦明文值泄露，就可能同时波及大量下游服务。Railway 承载了成千上万独立开发者和小团队的应用，因此影响范围远超平台本身，也加深了人们对托管云服务商“风险集中”问题的担忧。 在讨论进行时，该披露并未给出详细的根本原因分析或明确的时间线，这引来用户批评，称公司直到有客户公开发声才作出回应。此次事件还与同日曝出的 PHP 远程代码执行漏洞（即 “PHP2Shell” 漏洞）以及 eMudhra 证书泄露事件撞在一起，让需要同时负责多套技术栈的团队疲于应对。

hackernews · passenger · 10月21日 21:58 · [社区讨论](https://news.ycombinator.com/item?id=50188228)

**背景**: Railway 是一个云应用平台（PaaS），开发者推送代码后由平台负责构建、部署、数据库与扩缩容，配置通常通过环境变量下发。环境变量是把 API 密钥、数据库密码等敏感信息在运行时注入应用的标准方式，一般以加密形式静态存储，只在运行中的容器内解密。一旦解密后的值被泄露，就等于把可用凭据直接交给了攻击者，因此应急响应人员会把凭据轮换——签发新密钥并吊销旧密钥——视为首要且最紧急的补救措施。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://railway.com/">Railway | The all-in-one intelligent cloud provider</a></li>
<li><a href="https://docs.railway.com/platform">Platform | Railway Docs</a></li>
<li><a href="https://blog.gitguardian.com/secure-your-secrets-with-env/">Best Practices for Environment Variables Secrets Management</a></li>

</ul>
</details>

**社区讨论**: 评论者称这是安全领域“疯狂的一天”，把 Railway 事件与 PHP 远程代码执行漏洞、eMudhra 证书泄露并列，视作同时爆发的多重危机。多位读者表示在 Railway 的 Discord 中看到有人确认平台上存储的密钥已被第三方使用，还有人引用 Postiz 创始人的公开贴文，称其密钥已被盗用，而 Railway 直到他发声后才作出回应。整体情绪既有对攻击者能够读取解密环境变量的警觉，也有对这种“紧急打补丁、紧急轮换凭据”的日子可能成为常态的无奈。

**标签**: `#security`, `#incident-disclosure`, `#cloud-platform`, `#secrets-management`, `#cybersecurity`

---

<a id="item-5"></a>
## [新墨西哥州在剑桥分析案中赢得对 Meta 的 250 亿美元罚单](https://www.cnbc.com/2026/10/21/meta-new-mexico-cambridge-analytica-penalty.html) ⭐️ 8.0/10

2026 年 10 月 21 日，新墨西哥州司法部宣布，在围绕剑桥分析（Cambridge Analytica）数据抓取丑闻的长期诉讼中，该州赢得了对 Meta 高达 250 亿美元的里程碑式民事罚款。新墨西哥州没有加入多州集体诉讼，而是单独提起诉讼，主张 Facebook 在用户个人数据如何被收集和共享的问题上欺骗了用户。 这一判决是迄今为止美国单个州对 Meta 开出的最大隐私罚单，远超 2022 年那笔 7.25 亿美元的多州集体诉讼和解金，表明各州总检察长若依据本州消费者保护法单独起诉，有可能拿到高得多的金额。如果判决在上诉后得以维持，将开创先例，鼓励其他州放弃联合和解、改为单独执法。 该罚款依据《新墨西哥州不公平行为法》作出，该法允许总检察长就每一项故意违法行为索赔最高 5000 美元，因此罚款总额随受影响的该州用户数量估算而放大。Meta 预计将提起上诉，而此类巨额法定罚款在复审中往往会被大幅削减，最终金额可能只是 250 亿美元的一小部分。

hackernews · cbg0 · 10月21日 17:45 · [社区讨论](https://news.ycombinator.com/item?id=50184820)

**背景**: 剑桥分析丑闻于 2018 年爆发，当时曝出研究员亚历山大·科根开发的一款性格测试应用抓取了多达 8700 万 Facebook 用户的数据，并将其提供给了为特朗普 2016 年竞选服务的政治咨询公司剑桥分析。Facebook 此后向美国联邦贸易委员会（FTC）支付了 50 亿美元罚款，并于 2022 年与用户达成 7.25 亿美元的集体诉讼和解。2026 年 8 月，Meta 还与 47 个州、华盛顿特区及美国属地就“平台危害儿童”的指控达成了 171 亿美元和解，该协议中包含一项条款，以约 4.59 亿美元了结各州与剑桥分析相关的索赔。而早在 2018 年就依据本州消费者保护法自行起诉的新墨西哥州，并不受这些协议约束。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://edition.cnn.com/2026/10/21/tech/meta-25-billion-new-mexico-judgment">Meta ordered to pay $25 billion in New Mexico case over Cambridge...</a></li>
<li><a href="https://www.nytimes.com/2026/10/21/technology/meta-penalty-new-mexico.html">Meta Ordered to Pay $25 Billion for Deceiving Users on Privacy</a></li>
<li><a href="https://law.justia.com/codes/new-mexico/chapter-57/article-12/section-57-12-11/">New Mexico Statutes Section 57-12-11 (2025) - Civil penalty ...</a></li>

</ul>
</details>

**社区讨论**: 评论者对这笔罚款是否真能形成威慑表示怀疑，认为真正的问责应当是对高管追究刑事责任或个人责任，而不是对企业罚款——后者不过是经营成本。也有人提供了有价值的背景：新墨西哥州总检察长办公室公布的扎克伯格与桑德伯格证词视频链接；有人指出参与集体诉讼的所有州合计只分到 7.25 亿美元，而新墨西哥州一家就拿到 250 亿美元；还有人测算，47 州和解仅以 4.59 亿美元就了结了剑桥分析相关索赔。主流预期是 Meta 会上诉，罚款最终可能被削减到名义金额的约 10%。

**标签**: `#privacy`, `#meta`, `#regulation`, `#tech-policy`, `#cambridge-analytica`

---

<a id="item-6"></a>
## [eMudhra 中间证书私钥熵值过低，毫秒级被破解，各大平台紧急停止信任](https://scotthelme.co.uk/eight-bits-of-trust-emudhras-ca-keys-cracked-in-milliseconds/) ⭐️ 8.0/10

印度证书机构 eMudhra 的 8 张中间证书被查出其 RSA 私钥只有约 8 比特的真实熵——也就是大约 256 种可能取值，因此可在毫秒级被穷举还原。该问题由 Google 开源的 paranoid\_crypto 工具发现，随即引发紧急封禁：Mozilla 在 10 月 17 日收到报告后 3 小时内向所有 Firefox 用户推送撤销，Google 同日屏蔽受影响的公钥，Apple 与 Microsoft 也相继跟进。 一家被公开信任的 CA 签发出建立在可轻易分解的密钥之上的证书，直接击穿了整个 TLS 信任模型的核心假设——即只有该 CA 才能为某个域名签发有效证书。任何还原出这些私钥的人都能冒充 eMudhra，为任意网站签发看似合法的 HTTPS 证书；而大量嵌入式与 IoT 设备永远收不到信任库更新，因此浏览器修复之后风险仍可能长期存在。 在受影响的 8 张中间证书中，6 张可用于签发 TLS 服务器证书，2 张可用于代码签名；而实际修复方式因平台差异极大：浏览器会自动接收推送的撤销信息，但 Go 编译的二进制程序以及依赖 Python certifi 证书包的程序并不检查撤销数据，在其根证书包或代码更新之前会继续信任这条证书链。Google 表示计划于 10 月 27 日移除相关根证书，这给运维方设定了重建容器镜像、刷新 CA 软件包的截止期限。

hackernews · hkc · 10月21日 09:08 · [社区讨论](https://news.ycombinator.com/item?id=50177916)

**背景**: RSA 的安全性建立在“分解一个大整数很难”这一前提上，这个大整数由两个随机选取的素数相乘得到；如果选取素数时使用的随机性很弱，密钥空间就会坍缩，模数几乎可以瞬间被分解。证书机构位于 TLS 信任体系的顶端：浏览器和操作系统内置一份受信任根证书库，这些 CA 再签发中间证书，中间证书再去签发网站使用的终端实体证书。Google 的 paranoid\_crypto 是一款专门扫描此类缺陷的工具，它通过对大规模公钥集合（例如 CCADB 中由 CA 持有的证书语料）进行分解与相关检验，来发现重复密钥、共享素因子以及熵不足生成的密钥。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/EMudhra">eMudhra - Wikipedia</a></li>
<li><a href="https://thehackernews.com/2026/10/eight-emudhra-ca-keys-compromised.html">Eight eMudhra CA Keys Compromised, Triggering Emergency Fixes...</a></li>
<li><a href="https://blog.cloudflare.com/emudhra-certificate-compromise/">8 eMudhra certificates are compromised. | Cloudflare Blog</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论把这起事件视为对整个体系的控诉而非孤立漏洞，有人调侃说“回头看看，同时信任 100 家证书机构可能确实有点过头了”。最初报告此事的 Wayne 现身说明，paranoid\_crypto 在 CCADB 语料上开箱即命中这些密钥，随后对全部现有 CCADB 证书的复查未再发现新的案例；另一些评论者则把焦点放在无法修补的 IoT 与嵌入式设备上，它们会继续信任已被撤销的证书链。还有一个讨论方向颇具创意：有人提问能否利用这些弱密钥签发证书来给锁定的设备越狱，并指出这种情况似乎已经在发生。

**标签**: `#security`, `#TLS`, `#certificate-authority`, `#cryptography`, `#IoT`

---

<a id="item-7"></a>
## [SemiAnalysis 实测华为昇腾 950PR 与 DeepSeek DSv4.1 Flash](https://newsletter.semianalysis.com/p/huawei-deepseek) ⭐️ 8.0/10

SemiAnalysis 发布深度分析报告，既包含对华为昇腾 950PR 加速卡的原创微基准测试（microbenchmark），也分析了 DeepSeek 新发布的 DSv4.1 Flash 模型及其对昇腾平台的支持。文章将二者描述为华为国产 AI 硬件与 DeepSeek 开放权重模型之间日益紧密的“共生关系”。 在美国出口管制推动中国实验室转向国产芯片的背景下，一份有实测数据支撑的非英伟达 AI 技术栈分析具有重要意义，而华为与 DeepSeek 的组合正是最具代表性的“自给自足”方案。中国以外的采购方与基础设施规划者也急需真实性能数据来判断昇腾是否具备竞争力，而不是只听厂商宣传。 报道中的数据显示，昇腾 950PR 的算力约为英伟达 H20（英伟达可合法对华销售的最强芯片）的 2.87 倍，并配备 112GB 的 HiBL 内存；但华为自身路线图显示，950PR/950DT 的总处理性能反而低于 2025 年的昇腾 910C，首款超越 H200 的芯片要等到 2027 年第四季度的 960。DeepSeek 的 V4.1 Flash 则采用全新的非对称模型结构，具备原生多模态视觉理解能力，通过 DeepSeek API 以 deepseek-flash 模型名提供服务，并下线了此前的 V4-Flash 与 V4-Flash-Vision-Exp。

rss · Semianalysis · 10月21日 17:34

**背景**: 华为昇腾系列是中国最具代表性的国产 AI 加速卡产品线，被视为受出口限制无法进入中国的英伟达 GPU 的替代方案，其中 “PR” 型号属于与 950DT 并列的路线图产品。DeepSeek 是一家总部位于杭州的 AI 公司，由对冲基金幻方量化（High-Flyer）出资支持，以发布开放权重大语言模型著称，其 “Flash” 系列主打低延迟与低成本，而非最大规模。微基准测试（microbenchmark）是对特定硬件操作的底层测量，SemiAnalysis 借此刻画超出峰值 TOPS 数字的真实性能表现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.spheron.network/blog/huawei-ascend-950-vs-nvidia-b300-b200-llm-inference-2026/">Huawei Ascend 950 vs NVIDIA B300 and B200 for... | Spheron Blog</a></li>
<li><a href="https://convly.ai/huawei-ascend-950-pangu-explained-2026/">Huawei Ascend 950 &amp; Pangu: China&#x27;s 2026 AI-Chip Play</a></li>
<li><a href="https://www.deepseek.com/en/news/deepseek-v4-1-flash/">DeepSeek | Introducing DeepSeek-V4.1-Flash: smarter, faster ...</a></li>

</ul>
</details>

**标签**: `#AI hardware`, `#Huawei Ascend`, `#DeepSeek`, `#semiconductors`, `#benchmarking`

---

<a id="item-8"></a>
## [SpaceX 下月将首次尝试完整回收星舰飞船与超级重型助推器](https://www.theverge.com/science/1014913/spacex-will-try-catching-starship-and-its-booster-for-first-time-musk-says) ⭐️ 8.0/10

马斯克在财报电话会上表示，SpaceX 将于下月首次尝试在同一飞行任务中同时回收星舰飞船和超级重型助推器。他坦言此次尝试并不保证成功，但称成功率比上一次飞行更高。 如果两级都能完好回收，这将是人类首次完整回收一枚轨道级运载火箭，是迈向类似飞机那样快速复用的关键一步，有望大幅降低发射成本。成功还将巩固 SpaceX 在商业发射市场的地位，并有利于其承担 NASA 阿尔忒弥斯登月着陆器的承诺。 上一次飞行因一台发动机提前关机，任务被迫缩短至约 3 小时，助推器与飞船均未回收。超级重型助推器不靠着陆腿，而是由发射塔的机械“筷子”臂在半空中夹住；星舰飞船本身则需经受再入大气层并完成受控溅落或回收。

telegram · zaihuapd · 10月21日 06:00

**背景**: SpaceX 自 2010 年代以来一直在研发完全可复用的发射系统，目标是让火箭经过极少翻修即可多次飞行，而不是每次发射后就被丢弃。超级重型助推器由被称为“筷子”的巨大机械臂夹住，这对机械臂是名为 Mechazilla 的发射塔的一部分，该技术在 2024 年 10 月星舰第五次飞行测试中首次公开展示。完全可复用的轨道运载工具与当今的部分复用火箭不同，后者通常只能回收一级。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.inverse.com/heres-how-spacexs-chopsticks-caught-a-rocket">Here&#x27;s How SpaceX&#x27;s &quot;Chopsticks&quot; Caught a Rocket In This ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Reusable_launch_vehicle">Reusable launch vehicle - Wikipedia</a></li>

</ul>
</details>

**标签**: `#SpaceX`, `#Starship`, `#reusable rockets`, `#spaceflight`, `#aerospace`

---