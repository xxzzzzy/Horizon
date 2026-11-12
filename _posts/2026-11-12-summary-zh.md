---
layout: default
title: "Horizon Summary: 2026-11-12 (ZH)"
date: 2026-11-12
lang: zh
---

> 从 123 条内容中筛选出 18 条重要资讯。

---

**科技新闻**
1. [台积电拟向 OpenAI 和 Anthropic 投资 10 亿美元](#item-tech-news-1) ⭐️ 8.0/10
2. [DeepMind 用 AI 形式验证 Signal 关键保证](#item-tech-news-2) ⭐️ 8.0/10
3. [英伟达董事会据报考虑罢免黄仁勋](#item-tech-news-3) ⭐️ 8.0/10
4. [Google 开源 XSE，每秒处理六百万次查询](#item-tech-news-4) ⭐️ 8.0/10
5. [AlphaGenome 2 提升细胞类型特异变异预测](#item-tech-news-5) ⭐️ 8.0/10
6. [美商务部拟封堵中国 AI 远程用芯](#item-tech-news-6) ⭐️ 8.0/10
7. [aws-emulator](#item-tech-news-7) ⭐️ 7.0/10
8. [Anthropic IPO 路演披露 Claude 多芯片战略](#item-tech-news-8) ⭐️ 7.0/10
9. [《Big Walk》AI 修 bug 引发独立游戏争议](#item-tech-news-9) ⭐️ 7.0/10
10. [IBM 调整 Nighthawk 量子路线图](#item-tech-news-10) ⭐️ 7.0/10
11. [谷歌 DeepMind 发布 AlphaGenome 2，预测 DNA 变异对细胞的影响](#item-tech-news-11) ⭐️ 7.0/10
12. [OpenAI 季度营收据报首次突破 100 亿美元](#item-tech-news-12) ⭐️ 7.0/10
13. [Google 推出 Gemini Decision 1 决策 API](#item-tech-news-13) ⭐️ 6.0/10
14. [llm 0.37.2](#item-tech-news-14) ⭐️ 6.0/10

**财经新闻**
1. [美联储官员称 10 月通胀数据&quot;令人不安&quot;，期货已一致预期 12 月加息](#item-finance-news-1) ⭐️ 8.0/10
2. [离岸信托收益征税过渡期结束，累计申报超 1600 亿元](#item-finance-news-2) ⭐️ 8.0/10
3. [阿里巴巴拟分拆芯片子公司平头哥赴港上市](#item-finance-news-3) ⭐️ 7.0/10
4. [英伟达董事会据称讨论罢免黄仁勋](#item-finance-news-4) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [台积电拟向 OpenAI 和 Anthropic 投资 10 亿美元](https://arstechnica.com/ai/2026/11/taiwans-chipmaking-giant-tsmc-to-invest-1b-in-anthropic-openai/) ⭐️ 8.0/10

台积电董事会已批准最多向 OpenAI 投资 5 亿美元，认购面向大型投资者的优先股，并最多向 Anthropic 投资 5 亿美元，按后者预期 IPO 价格购买普通股。这将使台积电直接持有两家主要 AI 开发商的股份，而台积电的代工业务本已从 AI 数据中心建设中显著获益。台积电为英伟达绝大多数 AI 数据中心芯片和苹果多数定制芯片提供制造服务，主要产能位于台湾，并在日本、中国、美国亚利桑那州及德国布局。《华尔街日报》称，该交易可能提振市场对 AI 产业的信心，但分析师警告，投资者、供应商与客户之间的循环融资使真实 AI 硬件和服务需求更难判断。

rss · Ars Technica · 11月11日 18:16

**「背景」** 理解这项交易的关键，是台积电同时处于 AI 产业链的供应商和投资者位置：它为英伟达和苹果代工芯片，同时拟成为 OpenAI 与 Anthropic 的股东。投资者、供应商与客户相互注资会形成所谓“循环融资”，使订单、收入与估值相互支撑，令外界更难判断 AI 硬件和服务的真实市场需求。

**「产业影响」** 最高 10 亿美元的投资将使台积电从 OpenAI 和 Anthropic 的代工供应商变为直接股东，进一步绑定其先进制程业务与头部 AI 客户的利益。与此同时，这类供应商、投资者与客户之间的循环融资将加大外部投资者评估真实 AI 硬件需求的难度。

**标签**: `#TSMC`, `#AI investment`, `#OpenAI`, `#Anthropic`, `#semiconductors`

---

<a id="item-tech-news-2"></a>
### [DeepMind 用 AI 形式验证 Signal 关键保证](https://arstechnica.com/ai/2026/11/signals-encryption-just-passed-an-ai-powered-mathematical-checkup/) ⭐️ 8.0/10

据报道，Google DeepMind 研究人员使用代理式 AI 框架 AlphaProof Code，对 Signal 协议中的若干关键密码学保证进行了形式验证。这项耗时四周的概念验证既为 Signal 保护的通信安全性提供了额外独立验证，也展示了 AI 辅助形式证明的潜力。验证范围并未覆盖整个 Signal 移动应用；研究人员在所检查的部分未发现新漏洞，但 AlphaProof Code 分析包含已知且早已修复漏洞的旧版 Signal 时，正确识别了这些问题并判定其无法通过形式验证。研究团队将公开 Signal 分析所用的规格和证明，以供其他形式验证工作复用。

rss · Ars Technica · 11月11日 14:08

**「背景」** 形式验证通过数学规格和证明检查软件是否满足预期性质，但长期以来需要人工提炼性质、建立公式并完成证明，因此十分耗时。代理式 AI 能够显著减少其中的证明工作，不过此次成果仍只是迈向大规模软件验证的一步。

**「影响」** Signal 用户因此获得了针对部分协议保证的额外数学验证，但这并非对整个应用的安全认证。对开发者和验证社区而言，公开的规格与证明可作为后续工作的基础，但其可扩展性和实际采用成本仍未确立。

**标签**: `#formal verification`, `#AI-assisted reasoning`, `#cryptography`, `#Signal protocol`, `#AlphaProof Code`

---

<a id="item-tech-news-3"></a>
### [英伟达董事会据报考虑罢免黄仁勋](https://techcrunch.com/2026/11/11/nvidias-stock-drops-as-board-reportedly-preps-to-oust-ceo-jensen-huang/) ⭐️ 8.0/10

据报，英伟达股价因有关董事会可能罢免创始人兼 CEO 黄仁勋的消息而下跌。董事会最快可能于周三晚间决定是否撤换这位担任公司 CEO 达 33 年的负责人。若相关决定落地，将对英伟达的公司治理、战略连续性以及 AI 和半导体行业产生重大影响。不过，这一说法尚未获得证实，报道也未提供支持该消息的具体细节，因此目前只能视为未经确认的二手消息。

rss · TechCrunch · 11月11日 23:28

**「背景」** 黄仁勋创办英伟达并担任 CEO 已有 33 年，而英伟达如今是 AI 芯片与半导体产业的重要企业，因此董事会若更换他，涉及的不只是高管人事，也关系到公司治理和 AI 芯片战略的长期连续性。英伟达董事会据报道正因针对黄仁勋婚外关系的指控而准备撤换他；相关报道提到一名相关人士被美国情报机构认为是“中国间谍”，但这些说法来自媒体引述匿名知情人士，尚无英伟达官方确认。

**「潜在影响」** 若撤职真的发生，Nvidia 将立即面临创始人兼 CEO 黄仁勋离任后的继任安排，并使公司的治理及 AI 芯片战略连续性出现不确定性；但现有报道仅显示董事会正在讨论其未来，并无正式撤职决定。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.forbes.com/sites/petercohan/2026/11/11/if-jensen-huang-goes-nvidia-stock-and-the-ai-industry-may-suffer/">Nvidia Board Weighs Jensen Huang Exit as Stock Faces Risk</a></li>
<li><a href="https://www.reuters.com/world/china/view-nvidia-is-preparing-oust-ceo-jensen-huang-wsj-reports-2026-11-11/">VIEW Nvidia is preparing to oust CEO Jensen Huang, WSJ ...</a></li>
<li><a href="https://www.cbsnews.com/news/nvidia-board-ceo-jensen-huang-china/">Nvidia&#x27;s board preparing to oust CEO Jensen Huang, sources ...</a></li>
<li><a href="https://edition.cnn.com/2026/11/11/business/live-news/nvidia-jensen-huang-investigation-fallout">Scandal roils Nvidia , one of America’s most valuable companies: Live...</a></li>
<li><a href="https://www.theguardian.com/technology/live/2026/nov/12/nvidia-ceo-jensen-huang-affairs-share-price-plunges-live-latest">Nvidia board reportedly meeting to decide CEO Jensen ...</a></li>

</ul>
</details>

**标签**: `#Nvidia`, `#AI hardware`, `#semiconductors`, `#corporate leadership`

---

<a id="item-tech-news-4"></a>
### [Google 开源 XSE，每秒处理六百万次查询](https://www.theregister.com/devops/2026/11/11/google-gooses-python-ai-performance-by-removing-python/5308995) ⭐️ 8.0/10

Google 已开源高性能查询服务系统 XSE，据报道，该系统通过从关键服务路径中移除 Python 来提升性能。它在 Google 搜索、广告和 YouTube Shorts 等服务中每秒处理约 600 万次查询，表明 XSE 已用于大规模生产负载。所给材料未披露具体实现、基准测试、相对性能提升或资源开销，因此目前无法量化实际加速幅度及其可推广性。此次开源为外部审查该系统提供了基础，但其在不同工作负载下的收益仍需进一步验证。

rss · The Register · 11月11日 11:30

**「XSE 背景」** 查询服务系统负责承接海量在线请求，并将其调度到后端计算或模型资源后返回结果，因此吞吐量与调度效率会影响大型 AI 服务的扩展能力。此次 Google 开源 XSE，使其可用于搜索、广告和 YouTube Shorts 等内部服务场景，但现有摘要未说明其是否替代 Python，以及具体的实现与基准测试方法。“每秒六百万次查询”是系统吞吐规模指标，并不等同于单次响应延迟或模型性能。

**「实际影响」** 对需要以低延迟、高并发部署小型排序或嵌入模型的团队，开源的 XSE 提供了一个绕开 Python 服务层的新方案；Google 自测称其吞吐量可达最佳优化 Python 服务的 2—5 倍，并使单次预测的 CPU 消耗降低 30%—70%。不过，现有性能数据主要来自 Google 的内部环境与测试，其在生产工作负载中的实际收益仍需验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theregister.com/devops/2026/11/11/google-gooses-python-ai-performance-by-removing-python/5308995">Google gooses Python AI performance by... removing Python</a></li>
<li><a href="https://www.theregister.com/devops/2026/11/11/google-gooses-python-ai-performance-by-removing-python/5308995">Google gooses Python AI performance by... removing Python</a></li>
<li><a href="https://www.contentbuffer.com/news/google-ditches-python-xse-serving-6-million-queries-per-second-8fc73a94">Google Ditches Python for XSE, Serving 6 Million Queries Per ...</a></li>
<li><a href="https://cryptobriefing.com/google-open-sources-xla-serving-engine/">Google open sources XLA Serving Engine to run ML models ...</a></li>

</ul>
</details>

**标签**: `#AI infrastructure`, `#query serving`, `#performance optimization`, `#open source`, `#Python`

---

<a id="item-tech-news-5"></a>
### [AlphaGenome 2 提升细胞类型特异变异预测](https://deepmind.google/blog/alphagenome-2-deciphering-how-cells-read-dna-to-better-understand-disease/) ⭐️ 8.0/10

DeepMind 宣布推出下一代 DNA 序列模型 AlphaGenome 2，用于预测 DNA 序列及其变异如何影响特定人类细胞类型中的基因活动，从而帮助定位疾病相关的细胞机制。新模型采用条件式架构，将百万碱基序列与目标组织、细胞类型或状态共同输入，而不是像初代模型那样并行预测广义组织平均值；其训练数据涵盖人和小鼠的批量及单细胞数据、68 种组织和超过 1.07 亿个细胞档案，可预测基因表达、组蛋白修饰、染色质可及性和 DNA 甲基化。在包含 28 种主要免疫细胞的 TenK10K 数据集上，AlphaGenome 2 识别出的因果变异比例从 16% 提升至 30%，方向性基因效应从 23% 提升至 43%，相较经单细胞数据微调的初代 AlphaGenome 及其他专用工具表现更好，并成功重现了肠道巨噬细胞中远端调控变异通过激活 ETS2 驱动炎症性肠病的案例。研究人员还可利用仅含数十个细胞的单细胞 RNA 测序快照描述未见过的细胞状态，并借助跨模态插补预测未测量的实验指标；模型由此区分出疫苗激活的 T 细胞，并发现一项与重症 COVID-19 相关的变异在激活状态下造成的基因活动破坏更强。该模型现已通过 AlphaGenome API 面向非商业研究开放，商业研究处于私有预览阶段，但本次公告尚未提供完整的方法细节、广泛基准测试或独立验证。

rss · DeepMind Blog · 11月11日 15:00

**「背景」** 不同人体细胞通常携带相同的 DNA，但会根据自身类型和状态开启或关闭不同基因，因此同一遗传变异的调控效应可能只在特定细胞中显现。DeepMind 去年推出的初代 AlphaGenome 主要在广泛组织尺度上预测 DNA 变体对分子活性的影响，随后通过 AlphaGenome Atlas 扩展到人类基因组中的 90 亿种单字母替换。AlphaGenome 2 在此基础上转向以组织、细胞类型或状态为条件的建模，并引入大规模单细胞数据，以捕捉更精细的基因调控关系。

**「实际影响」** 对遗传学和疾病研究人员而言，AlphaGenome 2 可通过非商业 API 在数百种人类细胞与组织条件下预测变异效应；DeepMind 报告其在 TenK10K 数据集上识别出 30% 的因果变异和 43% 的方向性基因效应，高于原版 AlphaGenome 微调模型的 16% 和 23%，有助于更快筛选宽泛组织模型可能遗漏的疾病候选位点。商业研究目前仍处于私有预览阶段，且这些性能数字来自发布方公告，尚不代表独立验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepmind.google/blog/alphagenome-2-deciphering-how-cells-read-dna-to-better-understand-disease/">AlphaGenome 2 : Deciphering how cells read... — Google DeepMind</a></li>
<li><a href="https://storage.googleapis.com/deepmind-media/papers/alphagenome.pdf">AlphaGenome : advancing regulatory variant</a></li>
<li><a href="https://www.biorxiv.org/content/10.1101/2025.06.25.661532v1.full.pdf">AlphaGenome : advancing regulatory variant effect prediction with...</a></li>
<li><a href="https://deepmind.google/blog/alphagenome-2-deciphering-how-cells-read-dna-to-better-understand-disease/">AlphaGenome 2 : Deciphering how cells read... — Google DeepMind</a></li>

</ul>
</details>

**标签**: `#AI for science`, `#DNA sequence modeling`, `#human genetics`, `#single-cell biology`, `#disease research`

---

<a id="item-tech-news-6"></a>
### [美商务部拟封堵中国 AI 远程用芯](https://www.theinformation.com/articles/commerce-department-finalizing-long-awaited-ai-remote-access-rule) ⭐️ 8.0/10

据 The Information 报道，美国商务部正与相关政府机构磋商并敲定一项规则，拟阻止中国 AI 公司通过境外数据中心远程使用受限制的先进 AI 芯片，最早可能在报道所述当月公布。拟议规则将现有半导体出口限制扩展至包括马来西亚、新加坡和泰国在内的七个国家，同时封堵远程访问与芯片走私漏洞。白宫此前已要求国会立法，要求商务部制定该规则；英伟达则游说反对封堵远程访问路径，并主张美国 AI 基础设施需要在全球市场保持竞争力。规则尚未定稿，具体条文、实施细节及适用范围仍有待官方公布确认。

telegram · zaihuapd · 11月12日 03:42

**「远程用芯与规则背景」** 这里的“远程用芯”是指中国 AI 公司不直接取得受限芯片，而是通过境外数据中心远程调用先进 AI 芯片的算力。拟议规则针对现有半导体出口限制对这一使用路径的覆盖不足，并拟将管制延伸至马来西亚、新加坡、泰国等七个国家；白宫此前要求国会立法推动制定规则，英伟达则曾游说反对封堵这一缺口。规则仍在与其他政府机构协商定稿，具体覆盖范围、实施时间及法律细节尚待商务部正式公布。

**「中国企业远程算力受限」** 若规则按报道落地，中国 AI 公司将无法通过马来西亚、新加坡、泰国等七国的境外数据中心远程使用受限制的先进 AI 芯片，需调整算力采购和云服务布局；但最终条文、芯片覆盖范围及实施日期尚未公布。

**标签**: `#AI芯片`, `#出口管制`, `#算力基础设施`, `#东南亚`, `#Nvidia`

---

<a id="item-tech-news-7"></a>
### [aws-emulator](https://simonwillison.net/2026/Nov/11/aws-emulator/) ⭐️ 7.0/10

AWS has released an official Rust-based emulator for testing against local clones of multiple services without provisioning paid API access.

rss · Simon Willison · 11月11日 21:18

**标签**: `#AWS`, `#software testing`, `#cloud emulation`, `#Rust`, `#AI coding agents`

---

<a id="item-tech-news-8"></a>
### [Anthropic IPO 路演披露 Claude 多芯片战略](https://simonwillison.net/2026/Nov/11/anthropic-ipo-roadshow/) ⭐️ 7.0/10

Anthropic 在 IPO 路演视频中表示，公司已在 AWS Trainium、Google TPU、NVIDIA GPU 和 AMD GPU 上训练并服务 Claude；这种多芯片战略需要为每类芯片分别定制软件栈和推理栈，成本高昂且开发困难。公司称，2026 年首次接入 AMD GPU 时由 Mythos 尝试移植，三天内便让 Claude 在其上运行，几乎无需人工干预，Claude 移植或编写了近 100% 的内核，而以往引入新芯片平台需要数十名工程师工作数月。Anthropic 还把“有效算力”定义为物理算力与一系列“计算乘数”的乘积，并举例称 4 倍乘数可把训练同一模型所需的物理算力从 100 单位降至 25 单位，或用 100 单位训练此前需要 400 单位的更强模型。公司进一步预期 Claude 能在递归自我改进中自主发现更多计算乘数；不过，这些技术数字和前景判断属于路演中的公司陈述，且 Simon Willison 提供的非官方文字稿由 MacWhisper 提取，并非 Anthropic 官方文本。

rss · Simon Willison · 11月11日 15:11

**「多芯片与计算乘数」** Anthropic 的多芯片战略，是让 Claude 的训练和线上推理覆盖 AWS Trainium、Google TPU、NVIDIA GPU 与 AMD GPU，而不是绑定单一硬件平台；由于每类芯片都需要定制软件栈和推理栈，这会显著增加工程成本。公司所说的“计算乘数”是指通过软硬件优化提高物理算力的有效产出，例如 4 倍乘数可让同一模型少用约四分之三的物理算力，或用同等物理资源训练更强模型；Anthropic 进一步声称 Claude 最终可自行发现这类乘数。该方向此前已有迹可循：Anthropic 在 9 月发布的事故复盘中提到过仅影响 TPU 部署的故障，而 IPO 文件也未公布四类芯片各自的算力占比。

**「降低算力供应商锁定风险」** Anthropic 的多芯片策略把新增 AMD 平台适配从以往需要数十名工程师数月的工作缩短到借助 Mythos 在三天内完成（Claude 移植或编写了近 100% 的内核），并使其可结合 AWS Trainium2、Google TPU 和 NVIDIA 的大规模产能来分散单一供应商风险、增强容量保障。现有资料将其定位为面向 Trainium2/TPU 的百万芯片级部署，但路演未披露成本、吞吐量或 Claude 用户可感知的服务指标，因此实际价格与可用性收益仍未得到量化。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tomshardware.com/tech-industry/artificial-intelligence/anthropics-ipo-filing-shows-most-of-its-compute-goes-to-r-and-d-not-serving-customers-company-details-massive-usd800-billion-in-tpu-and-gpu-contracts">Anthropic ’s IPO filing shows most of its compute... | Tom &#x27;s Hardware</a></li>
<li><a href="https://www.datacenterfrontier.com/machine-learning/article/55335703/inside-anthropics-multi-cloud-ai-factory-how-aws-trainium-and-google-tpus-shape-its-next-phase">Inside Anthropic’s Multi-Cloud AI Factory: How AWS Trainium ...</a></li>
<li><a href="https://convergedigest.com/anthropic-infrastructure-roadmap-s1-filing/">What Anthropic’s S-1 Reveals About Data Centers, Chips and ...</a></li>
<li><a href="https://www.cognativ.com/blog/anthropic-google-cloud-200b-deal/">Anthropic and Google Cloud $200B Deal Analysis | Cognativ</a></li>

</ul>
</details>

**标签**: `#Anthropic`, `#AI hardware`, `#model infrastructure`, `#AI accelerators`, `#IPO`

---

<a id="item-tech-news-9"></a>
### [《Big Walk》AI 修 bug 引发独立游戏争议](https://arstechnica.com/gaming/2026/11/big-walk-used-ai-to-fix-a-bug-now-the-indie-gaming-world-is-having-a-reckoning/) ⭐️ 7.0/10

独立游戏《Big Walk》开发商 House House  belatedly 公开承认，开发末期曾少量使用大语言模型排查技术难题和 bug，相关代码占比“远低于 0.1%”。问题源于一个会导致部分情境下阴影长度“无限”的 Unity 引擎 bug；尽管 Unity 工程师判断无法修复，聊天机器人提出的方案仍经开发者大幅修改，最终形成游戏中的 10 行代码，也有社交媒体用户称该问题可通过大量人工努力解决。独立游戏节（IGF）50 多名评审中有 19 人公开宣布，拒绝为任何以任何方式使用生成式 AI 的游戏投票，并呼吁 IGF 推行全面禁止 AI 生成内容的政策。此次风波源于参选游戏中使用生成式 AI 工具的作品明显增加，评审列举了其在生态、经济、心理和劳工方面的影响。

rss · Ars Technica · 11月11日 17:37

**「背景」** 独立游戏节（Independent Games Festival，IGF）是面向独立游戏开发者的重要评选活动，其评审规则会影响开发者对制作工具和披露政策的取舍。近年来，游戏行业围绕生成式 AI 在美术、代码等开发环节的使用及其是否应向玩家披露一直存在争议；本次事件中，19 名 IGF 评审员公开表示拒绝为任何使用生成式 AI 的游戏投票，并要求 IGF 制定更严格的禁限政策。House House 随后披露，《Big Walk》仅在开发后期借助大语言模型排查 Unity 引擎导致的阴影卡顿问题，涉及代码不足总代码量的 0.1%，但这一有限使用仍使该作成为上述政策分歧的焦点。

**「行业影响」** 《Big Walk》即使仅让生成式 AI 参与了“远低于 0.1%”的最终代码，也将失去 19 名独立游戏节评委的选票，从而削弱其获奖机会，并增加其他使用生成式 AI 的独立游戏开发者参奖时面临的披露与评审阻力。由于独立游戏节尚未正式通过全面禁令、Steam 也不要求披露代码或聊天机器人使用情况，具体影响仍取决于其余评委和主办方规则。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arstechnica.com/gaming/2026/11/big-walk-used-ai-to-fix-a-bug-now-the-indie-gaming-world-is-having-a-reckoning/">Big Walk used AI to fix a bug. Now the indie gaming world is ...</a></li>
<li><a href="https://godisageek.com/2026/11/big-walk-ai-use-igf-jurors/">House House Reveals Big Walk AI Use as IGF Jurors Push Back</a></li>
<li><a href="https://insider-gaming.com/big-walk-devs-issue-statement-regarding-ai-usage-following-award-controversy/">Big Walk Devs Issue Statement Regarding AI Usage Following ...</a></li>
<li><a href="https://www.eurogamer.net/house-house-big-walk-generative-ai-development">Under pressure, Big Walk studio reveals it used generative AI ...</a></li>
<li><a href="https://www.pcgamer.com/games/puzzle/big-walk-developer-reveals-it-used-generative-ai-sparingly-estimates-well-under-0-1-percent-was-actually-coded-using-llms/">Big Walk developer reveals it used generative AI ... | PC Gamer</a></li>

</ul>
</details>

**标签**: `#generative AI`, `#game development`, `#AI disclosure`, `#industry policy`, `#independent games`

---

<a id="item-tech-news-10"></a>
### [IBM 调整 Nighthawk 量子路线图](https://arstechnica.com/science/2026/11/ibm-to-offer-access-to-a-dual-processor-quantum-system-in-2027/) ⭐️ 7.0/10

IBM 在量子开发者大会上更新路线图，计划在 2027 年向用户提供两个互联的 Nighthawk 处理器，并将多处理器互联规模从原计划的九套缩减为两套。Nighthawk 将新增一个拥有 500 多个可编程量子比特的版本，但 2027 年规划中的量子比特总数不变，变化主要体现在架构和功能扩展上。IBM 称，9 月发布的 Nighthawk 通过硬件级量子比特重置获得性能提升，但现有内容未提供独立性能数据。其纠错路线分为两条并行路径：一条研发构建纠错硬件所需的技术，目标是在 2030 年前实现纠错量子计算机；另一条面向用户，以通用型处理器支持当前的算法测试。面向公众的 Nighthawk 现有版本包含 120 个硬件量子比特，预计约执行 5,000 次门操作后错误便难以忽视，因此 2028 年该路线主要通过修订现有处理器继续推进。

rss · Ars Technica · 11月11日 16:33

**「背景：IBM 的并行量子计算路线」** 量子纠错通过量子纠错码把多个物理量子比特组合成逻辑量子比特；物理量子比特的错误率必须足够低，才能在错误不断累积前将其识别和纠正。IBM 的路线图分为两条并行路径：一条测试构建容错硬件所需的技术，另一条提供面向近期算法测试的通用处理器 Nighthawk。由于纠错码要求特定数量和几何连接方式的物理量子比特，并需要额外的辅助量子比特，直接在未纠错的硬件上运行算法未必能获得最佳结果。

**「实际影响」** 对计划在 2027 年使用 IBM 量子系统进行算法测试的开发者而言，路线图调整将提供两台互连的 Nighthawk 处理器，其中可扩展版本达到 520 个量子比特、两台合计 1,040 个量子比特，并通过硬件级量子比特复位提升处理器性能。原计划互连九台缩减为两台且总规划量子比特数不变，表明 IBM 正以单机容量和近期可用性换取较少的多机扩展；不过这些仍是 2027 年目标，实际互连收益与性能改善尚待验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arstechnica.com/science/2023/12/ibm-adds-error-correction-to-updated-quantum-computing-roadmap/">IBM releases 1,000+ qubit processor , roadmap to error correction</a></li>
<li><a href="https://www.ibm.com/roadmaps/quantum/2026/">Quantum 2026 — IBM Technology Atlas</a></li>
<li><a href="https://shiftdelete.net/en/ibm-nighthawk-r3">IBM Nighthawk r3: 520 Qubits , 1,040- Qubit System in 2027</a></li>

</ul>
</details>

**标签**: `#quantum-computing`, `#hardware`, `#error-correction`, `#IBM`

---

<a id="item-tech-news-11"></a>
### [谷歌 DeepMind 发布 AlphaGenome 2，预测 DNA 变异对细胞的影响](https://www.theverge.com/ai-artificial-intelligence/1031524/google-deepmind-alphagenome-2-genetic-ai-model) ⭐️ 7.0/10

Google DeepMind 的研究人员发布了新的人工智能模型 AlphaGenome 2，用于预测 DNA 的变化如何影响不同细胞类型中的基因活性。模型的出发点是为科学家提供一个更细致、更难以企及的观察视角，帮助理解 DNA 变异在不同细胞中的具体作用，其中可能包含疾病成因的关键线索，并为新疗法的研发指明方向。AlphaGenome 2 是此前 AlphaGenome 模型的后继迭代版本。目前公开的报道篇幅简短，尚未披露模型的技术细节、性能基准数据，也没有说明其在方法层面相较前代是否有实质性的新突破。

rss · The Verge · 11月11日 15:00

**「背景」** 此前，Google DeepMind 于 2025 年 6 月 25 日发布初代 AlphaGenome，用于预测单碱基变异或突变如何影响调控基因的多种生物过程；该模型统一了多模态预测、长序列上下文和碱基对分辨率，可处理约 1 Mb 的 DNA 序列。Google 将其定位为连接基因组“蓝图”与基因调控“控制面板”的工具，而 AlphaGenome 2 延续这一方向，并进一步考察 DNA 变化对不同细胞类型的影响。

**「实际影响」** AlphaGenome 2 可预测特定人类细胞类型中 DNA 序列及变异的影响，并判断变异可能发挥作用的细胞类型，从而帮助研究人员定位疾病机制和寻找治疗方向。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepmind.google/science/alphagenome/">AlphaGenome — Google DeepMind</a></li>
<li><a href="https://www.nature.com/articles/s41586-025-10014-0">Advancing regulatory variant effect prediction with AlphaGenome</a></li>
<li><a href="https://deepmind.google/blog/alphagenome-ai-for-better-understanding-the-genome/">AlphaGenome: AI for better understanding the genome</a></li>
<li><a href="https://www.nature.com/articles/d41586-026-03673-0">DeepMind&#x27;s ultra-powerful AI for genome mapping wows ...</a></li>
<li><a href="https://deepmind.google/blog/alphagenome-2-deciphering-how-cells-read-dna-to-better-understand-disease/">AlphaGenome 2: Deciphering how cells read DNA to better ...</a></li>

</ul>
</details>

**标签**: `#AlphaGenome`, `#Google DeepMind`, `#genomics`, `#AI for science`, `#bioinformatics`

---

<a id="item-tech-news-12"></a>
### [OpenAI 季度营收据报首次突破 100 亿美元](https://techcrunch.com/2026/11/11/openais-quarterly-revenue-reportedly-crosses-10b-for-the-first-time/) ⭐️ 7.0/10

据 TechCrunch 报道，OpenAI 的季度营收首次超过 100 亿美元，较第二季度的 67 亿美元增长近 50%。这一里程碑表明 OpenAI 的业务规模正在显著扩大，也是头部 AI 企业商业化进展的重要指标。不过，现有报道未披露收入构成、统计口径或公司确认等支持细节，因此该数字的可核验性仍有限。

rss · TechCrunch · 11月11日 16:14

**「背景」** 报道中的“季度收入”指 OpenAI 在一个三个月周期内实现的营收，而非年化收入。此前 2026 年第二季度营收为 67 亿美元；同期收入同比增长 18%，但经营亏损扩大至 123 亿美元，因此此次突破更多体现销售规模增长，并不代表公司已经实现盈利。

**「商业化影响」** 对开发者和企业采购方而言，OpenAI 单季营收据报首次突破 100 亿美元、较第二季度的 67 亿美元增长近 50%，使其商业规模成为模型能力、价格和供应商连续性之外的直接选型指标；另有材料显示 Anthropic 2026 年第二季度营收达到 109 亿美元，表明头部 AI 实验室已进入相近的营收量级。现有信息未披露收入确认口径、利润或现金流，因此这些数字能证明商业规模扩张，但不能证明 OpenAI 已实现盈利或在市场竞争中最终领先。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://sfg.media/en/a/anthropic-surpasses-openai-quarterly-revenue/">Anthropic Surpassed OpenAI in Quarterly Revenue for the First Time ...</a></li>
<li><a href="https://siliconvalleyconfidential.com/en/dossier/karpathy-900-billion-and-a-first-profit/">Karpathy, $900 Billion , and a First Profit — Silicon Valley Confidential</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#AI industry`, `#revenue growth`, `#business metrics`

---

<a id="item-tech-news-13"></a>
### [Google 推出 Gemini Decision 1 决策 API](https://simonwillison.net/2026/Nov/11/gemini-decisions-api/) ⭐️ 6.0/10

2026 年 11 月，Google 推出 Gemini Decision 1 API，面向是/否、选项选择和按评分量表打分三类决策任务，并沿用 Jev 对是/否问题所用的“Noul”称谓。它与 OpenAI 的 GPT-6 Luna 决策模型定价相同，每百万输入 token 收取 0.10 美元且输出免费；Jev 的输入价则更低，为每百万 token 4.2 美分。相比仅支持文本与 JSON 的 Jev 和支持文本与图像的 OpenAI，Gemini Decision 1 覆盖文本、图像、音频、视频和 PDF。Simon Willison 用机器人视频测试时，模型对“有机器人”和“在美国”给出约 0.923 的概率，对“有龙”和“在法国”分别给出约 0.050 和 0.083，但原文没有提供基准测试或三者的准确率对比。

rss · Simon Willison · 11月11日 22:03

**「决策模型 API」** 这里的“决策模型”指专门对一组问题给出可结构化判断的接口，而不是像聊天模型那样生成开放式回答：Gemini Decision 1 支持 yes/no、choice 和 rubric-scoring 三类问题，单次调用最多评估 1,000 个问题，并返回概率或评分。它在输入范围上覆盖文本、图像、音频、视频和 PDF；相比仅支持文本/JSON 的 Jev，以及支持文本和图像的 OpenAI 方案，Gemini Decisions API 将多模态判断作为核心能力。

**「影响」** 开发者可以用与 GPT-6 Luna 相同的输入价格将多模态材料接入结构化决策任务，但 Jev 仍具成本优势，且现有测试不足以判断哪种模型更准确。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/technology/developers-tools/gemini-decisions-api/">Gemini Decisions API: Fast multimodal decisions - The Keyword</a></li>

</ul>
</details>

**标签**: `#Gemini API`, `#decision models`, `#multimodal AI`, `#LLM pricing`

---

<a id="item-tech-news-14"></a>
### [llm 0.37.2](https://simonwillison.net/2026/Nov/11/llm/) ⭐️ 6.0/10

LLM 0.37.2 addresses two API-key disclosure vulnerabilities involving configuration of external OpenAI-compatible endpoints.

rss · Simon Willison · 11月11日 17:19

**标签**: `#LLM`, `#security`, `#API keys`, `#OpenAI-compatible APIs`, `#software releases`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [美联储官员称 10 月通胀数据&quot;令人不安&quot;，期货已一致预期 12 月加息](https://www.cnbc.com/2026/11/11/goolsbee-october-inflation-fed-rates-disturbing-distressing.html) ⭐️ 8.0/10

芝加哥联储主席奥斯坦·古尔斯比称 10 月通胀报告&quot;令人不安&quot;：美国消费者价格指数环比上涨 0.4%（季调），高于经济学家预期，且为连续第三个月大幅上涨，多位美联储官员因此表示可能需要更果断地加息。联邦基金利率期货目前一致预期美联储在 12 月会议上加息，其中加息 50 个基点的概率为 15%；美联储 9 月已加息 25 个基点至 3.75%—4%，10 月按兵不动，最终决定尚未作出。

rss · CNBC Finance · 11月11日 16:49

**「背景」** 美联储 9 月加息 25 个基点后，将联邦基金利率目标区间设在 3.75%—4%，并在 10 月维持不变；下一次议息会议定于 12 月 8 日至 9 日。

**「市场影响」** 更热的美国通胀数据及美联储更大幅度加息的预期推动美债收益率和美元走高，并导致黄金、白银价格下跌，使贵金属投资者面临直接的价格压力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.gate.com/blog/fed-december-rate-hike-odds-hit-100-is-50-bps-next">Fed December Rate Hike Odds Hit 100%: Is 50 Bps Next? | Gate Blog</a></li>
<li><a href="https://www.kitco.com/news/article/2026-11-10/gold-silver-plunge-hotter-us-inflation-raises-prospect-larger-fed-rate-hike">Gold, silver plunge as hotter U . S . inflation raises... | Kitco News</a></li>

</ul>
</details>

**标签**: `#Federal Reserve`, `#inflation`, `#interest rates`, `#monetary policy`

---

<a id="item-finance-news-2"></a>
### [离岸信托收益征税过渡期结束，累计申报超 1600 亿元](https://www.news.cn/20261111/9bcce99c779b4a6197ff45bbbc3e4c50/c.html) ⭐️ 8.0/10

税务总局 11 月 11 日表示，离岸信托收益征税 90 天过渡期已平稳结束，累计申报个人所得税超过 1600 亿元，其中 10 月入库超 1200 亿元，带动 10 月全国个人所得税收入增长近 90%。2026 年 7 月 24 日，财政部、税务总局公告明确，过渡期内完成申报缴税不加收滞纳金。未主动申报或申报不实的将被督促补缴并加收滞纳金，仍不改正的将依法立案稽查。

telegram · zaihuapd · 11月11日 10:35

**标签**: `#离岸信托`, `#个人所得税`, `#税收政策`, `#财政收入`, `#税务稽查`

---

<a id="item-finance-news-3"></a>
### [阿里巴巴拟分拆芯片子公司平头哥赴港上市](https://www.cnbc.com/2026/11/11/alibaba-pr.html) ⭐️ 7.0/10

阿里巴巴宣布计划分拆人工智能芯片子公司平头哥，并在香港公开发行其股份；上市仍须香港交易所和中国证监会批准，上市日期及发行规模均未披露。

rss · CNBC Finance · 11月11日 07:47

**「背景」** 阿里巴巴已于 9 月 11 日秘密提交 T-Head 赴港上市申请；这家全资子公司研发“镇武”系列 AI 芯片，反映中国企业在美国芯片出口限制下寻求本土替代。

**「潜在影响」** 若获批上市，T-Head 将获得独立融资渠道，为阿里巴巴投入国产 AI 芯片研发提供资金；但上市日期和规模尚未披露，实际融资效果仍不确定。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/11/11/alibaba-pr.html">Alibaba announces plans to list T - Head , its Nvidia chip rival</a></li>
<li><a href="https://www.scmp.com/business/companies/article/3373974/alibaba-chip-unit-t-head-files-hong-kong-ipo-plan-amid-chinas-ai-self-sufficiency-drive">Alibaba chip unit T - Head files for Hong Kong IPO amid China’s AI push</a></li>
<li><a href="https://www.investing.com/news/stock-market-news/alibaba-advances-hong-kong-ipo-plans-for-chip-subsidiary-thead-5015307">Alibaba advances Hong Kong IPO plans for chip subsidiary T - Head ...</a></li>
<li><a href="https://www.cnbc.com/2026/11/11/alibaba-pr.html">Alibaba announces plans to list T - Head , its Nvidia chip rival</a></li>
<li><a href="https://www.scmp.com/business/companies/article/3373974/alibaba-chip-unit-t-head-files-hong-kong-ipo-plan-amid-chinas-ai-self-sufficiency-drive">Alibaba chip unit T - Head files for Hong Kong IPO amid China’ s AI push</a></li>

</ul>
</details>

**标签**: `#Alibaba`, `#T-Head`, `#Hong Kong IPO`, `#AI semiconductors`, `#China tech`

---

<a id="item-finance-news-4"></a>
### [英伟达董事会据称讨论罢免黄仁勋](https://www.wsj.com/business/nvidia-is-preparing-to-oust-nvidia-ceo-jensen-huang-30f421ad?mod=tech_lead_pos2) ⭐️ 7.0/10

据《华尔街日报》援引的报道，英伟达董事会正讨论罢免首席执行官黄仁勋，最早可能于当天开会决定其去留，英伟达尚未正式回应。消息传出后，英伟达股价盘后下跌约 8%；报道涉及的婚外关系及中国情报机构关联指控尚未获证实。

telegram · zaihuapd · 11月11日 23:39

**「背景」** 此前，英伟达董事会已宣布对有关黄仁勋婚外关系及据称遭外国情报机构针对的报道展开独立调查；有关罢免的具体决定尚未得到英伟达正式确认。

**「直接影响」** 持有英伟达股票的投资者成为直接受影响者：报道后股价盘后下跌约 8%，但英伟达尚未确认董事会拟罢免黄仁勋，因此目前反映的是市场对潜在最高管理层变动的即时重估，而非罢免已经落地。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.wsj.com/tech/ai/nvidias-board-to-investigate-reports-that-jensen-huang-was-spying-target-c630325e">Nvidia’s Board Investigates Reports That CEO Jensen Huang Was ...</a></li>
<li><a href="https://finance.yahoo.com/markets/stocks/articles/nvidia-stock-falls-7-report-225154315.html?fr=sycsrp_catchall">Nvidia stock falls 8% after report board is preparing to oust ...</a></li>
<li><a href="https://finance.yahoo.com/markets/stocks/articles/nvidias-stock-dives-board-weighs-234215054.html?fr=sycsrp_catchall">Nvidia&#x27;s stock dives as board weighs move to oust Jensen Huang Nvidia board meets to decide CEO Huang&#x27;s future as leadership ... Nvidia Stock Plunges As Board Weighs Ousting Billionaire CEO ... Nvidia shares fall 8% after hours as its board is reportedly ... Nvidia Board Weighs Ousting Jensen Huang as Shares Slide 8 ...</a></li>

</ul>
</details>

**标签**: `#英伟达`, `#黄仁勋`, `#公司治理`, `#高管变动`, `#半导体`

---