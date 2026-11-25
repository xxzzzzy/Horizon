---
layout: default
title: "Horizon Summary: 2026-11-25 (ZH)"
date: 2026-11-25
lang: zh
---

> 从 111 条内容中筛选出 16 条重要资讯。

---

**科技新闻**
1. [预印本声称矩阵乘法指数恰为 9/4](#item-tech-news-1) ⭐️ 9.0/10
2. [GPT-6 展现通用蛋白质设计能力](#item-tech-news-2) ⭐️ 8.0/10
3. [Active intrusion campaign against Check Point security management servers](#item-tech-news-3) ⭐️ 8.0/10
4. [AI 辅助黎曼猜想证明仍待审查](#item-tech-news-4) ⭐️ 8.0/10
5. [Amazon says hackers&\#x27; AI agents found and exploited 0-day with little human input](#item-tech-news-5) ⭐️ 8.0/10
6. [vCenter 9.8 分鉴权绕过漏洞已遭利用](#item-tech-news-6) ⭐️ 8.0/10
7. [过去十二个月的三次 LLM 拐点](#item-tech-news-7) ⭐️ 7.0/10
8. [微软云故障暴露部署与扩容盲区](#item-tech-news-8) ⭐️ 7.0/10
9. [Tidal 将删除 2700 万首全 AI 生成曲目](#item-tech-news-9) ⭐️ 7.0/10
10. [英伟达火速恢复黄仁勋 CEO 职务](#item-tech-news-10) ⭐️ 7.0/10
11. [数十艘油轮及化学品运输船近期遭黑客攻击](#item-tech-news-11) ⭐️ 7.0/10
12. [亚马逊收购 Decart，押注软件缩小芯片差距](#item-tech-news-12) ⭐️ 7.0/10
13. [CrowdStrike 拟以 440 亿美元收购 Zscaler](#item-tech-news-13) ⭐️ 7.0/10
14. [Microduck 的 ToF 仿真到现实避障工作流](#item-tech-news-14) ⭐️ 6.0/10
15. [用 Astra 和 Codex 搜寻遥远行星](#item-tech-news-15) ⭐️ 6.0/10
16. [字节跳动开源异步强化学习后训练框架 Laminar](#item-tech-news-16) ⭐️ 6.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [预印本声称矩阵乘法指数恰为 9/4](https://github.com/openai/math/blob/main/preprints/The-matrix-multiplication-exponent-is-nine-fourths-November-24-2026/paper.pdf) ⭐️ 9.0/10

OpenAI 的一篇预印本声称已证明矩阵乘法指数为 9/4；此前上界 O\(n²·²⁵\) 已知，新结果据称补上了 Ω\(n²·²⁵\) 的下界。若该证明成立，这将显著改善已知最佳界，并解决复杂度理论领域的长期难题。不过，现有材料尚未独立验证该定理及其适用范围。

hackernews · E-Reverance · 11月25日 01:19 · [社区讨论](https://news.ycombinator.com/item?id=50637220)

**标签**: `#matrix multiplication`, `#theoretical computer science`, `#algorithms`, `#complexity theory`, `#OpenAI`

---

<a id="item-tech-news-2"></a>
### [GPT-6 展现通用蛋白质设计能力](https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities) ⭐️ 8.0/10

OpenAI 在预印本《GPT-6 as a Universal Foundation Model for Protein Biology: Beyond Specialized Models》中称，GPT-6 系列模型仅凭推理和通用代码即可设计蛋白质三维结构及氨基酸序列，生成阶段无需调用专用生物模型。内部研究模型在多项蛋白质设计任务上达到或超过专用模型，最新模型在多数计算任务中与其相当或更优，并能按提示控制结合位点、形状和 minibinder 的线圈或股数；但完整蛋白质结构预测仍是明显短板，GPT-6.2 的三维设计质量评分也略低于 RFdiffusion。与 Onava 开展的实验室验证中，团队将预发布版 GPT-6.2 的结构设计制成 322 个 minibinder 并测试 5 个靶点，其中 35 个（10.9%）显示与预期靶点结合，PD-L1、IL-7Rα、TrkA、VEGF-A 和 IL-17A 分别取得 5、3、1、8 和 18 个命中。在序列重设计实验中，MDM2、VEGF-A 和 PD-1 分别有 75/88（85%）、26/42（62%）和 8/59（14%）显示结合，新序列与原序列的中位差异分别为 43%、50%和 15%，重设计抗体也保留了结合能力。不过，SolubleMPNN、ProteinMPNN 等专用模型仍为实验提供序列或参与候选选择，原 RFdiffusion 研究报告的命中率也更高，因此这些结果只是通用设计潜力的早期证据，尚不能证明 GPT-6 已能端到端取代专用系统。

rss · OpenAI News · 11月24日 13:00 · [社区讨论](https://news.ycombinator.com/item?id=50634658)

**「蛋白质设计基础」** 蛋白质由氨基酸链组成，序列会影响其折叠成三维结构，而结构和界面又决定结合对象、稳定性和功能。过去，科学家通常依赖 RFdiffusion、SolubleMPNN 和 ProteinMPNN 等专用模型，分别辅助生成结构、提出氨基酸序列或筛选实验候选；GPT‑6 的研究则尝试通过通用推理和代码处理这些任务，并用提示指定结合位置、形状等约束。需要区分的是，实验验证中 GPT‑6.2 设计的三维结构仍由 SolubleMPNN 等专用模型补充氨基酸序列并协助筛选，因此“无专用模型参与”主要指模型自身的设计能力，而不是整个湿实验流程已经完全自动化。

**「实际影响」** 对 AI 蛋白质设计团队而言，GPT‑6.2 展示了以通用推理和代码串联蛋白设计流程的可行性：Onava 对 322 个 minibinder 的实验中，针对 5 个靶点有 35 个（10.9%）出现预期结合，表明其三维设计已可用于实验室验证。由于序列仍需 SolubleMPNN 等专用模型提供或协助筛选，且完整蛋白质结构预测仍是明显短板，现阶段更适合作为专用工具的编排层，而非完全替代现有蛋白设计系统。

**「社区讨论」** 多位评论者认可 GPT-6 通过编写代码执行蛋白质设计的潜力，有人将其视为模型的“超能力”，也有人认为它更像连接专用生物模型的“胶合层”，因此“超越专用模型”的说法尚为时过早。分歧主要集中在证据强度：评论者质疑 GPT-6.2 究竟主导了结构还是序列设计，并认为现有生物对照偏少、计算探索偏多；另有评论者希望将 GPT 与更强的开放权重生物学模型重新进行基准测试。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/">GPT-6 models demonstrate intrinsic protein-design ... - OpenAI</a></li>
<li><a href="https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/">GPT - 6 models demonstrate intrinsic protein - design ... | OpenAI</a></li>

</ul>
</details>

**标签**: `#protein-design`, `#AI-for-science`, `#foundation-models`, `#code-reasoning`, `#OpenAI`

---

<a id="item-tech-news-3"></a>
### [Active intrusion campaign against Check Point security management servers](https://www.greynoise.io/blog/check-point-security-management-servers-intrusion-campaign) ⭐️ 8.0/10

An active campaign reportedly reconstructs Check Point management-server session-signing keys from weak PRNG output, enabling forged administrator sessions.

hackernews · louiereederson · 11月24日 16:32 · [社区讨论](https://news.ycombinator.com/item?id=50630594)

**标签**: `#Check Point`, `#active exploitation`, `#PRNG vulnerability`, `#session security`, `#cybersecurity`

---

<a id="item-tech-news-4"></a>
### [AI 辅助黎曼猜想证明仍待审查](https://arstechnica.com/ai/2026/11/whats-going-on-with-the-riemann-hypothesis/) ⭐️ 8.0/10

据报道，在 Anthropic 任职的数学家 Levent Alpöge 宣布利用 Claude 生成了一份黎曼猜想的证明。数学家仍在消化和评估该成果，原文也没有提供证明的关键技术步骤，只称 Mathlib Initiative 给出了进一步确认与信息。由于公告措辞颇为华丽，Alpöge 还似乎暗示其中部分内容意在开玩笑，因此目前不能将这项报告视为已经完成同行评审或得到学界公认的突破。黎曼猜想关系到素数分布，对数论和密码学具有深远意义；若证明最终成立，它将展示大语言模型辅助高难度数学研究的新路径。

rss · Ars Technica · 11月24日 20:34

**「背景」** ...

**「潜在影响」** 对数学研究者和 AI 工具开发者而言，最直接的影响是这项由 Anthropic 数学家 Levent Alpöge 借助 Claude 提交的正式证明需要接受严格同行审查，且已有两个团队开始验证相关主张；在独立确认前，黎曼猜想不能被视为已获数学界公认解决。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Alp%C3%B6ge&#x27;s_proof_of_the_Riemann_hypothesis">Alpöge &#x27;s proof of the Riemann hypothesis - Wikipedia</a></li>
<li><a href="https://www.theguardian.com/technology/2026/nov/21/anthropic-riemann-hypothesis-solved-claude-ai">Two groups verify mathematician’s claim that Claude ... | The Guardian</a></li>
<li><a href="https://en.wikipedia.org/wiki/Alp%C3%B6ge&#x27;s_proof_of_the_Riemann_hypothesis">Alpöge &#x27;s proof of the Riemann hypothesis - Wikipedia</a></li>
<li><a href="https://www.theguardian.com/technology/2026/nov/21/anthropic-riemann-hypothesis-solved-claude-ai">Two groups verify mathematician ’s claim that Claude ... | The Guardian</a></li>

</ul>
</details>

**标签**: `#AI for mathematics`, `#Riemann hypothesis`, `#LLM-assisted proof`, `#mathematical research`

---

<a id="item-tech-news-5"></a>
### [Amazon says hackers&\#x27; AI agents found and exploited 0-day with little human input](https://arstechnica.com/security/2026/11/amazon-says-hackers-ai-agents-found-and-exploited-0-day-with-little-human-input/) ⭐️ 8.0/10

Amazon says attackers used Cairn AI agents to autonomously find and exploit a zero-day in a medical-imaging application and gain control of a university server.

rss · Ars Technica · 11月24日 12:30

**标签**: `#AI agents`, `#zero-day exploitation`, `#autonomous penetration testing`, `#Cairn`, `#AI security`

---

<a id="item-tech-news-6"></a>
### [vCenter 9.8 分鉴权绕过漏洞已遭利用](https://thehackernews.com/2026/11/vmware-vcenter-hit-by-another-critical.html) ⭐️ 8.0/10

据报道，VMware vCenter 的目录服务组件 vmdir 存在鉴权绕过漏洞 CVE-2026-123903，CVSS 评分为 9.8；能够访问 vCenter 的攻击者无需有效凭据即可绕过认证并直接进入系统。该漏洞在披露前几天已被零日利用，未授权访问已构成现实威胁。Broadcom 已随针对 VMware 产品线的 23 项漏洞更新发布相应补丁。现有信息未说明受影响版本、具体利用方式或修复细节，使用 vCenter 的组织仍需依据官方公告确认适用范围并完成修补。

telegram · zaihuapd · 11月24日 14:50

**「漏洞背景」** vCenter 的 VMware Directory Service（vmdir）负责目录身份与访问令牌等认证处理，此次 CVE-2026-123903 的核心问题是 vmdir 鉴权绕过。公开技术分析称，失败的 LDAP SASL 绑定仍会在连接上写入所声明身份的访问令牌，使后续明文 LDAP 操作以该身份执行且无需凭据；Broadcom 公告要求按响应矩阵中的 Fixed Version 安装补丁，并明确没有可用的临时变通方案。

**「影响」** 任何能够通过网络访问受影响 vCenter 部署的未认证攻击者，都可能绕过身份验证并取得系统管理员级访问，因此相关组织应立即应用 Broadcom 随 23 项漏洞更新发布的补丁，并排查已被入侵迹象。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/dinosn/CVE-2026-123903">dinosn/ CVE - 2026 - 123903 : CVE - 2026 - 123903 : VMware vCenter vmdir ...</a></li>
<li><a href="https://support.broadcom.com/web/ecx/support-content-notification/-/external/content/SecurityAdvisories/0/39626">Support Content Notification - Support Portal - Broadcom support portal</a></li>
<li><a href="https://www.rapid7.com/blog/post/etr-cve-2026-123890-critical-authentication-bypass-vmware-vcenter/">CVE-2026-123890: Critical Authentication Bypass in VMware vCenter</a></li>
<li><a href="https://brandefense.io/knowledge-hub/vulnerabilities/cve-2026-123903/">CVE-2026-123903: vCenter Auth Bypass, Fix Status</a></li>

</ul>
</details>

**标签**: `#vCenter`, `#鉴权绕过`, `#零日利用`, `#漏洞修复`, `#供应链安全`

---

<a id="item-tech-news-7"></a>
### [过去十二个月的三次 LLM 拐点](https://simonwillison.net/2026/Nov/24/llm-inflection-points/) ⭐️ 7.0/10

Simon Willison 在 AI Engineer Code Summit 主题演讲及后续文章中，将过去十二个月概括为三次 LLM 与编程代理能力拐点，这些判断主要来自个人使用经验而非统一基准测试。第一，2025 年 11 月 24 日发布的 Claude Opus 4.5 让 Claude Code 对多数日常编码任务默认给出正确结果，而同期推出的 GPT-5.1 Instant、GPT-5.1 Thinking、GPT-5.1-Codex 和 GPT-5.1-Codex-Max 也使 Codex 变得可靠实用。第二，Anthropic 在发布受出口管制限制的 Claude Fable 5 后，Willison 将具备“给定目标和工具即可主动解决问题”特征的模型称为“Fable 级模型”，并把 Fable 5 至 5.2、Claude Opus 5.5、GPT-6 Astra 以及可能包括 Gemini 4 Neon 的模型归入这一类；Fable 5.2 曾借助五个 WebAudio 麦克风将异常蜂鸣定位到约 40 厘米范围内。第三，2026 年 9 月至 10 月，前沿模型在 Blender 和 Three.js 三维建模及游戏开发方面显著提升，9 月 22 日发布的 Opus 5.5 经 12 小时试玩和平衡调整后，还把 Willison 的即时战略游戏从乏味变为“非常有趣”，显示模型开始不仅生成可运行的代码，也能围绕体验目标反复迭代。

rss · Simon Willison · 11月24日 23:02

**「背景」** 这里的“拐点”指 Simon Willison 根据个人使用体验，对大语言模型与编码代理在过去 12 个月中三次显著能力跃迁所作的归纳：2025 年 11 月的 Claude Opus 4.5 与 GPT-5.1 系列提高了日常编码可靠性，2026 年 6 月至 7 月的“Fable 级模型”展现出目标驱动、主动调用工具并持续求解的能力，9 月至 10 月则出现 3D 建模与游戏开发能力的明显提升。Willison 将 Claude Fable 5 至 5.2、Claude Opus 5.5 和 GPT-6 Astra 归入“Fable 级”，并认为 Gemini 4 Neon 也可能符合。这是作者基于实际项目形成的分类，而非由统一基准测得的正式代际标准。

**「实际影响」** 对编码代理用户和 AI 辅助游戏开发者而言，Claude Opus 4.5 及同期 GPT-5.1 系列让 Claude Code 和 Codex 开始可靠承担日常任务，而 Fable 级自主代理与 3D 建模、Three.js/Blender 及可玩性迭代能力又把前沿模型的应用门槛推进到复杂目标执行和可用原型生成；但这些主要是个人实践观察，工具结果中的 BenchLM 榜单也标注了支持度与估算差异，不能据此视为普适性能结论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://simonwillison.net/2026/Nov/24/llm-inflection-points/">Three LLM inflection points in twelve months - simonwillison.net</a></li>
<li><a href="https://aiweekly.co/alerts/simon-willison-names-three-llm-inflection-points-in-a-year">Simon Willison names three LLM inflection points in a year</a></li>
<li><a href="https://injazai.com/en/news/llm-inflection-points-opus-fable">Three LLM inflection points in 12 months: from Opus 4.5 to ...</a></li>
<li><a href="https://injazai.com/en/news/llm-inflection-points-opus-fable">Three LLM inflection points in 12 months: from Opus 4.5 to ...</a></li>
<li><a href="https://www.learn.telusko.com/newsletter/three-llm-leaps-reliable-coding-agents-fable-class-initiative-and-3d-game-design">Three LLM leaps: Reliable coding agents, Fable-class ...</a></li>
<li><a href="https://benchlm.ai/coding">Best LLM for Coding (November 2026): SWE-bench ...</a></li>

</ul>
</details>

**标签**: `#LLMs`, `#coding agents`, `#AI engineering`, `#software development`

---

<a id="item-tech-news-8"></a>
### [微软云故障暴露部署与扩容盲区](https://arstechnica.com/gadgets/2026/11/microsofts-historic-cloud-outage-exposed-an-engineering-fog-of-war/) ⭐️ 7.0/10

微软在 11 月 12 日发生全球性 Microsoft 365 中断，Exchange Online、Teams 和 Outlook 受到影响；微软云核心业务总裁 Jason Henderson 称，这是 Exchange Online 历史上客户影响最严重的一次事故。11 月 20 日的事故后报告将根因指向 7 月引入但未被发现的 Windows 可伸缩性缺陷，该缺陷导致网关进程出现锁争用，而当时因维护已有近 14%的网关服务器容量离线。Teams 流量故障转移随后又将额外负载施加到已经承压的基础设施上。据路透社审阅但微软尚未公开的内部备忘录，微软已启动名为“Code Red”的工程响应改革，因为一项紧急生产修复用了五至六天才在全球完全生效，而其对最紧急安全修复的目标是一个小时内完成安全部署。

rss · Ars Technica · 11月24日 22:36

**「工程迷雾与事故复盘」** “工程迷雾”是指在高复杂度生产系统中，故障模式、真实影响范围和修复风险往往难以及时看清，尤其是在代码缺陷、容量变化与流量切换相互叠加时。此次事故中，7 月引入且未被发现的 Windows 可扩展性缺陷造成网关进程锁争用，Teams 流量故障转移进一步增加负载，而维护期间近 14% 的网关容量离线，最终使多个 Microsoft 365 服务受到影响。事故后的“Code Red”改革因此不只针对代码修复，也涉及渐进式发布、容量管理和可观测性；内部备忘录称紧急修复从检测到全球安全部署耗时五至六天，而目标是一个小时。

**「影响」** 对依赖 Microsoft 365 的组织而言，此次事故表明维护期容量收缩、隐藏的可伸缩性缺陷与流量故障转移叠加后，可能迅速演变为全球性服务中断，凸显变更验证、容量规划和分阶段发布的重要性。整改措施的实际成效尚未公开，部分关键结论也仅来自微软未公开的内部备忘录。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cybersecuritynews.com/microsoft-outage-incident-report/">Microsoft Reveals How a Hidden Windows Bug Took Down ...</a></li>
<li><a href="https://windowsreport.com/microsoft-explains-root-cause-of-massive-outlook-and-exchange-outage-reveals-three-failures-behind-global-meltdown/">Microsoft Explains Root Cause of Massive ... - Windows Report</a></li>
<li><a href="https://www.365fanatic.com/m365-outage-12-november-2026-final-report/">Microsoft 365 outage 12 November 2026: final report | 365Fanatic</a></li>

</ul>
</details>

**标签**: `#cloud reliability`, `#Microsoft 365`, `#incident response`, `#scalability`, `#deployment engineering`

---

<a id="item-tech-news-9"></a>
### [Tidal 将删除 2700 万首全 AI 生成曲目](https://arstechnica.com/ai/2026/11/tidal-will-ban-fully-ai-generated-music-on-december-9/) ⭐️ 7.0/10

Tidal 宣布将于 2026 年 12 月 9 日删除平台现有的 2700 万首完全由 AI 生成的曲目，占其音乐目录的 6.3%，并禁止此类内容继续上传。数据显示，过去 90 天新上传曲目中完全由 AI 生成的比例为 43%，11 月 6 日更升至 60%，促使平台收紧此前仅标注和取消变现的政策。Tidal 表示，96% 的 AI 标记曲目在过去 90 天播放量为零，因此删除预计不会对业务造成实质负面影响。平台仍允许使用 AI 工具辅助、但最终作品包含人类元素的歌曲；此前 Tidal 还因冒充艺人移除了约 6.6 万首曲目。

rss · Ars Technica · 11月24日 17:34

**「背景」** Tidal 于 2026 年 7 月推出首版 AI 政策，对完全由 AI 创作的歌曲进行标记并取消变现。此次公告将治理措施升级为彻底删除，同时继续区分“完全由 AI 生成”与“使用 AI 辅助”的歌曲。

**「影响」** 完全依赖 AI 批量生成并上传曲目的发行方和上传者将失去这些曲目的平台曝光及后续播放分成，包含明确人类创作元素的 AI 辅助作品则不受禁令影响。Tidal 声称相关曲目几乎无人收听，但音乐人仍需关注全 AI 曲目的识别和审核规则。

**标签**: `#generative AI`, `#music streaming`, `#AI policy`, `#copyright`, `#Tidal`

---

<a id="item-tech-news-10"></a>
### [英伟达火速恢复黄仁勋 CEO 职务](https://arstechnica.com/tech-policy/2026/11/how-trump-and-silicon-valley-forced-nvidia-to-take-jensen-huang-back/) ⭐️ 7.0/10

据《金融时报》报道，英伟达创始人兼 CEO 黄仁勋在辞职不到两周后重返圣克拉拉总部，董事会迅速恢复其职务。报道称，这一逆转受到特朗普施加的压力推动；黄仁勋的硅谷盟友组成“作战室”，游说特朗普和副总统 JD·万斯，强调他之于英伟达、美国 AI 产业、股市及整体经济的重要性。黄仁勋此前据称因与一名客户及一名涉嫌中国间谍发生婚外情而辞职，另有一桩涉及下属的婚外情报道，但相关细节主要依赖匿名消息。复职消息推动英伟达市值增加近 1 万亿美元，不过其市值仍比一个月前低约五分之一。黄伟达与黄仁勋仍面临 FBI、SEC 及国会调查，治理问题以及与涉嫌向中国走私芯片者的关系也尚未厘清。

rss · Ars Technica · 11月24日 14:56

**「背景」** 英伟达最初以视频游戏芯片起家，黄仁勋带领公司转向人工智能处理器，使其成为该领域的主导供应商，并深度受益于全球 AI 热潮。黄仁勋不仅是公司的创始人，其领导力也被视为美国维持 AI 及对华竞争优势的重要支柱，因此他与英伟达的关系一直具有超出单一公司治理的技术与政策意义。

**「影响」** 黄仁勋在特朗普介入后复任 Nvidia CEO，缓解了市场对该公司领导层及 AI 芯片业务连续性的担忧；消息推动其股价上涨 31%，市值增加近 1 万亿美元。尽管如此，英伟达股价仍较一个月前低约五分之一，且相关的 FBI、SEC 和国会调查并未因复职而结束。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theguardian.com/technology/2026/nov/23/jensen-huang-reinstated-as-nvidia-chief-executive">Jensen Huang reinstated as Nvidia CEO after Trump ... | The Guardian</a></li>
<li><a href="https://www.ft.com/content/20d2ebe3-e945-4659-a122-31bf85a4e4e5?syn-25a6b1a6=1">Jensen Huang ’s return as it happened: Nvidia gains nearly $1tn in...</a></li>
<li><a href="https://www.reuters.com/technology/nvidia-reinstates-jensen-huang-ceo-2026-11-23/">Huang returns as Nvidia CEO after Trump intervention in ...</a></li>
<li><a href="https://www.cnbc.com/2026/11/23/nvidia-jensen-huang-ceo.html">Jensen Huang reinstated as Nvidia CEO. Stock skyrockets 31%</a></li>
<li><a href="https://www.hindustantimes.com/ht-explainers/jensen-huang-returns-nvidia-ceo-trump-ai-bubble-stock-market-crash-101795499680720.html">Jensen Huang returns as Nvidia CEO: Did Trump save the &#x27;AI ...</a></li>

</ul>
</details>

**标签**: `#Nvidia`, `#Jensen Huang`, `#AI chips`, `#tech policy`, `#corporate governance`

---

<a id="item-tech-news-11"></a>
### [数十艘油轮及化学品运输船近期遭黑客攻击](https://techcrunch.com/2026/11/24/dozens-of-oil-and-shipping-tankers-hacked-in-recent-weeks-per-report/) ⭐️ 7.0/10

据报道，过去数周已有数十艘油轮和化学品运输船遭到网络攻击。伊朗被列为这些袭击的主要嫌疑方。现有材料未披露攻击的具体技术细节、受害船舶清单或确认嫌疑归属的证据，因此该归因仍属报道中的判断。

rss · TechCrunch · 11月24日 21:09

**「海事网络攻击背景」** 海事网络攻击可能涉及船舶通信、导航设备以及与港口或船队相连的管理系统，因此针对油轮和化学品船的事件不仅影响单船运行，也可能波及能源与危险品物流。近期针对数十艘商业船只和油轮的网络攻击，与同期霍尔木兹海峡油轮触雷起火属于不同类型的安全事件，不应将黑客攻击与物理袭击混为一谈。美国正调查伊朗是否参与这些网络攻击，但现有公开信息仅表明调查和嫌疑指向，尚不足以确认责任归属。

**「海上能源航运风险上升」** 数十艘油轮和化学品运输船遇袭，加剧了全球海上贸易与能源供应的安全担忧；报道显示，一艘载有近 230 万桶原油、驶往得州的油轮遭黑客攻击后不得不请求 FBI 和美国海岸警卫队协助处置。伊朗是主要嫌疑人的说法仍处于调查阶段，并非已获确认的归因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.youtube.com/watch?v=93kTFBPDQGM">NEW: US probes possible Iran CYBERATTACKS targeting dozens of ...</a></li>
<li><a href="https://www.cnbc.com/2026/11/24/iran-trump-hormuz-crude-.html">Iran says three tankers hit mines in Hormuz despite U.S. escort</a></li>
<li><a href="https://www.yahoo.com/news/world/articles/iran-vows-end-u-naval-113037780.html">Iran vows to end U.S. naval blockade by &quot;all available means&quot;</a></li>
<li><a href="https://gulfnews.com/world/mena/cyber-threats-targeting-50-ships-spark-fears-of-escalating-us-iran-conflict-in-maritime-trade-1.500758663">Cyberattacks on 50 Ships Raise Alarms Over US-Iran Maritime ...</a></li>
<li><a href="https://cybernews.com/news/iran-oil-tanker-cyberattack-fbi-texas/">Tanker cyberattack hits two US-bound oil ships, Iran link ...</a></li>
<li><a href="https://www.ibtimes.com/us-investigates-cyberattacks-commercial-ships-3810121">US Probes Iran’s Possible Role In Cyberattacks On Up To 50 ...</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#maritime security`, `#critical infrastructure`, `#Iran`

---

<a id="item-tech-news-12"></a>
### [亚马逊收购 Decart，押注软件缩小芯片差距](https://techcrunch.com/2026/11/24/amazons-decart-acquisition-is-a-bet-on-using-software-to-narrow-the-gap-with-nvidia-in-the-ai-chip-race/) ⭐️ 7.0/10

亚马逊已决定收购人工智能模型与芯片优化公司 Decart，交易金额据报道为 75 亿美元。此次收购是亚马逊提升 Trainium AI 芯片效率、增强其与英伟达硬件竞争力的重要软件押注，核心思路是通过软件优化弥补专用加速器在整体生态和性能上的差距。现有信息未披露 Decart 的具体技术、整合方案或 Trainium 性能提升数据，因此尚无法量化此次收购的效果。

rss · TechCrunch · 11月24日 15:51

**「背景」** Decart 是一家前沿 AI 实验室，其 Decart Optimization Stack（DOS）被描述为一种面向异构 AI 加速器的软件层，用于让模型工作负载在不同芯片上更高效地运行，并据报道支持 Nvidia GPU、Google TPU 和 Amazon Trainium。对 Amazon 而言，引入这类跨芯片优化技术，核心意义在于借助软件提升 Trainium 的硬件利用率和易用性，而不只是与 Nvidia 比拼芯片的峰值性能。另需注意，收购 Decart 当时仍被报道为约 70 亿美元的交易谈判，并非已经完成的交易，Amazon 也未对此置评。

**「Trainium 客户的潜在收益」** Amazon 表示，收购 Decart 的 AI 优化技术将有助于提升推理效率和自研芯片性能，使客户能够以更低成本、更快速度训练和运行模型；随着 Trainium 被推向外部销售，AI 开发者和云客户可能获得 Nvidia 之外的加速器选择。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.agenticbrew.ai/news/e6c7ea0d-0de0-4648-8f9c-a1264143a131/amazon-in-talks-to-acquire-decart-for-7b">Amazon in talks to acquire Decart for ~$ 7 B — AI News | Agentic Brew</a></li>
<li><a href="https://www.earlybird.email/p/amazon-in-talks-to-buy-ai-startup-decart-for-about-7-billion">Amazon in Talks to Buy AI Startup Decart for About $ 7 Billion</a></li>
<li><a href="https://wirandhika.my.id/en/amazon-decart-7-billion-acquisition-talks/">Amazon Eyes $ 7 B Decart Acquisition | WiraNews</a></li>
<li><a href="https://techcrunch.com/2026/11/24/amazons-decart-acquisition-is-a-bet-on-using-software-to-narrow-the-gap-with-nvidia-in-the-ai-chip-race/">Amazon &#x27;s Decart acquisition is a bet on using software to narrow the...</a></li>
<li><a href="https://techcrunch.com/2026/11/23/amazon-snaps-up-decarts-ai-optimization-tech-for-7-5b-as-it-prepares-to-sell-trainium-chips/">Amazon snaps up Decart &#x27;s AI optimization tech for... | TechCrunch</a></li>
<li><a href="https://www.aboutamazon.com/news/company-news/amazon-decart-ai-optimization">Amazon to purchase Decart &#x27;s AI optimization technology</a></li>

</ul>
</details>

**标签**: `#AI accelerators`, `#Amazon Trainium`, `#Decart acquisition`, `#chip optimization`, `#Nvidia competition`

---

<a id="item-tech-news-13"></a>
### [CrowdStrike 拟以 440 亿美元收购 Zscaler](https://www.theregister.com/security/2026/11/24/crowdstrike-splashes-44b-on-zscaler-customers-brace-for-the-bill/5311877) ⭐️ 7.0/10

据报道，CrowdStrike 拟以 440 亿美元收购 Zscaler，该交易被称为网络安全行业创纪录的收购案。若交易完成，两家公司的安全产品预计将进一步整合，可能影响客户现有的安全架构和采购组合。系统管理员则担忧整合带来价格上涨与供应商锁定，但现有材料未提供交易结构、兼容性安排或具体定价变化，实际影响仍不明确。

rss · The Register · 11月24日 12:22

**「交易背景」** CrowdStrike 已同意以全股票交易收购网络安全厂商 Zscaler，交易价值约 439 亿美元，预计于 CrowdStrike 2028 财年下半年完成。该交易是在人工智能加剧网络攻击担忧、企业寻求整合安全能力的背景下达成，因此可能扩大 CrowdStrike 的产品覆盖，同时引发客户对整合后定价和供应商锁定的担忧。

**「客户影响」** 这项已达成协议的交易将终端与网络安全进一步集中到同一厂商，Zscaler 约 8,000 家客户在续约时可能面临更高的价格和更深的平台绑定，但也可能获得更统一的零信任安全整合。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/11/23/crowdstrike-zscaler-aquisition-ai-cyberattacks.html">CrowdStrike to buy Zscaler in $ 44 B deal as AI supercharges...</a></li>
<li><a href="https://www.nytimes.com/2026/11/23/business/crowdstrike-zscaler-cybersecurity.html">Two Major Cybersecurity Firms to Combine in $ 44 Billion Deal</a></li>
<li><a href="https://www.bloomberg.com/news/articles/2026-11-23/crowdstrike-reaches-44-billion-cybersecurity-deal-for-zscaler">CrowdStrike Reaches $ 44 Billion Cyber Deal for Zscaler - Bloomberg</a></li>
<li><a href="https://www.forbes.com/sites/stevemcdowell/2026/11/23/what-crowdstrikes-439-billion-zscaler-acquisition-means-for-buyers/">What CrowdStrike’s $43.9 Billion Zscaler Acquisition Means ...</a></li>
<li><a href="https://www.theregister.com/security/2026/11/24/crowdstrike-splashes-44b-on-zscaler-customers-brace-for-the-bill/5311877">CrowdStrike splashes $44B on Zscaler, customers brace for the ...</a></li>
<li><a href="https://www.zscaler.com/press/crowdstrike-acquire-zscaler-bringing-network-security-and-zero-trust-falcon-platform">CrowdStrike to Acquire Zscaler for Zero Trust</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#acquisitions`, `#CrowdStrike`, `#Zscaler`, `#vendor lock-in`

---

<a id="item-tech-news-14"></a>
### [Microduck 的 ToF 仿真到现实避障工作流](https://huggingface.co/blog/nvidia/microduck-obstacle-avoidance) ⭐️ 6.0/10

这期教程展示了如何在 NVIDIA Isaac Lab 与 Newton 中为 Microduck 增加局部避障能力：保留此前导出的 backlash 行走策略权重不变，另行训练一个基于飞行时间（ToF）传感器的导航控制器。手柄用于选择运动方向，控制器以 50 Hz 调整前向、横向和偏航速度命令，再由固定的行走策略转换为关节动作；训练用 critic 可读取额外的仿真状态，但部署只需 actor、归一化器及实机可获得的状态。MicroDuckToFCamera 基于 Newton 的 LegacyMultiMeshRayCasterCamera 模拟 VL53L5CX 传感器，以 15 Hz 提供 8×8 距离网格，视场角为 45°、范围为 0.12–4 米，并通过噪声、延迟、缺失读数和安装偏差进行随机化。环境使用纸箱、办公室垃圾桶、床头柜、锥体及 Hugging Face SimReady Central 的固定版本 OpenUSD 资产生成多样化障碍布局；示例以 PPO 并行训练 16,384 个环境、运行 1,500 次迭代，而 NVIDIA DGX Spark 上的较小配置使用 4,096 个环境、3,000 次更新并耗时约 6 小时，环境数减少时达到相近表现可能需要更多训练时间。工作流还涵盖策略回放评估、ONNX 导出以及实机测试接口准备；硬件测试需要兼容的 Linux/NVIDIA GPU 环境、同一行走策略检查点、已记录配置的受支持 ToF 传感器、配对手柄和带障碍物的平整测试区域。

rss · Hugging Face Blog · 11月24日 16:34

**「分层控制与仿真到现实」** 此前，Microduck 已通过 Isaac Lab 与 Newton 在仿真中训练并以 ONNX 导出行走策略，再部署到实体双足机器人；该策略负责保持平衡并将运动指令转换为关节动作，本身不负责绕障。新教程因此采用分层控制：冻结行走策略，另用基于 8×8、15 Hz VL53L5CX ToF 测距信息的导航策略以 50 Hz 调整前进、横向和偏航指令，并通过 Newton 射线投射模拟传感器。为缩小仿真与现实之间的差距，训练还随机化传感器安装偏差、噪声、延迟和缺测。

**「实际影响」** Microduck 使用者和机器人开发者可依照该 Isaac Lab/Newton 教程，在冻结既有步态策略的情况下训练并导出基于 ToF 的局部避障控制器，再部署到实体机器人，从而将导航学习与平衡策略解耦并避免重新训练后者。实机采用仍需兼容的 NVIDIA GPU 和驱动、受支持且已配置的 ToF 传感器，文中未提供跨场景障碍规避成功率等广泛验证数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/blog/nvidia/microduck-obstacle-avoidance">Microduck Obstacle Avoidance: A Sim2Real Workflow with Isaac ...</a></li>
<li><a href="https://huggingface.co/blog/nvidia/microduck-isaac-lab-sim-to-real">Train in Simulation, Deploy on a Real Robot: Microduck with ...</a></li>
<li><a href="https://developer.nvidia.com/blog/using-ai-agents-to-teach-robots-like-microduck-to-walk-in-simulation/">Using AI Agents to Teach Robots Like Microduck to Walk in ...</a></li>
<li><a href="https://huggingface.co/blog/nvidia/microduck-obstacle-avoidance">Microduck Obstacle Avoidance: A Sim2Real Workflow with Isaac ...</a></li>

</ul>
</details>

**标签**: `#sim-to-real robotics`, `#obstacle avoidance`, `#NVIDIA Isaac Lab`, `#Newton physics simulation`, `#time-of-flight sensing`

---

<a id="item-tech-news-15"></a>
### [用 Astra 和 Codex 搜寻遥远行星](https://openai.com/index/searching-for-distant-planets-with-astra) ⭐️ 6.0/10

OpenAI 介绍了两名业余天文学家 Kevin Bond 与 Ethan Byrd 利用公开望远镜数据寻找系外行星候选体的案例。Bond 用 Codex 比较已发表的方法、将其组合成搜索程序，并让两个 AI 代理分别扫描光变曲线和复核候选信号；他处理了开普勒望远镜约 10 万颗恒星的数据，筛出 200 多个信号，其中 10 个来自已确认行星。SETI Institute 的天文学家独立复核后再次找到其中两个信号：KIC 5689121 每 13.8 天出现一次亮度下降，若由行星造成，其直径约为地球的 2.4 倍；KIC 6691030 每 4.8 天出现一次下降，尺度与小于海王星的行星一致。Byrd 则让 Astra 审阅公开方法、编写并运行搜索程序，对约 1,900 万颗恒星的 TESS 及其他公共档案数据进行初筛，得到 49 个候选体，其中最强候选已提交给 TESS 任务研究人员等待进一步分析，另有两个待提交，搜索仍在继续。该案例显示，AI 辅助编码和大规模信号筛查能让业余研究者产出可供专业团队跟进的线索，但这些候选体尚未得到确认，可能需要数月或数年的观测排除双星掩食、仪器变化等假象，并通过统计检验、补充观测和同行评议验证。

rss · OpenAI News · 11月24日 11:00

**「凌日法与 AI 搜星背景」** 系外行星凌日法通过测量恒星亮度的周期性微小下降来寻找候选信号；重复出现的凹陷可能由行星遮挡造成，但双星互食和望远镜温度变化也会产生类似现象，因此仍需后续观测、径向速度测量和同行评议来确认。开普勒空间望远镜（2009—2018 年）与 TESS（2018 年发射）积累的公开巡天数据，可供研究者编写程序并在大量恒星中筛查凌日信号。AI 辅助搜星并非新概念：2017 年，研究人员以开普勒望远镜的 1.5 万条已审查信号训练神经网络，并借此发现 Kepler-90 的第八颗行星，奠定了如今 Codex 和 Astra 辅助公民科学搜索的技术背景。

**「实际影响」** Codex 和 Astra 已帮助业余研究者从 Kepler、TESS 等公开数据中筛出可交由专业团队复核的系外行星候选目标，其中两个信号还由 SETI Institute 的天文学家独立找回，为公民科学参与行星发现提供了更具体的途径。不过这些结果尚未构成行星确认，相关候选仍需进一步分析、后续观测和同行评审，确认过程可能持续数月或数年。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/searching-for-distant-planets-with-astra/">Searching for distant planets with Astra | OpenAI</a></li>
<li><a href="https://science.nasa.gov/exoplanets/citizen-science/">Citizen Science - NASA Science</a></li>

</ul>
</details>

**标签**: `#AI for science`, `#exoplanet detection`, `#astronomy`, `#Codex`, `#Astra`

---

<a id="item-tech-news-16"></a>
### [字节跳动开源异步强化学习后训练框架 Laminar](https://news.google.com/rss/articles/CBMinAFBVV95cUxOREtoZmNWcnFoV0VTT2trNlBya2JEZllsaUFSYVgwcm9sMk5iZUJtR1FIVjJtRXhCaUh5ZjdFbE1SZFBzbC1yalZ2Y2dpMjY3X3ZOTTJhcG5fanJmTWZaQmptc3dEV3JtcGl5NExCeFh2QXVEVHZhSDczM0lBbERUeVliQzc3a0Utekx4ME0zUlJNckloYWtjTzZxUHjSAZwBQVVfeXFMTkRLaGZjVnJxaFdFU09razZQcmtiRGZZbGlBUmFYMHJvbDJOYmVCbUdRSFYybUV4QmlIeWY3RWxNUmRQc2wtcmpWdmNnaTI2N192Tk0yYXBuX2pyZk1mWkJqbXN3RFdybXBpeTRMQnhYdkF1RFR2YUg3MzNJQWxEVHlZYkM3N2tFLXpMeDBNM1JSTXJJaGFrY082cVB4?oc=5) ⭐️ 6.0/10

据 MarkTechPost 报道，字节跳动研究人员开源了 Laminar，这是一个面向 AI 模型后训练的异步强化学习（RL）框架。该项目聚焦强化学习后训练并采用异步执行方式，为研究人员和工程师提供了一个可进一步评估的开源工具。现有报道未说明其系统架构、兼容范围、基准测试与性能数据，也未提供许可证、代码仓库地址或实际采用情况。因此，目前只能确认其开源定位，尚无法判断其相对现有 RL 框架的优势、局限或落地成熟度。

google\_news · MarkTechPost · 11月25日 05:42

**「相关背景」** 强化学习后训练通常涉及...。为突破同步（lockstep）更新造成的扩展瓶颈，Laminar 采用完全解耦架构，以轨迹级异步方式独立生成和消费轨迹，并以中继工作者组成的分布式参数服务替代全局更新；相关论文题为...，arXiv 版本发表于 2025 年 10 月 14/15 日。

**「实际影响仍待验证」** Laminar 的开源为 AI 和机器学习开发者提供了一个探索异步强化学习后训练流程的公开实现，但现有材料未披露许可证、兼容性、基准测试或采用情况，因此尚无法判断其实际性能收益与部署门槛。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2510.12633">[2510.12633] Laminar: A Scalable Asynchronous RL Post ...</a></li>
<li><a href="https://arxiv.org/pdf/2510.12633">Laminar: A Scalable Asynchronous RL Post-Training Framework</a></li>

</ul>
</details>

**标签**: `#reinforcement-learning`, `#AI-post-training`, `#open-source`, `#AI-frameworks`

---