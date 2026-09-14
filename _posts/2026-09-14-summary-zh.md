---
layout: default
title: "Horizon Summary: 2026-09-14 (ZH)"
date: 2026-09-14
lang: zh
---

> 从 46 条内容中筛选出 1 条重要资讯。

---

1. [Homebrew 7.0.0 发布：官方 macOS 原生图形界面与更强安全沙箱](#item-1) ⭐️ 9.0/10

---

<a id="item-1"></a>
## [Homebrew 7.0.0 发布：官方 macOS 原生图形界面与更强安全沙箱](https://brew.sh/2026/09/13/homebrew-7.0.0/) ⭐️ 9.0/10

Homebrew 发布了 7.0.0 版本，新增官方 macOS 原生图形界面，提升了安装与升级速度，并引入更严格的沙箱保护、内置漏洞检查以及安全公告数据库。该版本同时停止支持 macOS 10.15 及更早版本，将 Intel Mac 降为 Tier 3，并把 Linux 端的沙箱从 Bubblewrap 更换为 Landlock。 Homebrew 是 macOS 开发者事实上的标准包管理器，此次大版本加入官方图形界面和内置漏洞扫描，会直接改变数百万用户的日常工作流。平台支持策略的调整也释放出明确信号：Apple Silicon 已成为首要目标，而 Intel Mac 与老旧系统正在被逐步淘汰。 Intel Mac 被降为 Tier 3 意味着 Homebrew 将不再为 x86\_64 macOS 提供新的预编译包（bottle），不过官方表示在 2027 年 9 月之前仍可在 Intel 上运行，只是不再提供项目支持。Linux 沙箱的迁移则是用内核态的 Landlock 安全模块取代 Bubblewrap 的用户命名空间方案，让非特权进程也能自行限制自身权限。

telegram · zaihuapd · 9月13日 11:23

**背景**: Homebrew 是一个开源包管理器，用于在 macOS 和 Linux 上安装命令行工具与库，软件以 formula 形式从源码构建，或以称为 bottle 的预编译二进制分发。Homebrew 的支持层级体系规定了哪些平台能获得官方构建、CI 测试和维护者支持，Tier 1 为完全支持，Tier 3 则不受支持。沙箱之所以重要，是因为包管理器会执行第三方的构建与安装脚本：Bubblewrap 借助 Linux 用户命名空间构建沙箱，而 Landlock 是自 Linux 5.13 起可用的可堆叠 Linux 安全模块，允许任意进程安全地限制自身及其子进程。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://brew.sh/2026/09/13/homebrew-7.0.0/">Homebrew: 7.0.0</a></li>
<li><a href="https://docs.brew.sh/Support-Tiers">Homebrew Documentation: Support Tiers</a></li>
<li><a href="https://docs.kernel.org/security/landlock.html">Landlock LSM: kernel documentation — The Linux Kernel documentation</a></li>

</ul>
</details>

**标签**: `#Homebrew`, `#package manager`, `#macOS`, `#security`, `#release`

---