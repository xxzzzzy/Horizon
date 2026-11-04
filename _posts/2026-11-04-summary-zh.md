---
layout: default
title: "Horizon Summary: 2026-11-04 (ZH)"
date: 2026-11-04
lang: zh
---

> 从 128 条内容中筛选出 19 条重要资讯。

---

**科技新闻**
1. [PostgreSQL 内部机制与版本行为指南](#item-tech-news-1) ⭐️ 8.0/10
2. [Postman 被指静默自动安装 AI 插件并共享 API 数据](#item-tech-news-2) ⭐️ 8.0/10
3. [BlackX UEFI 引导套件感染已修补的 Windows](#item-tech-news-3) ⭐️ 8.0/10
4. [纽约时报等诉 Brave 绕过付费墙并向 AI 供数](#item-tech-news-4) ⭐️ 7.5/10
5. [本地 Qwen 3.8 27B 可解读模型权重](#item-tech-news-5) ⭐️ 7.0/10
6. [Mac 数据中心级构建的工程挑战](#item-tech-news-6) ⭐️ 7.0/10
7. [飞机背景声可泄露视频位置](#item-tech-news-7) ⭐️ 7.0/10
8. [俄数据中心地下化应对袭击](#item-tech-news-8) ⭐️ 7.0/10
9. [Google 关闭感染逾 130 万台 Android 电视盒子的 x.cpe 僵尸网络](#item-tech-news-9) ⭐️ 7.0/10
10. [币安披露 63 亿美元加密货币失窃攻击链](#item-tech-news-10) ⭐️ 7.0/10
11. [CrowdStrike 斥资近 5 亿美元收购两家 AI 安全初创公司](#item-tech-news-11) ⭐️ 7.0/10
12. [树莓派 16GB Pi 5 再涨价](#item-tech-news-12) ⭐️ 7.0/10
13. [OpenVDDK 开源替代 VMware 未公开迁移工具](#item-tech-news-13) ⭐️ 7.0/10
14. [StateBench：长文档状态跟踪评测](#item-tech-news-14) ⭐️ 7.0/10
15. [Google Antigravity 的智能体化学信息学工作流](#item-tech-news-15) ⭐️ 7.0/10
16. [Palette：让小型开放权重模型按组织设计语言生成幻灯片](#item-tech-news-16) ⭐️ 6.0/10
17. [机器学习与 AI 在精准医学预测建模中的应用](#item-tech-news-17) ⭐️ 6.0/10

**财经新闻**
1. [财报发布后美股盘前个股分化](#item-finance-news-1) ⭐️ 7.0/10
2. [黑石称 AI 建设需增加股权融资](#item-finance-news-2) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [PostgreSQL 内部机制与版本行为指南](https://www.interdb.jp/pg/index.html) ⭐️ 8.0/10

这是一份面向数据库工程师的 PostgreSQL 实现级参考，系统讲解存储、并发控制、索引和版本相关行为，重点涉及 HoT 更新、zHeap/TOAST、SSI 与 MVCC。评论者特别提醒 PostgreSQL 18 的全文检索会通过集群默认排序规则提供程序读取词典和配置，因此使用 ICU 或内置 PG\_UNICODE\_FAST 的集群可能需要重建 FTS 与 pg\_trgm 索引；此外，非确定性排序规则下的 LIKE 不再一律报错。该资源是可供长期查阅的技术指南，而不是 PostgreSQL 18 的一次重大发布公告。

hackernews · ibobev · 11月3日 21:51 · [社区讨论](https://news.ycombinator.com/item?id=50358702)

**「相关背景」** PostgreSQL 使用多版本并发控制（MVCC）保存行的多个版本，因此更新通常会写入新的行版本，而不是原地覆盖旧版本。当更新未修改任何带索引的列，且新版本仍能放入同一数据页时，堆元组更新（HOT）可减少索引维护开销，但旧版本最终仍需由清理机制回收。《The Internals of PostgreSQL》将这些存储、并发控制和索引机制整理为实现级参考，有助于理解不同 PostgreSQL 版本的行为差异与实际调优取舍。

**「实际影响」** 数据库工程师和运维人员可借此判断 HOT 更新为何生效或失效、排查并发与存储行为，并评估 PostgreSQL 18 升级后的全文检索、pg\_trgm 索引及排序规则兼容性。

**「社区讨论」** 多位评论者认为 HoT 章节最具直接实用价值：只有未修改索引列且新元组能留在同一页时才会使用 HOT，较低的 fillfactor 可改善其适用概率，而对比 n\_tup\_hot\_upd 与 n\_tup\_upd 可检查更新是否走 HOT。讨论还强调结合 SSI、zHeap/TOAST 理解 PostgreSQL 的并发实现，并指出该资料没有覆盖 OrioleDB 等较新的 MVCC 路径。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.interdb.jp/pg/">interdb . jp / pg</a></li>
<li><a href="https://www.postgresql.org/docs/current/storage-hot.html">PostgreSQL : Documentation: 18 : 66.7. Heap -Only Tuples ( HOT )</a></li>

</ul>
</details>

**标签**: `#postgresql`, `#database-internals`, `#mvcc`, `#concurrency`, `#indexing`

---

<a id="item-tech-news-2"></a>
### [Postman 被指静默自动安装 AI 插件并共享 API 数据](https://github.com/postmanlabs/postman-app-support/issues/14370) ⭐️ 8.0/10

Postman 支持仓库中的一项 issue 指称，该工具在未明确告知用户的情况下自动安装 AI 插件，并可能把 API 请求数据发送至其服务器。社区用户称，模板变量（如 \{\{some\_secret\}\}）中的真实密钥会随查询参数一并上传，而阻断相关日志端点可能导致应用无法正常工作；不过相关行为的实际范围和意图尚未查明。另有医疗行业用户表示，其团队因安全与合规顾虑已停用 Postman 并转用 Bruno。

hackernews · sidgarimella · 11月3日 17:22 · [社区讨论](https://news.ycombinator.com/item?id=50354960)

**标签**: `#Postman`, `#API security`, `#data privacy`, `#AI plugins`, `#developer tools`

---

<a id="item-tech-news-3"></a>
### [BlackX UEFI 引导套件感染已修补的 Windows](https://arstechnica.com/security/2026/11/uefi-bootkit-infected-fully-patched-windows-machines-is-microsoft-to-blame/) ⭐️ 8.0/10

Ars Technica 报道称，BlackX UEFI 引导套件感染了已安装微软相关修复的 Windows 组织；此前，BlackLotus 于 2023 年成为首个有公开记录、可在完全更新的 Windows 11 系统上绕过 Secure Boot 的在野 UEFI 引导套件。BlackLotus 和 BlackX 都利用 Windows 启动管理器中的“Baton Drop”逻辑缺陷 CVE-2022-21894，在 Windows 完全加载及多数安全防御启动前运行恶意代码，并可能绕过 Secure Boot、在特定条件下提取 BitLocker 加密密钥。微软已于 2022 年修补该漏洞，又在 2023 年加入不再信任易受攻击启动管理器的新证书，并于 2024 年提供撤销旧启动管理器签名证书信任的机制，但受感染组织已经安装这些更新。文章原本将进一步解释 BlackX 如何突破这些防线，但提供的节选在完整攻击链及微软责任的根因说明之前被截断，因此无法据此判定责任归属。

rss · Ars Technica · 11月3日 16:03

**「UEFI 启动链与 Secure Boot」** UEFI（统一可扩展固件接口）是在计算机开机后、操作系统加载前运行的固件，负责初始化硬件并加载系统；Windows 的启动管理器（boot manager）会从专用分区启动操作系统。Secure Boot 通过验证启动软件的数字签名建立信任链，以阻止未经授权的启动代码运行，但 BlackLotus 和 BlackX 利用了 Windows 启动管理器中的“Baton Drop”逻辑缺陷（CVE-2022-21894），从而绕过这一机制；该漏洞于 2022 年公开并修复。

**「安全影响」** 已安装全部相关更新的组织仍遭感染，表明这些 Windows 侧修复未能单独阻止 BlackX 在操作系统加载前建立恶意执行链。由于现有节选缺少完整攻击链，尚不能确定问题源于微软的实现缺陷、证书处置延迟，还是 BlackX 采用了不同的绕过路径。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arstechnica.com/security/2026/11/uefi-bootkit-infected-fully-patched-windows-machines-is-microsoft-to-blame/">UEFI bootkit infected fully patched Windows machines. Is ...</a></li>

</ul>
</details>

**标签**: `#UEFI security`, `#bootkits`, `#Windows security`, `#Secure Boot`, `#malware analysis`

---

<a id="item-tech-news-4"></a>
### [纽约时报等诉 Brave 绕过付费墙并向 AI 供数](https://arstechnica.com/tech-policy/2026/11/nyt-demands-brave-shut-down-its-paywall-blocker-and-end-deals-with-ai-firms/) ⭐️ 7.5/10

《纽约时报》联合多家报纸在美国纽约南区联邦地区法院起诉 Brave Software，指控其绕过新闻网站付费墙、抓取受版权保护的内容，并通过搜索索引和 API 未经出版商许可向 AI 企业提供新闻。诉状称，Anthropic、Perplexity、Mistral、xAI 和 Cohere 等生成式 AI 公司付费使用 Brave 索引中的实时内容，用于训练模型及回答用户查询；Brave 官网则表示，其 Brave Search API 正被 Cohere、Mistral、Perplexity 和 You.com 等 AI 客户使用。原告还称，Brave 浏览器内置的付费墙绕过设置在启用后可向用户提供受限内容、屏蔽原站广告并改用 Brave 广告，同时从用户分成中获利；诉状援引第三方营收估算称，Brave 借此获得超过 1 亿美元，而出版商未获报酬。案件指控 Brave 构成直接侵权、帮助侵权和替代侵权，并违反《数字千年版权法》关于规避技术措施的规定，《纽约时报》要求其停止相关行为，但这些目前均属尚未经法院审理和认定的诉讼主张。

rss · Ars Technica · 11月3日 18:30

**「技术与法律背景」** Brave Search 通过抓取网页建立搜索索引，并经由 Brave Search API 向合作方提供实时网页内容；诉讼称，这些机制会将新闻报道送入外部 AI 公司的检索与训练流程。与此同时，Brave 浏览器提供可绕过部分网站付费墙并替换广告的设置，原告据此主张其规避了技术保护措施并侵害版权。纽约时报此前已于 2023 年末起诉 OpenAI 和微软，本案则将争议延伸至浏览器、搜索索引和 API 组成的商业分发链条；相关侵权及违反《数字千年版权法》的说法目前均只是诉状主张，尚非法院认定。

**「实际影响」** 出版社的诉讼已使 Brave 绕过付费墙、抓取新闻内容并通过 Brave Search API 向 Anthropic、Perplexity、Mistral、xAI 和 Cohere 等 AI 公司提供实时内容的做法面临司法审查，直接加大其浏览器、搜索索引和内容分发业务的版权及 DMCA 合规风险；这些指控目前尚未经法院裁决。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://kod.ru/nyt-brave-isk-ii">The New York Times подала в суд на Brave за сбор статей для ИИ</a></li>
<li><a href="https://techcrunch.com/2026/11/02/new-york-times-and-other-outlets-sue-web-browser-brave-over-alleged-content-scraping/">New York Times and other outlets sue web browser Brave over...</a></li>
<li><a href="https://www.theverge.com/tech/1024588/brave-lawsuit-ai-scraping-new-york-times">The New York Times sues Brave web browser for AI ... | The Verge</a></li>

</ul>
</details>

**标签**: `#AI content licensing`, `#copyright law`, `#Brave Search`, `#publishing`

---

<a id="item-tech-news-5"></a>
### [本地 Qwen 3.8 27B 可解读模型权重](https://simonwillison.net/2026/Nov/3/qwen-can-interpret-model-weights/) ⭐️ 7.0/10

Simon Willison 复现了 Rikiya Takehi、Jayden Teoh、Alex Zhang 和 Omar Khattab 的“权重空间编程”实验：论文宣称 GPT-6 Astra 可直接阅读、解释并修改以浮点数表示的模型权重，甚至无需编写训练循环即可生成游戏策略网络或修正 Qwen3.5-0.8B 的数学能力问题。Willison 通过 LM Studio 在笔记本上运行 17GB 的 Qwen3.8-27B Q4\_K\_M 量化版，在默认 8192 上下文报错后改用长上下文；该模型经过 46 分 12 秒和 43,506 个推理 token，正确识别出简化的“吃豆人”网格游戏，并给出 72% 的置信度，他还成功识别了 Pong。作为对照，通过 OpenRouter 运行的 Kimi K3.1 Pro 在 9 分 41 秒和 19,493 个推理 token 后正确判断了 Breakout。这表明至少在特定游戏策略网络的识别任务上，较小且可本地运行的模型也能从原始权重推断行为，但该演示不等同于已证明模型能可靠理解或编辑任意神经网络。

rss · Simon Willison · 11月3日 16:29 · [社区讨论](https://news.ycombinator.com/item?id=50355251)

**「权重空间编程」** 传统上，模型权重通常由训练算法通过梯度更新产生，而“权重空间编程”指语言模型直接把神经网络参数（浮点数值）当作可分析、修改或生成的对象，而非只借助代码工具来训练或编辑模型。该论文区分了两类能力：不使用工具时仅从原始权重推断网络行为，以及配合代码执行后更新其他模型；这次 Qwen 3.8 27B 的演示主要针对前者。其测试使用强化学习训练出的简化 10×10 网格游戏策略网络，并让模型仅凭权重判断网络所训练的游戏。

**「实际影响」** 这表明研究者在运行 17GB 量化版 Qwen 3.8 27B 的个人笔记本上，也能让模型直接读取并推理原始浮点权重，从而降低体验“权重空间编程”的硬件门槛。当前证据主要限于识别特定小游戏策略网络，且 Qwen 的一次推理耗时 46 分 12 秒、消耗 43,506 个推理词元，尚未证明其能可靠编辑权重或达到论文中 GPT-6 Astra 的效果。

**「评论者强调正确性与可扩展性」** 评论者认可这更像一次范式变化的开端，但质疑模型给出的解释是否可靠，以及它是否真的理解权重而非仅识别模式；也有人认为 Qwen3.8-27B 在较高层架构与决策指导下已能接近前沿模型的表现。进一步的问题集中在模型能否编辑同代模型权重、训练数据与实际权重理解之间的区别，以及 steering vectors、J spaces 和 LoRA 等既有方法会发挥多大作用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://rikiyat.github.io/blog/weight-space-programming/">Sparks of Weight - Space Programming : LLMs can natively read ...</a></li>
<li><a href="https://simonwillison.net/2026/Nov/3/qwen-can-interpret-model-weights/">Qwen 3 .8 27 B on my laptop can interpret model weights , too</a></li>
<li><a href="https://simonwillison.net/2026/Nov/3/qwen-can-interpret-model-weights/">Qwen 3.8 27B on my laptop can interpret model weights, too</a></li>

</ul>
</details>

**标签**: `#weight-space programming`, `#LLMs`, `#model-weight interpretation`, `#Qwen`, `#AI research`

---

<a id="item-tech-news-6"></a>
### [Mac 数据中心级构建的工程挑战](https://namespace.so/blog/mac-at-any-scale) ⭐️ 7.0/10

《Mac at any scale》深入探讨了在 Apple 封闭且严格控制的生态中，将 Mac 扩展到数据中心规模以支撑软件构建和测试所面临的工程问题。关键约束不只是增加设备数量，还包括 iOS 构建对 Mac 和专用工具链的依赖、代码签名与证书管理、跨编译方案，以及无人值守自动化带来的运维取舍。文章还关注设备小型化对集中部署的意义，因为即使计算性能充足，工具链限制和维护成本仍会直接影响基础设施的可扩展性。现有材料将其定位为工程经验型深度解读，而非包含新产品、版本、性能数据或行业级突破的发布公告。

hackernews · anner\_ · 11月3日 14:53 · [社区讨论](https://news.ycombinator.com/item?id=50352758)

**「iOS 构建为何依赖 Mac」** Apple 官方支持的 iOS 开发流程以运行 macOS 的 Mac、Xcode、代码签名和相关测试工具为核心；尽管社区有人尝试从 Linux 交叉编译，常规构建与测试仍高度依赖这一工具链。文中“Mac at any scale”指服务商集中运营 Mac 构建与测试集群，而不是 Apple 推出的新型硬件。由于 Apple 没有提供适合数据中心的替代方案，Namespace 需要自行解决 Mac 的采购、部署、调度和持续维护等问题。

**「规模化构建的运维代价」** 对于需要规模化构建和测试 iOS/macOS 软件的团队，这套方案要求部署定制 Mac 机架，并处理 macOS 虚拟化与大型镜像分发，直接增加了基础设施和运维负担。

**「社区讨论」** 多位评论者认为，这类方案的主要困难来自 Apple 工具链、代码签名、测试能力和遗留限制；有人表示，如果 Apple 推出性能接近 Mac mini、但价格更高的 Xserve，用户仍可能购买，因为数据中心运维本身就十分昂贵。分歧集中在“iOS 构建是否绝对无法离开 Mac”：一名开发者称自己曾从 Linux 主机交叉编译 C、C++ 和 Fortran 的 iOS/macOS 应用，提供了有限范围内的反例，但这并不等同于官方完整工具链可以被完全替代。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://namespace.so/blog/mac-at-any-scale">Mac at any scale | Namespace</a></li>
<li><a href="https://namespace.so/blog/mac-at-any-scale">Mac at any scale - Namespace</a></li>

</ul>
</details>

**标签**: `#macOS infrastructure`, `#iOS toolchains`, `#build automation`, `#Apple ecosystem`, `#data centers`

---

<a id="item-tech-news-7"></a>
### [飞机背景声可泄露视频位置](https://simonwillison.net/2026/Nov/3/a-sound-that-leaks-your-exact-location/) ⭐️ 7.0/10

Simon Willison 于 2026 年 11 月 3 日介绍了 Colsto 的一项开源情报（OSINT）演示：从视频中几乎难以察觉的背景飞机噪声提取多普勒曲线，再与 ADS-B 飞行数据交叉比对。分析会利用飞机的速度、距离以及不同航班出现间隔等线索，据称能够推断视频的准确拍摄位置。该方法揭示了普通环境音可能成为位置追踪工具的隐私与监控风险，但原文仅提供简要概述，没有给出具体实现步骤或验证细节。

rss · Simon Willison · 11月3日 05:32

**「背景」** 这一方法建立在多普勒效应上：当飞行器接近或远离录音点时，其发动机或螺旋桨噪声的频率会随径向速度产生可测量的变化。分析者可从视频音轨中提取这些几乎听不见的飞机噪声，绘制多普勒曲线，再与 ADS-B 航空器位置和速度轨迹进行匹配，利用多架飞机出现的时间间隔、距离与速度约束推算拍摄地点；公开报道给出的案例精度可达约 100 米。

**「潜在隐私影响」** 对会在公开视频中保留飞机环境声的创作者而言，未刻意透露的拍摄地点可能被他人通过多普勒曲线与 ADS-B 飞行数据匹配而推断；独立的 DOPPLERGEIST 重建项目也表明这一方法可被工具化，但实际定位仍取决于飞机声是否清晰可辨及数据匹配条件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.techradar.com/computing/cyber-security/youtuber-discovers-aircraft-noise-trick-that-can-geolocate-your-videos-to-within-100m-doppler-effect-pinpoints-locations-from-just-60-seconds-of-audio">YouTuber discovers aircraft noise trick that can geolocate ...</a></li>
<li><a href="https://www.youtube.com/watch?v=UytYrhYLOKI">I discovered a sound that leaks your exact location (and it&#x27;s ... YouTuber Reveals How Sounds Humans Cannot Hear Can Expose a ... I discovered a sound that leaks your exact location (and it&#x27;s ... GitHub - AlanBacker/audio-flyover-geolocation: Locate where a ... aircraft-doppler-geolocation · Plugin Catalog | Hermes Agent</a></li>
<li><a href="https://github.com/1337isnot1337/DOPPLERGEIST">GitHub - 1337isnot1337/DOPPLERGEIST: A tool to geolocate audio ...</a></li>

</ul>
</details>

**标签**: `#OSINT`, `#privacy`, `#geolocation`, `#audio analysis`, `#ADS-B`

---

<a id="item-tech-news-8"></a>
### [俄数据中心地下化应对袭击](https://arstechnica.com/ai/2026/11/russia-looks-to-hide-data-centers-underground-as-ukrainian-drones-strike-back/) ⭐️ 7.0/10

乌克兰无人机袭击造成俄罗斯多家数据中心及其 AI 超级计算机受损，并导致云服务中断，Yandex、Sberbank、VKontakte 和俄罗斯财政部运营的相关设施均受到影响或被停用。国有电信运营商 Rostelcom 正与 Norilsk 矿业公司讨论将部分数据中心迁入地下，俄罗斯地方官员还提议在露天煤矿内建设设施并以绿色公园覆盖伪装。普京于 11 月 2 日签署法令，要求私营数据中心运营商预留 10%的可用场地和计算能力；数字发展部将负责清查资源，政府成立委员会统筹征用，运营商须在接到通知后 24 小时内交付使用，经俄罗斯联邦安全局批准后还可临时调用境外数据中心。这些措施把计算资源纳入战时国家征用和冗余体系，同时凸显常规云与 AI 基础设施面对无人机袭击和地缘冲突时的脆弱性。

rss · Ars Technica · 11月3日 20:39

**「地下数据中心与应急算力」** 此次规划的背景是，俄乌战争中的无人机袭击已波及俄罗斯境内的云计算与 AI 基础设施，Yandex、Sberbank、VKontakte 和俄罗斯财政部相关数据中心受损或中断，暴露出关键算力设施过度集中且缺乏物理防护的问题。俄方因而讨论将部分数据中心迁入地下专用设施或废弃露天煤矿，以降低无人机打击风险，但这些方案仍处于提议和初步洽谈阶段。另一项并行措施是普京于 2026 年 11 月 2 日签署法令，要求私营数据中心预留 10%的场地和计算容量供政府应急征用，从固定设施防护延伸至战时算力调度。

**「直接影响」** 乌克兰无人机袭击已损毁 Yandex 在俄罗斯的五座数据中心中的三座，Sasovo 站点严重受损并全面停机，Yandex Cloud、支付等下游服务随之中断；与此同时，俄罗斯政府可在通知后 24 小时内调用私营运营商预留的 10% 算力，使云服务连续性与战时国家资源调度之间的取舍更为直接。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://understandingwar.org/research/russia-ukraine/russian-offensive-campaign-assessment-november-2-2026/">Russian Offensive Campaign Assessment, Nov 2 , 2026 | ISW</a></li>
<li><a href="https://www.techradar.com/pro/data-centers-can-be-located-in-exhausted-open-pits-russia-eyes-300-meter-deep-coal-mines-to-shield-server-infrastructure-from-ukrainian-drones">Russia eyes abandoned coal mines for underground data centers</a></li>
<li><a href="https://www.theregister.com/security/2026/10/12/ukrainian-drone-strikes-on-yandex-datacenters-knock-cloud-and-payments-offline/5302577">Ukrainian drone strikes on Yandex datacenters knock cloud and...</a></li>
<li><a href="https://www.tomshardware.com/tech-industry/data-centers/ukrainian-drones-hit-russias-yandex-data-centers-housing-two-top-supercomputers-major-outage-follows-retaliatory-strike">Ukrainian drones hit Russia &#x27;s Yandex data centers housing two top...</a></li>

</ul>
</details>

**标签**: `#AI infrastructure`, `#data centers`, `#cloud computing`, `#infrastructure resilience`, `#geopolitics`

---

<a id="item-tech-news-9"></a>
### [Google 关闭感染逾 130 万台 Android 电视盒子的 x.cpe 僵尸网络](https://arstechnica.com/google/2026/11/google-dismantles-botnet-secretly-running-on-1-3-million-android-tv-boxes/) ⭐️ 7.0/10

Google 威胁情报组称，已关闭 x.cpe 僵尸网络；该网络鼎盛期运行在超过 130 万台 Android TV 设备上，其中多数是获得 Google 认证、主要以 MECOOL 品牌销售的电视盒子。恶意软件由单阶段加载器迅速演化为模块化的三阶段平台，并面向第三方出售接入权限；深圳 Videostrong Technology 利用混淆技术绕过认证筛查，受感染设备完成设置并联网后，还会通过后门远程安装恶意软件。初始程序 x.cpe（包名 com.oemservice）本身不具恶意功能，但拥有按运营方指令安装模块所需的系统级权限，并会关闭本应拦截静默安装恶意包的 Play Protect。Google 称，多数设备被用于住宅代理以路由大量恶意流量，或运行广告欺诈模块；Videostrong 还能够执行终端命令、截取屏幕及探测局域网内其他设备，Google 曾实时观察到其相关活动。

rss · Ars Technica · 11月3日 17:08

**「背景：x.cpe 如何绕过 Android TV 认证」** Android TV 设备若要使用 Google 应用和品牌，必须通过 Google 的认证流程；该流程通常检查预装软件与固件，但认证完成后通过远程后门植入的恶意代码可能不在筛查范围内。x.cpe 采用三阶段模块化结构，包名为 com.oemservice 的桩应用取得系统级权限并关闭 Play Protect，再按操作者指令安装负责代理流量或广告欺诈等功能的模块。事件发生后，Google 将 Videostrong 及未来关联实体排除在认证 Android 设备市场之外，并表示将加强认证 Android TV 设备的固件完整性检查。

**「影响」** 这意味着逾 130 万台主要贴有 MECOOL 品牌、已获 Google 认证的 Android TV 机顶盒曾可能被用于住宅代理、广告欺诈及安装更多恶意模块，暴露了设备认证与固件供应链的安全缺口。尽管 Google 已中断 x.cpe 僵尸网络，受感染设备中的固件后门仍然存在，因此用户和厂商仍需单独修复或更换设备，不能仅凭僵尸网络被关闭就认为风险已经消失。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cloud.google.com/blog/topics/threat-intelligence/shutting-the-door-on-the-xcpe-botnet">Shutting the Door on the XCPE Botnet | Google Cloud Blog</a></li>
<li><a href="https://thehackernews.com/2026/11/google-disrupts-13-million-device.html">Google Disrupts 1 . 3 Million - Device Android Botnet, Says TV Box...</a></li>
<li><a href="https://www.malwarebytes.com/blog/mobile/2026/11/a-hidden-backdoor-put-1-3-million-tv-boxes-to-work-for-criminals">A hidden backdoor put 1 . 3 million TV boxes to work for... | Malwarebytes</a></li>
<li><a href="https://www.theverge.com/tech/1024807/google-botnet-android-tv-shut-down">One of Google ’s Android partners turned 1 . 3 million ... | The Verge</a></li>

</ul>
</details>

**标签**: `#Android TV`, `#botnet`, `#malware analysis`, `#cybersecurity`, `#supply-chain security`

---

<a id="item-tech-news-10"></a>
### [币安披露 63 亿美元加密货币失窃攻击链](https://www.theverge.com/news/1025576/binance-cyrpto-theft-explained) ⭐️ 7.0/10

币安在事后分析中称，一起规模达 63 亿美元的加密货币盗窃并非单次入侵或简单钓鱼，而是历时数月的多阶段攻击。攻击始于 6 月，一名开发人员下载了疑似通过恶意 Google 广告传播的被篡改安装程序，导致工程师相关信息暴露；后续还涉及虚假招聘、被攻陷的开发人员及恶意软件分发。币安称，攻击过程中可能还滥用了某款内部 AI 工具，但现有信息未说明其具体作用或证据。此次事件凸显了加密货币交易所面临的社工攻击、开发者端点入侵与软件供应链风险。

rss · The Verge · 11月3日 22:04

**「多阶段渗透与内部工具风险」** 理解此次事件的关键，是把它视为多阶段渗透而非单次钓鱼：攻击者先通过虚假招聘或恶意广告诱导开发者使用被篡改的软件，再以受感染设备为支点逐步获取更深层的系统权限。攻击链因而可以跨越人员、软件分发和内部工具等环节，并持续数月；内部 AI 工具若能继承密钥、审批或交易流程权限，被滥用后可能扩大影响，但公开信息尚未说明此次工具的具体能力和权限边界。

**「直接影响」** 这次入侵最终导致约 63 亿美元资产从币安钱包转出，其中约 90%（约 57 亿美元）被盗并由币安补充，迫使区块链安全机构与加密公司追踪受影响钱包并阻止资金继续流动。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.reuters.com/world/binance-says-hackers-used-fake-job-interview-compromise-computer-before-63-2026-11-03/">Binance hackers used fake job interview in $6.3 billion ...</a></li>
<li><a href="https://www.cnbc.com/2026/11/03/binance-co-ceo-teng-says-hackers-used-fake-job-interviews-to-steal-6point3-billion-in-crypto.html">Binance co-CEO Teng says hackers used fake job interviews to ...</a></li>
<li><a href="https://coinpedia.org/research-report/binance-hack-detailed-report-what-happened-how-6-3-billion-was-stolen-and-whats-next/">Binance Hack 2026: The $6.3 Billion Crypto Theft, How It ...</a></li>
<li><a href="https://www.businessinsider.com/binance-hack-heist-crypto-security-2026-10">Binance Says 90% of $6.3 Billion in Crypto Stolen in Hack ...</a></li>
<li><a href="https://www.forbes.com/sites/digital-assets/2026/11/03/the-63-billion-binance-hack-exposes-cryptos-biggest-internal-control-problem/">The $6.3 Billion Binance Hack Exposes Crypto&#x27;s Biggest ...</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#supply-chain attack`, `#AI security`, `#social engineering`, `#cryptocurrency`

---

<a id="item-tech-news-11"></a>
### [CrowdStrike 斥资近 5 亿美元收购两家 AI 安全初创公司](https://techcrunch.com/2026/11/03/crowdstrike-to-shell-out-nearly-500m-for-2-ai-security-startups-as-the-market-for-securing-agents-takes-off/) ⭐️ 7.0/10

CrowdStrike 宣布将收购 Fiddler AI 和 Dreadnode，交易总额近 5 亿美元。Fiddler AI 提供 AI 代理可观测性软件，Dreadnode 则帮助企业自动化 AI 安全测试。此次收购将补强 CrowdStrike 在 AI 代理可观测性和安全验证领域的能力，反映 AI 代理安全市场正在升温。

rss · TechCrunch · 11月3日 17:56

**「AI 智能体安全背景」** AI 智能体可观测性是指监控企业环境中 AI 智能体的运行情况，Fiddler AI 提供这类软件，帮助企业观察智能体的运行状态。自动化 AI 安全测试是 Dreadnode 的重点，可在模型、应用或智能体上线前自动检测缺陷。此次收购延续了 CrowdStrike 通过并购扩充安全产品线的做法，该公司此前曾收购 Payload Security 和 Preempt Security。

**「影响」** 若交易完成，CrowdStrike 将把 Fiddler AI 的 AI 智能体可观测能力和 Dreadnode 的自动化安全测试能力纳入 Falcon 平台，帮助企业安全团队在上线前发现模型、应用及智能体中的漏洞，并持续监控智能体行为。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/CrowdStrike">CrowdStrike - Wikipedia</a></li>
<li><a href="https://techcrunch.com/2026/11/03/crowdstrike-to-shell-out-nearly-500m-for-2-ai-security-startups-as-the-market-for-securing-agents-takes-off/">CrowdStrike to shell out nearly $ 500 M for 2 AI security ... | TechCrunch</a></li>
<li><a href="https://techcrunch.com/2026/11/03/crowdstrike-to-shell-out-nearly-500m-for-2-ai-security-startups-as-the-market-for-securing-agents-takes-off/">CrowdStrike to shell out nearly $500M for 2 AI security ... | TechCrunch</a></li>
<li><a href="https://www.crowdstrike.com/en-us/blog/">Cybersecurity Blog | CrowdStrike</a></li>

</ul>
</details>

**标签**: `#AI security`, `#AI agents`, `#acquisitions`, `#observability`, `#security testing`

---

<a id="item-tech-news-12"></a>
### [树莓派 16GB Pi 5 再涨价](https://www.theregister.com/personal-tech/2026/11/03/raspberry-pi-hikes-prices-again-barely-a-month-after-the-last-round/5307004) ⭐️ 7.0/10

《The Register》报道称，树莓派将 16GB Pi 5 的售价上调至 385 美元，原因与当前内存供应紧张有关。这是在不到一个月前刚涨价后再次调价，也使该现售型号的价格超过发布时价格的三倍。Rapid ...

rss · The Register · 11月3日 09:30

**「16GB Pi 5 的价格背景」** 16GB Raspberry Pi 5 是 Raspberry Pi 5 系列中内存密度最高的型号；官方称，缺乏替代的 16GB DRAM 供应，加上其他零部件持续短缺，迫使公司再次上调这类产品的价格。该型号于 2026 年 11 月 2 日起从 305 美元涨至 385 美元，相比 2025 年 1 月上市时价格已超过三倍。

**「采购成本影响」** 16GB Raspberry Pi 5 加价 80 美元至 385 美元，将直接抬高面向爱好者、教育机构和边缘计算项目的采购成本；官方称 16GB DRAM 缺乏替代供应是此次涨价的重要原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.techtroduce.com/raspberry-pi-5-16gb-price-increase-november-2026/">Raspberry Pi 5 16GB Price Rises to $385 Amid Memory Shortage</a></li>
<li><a href="https://www.raspberrypi.com/news/price-rises-for-some-16gb-raspberry-pi-products/">Price rises for some 16GB Raspberry Pi products</a></li>
<li><a href="https://tech.yahoo.com/computing/articles/16gb-raspberry-pi-5-hiked-161735763.html">16GB Raspberry Pi 5 hiked to $385, more than triple its ...</a></li>
<li><a href="https://windowsreport.com/raspberry-pi-5-16gb-now-costs-385-after-another-price-increase/">Raspberry Pi 5 16GB Now Costs $385 After Another Price Increase</a></li>
<li><a href="https://www.raspberrypi.com/news/price-rises-for-some-16gb-raspberry-pi-products/">Price rises for some 16GB Raspberry Pi products</a></li>

</ul>
</details>

**标签**: `#Raspberry Pi`, `#hardware pricing`, `#memory shortages`, `#single-board computers`

---

<a id="item-tech-news-13"></a>
### [OpenVDDK 开源替代 VMware 未公开迁移工具](https://www.theregister.com/virtualization/2026/11/03/architect-creates-open-source-replacement-for-vm-migration-tool-vmware-has-hidden/5307124) ⭐️ 7.0/10

一名架构师创建了开源项目 OpenVDDK，用于替代 VMware 一款未公开的虚拟机迁移工具。据报道，OpenVDDK 目前已在生产环境中以较大规模使用。这为 VMware 原本未公开的相关迁移能力提供了开源替代方案，但现有资料未说明其具体功能、性能、兼容性或部署条件。

rss · The Register · 11月3日 04:45

**「背景」** VMware VDDK（Virtual Disk Development Kit）是一组供软件访问和操作虚拟磁盘的库与工具；VMware 已将其从公开下载渠道撤下，而 OpenVDDK 被定位为该能力的开源替代方案。OpenVDDK 采用 Apache 2.0 许可，目标是直接替代 VMware 备份与迁移工具加载的 libvixDiskLib.so.8.0.3；项目方称其仅依据公开文档和黑盒测试从头编写，未包含 VMware 代码。

**「对 VMware 迁移方案的影响」** 需要摆脱 VMware VDDK 的团队可采用据报道已在生产环境中规模化使用的 OpenVDDK；这个 GPL-3.0 洁净室实现定位为兼容替代品，可降低迁移工作流对专有组件的依赖。它并非唯一选择，OpenNebula OneSwap 宣称迁移成功率为 96%，Nutanix Move 也已支持无需 VDDK 的迁移。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theregister.com/virtualization/2026/11/03/architect-creates-open-source-replacement-for-vm-migration-tool-vmware-has-hidden/5307124">Architect creates open source replacement for VM migration ...</a></li>
<li><a href="https://openvddk.com/">OpenVDDK – Independent Virtual Disk Library</a></li>
<li><a href="https://www.theregister.com/virtualization/2026/11/03/architect-creates-open-source-replacement-for-vm-migration-tool-vmware-has-hidden/5307124">Architect creates open source replacement for VM migration tool...</a></li>
<li><a href="https://github.com/jimmyma-zhanwei/openvddk">GitHub - jimmyma-zhanwei/ openvddk : Clean-room, high-performance...</a></li>

</ul>
</details>

**标签**: `#virtualization`, `#VM migration`, `#open source`, `#VMware`

---

<a id="item-tech-news-14"></a>
### [StateBench：长文档状态跟踪评测](https://huggingface.co/blog/allenai/statebench) ⭐️ 7.0/10

Hugging Face 博客发布了 StateBench，用于衡量语言模型在长文档中跟踪实体信息及其变化的能力，并提供技术报告、数据和代码。基准包含四个逐级复杂的难度：R-trivial 仅涉及不可变赋值，Aperiodic 要求找出最近一次按值重赋值的结果，Soluble 加入依赖当前值的自引用更新，General finite 则涉及按引用赋值和变量交换等跨状态依赖。开放预训练模型实验显示，Olmo 3、Olmo Hybrid 及较小模型均未在训练中见过超过 64,000 个 token 的上下文，但多数模型在 R-trivial 上表现良好、随输入增长在 Aperiodic 上准确率下降，并在 General finite 上接近随机水平；同一问题采用 RULER 风格或电子表格编辑形式时，结果也可能相差悬殊。Gemini 3.8 Flash、Claude Opus 5.5、GPT-6 Sol 和 GPT-6 Luna 在 R-trivial 与 Aperiodic 上表现良好，但在 Soluble 和 General finite 上随输入变长而明显退化，最长的 General finite 任务准确率降至 13% 或更低。研究人员还从零训练了六种 2.75 亿参数模型，在最长 256 次赋值上训练并测试最长 64,000 次赋值；Gated DeltaNet 和混合架构在较简单的三个层级上几乎完美泛化，而 Transformer 在长序列上退化，并且始终未能学会 General finite 问题。

rss · Hugging Face Blog · 11月3日 17:15

**「状态跟踪与理论背景」** 状态跟踪是指在代码或叙事中持续更新实体当前状态，例如追踪变量重赋值、物品持有人或角色位置。Transformer 在具有长依赖链的困难状态跟踪任务上存在已知理论限制，这推动了采用持续记忆机制的循环架构和混合架构；StateBench 的四级分类则依据 Krohn–Rhodes 理论，将有限状态跟踪问题按可分解的原语加以区分。

**「实际影响」** 对于评估长代码、长叙事或其他长上下文应用的研究者与开发者，实验表明上下文窗口长度不足以代表状态可靠性，模型架构、针对性训练以及题目呈现格式都必须纳入测试。

**标签**: `#large language models`, `#long-context evaluation`, `#state tracking`, `#AI benchmarks`

---

<a id="item-tech-news-15"></a>
### [Google Antigravity 的智能体化学信息学工作流](https://deepmind.google/blog/agentic-cheminformatics-with-google-antigravity/) ⭐️ 7.0/10

Google DeepMind 展示了为 Google Antigravity 开发的 Cheminformatics Skills：底层语言模型负责工作流编排、数据库导航和科学推理，并通过基于 RDKit 的确定性工具以及 ChEMBL、PubChem 连接器执行和核验化学任务。在以克唑替尼、洛拉替尼等肺癌药物为案例的演示中，智能体约一小时内检索并整理了数千个化合物，执行匹配分子对分析，构建多种效力预测模型并用留出集验证，最终提出带合成路线的新型刚性大环候选物。分析显示，环化通常能减少可旋转键并提高效力，而智能体生成的结构还可继续交给 AlphaFold 或分子动力学等方法分析。相关技能现已可通过 Antigravity 应用和 Science 插件使用，企业用户也可使用 Google Cloud 凭据接入。DeepMind 强调，数据稀疏、跨实验室测定噪声和狭窄动态范围会限制预测精度，计算设计仍须经过合成与实验验证，且该演示未报告对照基线或系统基准。

rss · DeepMind Blog · 11月3日 17:01

**「化学信息学与药物设计基础」** 化学信息学研究如何统一文献、专利和供应商目录中的分子表示，并将其与数据库查询、性质预测和分子设计工具衔接；由于同一分子可能以 IUPAC 名称、Markush 结构或结构数据文件出现，数据归一化和错误控制一直是关键难点。药物研发中的“刚性化”通常通过增加化学键来减少可旋转键与构象自由度，从而可能提高结合亲和力和效力，Google Antigravity 的示例以克唑替尼和洛拉替尼说明了这一思路。匹配分子对分析通过比较仅有一个离散结构差异的分子来评估该变化的影响，而新推出的 Cheminformatics Skills 让语言模型负责工作流编排与科学推理，再调用 RDKit、ChEMBL 和 PubChem 等确定性工具和数据源执行化学计算。

**「影响」** Google Antigravity 的 Cheminformatics Skills 已向用户开放，使药物发现团队在此次肺癌药物演示中于约一小时内完成数千种化合物的检索与分析、效力建模，并提出带合成路线的新刚性大环设计，将过去需数天的候选分析迭代压缩为更快的假设生成流程。其实际价值仍取决于候选分子的合成与实验验证，因此目前可确认的是前期研究提速，而非临床开发周期已经缩短。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepmind.google/blog/agentic-cheminformatics-with-google-antigravity/">Agentic Cheminformatics with Google ... — Google DeepMind</a></li>
<li><a href="https://deepmind.google/blog/agentic-cheminformatics-with-google-antigravity/">Agentic Cheminformatics with Google Antigravity</a></li>
<li><a href="https://aiunderstanding.org/news/google-antigravity-adds-cheminformatics-skills-for-drug-discovery">Google Antigravity adds cheminformatics skills for drug discovery</a></li>

</ul>
</details>

**标签**: `#agentic AI`, `#cheminformatics`, `#drug discovery`, `#molecular generation`, `#Google DeepMind`

---

<a id="item-tech-news-16"></a>
### [Palette：让小型开放权重模型按组织设计语言生成幻灯片](https://huggingface.co/blog/ibm-research/palette-deck-building) ⭐️ 6.0/10

Palette 试图让企业自托管的小型开放权重模型生成符合自身设计语言的演示文稿，同时避免敏感内容离开内部系统。研究团队以 LoRA 微调一个 20B 参数模型，用合成数据训练“设计师”和“编码器”两种角色，并通过检查与修复工具检测文字溢出、遮挡等版式问题；其编码阶段并行运行后约快 6–7 倍。文章称，该模型在 PresentBench 所测三个领域中的两个排名第一，训练数据约覆盖 1000 份演示文稿和 1 万张幻灯片。不过，现有内容未给出与前沿模型对比的完整基准、模型发布信息，因此其实际优势仍待验证。

rss · Hugging Face Blog · 11月3日 16:35

**标签**: `#small language models`, `#open-weight AI`, `#slide generation`, `#fine-tuning`, `#privacy`

---

<a id="item-tech-news-17"></a>
### [机器学习与 AI 在精准医学预测建模中的应用](https://news.google.com/rss/articles/CBMiX0FVX3lxTE16NWIxdF9vMHNNVGpKbVl4V1dNc1V6VFFNaDU3czQ0TmFoTVFOTWk5RDhJT1N1WmJhVmpUVnl3M25ZazVndVFpYnNYOW5CVXZuMlI1emF3WW94dHdhUDdF?oc=5) ⭐️ 6.0/10

Nature 的一篇文章聚焦机器学习和人工智能在精准医学预测建模中的新兴应用。现有材料仅提供标题与来源，未说明所采用的技术、数据集、验证方法、性能指标或临床部署情况。文章可作为该领域的概览入口，但目前证据不足以评估其技术深度、具体贡献、创新性或实际影响。

google\_news · Nature · 11月3日 17:18

**「精准医疗与预测建模背景」** 精准医疗...。机器学习与人工智能...，用于...。

**「潜在影响」** 对精准医疗和医疗 AI 研究者而言，这篇发表于《npj Digital Medicine》的文章梳理了机器学习与人工智能在个体化预测建模中的新兴应用，可作为评估研究方向与应用机会的参考；但现有材料未提供具体模型性能、临床验证或部署结果，因此不能据此认定其已改善临床决策或患者结局。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://medicine.net/news/TechnologyAI/Emerging-Applications-of-Machine-Learning-and-AI-for-Predictive-Modeling-in-Precision-Medicine.html">Emerging Applications of Machine Learning and AI ... - Medicine .net</a></li>
<li><a href="https://medicine.net/news/TechnologyAI/Emerging-Applications-of-Machine-Learning-and-AI-for-Predictive-Modeling-in-Precision-Medicine.html">Emerging Applications of Machine Learning and AI ... - Medicine .net</a></li>
<li><a href="https://www.nature.com/articles/s41746-026-03393-9">Emerging applications of machine learning and AI for ... - Nature</a></li>

</ul>
</details>

**标签**: `#machine learning`, `#artificial intelligence`, `#predictive modeling`, `#precision medicine`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [财报发布后美股盘前个股分化](https://www.cnbc.com/2026/11/03/stocks-making-the-biggest-moves-premarket-pfe-pltr-aapl-zbra.html) ⭐️ 7.0/10

Palantir 股价盘前跌近 8%，尽管其第三季度美国商业收入同比增长 148%至 9.84 亿美元，并预计 2026 年全年营收 85.3 亿美元；Apple 跌近 4%，因财年第四季度利润率展望及 iPad 销售低于市场预期。辉瑞第三季度调整后每股收益 0.87 美元、营收 165.8 亿美元，均高于 LSEG 预期，股价基本持平；Zebra Technologies 和 Gartner 均跌逾 6%，前者虽业绩超预期，但全年自由现金流指引至少 10 亿美元，略低于市场预估的 10.2 亿美元。Revvity 因将全年备考调整后每股收益指引上调至 5.40 至 5.45 美元而涨 7%；Yum Brands 第三季度调整后每股收益 1.56 美元高于预期、营收 20.5 亿美元符合预期，涨 1%。

rss · CNBC Finance · 11月3日 12:47

**「背景」** 此次名单按正式开盘前交易时段的股价涨跌幅编排，异动主要源于各公司最新季度业绩及全年指引与分析师预期的差异。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/11/03/stocks-making-the-biggest-moves-premarket-pfe-pltr-aapl-zbra.html">Stocks making the biggest moves premarket : PFE, PLTR, AAPL...</a></li>

</ul>
</details>

**标签**: `#earnings results`, `#corporate guidance`, `#premarket trading`, `#technology stocks`, `#pharmaceuticals`

---

<a id="item-finance-news-2"></a>
### [黑石称 AI 建设需增加股权融资](https://www.cnbc.com/2026/11/03/equity-ai-debt-blackstone-pimco-financing.html) ⭐️ 7.0/10

黑石总裁乔恩·格雷称，AI 基础设施建设需要更多股权融资，因为贷款人对该行业及单一公司的风险敞口正在集中。皮姆科 CEO 埃曼纽尔·罗曼援引估算称，未来五年 AI 资本支出可能达到 10 万亿美元，而全球公司债市场约为 20 万亿美元；他警告如此庞大的融资规模可能超出市场承受力。

rss · CNBC Finance · 11月3日 06:46

**「背景」** AI 基础设施目前依靠股权、债务、公开市场、银行和私募资本共同融资；贷款人的回报主要限于利息和本金，而股权投资者还能分享公司增长，因此增加股权融资有助于降低债务集中风险。

**「影响」** 若资本需求预测兑现，AI 基础设施企业将更依赖股权融资和结构化交易，贷款人的行业及单一公司集中风险可能上升。

**标签**: `#AI infrastructure`, `#debt financing`, `#equity capital`, `#data-center spending`, `#financial concentration risk`

---