---
layout: default
title: "Horizon Summary: 2026-11-09 (ZH)"
date: 2026-11-09
lang: zh
---

> 从 70 条内容中筛选出 11 条重要资讯。

---

**科技新闻**
1. [高盛据报撤回银行家与交易员的 Claude Code 权限](#item-tech-news-1) ⭐️ 7.0/10
2. [Nvidia is investigating Jensen Huang’s relationship with a Chinese spy](#item-tech-news-2) ⭐️ 7.0/10
3. [iOS 27.2 沙盒逃逸 PoC 被公开](#item-tech-news-3) ⭐️ 7.0/10
4. [剑桥 AI 设计禽流感候选疫苗](#item-tech-news-4) ⭐️ 7.0/10
5. [SQLite parse\_number 扩展：C 与 Rust 对比](#item-tech-news-5) ⭐️ 6.0/10
6. [物理学家借电流噪声破解超导谜团](#item-tech-news-6) ⭐️ 6.0/10
7. [Epic Games 启动器确认支持 SteamOS](#item-tech-news-7) ⭐️ 6.0/10
8. [苹果正加速推进智能体式 Siri](#item-tech-news-8) ⭐️ 6.0/10
9. [埃尔维斯与 Eminem 权利方起诉 Suno](#item-tech-news-9) ⭐️ 6.0/10
10. [华为称已打造全中国组件 PC](#item-tech-news-10) ⭐️ 6.0/10
11. [国际电联将审议 278 项互联网治理提案](#item-tech-news-11) ⭐️ 6.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [高盛据报撤回银行家与交易员的 Claude Code 权限](https://www.thestateofai.com/news/goldman-sachs-claude-code-traders-bankers) ⭐️ 7.0/10

据 The State of AI 报道，Goldman Sachs（高盛）正在撤回银行家和交易员对 Anthropic Claude Code 的使用权限，限制这款代理式编码工具在这些岗位上的可用性。由于现有材料没有高盛官方公告或报道原文，调整的具体范围、实施时间及原因尚无法确认，安全、合规、权限管理和使用成本目前只能视为可能因素。这一动作表明，受监管金融机构采用代理式 AI 时，不仅要评估其编码能力，还必须控制代理对敏感数据、邮件、内部网络和可审计工作流的访问。对企业 AI 而言，这也是从试点走向生产时遭遇治理与成本约束的一个具体案例。

hackernews · TheWiggles · 11月8日 18:16 · [社区讨论](https://news.ycombinator.com/item?id=50415628)

**「背景」** Claude Code 是 Anthropic 的代理式编码工具，可在获授权的开发环境中读取和修改代码，并通过获准工具执行多步骤任务，而不只是提供文本建议。金融机构通常要求细粒度访问控制、数据与模型使用许可、可审计的审批链以及明确的责任边界，因此将此类代理接入个人工作站或内部系统的门槛较高。

**「直接影响」** 最直接影响是受影响的银行家和交易员将失去或收紧 Claude Code 能力，可能需要改用其他工具或经批准的人工流程完成相关任务，但现有材料不足以判断这是全面撤销、临时暂停还是局部授权调整。

**「社区讨论」** 评论者没有形成单一结论：一种观点认为，让半无人值守代理在同一工作站接触客户、交易和专有信息、邮箱、互联网及内部网络，会形成直接的安全风险。另一位称其所在组织因持续账单超额而收回 Claude Code 权限，并称 Anthropic 缺乏统一费率，而 Gemini 的平坦计费与限流更有吸引力；也有人猜测公告时机与 Anthropic IPO 临近或操作事故有关，并强调数据许可、细粒度授权和审批链，但这些原因均未获高盛证实。

**标签**: `#enterprise AI`, `#coding agents`, `#AI security`, `#financial services`, `#Claude Code`

---

<a id="item-tech-news-2"></a>
### [Nvidia is investigating Jensen Huang’s relationship with a Chinese spy](https://www.theverge.com/ai-artificial-intelligence/1029562/nvidia-investigating-jensen-huang-relationship-chinese-spy) ⭐️ 7.0/10

Nvidia’s board has opened an independent investigation into CEO Jensen Huang’s relationship with Megaspeed executive Alice Huang, reportedly recruited by China’s Ministry of State Security to spy on the company.

rss · The Verge · 11月8日 20:22

**标签**: `#Nvidia`, `#Jensen Huang`, `#corporate governance`, `#China`, `#espionage`

---

<a id="item-tech-news-3"></a>
### [iOS 27.2 沙盒逃逸 PoC 被公开](https://x.com/forcequitOS/status/2119475139528020218?) ⭐️ 7.0/10

forcequitOS 于 11 月 8 日公开名为 worse\_query 的 iOS 沙盒逃逸概念验证（PoC），称其支持 iOS 26.0–26.7.2、iOS 27.2，并包含 27.3 beta。该漏洞被描述为 bad\_query 的继任者，利用前提是目标应用配置了 App Group；据发布者称，PoC 可访问系统路径并修改应用数据，但这一能力仅用于开发研究，并非越狱。发布者表示漏洞报告已提交苹果、但当时尚未封堵，社区随后出现了 GestaltX 等衍生工具；不过现有材料没有提供漏洞实现细节、苹果的补丁确认或独立验证，因此其“零日”状态及实际影响仍待核实。

telegram · zaihuapd · 11月9日 02:36

**「iOS 沙盒逃逸背景」** iOS 沙盒用于隔离应用进程及其数据，沙盒逃逸 PoC 则用于验证应用是否能越过系统授予的访问边界。worse\_query 被其作者描述为 bad\_query 的直接继任者，使用前需为应用配置 App Group 容器，并被定位为面向开发者的研究性概念验证，而非单独的通用攻击工具。

**「潜在影响」** 在 iOS 26.0–26.7.2 和 27.2（来源还称涵盖 27.3 beta）上，具备合适 App Group 容器配置的应用或研究者可利用 worse\_query 访问受限系统路径并修改应用数据，扩大沙盒权限。实际利用仍依赖 App Group 条件，公开 PoC 本身并非通用越狱能力，且漏洞是否尚未修复尚缺少苹果公告或独立验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/forcequitOS/worse_query">forcequitOS / worse _ query : A sandbox escape for iOS 26 and 27...</a></li>
<li><a href="https://github.com/forcequitOS/worse_query">GitHub - forcequitOS/ worse _ query : A sandbox escape for iOS 26...</a></li>

</ul>
</details>

**标签**: `#iOS`, `#沙盒逃逸`, `#零日漏洞`, `#漏洞研究`, `#安全工具`

---

<a id="item-tech-news-4"></a>
### [剑桥 AI 设计禽流感候选疫苗](https://www.cam.ac.uk/stories/ai-developed-vaccines-against-viruses) ⭐️ 7.0/10

剑桥大学团队等机构于 2026 年 11 月在线发表于《Cell Reports Medicine》的一项研究显示，AI 辅助设计的禽流感候选疫苗在小鼠和雪貂实验中产生了广谱免疫与保护效果，优于研究中基于 WHO 候选疫苗病毒制备的对照制剂。团队人工设计的广谱抗原在自然界中并不存在，旨在利用 AI 加快疫苗抗原设计并为应急应用做准备。该候选疫苗下一步计划推进人体临床试验，以验证其在人群中的安全性、免疫原性和保护效果；目前仅有动物试验结果，尚未证实能够保护人类。

telegram · zaihuapd · 11月9日 03:00

**「研究背景」** 这项研究的关键背景是，人工智能被用于设计自然界不存在的广谱流感抗原，目标是诱导针对多种流感病毒的免疫反应；对照制剂则采用基于 WHO 候选疫苗病毒的抗原。小鼠和雪貂试验属于人体试验前的动物评估阶段，其结果不能证明候选疫苗已经能在人群中提供保护，仍需后续临床试验验证。

**「对疫苗研发与应急应用的影响」** ...

**标签**: `#AI辅助药物设计`, `#禽流感疫苗`, `#动物实验`, `#计算生物学`

---

<a id="item-tech-news-5"></a>
### [SQLite parse\_number 扩展：C 与 Rust 对比](https://simonwillison.net/2026/Nov/8/sqlite-parse-number-c-vs-rust/) ⭐️ 6.0/10

Simon Willison 使用 Claude Opus 5.5 协助实现 SQLite 可加载扩展 parse\_number\(value\)，用于把带有负号、逗号、美元或英镑符号及百分号的字符串转换为可求和和排序的数值，无法解析时返回 NULL。首版 Rust 扩展分别借助 rusqlite 和 sqlite-loadable-rs，生成的 .so 文件为 321 KB 和 298 KB，而 C 扩展仅 14 KB；Rust 版本起初反而更快，Willison 称 Rust 中与 C 的 strtod 对应的实现“快两倍”。在 200 万行基准的每行净成本测试中，初版 C、Rusqlite 和 sqlite-loadable-rs 分别为混合数据 67、46、41 ns，整数 25、36、32 ns，小数 106、55、47 ns；要求模型改写 C 解析器后，C 降至 19、16、18 ns，三组均领先。该实验显示，在这个原型中，定制 C 解析器能以远小于首版 Rust 扩展的体积取得更低开销，说明所用语言并不必然决定性能；不过材料未完整交代基准方法，因此这些数字不宜直接外推为 C 普遍优于 Rust。Willison 最终让 Claude 将调查整理成 GitHub research 报告。

rss · Simon Willison · 11月8日 22:26

**「背景」** SQLite 的可加载扩展机制允许开发者注册自定义 SQL 函数；这里的 parse\_number\(\) 用于把包含千位分隔符、货币符号或百分号的文本转换为可排序和求和的数值，并对无法解析的输入返回 NULL。实现比较涉及字符串到数值转换的不同路径：C 版本可使用标准库函数 strtod，而 Rust 版本采用功能相近但性能特征不同的解析方式，因此扩展体积和速度不能仅按编程语言判断。

**「实际影响」** 对需要部署可加载 SQLite 扩展的开发者，这一原型显示 C 实现可在初版扩展仅 14 KB 的基础上，经重写将 parse\_number\(\) 的每行成本降至 16–19 ns，低于两个 Rust 版本的 32–55 ns，因此在该场景中 C 可能更适合兼顾部署体积与吞吐量。不过，该结论仅基于这一原型的 200 万行基准，不能直接外推到其他扩展或工作负载。

**标签**: `#SQLite`, `#Rust`, `#C`, `#performance comparison`, `#AI-assisted development`

---

<a id="item-tech-news-6"></a>
### [物理学家借电流噪声破解超导谜团](https://arstechnica.com/science/2026/11/physicists-listened-to-electrical-noise-to-crack-a-superconductor-mystery/) ⭐️ 6.0/10

由慕尼黑路德维希·马克西米利安大学的 Milan Allan 和荷兰乌得勒支大学的 Ingmar Swart 领衔的团队，在近期发表于《Science》的研究中利用流经铜基杯状氧化物时的微弱电流噪声，调查长期争议的赝能隙，并据报道取得了部分答案。赝能隙表现为材料在进入超导态后、特定能量处的电子似乎减少，但其成因主要有两种解释：电子冻结成电荷密度波等有序结构，或电子先形成 Cooper 对、只是尚未协同导电。研究团队希望通过噪声信号直接识别电子对，从而帮助区分这两套机制。现有摘录没有给出具体的噪声处理方法、量化结果或已验证的应用，因此尚无法据此评估“找到部分答案”的具体程度。

rss · Ars Technica · 11月8日 12:15

**「概念背景」** 杯状氧化物是 20 世纪 80 年代末发现的铜基高温超导材料，其工作温度可达到液氮可及的范围，但高温超导机制至今仍无共识。赝能隙出现在材料的超导转变温度以上，主流解释包括电子有序冻结和超导前形成 Cooper 对；两种机制会产生部分相似的实验信号，因此长期难以明确区分。

**「研究影响」** 这项工作为凝聚态物理研究者提供了一种利用电流噪声检验赝能隙起源的实验路径，但现有内容没有显示其已转化为材料、器件或硬件应用。

**标签**: `#superconductivity`, `#cuprates`, `#condensed-matter physics`, `#electrical-noise analysis`

---

<a id="item-tech-news-7"></a>
### [Epic Games 启动器确认支持 SteamOS](https://www.theverge.com/games/1029557/epic-games-launcher-is-coming-to-steamos) ⭐️ 6.0/10

Epic Games 已确认其 Epic Games Launcher 将支持 Valve 基于 Linux 的 SteamOS，并同时支持另外数种 Linux 发行版；该消息由 Epic Games 通信主管 Jake Jones 向 GamingOnLinux 确认。此前在 10 月，Epic 仅表示正在“调查”让《堡垒之夜》兼容 SteamOS，当时处于预览阶段的 Epic Games Launcher 也尚未把 SteamOS 明确列为受支持的发行版。此次确认解决的是启动器兼容问题，不能据此认定《堡垒之夜》或其他具体游戏现已可在 SteamOS 上运行。对 SteamOS 与 Linux 游戏用户而言，这扩大了 Epic Games Launcher 的官方平台覆盖范围，但实际游戏兼容性仍需逐款确认。

rss · The Verge · 11月8日 20:52

**「SteamOS 兼容性背景」** Epic Games 曾于 10 月表示正在“调查”让《堡垒之夜》兼容 Valve 基于 Linux 的 SteamOS，当时处于预览阶段的新版 Epic Games Launcher 尚未明确将 SteamOS 列为受支持的发行版。随后，Epic 确认新版启动器计划支持 SteamOS、Fedora、Cachy、Omarchy 等发行版，并测试不同的打包格式及恢复 AppImage 发布。此次确认针对启动器本身，不能据此认定《堡垒之夜》已经兼容 SteamOS。

**「对 Linux 玩家的影响」** SteamOS 用户将获得官方支持的 Epic Games Launcher，但其中具体游戏能否运行，仍取决于各游戏的 Linux 与 SteamOS 兼容性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.gamingonlinux.com/2026/11/epic-games-comments-on-planned-linux-distribution-support/">Epic Games comments on planned Linux distribution support</a></li>

</ul>
</details>

**标签**: `#Linux gaming`, `#SteamOS`, `#Epic Games Launcher`, `#game distribution`

---

<a id="item-tech-news-8"></a>
### [苹果正加速推进智能体式 Siri](https://www.theverge.com/ai-artificial-intelligence/1029552/apple-siri-ai-agentic) ⭐️ 6.0/10

据彭博社记者 Mark Gurman 报道，苹果 CEO John Ternus 正要求 AI 负责人 Craig Federighi 加快 Siri 路线图，以交付能够与 OpenAI 的 Dots 或 Meta 的 Muse 竞争的 AI 智能体。Federighi 已在极短时间内完成了一个可运行的 Siri AI 版本，但报道没有说明其具体功能、发布时间或性能基准。这意味着苹果正努力提升 Siri 执行复杂任务的能力，以应对消费级 AI 竞争；不过，现有二手简讯不足以证明新版 Siri 的实际成熟度。

rss · The Verge · 11月8日 19:18

**「背景」** “智能体式”Siri 是指不仅回答单次语音问题，还能理解目标、调用应用或工具并连续完成多步任务的 AI 系统。报道将 OpenAI 的 Dots 和 Meta 的 Muse 列为潜在竞争对象，但所给材料没有提供这些产品的功能、可用性或发布时间信息。

**「影响」** 如果苹果按计划推进，Siri 的任务执行能力可能得到显著增强，但由于报道未披露功能、测试结果和上线时间，用户何时以及能否实际受益仍不确定。

**标签**: `#Apple Siri`, `#AI agents`, `#consumer AI`, `#product strategy`

---

<a id="item-tech-news-9"></a>
### [埃尔维斯与 Eminem 权利方起诉 Suno](https://www.theverge.com/ai-artificial-intelligence/1029533/elvis-eminem-suno-ai-music-clone-lawsuit) ⭐️ 6.0/10

生成式音乐公司 Suno 又面临两起诉讼，原告分别是埃尔维斯·普雷斯利音乐权利人团体和 Eminem 部分重要唱片的出版商。起诉方称，Suno 未经授权生成模仿这两位艺人的音乐与歌词，其中普雷斯利案的律师主张相关行为违反田纳西州法律，但现有材料未披露具体法条或诉由。案件再次将生成式音乐中的版权授权和艺人模仿边界置于法律审查之下，但这些内容目前仅代表原告指控，尚不能说明法院已认定侵权成立。这一行动是 Suno 现有法律争议中的又一项进展，而非行业规则已经改变。

rss · The Verge · 11月8日 17:23

**「音乐风格模仿与权利保护」** Elvis Presley 是美国歌手和演员，其录音作品、词曲以及姓名和肖像等权益由不同权利主体管理；Eminem 的热门唱片也分别涉及录音、词曲的版权与出版权益。相关诉讼需要区分“模仿某位艺人”的风格与复制具体录音、歌词或旋律，因为风格相似本身通常不自动构成版权侵权。Presley 一方除主张版权问题外，还援引田纳西州关于姓名、肖像等公开权的法律追究 Suno，争议焦点因此落在其输出是否复制了受保护的表达或侵犯了相关公开权。

**「实际影响」** 这两项诉讼将增加 Suno 面临的版权法律风险，并使其生成模仿 Elvis Presley 和 Eminem 的音乐与歌词的能力成为司法审查对象。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.m.wikipedia.org/wiki/Elvis_Presley">Elvis Presley - Wikipedia</a></li>

</ul>
</details>

**标签**: `#generative-audio`, `#Suno`, `#copyright`, `#music-ai`, `#legal`

---

<a id="item-tech-news-10"></a>
### [华为称已打造全中国组件 PC](https://www.theregister.com/systems/2026/11/09/huawei-says-its-made-a-100-percent-chinese-pc/5308335) ⭐️ 6.0/10

《The Register》称，华为表示已生产出一台所有组件均来自中国的 PC。现有报道摘录没有说明“100%”的判定范围，也未提供处理器、操作系统、主板或其他关键部件的具体型号和制造信息。该主张尚无独立验证，兼容性、性能、量产能力及供应限制也均不明确，因此目前只能确认华为提出了这一说法，不能确认整机方案的实际完整度。若属实，它将是中国本土硬件与零部件供应链整合的重要进展，但现阶段不足以判断其对相关生态的实际影响。

rss · The Register · 11月9日 02:14

**「背景」** “100%中国 PC”通常意味着整机的关键硬件均采用中国供应商的产品，但这并不必然表示所有芯片、操作系统和软件都在中国自主开发。要评估此类声明，需要查看具体物料清单、供应商信息、测试结果及独立验证，并区分“国产化”与“完全国产化”。

**「对国产硬件生态的影响」** 如果该主张属实，这台完全采用中国组件的 PC 将显示华为在构建自主硬件供应链方面取得进一步进展，并可能提升中国 PC 产业降低对外部部件依赖的能力；但现有报道未提供配置、供应链细节或独立验证，因此目前难以确认其对实际采购和生态采用的短期影响。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bloomberg.com/graphics/2023-china-huawei-semiconductor/">How Huawei Is Helping China Build Up Its Semiconductor ...</a></li>

</ul>
</details>

**标签**: `#Huawei`, `#personal computing`, `#Chinese hardware`, `#supply chains`

---

<a id="item-tech-news-11"></a>
### [国际电联将审议 278 项互联网治理提案](https://www.theregister.com/networks/2026/11/08/internet-governance-about-to-get-its-quadrennial-stress-test-at-itu-meeting/5308031) ⭐️ 6.0/10

国际电信联盟（ITU）即将举行每四年一次的互联网治理相关会议，议程中可能讨论 278 项提案。部分人士担心，这些提案会推动决策权进一步向政府转移，并改变政府、标准机构及其他利益相关方之间的权力平衡。现有报道尚未说明具体提案及其技术影响，也没有确认会议会产生何种结果，因此目前只能确认潜在治理方向存在争议，不能据此认定互联网治理体系已经改变。

rss · The Register · 11月8日 09:33

**「国际电信联盟的作用」** 国际电信联盟（ITU）是联合国负责国际电信标准、无线电规则和全球通信协调的专门机构，其最高决策机构全权大会每四年举行一次，由成员国决定公约修订、选举管理层并制定中期战略。电信运营商、标准化组织和企业界代表可在正式表决前参与讨论与磋商，因此会议既涉及国家间协商，也关系到政府与互联网社群、技术标准机构之间的权力平衡。

**「潜在影响」** 如果 278 项提案中涉及扩大政府权限的内容在 ITU 全权代表大会 PP-26 上获通过，国家对互联网标准制定和治理的影响力可能上升，进而改变政府、标准组织及其他利益相关方的决策权分配。不过，现有信息未说明相关提案的具体内容或审议结果，因此目前无法确定其实际技术、兼容性或市场影响。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.itu.int/">ITU : Connecting the world and beyond</a></li>

</ul>
</details>

**标签**: `#Internet governance`, `#ITU`, `#Technology policy`, `#Internet standards`

---