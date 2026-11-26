---
layout: default
title: "Horizon Summary: 2026-11-26 (ZH)"
date: 2026-11-26
lang: zh
---

> 从 112 条内容中筛选出 16 条重要资讯。

---

**科技新闻**
1. [1Password 安全事件暴露生产部署控制疑问](#item-tech-news-1) ⭐️ 8.0/10
2. [Anthropic 的精简版 GRH Lean 验证](#item-tech-news-2) ⭐️ 8.0/10
3. [Google 发布 Cogentic 密码学论文](#item-tech-news-3) ⭐️ 8.0/10
4. [FCC 条件批准 SpaceX 部署百万颗 Starmind 卫星](#item-tech-news-4) ⭐️ 8.0/10
5. [数据中心遭军事袭击或不会停止](#item-tech-news-5) ⭐️ 8.0/10
6. [Hera 揭示小行星撞击后的混沌现场](#item-tech-news-6) ⭐️ 7.0/10
7. [Ladybird 发布首个可下载 Alpha 版本](#item-tech-news-7) ⭐️ 7.0/10
8. [华为被美陪审团裁定窃密并规避伊朗制裁](#item-tech-news-8) ⭐️ 7.0/10
9. [伊朗黑客大规模操纵法国超市制冷系统](#item-tech-news-9) ⭐️ 7.0/10
10. [纽约禁止 AI 聊天机器人玩具五年](#item-tech-news-10) ⭐️ 7.0/10
11. [州检察长反对拍卖 Character.AI 私聊](#item-tech-news-11) ⭐️ 7.0/10
12. [sqlite3\_rsync：低磁盘占用的 SQLite 快照复制](#item-tech-news-12) ⭐️ 6.0/10
13. [Evaluating Recent Model Releases on GDPx](#item-tech-news-13) ⭐️ 6.0/10
14. [NVIDIA Nemotron 3.5 Parse 开放训练与推理优化](#item-tech-news-14) ⭐️ 6.0/10
15. [IBM 用 CUGA 构建印度语言语音智能体](#item-tech-news-15) ⭐️ 6.0/10
16. [欧盟拟设 550 亿美元基金支持 AI 与量子技术](#item-tech-news-16) ⭐️ 6.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [1Password 安全事件暴露生产部署控制疑问](https://1password.com/blog/update-on-nov-2026-security-incident) ⭐️ 8.0/10

据现有材料，1Password 在关于 2026 年 11 月安全事件的更新中称，攻击者利用遭入侵的员工环境，将恶意代码推送至与生产后端服务相关的代码路径，但尚不清楚这些变更是否实际部署至生产环境。这一事件凸显了 SaaS 供应链风险：当员工设备、代码仓库权限和有效身份同时失守时，攻击者可能绕过原有的软件交付边界。现有材料没有说明 1Password 是否禁止直接推送主分支、分支保护和代码审查是否启用，以及部署审批能否识别此类改动。官方对加密保险库数据是否可能被访问或下载、以及受影响用户范围的具体说明也不充分，因此不能据此断言保险库内容已经泄露。

hackernews · lxhrstn · 11月25日 17:18 · [社区讨论](https://news.ycombinator.com/item?id=50644817)

**「背景」** 据 1Password 公告称，公司于 2026 年 11 月 19 日开始调查员工企业 GitHub 账户遭入侵事件，攻击者据称利用该账户访问源代码，并将恶意代码推送至后端服务。这属于典型的 SaaS 软件供应链风险：一旦开发者账户或生产环境权限被滥用，攻击者就可能影响代码审查、构建流程乃至部署结果，因此分支保护、最小权限和独立发布审批等控制措施成为此次事件的核心背景。

**「实际影响」** 员工账号或终端被攻陷后，攻击者可能沿内部代码与部署链路向生产服务推送恶意代码，使依赖 1Password 的 SaaS 团队面临供应链入侵风险；此次还已有部分客户账户信息被窃取的报道，因此相关组织应优先核验分支保护、部署审批和凭据隔离措施，而不能仅因客户密码未泄露而降低防范。

**「社区讨论」** 多数评论者认为，员工环境被攻陷后向生产代码推送是严重且典型的 SaaS 供应链风险，并集中质疑 1Password 是否禁止直接推送主分支，以及分支保护、代码审查和部署审批能否抵御此类攻击。一名长期用户因类似担忧使用本地保险库并停留在旧版应用，也有人要求官方明确保证加密保险库记录未被下载；另有用户称事件后收到疑似利用相关数据制作的高质量钓鱼邮件，但这一关联尚未得到证实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://1password.com/blog/update-on-nov-2026-security-incident">Update on a security incident involving... | 1 Password</a></li>
<li><a href="https://news.ycombinator.com/item?id=50644817">1 Password Security Incident | Hacker News</a></li>
<li><a href="https://9to5mac.com/2026/11/25/1password-confirms-security-incident-heres-what-you-need-to-know/">1Password confirms security incident, here’s what you need to ...</a></li>
<li><a href="https://techcrunch.com/2026/11/25/1password-said-hackers-broke-into-its-internal-systems-but-customer-passwords-are-safe/">1Password said hackers broke into its internal systems, but ...</a></li>

</ul>
</details>

**标签**: `#1Password`, `#SaaS security`, `#supply-chain security`, `#developer tooling`, `#credential management`

---

<a id="item-tech-news-2"></a>
### [Anthropic 的精简版 GRH Lean 验证](https://github.com/lsernau/grh-lean) ⭐️ 8.0/10

GitHub 仓库 lsernau/grh-lean 展示了一份据称由 Anthropic 生成的广义黎曼猜想（GRH）Lean 形式化验证，目标是此前的验证提供更短、更易阅读的版本。讨论中给出的规模数据称，代码从约 1700 万行缩减至约 7.6 万行，降幅为 99.56%；但由于现有材料未包含仓库正文或独立测量，这一数字及 Anthropic 归因仍待核实。仓库据称还补充了文档，并明确区分“已知数学”和“新数学”，以帮助读者定位既有结果与新增论证。争议的核心是，这种精简和文档化能否真正提升人类的理解与独立验证能力，而不只是让模型更高效地压缩证明。

hackernews · nb-t · 11月25日 21:48 · [社区讨论](https://news.ycombinator.com/item?id=50648050)

**「背景」** 黎曼猜想断言黎曼 ζ 函数的非平凡零点都位于复平面实部为 1/2 的临界线上；广义黎曼猜想（GRH）则将类似断言扩展至一族 L 函数。Lean 4 是用于描述并机器检查数学证明的形式化语言，但代码行数不能直接代表证明的数学深度或人类可读性。该仓库提供约 7.6 万行的精简版本，要求使用 Lean v4.35.0 和指定的 Mathlib 提交；讨论中所谓“缩减 99.56%”源于将约 1700 万行版本与约 7.6 万行版本对比。

**「对形式化验证工作的实际影响」** 如果仓库的声明成立，Lean/Mathlib 研究者将能利用约 7.6 万行的精简版和约 30 万行的可读版，更实际地审阅、复用并人工检查这项涉及黎曼猜想与狄利克雷 L 函数 GRH 的证明，而文档及“已知数学/新数学”分区也降低了理解大型证明的门槛。仓库还声明仅依赖 propext、Classical.choice 和 Quot.sound 等标准公理，便于核验其可信度；但 Anthropic/Claude 归属、约 99.56% 的压缩比例及独立审阅状态仍主要来自项目说明和外部报道，尚需进一步验证。

**「社区讨论」** 部分评论者认为，文档和“已知数学”与“新数学”的分区显著改善了可读性；另一些人则援引具体 Lean 文件，质疑普通研究者能否真正读懂并独立核验这些代码。讨论还将其与 Tao 近期关于缺乏洞察的超大证明所构成问题的观点联系起来，但现有评论不足以判断实际阅读难度和验证成本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Riemann_hypothesis">Riemann hypothesis - Wikipedia</a></li>
<li><a href="https://github.com/lsernau/grh-lean">GitHub - lsernau / grh - lean : A short Lean 4 proof of the Generalized ...</a></li>
<li><a href="https://news.ycombinator.com/item?id=50648050">Much shorter version of GRH Lean verification from Anthropic</a></li>
<li><a href="https://explainx.ai/blog/anthropic-grh-lean-76000-lines-compact-proof-claimed-vs-verified-2026">GRH Lean Proof Shrunk to 76,000 Lines: What Is Verified ...</a></li>
<li><a href="https://github.com/lsernau/grh-lean/tree/main">GitHub - lsernau/grh-lean: A short Lean 4 proof of the ...</a></li>

</ul>
</details>

**标签**: `#AI-assisted theorem proving`, `#Lean`, `#formal verification`, `#generalized Riemann hypothesis`, `#Anthropic`

---

<a id="item-tech-news-3"></a>
### [Google 发布 Cogentic 密码学论文](https://github.com/google-research/google-research/tree/master/cogentic_research_papers) ⭐️ 8.0/10

Google Research 在其 google-research 仓库中发布了一组 Cogentic 研究论文，主题涵盖整数分解、离散对数及相关计算问题。该工作试图为这些经典密码学难题提供新的算法路径，因此可能影响密码分析研究，但现有材料不足以确认其结果的有效性、相对新颖性或实际性能。社区评论称，整数分解方案建立在通用数域筛（GNFS）之上，并未证明 GNFS 依赖的三个未证实猜想，而是替换了其中依赖这些假设的部分，同时付出显著的复杂度代价；这意味着其理论定位与 GNFS 的比较仍是关键问题。此次发布引发了对 AI 推动数学研究及潜在后续突破的强烈兴趣。

hackernews · rgwohlbold · 11月25日 13:33 · [社区讨论](https://news.ycombinator.com/item?id=50642086)

**「相关密码学问题背景」** 整数分解与离散对数都是密码学中的基础计算问题：前者要求把合数分解为素因子，是 RSA 等公钥密码的安全基础；后者要求从群运算结果中恢复指数，关系到 Diffie–Hellman 密钥交换和椭圆曲线密码。经典通用整数分解算法中，通用数域筛（GNFS）具有目前最优的已知渐近复杂度，但其实际分析依赖若干未获证明的启发式假设。社区评论将 Cogentic 理解为在 GNFS 框架上替换部分依赖这些假设的步骤，并以更高的计算复杂度为代价；现有材料不足以确认这种定位是否已经得到严格验证。

**「实际影响」** 这批论文使密码学研究者和安全团队能够审查 Cogentic 所声称的整数分解与离散对数复杂度界，但因子分解结果尚待公开 Lean 证明和外部复核，因此目前不能据此认定现有密码部署或实际破解能力已得到改进。近期影响主要是引发对新算法的验证与评估。

**「社区反馈」** 评论者对 AI 加速数学发现的频率感到兴奋，并将其类比于 AlphaGo；也有人转述未经证实的说法，猜测这些成果只是更大进展的开端。一名技术评论者强调，Cogentic 的整数分解结果虽建立在 GNFS 之上并替换了依赖未证实猜想的部分，却因复杂度代价而未形成对 GNFS 的明确优势，因此启发式基础和实际意义仍比“突破”标签更值得关注。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://magica.com/news/google-cogentic-six-math-papers-factoring-proof-claim">Google Cogentic claims new factoring bound in six math papers ...</a></li>
<li><a href="https://github.com/google-research/google-research/tree/master/cogentic_research_papers">Google Releases Cogentic Papers on Integer Factorization ...</a></li>

</ul>
</details>

**标签**: `#cryptography`, `#integer-factorization`, `#discrete-logarithm`, `#AI-for-mathematics`, `#Google-Research`

---

<a id="item-tech-news-4"></a>
### [FCC 条件批准 SpaceX 部署百万颗 Starmind 卫星](https://arstechnica.com/space/2026/11/the-fcc-has-authorized-spacex-to-deploy-1-million-satellites/) ⭐️ 8.0/10

美国联邦通信委员会（FCC）有条件批准 SpaceX 部署最多 100 万颗配备 AI 芯片的 Starmind 卫星，用于建设在轨数据中心星座；若全部建成，轨道卫星数量将增加约 50 倍。SpaceX 获准在六条轨道运行，轨道高度约 550 至 1000 公里，并须在七年内部署首颗可运行卫星、到 2035 年 11 月部署 10 万颗、到 2040 年 11 月完成整个星座。授权条件包括通信备份、定期提交进展报告和轨道碎片减缓方案，并允许 600 公里以上的退役卫星进入地球处置轨道或日心轨道。FCC 驳回了亚马逊、Viasat 和美国天文学会的部分反对意见，但此次批准并不能证明在轨数据中心在技术或经济上可行，也不保证百万颗卫星会按期建成并成功运营。

rss · Ars Technica · 11月25日 18:22

**「背景」** 与主要承担信号转发的通信卫星不同，Starmind 设想让卫星搭载 AI 芯片并在轨道上承担数据处理，因此属于“轨道数据中心”星座方案。FCC 对此类非地球同步轨道（NGSO）卫星系统的授权属于联邦监管许可，SpaceX 此前 Gen2 NGSO 系统的部分授权及待决复议构成相关监管背景；因此，本次有条件许可并不等同于 FCC 已验证该架构在技术和经济上可行。

**「实际影响」** 对 SpaceX 而言，这项有条件授权清除了部署 Starmind 星座的关键监管门槛，使其可在七年内投运首颗卫星，并在 2035 年 11 月前部署 10 万颗、2040 年 11 月前完成整个星座；FCC 还批准了部分规则豁免，并驳回 Amazon、Viasat 和美国天文学会的反对意见。该决定并不保证 SpaceX 会完成建设，也未证明在轨数据中心在技术和商业上可行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.fcc.gov/document/fcc-authorizes-1-million-satellites-data-centers-space-0">FCC Authorizes 1 Million Satellites for Data Centers in Space</a></li>
<li><a href="https://docs.fcc.gov/public/attachments/DA-26-36A1.txt">docs.fcc.gov/public/attachments/DA-26-36A 1 .txt</a></li>
<li><a href="https://www.satellitetoday.com/connectivity/2026/11/25/fcc-approves-spacexs-1-million-satellite-orbital-data-center-constellation/">FCC Approves SpaceX’s 1-Million Satellite Orbital Data Center ...</a></li>
<li><a href="https://spaceflightnow.com/2026/11/26/fcc-green-lights-spacexs-plan-to-launch-1-million-starmind-data-center-satellites/">FCC green lights SpaceX’s plan to launch 1 million ‘Starmind ...</a></li>

</ul>
</details>

**标签**: `#orbital data centers`, `#satellite constellations`, `#FCC regulation`, `#SpaceX`, `#space computing`

---

<a id="item-tech-news-5"></a>
### [数据中心遭军事袭击或不会停止](https://arstechnica.com/gadgets/2026/11/ars-live-recap-dont-expect-military-attacks-on-data-centers-to-stop/) ⭐️ 8.0/10

Ars Technica 围绕数据中心正日益成为军事目标举行了现场讨论。报道称，2026 年中东首次出现针对亚马逊数据中心的军事袭击，俄罗斯与乌克兰也相互发动了前所未有的密集无人机打击，相关讨论聚焦此类行动对云服务可靠性、基础设施韧性及军民两用云计算的影响。英国皇家联合军种研究所的约瑟夫·雅尔内茨基指出，军队已将公共云和私人云数据中心用于战场管理、人力资源及资源管理，因此这些设施可能被视为军事目标并招致攻击。他还强调，便宜的“神风”无人机能以较低弹药成本造成广泛云中断和巨额经济损失，并非常保守地估计 AWS 等海湾数据中心投资与所用 Shahed 无人机成本之比至少可达 100 倍，甚至更高；讨论同时提及乌克兰在 2022 年 2 月俄罗斯全面入侵后采取的云基础设施防护措施，但所供摘录未展示具体方案。

rss · Ars Technica · 11月25日 16:47

**「背景」** 云计算数据中心兼具民用与军事用途：英国皇家联合军种研究所研究员约瑟夫·雅尔内茨基指出，军方使用其计算资源执行战场管理、人力资源和资源管理后，这类设施可能因“双重用途”而成为军事目标。与此同时，包括 Shahed 在内的廉价神风无人机可用较低的弹药成本攻击高投入的数据中心，从而将局部打击放大为广泛的云服务和经济中断。俄乌自 2022 年 2 月全面入侵以来针对数据中心及云基础设施的袭击与防护实践，构成了此次讨论的历史背景。

**「具体影响」** 对依赖受影响区域云服务的客户，军事打击已造成超出短暂宕机的实际后果：AWS 确认中东受战争影响的数据中心中部分客户数据永久无法恢复，Amazon 据报道仍需数月才能完成修复并恢复正常运营。由此，依赖单一区域云资源的组织面临数据永久丢失与服务中断长期化的双重风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arstechnica.com/gadgets/2026/11/ars-live-recap-dont-expect-military-attacks-on-data-centers-to-stop/">Ars Live recap: Don’t expect military attacks on data centers ...</a></li>
<li><a href="https://cybersecuritynews.com/aws-cloud-data-war-damage/">AWS Says Some Cloud Data Cannot Be Recovered After Data ...</a></li>
<li><a href="https://arstechnica.com/gadgets/2026/05/amazon-stuck-with-months-of-repairs-after-drone-strikes-on-data-centers/">Amazon stuck with months of repairs after drone strikes on ...</a></li>

</ul>
</details>

**标签**: `#cloud infrastructure`, `#data center security`, `#cloud resilience`, `#military conflict`, `#geopolitics`

---

<a id="item-tech-news-6"></a>
### [Hera 揭示小行星撞击后的混沌现场](https://arstechnica.com/space/2026/11/europes-hera-mission-returns-to-the-chaotic-scene-of-a-cosmic-smashup/) ⭐️ 7.0/10

欧洲航天局的 Hera 航天器抵达双星系统 Didymos 与 Dimorphos 附近，并发布首批影像，揭示 NASA“双星小行星重定向测试”（DART）撞击 Dimorphos 后留下的巨大陨石坑和复杂碎片场。DART 于 2022 年 9 月以每秒 6.14 公里撞击这颗直径约 151 米的小行星，释放约 100 亿焦耳能量，使其绕 Didymos 的 12 小时轨道缩短约 33 分钟，达到保守预期的 25 倍。由于撞击探测器 DART 损毁且地面望远镜只能观测撞击闪光，研究团队此前一直无法确认撞击形成的具体破坏形态；Hera 的首批观测填补了这一关键信息缺口。这项试验证明撞击式偏转能够有效改变小行星轨道，对行星防御具有重要意义，而 Didymos 和 Dimorphos 虽然类似许多近地小行星，但目前没有撞击地球的风险。

rss · Ars Technica · 11月25日 22:36

**「背景」** DART（“双小行星重定向测试”）是 NASA 于 2022 年撞击 Didymos 的小卫星 Dimorphos 的动能撞击器试验，旨在验证改变小行星轨道、用于行星防御的技术路径。撞击使 Dimorphos 绕 Didymos 的运行周期缩短约 33 分钟，但地面望远镜无法近距离查清撞击坑、碎片和动量传递等细节。欧洲航天局的 Hera 是后续勘测任务，将近距离观测撞击后果，以评估动能撞击器能否成为可靠部署的行星防御手段。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.esa.int/articles/about-us/directorates/operations/space-safety/hera/hera-reveals-stadium-sized-asteroid-crater-left-after-spacecraft-impact">Hera reveals stadium-sized asteroid crater from spacecraft impact</a></li>
<li><a href="https://www.esa.int/missions/about-us/directorates/operations/space-safety/hera">Hera - European Space Agency</a></li>

</ul>
</details>

**标签**: `#asteroid deflection`, `#planetary defense`, `#spacecraft`, `#DART`, `#Hera mission`

---

<a id="item-tech-news-7"></a>
### [Ladybird 发布首个可下载 Alpha 版本](https://arstechnica.com/gadgets/2026/11/ladybirds-new-alpha-shows-theres-life-beyond-chromium/) ⭐️ 7.0/10

Ladybird 项目于 11 月 23 日发布首个可下载的 Alpha 版本，为 macOS 和 Linux 提供预构建安装包和自动更新；此前，用户必须自行从源码编译。其渲染引擎与 LibJS JavaScript 引擎均由项目从零开发，并非 Chrome、Edge、Brave 和 Opera 所用 Blink 或 Firefox 所用 Gecko 的分支，项目负责人 Andreas Kling 称当前浏览器较为基础但可正常使用。这一独立实现为 Web 标准增加了可供测试的引擎，有助于暴露网站对 Chromium 特有行为的依赖，并推动生态更贴近正式规范。Ladybird 源自 Andreas Kling 的 SerenityOS 项目，现由接受赞助和捐赠的 501\(c\)\(3\) 非营利组织 Ladybird Browser Initiative 运作，且没有赞助搜索引擎协议；但该 Alpha 版本尚不足以证明其具备广泛网站兼容性或重大行业影响力。

rss · Ars Technica · 11月25日 17:33

**「项目背景」** 现代网页主要由 WebKit、Gecko 和 Blink 三类浏览器引擎实现，Chrome、Edge、Brave 和 Opera 共用 Blink，Firefox 则使用 Gecko。Ladybird 源于 Andreas Kling 的独立操作系统项目 SerenityOS，之后分离为独立项目，并从头开发自己的渲染引擎和 LibJS JavaScript 引擎，而不是分支自现有浏览器。该项目由 Ladybird Browser Initiative 这一美国 501\(c\)\(3\) 非营利组织运营，依靠赞助和捐赠维持，目前没有赞助搜索引擎协议。

**「实际影响」** macOS 和 Linux 用户现在无需自行编译源码，即可安装 Ladybird 的首个可下载 Alpha 并通过自动更新持续试用这套独立引擎，开发者也能更方便地测试其 Web 标准兼容性。现阶段的影响主要是扩大测试与反馈样本，而非证明它已具备主流浏览器的完整兼容性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/SerenityOS">SerenityOS - Wikipedia</a></li>
<li>Ladybird browser&#x27;s first downloadable alpha is surprisingly capable</li>
<li><a href="https://en.wikipedia.org/wiki/Ladybird_%28web_browser%29">Ladybird (web browser) - Wikipedia</a></li>
<li><a href="https://ladybird.org/">Ladybird</a></li>
<li><a href="https://github.com/LadybirdBrowser/ladybird">GitHub - LadybirdBrowser/ladybird: Truly independent web ...</a></li>

</ul>
</details>

**标签**: `#Ladybird`, `#browser engines`, `#JavaScript`, `#open-source software`

---

<a id="item-tech-news-8"></a>
### [华为被美陪审团裁定窃密并规避伊朗制裁](https://arstechnica.com/tech-policy/2026/11/jury-convicts-huawei-of-stealing-us-trade-secrets-evading-iran-sanctions/) ⭐️ 7.0/10

美国陪审团周二裁定华为技术有限公司犯有窃取美国科技企业商业秘密及规避对伊朗制裁等罪行，相关指控可追溯至 2018 年。华为被判罪名包括银行欺诈、合谋欺诈美国、洗钱合谋，以及实质性违反《国际紧急经济权力法》；美国司法部称，华为曾反复向银行和美国政府谎报其伊朗业务。检方称，华为以“Skycom”为名在伊朗经营，向其提供互联网骨干网和移动网络接入的整套服务、互联网监控与审查能力，以及用于监控抗议的监控摄像头，其窃密目标包括 T-Mobile、Cisco、存储半导体企业 CNEX 和天线制造商 Quintel。美国司法部认为，华为借助全球市场准入持续获得数十亿美元，并借此接触和窃取美国技术；判决发生在特朗普准备提高对华关税之际，可能进一步加剧中美紧张。所给材料未说明具体量刑期限或罚款金额。

rss · Ars Technica · 11月25日 16:33

**「案件背景」** 该案由美国纽约东区联邦法院审理，相关指控可追溯至 2018 年，经过约三个月审判后，陪审团作出有罪裁决。案件包含两条法律性质不同的主线：华为被控不当获取 T-Mobile、思科等美国企业的商业秘密，同时通过“Skycom”在伊朗开展业务并隐瞒交易，涉及银行欺诈、洗钱及违反美国对伊制裁规定；其中《国际紧急经济权力法》（IEEPA）是美国在国家紧急状态下实施经济制裁的重要法律依据。

**「直接影响」** 华为及三家子公司在 12 项指控中有 10 项被裁定有罪，将进入量刑阶段并可能面临罚款及其他刑事处罚，使其在美经营和参与全球金融体系的合规风险进一步上升。具体量刑尚未确定，但该定罪还可能加剧美中科技与贸易紧张。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.justice.gov/opa/pr/chinese-tech-giant-huawei-and-subsidiaries-convicted-sanctions-violations-fraud-conspiracy">Office of Public Affairs | Chinese Tech Giant Huawei and ...</a></li>
<li><a href="https://arstechnica.com/tech-policy/2026/11/jury-convicts-huawei-of-stealing-us-trade-secrets-evading-iran-sanctions/">Jury convicts Huawei of stealing US trade secrets, evading ...</a></li>
<li><a href="https://www.cnn.com/2026/11/24/china/china-huawei-iran-conviction-intl-hnk">US court convicts China ’s Huawei for fraud, conspiring to steal trade ...</a></li>
<li><a href="https://www.foxbusiness.com/fox-news-tech/federal-jury-convicts-huawei-stealing-us-trade-secrets-violating-iran-sanctions">Federal jury convicts Huawei of stealing US trade secrets , violating...</a></li>
<li><a href="https://arstechnica.com/tech-policy/2026/11/jury-convicts-huawei-of-stealing-us-trade-secrets-evading-iran-sanctions/">Huawei didn’t try very hard to hide thefts of US trade secrets , DOJ says.</a></li>

</ul>
</details>

**标签**: `#Huawei`, `#trade secrets`, `#telecommunications`, `#sanctions`, `#US-China tech policy`

---

<a id="item-tech-news-9"></a>
### [伊朗黑客大规模操纵法国超市制冷系统](https://arstechnica.com/security/2026/11/a-familiar-iranian-hacking-group-has-found-a-new-way-to-cause-chaos/) ⭐️ 7.0/10

据报道，10 月一夜，攻击者操纵了法国数百家超市的商用冷藏和冷冻系统，升高温度并造成数百万欧元食品损失，这是已知针对商业制冷系统规模最大、且发生在欧洲腹地的类似攻击。法国情报机构在数字痕迹中发现波斯语（Farsi）及其他线索，指向伊斯兰革命卫队网络电子司令部下属的精英黑客单位“Shahid Kaveh”；该组织常以“CyberAv3ngers”名义活动，但这一归因仍属指称。该单位曾于 2023 年和 2024 年攻击美国多个州供水、制造和交通系统中的以色列制造工业控制设备，虽然运营中断有限，但每次都会留言称“每一台‘以色列制造’的设备都是 CyberAv3ngers 的合法目标”。分析人士将此次事件视为伊朗网络战策略升级及更愿意打击欧洲基础设施的迹象；欧洲对外关系委员会的 Ellie Geranmayeh 认为，这也呼应了伊朗因被排除在全球经济之外而发出的 disrupt 威胁。

rss · Ars Technica · 11月25日 14:29

**「背景：从控制系统到实体运营」** 网络物理攻击可通过入侵运营技术直接干扰现实设施；针对商用冷柜和冷库的攻击此前已有先例，但此次法国事件的规模和地域影响显著更大。法国情报机构据称根据数字活动中的波斯语等线索，将攻击指向伊斯兰革命卫队网络电子司令部下属的精英黑客组织 Shahid Kaveh，该组织也常以 CyberAv3ngers 名义活动。2023 年和 2024 年，该组织曾侵入美国多个州水务、制造和运输系统中的以色列制造工业控制设备，但当时造成的运营中断有限。

**「网络入侵可转化为实体食品损失」** 此次事件表明，商用制冷和工业控制系统遭入侵后，攻击者能够直接造成食品报废、门店运营中断和实体经济损失，而不只是篡改数据或显示界面。现有报道未披露具体入侵路径、受影响设备类型及支撑归因的技术证据，因此攻击的可复制性和防御缺口仍无法确定。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ft.com/content/5f3a85ad-e621-4189-bada-989f41702ed9?syn-25a6b1a6=1">The secretive Iranian cyber unit behind Europe’s freezer hacks</a></li>
<li><a href="https://www.irishtimes.com/world/middle-east/2026/11/25/the-secretive-iranian-cyber-unit-behind-europes-freezer-hacks/">The secretive Iranian cyber unit behind Europe’s freezer hacks</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#cyber-physical attacks`, `#operational technology`, `#Iranian threat actors`, `#critical infrastructure`

---

<a id="item-tech-news-10"></a>
### [纽约禁止 AI 聊天机器人玩具五年](https://techcrunch.com/2026/11/25/want-to-buy-your-kid-an-ai-toy-this-christmas-not-in-new-york/) ⭐️ 7.0/10

纽约已禁止 AI 聊天机器人玩具，禁令期限为五年；据报道，这使当地消费者今年圣诞节无法购买此类产品。Common Sense Media 的新研究指出，这类玩具存在安全失效，包括让儿童接触不合适内容的风险，以及可能影响其情绪发展的风险。纽约因此不只是收到风险警告，而是以五年期禁令对相关产品作出监管限制。不过，现有材料没有说明禁令究竟覆盖销售、持有、使用还是其他环节，也未交代研究的方法、样本和效果数据，因此其精确范围与证据强度仍不确定。

rss · TechCrunch · 11月25日 18:11

**「监管背景」** AI 聊天机器人玩具是指将生成式 AI 对话功能嵌入实体玩具，使儿童能够通过文字或语音与虚拟角色交流。纽约州长凯茜·霍赫尔签署的法案所设的“五年禁令”更准确地说是一项暂停措施：在签署 90 天后生效后，禁止制造、分销和销售面向 18 岁以下用户的这类玩具，直至制定相应安全规范（tool-1-1、tool-1-2）。

**「用户影响」** 纽约州将五年禁止制造和销售 AI 聊天机器人玩具，包括可联网与儿童对话的毛绒动物、洋娃娃和机器人，因此当地消费者无法购买此类产品，制造商和零售商也无法在州内合法销售。

<details><summary>参考链接</summary>
<ul>
<li>Governor Kathy Hochul | New York State</li>
<li>New York placed a moratorium on the manufacturing, distribution and sale ...</li>
<li><a href="https://www.theguardian.com/us-news/2026/nov/25/new-york-bans-ai-toys">New York bans AI toys , including those using internet to talk to children</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#AI regulation`, `#chatbots`, `#children&\#x27;s technology`

---

<a id="item-tech-news-11"></a>
### [州检察长反对拍卖 Character.AI 私聊](https://techcrunch.com/2026/11/25/state-ags-fight-character-ais-plan-to-auction-off-users-private-chats/) ⭐️ 7.0/10

美国多州总检察长反对 Character.AI 将用户私人聊天纳入拟议破产拍卖的计划，担心敏感个人数据可能随交易被转移或披露。总检察长称，相关数据涉及超过 2100 万个美国账户，其中约 210 万个账户注册者为未成年人。这起争议将平台破产处置与聊天隐私及未成年人数据保护直接联系起来。现有信息未说明具体参与州、反对理由细节或交易结构，也无法判断该挑战的结果。

rss · TechCrunch · 11月25日 17:35

**「背景」** Character.AI 是一款生成式 AI 聊天平台，用户与虚拟角色互动产生的私人对话可能包含个人及敏感信息。此次争议源于该公司的破产资产出售计划；由 42 名州总检察长组成的跨党派联盟反对将平台及逾 2100 万美国账户的聊天记录拍卖，称其中包括逾 210 万未成年人注册账户，且交易缺少保护聊天者的隐私措施。

**「用户隐私风险」** 如果州总检察长的异议未能阻止出售，买方可能取得逾 2100 万美国账户的私人聊天数据，其中包括 210 万未成年人账户，使相关用户面临敏感对话被转移或泄露的风险；该方案目前仍处于破产出售提案阶段，不能认定数据已经出售。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://oag.ca.gov/news/press-releases/attorney-general-bonta-opposes-asset-sale-characterai-amid-child-safety-concerns">Attorney General Bonta Opposes Asset Sale of Character.AI ...</a></li>
<li><a href="https://portal.ct.gov/ag/press-releases/2026-press-releases/attorney-general-tong-challenges-plan-to-auction-off-character-ai-private-chats">Attorney General Tong Challenges Plan to Auction Off ...</a></li>
<li><a href="https://coag.gov/press-releases/weiser-challenges-auction-of-millions-of-private-character-ai-conversations/">Attorney General Weiser challenges auction of millions of ...</a></li>
<li><a href="https://techcrunch.com/2026/11/25/state-ags-fight-character-ais-plan-to-auction-off-users-private-chats/">Character . AI ’s plan to auction off users’ private chats ... | TechCrunch</a></li>

</ul>
</details>

**标签**: `#AI`, `#Data Privacy`, `#Character.AI`, `#Legal Regulation`

---

<a id="item-tech-news-12"></a>
### [sqlite3\_rsync：低磁盘占用的 SQLite 快照复制](https://simonwillison.net/2026/Nov/26/sqlite3-rsync/) ⭐️ 6.0/10

SQLite 的附加工具 sqlite3\_rsync 可通过 SSH 将数据库快照复制到另一台机器，无需先在源端创建完整本地副本，因此适合磁盘空间有限、已使用过半容量的实例。该工具于 SQLite 3.47.0（2024 年 10 月）以实验性功能加入，并在 SQLite 3.50.0（2025 年 5 月）得到增强。它也能与已有副本增量同步，只传输不同页面：副本端发送页面或页组的密码学哈希，源端返回差异内容，必要时要求更细粒度的哈希。若两端文件差异极大，哈希交换会带来额外流量，源文称超出整个数据库大小的幅度最多仅为几个百分点。

rss · Simon Willison · 11月26日 06:08

**「背景」** 传统上，通过 SQLite Backup API 或 VACUUM INTO 获取快照，都要求源端有足够磁盘空间容纳数据库的完整副本。sqlite3\_rsync 的工作方式类似 rsync，借助页面级哈希识别差异并复制数据库快照，从而绕开先创建本地完整副本这一空间要求。

**「实际影响」** 对于磁盘空间紧张、需要跨机器复制 SQLite 数据库快照的运维人员，sqlite3\_rsync 可直接通过 SSH 传输快照，并在同步已有副本时只交换差异，避免创建完整本地副本或重复传输整个数据库。若两端数据库差异极大，哈希协商产生的额外网络开销最多约为几个百分点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.sqlite.org/rsync.html">Database Remote-Copy Tool For SQLite</a></li>

</ul>
</details>

**标签**: `#SQLite`, `#Database Backup`, `#rsync`, `#Data Replication`

---

<a id="item-tech-news-13"></a>
### [Evaluating Recent Model Releases on GDPx](https://newsletter.semianalysis.com/p/evaluating-recent-model-releases) ⭐️ 6.0/10

The article compares recent model releases on GDPx, highlighting strong benchmark performance alongside weaknesses in software engineering, overstated capabilities, and high costs.

rss · Semianalysis · 11月26日 00:05

**标签**: `#AI model evaluation`, `#large language models`, `#benchmarks`, `#software engineering`

---

<a id="item-tech-news-14"></a>
### [NVIDIA Nemotron 3.5 Parse 开放训练与推理优化](https://huggingface.co/blog/nvidia/building-on-nemotron-35-parse-open-data-fine-tunin) ⭐️ 6.0/10

NVIDIA Nemotron 3.5 Parse 将文档页面图像转换为结构化数据，按阅读顺序识别标题、段落、表格和图表并输出边界框，表格与图表可生成供 RAG 和智能体使用的结构化记录；新版还强化了对无明确数值标注的柱状图及复杂表格的读取。NVIDIA 开放了三个合成训练集：包含 998 万个图表样本的 Synthetic Charts V1、包含 100 万个表格样本的 Synthetic Tables V1，以及包含 790 万个多语言 OCR 样本的 OCR Synthetic Multilingual v2，每个数据集均提供图像、标注、生成说明和训练格式。Parse 3.5 先通过覆盖文本、版面、表格、图表和多语言文档的监督微调学习目标结构，再使用基于 GRPO 的可验证奖励强化学习；在与最终发布模型分开的开发检查点对比中，被标记为循环的输出从 126 页降至 29 页，约减少 77%，触及 9,000 token 上限的输出从 185 页降至 35 页，总分从 66.24 升至 71.38，其中表格和图表分别提高 5.18 和 4.15 分。推理侧采用 NaViT 动态矩形输入、压缩视觉 token 前缀和 GQA-8，DFlash2 则让小型草稿模型一次提出最多 32 个 token，再由 Parse 统一验证，平均接受约 14 个草稿 token；在单张 H200、BF16、使用同一批 2,078 页的原生单遍测试中，相比禁用推测解码的 Parse 3.5，DFlash2 在并发 1 时将吞吐量提高 7.62 倍，在并发 512 时从 13.48 页/秒提高到 20.44 页/秒，而 Parse 2.0 为 2.98 页/秒，双遍和三遍处理则分别比单遍增加 2.18 和 2.46 个 ParseBench 点，但会消耗更多吞吐量。配套微调流程涵盖成对数据生成、NeMo Automodel SFT、使用 vLLM 生成候选答案的 NeMo RL GRPO；在一个包含 256 份合成牙科表单的参考实验中，采样 pass@1 估算值从基础模型的 0.00% 升至 SFT 后的 95.85%，再由 RLVR 提升至 96.58%。

rss · Hugging Face Blog · 11月26日 05:05

**「相关技术背景」** 文档解析模型需要把页面像素转换为保留阅读顺序、版面关系和元素位置的结构化表示，其中表格、图表和边界框是下游 RAG、智能体检索与核对流程的重要输入。监督微调通过图像与目标结构的成对样本学习格式映射，而基于可验证奖励的强化学习依据抽取正确性和完整完成情况调整策略；推测解码则由较小的草稿模型提前生成 token，再由目标模型批量验证，以减少逐步解码开销。

**「实际影响」** 对于构建文档 RAG 与智能体的开发者和企业，三套合计约 1,880 万条开放合成样本及 NeMo Automodel 的 SFT/GRPO 配方可直接用于适配专有文档和语言；NVIDIA 的单张 H200、BF16 测试还显示，DFlash2 相对关闭推测解码的 Parse 3.5 可将并发 1 吞吐提升 7.62 倍，或通过多遍解析使困难表格和图表增加 2.18–2.46 个 ParseBench 分。不过，这些数值来自 NVIDIA 的受控单卡评测，实际收益仍会随并发、页面难度及多遍处理的开销而变化。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/nvidia/Nemotron-3.5-Parse">nvidia/Nemotron-3.5-Parse · Hugging Face</a></li>
<li><a href="https://build.nvidia.com/nvidia/nemotron-3.5-parse/modelcard">Model Card | nemotron-3.5-parse Model by NVIDIA | NVIDIA NIM</a></li>

</ul>
</details>

**标签**: `#document parsing`, `#RAG agents`, `#synthetic training data`, `#fine-tuning and reinforcement learning`, `#inference optimization`

---

<a id="item-tech-news-15"></a>
### [IBM 用 CUGA 构建印度语言语音智能体](https://huggingface.co/blog/ibm-research/an-indic-voice-agent-with-cuga) ⭐️ 6.0/10

IBM Research 基于开源 CUGA（Configurable Generalist Agent）智能体框架构建了一个小型印度语言语音智能体，用户可用印地语、泰米尔语等语言询问如何辨别种子好坏，答案由检索到的农业资料生成。该方案将 CUGA 作为嵌入式 SDK，利用其模型连接、工具管理、状态与护栏能力，把语音链路拆分为语音转文本、知识检索、CUGA 生成有依据的回答及文本转语音，并支持 Sarvam AI 云端 API 或自托管的 SraVaani 与 Svara 模型。关键难点是跨语言检索：CUGA 默认的英语嵌入模型会为非英语问题返回无关段落且不报错，团队改用 intfloat/multilingual-e5-large，并通过教程中的小幅适配解决，使同一批英文文档能够服务多种语言。智能体还能利用 OFF\_TOPIC 将板球或编程问题礼貌引回农业领域，且无需第二次调用大语言模型；通过替换知识库可扩展到医疗、法律或政府服务，并可在云端与本地部署之间切换以满足数据主权要求。文章称 CUGA 是 AppWorld Benchmark 的领先者，但所给内容没有列出具体基准结果，因此这一排名无法仅凭本文内容得到验证。

rss · Hugging Face Blog · 11月25日 10:22

**「背景」** CUGA（Configurable Generalist Agent）是 IBM Research 的开源智能体框架，负责模型接线、工具管理、状态和护栏，开发者则通过编写工具与提示词定义代理行为。该语音方案采用“语音转文本—文本代理—文本转语音”的架构，使 CUGA 核心始终只处理文本，并可灵活替换云端或自托管语音模型。多语言检索是其关键难点：由于 CUGA 默认的嵌入模型仅支持英语，印地语等查询虽能返回结果却往往语义不匹配，因此示例改用 intfloat/multilingual-e5-large，使不同语言中的相同含义能够映射到相近的向量空间。

**「...」** ...

<details><summary>参考链接</summary>
<ul>
<li>An Indic Voice Agent with CUGA - Hugging Face</li>
<li><a href="https://huggingface.co/blog/ibm-research/cuga-harness">Same Model, Different Harness: CUGA , Hermes, and Deep Agents ...</a></li>
<li><a href="https://www.youtube.com/watch?v=2Pc1YeKBTms">IBM CUGA Agent Harness: Same Model Scores 30% vs 81... - YouTube</a></li>

</ul>
</details>

**标签**: `#voice-agents`, `#agent-frameworks`, `#indic-languages`, `#open-source`, `#guardrails`

---

<a id="item-tech-news-16"></a>
### [欧盟拟设 550 亿美元基金支持 AI 与量子技术](https://news.google.com/rss/articles/CBMi-AFBVV95cUxNQ0t5eEphdWw0c05LVkNKUHNiMFdrNlRoSHVHMndudEFVYnQ4UGYzbm5QTllJcmtSODRKOE1kQ2JDazZhdEV0UmxMakl6d1ZxX0tnUXhXdzI5cjdKc1l0X3ZJc1NOdkFpREo1em42M0syQW9Qak9pWkJFZW9xWDFORjBMVTFVQzVkV1I1aEVHNGloaFlGOVlKUEI5SHcxdWtCbG1iOXp2VDlIZ29ISDdWdkR1UnctTVFhSWxlN2NwWVdoMnZpajJscWpqZlNNODlqWXJwU2hUQ1cySjlyT2Z3TjF6dTJxUlEwUjl3TDYwZGdSWGIyRDgzSQ?oc=5) ⭐️ 6.0/10

据 Forbes Middle East 经 Google News 发布的标题，欧盟计划设立规模达 550 亿美元的技术基金，重点支持人工智能和量子计算能力，以缩小相关差距并降低对美国和中国技术的依赖。该计划旨在推动欧洲战略技术能力建设，但现有材料仅提供标题，未说明资金来源与结构、实施时间表、覆盖项目、拨款机制或官方确认。其具体规模、可行性和落地条件因此仍无法核实。

google\_news · Forbes Middle East · 11月25日 17:42

**「背景」** 报道所说的“缩小差距”，是指欧盟整体在人工智能、量子计算等关键技术上的能力差距。人工智能利用数据和模型形成智能能力，量子计算则利用量子态处理特定计算任务；报道所称基金最高为 550 亿美元（500 亿欧元），也覆盖其他关键技术，目标是降低欧盟对美国和中国技术力量的依赖。

**「潜在影响」** 若计划得以实施，面向欧洲人工智能和量子计算企业的长期高风险投资最多将达 500 亿欧元，可能降低欧盟对美国和中国技术供应的依赖；但基金结构、落地时间及受益范围尚未确定。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.forbesmiddleeast.com/innovation/artificial-intelligence-machine-learning/eu-plans-55b-tech-fund-to-narrow-ai-and-quantum-gap-reducing-us-and-china-dependence">EU Plans $55B Tech Fund To Narrow AI And Quantum Gap</a></li>
<li><a href="https://www.ft.com/content/53d4b629-7ae4-4d63-ac37-e773b1dd3af0?syn-25a6b1a6=1">EU plans €50bn tech fund to close gap with US and China</a></li>

</ul>
</details>

**标签**: `#European Union`, `#Technology Policy`, `#Artificial Intelligence`, `#Quantum Computing`, `#Strategic Funding`

---