---
layout: default
title: "Horizon Summary: 2026-10-09 (ZH)"
date: 2026-10-09
lang: zh
---

> 从 137 条内容中筛选出 14 条重要资讯。

---

**科技新闻**
1. [OpenAI withdraws three mathematical results](#item-tech-news-1) ⭐️ 7.0/10
2. [Let&\#x27;s Encrypt 将证书有效期从 90 天缩短至 64 天，2027 年 2 月生效](#item-tech-news-2) ⭐️ 7.0/10
3. [亚马逊放弃 Fire 品牌，Alexa 平板全面转向谷歌认证 Android](#item-tech-news-3) ⭐️ 7.0/10
4. [亚马逊造出第 1000 颗卫星，年底前推出太空互联网服务](#item-tech-news-4) ⭐️ 7.0/10
5. [英伟达加码物理 AI 安全系统，从自动驾驶拓展至人形机器人](#item-tech-news-5) ⭐️ 7.0/10
6. [Anthropic 推出免费 OSS Scanner 为开源项目提供 AI 安全扫描](#item-tech-news-6) ⭐️ 7.0/10
7. [被解雇的 OpenAI 安全研究人员公开反驳不当行为指控并警告寒蝉效应](#item-tech-news-7) ⭐️ 7.0/10
8. [Google 将智能体 AI 引入 Gemini，先从企业市场起步](#item-tech-news-8) ⭐️ 7.0/10
9. [Anthropic 宣布加强关键基础设施与开源项目防御，应对 AI 驱动的攻击](#item-tech-news-9) ⭐️ 7.0/10
10. [英伟达 dreamDojo 论文被指代码多处错误，仍获 ICML spotlight](#item-tech-news-10) ⭐️ 7.0/10
11. [ThinkingBox: Solving an agent task once vs. solving it 20/20: 507 stateful workflows graded on terminal database state \[R\]](#item-tech-news-11) ⭐️ 7.0/10
12. [北京不会放慢前沿步伐：中国速度优先的 AI 安全监管体系](#item-tech-news-12) ⭐️ 6.0/10

**财经新闻**
1. [标普：中国房地产长期低迷或接近尾声](#item-finance-news-1) ⭐️ 7.0/10
2. [华为加码智能手机,电动车交付 9 月同比下滑 29%](#item-finance-news-2) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [OpenAI withdraws three mathematical results](https://twitter.com/danintheory/status/2108065033070789090) ⭐️ 7.0/10

OpenAI withdrew three mathematical results from its AI-generated proofs repository, prompting expert discussion about the reliability and verification of LLM-produced mathematical claims.

hackernews · sashank\_1509 · 10月8日 07:05 · [社区讨论](https://news.ycombinator.com/item?id=50002650)

**标签**: `#AI`, `#formal-verification`, `#LLM-limitations`, `#mathematics`, `#scientific-integrity`

---

<a id="item-tech-news-2"></a>
### [Let&\#x27;s Encrypt 将证书有效期从 90 天缩短至 64 天，2027 年 2 月生效](https://arstechnica.com/gadgets/2026/10/lets-encrypt-cuts-certificate-lifetimes-to-64-days-starting-february-2027/) ⭐️ 7.0/10

Let&\#x27;s Encrypt 宣布将自 2027 年 2 月 10 日起，把免费 SSL/TLS 证书的有效期从 90 天缩短至 64 天，并将于 2026 年 10 月 14 日先行开放测试供用户提前验证流程。缩短证书有效期的核心动因在于压缩私钥失窃或误颁后的暴露窗口，同时推动用户从按固定偏移（如到期前 60 天）触发续期的脚本，迁移至支持 ACME Renewal Information（ARI）的全自动化 ACME 客户端；已使用支持 ARI 的现代客户端的环境可无缝切换，仍依赖硬编码计划或手动流程的部署则需在 2027 年 2 月之前完成升级，否则将面临证书意外过期。文章同时透露 45 天默认值计划在 2028 年跟进，并指出缩短证书寿命已成整个行业（连同 DigiCert 等其他 CA）共同的方向。

rss · Ars Technica · 10月8日 19:57

**「背景」** Let&\#x27;s Encrypt 是一个免费的证书颁发机构（CA），自 2016 年初推出以来一直提供默认 90 天有效期的 SSL/TLS 证书，旨在强制推动证书续期自动化，从而缩短私钥泄露后的暴露窗口。ACME（Automatic Certificate Management Environment）协议负责自动化证书申请与续期，而其扩展 ARI（ACME Renewal Information）则允许 CA 主动通知客户端何时应该续期，取代依赖固定偏移量的脚本化更新方式。此次降至 64 天的决定也是为了与浏览器即将收紧的 CA 签发证书最长有效期要求保持一致，并将在 2028 年进一步缩短至 45 天。

**「实际影响」** 使用支持 ARI（ACME Renewal Information）协议的现代 ACME 客户端的管理员将无需手动调整即可自动续期；但仍依赖固定偏移脚本（例如“到期前 60 天触发续期”）或手动流程的运维人员，必须在 2027 年 2 月 10 日之前升级，否则从该日起签发的 64 天证书将按预期提前到期，可能导致网站和服务出现意外的 HTTPS 中断。

**「社区讨论」** 来源内容附带的评论者观点认为，Let&\#x27;s Encrypt 实际将进一步下调至 47 天，因为浏览器即将限制 CA 所颁发证书的最大有效期；该说法与原文标题及正文给出的 64 天存在出入，目前尚无原文之外的权威证实，仅可作参考性意见看待。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arstechnica.com/gadgets/2026/10/lets-encrypt-cuts-certificate-lifetimes-to-64-days-starting-february-2027/">Let &#x27; s Encrypt cuts certificate lifetimes to 64 days ... - Ars Technica</a></li>
<li><a href="https://letsencrypt.org/2026/10/07/64-day-certs">64 - Day Certificate Lifetimes Coming Feb 2027 - Let &#x27; s Encrypt</a></li>
<li><a href="https://www.geekslop.com/technology-articles/computers-programming/hacking-and-security-technology-articles/2026/lets-encrypt-64-day-ssl-certs">Let &#x27; s Encrypt Cuts SSL Cert Lifetimes To 64 Days ... - Geek Slop</a></li>
<li><a href="https://aideworks.com/blog/ssl-47-day-certificates-what-agencies-need-to-know">SSL certificates are about to expire 8× faster — what... — Aideworks</a></li>
<li><a href="https://www.digicert.com/blog/tls-certificate-lifetimes-will-officially-reduce-to-47-days">TLS Certificate Lifetimes Will Officially Reduce to 47 Days | DigiCert</a></li>

</ul>
</details>

**标签**: `#TLS/SSL`, `#certificates`, `#security`, `#infrastructure`, `#DevOps`

---

<a id="item-tech-news-3"></a>
### [亚马逊放弃 Fire 品牌，Alexa 平板全面转向谷歌认证 Android](https://arstechnica.com/gadgets/2026/10/amazons-new-alexa-tablets-drop-the-fire-branding-but-are-more-android-than-ever/) ⭐️ 7.0/10

亚马逊取消沿用约 15 年的 Fire 平板品牌，发布三款全新的&quot;Alexa 平板&quot;，并首次采用谷歌认证的 Android 系统，集成 Google Play 商店与完整谷歌服务生态，这一变化发生在亚马逊去年关闭其 Appstore 应用商店之后。基础款 Alexa 平板 8 起售价 230 美元、平板 11 起售价 330 美元，均搭载联发科 8189 处理器和 16:10 比例屏幕；旗舰款 Alexa 平板 12 Pro 起售价 500 美元，采用更利于多任务分屏的 3:2 比例屏幕，分辨率达 2800×1840、刷新率 120Hz、峰值亮度 500 尼特，搭载联发科 Dimensity 8400 处理器、8GB 内存与 128GB 存储，并提供加价 50 美元的哑光屏幕、150 美元的键盘以及 90 美元的触控笔配件。

rss · Ars Technica · 10月8日 16:32

**「背景」** Fire 平板自约 2011 年面市以来一直运行亚马逊定制的&quot;Fire OS&quot;系统，该系统基于 Android 但剥离了谷歌服务和 Play Store，仅通过亚马逊自营的 Appstore 分发应用，长期被视为低价但生态受限的消费级平板设备。亚马逊去年彻底关停 Appstore，失去了 Fire OS 赖以运行的应用分发渠道，从而推动了本次向完整谷歌 Android 的战略转型，而三款新机也均由塑料/金属混合机身改为一体化铝合金机身。

**「影响」** 对于原 Fire 平板用户，新设备可直接访问 Play Store 与全部谷歌应用，缓解了 Appstore 关停带来的应用来源缺失问题；但与此同时，亚马逊硬件策略出现明显分化——平板产品线回归标准 Android，而 Fire Stick 流媒体设备正迁移到自研的 Linux 内核的 Vega OS。

**标签**: `#hardware`, `#android`, `#amazon`, `#consumer-electronics`, `#ecosystem-strategy`

---

<a id="item-tech-news-4"></a>
### [亚马逊造出第 1000 颗卫星，年底前推出太空互联网服务](https://arstechnica.com/space/2026/10/amazon-builds-1000th-satellite-is-weeks-away-from-space-internet-rollout/) ⭐️ 7.0/10

亚马逊位于华盛顿州柯克兰的工厂已制造出第 1000 颗卫星，产能达每天数颗，使其成为仅次于 SpaceX 的全球第二大卫星制造商。该项目现称为 Amazon Leo，由曾在 Starlink 早期负责项目、八年前被马斯克解雇的 Rajeev Badyal 领衔，量产由总监 Paul Palcisco 负责，商业事务由副总裁 Chris Weber 牵头。联合发射联盟的火神（Vulcan）火箭即将复飞，首飞即搭载 Amazon Leo 卫星，紧邻的另一枚火神火箭也将在今年晚些时候再发射一批卫星入轨。Amazon Leo 将在未来数周内推出首个商业服务，目标客户涵盖消费者、企业和政府机构，是目前唯一能在全球范围内与 Starlink 抗衡的低轨道宽带系统，因为 OneWeb 仅提供有限服务。

rss · Ars Technica · 10月8日 15:28

**「背景信息」** 低轨道卫星宽带通过部署数百至数千颗近地卫星实现全球互联网覆盖，自五年前 Starlink 推出以来，这一市场由 SpaceX 主导。Rajeev Badyal 曾任 Starlink 早期负责人，但因被马斯克认为推进速度过慢而在大约八年前被解雇，之后加入亚马逊主导其卫星互联网项目。亚马逊自近十年前开始研发这一星座，目标是在低轨道宽带领域挑战 SpaceX 的近乎垄断地位。

**「影响」** 消费者、企业和政府机构将首次获得由 Starlink 以外供应商提供的全球高速卫星互联网选择。但具体覆盖范围、定价、带宽等级仍待 Amazon Leo 正式公布，且火神火箭复飞任务能否按计划执行仍存在不确定性，可能影响首批商用服务的时间表。

**标签**: `#satellite-internet`, `#space-tech`, `#broadband-infrastructure`, `#amazon`, `#leo-constellation`

---

<a id="item-tech-news-5"></a>
### [英伟达加码物理 AI 安全系统，从自动驾驶拓展至人形机器人](https://arstechnica.com/ai/2026/10/nvidias-big-bet-on-physical-ai-aims-for-safer-robotaxis-humanoid-robots/) ⭐️ 7.0/10

英伟达将其 Halos 全栈安全系统从自动驾驶车辆扩展至更广泛的物理 AI 领域，涵盖仓库自主移动机器人、工厂人形机器人以及手术机器人。公司机器人生态与边缘计算负责人 Amit Goel 表示，随着 AI 模型和机器人硬件日趋成熟，安全将成为制约行业发展的下一个关键瓶颈。Halos for Robotics 于 2026 年 6 月发布，硬件层面采用配备独立安全处理器的 IGX Thor 计算模块以并行运行功能系统与安全系统。英伟达 CEO 黄仁勋透露，物理 AI 业务已为公司带来近 100 亿美元的年营收，公司还入股了 Agility Robotics、Figure AI 等人形机器人初创企业，并与宇树科技合作推出开源人形机器人参考设计。

rss · Ars Technica · 10月8日 11:15

**标签**: `#AI safety`, `#robotics`, `#Nvidia`, `#autonomous vehicles`, `#industry strategy`

---

<a id="item-tech-news-6"></a>
### [Anthropic 推出免费 OSS Scanner 为开源项目提供 AI 安全扫描](https://www.theverge.com/ai-artificial-intelligence/1008521/anthropic-open-source-oss-scanner) ⭐️ 7.0/10

Anthropic 推出了一项名为 OSS Scanner 的免费服务，允许符合条件的开源项目自愿接入，使用包括 Claude 在内的最强模型进行周期性安全漏洞扫描。扫描报告由模型自动生成，包含漏洞复现步骤、漏洞说明，以及在可能时给出的补丁建议，但不经过人工审核，因此可能存在错误。Anthropic 披露，在过去半年中该系统已发现超过 2.9 万个候选漏洞，其中约 6000 个经过人工审查；在早期测试覆盖的 97 个高危或严重级别漏洞中，有 85 个符合其披露流程要求。符合条件的开源项目核心维护者可通过提交 GitHub PR 来申请接入该服务。

rss · The Verge · 10月8日 21:53

**「背景信息」** OSS Scanner 是 Anthropic 面向开源生态推出的 AI 驱动安全扫描工具，定位为传统静态分析和人工安全审计的补充。开源项目维护者通常依赖社区报告或安全研究者的披露来发现漏洞，发现速度有限，而大语言模型能够批量阅读代码并定位潜在风险点，但同时也带来误报风险，因此扫描结果需要由人工复核后再决定是否披露与修复。

**「影响」** 符合条件的开源项目核心维护者可免费获得周期性 AI 漏洞扫描，有望更早发现安全问题；但由于扫描报告未经人工审核且可能存在误报，维护者在采纳前需自行验证。

**标签**: `#AI`, `#open-source`, `#security`, `#developer-tools`, `#Anthropic`

---

<a id="item-tech-news-7"></a>
### [被解雇的 OpenAI 安全研究人员公开反驳不当行为指控并警告寒蝉效应](https://techcrunch.com/2026/10/08/fired-openai-safety-researchers-dispute-misconduct-claims-warn-of-chilling-effect/) ⭐️ 7.0/10

三名被解雇的 OpenAI 安全研究人员联合发布公开信，反驳公司对他们不当处理敏感信息的指控。他们在信中警告，这些解雇事件正在 OpenAI 内部产生寒蝉效应，可能使其他研究人员不敢自由表达对 AI 安全问题的担忧。此次公开抗议发生在 AI 安全治理受到日益关注的背景下，涉及一家前沿 AI 实验室内部的安全研究文化与问责机制之间的张力。此事件凸显了商业化 AI 公司在安全研究方面面临的内部压力，也对 OpenAI 在 AI 安全领域的公开承诺提出了新的质疑。

rss · TechCrunch · 10月8日 20:04

**「背景」** OpenAI 作为前沿 AI 开发机构，其内部安全团队负责评估模型风险并就部署决策向管理层提供意见，而第三方安全审计和模型可监控性（model monitorability），即对模型行为进行持续独立监测的能力，是 AI 治理中用于外部制衡的关键机制。此次公开发声的三位被解雇研究员（Jasmine Wang、Tomek Korbak、Mikita Balesni）正是在公开信中要求 OpenAI 兑现嵌入第三方审计师和保护模型可监控性的承诺，反映了公司内部围绕治理透明度与商业化压力之间长期存在的争论。

**「影响」** 对于在 AI 公司从事安全研究的工作人员而言，这一事件可能加剧内部就安全问题自由表达的顾虑，并削弱公众和研究者群体对前沿实验室安全承诺的信任。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://chang.aevumnews.com/en/openai-ex-safety-researchers-challenge-misconduct-claims-allege-chilling-effect">OpenAI Ex- Safety Researchers Challenge Misconduct Claims ...</a></li>
<li><a href="https://fourweekmba.com/ai-fired-openai-safety-researchers-deny-leak-in-open-letter/">Fired OpenAI Safety Researchers Deny Leak in Open Letter</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#OpenAI`, `#AI governance`, `#industry news`, `#workplace culture`

---

<a id="item-tech-news-8"></a>
### [Google 将智能体 AI 引入 Gemini，先从企业市场起步](https://techcrunch.com/2026/10/08/google-brings-agentic-ai-to-gemini-starting-with-businesses/) ⭐️ 7.0/10

Google 正在将 Gemini 打造为一款能够规划任务、执行任务并跨企业应用和系统协同工作的 AI 智能体。该智能体可以将工作委派给子智能体，调用多种 AI 模型，还拥有专属的工作身份，包括一个电子邮件地址。这一举措标志着 Gemini 正式向企业级智能体平台演进。

rss · TechCrunch · 10月8日 18:18

**标签**: `#agentic AI`, `#Google Gemini`, `#enterprise AI`, `#AI agents`, `#multi-agent systems`

---

<a id="item-tech-news-9"></a>
### [Anthropic 宣布加强关键基础设施与开源项目防御，应对 AI 驱动的攻击](https://www.theregister.com/ai-and-ml/2026/10/09/ai-company-moves-to-defend-critical-infrastructure-and-open-source-projects-from-ai/5302128) ⭐️ 7.0/10

AI 公司 Anthropic 宣布将采取措施，防御针对关键基础设施和开源项目的 AI 驱动攻击。根据该公司的判断，在接下来两年内，攻击者将在攻防对抗中占据优势地位。这一表态意味着 Anthropic 正主动介入 AI 安全领域，针对日益严重的 AI 武器化威胁建立防御机制，覆盖关键基础设施与开源生态两大方向。由于现有公开细节较为有限，具体的防御技术细节、合作对象与项目范围尚待进一步披露。

rss · The Register · 10月8日 23:57

**「背景」** Anthropic 是一家总部位于美国旧金山的 AI 公益公司，旗下 Claude 系列大语言模型是其旗舰产品，公司专注于 AI 安全研究。关键基础设施（如电力、供水系统）和开源软件项目长期是网络攻击的重点目标，AI 技术使攻击者能够更快发现和利用软件漏洞，传统的防御手段面临更大挑战。在此背景下，Anthropic 启动了网络使命计划，通过 Claude 等前沿模型协助发现和修复漏洞，并推出免费的开源软件漏洞扫描服务 OSS Scanner，以缩小攻防差距。

**「影响」** 运营电力网络、供水系统和交通等关键基础设施的企业将能够通过 Anthropic 的关键基础设施防御计划获得其前沿 AI 模型和工程师资源，用于应对 AI 驱动的攻击，但 Anthropic 自身预计在未来两年内攻击方仍将占据优势，因此该计划的实际防御效果在此窗口内存在不确定性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Anthropic">Anthropic - Wikipedia</a></li>
<li><a href="https://www.anthropic.com/news/anthropic-cyber-mission">Introducing the Anthropic Cyber Mission \ Anthropic</a></li>
<li><a href="https://www.axios.com/2026/10/08/anthropic-critical-infrastructure-cybersecurity">Anthropic launches AI push to protect critical infrastructure</a></li>
<li><a href="https://www.axios.com/2026/10/08/anthropic-critical-infrastructure-cybersecurity">Anthropic launches AI push to protect critical infrastructure</a></li>
<li><a href="https://www.anthropic.com/news/anthropic-cyber-mission">Introducing the Anthropic Cyber Mission \ Anthropic</a></li>

</ul>
</details>

**标签**: `#AI Security`, `#Critical Infrastructure`, `#Open Source`, `#Cybersecurity`, `#Anthropic`

---

<a id="item-tech-news-10"></a>
### [英伟达 dreamDojo 论文被指代码多处错误，仍获 ICML spotlight](https://www.reddit.com/r/MachineLearning/comments/1x0i6b5/nvidias_erroneous_paper_accepted_as_icmls/) ⭐️ 7.0/10

Nvidia 的 dreamDojo 论文被 ICML 接受为 spotlight，但其代码被指存在重大错误。该研究基于其前期工作 Cosmos 2.5 构建机器人世界模型，使用约 44,000 小时人类数据进行预训练，并借助 256 张 H100 GPU 完成训练，但论文 Table 4 显示相对 Cosmos 2.5 仅取得约 0.5 dB PSNR 的微弱提升。一位尝试复现该工作的研究者与同事（在 Claude 辅助下）发现其后训练代码存在一处 bug，GitHub Issues 中还报告了另外两处影响整个预训练流程的错误。结合这些漏洞，作者质疑&quot;投入海量数据和算力却几乎没有任何实质改进&quot;的结果更可能是由代码缺陷导致，而非真正的边际改进。该事件引发了对顶会 ML 同行评审严谨性，以及&quot;基础模型&quot;宣传与实际增量改进之间差距的讨论。

reddit · r/MachineLearning · /u/Amazing-Fox-7295 · 10月8日 04:58

**「背景」** 世界模型（World Model）是机器人学中用于模拟和预测环境动态的 AI 模型，常被用于生成训练数据或评估机器人策略。ICML 是机器学习领域的顶级会议，论文接收后会被分为 Oral、Spotlight 和 Poster 等类别，其中 Spotlight 通常授予约 5%–10% 的接收论文以表彰其影响力。DreamDojo 是 Nvidia 基于其 Cosmos 2.5 世界模型开发的通用机器人世界模型，通过在约 44,000 小时的人类第一人称视频上进行预训练以学习物理知识，再针对具体机器人本体进行后训练。

**「影响」** 若论文中影响预训练、后训练与评估的代码 bug 属实，则 dreamDojo 报告的所有性能数据都可能不可信，并对 ICML 等顶会同行评审在大模型时代下能否有效核查资源密集型工作的代码正确性提出警示。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/NVIDIA/DreamDojo">GitHub - NVIDIA / DreamDojo : Official Codebase for &quot; DreamDojo ...&quot;</a></li>
<li><a href="https://huggingface.co/nvidia/DreamDojo">nvidia / DreamDojo · Hugging Face</a></li>
<li><a href="https://dreamdojo-world.github.io/">DreamDojo : A Generalist Robot World Model from Large-Scale Human...</a></li>

</ul>
</details>

**标签**: `#reproducibility`, `#peer-review`, `#world-models`, `#robotics`, `#nvidia`

---

<a id="item-tech-news-11"></a>
### [ThinkingBox: Solving an agent task once vs. solving it 20/20: 507 stateful workflows graded on terminal database state \[R\]](https://www.reddit.com/r/MachineLearning/comments/1x17shf/thinkingbox_solving_an_agent_task_once_vs_solving/) ⭐️ 7.0/10

Microsoft researchers introduce ThinkingBox-Bench, a 507-task, 5-domain benchmark showing that AI agents&\#x27; single-run success rates poorly predict actual terminal-state correctness across 10,140 trials per model.

reddit · r/MachineLearning · /u/tuhin\_k · 10月9日 00:50

**标签**: `#AI-agents`, `#agent-evaluation`, `#benchmark`, `#LLM-reliability`, `#Microsoft-Research`

---

<a id="item-tech-news-12"></a>
### [北京不会放慢前沿步伐：中国速度优先的 AI 安全监管体系](https://newsletter.semianalysis.com/p/beijing-will-not-pace-the-frontier) ⭐️ 6.0/10

据 SemiAnalysis 分析报道，中国的 AI 安全监管采取速度优先策略，北京不太可能因安全考虑而减缓前沿 AI 的发展。分析指出，AI 安全议题目前备受关注，但中国在监管与推进前沿技术之间的平衡与美国形成鲜明对比。

rss · Semianalysis · 10月8日 17:46

**标签**: `#AI policy`, `#AI safety`, `#China`, `#geopolitics`, `#regulation`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [标普：中国房地产长期低迷或接近尾声](https://www.cnbc.com/2026/10/08/chinas-real-estate-market-may-be-set-for-a-turnaround-sp-says.html) ⭐️ 7.0/10

标普全球评级周四发布报告称，中国持续多年的房地产市场低迷可能接近尾声，预计全国住宅价格将于 2028 年第三季度触底，北京、上海等一线城市最早 2027 年即可回升。该机构今年 2 月还认为高库存使&quot;市场复苏无望&quot;。

rss · CNBC Finance · 10月8日 09:27

**「背景」** 自 2021 年峰值以来，中国住宅价格已累计下跌 22%，相比之下日本楼市危机期间最大跌幅达 67%。标普分析师表示，预测转向源于两项新政策：8 月出台的限制开发商销售未完工楼盘措施，以及针对总价低于 150 万元（约 22 万美元）、面积不超过 120 平方米的首套房按揭利率补贴。

**「影响」** 标普分析师 Edward Chan 指出，开发商将因此谨慎购地、减少新项目开发，该机构预计供应收缩将成为未来一到两年稳定房价的主要因素。

**标签**: `#China economy`, `#real estate`, `#S&amp;P forecast`, `#property policy`, `#global markets`

---

<a id="item-finance-news-2"></a>
### [华为加码智能手机,电动车交付 9 月同比下滑 29%](https://www.cnbc.com/2026/10/08/huawei-china-smartphone-ev-slow.html) ⭐️ 7.0/10

华为发布搭载自研&quot;LogicFolding&quot;芯片的 Mate 90 系列智能手机并将重心重新聚焦手机业务;CNBC 测算显示其电动车合作伙伴 HIMA 9 月交付量同比下滑 29%,Counterpoint 数据亦显示 8 月、9 月中国智能手机市场出现两位数同比下跌。

rss · CNBC Finance · 10月8日 08:04

**「背景」** 受 2019 年美国制裁影响,华为消费者业务收入 2021 年减半至约 340 亿美元,2025 年回升至约 510 亿美元\(占总营收 39%\);华为不直接造车,而是为赛力斯等合作车企提供软件与辅助驾驶系统。

**「影响」** 华为电动车主要合作方赛力斯年内股价跌超 60%,而比亚迪月销量稳定在 40 万辆以上、零跑月交付突破 10 万辆,显示华为在手机与电动车两条赛道均面临强势竞争对手。

**标签**: `#Huawei`, `#smartphones`, `#China EV market`, `#semiconductors`, `#corporate strategy`

---