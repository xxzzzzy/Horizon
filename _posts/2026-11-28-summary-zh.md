---
layout: default
title: "Horizon Summary: 2026-11-28 (ZH)"
date: 2026-11-28
lang: zh
---

> 从 69 条内容中筛选出 10 条重要资讯。

---

**科技新闻**
1. [美国政府以不可谈判条件取得英特尔 10%股权](#item-tech-news-1) ⭐️ 8.0/10
2. [OpenSec 披露 Linux 内核 NFS 远程提权漏洞](#item-tech-news-2) ⭐️ 8.0/10
3. [Google DeepCrossAttention：相近质量下最高提速 3 倍](#item-tech-news-3) ⭐️ 7.0/10
4. [购物网站盗卡脚本或借 WebRTC 规避检测](#item-tech-news-4) ⭐️ 7.0/10
5. [AWS Challenger: Trainium3 Inference and Microarchitecture Deep Dive](#item-tech-news-5) ⭐️ 7.0/10
6. [伯明翰 Oracle ERP 项目损失升至 1.28 亿英镑](#item-tech-news-6) ⭐️ 6.0/10
7. [欧洲 AI 主权：有云难掩外部依赖](#item-tech-news-7) ⭐️ 6.0/10
8. [AI 需求加剧光网络设备供应紧张](#item-tech-news-8) ⭐️ 6.0/10
9. [British social security system techies yank services offline following &\#x27;cyber incident&\#x27;](#item-tech-news-9) ⭐️ 6.0/10
10. [How cutting-edge prosthetics can help probe the human mind](#item-tech-news-10) ⭐️ 6.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [美国政府以不可谈判条件取得英特尔 10%股权](https://arstechnica.com/tech-policy/2026/11/intel-faced-a-choice-give-trump-10-or-face-the-consequences/) ⭐️ 8.0/10

据联邦诉讼中披露的英特尔内部通话记录，商务部律师 David Shapiro 于 2025 年 8 月向英特尔 CFO 表示，政府希望立即获得公司股份，并警告董事会不要把这视为谈判。Shapiro 承认董事会可以拒绝，但称拒绝会带来“无法预测的后果”；数日后，董事会接受了政府的条件。特朗普随后称美国现在“完全拥有并控制”英特尔 10%股份，政府没有支付对价，这部分股份估值约 110 亿美元。这意味着联邦政府已直接进入英特尔的所有权和公司治理，而一名前商务部官员向 WIRED 表示，政府的政策重心正从就业、竞争力和市场份额等指标转向要求企业以现金或股权回馈政府。

rss · Ars Technica · 11月27日 12:05

**「相关背景」** 英特尔是一家总部位于美国加州圣克拉拉的跨国半导体企业，主要设计、制造和销售 CPU 等计算组件，因此其所有权与治理变化会同时牵动芯片供应链和产业政策。按报道所述，此次安排并非普通的政府补贴或采购，而是美国政府直接取得英特尔 10%的股份并宣称对其拥有控制权；来源还将此事置于政府更广泛介入关键芯片企业管理层和财务决策的背景下。

**「影响」** 美国政府成为持有并控制英特尔 10%股份的股东后，芯片客户、供应商和开发者评估其供货与投资风险时，需要纳入联邦政府对英特尔治理和战略的直接影响；官方协议所列政府投资额为 89 亿美元，而报道引述特朗普称股份为零对价、价值约 110 亿美元。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Intel">Intel - Wikipedia</a></li>
<li>Intel and Trump Administration Reach Historic Agreement to Accelerate...</li>

</ul>
</details>

**标签**: `#Intel`, `#semiconductors`, `#US industrial policy`, `#government intervention`, `#chip supply chains`

---

<a id="item-tech-news-2"></a>
### [OpenSec 披露 Linux 内核 NFS 远程提权漏洞](https://opensec.in/blog/nfs2root-cve-2026-99362) ⭐️ 8.0/10

OpenSec 披露了 Linux 内核 NFS 服务器组件 nfsd 的预认证堆溢出漏洞 CVE-2026-99362，CVSS 评分为 9.8；攻击者无需登录，只需向目标发送单个 TCP/2049 连接，即可越界写入内核堆并获取 root shell。该漏洞自 2014 年的 Linux 3.16 起存在，影响启用 NFSv4.1 或 NFSv4.2 的主机，包括文件服务器、NAS 和集群存储节点。修复版本为 Linux 6.12.117、6.18.61、7.3.2 和 7.4-rc1，运维人员应尽快升级内核并重启，无法立即升级时可通过应用防火墙限制 TCP/2049 访问；该 CVE 于 2026 年 11 月 20 日公开，但目前披露内容尚缺少漏洞原理、利用验证及真实攻击活动证据。

telegram · zaihuapd · 11月27日 12:57

**「漏洞背景」** Linux 内核的 nfsd 是实现 NFS 文件共享协议的服务端组件；启用 NFSv4.1 或 4.2 的主机通常通过 TCP 2049 接受连接，因此漏洞可在客户端完成 NFS 登录前触发。CVE-2026-99362 属于 nfsd 预认证路径中的堆缓冲区溢出，OpenSec 称单次连接即可越过内核堆对象边界写入 61 字节，相关报道则指出该缺陷自 2014 年发布的 Linux 3.16 起存在。NFS 的作用是让网络客户端共享和访问服务器文件，因此这一缺陷直接位于远程文件服务的数据处理边界。

**「NFS 主机需紧急修补」** 运行 Linux 内核 nfsd 且启用 NFSv4.1 或 4.2 的文件服务器、NAS 和集群存储节点面临无需认证的远程 root 入侵风险，应将内核升级至 6.12.117、6.18.61、7.3.2 或 7.4-rc1 并重启；无法立即升级时，应限制对 TCP/2049 的访问。目前披露未提供在野攻击或利用验证，因此该后果反映的是漏洞的潜在影响，而非已确认的大规模利用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://opensec.in/blog/nfs2root-cve-2026-99362">NFS2 ROOT ( CVE - 2026 - 99362 ): pre -auth root in Linux nfsd | OpenSec</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/new-nfs2root-linux-flaw-can-let-attackers-gain-root-privileges/">New NFS2 ROOT Linux flaw can let attackers gain root privileges</a></li>

</ul>
</details>

**标签**: `#Linux 内核`, `#NFS`, `#CVE-2026-99362`, `#远程代码执行`, `#漏洞修复`

---

<a id="item-tech-news-3"></a>
### [Google DeepCrossAttention：相近质量下最高提速 3 倍](https://research.google/blog/supercharging-transformer-residual-connections/) ⭐️ 7.0/10

Google 推出 DeepCrossAttention（DCA），将 Transformer 传统的逐 token 注意力改为沿网络深度跨层执行注意力，以利用不同层之间的信息。据所给材料，该架构在保持可比模型质量的同时，速度最高可提升至 3 倍。按材料中的技术描述，DCA 会让序列中的 token 查询此前层表示的动态加权组合，从而在不增加传统 token 注意力计算负担的情况下获得更完整的历史上下文。不过，现有证据未提供模型规模、评测任务、硬件条件或质量指标，因此无法确认该加速幅度能否广泛复现，也不能据此判断其是否已达到生产就绪程度。

hackernews · ComputedCamp995 · 11月27日 23:06 · [社区讨论](https://news.ycombinator.com/item?id=50672565)

**「背景」** 传统 Transformer 的残差连接通常将当前层的输入与输出逐元素相加，但随着网络加深，早期信息可能在反复传递中逐渐稀释。DeepCrossAttention（DCA）改用可学习权重和深度方向的交叉注意力，让不同 token 动态组合先前层的表示，从而在跨层计算中利用更完整的历史信息。

**「实际影响」** 对需要在保持可比模型质量的同时降低 Transformer 推理延迟的开发者，DeepCrossAttention 报告最高可实现约 3 倍加速。社区已有 PyTorch 实现可供实验和集成，但现有证据尚不足以证明其在广泛基准或生产环境中均能获得同等收益。

**「社区讨论」** 评论者将 DCA 解读为让 token 跨层查询此前层表示的混合，并猜测它或许有助于解决“草莓问题”；也有人将其与 DenseNet 联系起来，但这些观点尚未得到验证。其他评论主要质疑图表应改用柱状图，以及讨论 Gemini Neon 与 Claude 的价格和体验，并未直接支持 DCA 的速度或质量结论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://research.google/blog/supercharging-transformer-residual-connections/">Supercharging transformer residual connections</a></li>
<li><a href="https://github.com/Yuan-ManX/DeepCrossAttention-PyTorch/blob/main/README.md">DeepCrossAttention -PyTorch/README.md at main · Yuan-ManX ... -...</a></li>

</ul>
</details>

**标签**: `#transformers`, `#attention mechanisms`, `#model inference efficiency`, `#deep learning research`

---

<a id="item-tech-news-4"></a>
### [购物网站盗卡脚本或借 WebRTC 规避检测](https://www.infohawk.com/news/2026-11-27-black-friday-webrtc-skimmer) ⭐️ 7.0/10

一份报告称，热门购物网站上发现了电子盗卡脚本，这些脚本可能借助 WebRTC 外传数据，以绕过常规网络安全监测。问题并非 WebRTC 本身存在漏洞，而是第三方 JavaScript 能在用户浏览器中运行、接触支付流程，而相关行为又往往处于监控盲区。当前材料未提供受影响网站名单、具体实现或完整技术分析，因此实际影响范围及 WebRTC 的使用方式仍待核实。

hackernews · scanr · 11月27日 15:40 · [社区讨论](https://news.ycombinator.com/item?id=50668145)

**「背景」** 电子盗卡（e-skimming）通常通过植入电商页面的恶意脚本，在用户提交支付信息时截获银行卡数据。WebRTC 原本是浏览器用于实时通信的接口，恶意脚本也可能借助这类较少被监控的通道外传数据，但根本风险在于网站允许不可信的第三方脚本执行，而非 WebRTC 本身存在漏洞。

**「实际风险」** 据报道，热门购物网站中的恶意第三方脚本可能窃取消费者结账时输入的支付卡数据，商户因此需要加强脚本隔离、权限限制及异常外联监控。WebRTC 并非根本漏洞，评论指出仅封禁 WebRTC 无法替代这些防护，因为类似数据外传同样可通过普通 HTTP 请求完成。

**「社区讨论」** 评论者普遍认为，核心风险是不受信任的第三方脚本和监控不足，而非 WebRTC 的技术能力；有人指出普通 HTTP 请求同样可以外传数据，移动设备更难被发现也可能解释其成为攻击目标的原因。其他人主张对广告等第三方内容实施沙箱隔离，甚至让浏览器只渲染数据而不执行 JavaScript；也有人借此事批评支付体系仍依赖共享对称密钥及交易撤销中介。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://sifirincidakika.com/haber/populer-alisveris-sitelerinde-webrtc-tabanli-kredi-karti-skimming-betikleri-bulundu">Popüler alışveriş sitelerinde WebRTC tabanlı kredi kartı skimming ...</a></li>

</ul>
</details>

**标签**: `#WebRTC`, `#e-skimming`, `#third-party JavaScript`, `#browser security`, `#e-commerce`

---

<a id="item-tech-news-5"></a>
### [AWS Challenger: Trainium3 Inference and Microarchitecture Deep Dive](https://newsletter.semianalysis.com/p/trainium3-inferencex) ⭐️ 7.0/10

SemiAnalysis examines the microarchitecture of AWS&\#x27;s Trainium3 inference accelerator, analyzing its performance-per-cost and utilization characteristics versus NVIDIA&\#x27;s GB300 platform.

rss · Semianalysis · 11月27日 15:54

**标签**: `#AI hardware`, `#AWS Trainium`, `#inference accelerators`, `#microarchitecture`, `#semiconductors`

---

<a id="item-tech-news-6"></a>
### [伯明翰 Oracle ERP 项目损失升至 1.28 亿英镑](https://www.theregister.com/public-sector/2026/11/27/bill-for-birminghams-oracle-debacle-reaches-128m/5312563) ⭐️ 6.0/10

据报道，伯明翰市由 Oracle 主导的企业资源规划（ERP）替换项目失败，相关成本已达 1.28 亿英镑。该项目在 Oracle 方案受挫后转向 SAP，但替代系统同样出现延误。原报道标题称，延误的 SAP 替换项目帮助促成了伯明翰市破产；现有材料未披露成本构成或完整时间线。最终总成本可能显著高于 1.28 亿英镑，但目前没有更高的估算数字。

rss · The Register · 11月27日 14:03

**「背景」** ERP 系统用于整合组织的财务和核心业务流程，公共部门更换此类系统通常涉及复杂的系统集成、合同管理和长期治理。伯明翰的案例表明，替换项目的已知成本并非全部风险，原方案失败还可能通过后续替代项目延误进一步放大损失。

**「影响」** 对伯明翰市而言，Oracle 方案失败及 SAP 替代延误已带来据报 1.28 亿英镑的财政损失，而最终损失仍可能继续增加。

**标签**: `#enterprise software`, `#Oracle`, `#SAP`, `#public-sector IT`, `#project failure`

---

<a id="item-tech-news-7"></a>
### [欧洲 AI 主权：有云难掩外部依赖](https://www.theregister.com/ai-and-ml/2026/11/27/europes-ai-sovereignty-push-lots-of-cloud-not-much-silver-lining/5312120) ⭐️ 6.0/10

欧洲的数据中心和云计算投资正蓬勃增长，但其 AI 主权建设仍面临结构性限制。文章指出，关键 AI 模型、AI 芯片及相关产业话语权仍主要集中在美国和亚洲，因此新增算力和云容量并不等于欧洲已经掌控完整的 AI 技术栈与产业影响力。欧洲能否将基础设施扩张转化为真正的技术自主，仍取决于其对模型、芯片及供应链关键环节的控制力；这项分析侧重结构性挑战，并未提出单一的技术突破或政策结论。

rss · The Register · 11月27日 11:32

**「背景：AI 主权与基础设施自主」** AI 主权通常指一个地区在算力基础设施、核心模型、芯片供应和产业决策方面具备自主可控能力，而不只是建设本地数据中心。本文讨论的核心张力是，欧洲虽然持续扩大云和数据中心投资，但模型、AI 芯片及产业影响力仍主要集中在美国和亚洲，因此基础设施增长本身并不等同于完整的 AI 主权。

**「实际影响」** 对欧洲政府和依赖 AI 的企业而言，云与数据中心投资的增长并不会自动带来主权能力，因为关键模型、芯片和产业控制力仍集中在美国和亚洲，相关供应链依赖难以实质性降低。

**标签**: `#AI sovereignty`, `#data centers`, `#cloud computing`, `#AI chips`, `#AI policy`

---

<a id="item-tech-news-8"></a>
### [AI 需求加剧光网络设备供应紧张](https://www.theregister.com/networks/2026/11/27/ai-boom-leaves-network-operators-waiting-up-to-18-months-for-kit/5312366) ⭐️ 6.0/10

AI 数据中心需求正在加剧光网络设备及关键组件的供应紧张，电信运营商与数据中心争夺同类部件。据研究机构 RETN 报道，光设备价格今年已上涨约 50%，部分运营商为相关设备等待最长 18 个月。这一瓶颈可能拖慢 AI 基础设施扩张并显著抬高网络升级成本，但现有信息未披露具体设备类别、供应商或订单规模。

rss · The Register · 11月27日 10:45

**「供应背景」** RETN 是连接欧洲和亚洲的数据网络平台，其网络建设同样依赖光传输设备及相关组件。随着 AI 数据中心扩张，电信运营商与数据中心争夺有限的供应，设备交付周期和价格因此承压；这种短缺还已外溢到光纤无人机等专用系统，相关光纤价格据称在 2025 至 2026 年间上涨约 6 至 10 倍。

**「影响」** AI 数据中心争抢光器件可能使电信运营商的设备等待期延长至最长 18 个月，同时令相关组件价格年内上涨约 50%，从而拖慢光纤扩容和宽带部署并增加预算压力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://retn.net/">RETN : Leading Data Network Platform Connecting Europe and Asia</a></li>
<li><a href="https://arstechnica.com/gadgets/2026/11/ukraines-fiber-optic-drones-get-squeezed-by-ai-data-center-demand/">Ukraine’s fiber- optic drones get squeezed by AI data center demand</a></li>
<li>AI buildout is straining broadband supply chains - CoBank</li>
<li>[PDF] Opportunities in networking optics: Boosting supply for data centers</li>

</ul>
</details>

**标签**: `#AI infrastructure`, `#networking hardware`, `#supply chains`, `#data centers`

---

<a id="item-tech-news-9"></a>
### [British social security system techies yank services offline following &\#x27;cyber incident&\#x27;](https://www.theregister.com/security/2026/11/27/british-social-security-system-techies-yank-services-offline-following-cyber-incident/5312522) ⭐️ 6.0/10

British social security technology staff took services offline following a cyber incident, while pensioners were assured that funds would arrive as normal.

rss · The Register · 11月27日 10:01

**标签**: `#cybersecurity`, `#government IT`, `#social security`, `#service outage`, `#UK`

---

<a id="item-tech-news-10"></a>
### [How cutting-edge prosthetics can help probe the human mind](https://www.technologyreview.com/2026/11/27/1149946/cutting-edge-prosthetics-allow-researchers-to-probe-the-human-mind/) ⭐️ 6.0/10

An early clinical trial is testing a prosthetic hand that connects to arm nerves and enables its user to move and feel with it independently at home.

rss · MIT Technology Review · 11月27日 10:00

**标签**: `#neurotechnology`, `#prosthetics`, `#sensory feedback`, `#peripheral nerve interfaces`, `#clinical trials`

---