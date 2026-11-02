---
layout: default
title: "Horizon Summary: 2026-11-02 (ZH)"
date: 2026-11-02
lang: zh
---

> 从 61 条内容中筛选出 10 条重要资讯。

---

**科技新闻**
1. [OmniDiff：面向多格式的 Rust Git 差异工具](#item-tech-news-1) ⭐️ 7.0/10
2. [数学研究应如何适应 AI](#item-tech-news-2) ⭐️ 7.0/10
3. [FBI 指称朝鲜实施 63 亿美元币安加密货币盗窃案](#item-tech-news-3) ⭐️ 7.0/10
4. [AI“分词器税”造成最高 17 倍 Token 消耗差距](#item-tech-news-4) ⭐️ 7.0/10
5. [微软拟向 6 万名员工提供买断方案](#item-tech-news-5) ⭐️ 7.0/10
6. [GDPx：跨领域衡量前沿模型能力](#item-tech-news-6) ⭐️ 6.0/10
7. [数据中心反弹两党化，2028 年建设风险上升](#item-tech-news-7) ⭐️ 6.0/10
8. [NASA 征集商业方案延长哈勃寿命](#item-tech-news-8) ⭐️ 6.0/10
9. [加州第 45 号提案或为数据中心留下监管漏洞](#item-tech-news-9) ⭐️ 6.0/10
10. [Emacs 与 Vi 迎来 50 周年](#item-tech-news-10) ⭐️ 6.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [OmniDiff：面向多格式的 Rust Git 差异工具](https://github.com/ivankovic/omnidiff) ⭐️ 7.0/10

Show HN 项目 OmniDiff 是一个仍在早期开发中的 Rust 开源 Git difftool，采用 AGPLv3 许可，目标是按内容类型展示代码与非代码文件的差异。它支持 25 种语言的代码，以及配置文件、图片、PDF、压缩包、光标和字体等内容。作者称，其设计依据来自 Gentoo packages 所列 7,400 个仓库中抽样的 2,000 份真实 diff，并人工解决了这些差异；同一语料也用于 CI，因此作者认为代码库具有较高鲁棒性。作者自测称，在一台 2023 款 ThinkPad T14s 上，处理数万行 C++ 文件的差异可在 100 毫秒内完成；当前版本为 v0.3.0，作者已连续数月将其作为日常 Git difftool 使用，但三方差异等能力尚未得到确认。作者同时披露会使用 AI，但强调并非完全依赖 AI 编程。

hackernews · FabCH · 11月1日 13:02 · [社区讨论](https://news.ycombinator.com/item?id=50325253)

**「背景」** Git difftool 是让 Git 调用外部差异查看器的机制，而“内容感知”比较会按代码、配置、图像、PDF 等格式分别解析内容，而不是仅逐行比较文本。OmniDiff 是一个以 Rust 编写、采用 AGPLv3 许可证的早期项目，目前版本为 v0.3.0；其格式处理管线源于对 Gentoo 软件包所列 7,400 个仓库中 2,000 个差异样本的人工研究与解决经验。

**「实际影响」** 开发者可通过交互式向导将 OmniDiff v0.3.0 配置为全局或当前仓库的 Git difftool 后端，以统一查看代码及配置、图像、PDF、压缩包等异构内容；不过其三方差异与合并支持仍不明确，复杂 rebase 冲突场景的收益尚待验证。

**「社区反馈」** 评论者认可这一采用 AGPLv3 的 Rust 新项目，但也指出上下文变化可能使 Git rebase 产生本可由人工轻松解决的冲突，Markdown 列表末尾追加内容等情况尤其明显。其他疑问集中在使用方式和生态集成上，包括能否不修改全局 Git 配置而直接管道调用、是否支持三方差异以及能否集成到 Git 上游；也有人认为其展示效果尚未达到 delta 的 diff-so-fancy 模式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ivankovic/omnidiff">GitHub - ivankovic/omnidiff: Fast, robust, accurate diffing</a></li>

</ul>
</details>

**标签**: `#developer-tools`, `#git`, `#rust`, `#open-source`, `#content-aware-diffing`

---

<a id="item-tech-news-2"></a>
### [数学研究应如何适应 AI](https://terrytao.wordpress.com/2026/11/01/mathematics-has-changed-lets-act-like-it/) ⭐️ 7.0/10

陶哲龙在 2026 年 11 月 1 日发表的文章《Mathematics has changed. Let&\#x27;s act like it》中主张，数学界应正视 AI 已经进入证明生成、选题、结果消化和研究方向规划等环节，并据此调整研究实践与成果评价。数学贡献不应仅以原始证明中是否出现新的关键思路衡量：能够借助 AI 得到证明、充分理解其内容并由此提出有价值后续问题的人，同样可能做出实质贡献。随着 AI 能力可能从定理证明继续扩展到选择值得探索的问题、协调研究资源和向外界解释发现，成果归属、协作方式、发表机制与学术信用都将成为需要重新审视的问题。现有材料没有展示具体的新定理、AI 系统、性能指标或量化收益，因此该文提出的是数学工作方式将变，而非某项技术突破已经发生的论证。

hackernews · smilelamp · 11月1日 18:28 · [社区讨论](https://news.ycombinator.com/item?id=50328251)

**「AI 参与数学研究」** 这场讨论的背景是，AI 已开始参与定理证明和数学研究流程，使证明环节出现新的分工方式，而数学贡献也需结合选题、理解和后续探索来衡量。陶哲轩将这一观点概括为：即使证明完全由 AI 生成，只要研究者选择值得解决的问题、彻底理解证明，并据此提出进一步的问题或方向，也可以构成实质性数学贡献；相关讨论还强调，AI 的作用不只限于证明，也包括选择研究方向、吸收和解释结果，以及组织他人继续探索。

**「对数学研究与培养的影响」** 随着 AI 参与证明、选题和成果阐释，数学研究与培养体系可能需要更重视提出有价值的问题、彻底理解并消化所得结果、据此拓展新方向及吸引他人参与，而不再仅以是否贡献了新的证明技巧来评价工作；研究生教育也可能更强调跨领域的全局视野与扎实技术能力。现有材料主要是主张和社区讨论，尚无新定理、系统或量化成效证明这种改变已经落地。

**「社区讨论」** 社区中较明确的共识是，AI 参与不应把“是否贡献了原证明的新要素”当作唯一标准；选题、完整理解和基于 AI 证明继续追问，也可以构成重要的数学贡献。讨论也指出，许多生成的证明往往冗长、晦涩，早期版本不够优雅并不罕见；不少数学家因数学界社会基础改变及“我现在该做什么”而感到受挫，说明对更广泛智能体能力的乐观预期与实际适应焦虑并存。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://terrytao.wordpress.com/2026/11/01/mathematics-has-changed-lets-act-like-it/">Mathematics has changed . Let ’ s act like it | What&#x27;s new</a></li>
<li><a href="https://news.ycombinator.com/item?id=50328251">Mathematics has changed . Let &#x27; s act like it | Hacker News</a></li>
<li><a href="https://news.ycombinator.com/item?id=50328251">Mathematics has changed . Let &#x27; s act like it | Hacker News</a></li>
<li><a href="https://terrytao.wordpress.com/2026/11/01/mathematics-has-changed-lets-act-like-it/">Mathematics has changed. Let’s act like it | What&#x27;s new</a></li>

</ul>
</details>

**标签**: `#AI-assisted mathematics`, `#AI agents`, `#research workflow`, `#mathematical proof`

---

<a id="item-tech-news-3"></a>
### [FBI 指称朝鲜实施 63 亿美元币安加密货币盗窃案](https://www.theverge.com/tech/1024176/north-korea-binance-crypto-heist) ⭐️ 7.0/10

美国联邦调查局（FBI）称，10 月 29 日针对币安（Binance）的 63 亿美元加密货币盗窃案由朝鲜行为体实施，并将相关行动命名为“TraderTraitor”。FBI 表示，与该黑客活动有关的 actors 正在把被盗代币转换为以太坊，并为进一步洗钱做准备。币安则称，目前已覆盖被盗资产的 95%，但现有报道没有说明“覆盖”的具体方式。朝鲜责任及 63 亿美元规模源自 FBI 的指称，公开材料披露的技术细节仍然有限。

rss · The Verge · 11月1日 14:33

**「TraderTraitor 的背景」** “TraderTraitor”是美国联邦调查局用于指称朝鲜国家支持型黑客行动的名称，此前曾与 2025 年 Bybit 的 15 亿美元盗币事件及 2022 年约 6.2 亿美元的其他加密货币盗窃案相关。此次归因属于 FBI 的调查结论；币安尚未公布最终攻击者认定，并表示仍在与执法机构合作。

**「Binance 用户提款分阶段恢复」** 这起事件已直接扰动 Binance 用户：平台在称已覆盖被盗资产的 95%后分阶段恢复提款，交易所重新上线时提款量一度激增，意味着部分用户仍面临提款延迟与被盗资金追回的不确定性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://changenow.io/blog/binance-hack-2026">Binance Hack 2026: How $ 6 . 3 B Was Stolen | ChangeNOW Blog</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/fbi-links-63-billion-binance-crypto-heist-to-north-korean-hackers/">FBI links $ 6 . 3 billion Binance crypto heist to North Korean hackers</a></li>
<li><a href="https://www.yahoo.com/news/us/articles/fbi-links-record-6-3-010848750.html">FBI links record $ 6 . 3 billion Binance crypto theft to North Korea</a></li>
<li><a href="https://www.reuters.com/legal/government/binance-resumes-bitcoin-withdrawals-after-covering-bulk-stolen-63-billion-2026-11-01/">Binance sees spike in withdrawals as exchange returns online ...</a></li>
<li><a href="https://www.cnbc.com/2026/10/31/binance-hack-asset-coverage-withdrawals.html">Binance resumes withdrawals following record $6.3 billion hack</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#cryptocurrency`, `#state-sponsored hacking`, `#Binance`, `#North Korea`

---

<a id="item-tech-news-4"></a>
### [AI“分词器税”造成最高 17 倍 Token 消耗差距](https://clear-languages.org/blog/the-tokenizer-tax) ⭐️ 7.0/10

CLEAR 研究联盟发布报告称，主流 AI 模型的分词器明显偏向英语及高资源语言，部分语言处理相同内容所需 Token 数量显著更高。报告覆盖约 200 种语言，并给出同一句话的对比：英语需要 13 个 Token，马拉雅拉姆语需要 26 个，阿姆哈拉语高达 78 个；不同语言的 Token 消耗差距最高被报告为 17 倍。这可能使多语言使用面临更高调用成本、更长响应延迟和更小的有效上下文容量。不过，现有材料未说明所用模型、分词基准与实验方法，17 倍应理解为报告中的 Token 消耗差距，实际成本差异还取决于计费方式和模型配置。

telegram · zaihuapd · 11月1日 16:06

**「什么是“分词器税”」** 大语言模型会先通过分词器把文本切分为 Token；相同语义在不同语言中可能产生不同数量的 Token，这种差异通常以“分词器 fertility”（每个词对应的 Token 数）衡量。相关研究利用平行文本比较各语言的 Token 消耗，例如一项研究考察了 10 个基础模型和 25 种欧洲语言，并建立了受控的分词器成本图谱。由于 API 费用通常随输入 Token 计算，Token 越多也会占用更多有限上下文，因此非英语文本可能同时面临成本和容量劣势。

**「实际影响」** 多语言应用开发者需要按目标语言实测 Token 用量，否则基于英语估算的费用可能低估账单，而低资源语言消耗更多上下文还会压缩模型可用的信息量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://restofworld.org/2026/ai-tokenizer-tax-non-english-languages-cost-inequity/">The Tokenizer Tax : Why non-english AI users pay... - Rest of World</a></li>
<li><a href="https://huggingface.co/papers/2605.24718">Paper page - The Tokenizer Tax Across 25 European Languages ...</a></li>

</ul>
</details>

**标签**: `#大语言模型`, `#分词器`, `#多语言AI`, `#AI成本`

---

<a id="item-tech-news-5"></a>
### [微软拟向 6 万名员工提供买断方案](https://news.google.com/rss/articles/CBMia0FVX3lxTE9hcEdkSTR5MEx3UUQxbmpDVlNfTHdmTkl3eGlvbTBMMnlabnh4RW1ad1ZzY0pGbjdXaFlfc2dCV2hyQm5RT3UwN2hnWkU2ZURKbWdKLU50NVZ6dzgyWUF5TWtabkVZMFRPQXZB?oc=5) ⭐️ 7.0/10

据 Mashable 报道，微软拟向约 6 万名员工提供自愿买断方案，此举发生在公司增加人工智能投资之际。若方案得到确认且覆盖全部员工，将构成一次大规模劳动力调整；但现有标题并未证明买断与 AI 投资之间存在直接因果关系。当前材料未说明涉及的业务线、地区、补偿金额、实施时间、员工资格及微软的正式确认，因此相关规模与影响仍待进一步核实。

google\_news · Mashable · 11月1日 20:35

**「买断方案与用工背景」** 这里的“买断”是公司向符合条件的员工提供自愿离职补偿的方案；“6 万名”指潜在覆盖规模，并不代表所有员工都会接受或离开。此类举措反映科技公司在增加 AI 投入的同时，通过自愿离职缩减成本并调整岗位；报道还称，微软此前已向约 9,000 名美国员工提供类似买断，而其全球全职员工约为 223,000 人。

**「影响」** 微软向约 6 万名员工提供自愿买断，为受影响员工提供离职补偿渠道，并可能借 AI 高额投资降低人力成本。微软预计只有少数员工会接受，因此实际离职规模可能远低于 6 万人，但自愿买断也存在顶尖人才流失的风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.kucoin.com/news/flash/microsoft-offers-voluntary-buyouts-to-60-000-employees-amid-ai-investment-surge">Microsoft Offers Voluntary Buyouts to 60 , 000 Employees Amid AI ...</a></li>
<li><a href="https://www.usnews.com/news/top-news/articles/2026-10-26/microsoft-is-offering-buyouts-to-around-60-000-employees-business-insider-reports">Microsoft Offers Buyouts to Around 60 , 000 Employees to Contain...</a></li>
<li><a href="https://www.theguardian.com/technology/2026/oct/26/microsoft-buyout-offers-ai-cuts">Microsoft to reportedly offer buyouts to 60 , 000 employees in latest...</a></li>
<li><a href="https://www.nytimes.com/2026/10/26/technology/microsoft-buyouts-ai-spending.html">Microsoft Offers Buyouts to 60 , 000 Employees as It Spends on A . I .</a></li>
<li><a href="https://hbr.org/2026/10/are-microsofts-voluntary-buyouts-a-sign-of-whats-to-come">Are Microsoft ’s Voluntary Buyouts a Sign of What’s to Come?</a></li>

</ul>
</details>

**标签**: `#Microsoft`, `#AI investment`, `#workforce restructuring`, `#employee buyouts`

---

<a id="item-tech-news-6"></a>
### [GDPx：跨领域衡量前沿模型能力](https://newsletter.semianalysis.com/p/gdpx-measuring-frontier-model-capabilities) ⭐️ 6.0/10

GDPx 提出一个跨领域基准，用于衡量前沿 AI 模型在软件工程、硬件与芯片设计、网络安全、生物科学、金融、法律、量化交易、材料科学、对齐以及 RSI 等领域的 capabilities。该基准旨在以跨领域方式评估模型在多个高价值技术与专业领域中的表现。现有材料仅说明了覆盖范围，未提供具体任务、评分方法、模型测试结果、外部验证或与既有基准的对比。因此，GDPx 的实际评测价值与影响尚无法从当前信息中确认，仍需后续方法论和实验数据支持。

rss · Semianalysis · 11月2日 01:51

**「概念背景」** GDPx 被定位为评估智能体式 AI 能力的基准，关注模型完成多步骤真实任务的表现，而非传统单题问答；它也不同于按 GDP 占比或 O\*NET 职业分类为任务加权的思路，转而押注早期 AI 收入会集中于少数高投资回报领域。它的名称容易与 OpenAI 于 2025 年 9 月 25 日推出的 GDPval 混淆，后者是另一项评测，用于衡量模型在 44 种职业中具有经济价值的真实任务上的表现。

**「实际影响」** GDPx 为模型开发者及软件工程、网络安全、生物、金融和芯片设计等领域的评测者提供了跨领域能力评估框架的候选方案；但在缺少方法、结果与验证的情况下，尚无证据表明它能可靠比较前沿模型或实际指导部署决策。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://newsletter.semianalysis.com/p/gdpx-measuring-frontier-model-capabilities">GDPx: Measuring Frontier Model Capabilities Across the Most ...</a></li>
<li><a href="https://openai.com/index/gdpval/">Measuring the performance of our models on real-world tasks</a></li>
<li><a href="https://www.theai.news/">The AI News — the two-model consensus AI briefing</a></li>

</ul>
</details>

**标签**: `#AI benchmarks`, `#frontier models`, `#model evaluation`, `#software engineering`, `#AI safety`

---

<a id="item-tech-news-7"></a>
### [数据中心反弹两党化，2028 年建设风险上升](https://newsletter.semianalysis.com/p/the-datacenter-backlash-goes-bipartisan) ⭐️ 6.0/10

文章称，美国数据中心扩张的 2027 年部署大体已成定局，但 2028 年建设计划面临显著更高的许可和政治风险。得克萨斯州可能长期冻结相关许可，被列为全美数据中心扩建的最大单一风险。两党的政策主张都趋向更严格的规则，显示数据中心监管阻力正跨越党派界线。对 AI 基础设施规划者而言，2028 年的项目容量与上线节奏需要按照可能延后而非确定兑现来评估。

rss · Semianalysis · 11月1日 18:40

**「德州数据中心许可冻结背景」** 2026 年 9 月 21 日，德州州长格雷格·阿博特指示德州环境质量委员会（TCEQ）暂停签发所有数据中心许可，直至德州电力可靠性委员会（ERCOT）完成审计。相关报道将这一没有明确结束时间的措施称为开放式冻结，意味着数据中心扩建同时受到环境许可和电网审计约束。

**「潜在影响」** 对在得州布局 2028 年数据中心的开发商而言，若许可冻结持续，项目可能因 ERCOT 的电网与水资源审查而延迟审批，并迫使开发商调整选址和资本计划；叠加两党收紧规则，2028 年美国数据中心新增容量的交付确定性将低于已基本锁定的 2027 年。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://gov.texas.gov/news/post/governor-abbott-directs-tceq-to-halt-data-center-permits">Governor Abbott Directs TCEQ To Halt Data Center Permits</a></li>
<li><a href="https://finance.yahoo.com/technology/articles/texas-imposes-open-ended-freeze-132054535.html?fr=sycsrp_catchall">Texas imposes open-ended freeze on data-center environmental ...</a></li>
<li><a href="https://constructionreviewonline.com/texas-hits-the-pause-button-on-data-centers-as-ai-boom-meets-infrastructure-limits/">Texas Hits the Pause Button on Data Centers as AI Boom Meets ...</a></li>
<li><a href="https://gridreadiness.com/blog/texas-data-center-permit-freeze-ercot-audit-2026">Texas Just Froze Data Center Permits. Here&#x27;s What Changed</a></li>
<li><a href="https://www.landgate.com/news/texas-halts-data-center-permits-what-developers-need-to-know">Texas Halts Data Center Permits: What Developers Need to Know</a></li>

</ul>
</details>

**标签**: `#data centers`, `#AI infrastructure`, `#US policy`, `#permitting`, `#infrastructure planning`

---

<a id="item-tech-news-8"></a>
### [NASA 征集商业方案延长哈勃寿命](https://www.theverge.com/science/1024239/nasa-commercial-space-save-hubble) ⭐️ 6.0/10

NASA 正在邀请商业航天行业提交方案，通过提升哈勃空间望远镜的轨道来延长其运行寿命。哈勃仍会因地球引力而缓慢降低轨道，但目前没有立即坠入大气层的危险；若不采取轨道提升措施，其运行寿命预计将在 2030 年代初至中期左右结束。现有信息尚未说明具体提案要求、技术路线、任务时间表或预算，因此能否以及何时成功延长哈勃寿命仍不确定。

rss · The Verge · 11月1日 21:09

**「背景」** 哈勃空间望远镜于 1990 年发射进入近地轨道，此后持续开展天文观测并取得多项重要发现。近地轨道会因稀薄大气阻力而逐渐降低，因此延长望远镜寿命需要设法提升其轨道高度。NASA 早期运营研究曾认为当时的机器人维修方案尚不可行，并建议实施一次增加安全措施的后续载人维修任务，这也构成了此次重新征集商业方案的历史背景。

**「潜在影响」** 若商业轨道提升方案获选并成功执行，NASA 有望让哈勃望远镜在低地球轨道中的运行寿命延长至 2030 年代之后，从而继续支持天文学观测与研究；但该计划目前仅处于征集提案阶段，尚无确定的任务、合同或实施时间表。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Hubble_Space_Telescope">Hubble Space Telescope - Wikipedia</a></li>
<li><a href="https://science.nasa.gov/mission/hubble/">Hubble Space Telescope - NASA Science</a></li>
<li><a href="https://www.govinfo.gov/content/pkg/GOVPUB-NAS-PURL-gpo152941/pdf/GOVPUB-NAS-PURL-gpo152941.pdf">Not Yet Imagined: A Study of Hubble Space Telescope Operations</a></li>
<li><a href="https://en.wikipedia.org/wiki/Hubble_Space_Telescope">Hubble Space Telescope - Wikipedia</a></li>
<li><a href="https://science.nasa.gov/apod/archive/">Astronomy Picture of the Day Archive - NASA Science</a></li>

</ul>
</details>

**标签**: `#Hubble Space Telescope`, `#orbital servicing`, `#commercial space industry`, `#NASA`

---

<a id="item-tech-news-9"></a>
### [加州第 45 号提案或为数据中心留下监管漏洞](https://www.theverge.com/policy/1023877/prop-45-california-data-centers-energy) ⭐️ 6.0/10

加州第 45 号 ballot 提案拟为符合条件的“必要基础设施”缩短州级环境评估期限，同时增加居民在法院质疑相关项目的难度。环境倡导者警告称，数据中心开发商可能借此绕开公开审查，使该提案成为数据中心的潜在监管漏洞。支持者提出的理由及提案的项目适用范围、具体司法程序变更在现有来源中尚未完整披露，因此这一风险目前属于倡议者的主张，而非已经证实的结果。

rss · The Verge · 11月1日 13:00

**「政策背景」** 加州《环境质量法》（CEQA）要求对可能显著影响环境的发展项目进行审查；支持者认为它是环境评估的重要工具，批评者则认为相关程序有时会拖慢住房等建设。Proposition 45 拟缩短“必要基础设施”项目的审查时限并增加法律挑战难度，若在 11 月 3 日公投中通过，还可能限制政府和地方在项目申请提交后改变开发规则。

**「潜在影响」** 如果 Proposition 45 获通过且数据中心被认定为符合条件的“关键基础设施”，开发商可能获得更快的环境审查，同时削弱居民通过诉讼挑战项目的空间，进而加快加州 AI 基础设施建设。数据中心是否实际适用该条款仍存在争议，因此其影响程度取决于最终认定和实施方式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.latimes.com/environment/story/2026-10-14/californias-prop-45-aims-to-speed-construction-projects-opponents-say-data-centers-will-benefit">California ’s Prop. 45 aims to speed construction projects.</a></li>
<li><a href="https://www.nytimes.com/2026/10/15/business/economy/californias-housing-proposition-45.html">California ’s Proposition 45 Brings the Sprawl Debate Back - The New...</a></li>
<li><a href="https://www.yahoo.com/news/politics/articles/last-minute-guide-proposition-45-120000991.html">Your last-minute guide to Proposition 45 : CEQA and data centers</a></li>
<li><a href="https://calmatters.org/economy/technology/2026/10/prop-45-could-open-door-for-california-data-centers/">Prop. 45 could reshape the fight over California data centers</a></li>
<li><a href="https://www.latimes.com/environment/story/2026-10-14/californias-prop-45-aims-to-speed-construction-projects-opponents-say-data-centers-will-benefit">California’s Prop. 45 aims to speed construction projects ...</a></li>
<li><a href="https://www.sacbee.com/news/politics-government/capitol-alert/article317037230.html">Are new data centers included in Prop 45? It’s up for debate ...</a></li>

</ul>
</details>

**标签**: `#data centers`, `#regulation`, `#infrastructure`, `#environmental policy`, `#California`

---

<a id="item-tech-news-10"></a>
### [Emacs 与 Vi 迎来 50 周年](https://www.theregister.com/applications/2026/11/01/mother-of-all-editors-emacs-is-50/5306727) ⭐️ 6.0/10

...

rss · The Register · 11月1日 11:51

**「历史背景」** Emacs 最初并非一款独立编辑器：其前身是 Dan Murphy 于 1962 年编写的 TECO（Text Editor and Corrector），随后在麻省理工学院人工智能实验室发展出名为“Editing MACroS”的宏扩展，因此这段历史通常从 1974 年算起。Vi 后来成为 Emacs 长期并存的经典对手，所以“Emacs 与 Vi 同庆 50 岁”回顾的是两条经典文本编辑器技术谱系在终端时代的演进，而非某项新版本发布。

**「实际影响」** 对开发者和 Linux 用户而言，Emacs 与 Vi 同满 50 岁凸显的是两者塑造并延续了深植于黑客与自由软件文化的“编辑器战争”，长期形成的习惯和工作流仍使它们保持较强影响力。此次周年节点本身不代表新的功能、兼容性或性能变化，其实际意义主要在于历史与文化层面。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theregister.com/applications/2026/11/01/mother-of-all-editors-emacs-is-50/5306727">&#x27;Mother of all editors&#x27; Emacs is 50 - The Register</a></li>
<li><a href="https://news.lavx.hu/article/mother-of-all-editors-emacs-is-50">&#x27;Mother of all editors&#x27; Emacs is 50 | LavX News</a></li>
<li><a href="https://en.wikipedia.org/wiki/Editor_war">Editor war - Wikipedia</a></li>
<li><a href="https://www.zdnet.com/article/5-top-linux-text-editors-that-arent-vi-or-emacs-and-why-they-are-my-favorite/">5 top Linux text editors that aren&#x27;t vi or Emacs ( and why...) - ZDNET</a></li>

</ul>
</details>

**标签**: `#Emacs`, `#Vi`, `#text editors`, `#software history`

---