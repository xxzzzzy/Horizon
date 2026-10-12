---
layout: default
title: "Horizon Summary: 2026-10-12 (ZH)"
date: 2026-10-12
lang: zh
---

> 从 75 条内容中筛选出 7 条重要资讯。

---

**科技新闻**
1. [陶哲轩&quot;数学 2.0&quot;讲座:AI 重塑数学研究范式的反思](#item-tech-news-1) ⭐️ 7.0/10
2. [AI 系统已具备攻击关键基础设施的能力，防御方却尚未就绪](#item-tech-news-2) ⭐️ 7.0/10
3. [Sliced Wasserstein 嵌入 + HNSW 实现 4.8 万幅画作色彩方案检索](#item-tech-news-3) ⭐️ 7.0/10
4. [关于大模型能力认知差距正在拉大](#item-tech-news-4) ⭐️ 6.0/10
5. [伊利诺伊州一学院试图终止 Flock Safety 合同遭拒](#item-tech-news-5) ⭐️ 6.0/10
6. [韩国研究人员用氧气控制二维半导体晶体生长，瞄准 2030 年商用](#item-tech-news-6) ⭐️ 6.0/10

**财经新闻**
1. [中国内存芯片商长鑫存储获多家机构&quot;跑赢大盘&quot;评级](#item-finance-news-1) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [陶哲轩&quot;数学 2.0&quot;讲座:AI 重塑数学研究范式的反思](https://teorth.github.io/tao-web/slides/math-2-0-caltech-2026.pdf) ⭐️ 7.0/10

菲尔兹奖得主陶哲轩在加州理工学院 2026 年的演讲中以&quot;数学 2.0&quot;为题,探讨 AI 对数学研究流程与文化的深层冲击,并将其与软件代码库类比,认为纯粹数学本质上是一个由人类长期维护的高质量&quot;代码库&quot;,包含理论、定义与证明,而当前的数学 AI 虽然能产出解答,却尚未扮演好&quot;良好市民&quot;,缺乏对优雅性和结构性的自觉。幻灯片借助&quot;开放问题是灯塔而非目的地&quot;的比喻,指出这些难题之所以悬而未决,是因为现有理论在相关方向上解释力不足,需要被视为指引理论延伸的方向,而不是单纯等待答案的终点。演讲还引申到 AI 在癌症医学等领域的应用,抛出&quot;不理解机制是否构成治疗障碍&quot;的问题,并延续他此前关于 Oct 8 讨论的 100 多条反馈——部分数学家长期攻关的问题被 AI 在数小时内解决,他们形容这种感觉像&quot;失去一位老朋友或爱人&quot;,并需要重写刚提交的研究申请。

hackernews · Anon84 · 10月11日 13:16 · [社区讨论](https://news.ycombinator.com/item?id=50043026)

**「背景」** 陶哲轩是 2006 年菲尔兹奖得主,长期关注形式化证明、Lean 等证明语言,以及 AI 在数学中的角色等议题。&quot;Math 2.0&quot;这一提法延续他此前在网络上关于 AI 解题体验的讨论,试图把零散观察整合成一个更具结构性的研究范式框架,并与医疗、法律等其他知识行业被 AI 重塑的过程做横向类比。

**「影响」** 数学界需要重新思考选题标准、证明呈现方式与跨人机协作的研究流程,以适应 AI 可在数小时内产出长期开放问题解答草案的新现实;对以&quot;独占难题&quot;为职业身份认同的研究者而言,这一变化可能带来显著的心理与职业冲击。

**「社区讨论」** HN 评论对 Tao 关于 AI 与癌症医学的类比存在明显分歧:从事药物发现的从业者认为幻灯片对医学理解得过于乐观,举例称全身麻醉机制至今未被完全厘清却已广泛使用,质疑&quot;不理解机制就不应使用&quot;的前提;也有评论者从纯数学价值出发,担忧当 AI 解决长期开放问题时,钻研者会感到&quot;失去老朋友或爱人&quot;般的失落,并对整个学科身份认同产生动摇。

**标签**: `#AI`, `#mathematics`, `#research`, `#future-of-work`, `#Terence Tao`

---

<a id="item-tech-news-2"></a>
### [AI 系统已具备攻击关键基础设施的能力，防御方却尚未就绪](https://www.theregister.com/security/2026/10/11/ai-systems-are-fully-capable-of-carrying-out-nightmare-attacks-against-infrastructure-and-nobodys-ready/5302450) ⭐️ 7.0/10

The Register 报道称，AI 智能体已具备对关键基础设施发动复杂攻击的能力，具体手段包括操控机械臂实施物理动作，以及篡改 OT（运营技术）设备操作员的屏幕画面以误导人工判断。这些攻击路径将物理动作（驱动机械臂）与社会工程（向操作员呈现不实数据）结合起来，对工业控制系统构成叠加风险。该报道指出，基础设施运营者在防御 AI 驱动的威胁方面尚未做好准备，并警示此类攻击模糊了网络入侵与物理破坏之间的界限。

rss · The Register · 10月11日 11:30

**「背景说明」** 操作技术（OT）是指用于监控和控制物理设备与工业流程的计算系统，广泛应用于电力、水务、制造、核设施等关键基础设施领域，与传统的办公 IT 网络相比，其安全防护往往更为薄弱。2026 年，AI 代理技术迅速发展，能够自主执行多步推理与物理操作任务，与此同时，AI 驱动的网络攻击已开始出现实际案例，例如伊朗关联的 APT 组织攻击暴露在互联网上的可编程逻辑控制器（PLC），以及疑似中国国家支持的黑客使用基于开源框架构建的自主 AI 代理对台湾政府和能源部门发起端到端攻击。这些先例表明，AI 在针对关键基础设施的攻击中已从理论威胁转变为现实风险，而文中所描述的操控机械臂与伪造操作员屏幕画面则代表了 AI 代理从纯网络攻击向物理世界延伸的新阶段。

**「影响」** 运营关键基础设施和 OT/ICS 系统的组织需立即将 AI 智能体视为一种新型复合威胁——它能同时进行物理层面的设备操控（如直接驱动机械臂）与对运维人员人机界面的实时伪造欺骗,这使传统依赖网络边界和签名检测的 OT 防护策略明显不足以应对此类攻击路径。考虑到原文仅提供了攻击能力的描述性论断,针对 AI 驱动物理-欺骗复合攻击的有效防御方案及行业实际部署成熟度仍存在不确定性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.elisity.com/blog/ai-agents-ot-security-s4x26-insights">AI Agents in OT Security: What S4x26 Revealed for 2026</a></li>
<li><a href="https://elmoz.de/blog/ai-agents-critical-infrastructure-2026">AI Attacks on Critical Infrastructure: The Evidence - elmoz.de</a></li>
<li><a href="https://undercodetesting.com/autonomous-ai-agents-launch-first-documented-end-to-end-cyberattacks-against-critical-infrastructure-video/">Autonomous AI Agents Launch First Documented End-to-End ...</a></li>
<li><a href="https://abnormal.ai/glossary/ai-enabled-cyberattacks">What Are AI - Enabled Cyberattacks ? Why They&#x27;re... | Abnormal AI</a></li>
<li><a href="https://www.linkedin.com/posts/cyberdeflex_icssecurity-scada-criticalinfrastructure-activity-7447282038610702337-qoJ2">#icssecurity # scada #criticalinfrastructure #operationaltechnology...</a></li>
<li><a href="https://threatsys.co.in/scada-critical-infrastructure-security-guide/">SCADA Security for Critical Infrastructure : A Complete Guide</a></li>

</ul>
</details>

**标签**: `#AI security`, `#critical infrastructure`, `#OT security`, `#AI agents`, `#cybersecurity`

---

<a id="item-tech-news-3"></a>
### [Sliced Wasserstein 嵌入 + HNSW 实现 4.8 万幅画作色彩方案检索](https://www.reddit.com/r/MachineLearning/comments/1x39uu6/sliced_wasserstein_embeddings_hnsw_for/) ⭐️ 7.0/10

博客项目 &quot;Palette Atlas&quot; 将 48,695 幅公共领域画作各压缩为 128 个等权颜色，使 Earth Mover&\#x27;s Distance（W1）成为自然度量，但逐对计算约需 6 毫秒，无法直接做最近邻。作者把 OKLab 颜色投影到 Fibonacci 半球上 8 个方向排序、再分 16 个分位取均值，使两向量之间的 L1 距离成为各方向上 1D W1 的平均，从而构成真实 W1 的下界。在 240 次查询上与精确 EMD 比较，8×16 切片 + L1 的 Top-10 重合率为 78%、平均偏离 1.8%，明显优于软颜色直方图 Hellinger 距离（45%、13.5%）和平均色（3%、161%）。与此同时，作者从零实现了 HNSW 索引（M=16，efConstruction=200），在 ef=32 下取得 recall@10 = 1.000，单次查询 0.25 毫秒，相比 14 毫秒的暴力搜索提速约 56 倍。文章还分析嵌入向量本征维度约 11，并将 HNSW 顶层节点替换为 8 个 k-means 路标，搜索代价几乎不变（平均 2,558 vs 2,556 次距离计算），每类色彩簇对应一幅代表性画作。

reddit · r/MachineLearning · /u/Potential-Barber8658 · 10月11日 14:39

**「背景」** Earth Mover&\#x27;s Distance（Wasserstein-1）将两个分布看作&quot;土堆&quot;与&quot;坑&quot;，计算把它们互相搬运所需的最少代价，常被用作颜色直方图或光谱分布之间的相似度。Sliced Wasserstein 则是把高维分布在多条确定或随机方向上投影为一维分布，再对各方向的 W1 取平均，常作为快速近似。HNSW（Hierarchical Navigable Small World）通过多层小世界图把近似最近邻搜索的复杂度压到对数级，是目前主流的向量索引结构之一；当数据本征维度过高时，这种对数加速可能失效，这正是本项目特意测量嵌入维度（约 11）的原因。

**「影响」** 对需要在 Wasserstein/EMD 距离下做大规模最近邻检索的研究者与工程师而言，该切片嵌入法提供了一种可复用的下界手段，把近似检索延迟降到亚毫秒级；但 Palette Atlas 本身是面向艺术画作的色彩方案搜索工具，直接受众相对有限。

**标签**: `#machine-learning`, `#nearest-neighbor-search`, `#wasserstein`, `#hnsw`, `#computer-vision`

---

<a id="item-tech-news-4"></a>
### [关于大模型能力认知差距正在拉大](https://twitter.com/karpathy/status/2109361546505966046) ⭐️ 6.0/10

Hacker News 上由 Karpathy 一条推文引发的 486 条讨论聚焦于大语言模型与智能体实际能力与公众认知之间的差距。Karpathy 指出，仅约 0.2% 的人群对 LLM 的真实能力拥有更深入的理解，且这一差距仍在拉大。部分评论者否认这一群体普遍认同&quot;智能体可通过提示词在数周内完成以往的大型复杂项目&quot;，并强调在代码维护、令牌成本、优化、代码腐蚀及模型潜在错误等方面仍需人工把关。对于普通公众应如何对待这些模型，社区也存在疑问，部分意见认为 AI 技术仍处早期阶段；另有人指出软件应用自动化的影响可能有限，而具身智能若取得突破将带来深远变革。

hackernews · albertzeyer · 10月11日 20:20 · [社区讨论](https://news.ycombinator.com/item?id=50047422)

**「背景」** Karpathy 是知名 AI 研究者，曾任职于特斯拉与 OpenAI，此次观点最初以推文形式发出。&quot;认知差距&quot;是 AI 炒作与一线实践者认知之间长期存在的议题，但因本次 486 条高质量评论而具有讨论价值。

**「影响」** 对于正在校准智能体编程工具预期的软件工程师而言，评论共识指向：智能体仍无法替代对代码库、维护成本与潜在错误的深入人工审查。

**「社区讨论」** 部分评论者认同 Karpathy 的判断，认为差距源于一线从业者与公众对模型局限性的认知差异；另一些则认为所谓&quot;差距&quot;其实只是 LLM 现阶段只能完成有限子集工作的客观反映。整体上对这一差距的性质与严重程度仍无共识。

**标签**: `#LLM`, `#AI`, `#software engineering`, `#agentic coding`, `#industry analysis`

---

<a id="item-tech-news-5"></a>
### [伊利诺伊州一学院试图终止 Flock Safety 合同遭拒](https://www.theverge.com/tech/1009411/elgin-community-college-flock-safety-cameras) ⭐️ 6.0/10

2025 年 4 月，伊利诺伊州埃尔金社区学院部署了 6 台 Flock Safety 摄像头，用于提升校园学生安全。到 2025 年 9 月，校方因三项担忧试图终止合同：Flock 与美国海关与边境保护局（CBP）共享数据、摄像头视频流缺乏足够的安全保护，以及执法部门可访问相关数据。学院提出解约后，Flock 拒绝接受取消请求。这一事件反映出公共机构在引入 AI 监控系统时面临的供应商锁定、联邦数据共享以及网络安全漏洞等多重风险。

rss · The Verge · 10月11日 20:06

**「背景说明」** Flock Safety 是一家提供基于计算机视觉与机器学习的自动车牌识别及安防摄像头厂商，其系统通常由执法机构或私营组织部署，云端数据可通过其网络平台被查询。CBP（美国海关与边境保护局）为美国联邦执法机构，有权在边境及内陆检查站查询多种监控数据库，因而社区摄像头数据可能被间接纳入其查询范围。

**「影响」** 此次解约失败意味着埃尔金社区学院在合同到期前仍须继续使用 Flock 摄像头，并接受其当前的数据共享条款与安全状况；其他采购 AI 监控摄像头的学校与机构也需要在签约前审查类似的数据外泄、联邦机构访问与合同解除条款风险。

**标签**: `#surveillance-tech`, `#privacy`, `#AI-policy`, `#computer-vision`, `#vendor-lock-in`

---

<a id="item-tech-news-6"></a>
### [韩国研究人员用氧气控制二维半导体晶体生长，瞄准 2030 年商用](https://www.theregister.com/science/2026/10/11/researchers-work-out-how-to-control-2d-semiconductor-growth-for-future-chips/5301666) ⭐️ 6.0/10

韩国研究人员开发出一种利用氧气控制二维半导体晶体生长的新方法，旨在解决未来芯片制造中晶体取向不一致的关键难题。该方法通过引入氧气来抑制晶体在错误方向上成核，从而提高二维半导体薄膜的均匀性和质量。作为二维材料集成领域的重要进展，这项研究为在传统硅基工艺之外构建更薄、性能更优的晶体管层提供了一条可行路径。研究团队的目标是在 2030 年前将这项技术从实验室推向商业化生产，为下一代芯片制造提供新的材料解决方案。

rss · The Register · 10月11日 08:30

**「背景：二维半导体与晶体生长控制」** 二维半导体（如二硫化钼）是一类仅有几个原子层厚度的材料，被认为是硅之后下一代芯片制造的候选材料。但要将它们用于实际电路，关键难题在于如何让晶体只在指定位置、按单一取向生长——如果晶核在错误的地点或错误的方向形成，所得到的薄膜就无法构成可用的器件。传统晶体生长（如 Czochralski 法）已在大块硅等半导体上使用多年，但在二维材料的单晶晶圆级制备中仍缺乏类似的精确控制手段，这也是韩国团队此次研究的背景所在。

**「影响」** 如果该方法能够实现规模化生产，二维半导体芯片制造商将有望获得更可控的晶体生长工艺，从而降低缺陷率并提升下一代芯片的良率；不过目前仍处于实验室研究阶段，距离 2030 年商用目标能否如期实现还存在不确定性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Czochralski_method">Czochralski method - Wikipedia</a></li>
<li><a href="http://koreabizwire.com/new-crystal-growth-technique-could-pave-way-for-stacked-ai-chips/360570">New Crystal - Growth Technique Could Pave Way for Stacked AI Chips</a></li>
<li><a href="https://www.nature.com/articles/s41586-026-11095-1?error=cookies_not_supported&amp;code=5ea10956-ec7a-410d-b77a-6185893bed73">Spatially deterministic nucleation of 2 D semiconductors by... | Nature</a></li>

</ul>
</details>

**标签**: `#hardware`, `#semiconductors`, `#chip-manufacturing`, `#materials-science`, `#research`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [中国内存芯片商长鑫存储获多家机构&quot;跑赢大盘&quot;评级](https://www.cnbc.com/2026/10/11/this-chinese-memory-chip-maker-has-global-potential.html) ⭐️ 7.0/10

多家券商对中国最大 DRAM（动态随机存取内存）厂商长鑫存储\(CXMT\)给予&quot;跑赢大盘&quot;评级，CLSA 目标价 84.70 元人民币（较上周五收盘价高出逾 60%），预计其全球出货量份额到 2027 年达 14%（去年为 9%），但法巴维持中性评级，目标价仅 48.70 元。

rss · CNBC Finance · 10月11日 11:39

**「背景」** 全球内存价格上涨及供应趋紧为 CXMT 带来海外扩张机会；不过美国对其部分生产设备的出口管制构成地缘政治风险。

**「影响」** 伯恩斯坦援引 Gartner 数据指出，剔除中国和美国市场后，外国 PC、智能手机等终端厂商的内存需求可再为 CXMT 提供 10%以上的全球份额。

**标签**: `#semiconductors`, `#DRAM`, `#China`, `#analyst coverage`, `#geopolitics`

---