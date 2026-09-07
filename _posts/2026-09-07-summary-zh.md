---
layout: default
title: "Horizon Summary: 2026-09-07 (ZH)"
date: 2026-09-07
lang: zh
---

> 从 68 条内容中筛选出 11 条重要资讯。

---

**科技新闻**
1. [阿努比斯 WebAssembly 移植耗时一年，工程权衡深度解析](#item-tech-news-1) ⭐️ 7.0/10
2. [OpenAI 发布博文《外星人的思维》，探讨 AI 对齐与递归自我改进](#item-tech-news-2) ⭐️ 7.0/10
3. [OpenAI 研究加速：内部编码代理使用数据](#item-tech-news-3) ⭐️ 7.0/10
4. [Isar Aerospace 的 Spectrum 成欧洲首枚全商业入轨火箭](#item-tech-news-4) ⭐️ 7.0/10
5. [Interisle 报告：约五分之一新注册 gTLD 域名被用于诈骗](#item-tech-news-5) ⭐️ 6.0/10
6. [西雅图时报和新闻 day 起诉 OpenAI 和微软侵权](#item-tech-news-6) ⭐️ 6.0/10
7. [UTC 或将允许最多偏离一小时](#item-tech-news-7) ⭐️ 6.0/10
8. [Meta FAIR 发布 AI 研究偏好模型：排序 ML 实验以节省 GPU 算力](#item-tech-news-8) ⭐️ 6.0/10

**财经新闻**
1. [8 家中央金融企业共增资 3600 亿元 补充核心一级资本](#item-finance-news-1) ⭐️ 8.0/10
2. [糖价年内涨幅跑赢美股，供应担忧推升价格](#item-finance-news-2) ⭐️ 7.0/10
3. [长鑫科技 DRAM 市占率升至 10%](#item-finance-news-3) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [阿努比斯 WebAssembly 移植耗时一年，工程权衡深度解析](https://anubis.techaro.lol/blog/2026/anubis-wasm/) ⭐️ 7.0/10

Anubis 是一款被 GNOME、SourceHut 等开源项目采用的工作量证明（PoW）验证码，作者花了一年时间将其移植到 WebAssembly，以提升对依赖 JavaScript 求解器的 AI 爬虫的防御门槛。文中详细记录了工程改造过程，并讨论了兼容性权衡：为照顾智能电视等老旧浏览器，仍需保留 JavaScript 备用路径，同时不可避免地影响了无障碍体验。评论区还延伸出 Rust 的 wasm32v1-none 目标、目标 Chrome 66 等具体兼容性策略，整体技术讨论深入务实。

hackernews · xena · 9月6日 20:32 · [社区讨论](https://news.ycombinator.com/item?id=49590611)

**标签**: `#webassembly`, `#captcha`, `#anti-scraping`, `#open-source-infrastructure`, `#systems-engineering`

---

<a id="item-tech-news-2"></a>
### [OpenAI 发布博文《外星人的思维》，探讨 AI 对齐与递归自我改进](https://openai.com/index/an-alien-mind/) ⭐️ 7.0/10

OpenAI 在其官方博客发布文章《An Alien Mind》，围绕 AI 对齐、递归自我改进（RSI）以及推进 AI 能力发展的战略理由展开论述，认为加速研发更智能的模型是构建防御性系统、应对其他 AI 威胁的必要手段。该文在 Hacker News 上引发超过 340 点热度、近 300 条评论的广泛讨论，社区围绕 AI 安全竞赛逻辑、人类对齐难题以及公司商业化立场等议题展开了激烈辩论。有评论指出，文章带有明显的上市前定位色彩，将本应用于保护人类安全的使命与商业化进程绑定；也有声音认为，自动化 AI 研究将是放大智能算力规模的重要途径，OpenAI 正在以此保持在 AI 研究前沿。

hackernews · OpenAI News · 9月6日 16:27 · [社区讨论](https://news.ycombinator.com/item?id=49588080)

**标签**: `#AI safety`, `#AI strategy`, `#alignment`, `#OpenAI`, `#recursive self-improvement`

---

<a id="item-tech-news-3"></a>
### [OpenAI 研究加速：内部编码代理使用数据](https://simonwillison.net/2026/Sep/6/research-acceleration-the-view-inside-openai/) ⭐️ 7.0/10

Simon Willison 在其博客上撰文解读了 OpenAI 发布的《Research acceleration: The view inside OpenAI》报告，重点展示 OpenAI 研究人员使用编码代理（coding agents）的内部数据。报告配图显示，单名研究者每日的美元开销在 2026 年 2 月接近 0，4 月升至约 50，6 月达到约 150，7 月保持在 150–165 美元区间，随后在 7 月底至 8 月急剧攀升至约 600 美元。Simon 推测 7 月底的加速拐点可能对应内部员工开始使用后来作为 GPT-6 Astra 发布的模型。报告中未展开的缩写 RSI（Recursive Self-Improvement）被 Simon 解读为 OpenAI 对 AGI 的新提法，并与首席科学家 Jakub Pachocki 撰写的《An Alien Mind》一同构成 OpenAI 当天“RSI 日”的双重发布。

rss · Simon Willison · 9月6日 23:57

**「背景」** RSI（Recursive Self-Improvement，递归自我改进）指 AI 系统通过迭代改进自身能力的过程，是 OpenAI 在本轮发布中提出的新概念，用以替代或补充其此前对 AGI 的表述。Simon Willison 是长期追踪 OpenAI 等前沿实验室动向的 LLM 与生成式 AI 评论者，本篇解读基于 OpenAI 官方公开材料，属于一手资料的二次转述。该报告同时延续了 OpenAI 自 2025 年 11 月以来对自身 agentic 流程公开化的趋势。

**「影响」** 该图表为前沿 AI 实验室内部编码代理的实际采用情况提供了难得的可视化数据，说明 2026 年下半年 agentic engineering 在 OpenAI 研究流程中的开销与频次出现陡峭跃升；但由于数据来自 OpenAI 自身发布，测算口径与样本范围存在局限，文中未披露每位研究者具体使用何种代理或任务类型。

**标签**: `#AI`, `#OpenAI`, `#Coding Agents`, `#Agentic Engineering`, `#AGI`

---

<a id="item-tech-news-4"></a>
### [Isar Aerospace 的 Spectrum 成欧洲首枚全商业入轨火箭](https://arstechnica.com/space/2026/09/german-company-becomes-first-in-europe-to-launch-fully-commercial-orbital-rocket/) ⭐️ 7.0/10

德国 Isar Aerospace 从挪威安岛航天发射场成功将自研两级 Spectrum 火箭送入近地轨道，使其成为欧洲首枚实现入轨的全商业运载火箭。火箭于当地时间周六 22 时 12 分从北极圈内的安岛航天发射场升空，高约 28 米，并在约七分钟后进入轨道。此次任务将五颗小卫星和一项实验载荷送入太空；Isar Aerospace 将以此为基础扩大火箭生产、履行现有订单，并争取商业及机构发射客户。

rss · Ars Technica · 9月6日 11:55

**「欧洲发射市场背景」** 长期以来，欧洲的轨道发射能力主要由政府主导的项目提供，特别是欧洲航天局（ESA）旗下的阿丽亚娜系列火箭和织女星（Vega）小型运载火箭，由法国主导的 Arianespace 公司负责商业运营，形成事实上的发射垄断。近几年，以 Isar Aerospace（德国，2018 年由慕尼黑工业大学三名学生创立）、西班牙的 PLD Space 和德国的 HyImpulse 为代表的一批欧洲私营火箭公司相继涌现，瞄准中小型卫星发射市场，试图打破这种停滞的格局。Isar Aerospace 的 Spectrum 火箭为两级液体运载火箭，从挪威北部安岛航天发射场升空，专为低地球轨道小型至中型载荷设计。因此，2026 年 9 月 Spectrum 成功入轨，被视为欧洲首枚完全由商业公司开发并进入轨道的运载火箭，标志着欧洲在私营发射领域取得突破。

**「实际影响」** 欧洲商业和机构客户由此获得一个新的轨道发射服务选项，但此次成功尚不能证明 Spectrum 已具备高频、低成本或规模化发射能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.orbitalintel.org/powers/european-launch-startups/">European Launch Startups: PLD Space, HyImpulse, Isar Aerospace ...</a></li>
<li><a href="https://www.spaceinsights.io/insights/isar-aerospace-planet-labs-germany-w28">Isar Aerospace and Planet Labs Germany: The All-German Mission and the ...</a></li>

</ul>
</details>

**标签**: `#commercial space`, `#launch industry`, `#Europe`, `#orbital rockets`, `#Isar Aerospace`

---

<a id="item-tech-news-5"></a>
### [Interisle 报告：约五分之一新注册 gTLD 域名被用于诈骗](https://simonwillison.net/2026/Sep/6/the-purpose-of-dns-is-to-spread-scams/) ⭐️ 6.0/10

Simon Willison 在其链接博客中转述了 Terence Eden 对 Interisle 报告的看法，指出域名系统（DNS）正以惊人比例被犯罪分子用于实施诈骗。报告数据显示，2025 年全球新注册通用顶级域名（gTLD）达 8500 万个，其中约 850 万个在 2025 年 5 月前被各类拦截清单收录。Terence Eden 引用报告估算，新注册 gTLD 域名的滥用比率下限约为 10%，实际可能接近 20%，即每五个新域名中就有一个与诈骗相关。Willison 特别强调自己此前对这一问题严重程度毫无认知，并指出 ICANN 已就该问题讨论多年但未见明显成效。

rss · Simon Willison · 9月6日 14:40

**「背景说明」** 通用顶级域名（gTLD）是由 ICANN 管理的域名后缀类别（如 .com、.net 以及 2014 年后新增的数百个新顶级域）。Interisle 是一家长期追踪网络滥用与犯罪基础设施的研究机构，其定期发布的报告通过汇总多个公开拦截清单来估算恶意域名的注册与传播规模。长期以来，注册廉价、易于批量获取的域名并进行短期诈骗投放（即&quot;throwaway domains&quot;）已是网络犯罪的标准手法之一。

**「影响」** 对域名注册商、网络安全团队以及依赖域名黑名单拦截恶意流量的 Web 服务运营者而言，这意味着基于拦截清单的传统防御策略正面临结构性挑战，需要在注册阶段引入更严格的滥用检测与处置机制。

**标签**: `#DNS`, `#cybersecurity`, `#internet infrastructure`, `#web development`, `#security`

---

<a id="item-tech-news-6"></a>
### [西雅图时报和新闻 day 起诉 OpenAI 和微软侵权](https://www.theverge.com/ai-artificial-intelligence/990932/seattle-times-newsday-lawsuit-openai-microsoft) ⭐️ 6.0/10

西雅图时报（Seattle Times）和新闻 day（Newsday）加入出版商起诉 OpenAI 的行列，指控 OpenAI 和微软在未经许可的情况下将其新闻报道用作 AI 模型的训练数据，并在聊天机器人对用户查询的回应中复制了其报道的段落。该诉讼与此前纽约时报和其他出版商针对类似问题的法律行动相似，涉及生成式 AI 在训练阶段使用受版权保护新闻内容以及在输出中重现相关内容的核心指控。

rss · The Verge · 9月6日 23:36

**「背景」** 自 2023 年《纽约时报》率先起诉 OpenAI 和微软以来，针对生成式 AI 公司未经授权使用受版权保护的新闻内容训练模型的诉讼已形成一股潮流。此类诉讼通常指控 AI 公司未经许可抓取新闻稿件作为训练数据，并在聊天机器人输出中复现原文段落。由于微软的 Copilot 等产品基于 OpenAI 的技术构建，微软也常被列为共同被告。此次诉讼是这一系列法律行动中的最新一起，加入了此前已有近 400 家地方报纸发起的类似诉讼浪潮。

**「影响」** 此次起诉进一步增加了 OpenAI 和微软面临的版权诉讼压力，可能推动出版商在与 AI 公司就训练数据授权谈判时寻求更明确的许可和补偿机制，对 AI 训练数据的获取与使用实践产生累积性影响。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theverge.com/ai-artificial-intelligence/990932/seattle-times-newsday-lawsuit-openai-microsoft">Seattle Times and Newsday sue OpenAI and Microsoft ... | The Verge</a></li>
<li><a href="https://www.engadget.com/2251707/seattle-times-newsday-sue-openai-microsoft-for-copyright-infringement/">Two More News Organizations Sue OpenAI And Microsoft For...</a></li>
<li><a href="https://www.newsmax.com/newsfront/copyright-infringement-lawsuit-openai/2026/09/05/id/1268457/">Seattle Times , Newsday Sue OpenAI , Microsoft | Newsmax.com</a></li>

</ul>
</details>

**标签**: `#AI Legal`, `#Copyright`, `#OpenAI`, `#Generative AI`, `#Media Industry`

---

<a id="item-tech-news-7"></a>
### [UTC 或将允许最多偏离一小时](https://www.theregister.com/offbeat/2026/09/06/time-lords-prepare-to-kick-leap-seconds-into-the-next-millennium/5294538) ⭐️ 6.0/10

英国《The Register》报道，一项应对闰秒风险的提案正在推进，目标可能是取消或推迟闰秒调整。提案的核心变化是允许协调世界时（UTC）与基于地球自转的时间尺度之间积累偏差，极端情况下可达一小时。推动因素是未来可能出现史无前例的负闰秒，即通过删除一秒而非增加一秒来校准时间。报道未提供提案的正式表决时间、适用标准或对现有系统的具体兼容安排，因此目前更适合视为待评估的基础设施标准讨论，而非已生效的变更。

rss · The Register · 9月6日 08:09

**「背景」** 闰秒自 1972 年引入，用于将基于原子钟的协调世界时（UTC）与基于地球自转的世界时（UT1）之差控制在 0.9 秒以内，自该机制实行以来 UTC 已累计增加 27 次正闰秒。正闰秒历来会给数字基础设施带来风险——历史上 Reddit、Cloudflare 及多家航空公司的系统都曾因正闰秒插入而出现故障。负闰秒（删除一秒）则从未实施过，它同样会对依赖连续精确计时的系统构成严重风险，这也是相关国际计量机构正讨论彻底废除闰秒机制、并允许 UTC 相对 UT1 漂移更长时间的背景。

**「影响」** 如果提案最终获批并实施，依赖精确 UTC 的软件、通信网络和金融系统将需要评估时间尺度偏移及兼容改造问题，具体影响取决于采用范围和过渡方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theregister.com/offbeat/2026/09/06/time-lords-prepare-to-kick-leap-seconds-into-the-next-millennium/5294538">Time lords prepare to kick leap seconds into the next millennium</a></li>
<li><a href="https://theintelligent.co.uk/science/2026/nature-proposes-ending-leap-seconds-negative-leap-second-risk-rises">Nature proposes ending leap seconds as negative ... | The Intelligent</a></li>
<li><a href="https://theuniverseepisodes.com/how-fast-does-the-earth-spin/">How Fast Does the Earth Spin? Speed by Latitude ( 2026 )</a></li>

</ul>
</details>

**标签**: `#timekeeping`, `#infrastructure`, `#utc`, `#standards`, `#distributed-systems`

---

<a id="item-tech-news-8"></a>
### [Meta FAIR 发布 AI 研究偏好模型：排序 ML 实验以节省 GPU 算力](https://news.google.com/rss/articles/CBMi4wFBVV95cUxPYXZzVU94NzFvWkZNZmNTLWYxNjFaRmJCR0g2emRYdUxTeTdCcFhOMWh3M0pIcFZRRG12Zi1WNFp3Y0EwRkxnM1h3VjY2TFlUSmZMa2ctd3hOaG44RHFFZE5sSVFOYkFLQW5YWHptaHp1cXVLZjlMSl9LTVA3emFtaVdsb204a25kandyY3R5NndfTWRNYkZ3VHhialY1NDZvcU5xNGxDYXhPQ3MtdGRyal8yN1A5OWpTNGlxRjZyLWRHMEFkVUxXeFgtWmh4eGdrLWZkSmhnaFJhb3poWEFnZTYyRdIB4wFBVV95cUxPYXZzVU94NzFvWkZNZmNTLWYxNjFaRmJCR0g2emRYdUxTeTdCcFhOMWh3M0pIcFZRRG12Zi1WNFp3Y0EwRkxnM1h3VjY2TFlUSmZMa2ctd3hOaG44RHFFZE5sSVFOYkFLQW5YWHptaHp1cXVLZjlMSl9LTVA3emFtaVdsb204a25kandyY3R5NndfTWRNYkZ3VHhialY1NDZvcU5xNGxDYXhPQ3MtdGRyal8yN1A5OWpTNGlxRjZyLWRHMEFkVUxXeFgtWmh4eGdrLWZkSmhnaFJhb3poWEFnZTYyRQ?oc=5) ⭐️ 6.0/10

Meta FAIR 推出了名为 AI 研究偏好模型（Research Preference Models，简称 RPM）的方法，目标是先对机器学习实验进行排序与筛选，再决定是否投入 GPU 算力实际运行，从而减少在低潜力实验上浪费的计算资源。当前可获取的公开材料仅有标题层面的信息，未披露模型架构、训练数据、特征工程细节、评测协议或与现有实验筛选/早停方法（如贝叶斯优化、零成本代理指标等）的对比结果；MarkTechPost 作为二手聚合来源也未给出 Meta FAIR 官方论文、代码仓库或具体性能数据的链接，因此现阶段无法独立验证该方法的有效性边界与可复现性。该思路契合 ML 团队在大模型训练时代普遍面临的算力预算紧张问题，但在缺乏具体技术细节之前，只能将其视为一个有潜在实用价值的研究方向，而非可直接落地的工具。

google\_news · MarkTechPost · 9月6日 20:25

**「背景概念」** 机器学习研究通常需要运行大量实验，每次实验都会消耗大量 GPU 计算资源，因此如何优先选择值得运行的实验是研究工作流里的关键问题。偏好模型（Preference Model）的概念最早因大语言模型对齐中的 RLHF（基于人类反馈的强化学习）而广为人知，它通过对候选输出进行成对比较来预测哪一个更受人类偏好。Meta FAIR 团队将偏好建模扩展到了实验选择场景，利用冻结的预训练语言模型构建两类 RPM，对尚未执行的实验候选进行排序，从而在投入 GPU 资源之前判断哪些实验更值得运行。

**「影响」** 对算力预算受限的 ML 研究与工程团队而言，若 RPM 经证实有效，可在实验筛选阶段节省大量 GPU 小时数并加速研究方向收敛；但在 Meta FAIR 公开技术报告、复现细节与对比基准之前，尚无法判断其相对现有实验排序策略的实际增益与适用范围。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.marktechpost.com/2026/09/06/meta-fair-introduces-ai-research-preference-models-rpms-ranking-ml-experiments-before-spending-gpu-hours/">Meta FAIR Introduces AI Research Preference Models ( RPMs )...</a></li>
<li><a href="https://korshunov.ai/en/article/23541-fair-introduces-rpms-to-rank-ml-experiments-before-execution/">FAIR introduces RPMs to rank ML experiments before execution</a></li>
<li><a href="https://www.aoyii.com/en/ai-research-preference-models-rpm/">Research Preference Models : Meta Prioritizes AI Experiments</a></li>

</ul>
</details>

**标签**: `#machine-learning`, `#meta-fair`, `#research-tools`, `#gpu-optimization`, `#experiment-management`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [8 家中央金融企业共增资 3600 亿元 补充核心一级资本](https://www.news.cn/fortune/20260906/1633e4121bf14b52859aff2dffa36888/c.html) ⭐️ 8.0/10

9 月 6 日，工商银行等 8 家中央金融企业发布增资计划，合计补充核心一级资本 3600 亿元。其中，工行拟向财政部及中国烟草总公司等发行 A 股募资不超过 1000 亿元，农行募资不超过 1600 亿元；财政部分别向进出口银行、出口信用保险公司注资 300 亿元和 100 亿元。此外，中国人保拟募资不超过 150 亿元，财政部向中国人寿集团、中国太平分别注资 350 亿元和 70 亿元，中国再保拟募资 30 亿元。此次大规模注资涉及银行、保险及再保险等多个领域，显示出强化金融体系核心资本的系统性安排。

telegram · zaihuapd · 9月6日 10:47

**标签**: `#Banking`, `#China financial system`, `#Capital markets`, `#Government policy`, `#Insurance`

---

<a id="item-finance-news-2"></a>
### [糖价年内涨幅跑赢美股，供应担忧推升价格](https://www.cnbc.com/2026/09/06/sugar-is-outperforming-the-stock-market-this-year-whats-driving-it.html) ⭐️ 7.0/10

...

rss · CNBC Finance · 9月6日 13:19

**「背景」** ...

**「影响」** ...

**标签**: `#commodities`, `#agricultural-commodities`, `#sugar`, `#food-prices`, `#weather-impact`

---

<a id="item-finance-news-3"></a>
### [长鑫科技 DRAM 市占率升至 10%](https://www.zaobao.com.sg/news/china/story20260906-9633523) ⭐️ 7.0/10

Counterpoint 数据显示，长鑫科技 2026 年第二季度全球 DRAM 营收市占率由上年同期的 4%升至 10%，排名第四。公司 2026 年上半年营收为 1503.1 亿元，同比增长 873.64%。

telegram · zaihuapd · 9月6日 06:43

**「背景」** DRAM 是用于电脑和移动设备的存储芯片；行业在 2024 年至 2025 年初一度低迷，2026 年上半年则因 AI 基础设施需求和价格上涨而回暖，为长鑫科技第二季度营收市占率升至 10%提供了市场背景。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://aiwiki.ai/wiki/cxmt">CXMT (ChangXin Memory Technologies) | AI Wiki</a></li>

</ul>
</details>

**标签**: `#semiconductors`, `#DRAM`, `#market share`, `#AI infrastructure`, `#Chinese tech`

---