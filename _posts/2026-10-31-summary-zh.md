---
layout: default
title: "Horizon Summary: 2026-10-31 (ZH)"
date: 2026-10-31
lang: zh
---

> 从 121 条内容中筛选出 13 条重要资讯。

---

**科技新闻**
1. [Cursor 恶意 Claude Code 扩展植入 SSH 后门](#item-tech-news-1) ⭐️ 8.0/10
2. [币安据报遭 63 亿美元攻击仅耗时 20 分钟](#item-tech-news-2) ⭐️ 8.0/10
3. [Azure 最薄弱环节：五种完整的跨租户攻陷路径](#item-tech-news-3) ⭐️ 8.0/10
4. [Anthropic 官方 Cursor 扩展遭供应链投毒](#item-tech-news-4) ⭐️ 8.0/10
5. [币安报告 63 亿美元加密货币失窃](#item-tech-news-5) ⭐️ 8.0/10
6. [Qwen3.5-4B 权重内运行 NES 模拟器](#item-tech-news-6) ⭐️ 7.0/10
7. [全球火箭发射能力缺口扩大](#item-tech-news-7) ⭐️ 7.0/10
8. [通用汽车因转售驾驶数据支付 2.2 亿美元](#item-tech-news-8) ⭐️ 7.0/10
9. [Apple Intelligence 将随 iOS 27.3 登陆中国](#item-tech-news-9) ⭐️ 7.0/10
10. [AI 巨头支持统一反抓取退出标准](#item-tech-news-10) ⭐️ 7.0/10
11. [谷歌卫星首次从太空传回 AI 响应](#item-tech-news-11) ⭐️ 7.0/10
12. [Applebee’s 应用硬编码凭据暴露客户数据](#item-tech-news-12) ⭐️ 7.0/10
13. [Community safety report and new protections for teens](#item-tech-news-13) ⭐️ 6.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Cursor 恶意 Claude Code 扩展植入 SSH 后门](https://phorion.io/blog/offical-claude-code-vsx-compromise/) ⭐️ 8.0/10

据 Cursor 安全通告及 Anthropic 员工的说明，攻击者利用 Cursor 扩展市场的访问权限，上架了一个篡改版 Claude Code VS Code 扩展；该扩展并非 Anthropic 开发或发布，Anthropic 的系统和员工笔记本也未因此被攻破。恶意扩展将攻击者公钥以 \`svc-telemetry\` 标签追加到 SSH \`authorized\_keys\`，从而为攻击者保留持久 SSH 访问通道。影响限于 Cursor 用户，Anthropic 官方分发渠道的版本不受影响；该恶意版本约在周四太平洋时间凌晨 2:27 至下午 1:35 期间可下载。用户可检查 SSH 授权密钥中是否存在 \`svc-telemetry\`，macOS 上可使用 \`grep -qs svc-telemetry ~/.ssh/authorized\_keys\` 搜索。

hackernews · \_chall · 10月30日 07:09 · [社区讨论](https://news.ycombinator.com/item?id=50300683)

**「背景」** 此次事件属于软件供应链攻击：第三方扩展市场中的扩展若被篡改，恶意代码可能在用户安装或激活时修改本机配置。Claude Code for VS Code 是 Anthropic 的官方扩展，但此次恶意副本出现在 Cursor 的扩展市场；官方发布渠道未受影响。该版本会向用户的 \`~/.ssh/authorized\_keys\` 写入标记为 \`svc-telemetry\` 的攻击者公钥，从而建立持久化 SSH 访问后门。

**「安全影响」** 安装 Cursor 市场中恶意版本的最多 5,000 名用户面临持久化 SSH 未授权访问风险，因为该扩展会尝试向 authorized\_keys 写入标记为“svc-telemetry”的攻击者公钥、启用本地 SSH 服务并建立反向隧道，而 Anthropic 官方渠道发布的版本不受影响。

**「社区讨论」** 讨论基本认同，事件发生在 Cursor 的扩展发布链路，而非 Anthropic 官方发行渠道；Anthropic 表示正与 Cursor 协作处理。评论者对 Open VSX 是否也受影响仍有疑问，并指出公开报道未明确说明 Microsoft 官方 VS Code 扩展市场的情况，因此不宜将 Cursor 的事件直接外推到其他注册表。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cursor.com/blog/claude-code-extension-security-notice">Security notice — malicious version of Anthropic . claude - code ...</a></li>
<li><a href="https://thehackernews.com/2026/10/official-claude-code-vs-code-extension.html">Official Claude Code VS Code Extension Compromised to Install...</a></li>
<li><a href="https://thehackernews.com/2026/10/official-claude-code-vs-code-extension.html">Official Claude Code VS Code Extension Compromised to Install...</a></li>
<li><a href="https://cursor.com/blog/claude-code-extension-security-notice">Security notice — malicious version of Anthropic. claude - code ...</a></li>

</ul>
</details>

**标签**: `#supply-chain security`, `#VS Code extensions`, `#Claude Code`, `#Cursor`, `#SSH security`

---

<a id="item-tech-news-2"></a>
### [币安据报遭 63 亿美元攻击仅耗时 20 分钟](https://www.wired.com/story/the-dollar63-billion-binance-hack-was-pulled-off-in-just-20-minutes/) ⭐️ 8.0/10

据 Hacker News 收录的 Wired 报道，币安发生一宗据报涉及 63 亿美元损失的攻击，实际执行仅约 20 分钟。事件的重要性在于，它同时引发了对交易所安全、攻击准备、运营安全、损失追回以及监管问责的讨论。现有摘要没有说明被攻破的系统、具体攻击链、资产是否确已流失、币安赔付范围或执法进展，因此目前只能确认报道中的金额与执行时长，不能据此判定责任归属。

hackernews · domhudson · 10月30日 12:50 · [社区讨论](https://news.ycombinator.com/item?id=50303172)

**「事件背景」** 理解这起事件，需要结合加密货币交易所安全与朝鲜黑客活动：多家加密货币追踪机构称，朝鲜黑客组织 TraderTraitor 可能参与了这起被称为史上最大数字劫案的 Binance 攻击，但这一归属仍是追踪机构的判断。报道将这起 63 亿美元攻击作为 Binance 的纪录级事件持续追踪，涉及调查、行业回应和恢复提款计划，并指出攻击者正越来越多地采用人工智能等先进技术。

**「实际影响」** 对遭遇报道中这起攻击的用户，Binance 承诺通过安全资产基金（SAFU）承担全部损失，缓冲了直接资金损失；但攻击者已迅速将数十亿美元稳定币转换为更难冻结的资产，表明追赃成效将取决于行业冻结和转移资产的速度。

**「社区讨论」** 评论者质疑币安是否因安全疏忽而应被追责，并以 Cryptsy 案件及执法追偿效果作对照；也有人指出，20 分钟仅是执行阶段，发现或设计漏洞以及长期准备可能耗时多年。另有评论将该事件与所谓 Claude Code 供应链攻击的时间点联系起来，但这仅属个人猜测，现有材料未提供验证证据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.wired.com/story/the-dollar63-billion-binance-hack-was-pulled-off-in-just-20-minutes/">The $6.3 Billion Binance Hack Was Pulled Off in Just ... - WIRED</a></li>
<li><a href="https://cointelegraph.com/news/recap-binances-record-63b-hack-unfolded">Binance’s Record $6.3B Hack Recapped From Cointelegraph’s ...</a></li>
<li><a href="https://www.nytimes.com/2026/10/30/technology/binance-hack-ai-north-korea.html">Binance’s $6.3 Billion Hack Is Just the Start of a Risky New ...</a></li>
<li><a href="https://www.cnbc.com/2026/10/30/binance-hack-stolen-crypto-recovery.html">Binance hack : Recovering $ 6 . 3 billion in stolen crypto</a></li>
<li><a href="https://cointelegraph.com/magazine/binance-hackers-raced-to-move-billions-before-could-be-frozen">Binance Hack : How Attackers Raced to Move $ 6 . 3 B</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#cryptocurrency`, `#supply-chain security`, `#incident analysis`

---

<a id="item-tech-news-3"></a>
### [Azure 最薄弱环节：五种完整的跨租户攻陷路径](https://www.binarysecurity.no/posts/2026/10/one-root-case) ⭐️ 8.0/10

一篇漏洞研究文章称，Azure 存在五条可导致完整跨租户攻陷的路径，涉及授权缺陷、可伪造的 OAuth 回调、租户 ID 校验不足、路径遍历和 IDOR 等问题，可能削弱多租户云环境的隔离。评论者特别指出，若攻击者获知其他客户的 Azure 租户 ID，管理员同意流程的回调地址可能被伪造；文档也不应将租户 ID 用作用户认证或授权依据。目前材料尚未独立验证这些漏洞的有效性，也未确认微软是否已经修复。

hackernews · swq115 · 10月30日 10:06 · [社区讨论](https://news.ycombinator.com/item?id=50301854)

**标签**: `#Azure security`, `#cross-tenant compromise`, `#OAuth`, `#IDOR`, `#cloud vulnerability research`

---

<a id="item-tech-news-4"></a>
### [Anthropic 官方 Cursor 扩展遭供应链投毒](https://arstechnica.com/security/2026/10/anthropic-vs-code-extension-on-cursor-backdoored-for-nearly-12-hours/) ⭐️ 8.0/10

据多方报道，攻击者通过 Anthropic 在 Cursor 扩展市场中的官方账户发布了恶意版本 2.1.313，形成一次供应链投毒事件。该版本会在 Windows、macOS 和 Linux 上添加攻击者控制的 SSH 密钥、启用本地 SSH 服务并建立反向 SSH 隧道，以维持持久化访问。由于 Cursor 扩展继承集成开发环境的权限，恶意扩展可能访问本地文件、源代码和开发工具，也可能暴露开发者保存的云凭据。Anthropic 随后发布 2.1.314 替换恶意包，相关恶意版本流通近 12 小时，受影响用户最多为 5,000 名，包括手动下载者及自动拉取更新的用户。Anthropic 尚未公开通知客户，Cursor 和 Anthropic 也尚未说明攻击者如何取得官方账户的控制权。

rss · Ars Technica · 10月30日 21:09

**「背景说明」** Cursor 提供 AI 辅助开发工具及扩展市场，其扩展默认自动更新，但用户可以在设置中关闭更新。供应链投毒意味着攻击者借助受信任的软件分发渠道投放恶意代码，因此能够绕过逐个审查安装包，直接将风险扩散到扩展用户。

**「潜在影响」** 安装恶意版 2.1.313 的最多 5,000 名开发者可能面临持久化 SSH 入侵，以及本地文件、源代码、开发工具和云凭据暴露风险，但目前尚不清楚实际有多少数据被访问或外传。

**标签**: `#supply-chain security`, `#VS Code extensions`, `#Anthropic Claude`, `#Cursor`, `#developer credentials`

---

<a id="item-tech-news-5"></a>
### [币安报告 63 亿美元加密货币失窃](https://arstechnica.com/security/2026/10/hackers-steal-6-3-billion-from-binance-in-record-crypto-heist/) ⭐️ 8.0/10

全球最大加密货币交易所币安在遭遇疑似黑客攻击后暂停了所有提现，并将事件影响估算为约 63 亿美元；初步调查显示，攻击者可能攻陷了一名工程师的笔记本电脑，后续调查又发现了其他入侵点。币安称约 30 亿美元受影响资产（主要是稳定币）已被冻结，但 Elliptic 分析称，攻击者已将约 33 亿美元转换为无法冻结的数字资产，并试图兑现为传统货币。区块链情报公司 TRM Labs 把事件与朝鲜组织 TraderTraitor 联系起来，若获证实，这将成为史上规模最大的加密货币盗窃案，但归因和完整入侵路径仍在调查中。币安表示已预留超过 63.4 亿美元公司资金，其中 50 亿美元以受影响的精确代币持有，并正购买其余代币以补足，不过部分代币流动性不足且结算需要时间，补偿过程可能因此延长。

rss · Ars Technica · 10月30日 13:46

**「相关背景」** 加密货币交易所是用户将法币和数字资产相互转换、托管并进行交易的核心平台；稳定币在这类生态中承担近似现金的结算功能，因此部分被盗稳定币可通过发行方或链上追踪冻结，而已转入其他数字资产的资金则可能无法直接冻结。朝鲜黑客组织此前已被指参与加密货币盗窃，包括去年约 15 亿美元的 Bybit 攻击，但将本次事件归因于 TraderTraitor 仍是调查机构的初步判断，最终责任和完整损失规模仍待执法与链上追踪确认。

**「直接影响」** 这起攻击使 Binance 自 10 月 29 日晚起持续暂停提现，直接阻断用户提现操作；公司已为约 63 亿美元的估计损失预留逾 63.4 亿美元资金，但仍需采购低流动性代币并等待结算。Binance 曾以 11 月 1 日前恢复提现为目标，不过鉴于调查尚未结束且损失总额仍属估算，实际损失和恢复时间可能调整。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theguardian.com/business/2026/oct/29/binance-crypto-exchange-hack">North Korea is likely culprit behind $ 6 . 3 bn crypto hack ... | The Guardian</a></li>
<li><a href="https://winbuzzer.com/2026/10/30/binance-pauses-withdrawals-after-6-3-billion-crypto-theft-xcxwbn/">Binance Keeps Withdrawals Paused After $ 6 . 3 Billion Crypto Theft...</a></li>

</ul>
</details>

**标签**: `#cryptocurrency security`, `#Binance`, `#cyberattack`, `#blockchain forensics`, `#North Korea`

---

<a id="item-tech-news-6"></a>
### [Qwen3.5-4B 权重内运行 NES 模拟器](https://simonwillison.net/2026/Oct/30/nesformer/) ⭐️ 7.0/10

受 Divyansh Agrawal 的 qwenputer 项目启发，Drew Breunig 将一个可工作的 NES 6502 CPU 模拟器“烘焙”进 Qwen3.5-4B 的模型权重中，使《Super Mario Bros.》等 NES ROM 能在模型内运行，但速度很慢。Breunig 公开了使用 Opus 5.5 构建系统的提示词：先阅读 qwenputer 文章及相关源码，探索用该技术模拟 NES 芯片和 RAM、所需模型规模，以及更小、更快的模型能否达到标准时钟速度，随后要求“把它做出来”，即使速度不快。据称，Opus 在构建过程中找到并使用了 Christopher Pow 发布的 NES CPU 一致性测试 nestest.txt。相关实现以开源项目 dbreunig/nesformer 发布，并支持通过命令行指定 ROM，展示了让模型权重承载传统硬件模拟器的实验路径；但目前仅明确展示了极慢运行，缺少性能基准、达到标准时钟速度的证据及可扩展性数据，因此尚不能视为实用的 NES 模拟方案。

rss · Simon Willison · 10月30日 21:59

**「技术背景」** NESformer 延续了 qwenputer 的实验思路：把通常由软件实现的 NES 模拟器编译进标准 Qwen3.5-4B checkpoint，使 2A03 芯片所含的 6502 CPU、2 KB 工作 RAM 和卡带程序 ROM 都能在模型权重内执行。6502 是 NES 游戏逻辑的核心处理器，而 nestest 等一致性测试用于检查模拟器的指令和内存行为，因此该项目探索的是将语言模型用作可编程执行环境，而不只是生成模拟器代码。

**「实际影响」** 开发者现在可通过开源 CLI，让 NES 6502 CPU、2 KB 工作 RAM 和卡带程序 ROM 全部在标准 Qwen3.5-4B 权重中运行，从而实现可复现的模型内游戏实验。该方案目前每帧约需 1–6 秒，因此更适合研究与演示，而非实时游戏。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/dbreunig/nesformer">GitHub - dbreunig/nesformer: An NES CPU compiled into the ...</a></li>
<li><a href="https://github.com/dbreunig/nesformer">GitHub - dbreunig/nesformer: An NES CPU compiled into the ...</a></li>
<li><a href="https://explainx.ai/blog/nesformer-nes-cpu-compiled-into-qwen3-5-4b-weights-super-mario-bros-qwenputer-2026">Nesformer: NES Emulator Inside Qwen3.5 Weights Explained ...</a></li>

</ul>
</details>

**标签**: `#AI`, `#LLM`, `#model internals`, `#emulation`, `#open source`

---

<a id="item-tech-news-7"></a>
### [全球火箭发射能力缺口扩大](https://arstechnica.com/space/2026/10/analysts-find-looming-launch-crisis-is-more-severe-than-anticipated/) ⭐️ 7.0/10

Quilty Space 在最新报告中估计，到 2030 年，中国以外的商业火箭发射能力可能较卫星运营商和民用航天机构的需求少约 150 次，短缺预计在 2028 年最为严重，之后才会缓慢缓解。报告认为危机的严重程度和持续时间均高于此前预期，而且至少会贯穿本十年，最迟可能要到 2030 年代后期才开始消退。导致供给收缩的因素包括俄乌战争令俄罗斯火箭退出西方市场、亚马逊 Leo 需求增长，以及 New Glenn、Vulcan、Neutron、Terran R 和 Nova 等新一代火箭延期；Falcon 9 退出商业发射服务也进一步压缩了可用运力。若计入美国军方需求，且 SpaceX 不扩展 Falcon 9 和 Falcon Heavy 以满足国家安全任务，缺口可能翻倍。

rss · Ars Technica · 10月30日 16:12

**「缺口取决于需求与部署假设」** 该报告通过对比现有及计划中的商业发射能力与卫星、民用航天需求，估算未来五年的运力缺口。这一判断取决于是否计入美国军方需求，以及 SpaceX 是否延长 Falcon 9 和 Falcon Heavy 的部署，因此 150 次和可能翻倍属于情景估算。

**「尚未订舱的客户将承压」** 尚未预订发射且确有任务需求的卫星和民用航天机构可能难以获得运力，压力预计在 2028 年前后最为突出。

**标签**: `#space launch`, `#aerospace`, `#satellite industry`, `#launch capacity`, `#SpaceX`

---

<a id="item-tech-news-8"></a>
### [通用汽车因转售驾驶数据支付 2.2 亿美元](https://arstechnica.com/cars/2026/10/gm-to-pay-220-million-after-selling-customer-smart-driver-data/) ⭐️ 7.0/10

通用汽车同意支付 2.2 亿美元，以解决华盛顿特区与 35 个州总检察长对其转售 Smart Driver 客户数据提起的诉讼。相关数据被交给数据经纪商，再由经纪商出售给保险公司，部分驾驶者因此遭遇保险费上涨，并称自己并不知道数据会被用于此目的。此前，通用汽车与其 OnStar 子公司已与 FTC 达成独立和解，该协议于今年 1 月最终确定，禁止两家公司五年内向第三方共享地理位置或驾驶行为数据，通用汽车随后在全系停用了 Smart Driver。州级和解还将要求第三方评估通用汽车对新隐私计划的合规情况；GM 表示，联网车辆数据有助于提供更安全、更实用和个性化的体验，并承诺明确说明信息用途、保护方式及客户选择。

rss · Ars Technica · 10月30日 13:53

**「背景」** Smart Driver 是 GM 的连接车辆功能，面向家长监控青少年驾驶和成年人跟踪驾驶行为等场景，并涉及地理位置与驾驶行为数据。2024 年披露的信息显示，GM 曾将相关数据交给数据经纪商，后者再出售给保险公司，部分车主因此被提高保费，而许多车主表示不知道曾同意此类共享。此前 GM 与 FTC 达成的和解于今年 1 月最终确定，禁止 GM 及其 OnStar 子公司在五年内向第三方共享地理位置或驾驶行为数据，GM 随后停用了 Smart Driver；本次华盛顿特区和 35 州总检察长联合提出的案件则追索其向数据经纪商共享私人数据的行为。

**「实际影响」** 这起和解要求通用汽车支付 2.2 亿美元，并由第三方评估其新隐私计划的合规性；与此同时，联邦贸易委员会针对通用汽车和 OnStar 披露地理位置及驾驶行为数据的五年禁令，仍将限制其向第三方共享此类数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.attorneygeneral.gov/taking-action/attorney-general-sunday-secures-220-million-national-settlement-over-allegations-that-general-motors-shared-drivers-private-data/">Attorney General Sunday Secures $220 Million National ...</a></li>
<li><a href="https://oag.maryland.gov/News/pages/Attorney-General-Brown-Announces-$220M-Multistate-Settlement-with-General-Motors-for-Sharing-Drivers%E2%80%99-Private-Data.aspx">Attorney General Brown Announces $220M Multistate Settlement ...</a></li>
<li><a href="https://www.ftc.gov/news-events/news/press-releases/2026/01/ftc-finalizes-order-settling-allegations-gm-onstar-collected-sold-geolocation-data-without-consumers">FTC Finalizes Order Settling Allegations that GM and OnStar ...</a></li>
<li><a href="https://thehill.com/business/6182382-gm-settles-driver-data-lawsuit/">General Motors to pay $220M to settle driver data lawsuit</a></li>

</ul>
</details>

**标签**: `#data privacy`, `#connected vehicles`, `#driver telemetry`, `#FTC enforcement`, `#automotive technology`

---

<a id="item-tech-news-9"></a>
### [Apple Intelligence 将随 iOS 27.3 登陆中国](https://www.theverge.com/tech/1023974/apple-intelligence-china-ios-27-3) ⭐️ 7.0/10

Apple 将通过 iOS 27.3 在中国推出 Apple Intelligence。公司计划于 11 月 4 日先行发布 iOS 27.3 beta，为首批用户提供相关功能，正式版则定于 12 月推出。这标志着 Apple 的 AI 功能将进入中国这一重要市场，但现有报道尚未披露具体功能范围、设备兼容要求以及本地合作或监管细节。该消息源自 Apple 中国新闻室公告，并由 MacRumors 转述。

rss · The Verge · 10月30日 22:32

**「背景」** Apple Intelligence 是苹果推出的系统级人工智能功能集合，于 2024 年 6 月 10 日的世界开发者大会（WWDC）发布，并随 iOS 18 集成，采用设备端与服务器端结合的处理方式。此次 iOS 27.3 在中国的上线属于区域服务扩展，但据苹果表示，中国版本不会提供新版 Siri 及部分在 WWDC 2026 公布的功能。

**「直接影响」** 中国大陆用户将首次通过 iOS 27.3 获得 Apple Intelligence，其中测试版计划于 2026 年 11 月 4 日推出、正式版于 12 月发布，从而缩小苹果相对华为等本土厂商在 AI 功能上的竞争劣势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Apple_Intelligence">Apple Intelligence - Wikipedia</a></li>
<li><a href="https://www.macrumors.com/">MacRumors: Apple News and Rumors</a></li>
<li><a href="https://www.macrumors.com/2026/10/14/apple-intelligence-china-ios-27-3/">Apple Intelligence Coming to China in December With iOS 27.3</a></li>
<li><a href="https://www.bloomberg.com/news/articles/2026-10-14/apple-prepares-to-debut-first-ai-features-in-china-in-december">Apple Prepares to Debut First AI Features in China in December</a></li>
<li><a href="https://aiintelreport.com/enterprise-ai/apple-intelligence-china-launch-december-2026">Apple Intelligence China Launch Set for December After Two ...</a></li>

</ul>
</details>

**标签**: `#Apple Intelligence`, `#iOS`, `#AI rollout`, `#China`

---

<a id="item-tech-news-10"></a>
### [AI 巨头支持统一反抓取退出标准](https://www.theverge.com/tech/1023763/openai-google-microsoft-ai-scraping-standard-opt-out) ⭐️ 7.0/10

OpenAI、Google、Microsoft 与 Anthropic 表示将采用一种新的“策略令牌”（policy token）标准，让发布者表达反对 AI 抓取及用于训练的偏好。该机制提供可跨多家 AI 系统识别的共同退出信号，发布者因此可以一次表达偏好，而不必分别向每家公司重复设置。它有望提升出版方对 AI 数据抓取与训练使用的控制一致性，并降低多平台配置成本。现有来源尚未说明该令牌的技术实现、识别与验证方式、兼容性、时间表或实际采用范围，因此目前难以确认其覆盖效果。

rss · The Verge · 10月30日 20:26

**「背景」** 目前，网站主要通过 robots.txt 中的爬虫标识和规则向抓取工具表达偏好，而不同 AI 厂商会分别定义和使用各自的爬虫令牌。新的“policy token”标准旨在让发布者用统一信号表达 AI 抓取与训练偏好，从而不必为每家 AI 公司单独设置，但其具体技术实现和采用流程尚未披露。

**「对发布者的直接影响」** 发布者今后可通过统一的“策略令牌”一次性表达 AI 抓取与训练退出偏好，并让 OpenAI、Google、Microsoft 和 Anthropic 遵循该设置，从而减少逐家公司配置退出规则的工作；但该标准的具体执行机制与实际落地时间在现有报道中尚未说明。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theverge.com/tech/1023763/openai-google-microsoft-ai-scraping-standard-opt-out">The biggest names in AI are backing a new way to opt out of scraping</a></li>
<li><a href="https://rattlesnakesbymail.com/crawlers">Every crawler, fetcher, search bot, ads bot, and robots.txt policy token ...</a></li>
<li><a href="https://imvasa.dev/guides/ai-crawler-robots-txt-guide">AI Crawler Robots.txt Guide: 2026 AI Search &amp; Bot Rules</a></li>
<li><a href="https://www.techbuzz.ai/articles/ai-giants-unite-behind-universal-scraping-opt-out-standard">AI Giants Unite Behind Universal Scraping Opt-Out Standard</a></li>
<li><a href="https://www.theverge.com/tech/1023763/openai-google-microsoft-ai-scraping-standard-opt-out">The biggest names in AI are backing a new way to opt out of ...</a></li>

</ul>
</details>

**标签**: `#artificial intelligence`, `#web scraping`, `#publisher controls`, `#AI training data`, `#industry standards`

---

<a id="item-tech-news-11"></a>
### [谷歌卫星首次从太空传回 AI 响应](https://www.theverge.com/tech/1023528/google-project-suncatcher-ai-satellite-transmission) ⭐️ 7.0/10

谷歌表示，其搭载 AI 芯片的卫星已首次从太空生成并传回响应。该卫星成功启动 Tensor Processing Units（TPU），并由机载 Gemma 4 模型根据提示词生成了一首关于身处太空的俳句，其中包含“Blue marble below / Data streams in …”等片段。这一演示展示了在卫星端运行边缘 AI 并向地球传输结果的可能性，但公开技术细节有限且主要依据谷歌公告，目前尚不足以证明其已带来突破性的空间计算能力。

rss · The Verge · 10月30日 18:21

**「项目背景」** Project Suncatcher 是 Google 将数据中心级 TPU 算力部署到轨道的太空计算项目，旨在让卫星直接运行 AI 模型，减少将数据传回地面处理的需求。此次测试中，卫星成功启动 TPU 并运行 Gemma 4，将生成的太空主题俳句传回地球，但具体性能和工程细节仍主要来自 Google 自身披露。

**「在轨 AI 的初步验证」** 此次演示表明，配备 TPU 的卫星已能在轨运行 Gemma 4 并将推理结果传回地面，为太空自主系统部署边缘 AI 提供了可行性验证；但现有原型受功耗限制一次只能启用一个处理器，且仍需通过热与辐射测试，尚不能证明其具备长期稳定运行能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cryptopolitan.com/googles-first-orbital-ai-writes-a-haiku-as-the-data-center-race-moves-to-space/">Google &#x27;s first orbital AI writes a haiku as the... - Cryptopolitan</a></li>
<li><a href="https://hwbusters.com/news/project-suncatchers-orbiting-tpu-sends-back-its-first-ai-answer-and-its-a-haiku/">Project Suncatcher &#x27;s Orbiting TPU Sends Back Its First AI Answer...</a></li>
<li><a href="https://www.theverge.com/tech/1023528/google-project-suncatcher-ai-satellite-transmission">Google ’s satellite AI server transmits its first response to... | The Verge</a></li>
<li><a href="https://interestingengineering.com/ai-robotics/google-space-data-center-orbital-poem">Google&#x27;s space data center chip writes its first-ever poem in orbit</a></li>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/google-research/project-suncatcher-satellite-response/">Google receives response from Project Suncatcher prototype...</a></li>
<li><a href="https://hwbusters.com/news/project-suncatchers-orbiting-tpu-sends-back-its-first-ai-answer-and-its-a-haiku/">Project Suncatcher &#x27;s Orbiting TPU Sends Back Its First AI Answer...</a></li>

</ul>
</details>

**标签**: `#edge AI`, `#AI hardware`, `#satellite computing`, `#Google TPU`, `#Gemma`

---

<a id="item-tech-news-12"></a>
### [Applebee’s 应用硬编码凭据暴露客户数据](https://techcrunch.com/2026/10/30/applebees-exposed-customers-personal-data-after-leaving-database-password-in-app/) ⭐️ 7.0/10

据 Zack Whittaker 于 2026 年 10 月 30 日发布的 TechCrunch 独家报道，一名安全研究人员在 Applebee’s 应用中发现了硬编码的数据库凭据。报道称，该凭据可能使未经授权的人员不受限制地访问客户个人数据，因而构成严重的移动应用安全与隐私风险。现有内容未说明相关数据是否已被实际获取、具体涉及哪些信息或漏洞存在了多长时间。

rss · TechCrunch · 10月30日 21:48

**「背景」** 硬编码数据库凭据是指密码被直接嵌入移动应用代码，而不是在运行时安全获取；提取应用的人可能绕过正常身份验证并尝试访问后端数据库。Applebee’s 的 Android 应用被曝包含此类凭据，报道称其关联数据库含姓名、电子邮箱、出生日期、电话号码、邮编、退伍军人身份、登录记录及 IP 地址等数据，甚至可能被修改，但目前没有证据表明攻击者实际利用了漏洞或已造成经确认的数据泄露。

**「客户数据泄露风险」** Applebee’s 应用中的硬编码数据库凭据可被利用，使攻击者不受限制地访问客户个人数据，直接增加相关客户的隐私泄露风险。Dine Brands 已介入调查，但目前尚无证据表明支付卡数据或登录凭据遭泄露，受影响范围与处置措施应以官方通知为准。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://techcrunch.com/2026/10/30/applebees-exposed-customers-personal-data-after-leaving-database-password-in-app/">Applebee&#x27;s exposed customers&#x27; personal data after leaving ...</a></li>
<li><a href="https://www.androguider.com/2026/10/applebees-app-exposed-customer-data.html">Applebee’s App Exposed Customer Data After Hardcoded Database ...</a></li>
<li><a href="https://daily.dev/posts/applebee-s-exposed-customers-personal-data-after-leaving-database-password-in-app-rytxbqqpa">Applebee’s exposed customers’ personal data after...</a></li>
<li><a href="https://techcrunch.com/2026/10/30/applebees-exposed-customers-personal-data-after-leaving-database-password-in-app/">Applebee&#x27;s exposed customers&#x27; personal data after leaving ...</a></li>
<li><a href="https://www.whalesbook.com/news/English/technology/Dine-Brands-Probes-Applebees-Data-Security-Lapse/6ae514304fc30694db54dd14">Dine Brands Probes Applebee’s Data Security Lapse</a></li>
<li><a href="https://www.androguider.com/2026/10/applebees-app-exposed-customer-data.html">Applebee’s App Exposed Customer Data After Hardcoded Database ...</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#mobile apps`, `#hardcoded credentials`, `#data exposure`, `#privacy`

---

<a id="item-tech-news-13"></a>
### [Community safety report and new protections for teens](https://openai.com/index/community-safety-report-and-new-protections-for-teens) ⭐️ 6.0/10

OpenAI says it is expanding ChatGPT violence-prevention safeguards, intervening earlier, and committing to public safety reporting for teens.

rss · OpenAI News · 10月30日 09:00

**标签**: `#AI safety`, `#ChatGPT`, `#youth safety`, `#violence prevention`, `#public safety reporting`

---