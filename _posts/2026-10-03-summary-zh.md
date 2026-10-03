---
layout: default
title: "Horizon Summary: 2026-10-03 (ZH)"
date: 2026-10-03
lang: zh
---

> 从 122 条内容中筛选出 17 条重要资讯。

---

**科技新闻**
1. [AI 首次击败人类最强军棋选手，且训练成本极低](#item-tech-news-1) ⭐️ 8.0/10
2. [Fortinet 警告 FortiMail 零日漏洞正遭活跃利用](#item-tech-news-2) ⭐️ 8.0/10
3. [苹果收紧 macOS 完全磁盘访问权限以应对 AI 代理滥用风险](#item-tech-news-3) ⭐️ 7.0/10
4. [美国逮捕涉嫌走私 3 亿美元 Nvidia 芯片至中国的科技公司 CEO](#item-tech-news-4) ⭐️ 7.0/10
5. [Meta 开源 Muse AI 智能体代码，支持 DIY 硬件设备](#item-tech-news-5) ⭐️ 7.0/10
6. [Epic 暂停产品开发数周以修复危及患者数据的安全漏洞](#item-tech-news-6) ⭐️ 7.0/10
7. [arXiv 实施每月两篇投稿上限 应对 AI 生成低质论文](#item-tech-news-7) ⭐️ 7.0/10
8. [Don’t be fooled—LLMs don’t reason](#item-tech-news-8) ⭐️ 7.0/10
9. [OpenAI 发布 GPT-6 模型家族实用指南](#item-tech-news-9) ⭐️ 7.0/10
10. [Google Research 公布 Cogentic：多智能体协调数学证明探索](#item-tech-news-10) ⭐️ 7.0/10
11. [Claude Code 新增 mods 自定义扩展机制](#item-tech-news-11) ⭐️ 7.0/10
12. [亚马逊十亿美元社区投入难消数据中心反对声](#item-tech-news-12) ⭐️ 6.0/10
13. [AllenAI 开源 AstaBrief 8B：面向科研报告的快速生成模型](#item-tech-news-13) ⭐️ 6.0/10
14. [ServiceNow CoreAI 发布 AutoSynthData：为 企业 Agent 自动合成训练数据](#item-tech-news-14) ⭐️ 6.0/10
15. [AI 触发的快速反应通知与住院患者死亡率降低相关](#item-tech-news-15) ⭐️ 6.0/10

**财经新闻**
1. [美联储 10 月加息概率骤降，12 月加息预期仍存](#item-finance-news-1) ⭐️ 7.0/10
2. [Bitget 交易所遭近 3.88 亿美元黑客攻击，CEO 称预计难以追回大部分资金](#item-finance-news-2) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [AI 首次击败人类最强军棋选手，且训练成本极低](https://arstechnica.com/science/2026/10/ai-finally-beat-the-best-stratego-player-in-history-and-did-it-on-a-budget/) ⭐️ 8.0/10

一项发表于《自然》期刊的研究称，AI 系统终于在军棋（Stratego）这一长期被视为不完美信息博弈终极挑战的游戏中，击败了人类历史上最强的选手。该算法在训练效率上比 DeepMind 2022 年的 DeepNash 提升了约 34 倍，仅用极低的算力预算便达到了超越人类的水平。由于军棋隐藏信息所形成的博弈树远大于扑克，这一突破被视为不确定性下决策问题的重大算法进展，而非单纯依靠算力堆叠。

hackernews · PaulHoule · 10月2日 14:11 · [社区讨论](https://news.ycombinator.com/item?id=49933740)

**标签**: `#ai`, `#game-theory`, `#imperfect-information`, `#research`, `#reinforcement-learning`

---

<a id="item-tech-news-2"></a>
### [Fortinet 警告 FortiMail 零日漏洞正遭活跃利用](https://www.theregister.com/security/2026/10/02/fortinet-sounds-the-alarm-over-actively-exploited-fortimail-zero-day/5300803) ⭐️ 8.0/10

Fortinet 发布安全警告，称其 FortiMail 邮件安全产品线存在一个未经认证的零日漏洞，目前已在野遭到活跃利用。该漏洞无需登录凭据即可触发，显著降低了攻击门槛，使其对暴露在互联网上的 FortiMail 部署构成严重威胁。据 The Register 报道，尽管 Fortinet 已就此发出警报，但部分管理员仍在等待针对该漏洞的修复补丁发布，相关缓解措施与补丁可用性的具体细节在所提供的摘要中未予披露。鉴于 FortiMail 普遍部署于企业邮件网关位置，该漏洞对依赖其进行垃圾邮件防护、邮件过滤与数据防泄漏的组织具有直接的安全影响。

rss · The Register · 10月2日 10:53

**「背景」** FortiMail 是 Fortinet 公司推出的电子邮件安全网关产品,用于在企业邮件入口处拦截垃圾邮件、病毒以及定向邮件攻击,因此一旦其自身出现严重漏洞将直接暴露大量组织的邮件基础设施。本次披露的 CVE-2026-104286 是一个未经身份验证即可被远程利用的命令执行缺陷,攻击者仅需通过精心构造的 HTTP 请求即可在设备底层系统写入任意文件,CVSS 评分高达 9.8,属于严重级别。零日漏洞\(zero-day\)指的是厂商尚无补丁可用的安全缺陷,正因如此,CISA 已将其加入 Known Exploited Vulnerabilities 目录,并要求美国联邦民事机构在指定期限前完成取证排查和缓解措施。

**「影响」** 对运行 FortiMail 的企业而言，该未经认证且正遭活跃利用的零日漏洞意味着面向互联网的邮件网关存在被远程攻破的现实风险；在补丁尚未覆盖到位前，管理员应优先核查 FortiMail 实例的暴露面与可用的官方临时缓解方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/fortinet-warns-of-critical-fortimail-flaw-exploited-in-zero-day-attacks/">Fortinet warns of critical FortiMail flaw exploited in zero - day attacks</a></li>
<li><a href="https://www.theregister.com/security/2026/10/02/fortinet-sounds-the-alarm-over-actively-exploited-fortimail-zero-day/5300803">Fortinet sounds the alarm over actively exploited FortiMail zero - day</a></li>
<li><a href="https://thehackernews.com/2026/10/critical-fortimail-zero-day-flaw.html">Critical FortiMail Zero - Day Flaw Exploited in Attacks Allows...</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#vulnerability`, `#zero-day`, `#Fortinet`, `#enterprise-security`

---

<a id="item-tech-news-3"></a>
### [苹果收紧 macOS 完全磁盘访问权限以应对 AI 代理滥用风险](https://arstechnica.com/security/2026/10/apple-changes-full-disk-access-permissions-to-curb-abuse-from-ai-agents/) ⭐️ 7.0/10

苹果宣布将调整 macOS &quot;完全磁盘访问&quot;（Full Disk Access）权限的控制方式，要求用户在授予应用该权限时采取更明确的主动操作。该权限历来允许应用读取用户文件、邮件、信息和浏览历史等非系统级数据，苹果在周五的更新中警告，随着 AI 助手日益自主，宽泛的文件访问带来的隐私风险正在放大。这一调整的背景是专栏作家 Jason Aten 公开指控 Meta 的通用 AI 代理 Muse 在未经其明确同意的情况下读取了其 Apple Messages 对话；Meta CTO David Singleton 回应称该集成为 opt-in，需同时开启系统级完全磁盘访问和应用内的 Messages 连接器，但 macOS 安全专家 Patrick Wardle 反驳称从技术角度看授予完全磁盘访问后任何非根目录文件都可读取。Meta 发言人在被追问时仅重述了 Singleton 的原话，未提供进一步技术解释；苹果未在公告中点名 Meta，也未公布具体改动细节或上线时间。

rss · Ars Technica · 10月2日 23:03

**「背景说明」** macOS 的&quot;完全磁盘访问&quot;是一项系统级隐私权限，获准后应用可访问用户的本地文件、邮件、信息数据库、浏览器历史和 cookie 等数据，且无需对每类数据单独授权。该权限设计上较为粗放，长期以来仅依赖用户一次性确认。近期通用 AI 代理开始获得此类权限，其自主执行任务的能力被业界比作&quot;电锯&quot;等需要小心操作的电动工具，由此引发了对 AI 代理权限边界的新一轮讨论。

**「影响」** 对依赖完全磁盘访问权限读取用户数据的 AI 代理类第三方应用而言，未来将面临更严格的授权确认流程；不过苹果尚未披露具体技术改动和部署时间表，实际影响范围仍有待新机制上线后才能明确。

**标签**: `#AI agents`, `#macOS security`, `#privacy`, `#platform permissions`, `#Meta`

---

<a id="item-tech-news-4"></a>
### [美国逮捕涉嫌走私 3 亿美元 Nvidia 芯片至中国的科技公司 CEO](https://arstechnica.com/tech-policy/2026/10/us-arrests-tech-ceo-accused-of-smuggling-300m-in-nvidia-chips-into-china/) ⭐️ 7.0/10

美国司法部逮捕了 Earthmade Computer 公司 38 岁的 CEO Greg Lui，指控他通过虚假文件掩盖将价值超过 3 亿美元的服务器转运至中国的走私行为。据 FBI 起诉书，Lui 涉嫌与马来西亚和新加坡的货运代理公司合谋，将载有 Nvidia A100 和 H100 GPU 的服务器从美国出口后再转运至中国。这些 GPU 虽非 Nvidia 最先进型号，但仍具备训练大语言模型的能力，美国担忧其大规模流向中国可能加速 AI 或军事能力发展。证据包括 2024 年关于 70 台服务器的电子邮件与银行记录，显示部分货物最终流入杭州一家被《华尔街日报》称为中国 AI 枢纽的中国公司，Lui 还使用化名&quot;Jackie Lui&quot;伪造假买家 CEO 身份以欺骗美国官员。该走私计划据称从 2023 年 10 月持续至 2026 年 8 月。

rss · Ars Technica · 10月2日 18:39

**「背景：美对华 AI 芯片出口管制与绕道走私」** 自 2022 年起，美国商务部以国家安全为由，陆续收紧对华先进半导体出口管制，将 Nvidia 等公司可用于大规模 AI 训练的高端数据中心 GPU——包括 A100（2020 年发布）和 H100（2022 年发布）——列入出口管控清单，要求向中国出口须申请许可。由于正当中获取渠道受限，部分买家通过马来西亚、新加坡等东南亚第三国转运货物并伪造单据，试图规避许可审查，这已成为美国司法部近年来重点打击的一类走私模式。

**「影响」** 对于向中国转运受限 AI 芯片的制造商、货运代理及东南亚中间商而言，此案显示美国司法部正依据电邮和银行记录积极追查经马来西亚、新加坡转口的 Nvidia A100 与 H100 走私行为，相关企业的合规与刑事风险显著上升；该案并非孤例，过去一年已发生多起类似起诉，表明这是持续执法模式而非政策转向。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.yahoo.com/news/us/articles/greg-lui-arrested-smuggling-nvidia-130550365.html?fr=sycsrp_catchall">Greg Lui arrested for smuggling Nvidia AI chips to China - Yahoo</a></li>
<li><a href="https://nypost.com/2026/10/01/us-news/california-tech-ceo-arrested-for-allegedly-smuggling-300-million-in-restricted-ai-chips-into-china/">Exclusive | FBI arrests California tech CEO for smuggling ...</a></li>
<li><a href="https://cybersecuritynews.com/u-s-arrests-tech-company-owner/">U.S. Arrests Tech Company Owner for Allegedly Smuggling $300 ...</a></li>
<li><a href="https://techresearchonline.com/news/nvidia-h100-ai-chip-smuggling/">Nvidia H100 AI Chip Smuggling: DOJ Charges Two Chinese</a></li>
<li><a href="https://www.ec-compliance.com/en/china-linked-ai-chip-smuggling-network-key-export-control-red-flags/">AI Chip Export Control Violations: Red Flags from a China ...</a></li>
<li><a href="https://www.cnbc.com/2025/12/31/160-million-export-controlled-nvidia-gpus-allegedly-smuggled-to-china.html">$160 million export-controlled Nvidia GPUs allegedly ... - CNBC</a></li>

</ul>
</details>

**标签**: `#AI hardware`, `#export controls`, `#Nvidia`, `#tech policy`, `#supply chain`

---

<a id="item-tech-news-5"></a>
### [Meta 开源 Muse AI 智能体代码，支持 DIY 硬件设备](https://www.theverge.com/tech/1004330/meta-muse-ai-gadgets-home-link) ⭐️ 7.0/10

Meta 开源了用于其 Muse AI 智能体的代码，使开发者能够构建自定义 AI 硬件设备。公司建议的项目包括将 Muse 加载到彩色电子墨水显示屏上以显示提醒，或将其集成到 HDMI 棒上以在大屏幕上展示 Muse 内容。此次发布为开发者和硬件爱好者提供了基于 Muse AI 智能体的 DIY 工具集，是 Meta 在 AI 与开源硬件交叉领域的一次动作，有望降低构建定制 AI 智能设备的技术门槛。

rss · The Verge · 10月2日 21:08

**「背景信息」** Muse 是 Meta 推出的个人 AI 智能体，能够代替用户执行预订出行、填写表格和在线购物等任务，已拥有一定的用户基础。此次 Meta 开源的是 Muse Gadgets 项目的固件与设备 SDK，允许开发者将 Muse 接入自定义硬件，例如彩色电子墨水屏、HDMI 电视棒或带有按键与传感器的设备。这一举措延续了科技公司通过开放生态扩展 AI 平台覆盖范围的思路，即不自行制造所有形态的硬件，而是借助社区开发力量丰富产品形态。

**「影响」** 开发者可以直接基于 Meta 开源的代码将 Muse AI 代理部署到自制硬件上，例如彩色电子墨水提醒屏或 HDMI 显示棒，从而无需等待 Meta 推出官方硬件即可拓展 Muse 的设备形态和应用场景。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.unite.ai/meta-open-sources-muse-gadget-sdks-for-diy-ai-hardware-devices/">Meta Open-Sources Muse Gadget SDKs for DIY AI Hardware ...</a></li>
<li><a href="https://tech.yahoo.com/ai/meta-ai/articles/meta-wants-build-own-muse-004539910.html">Meta wants your next gadget to be Muse-infused</a></li>
<li><a href="https://vff.ai/article/2026/10/02/meta-open-sources-code-to-let-you-make-muse-ai-gadgets">Meta Open Sources Muse AI Agent for Custom Hardware</a></li>
<li><a href="https://eu.36kr.com/en/p/4009352273236101">Meta Open-Sources Muse Gadgets: Empower Global Developers to ...</a></li>
<li><a href="https://vff.ai/article/2026/10/02/meta-open-sources-code-to-let-you-make-muse-ai-gadgets">Meta Open Sources Muse AI Agent for Custom Hardware</a></li>

</ul>
</details>

**标签**: `#AI`, `#open source`, `#hardware`, `#Meta`, `#edge AI`

---

<a id="item-tech-news-6"></a>
### [Epic 暂停产品开发数周以修复危及患者数据的安全漏洞](https://techcrunch.com/2026/10/02/medical-records-giant-epic-pauses-product-development-to-fix-security-bugs-that-risk-patients-data/) ⭐️ 7.0/10

美国医疗科技软件巨头 Epic Systems 宣布将暂停产品开发数周，集中精力修复可能危及患者医疗数据的安全漏洞。此次安全整改涉及广泛使用的 MyChart 患者门户系统，该系统被大量医院用于患者访问个人医疗记录。Epic 作为医疗 IT 领域的主导厂商，此次罕见的全面停摆反映出漏洞的严重性已不容忽视。由于公开披露有限，目前尚不清楚所涉漏洞的性质、严重程度、受影响范围或修复时间表的更多细节，公司也未公开漏洞被实际利用或遭主动披露的具体证据。

rss · TechCrunch · 10月2日 13:23

**「背景」** Epic 是美国最大的电子健康记录供应商之一，旗下 MyChart 是面向数百万患者的在线门户，提供查询检查结果、预约挂号和与医生沟通等功能。近期，安全研究开始利用 AI 模型（如 Anthropic 推出的 Mythos）自动检测医疗软件中的漏洞，Epic 此次暂停产品开发并启动约六周的安全冲刺，正是为了修复此类 AI 所发现的&quot;静默访问&quot;类安全缺陷。

**「影响」** 对于使用 Epic/MyChart 的医院、医疗系统及其患者而言，这意味着所依赖的患者数据访问系统在短期内可能延迟获得新功能更新，同时安全修补成为当前最高优先事项；目前缺乏公开漏洞细节使受影响方难以独立评估实际风险敞口。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://asumetech.com/2026/10/02/why-epic-systems-paused-development-to-address-mychart-security-vulnerabilities/">Why Epic Systems Paused Development to Address MyChart ...</a></li>
<li><a href="https://techcrunch.com/2026/10/02/medical-records-giant-epic-pauses-product-development-to-fix-security-bugs-that-risk-patients-data/">Medical records giant Epic pauses product development to fix...</a></li>

</ul>
</details>

**标签**: `#Healthcare IT`, `#Security`, `#Data Privacy`, `#Software Engineering`, `#Vulnerability Management`

---

<a id="item-tech-news-7"></a>
### [arXiv 实施每月两篇投稿上限 应对 AI 生成低质论文](https://www.theregister.com/ai-and-ml/2026/10/02/arxiv-imposes-rate-limit-on-paper-submissions-to-stem-the-ai-slop-tide/5300899) ⭐️ 7.0/10

全球最大预印本平台 arXiv 自 10 月 1 日起实施新规,每位提交者每个自然月最多提交 2 篇论文,覆盖计算机、数学、物理等全部学科,且被拒稿件同样占用当月额度;多作者论文只计算实际提交者,其余合著者不受影响。arXiv 此举意在遏制 AI 生成低质量论文的泛滥,9 月投稿量达到 40363 篇,创下 35 年新高,其中 AI 分类论文在过去两年内增长超过 6 倍,大量低质量内容已严重挤占平台的人工审核资源。这一限投政策对科研人员的工作流产生直接影响,研究者需要在投稿节奏上进行更严格的规划,而 arXiv 也成为首个因 AI 生成内容问题而对提交频率设置硬性上限的主流学术平台。

rss · The Register · 10月2日 18:02

**「背景说明」** arXiv 是由康奈尔大学运营的开放预印本平台，覆盖物理、计算机、数学等领域，长期采用志愿审核者（volunteer moderators）对投稿进行分类筛选，是 AI/ML 研究传播的基础渠道。该平台在 2026 年 5 月已发布新规，对未披露使用 AI 生成内容的作者实施为期一年的封禁，此次限投是后续措施。由于审核依赖志愿者人工精力，近期投稿量激增——9 月单月达 40363 篇，创 35 年新高，其中 AI 类目两年内增长逾 6 倍，使志愿审核体系不堪重负，直接促成本次限速政策出台。

**「影响」** 对每位提交者而言，从 2026 年 10 月 1 日起每个自然月最多只能提交 2 篇论文，被拒稿件同样计入当月额度，且存在 3 篇的活跃在投上限，因此高产作者或依赖 AI 批量生成稿件的个人提交者最直接受到约束。由于该限额按提交者而非论文计数，多作者合作论文只占用实际提交者的额度，因此大型机构的多人团队基本不受影响。这一新规也可能促使被拒后转投其他预印本或期刊的流量发生迁移，但具体分流去向目前尚无公开数据可佐证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.arxiv.org/2026/10/01/updated-rate-limit-policy/">arXiv has updated its rate limit policy for all submitters.</a></li>
<li><a href="https://startupfortune.com/arxiv-now-limits-every-researcher-to-two-paper-submissions-a-month/">arXiv now limits every researcher to two paper submissions a ...</a></li>
<li><a href="https://blog.arxiv.org/2026/10/01/updated-rate-limit-policy/">arXiv has updated its rate limit policy for all submitters.</a></li>
<li><a href="https://www.theregister.com/ai-and-ml/2026/10/02/arxiv-imposes-rate-limit-on-paper-submissions-to-stem-the-ai-slop-tide/5300899">ArXiv imposes rate limit on paper submissions to stem the AI ...</a></li>
<li><a href="https://startupfortune.com/arxiv-now-limits-every-researcher-to-two-paper-submissions-a-month/">arXiv now limits every researcher to two paper submissions a ...</a></li>

</ul>
</details>

**标签**: `#AI`, `#scientific publishing`, `#arXiv`, `#research integrity`, `#policy`

---

<a id="item-tech-news-8"></a>
### [Don’t be fooled—LLMs don’t reason](https://www.technologyreview.com/2026/10/02/1145639/dont-be-fooled-llms-dont-reason/) ⭐️ 7.0/10

An MIT Technology Review opinion piece by AlphaGo co-creator Thore Graepel arguing that LLMs lack the genuine reasoning machinery that powered AlphaGo&\#x27;s landmark victory.

rss · MIT Technology Review · 10月2日 08:00

**标签**: `#AI`, `#LLMs`, `#reasoning`, `#AlphaGo`, `#deep learning`

---

<a id="item-tech-news-9"></a>
### [OpenAI 发布 GPT-6 模型家族实用指南](https://openai.com/index/practical-guide-building-gpt-6) ⭐️ 7.0/10

OpenAI 发布了一份面向开发者与初创公司的 GPT-6 模型家族实用指南，帮助用户在模型选型、推理强度调优、提示工程、技能组合以及工具协作等环节做出更合适的决策。该指南强调生产环境工作流的设计，涵盖从推理努力程度（reasoning effort）调节到工具协同与提示改进的具体实践。指南内容面向初创企业群体，定位偏实战参考而非深度技术规范，因此对个人开发者与大型企业团队的直接适用性需要结合自身场景评估。由于目前可获取的仅为概述性摘要，更具体的模型版本、定价、上下文窗口、性能基准及兼容性限制等关键细节需以 OpenAI 原始文档为准。

rss · OpenAI News · 10月2日 16:15

**「背景」** OpenAI 的 GPT-6 是一个由多个变体组成的模型系列，开发者可以在 gpt-6-astra、gpt-6.1-sol 和 gpt-6-luna 等不同型号之间按需选择，以匹配任务复杂度、成本和延迟要求。与早期只发布单一旗舰模型不同，GPT-6 引入了&quot;推理强度&quot;（reasoning effort）这一可调参数，允许在同一个模型上平衡响应速度与思考深度，从而使应用方能够根据细粒度编辑、多应用上下文检索或受限问题求解等场景精细调配算力。该指南由 OpenAI 直接发布，面向初创团队梳理选型、推理调优、提示与技能编排、工具协同以及生产化部署等关键决策。

**「影响」** 对于正在评估或已采用 GPT-6 系列的开发者与初创团队，该指南可作为模型选型、推理参数调节和生产工作流设计的官方参考起点，但其中的具体技术细节仍需查阅完整文档核实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/practical-guide-building-gpt-6/">A model guide for the GPT‑6 family - OpenAI</a></li>
<li><a href="https://developers.openai.com/api/docs/guides/latest-model">Using GPT-6 | OpenAI API</a></li>
<li><a href="https://developers.openai.com/api/docs/guides/model-selection">Model selection - OpenAI API</a></li>

</ul>
</details>

**标签**: `#AI`, `#LLM`, `#OpenAI`, `#developer-tools`, `#prompt-engineering`

---

<a id="item-tech-news-10"></a>
### [Google Research 公布 Cogentic：多智能体协调数学证明探索](https://arxiv.org/abs/2609.40324v1) ⭐️ 7.0/10

Google Research 公布 Cogentic，这是一套以 Gemini 为基础模型的多智能体架构，通过&quot;证明—验证&quot;循环让多个独立证明器并行探索不同证明方向，并由专门组件进行对抗式验证，已确认的结果存入可持续复用的验证账本。该系统在在线学习、拍卖理论和机制设计三个领域的 5 个开放问题上产出了新结论，配套论文称这些结果均由相应领域的专家独立验证。需指出的是，所引用的 arXiv 编号（2609.40324v1）对应 2026 年 9 月的预印本时间，原始信息来自 Telegram 聚合渠道而非 Google 官方发布，因此具体声明的真实性与发表状态仍待进一步核实。

telegram · zaihuapd · 10月2日 12:04

**「背景」** 近年来，研究者开始将多智能体（multi-agent）架构引入自动定理证明领域，将非正式推理大模型、形式化证明器（如 Lean）以及专门的验证组件组合成协同工作流，以应对单一模型难以处理的复杂开放问题。Cogentic 采用的“证明—验证循环”范式将证明搜索分解为多轮迭代：独立证明器并行探索不同方向，专门验证器对草稿进行对抗式挑战，已确认的引理被写入可持续复用的“验证账本”，供后续证明调用。这一思路与 Prover Agent、Ax-Prover 等近期工作同属“LLM + 形式化助手 + 反馈回路”的多代理方向，但 Cogentic 将其拓展到在线学习、拍卖理论和机制设计等经济理论领域的开放数学问题，而非依赖已有形式化基准。

**「影响」** 若论文与编号属实，多智能体&quot;证明—验证&quot;循环结合对抗式验证与持久账本的设计，为 AI 辅助数学发现提供了一种可复用的工作流模板，尤其可能影响经济理论与算法博弈论领域的研究进程。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2609.40324">[2609.40324] Cogentic: Multi-Agent Orchestration for ...</a></li>
<li><a href="https://cyberarctica.com/research/49_automated_theorem_proving.html">Multi-Agent Systems for Automated Theorem Proving</a></li>
<li><a href="https://arxiv.org/abs/2506.19923">[2506.19923] Prover Agent: An Agent-Based Framework for ... Next-Gen Theorem Proving: A Multi-Agent Paradigm for ... Ax-Prover: A Deep Reasoning Agentic Framework for Theorem ... Collaborative Theorem Proving with Large Language Models ... Benchmarking Automated Theorem Proving with Large Language ... Prover Agent: An Agent-based Framework for Formal ...</a></li>

</ul>
</details>

**标签**: `#AI research`, `#multi-agent systems`, `#automated theorem proving`, `#LLMs`, `#Google DeepMind`

---

<a id="item-tech-news-11"></a>
### [Claude Code 新增 mods 自定义扩展机制](https://claude.com/blog/claude-code-mods) ⭐️ 7.0/10

Anthropic 为 Claude Code 推出基于 TypeScript 的 mods 自定义功能，开发者可通过少量 TypeScript 代码改写提示词、新增界面元素或替换内置功能。Mods 以插件形式分发，现已同时支持 CLI 和桌面版。由于 mods 共享 Claude Code 的全部权限且不设沙箱，官方明确提醒用户仅从可信来源安装，并允许让 Claude 自行编写 mods。Anthropic 表示目前已有部分内置功能迁移为 mods，后续计划将更多内置功能转换为 mods。DeepSeek Harness 团队负责人崔添翼在 X 上发文祝贺并指出该设计与 DeepSeek Harness “一切皆插件”理念的相似之处。

telegram · zaihuapd · 10月2日 12:32

**「背景」** Claude Code 是 Anthropic 推出的 AI 编程助手，提供命令行与桌面两种使用形态。Mods 是一种由 TypeScript 编写的轻量扩展单元，开发者通过它可以在不改动主程序的情况下定制提示词、界面与功能，整体思路与传统软件的插件或扩展机制类似。

**「影响」** Claude Code 用户与插件开发者获得了官方支持的深度定制能力，但同时也需承担 mods 以无沙箱、全权限方式运行所带来的安全风险，仅应安装来自可信来源的插件。

**标签**: `#Claude Code`, `#developer tools`, `#plugin architecture`, `#AI coding assistants`, `#Anthropic`

---

<a id="item-tech-news-12"></a>
### [亚马逊十亿美元社区投入难消数据中心反对声](https://arstechnica.com/tech-policy/2026/10/amazons-1b-plan-to-combat-data-center-backlash-draws-more-backlash/) ⭐️ 6.0/10

亚马逊宣布将在未来五年内向其数据中心周边社区捐赠超过 10 亿美元，资金的具体用途由当地社区自行决定，覆盖教育、职业培训、能源可负担性、水资源与能源保护以及社区重点关切等领域。公司同时承诺其数据中心不会推高当地居民电价或耗尽本地水源，并力争在 2030 年前实现&quot;水正效益&quot;，声称 75%的项目已达成这一目标。AWS 首席执行官 Matt Garman 在发布上述承诺时，呼应美国总统特朗普的表态，警告称要求暂停数据中心的呼声可能受到外国虚假信息活动的煽动，否则美国在 AI 领域可能落后于中国。环保组织 Stand.Earth 反驳称亚马逊&quot;误导&quot;公众并散布&quot;企业宣传&quot;，将上述捐赠定性为对其数据中心建设已造成损害的&quot;挣扎式损害控制&quot;，并指出亚马逊计划支持的一座发电厂可能成为美国最大的气候污染源，但相关数据中心承诺却未提及该电厂。

rss · Ars Technica · 10月2日 20:30

**「背景」** 近年来，随着亚马逊、微软、谷歌等云服务提供商大规模扩建用于 AI 训练与推理的数据中心，美国多个州和地方社区对电力与水资源压力、噪音污染以及碳排放的反对情绪持续上升，已导致数十亿美元的数据中心项目被搁置或推迟。这一背景下，亚马逊此次的十亿美元承诺是云厂商迄今为缓解社区反对而作出的最大规模资金方案之一。

**「影响」** 这一承诺短期内为亚马逊的数据中心扩建争取了政治空间，但 Stand.Earth 等环保组织的公开反驳显示，企业宣传、社区实际诉求与未公开的电厂计划之间的分歧将持续成为数据中心扩张的主要争议焦点。

**标签**: `#data-centers`, `#AI-infrastructure`, `#cloud-computing`, `#tech-policy`, `#amazon-aws`

---

<a id="item-tech-news-13"></a>
### [AllenAI 开源 AstaBrief 8B：面向科研报告的快速生成模型](https://huggingface.co/blog/allenai/astabrief) ⭐️ 6.0/10

AllenAI 开源了 AstaBrief 8B，这是一款专为科研报告生成优化的小型语言模型，已在其 Asta 科学工作平台中以 Fast 模式上线，与基于 Claude 的 Thinking 模式并列提供。该模型基于 Qwen3-8B 训练，采用监督微调（SFT）与直接偏好优化（DPO）的组合路线，并使用了重新设计的报告生成流程，将整篇报告一次性生成，而不是按章节依次撰写。在完整 Asta 流水线中，Fast 模式平均每份报告耗时 51.1 秒，相比 Thinking 模式的 178.5 秒提速约 3.5 倍。训练数据来自真实的 ScholarQA 用户查询（90,000 条科研导向查询），经质量过滤后得到 47,000 条可用样本，目标输出由 Claude 3.5 Sonnet、Claude 3.7 Sonnet、o3、o4-mini 与 GPT-4.1 混合生成。AstaBrief 的权重、训练数据，以及一个可用于本地 PDF 报告生成的示例工作流一并发布，方便机构在本地基础设施上运行。文中说明，文中描述的大部分训练和评估工作在 2025 年完成，相关基准结果反映的是当时的模型前沿水平，并未针对当前最新前沿模型重新评测。

rss · Hugging Face Blog · 10月2日 15:19

**「背景」** Asta 是 AllenAI 推出的科学工作平台，其报告生成功能由 ScholarQA 框架驱动，通过检索相关文献并由模型合成带引用的报告。AstaBrief 是 AllenAI 在 NSF OMAI 计划下探索开源、面向科学需求的小型可适配模型的成果，专注于科研场景中对证据可追溯、结论不越界、用户可验证的要求。AstaBrief 通过一次性全报告生成（one pass）来替代 Thinking 模式中的片段摘要与聚类等耗时步骤。

**「影响」** AstaBrief 让研究者能够在 Asta 平台内以约 3.5 倍的速度获取带引用的科研报告，也可下载后在自有基础设施上部署，从而在处理敏感或未公开的科研问题时避免数据外传。

**标签**: `#open-source`, `#language-models`, `#scientific-research`, `#AI-tools`, `#NLP`

---

<a id="item-tech-news-14"></a>
### [ServiceNow CoreAI 发布 AutoSynthData：为 企业 Agent 自动合成训练数据](https://huggingface.co/blog/ServiceNow-AI/autosynthdata) ⭐️ 6.0/10

ServiceNow CoreAI 推出了 AutoSynthData，一种针对企业 Agent 能力短板自动生成训练数据的方法。该方法首先让目标模型在诊断任务上运行以发现失败模式，再借助更强的教师模型判断这些任务是否可解、理想行为应是怎样，从而提炼出&quot;能力规范卡&quot;并据此批量生成新任务。生成流程分两个阶段——Target 阶段产出经过验证、执行、求解评估与修复的核心样本，Multiply 阶段基于这些样本扩展出具有新用户请求、环境状态、实体配置和验证器的新变体。文章以 EnterpriseOps Gym 为示例环境，展示了如何将模型失败转化为可执行且具有训练价值的合成任务课程。

rss · Hugging Face Blog · 10月2日 04:01

**标签**: `#ai`, `#machine-learning`, `#synthetic-data`, `#enterprise-agents`, `#training-methodology`

---

<a id="item-tech-news-15"></a>
### [AI 触发的快速反应通知与住院患者死亡率降低相关](https://news.google.com/rss/articles/CBMi5wFBVV95cUxNMUc0NWhSWE1JMWVBRk5SNk5UWDNrNzRpSVZVaXRlb0hYUFNncnFkdm92OGhOX3JGY3RXUGtJdGQxT0Y4d2N3NUV3U0h2WjdfZGV0RGdZYUxEeXVtSnF5RGlMay1EQmtrM2ZENEJSaUhmTVp0T3NFbndtZVBnallGeTRKZEliVjV3WTItdWRKc3VsR0Mxa3JOR2tWSW1LdlF6dm8yWkxVdnpvZWg0WlN4YS1yWUJJeWlZZnhHM1lIY2hLcW1hY21OUlRBSWl0aWthY1JfNkRpazRTZDBjUEhLaU9GU0FyLWM?oc=5) ⭐️ 6.0/10

据 2 Minute Medicine 报道，一项研究摘要指出，由人工智能触发的快速反应通知与住院患者死亡率降低存在关联。该研究探讨了在医院环境中部署 AI 系统，以在患者病情恶化前自动触发快速反应团队通知，结果显示这种 AI 驱动的早期识别方法可能有助于改善住院患者的临床结局。然而，现有摘要未披露 AI 模型的设计架构、部署方式、训练数据、研究方法学、样本规模、统计效应量或具体医院环境等关键细节，因此难以评估该结论的普适性、潜在偏倚及实际临床应用价值。

google\_news · 2 Minute Medicine · 10月3日 01:44

**「背景」** 医院快速反应小组（Rapid Response Team, RRT）是一支由重症或急救专业人员组成的团队，当住院患者出现临床恶化迹象时，由病区护士或医生呼叫，以期在心跳呼吸骤停等严重事件发生前进行早期干预。AI 触发的快速反应通知指的是系统实时分析电子病历中的生命体征、实验室结果等数据，当机器学习模型（例如 Epic 恶化指数 Epic Deterioration Index）判断患者恶化风险超过预设阈值时，自动向 RRT 推送警报，从而缩短从恶化到干预的时间。本次报道涉及的 NEJM AI 研究覆盖 11 家医院站点，评估了这类自动通知在真实临床环境中的部署效果。

**「影响」** 对正在评估或部署 AI 临床预警系统的医院和医疗信息化团队而言，该研究表明自动化快速反应触发机制可能带来住院死亡率方面的获益，不过由于摘要缺少方法学细节，尚需查阅全文以指导具体实施。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ai.nejm.org/doi/full/10.1056/AIoa2500973">Implementation of an AI-Triggered Rapid Response ...</a></li>
<li><a href="https://www.europesays.com/ai/193853/">Artificial intelligence (AI)-triggered rapid response ...</a></li>
<li><a href="https://www.archyde.com/ai-triggered-rapid-response-alerts-associated-with-lower-inpatient-mortality/">AI-Triggered Rapid Response Alerts Associated with Lower ...</a></li>

</ul>
</details>

**标签**: `#AI/ML`, `#Healthcare`, `#Applied AI`, `#Clinical Decision Support`, `#Research`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [美联储 10 月加息概率骤降，12 月加息预期仍存](https://www.cnbc.com/2026/10/02/fed-rate-hike-odds-decline-after-september-jobs-report.html) ⭐️ 7.0/10

...

rss · CNBC Finance · 10月2日 13:29

**「背景」** ...

**标签**: `#monetary-policy`, `#employment-data`, `#inflation`, `#rate-expectations`, `#Federal-Reserve`

---

<a id="item-finance-news-2"></a>
### [Bitget 交易所遭近 3.88 亿美元黑客攻击，CEO 称预计难以追回大部分资金](https://www.cnbc.com/2026/10/02/bitget-crypto-stolen-hack-recovery.html) ⭐️ 7.0/10

加密货币交易所 Bitget 在上周遭网络攻击，被盗资金约 3.88 亿美元，目前仅冻结约 110 万美元。CEO Gracy Chen 接受 CNBC 采访时表示，鉴于以往交易所被盗案例的追回情况，预计难以追回大部分资金，但用户账户余额未受影响。Bitget 保护基金在事件前超 4.64 亿美元，事件后被消耗至不足 2 亿美元，目前已用自有资金补充回逾 3 亿美元，最新储备率自报为 131%。Mandiant 与 SlowMist 于 9 月 30 日发布的调查报告显示，攻击者通过利用第三方安全产品中的零日漏洞（最早可追溯至 8 月 31 日）获取内部特权访问，进而绕过正常提款流程，目前尚未将攻击归因于朝鲜。比特币、以太坊和 USDT 的提款已恢复，其余加密货币及法币与点对点服务计划于本周五恢复。

rss · CNBC Finance · 10月2日 06:03

**标签**: `#cryptocurrency`, `#cybersecurity`, `#exchange-hack`, `#digital-assets`, `#exchange-security`

---