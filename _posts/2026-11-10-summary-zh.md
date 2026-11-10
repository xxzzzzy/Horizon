---
layout: default
title: "Horizon Summary: 2026-11-10 (ZH)"
date: 2026-11-10
lang: zh
---

> 从 130 条内容中筛选出 18 条重要资讯。

---

**科技新闻**
1. [第三方报告称消费版 Gemini 或引入人工审阅](#item-tech-news-1) ⭐️ 8.0/10
2. [OpenSSH 与 musl 严重漏洞正遭利用](#item-tech-news-2) ⭐️ 8.0/10
3. [Claude Code 设置文件导致 GitHub 密钥泄露](#item-tech-news-3) ⭐️ 8.0/10
4. [研究人员攻破汽车厂商安卓应用远程控车](#item-tech-news-4) ⭐️ 8.0/10
5. [Claude Fable 5.2 与 Mythos 5.2 的实测与基准争议](#item-tech-news-5) ⭐️ 7.0/10
6. [Watched Earth：一周内过境卫星与实拍影像](#item-tech-news-6) ⭐️ 7.0/10
7. [Kalshi 遭亏损者起诉，指控违反州博彩法](#item-tech-news-7) ⭐️ 7.0/10
8. [黄仁勋婚外情引发国家安全调查](#item-tech-news-8) ⭐️ 7.0/10
9. [温德姆应用安全失误致客户数据暴露](#item-tech-news-9) ⭐️ 7.0/10
10. [Waymo 无人车更新后仍被指违规超越校车](#item-tech-news-10) ⭐️ 7.0/10
11. [Anthropic&\#x27;s super bug-finding Mythos model is going into Cisco and IBM products](#item-tech-news-11) ⭐️ 7.0/10
12. [HOPE 用二阶剪枝降低 MoE 推理内存](#item-tech-news-12) ⭐️ 7.0/10
13. [提示 Claude Fable 5.2：明确告诉模型代码库归你所有](#item-tech-news-13) ⭐️ 6.0/10
14. [用 Claude Code 定位神秘蜂鸣声](#item-tech-news-14) ⭐️ 6.0/10
15. [NVIDIA 发布日本金融合成人格数据集](#item-tech-news-15) ⭐️ 6.0/10
16. [Control Room：集中追踪并停止模型工作负载](#item-tech-news-16) ⭐️ 6.0/10
17. [新 AI 模型模拟从沙粒到蛋白质的物质行为](#item-tech-news-17) ⭐️ 6.0/10
18. [HUMAIN 与 Infra 达成 6.667 亿美元 AI 基础设施融资协议](#item-tech-news-18) ⭐️ 6.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [第三方报告称消费版 Gemini 或引入人工审阅](https://github.com/thisisme6598/gemini_files/) ⭐️ 8.0/10

一份第三方技术调查报告称，用户为消费版 Gemini 启用 Connected Apps 并授权 Gmail 或 Google Drive 后，相关邮件和文件内容有时会进入 Google 的人工标注流程。讨论将风险限定在消费版 Gemini：Google Workspace 版 Gemini 及 Workspace Intelligence 据称仍声明不会接受人工审阅。由于所给材料未提供可独立核验的完整证据、具体触发条件或 Google 官方确认，目前无法确定审阅范围、频率以及数据是否会被保留或用于模型改进，但这一说法仍凸显连接应用权限、敏感数据隔离和 AI 治理披露方面的重大隐私风险。

hackernews · gf74918 · 11月9日 18:24 · [社区讨论](https://news.ycombinator.com/item?id=50429426)

**「背景」** 这里的“Connected Apps”是指用户授权 Gemini 连接 Gmail、Drive 等服务后，助手可在具体任务中读取相关数据；断开 Workspace 连接也会同时切断 Drive、Docs、Keep 等应用及个人数据访问。Consumer Gemini 与面向企业的 Workspace Gemini/Workspace Intelligence 适用不同的产品与数据治理说明，讨论中的范围澄清称 Workspace 版本仍声明不受同类人工审查影响，因此本事件主要针对消费者版及其已授权连接应用。Google 的隐私说明将“人工审查者”列为可能接触数据的一方，但现有材料并未提供 Google 对本报告所指文件、邮件标注流程的官方确认。

**「用户影响」** 在 Consumer Gemini 中连接 Gmail 或 Google Drive 的用户，应撤销不必要的应用授权、在 Gemini Apps Activity 中关闭活动保存并删除既有记录，以降低邮件、文件和对话被人工审核、留存或用于训练的风险。该发现目前主要源于第三方调查，Workspace Gemini 是否完全豁免以及 Connected Apps 数据的具体审核范围仍待 Google 官方确认。

**「隐私担忧与实际体验」** 评论者普遍对“AI 能调用个人邮件后内容可能被人工查看”感到沮丧，并认为产品至少应明确披露；一名用户还怀疑 Gemini 曾异常准确地回应其邮件所涉事项，但该观察只是个人体验，不能证明人工审阅确实发生。讨论同时担忧人工标注员接触数据、数据被标记后用于训练或泄露，以及 Workspace 与消费版之间可能存在治理差异，不过这些扩展风险和泄露可能性并未由所给材料证实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tech.yahoo.com/ai/gemini/articles/stop-gemini-accessing-emails-two-103013901.html">Stop Gemini from accessing your emails with these two hidden settings</a></li>
<li><a href="https://proton.me/lumo/ai/gemini-privacy-policy">Gemini ’s privacy policy explained | Proton</a></li>
<li><a href="https://proton.me/blog/turn-off-gemini-on-android">Google AI is watching: How to turn off Gemini on Android | Proton</a></li>
<li><a href="https://windowsforum.com/threads/gmail-privacy-and-ai-training-how-to-opt-out-of-gemini-data-use.390715/">Gmail Privacy and AI Training: How to Opt Out of Gemini Data Use</a></li>

</ul>
</details>

**标签**: `#Google Gemini`, `#human annotation`, `#data privacy`, `#connected apps`, `#Google Workspace`

---

<a id="item-tech-news-2"></a>
### [OpenSSH 与 musl 严重漏洞正遭利用](https://arstechnica.com/security/2026/11/vulnerability-that-lets-hackers-ssh-into-linux-devices-is-under-active-exploitation/) ⭐️ 8.0/10

研究人员称...。...。GreyNoise 周一...。攻击活动...。OpenSSH 已发布...，但所给材料未列明受影响版本、具体触发条件或升级版本，因而难以仅凭该报道判断完整影响范围。

rss · Ars Technica · 11月9日 19:41

**「背景」** OpenSSH 的 sshd 负责处理 SSH 登录，而 musl 是 Alpine Linux 等部分轻量级 Linux 发行版采用的代码库。此次名为 \*sshole 的漏洞源于 OpenSSH 与未使用 PAM 的 musl 环境之间的交互，攻击者可利用超长密码绕过认证限制，登录某些原本未设置密码或禁止密码认证的账户。该漏洞公开后数日便出现实际入侵，OpenSSH 已发布修复，受影响系统需升级至 OpenSSH 10.6p2 或发行版提供的补丁版本，并重启 sshd。

**「实际影响」** 同时使用 OpenSSH 与 musl 且满足特定条件的 Linux 主机，可被攻击者通过 CVE-2026-123158 在数秒内取得未认证的高权限访问；Greynoise 已确认涉及 6 个攻击 IP 的利用后活动，并观察到 Python3 运行时和 TAC Agent 后门，因此运营方应立即安装已发布的 OpenSSH 修复并排查失陷痕迹。不过，并非所有 SSHole 活动都能归因于 GT10，且现有资料未列明完整的受影响版本范围，暴露情况仍需结合实际配置核查。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://radar.cloudflare.com/security/zero-wire/sshole">sshole : OpenSSH password bypass on musl Linux | Cloudflare Radar</a></li>
<li><a href="https://thehackernews.com/2026/11/hackers-exploited-openssh-sshole-flaw.html">Hackers Target OpenSSH SSHole Flaw Within Hours of Disclosure...</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/openssh-flaw-lets-attackers-log-into-password-disabled-linux-accounts/">OpenSSH flaw lets attackers log into password-disabled Linux accounts</a></li>
<li><a href="https://sshole.events.greynoise.io/">SSHole (CVE-2026-123158) Activity 2026 | Tagged IP Analysis</a></li>

</ul>
</details>

**标签**: `#Linux security`, `#OpenSSH`, `#musl`, `#active exploitation`, `#authentication bypass`

---

<a id="item-tech-news-3"></a>
### [Claude Code 设置文件导致 GitHub 密钥泄露](https://arstechnica.com/ai/2026/11/claude-code-settings-files-expose-thousands-of-secrets-on-github/) ⭐️ 8.0/10

Apiiro 的 AI 安全研究人员发现，Claude Code 在用户选择“Yes, and don’t ask again”批准自动执行 shell 命令后，会把规则写入本机的 \`.claude/settings.local.json\`，并且常常原样保存命令，使其中嵌入的 API 令牌、数据库密码、root 登录凭据或私钥进入该文件。虽然 Anthropic 文档称此文件会被加入开发者的全局 \`.gitignore\`，但仓库级配置并不继承这一保证，因此克隆仓库或把现有文件夹初始化为仓库后，该文件可能被意外上传；在许多案例中，Apiiro 称 Claude Code 本身会在用户不知情时提交相关变更。研究人员在公开 GitHub 仓库中发现了超过 100,000 个此类设置文件被上传的案例，其中约 1,100 个来自 63 个不同组织的案例包含 API 令牌、数据库密码或私钥等秘密。即使从原仓库删除这些文件，GitHub 分叉仍可能保留泄露的密钥。

rss · Ars Technica · 11月9日 17:24

**「背景」** Claude Code 的命令授权机制允许开发者保存常用 shell 命令的授权规则，以避免重复确认；问题不在这一功能本身，而在部分规则保留了包含凭据的完整命令文本。Git 的 \`.gitignore\` 规则是否生效取决于其所在层级和仓库配置，全局忽略项无法保证同一设置文件在每个克隆或新建仓库中都会被排除。

**「影响」** 使用 Claude Code 并曾在获批命令中直接写入凭据的开发者，面临 API 令牌、密码或私钥被公开提交并继续存在于分叉中的风险，需要撤销或轮换相关凭据并检查仓库历史与分叉。

**标签**: `#AI security`, `#Claude Code`, `#secret leakage`, `#GitHub`, `#developer tools`

---

<a id="item-tech-news-4"></a>
### [研究人员攻破汽车厂商安卓应用远程控车](https://www.theregister.com/security/2026/11/09/researchers-pwn-automakers-android-apps-to-remotely-unlock-cars-honk-horns/5308483) ⭐️ 8.0/10

两名研究人员在澳大利亚和美国演示了针对汽车厂商 Android 应用的攻击链：先绕过 Web 应用防火墙（WAF），再利用默认登录凭据访问应用功能。研究人员由此实现了对车辆的远程控制，包括解锁汽车和鸣笛。该漏洞链凸显了联网汽车应用在访问防护和身份认证设计上的风险，当两者同时失效时，攻击者可能将应用权限转化为对车辆的直接操作能力。现有材料未披露受影响的汽车品牌、车型、应用版本、漏洞编号、实际暴露规模以及厂商的修复或披露进展，因此影响范围尚不明确。

rss · The Register · 11月9日 17:31

**「背景」** 联网汽车的远程功能通常由车主的制造商 Android 应用调用云端服务完成，因此应用、Web API 与账户认证任一环节失守，都可能把“解锁、鸣笛”等指令传递到车辆。Web 应用防火墙（WAF）用于拦截异常或恶意请求，而默认登录凭据若未在部署时更换，也会形成可被直接利用的认证缺口；此次演示的核心正是将 WAF 绕过与默认凭据结合，在澳大利亚和美国实现远程车辆控制。

**「实际影响」** 研究人员利用两家汽车厂商 Android 应用中的 WAF 绕过与默认凭据，成功远程启动车辆发动机、闪灯并鸣笛，使受影响账户可直接转化为车辆控制权限。两家厂商在收到报告后约两小时内修复漏洞并轮换相关凭据，但完整攻击链仅在美国账户和车辆上验证，而受影响系统实际覆盖多个地区。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theregister.com/security/2026/11/09/researchers-pwn-automakers-android-apps-to-remotely-unlock-cars-honk-horns/5308483">Researchers pwn automakers ’ Android apps to remotely unlock ...</a></li>
<li><a href="https://www.theregister.com/security/2026/11/09/researchers-pwn-automakers-android-apps-to-remotely-unlock-cars-honk-horns/5308483">Researchers pwn automakers ’ Android apps to remotely unlock ...</a></li>
<li><a href="https://samcurry.net/forgerock">Hacking Two Automakers : ForgeRock Path Confusion, RCE, and...</a></li>

</ul>
</details>

**标签**: `#connected-car security`, `#Android apps`, `#authentication bypass`, `#web application firewalls`, `#vehicle remote control`

---

<a id="item-tech-news-5"></a>
### [Claude Fable 5.2 与 Mythos 5.2 的实测与基准争议](https://www.anthropic.com/claude-fable-and-mythos-5-2) ⭐️ 7.0/10

该条目聚焦 Anthropic 的 Claude Fable 5.2 与 Mythos 5.2 发布，但由于未提供原始公告正文，目前无法核实两款模型的准确规格、定位、兼容性或官方基准数据。现有讨论主要围绕 Fable 5.2 的编码与代码审查表现：一名用户让它审查一个由 Opus 5.5 开发的浏览器内机器视觉项目，模型在半小时内耗尽原本 5 小时的 token 配额并报告 7 个严重漏洞，用户同时提醒这些发现是否成立仍待确认。另一名早期测试者称，Fable 5.2 在两天内将一个 60 万行 Fortran 代码库中的计算材料科学工作提速 36 倍，但该说法尚未得到独立验证。社区还质疑发布材料中的基准设计，包括将 Fable xHigh 与 Carbon Med 对比、Carbon 的 effort-intel 曲线异常，以及 Cyber 和 robodojo 比较对象的选择。

hackernews · lairv · 11月9日 18:01 · [社区讨论](https://news.ycombinator.com/item?id=50429068)

**「背景」** Claude Fable 5.2 和 Claude Mythos 5.2 是 Anthropic 同批发布的两个模型版本，社区主要将 Fable 5.2 与 Opus 5.5、Sonnet 5.5 在代码审查和基准测试中进行比较。公告披露，Fable 5.2 在 Quantum ESPRESSO 声子代码的 13 个测试案例中，将同一 GPU 上的平均耗时从 3.3 小时降至不足 4 分钟，速度约提升 36 倍；讨论者也关注不同模型的推理强度设置是否使基准对比公平。

**「对用户的实际影响」** 对需要更强编码与代码审查能力的用户，Anthropic 的评测显示 Claude Fable 5.2 在几乎所有已测维度上高于 Opus 5.5，且 Fable 5.2 已向所有用户开放，因此它可直接成为现有 Opus 5.5 工作流的新候选。不过，目前公开的速度、价格和基准数据主要来自 Anthropic，独立真实负载测试仍待完成，实际升级收益尚不能仅凭官方榜单确认。

**「社区讨论」** 部分试用者认为 Fable 5.2 编程能力强、能在大型代码库中发现严重问题；也有人认为 Anthropic 各系列已更加均衡，Fable 5.2 与 Opus 5.5 在普通任务上差异不大，需要提高提示目标才能拉开差距。对官方基准的选择和呈现存在明显分歧；至于 OpenAI 与 Anthropic 互相跟随发布、并可能很快推出 Astra 的说法，则只是社区推测。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/claude-fable-and-mythos-5-2">Introducing Claude Fable 5 . 2 and Claude Mythos 5 . 2 \ Anthropic</a></li>
<li><a href="https://www.anthropic.com/claude-fable-and-mythos-5-2">Introducing Claude Fable 5.2 and Claude Mythos 5.2 \ Anthropic</a></li>
<li><a href="https://www.online-tech-tips.com/anthropic-claude-fable-5-2-mythos-5-2/">Anthropic releases Claude Fable 5.2 and Mythos 5.2 with ...</a></li>

</ul>
</details>

**标签**: `#large-language-models`, `#AI model releases`, `#software engineering`, `#model evaluation`

---

<a id="item-tech-news-6"></a>
### [Watched Earth：一周内过境卫星与实拍影像](https://www.watched.earth/) ⭐️ 7.0/10

开源项目 Watched Earth 可让用户输入任意地点，查找过去 7 天内从该地上空经过的卫星，并查看对应过境时刻的真实遥感影像。它基于 CelesTrak 星历目录进行 SGP4 轨道计算，在浏览器中追踪超过 1.7 万个在轨物体，开发者称计算耗时约半秒。项目使用 GPU 绘制轨道并逐帧求解开普勒方程，同时针对 Sentinel-2 时间戳通常与卫星实际过境相差 5 至 10 分钟的问题进行了校正。它只展示相应卫星实际拍摄的 Sentinel-2、Landsat 和 NASA 影像，并声明不会存储用户位置，源代码已发布在 GitHub。

hackernews · a585gupt · 11月9日 17:51 · [社区讨论](https://news.ycombinator.com/item?id=50428907)

**「背景」** SGP4 可根据轨道参数推演卫星在指定时刻的位置，而 Sentinel-2、Landsat 等地球观测卫星会在绕行地球期间持续拍摄地表。由于传感器成像时间有时不等于卫星经过目标地点的时间，将影像与对应过境事件准确匹配，是把轨道数据与真实照片关联起来的关键。Watched Earth 将这一匹配流程与 NASA 图像归档结合，用于展示指定地点过去七天内相关卫星的过境记录及实际拍摄结果。

**「实际影响」** ...。...。

**「社区评价」** 评论者普遍认为项目兼具视觉表现与实用性，尤其赞赏其将轨道渲染、地面轨迹、过境时间序列和多源影像整合到同一界面，以及能够查看卫星实际拍摄的对应影像。一位从事地理空间工作并使用哥白尼数据服务的用户认为它比同类站点更易用，也可用于规划背包旅行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/dev-Armaan/satellites">GitHub - dev-Armaan/satellites</a></li>
<li><a href="https://www.watched.earth/">Watched · Something watched you this week</a></li>
<li><a href="https://browser.dataspace.copernicus.eu/?zoom">Copernicus Browser</a></li>
<li><a href="https://www.watched.earth/">Watched · Something watched you this week</a></li>

</ul>
</details>

**标签**: `#satellite tracking`, `#earth observation`, `#orbital mechanics`, `#browser graphics`, `#open source`

---

<a id="item-tech-news-7"></a>
### [Kalshi 遭亏损者起诉，指控违反州博彩法](https://arstechnica.com/tech-policy/2026/11/man-who-lost-308000-on-sports-bets-sues-kalshi-for-offering-illegal-gambling/) ⭐️ 7.0/10

华盛顿州贝尔维尤居民斯科特·布莱特在 Kalshi 进行体育赛事押注后损失超过 30.8 万美元，并于 9 月 24 日在金县高等法院起诉 Kalshi，指其违反州网络博彩禁令，要求获赔逾 58 万美元。Kalshi 于 10 月 30 日提出驳回动议并要求将案件移交给华盛顿州西区联邦地区法院，否认布莱特参与的是“博彩”，而称其为仅受联邦监管的“事件合约”。布莱特援引华盛顿州自 2006 年起禁止互联网博彩，以及非法博彩损失者可向经营者追偿的法律；州总检察长此前起诉 KalshiEX LLC 时也主张可追回华盛顿居民的全部损失。华盛顿州已赢得限制 Kalshi 可在州内提供的投注类型的法院命令，但该命令在布莱特亏损后才生效。此案仍处于早期阶段，将检验州博彩法能否适用于预测市场，以及失败的顾客能否通过个人诉讼获得返还。

rss · Ars Technica · 11月9日 21:13

**「案件涉及预测市场的监管边界」** 这场诉讼的核心冲突，是 Kalshi 将相关交易认定为受联邦监管的事件合约，而布莱特和华盛顿州将其视为州法禁止的博彩。州法中的博彩损失追偿机制既可能由州总检察长代表居民执行，也可能成为个人亏损者主张退款的依据。

**「个人退费请求可能形成新的救济路径」** 若法院接受布莱特的州法追偿主张，其他在违法期间亏损的 Kalshi 用户可能获得个人退款路径；若“事件合约仅受联邦监管”的抗辩成立，这类州法院追偿主张将受到限制。

**标签**: `#prediction markets`, `#online gambling`, `#regulation`, `#Kalshi`, `#technology policy`

---

<a id="item-tech-news-8"></a>
### [黄仁勋婚外情引发国家安全调查](https://arstechnica.com/tech-policy/2026/11/ceo-jensen-huang-admits-affair-as-nvidia-probes-possible-chinese-espionage/) ⭐️ 7.0/10

英伟达创始人兼 CEO 黄仁勋承认与新加坡客户 Megaspeed 高管 Alice Huang 发生婚外情；美国情报界认为，后者曾被中国国家安全部招募为间谍。英伟达董事会因近期报道称黄仁勋成为外国情报行动目标，宣布开展独立调查，黄仁勋表示将配合并为辜负员工信任致歉。报道指出，这一事件不仅是个人丑闻，也可能影响这位 AI 芯片行业领袖的治理与国家安全审查，并给英伟达游说美国放宽芯片出口限制及维持中国市场准入带来阻力。英伟达股价在调查启动后下跌逾 4%，但现有材料未提供相关情报文件或美国政府的正式回应。

rss · Ars Technica · 11月9日 15:23

**「背景」** 黄仁勋是英伟达创始人兼 CEO，也是这家 AI 芯片巨头在人工智能浪潮中的核心人物；英伟达对华业务及美国芯片出口管制，使其领导层状况同时具有公司治理和国家安全意义。相关报道援引美国官员依据情报信息撰写的备忘录，称一名英伟达新加坡客户高管被招募为中国国家安全部工作，并与黄仁勋有婚外关系；英伟达董事会因此把事件作为针对其创始人的外国情报行动展开独立调查。现有材料没有公开具体情报文件或直接证据，相关身份与活动仍属官方判断和媒体披露。

**「实际影响」** 对英伟达及其投资者而言，调查启动后股价下跌逾 4%，而黄仁勋与疑似中国间谍的关系尚未证实，却可能削弱其治理信誉，并增加公司游说美国放宽对华芯片出口限制、维持中国市场准入的难度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nytimes.com/2026/11/08/technology/nvidia-investigation-jensen-huang-china.html">Nvidia Opens Investigation Into Jensen Huang’s Relationship ...</a></li>
<li><a href="https://www.cbsnews.com/news/nvidia-jensen-huang-investigation-china-intelligence/">Nvidia investigates CEO Jensen Huang over Chinese espionage ...</a></li>
<li><a href="https://www.cnbc.com/2026/11/08/nvidia-jensen-huang-investigation-china-spy.html">Nvidia investigates CEO Jensen Huang &#x27;s relationship with alleged...</a></li>
<li><a href="https://www.aljazeera.com/news/2026/11/9/why-is-nvidias-jensen-huang-at-the-centre-of-a-us-china-spy-scandal">Why is Nvidia ’s Jensen Huang at the centre of a US- China spy...</a></li>

</ul>
</details>

**标签**: `#Nvidia`, `#Jensen Huang`, `#national security`, `#Chinese espionage`, `#AI chips`

---

<a id="item-tech-news-9"></a>
### [温德姆应用安全失误致客户数据暴露](https://techcrunch.com/2026/11/09/hotel-giant-wyndham-exposed-customer-data-after-app-security-lapse/) ⭐️ 7.0/10

据 TechCrunch 报道，温德姆在面向客户的应用程序中遗留了一个硬编码凭据，任何人利用该凭据都可能访问客户数据。现有信息尚未说明受影响的数据范围、凭据暴露的持续时间或是否曾发生实际未经授权的访问。温德姆拒绝对能否检查过去的异常访问作出说明，因此历史访问情况仍无法确认。

rss · TechCrunch · 11月9日 23:03

**「背景」** “硬编码凭据”是指开发者把数据库密码或 API 密钥直接写入随应用分发的代码中；由于客户端可被逆向分析，这类密钥无法像服务端机密一样得到保护。此前，Applebee’s 移动应用也被发现使用硬编码数据库凭据，暴露了姓名、联系方式、生日和账户元数据，研究人员披露后该应用进行了修复，说明移动端凭据管理缺陷可能绕过正常身份验证并直接触达客户记录。

**「用户影响」** Wyndham 客户应用用户的姓名、邮箱、会员编号、用于维持登录状态的 JWT 令牌及 Wyndham 内部文件可能被未授权访问。由于 Wyndham 未说明能否排查历史未经授权的访问行为，实际数据被查看或滥用的范围仍无法确定。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.techradar.com/pro/security/applebees-forced-to-fix-serious-security-issue-which-exposed-customer-data">Researcher found hardcoded credentials in Applebee&#x27;s mobile app</a></li>
<li><a href="https://techcrunch.com/2026/11/09/hotel-giant-wyndham-exposed-customer-data-after-app-security-lapse/">Hotel giant Wyndham exposed customer data after app security ...</a></li>
<li><a href="https://daily.dev/posts/hotel-giant-wyndham-exposed-customer-data-after-app-security-lapse-ag5qjtv06">Hotel giant Wyndham exposed customer data after app...</a></li>

</ul>
</details>

**标签**: `#application security`, `#hardcoded credentials`, `#data exposure`, `#Wyndham`

---

<a id="item-tech-news-10"></a>
### [Waymo 无人车更新后仍被指违规超越校车](https://techcrunch.com/2026/11/09/waymo-robotaxis-kept-illegally-passing-school-buses-after-software-fix-feds-say/) ⭐️ 7.0/10

联邦监管机构称，Waymo 的自动驾驶出租车在相关软件更新部署近一年后，仍被指非法超越校车。更新后的违规行为使 Waymo 缺陷修复的有效性、回归测试和部署后安全监测受到质疑，并引发对自动驾驶安全验证及监管力度的关注。现有材料未说明监管机构名称、事发地点、违规次数、具体软件版本或判定违法的法律依据，也未提供 Waymo 的回应，因此尚不足以判断事件规模和技术根因。

rss · TechCrunch · 11月9日 15:24

**「相关背景」** Waymo 的自动驾驶车辆此前因驶过停靠的校车而引发美国联邦监管机构关注，相关事件还促使公司采取软件召回措施。Waymo 称已于 2025 年 11 月 17 日为所有受影响车辆完成软件更新，但美国国家公路交通安全管理局（NHTSA）表示，大多数相关事件发生在此次更新之后，因此问题并未因该修复而彻底解决。

**「安全与监管影响」** ...

<details><summary>参考链接</summary>
<ul>
<li><a href="https://techcrunch.com/2026/11/09/waymo-robotaxis-kept-illegally-passing-school-buses-after-software-fix-feds-say/">Waymo robotaxis kept illegally passing school buses after software ...</a></li>
<li><a href="https://news.google.com/stories/CAAqNggKIjBDQklTSGpvSmMzUnZjbmt0TXpZd1NoRUtEd2lzbXVTUEVCR2JmanpuQUFEZ1hTZ0FQAQ?hl=en-US&amp;gl=US&amp;ceid=US:en">Waymo to recall software after robotaxis pass school buses ...</a></li>
<li><a href="https://techcrunch.com/2026/11/09/waymo-robotaxis-kept-illegally-passing-school-buses-after-software-fix-feds-say/">Waymo robotaxis kept illegally passing school buses after software ...</a></li>
<li><a href="https://intelligibberish.com/articles/2026-03-30-waymo-school-bus-training-failure-ai-safety-limits/">A School District Tried to Help Train Waymo &#x27;s Robots... | Intelligibberish</a></li>

</ul>
</details>

**标签**: `#Waymo`, `#robotaxis`, `#autonomous vehicles`, `#AI safety`, `#transportation regulation`

---

<a id="item-tech-news-11"></a>
### [Anthropic&\#x27;s super bug-finding Mythos model is going into Cisco and IBM products](https://www.theregister.com/ai-and-ml/2026/11/10/anthropics-super-bug-finding-mythos-model-is-going-into-cisco-and-ibm-products/5308616) ⭐️ 7.0/10

Cisco and IBM are planning to embed Anthropic&\#x27;s Mythos bug-finding capabilities into enterprise security products without exposing the underlying model.

rss · The Register · 11月10日 00:00

**标签**: `#AI security`, `#vulnerability detection`, `#Anthropic`, `#enterprise software`, `#Cisco and IBM`

---

<a id="item-tech-news-12"></a>
### [HOPE 用二阶剪枝降低 MoE 推理内存](https://huggingface.co/blog/amazon/higher-order-pruning-experts) ⭐️ 7.0/10

Hugging Face 博客介绍了 HOPE（Higher-Order Pruning of Experts），这是一种面向混合专家（MoE）语言模型的二阶专家剪枝方法：它无需重新训练即可永久删除低价值专家，并可与量化组合，以降低推理内存且避开动态加载或卸载带来的延迟。问题在于模型规模与内存占用同步增长，例如 Qwen3.5-122B 的 48 个 MoE 层各有 256 个专家，每个 token 每层仅激活 8 个，专家 MLP 却占其约 250 GB 参数内存的 95%。HOPE 不再像一阶方法那样独立评分专家，而是用一次校准前向传播构建 F 矩阵：其对角线表示单个专家重要性，非对角线表示共同激活专家的成对协作贡献；随后通过带连续松弛并舍入为二元解的非凸二次规划选择剪枝集合，标准 QP 求解器每层约需 1–2 秒。实验覆盖 Qwen3.5-122B、Qwen3.5-35B 和 GLM-4.5-Air，使用 Evol-CodeAlpaca 与 SWE-Bench Verified 轨迹校准，并在 10%–50% 剪枝率下以 REAP、MAN、EAN、Frequency 为基线、在 Tulu3 和 SWE-Bench Pro 上测试；HOPE 获得 5 种方法中最佳平均排名 2.07，39% 的条件排名第一、67% 排名第二，50% 剪枝时在代理式编码任务上相对次优方法最高提升 6.1%。F 矩阵对角线几乎可复现 REAP 的专家排序，说明增益主要来自二阶交互项，但所给节选未披露绝对任务分数、实际内存降幅或完整质量损失，因此目前更适合证明相对剪枝效果，而非完整的部署收益。

rss · Hugging Face Blog · 11月9日 12:34

**「背景：MoE 专家剪枝」** 混合专家（MoE）语言模型通过路由器为每个 token 激活少量 top-K 专家，但推理时仍需让全部专家 MLP 驻留内存，因此总参数量会直接推高显存需求。早期的一次性专家剪枝方法，如结合路由门控值与专家激活范数的 REAP，主要按各专家的独立贡献评分，忽略了经常共同激活的专家之间的协同关系。HOPE 进一步引入专家间成对交互的二阶目标，通过最小化剪枝误差主要项的可计算上界来选择删除集合；理论上，忽略交互项的 REAP 可视为 HOPE 的特例。

**「实际影响」** 在评测覆盖的 10%–50% 裁剪率下，HOPE 可让开发者无需重新训练便永久删除 MoE 专家，降低推理时必须常驻的专家参数内存，并可继续配合量化使用；在 50% 裁剪时，其代理式编码任务表现较次优方法最高提升 6.1%。但现有材料未给出各模型的确切内存节省比例及质量损失，部署收益仍需逐模型验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2609.18916">[2609.18916] Higher-order pruning of experts in mixture-of ...</a></li>
<li><a href="https://arxiv.org/abs/2510.13999">[2510.13999] REAP the Experts: Why Pruning Prevails for One ... REAP the Experts: Why Pruning Prevails for One-Shot MoE ... REAP the Experts: Why Pruning Prevails for One-Shot MoE ... Router-weighted Expert Activation Pruning (REAP) - GitHub REAP E : WHY PRUNING PREVAILS FOR NE-S M E COMPRESSION Router-weighted Expert Pruning (REAP) - emergentmind.com REAP: - Cerebras</a></li>
<li><a href="https://github.com/awslabs/HOPE">GitHub - awslabs/HOPE</a></li>
<li><a href="https://todayforai.com/en/items/art-dc5121c2-115">Amazon&#x27;s HOPE Higher-Order Expert Pruning Cuts MoE Memory ...</a></li>

</ul>
</details>

**标签**: `#mixture-of-experts`, `#expert pruning`, `#LLM inference`, `#model compression`, `#higher-order pruning`

---

<a id="item-tech-news-13"></a>
### [提示 Claude Fable 5.2：明确告诉模型代码库归你所有](https://simonwillison.net/2026/Nov/10/prompting-claude-fable-52/) ⭐️ 6.0/10

Anthropic 的文档建议在提示中明确说明“这个代码库归你所有”，以促使 Claude Fable 5.2 在工作中主动改进代码结构。在小型编码任务测试中，使用这句话时，模型约有半数尝试会合并重复代码；未说明归属时则不到十分之一。该结果仅来自 Anthropic 的小型任务测试，尚不能直接外推到更广泛的编程场景。

rss · Simon Willison · 11月10日 05:34

**标签**: `#Claude Fable 5.2`, `#prompt engineering`, `#coding agents`, `#code refactoring`

---

<a id="item-tech-news-14"></a>
### [用 Claude Code 定位神秘蜂鸣声](https://simonwillison.net/2026/Nov/9/mysterious-beeps/) ⭐️ 6.0/10

Simon Willison 使用 Claude Code 构建了 Beep Locator，通过两台 iPad、一部 iPhone、MacBook Pro 和 Surface Ultra 协同定位房间内间歇出现的蜂鸣声。Python 主服务器利用 WebSockets 连接浏览器监听器，各设备保存最近 60 秒音频，并通过快速傅里叶变换和高通滤波检测蜂鸣；发现目标后，服务器让往返延迟最低的设备播放短 chirp，再收集从蜂鸣前约 0.6 秒到 chirp 后约 0.8 秒的音频片段以完成对齐。设备自动互发声音的定位效果不佳，因此项目加入了可手动拖动设备图标的 Rough mode，并提供拍手测试、逐设备回放和人工确认功能，界面记录的目标频率为 3345 Hz。系统最终将声源定位到约 40 厘米范围内，帮助 Willison 找到一只需要更换电池的老式一氧化碳探测器；项目最初是在 iPhone 上的 Claude Code Cloud 中以 Opus 5.5 Extra thinking 模式从空 GitHub 仓库开始构建的。

rss · Simon Willison · 11月9日 23:57

**「声学测距技术基础」** Beep Locator 的基础是 Chunyi Peng 等人于 2007 年提出的 BeepBeep 系统，它使用现成设备上的扬声器、麦克风和设备间通信进行无预置基础设施的声学测距与定位。该方案结合双向感知、信号自记录和采样计数来提高定位精度，Willison 的实现则用蜂鸣检测、同步 chirp 和多设备音频片段计算将其适配到浏览器环境中。

**「实际影响」** 对需要查找间歇性异响来源的用户，开源的 Beep Locator 允许手机、平板和笔记本作为分布式麦克风，在作者的实测中把声源定位到约 40 厘米内并据此找到了老旧的一氧化碳探测器。其更广泛意义是为开发者提供了一个 Claude Code 辅助构建、采用 Python、WebSocket 与 Web Audio 的多设备声学定位实例，但该项目仍是个人原型，手工粗略校准和实际房间声学条件限制了它作为通用定位方案的适用性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/simonw/beep-locator/compare">Compare · simonw/beep-locator · GitHub</a></li>
<li><a href="https://agihunt.info/en/p/1a1c2df25d43f876590321e3ed0">Simon Willison builds a Beep Locator with Claude… · AGI Hunt</a></li>
<li><a href="https://feeds.simonwillison.net/2026/Nov/9/mysterious-beeps/">Locating the source of a mysterious beep with Claude</a></li>

</ul>
</details>

**标签**: `#Claude Code`, `#AI-assisted development`, `#sound localization`, `#multi-device audio`, `#web applications`

---

<a id="item-tech-news-15"></a>
### [NVIDIA 发布日本金融合成人格数据集](https://huggingface.co/blog/nvidia/nemotron-personas-finance-japan) ⭐️ 6.0/10

NVIDIA 与 Elith 发布了面向日本金融场景的开源合成人格数据集 Nemotron-Personas-Finance-Japan，这是 Nemotron-Personas-Japan 的金融领域扩展，目标是依据日本官方统计、家庭财务和金融素养数据构建金融 AI 测试与训练环境。该数据集包含 100 万条记录，每条记录提供 9 个人格，总计 900 万人格；每条记录含 50 个字段，整体约 15 亿个令牌，其中人格文本约 7.5 亿个，并覆盖约 95 万个姓名和 1600 多个职业类别。生成流程使用 NeMo Data Designer、概率图模型框架 NeMo SDG-PGMs 和日文生成模型 gemma-4-31B-it，以官方人口与劳动力统计及公开调查数据约束人口、家庭财务和资产分布。所有人格均为合成内容，不对应真实个人，姓名遵循日本命名模式，从而让银行、保险公司及初创团队无需使用真实客户数据即可开展对话代理、客户模拟、销售评估、公平性测试和红队测试。数据集采用 CC BY 4.0 许可证，可用于商业及非商业用途，并可接入 NeMo User Sim；发布方称其为首个达到百万记录规模、结合日本官方统计与家庭财务及金融素养数据的开放人格数据集，但发布材料未提供下游模型基准或隐私风险实测结果，实际效果仍需进一步验证。

rss · Hugging Face Blog · 11月9日 15:05

**「背景」** 合成人物数据集...

**「实际影响」** 日本银行、保险公司及相关技术团队可利用 900 万个合成人物、50 个字段和约 15 亿词元，在不接触真实客户数据的情况下开发与评测金融智能体、客户模拟和偏差测试；CC BY 4.0 许可允许商业使用，有助于降低数据获取、隐私与合规门槛。由于发布材料尚未提供充分的生成方法、偏差审计或真实业务效果验证，该数据集适合作为开发与仿真资源，但不能单独证明生产系统的安全性或业务表现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.aitoolsoasis.com/en/news/nvidia-launches-nemotron-personas-finance-japan-9m-1794243726212">NVIDIA Nemotron-Personas-Finance-Japan: 9M Synthetic Personas</a></li>
<li><a href="https://explainx.ai/blog/nvidia-nemotron-personas-finance-japan-synthetic-dataset-2026">Nemotron Finance Japan Dataset: 9M Personas (Nov 2026 ...</a></li>
<li><a href="https://www.aiwins.news/story/nvidia-shares-synthetic-japan-finance-dataset-for-more-localized-ai-dc555c">NVIDIA Shares Synthetic Japan Finance Dataset for More ...</a></li>
<li><a href="https://www.aitoolsoasis.com/en/news/nvidia-launches-nemotron-personas-finance-japan-9m-1794243726212">NVIDIA Nemotron-Personas-Finance-Japan: 9M Synthetic Personas</a></li>

</ul>
</details>

**标签**: `#synthetic-data`, `#financial-AI`, `#persona-datasets`, `#privacy`, `#Japan`

---

<a id="item-tech-news-16"></a>
### [Control Room：集中追踪并停止模型工作负载](https://openai.com/index/control-room) ⭐️ 6.0/10

OpenAI 发布了集中式系统 Control Room，用于管理其研究基础设施中的模型工作负载。该系统能够统一追踪这些工作负载，并在出现安全或安保问题时快速停止相关运行。所给公告仅概述了这两项核心能力，没有披露工作负载的具体类型、系统架构、部署范围、停止时延或实际效果，因此目前无法判断其技术成熟度或更广泛的行业影响。

rss · OpenAI News · 11月9日 13:00

**「背景」** 模型工作负载泛指在研究基础设施上运行的模型相关计算任务，但所给材料没有界定 Control Room 覆盖哪些任务。集中式工作负载管理的意义在于将运行状态追踪与停止能力置于统一入口，从而支持在风险出现时快速处置。

**「影响」** 对 OpenAI 的研究基础设施运营方而言，Control Room 提供了一个集中追踪并停止问题工作负载的机制，但其覆盖规模和实际响应速度尚无公开证据支持。

**标签**: `#AI infrastructure`, `#AI safety`, `#workload management`, `#security`

---

<a id="item-tech-news-17"></a>
### [新 AI 模型模拟从沙粒到蛋白质的物质行为](https://news.google.com/rss/articles/CBMiXEFVX3lxTFBTSjNqRzBJc3lxdE1QQmJwUFdjemp6UGFWQ0d4T1V0VkpLXzBJWVVUQXhQQjJMZzVIZVB2MGs1VWk0Wm1xQW5ZSmhWZnNLWFJ3V0Q3VGw4RHpDSHNl?oc=5) ⭐️ 6.0/10

...

google\_news · EurekAlert\! · 11月9日 18:58

**「背景」** 传统科学模拟通常针对沙粒等颗粒材料、蛋白质折叠等不同物理系统分别建立模型，而 WorldParticle 被报道为一种尝试用统一人工智能架构跨系统模拟物质行为的“世界模型”。这一方向属于 AI for science，目标是让模型从数据中学习系统状态随时间的演化规律，再用于预测和模拟；不过现有材料尚未给出其具体网络结构、训练数据、基准测试或论文细节。

**「潜在影响」** 该模型若能准确模拟从沙粒材料到蛋白质的物质行为，相关研究团队或可减少为不同体系分别开发模拟工具的工作；但目前仅有标题信息，缺少基准、误差和适用条件，尚无法确认其实际收益或对现有方法的替代程度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.brightsurf.com/news/LRDYEKY8/new-ai-model-simulates-behavior-of-substances-from-sand-to-proteins.html">New AI model simulates behavior of substances, from sand to ...</a></li>

</ul>
</details>

**标签**: `#AI for science`, `#scientific machine learning`, `#simulation`, `#materials modeling`, `#protein modeling`

---

<a id="item-tech-news-18"></a>
### [HUMAIN 与 Infra 达成 6.667 亿美元 AI 基础设施融资协议](https://news.google.com/rss/articles/CBMi4gFBVV95cUxNcmdtc3hpSzRWa2JtTlJ6WTRZbFp4N1ctOFFoNzNIM3J1TEZ1Qk1aZFQ1Q2htLU1hSmd4dmxiakdGQjI1ejlJVjVxMUZtdG5UWFdLU1N2QjlMN1JMMDJ3R21DalU5bjQ1VVJCMGt6U2EzTHpHWnQxV1BVbm9FckY5cXFHUUZ6Q09tX3JuWlVfaFlPVXdzcUFVV1ppZUtxcVppRlNxUXdaTTIweHJvMDVMVnFaTkJ6cGxJWXBpUW9vZFVqWHl2S2tqalBNXzN1Vk01ajFhTWUzR2tuVDN6cmFxNlhB?oc=5) ⭐️ 6.0/10

据《福布斯中东》报道，HUMAIN 与 Infra 已就沙特人工智能基础设施融资达成协议，金额为 6.667 亿美元。该交易若完成，将为沙特 AI 基础设施建设提供大额资金支持。现有内容仅提供标题，未披露资金来源、股权或债务结构、算力规模、具体技术方案及交付时间。由于关键条款和实施细节尚不明确，目前无法进一步判断其对沙特 AI 算力供给或相关产业生态的具体影响。

google\_news · Forbes Middle East · 11月9日 15:39

**「融资背景」** HUMAIN 是由沙特公共投资基金（PIF）支持的 AI 基础设施项目方，沙特国家基础设施基金（NIF）在此次合作中承担融资角色。双方更广的融资框架据报道最高达 12 亿美元，采用非约束性融资条款，覆盖 AI 与数字基础设施，并涉及 HUMAIN 规划的最高 250MW 超大规模 AI 数据中心容量；现有来源尚未说明新闻标题中的 6.667 亿美元与该框架之间的具体拆分或关系。

**「影响」** 这将扩大 HUMAIN 以 GPU 集群提供 AI 训练与推理服务的能力，并面向沙特本地、区域及全球客户形成新的数据中心算力供给。外部报道将整体安排描述为最高 12 亿美元、规划 250MW 数据中心容量，但当前信息未说明 6.667 亿美元融资的具体投放节奏，因此实际可用算力仍取决于后续建设与部署。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.linkedin.com/posts/aashishgidwani_humain-infra-announce-12bln-ai-projects-activity-7421417792987578368-sVoe">Saudi Arabia AI Infrastructure Fund Reaches... | LinkedIn</a></li>
<li><a href="https://www.bernama.com/en/news.php?id=2516766">Infra , HUMAIN Seal US$1.2 Bln Saudi AI Infrastructure Deal</a></li>
<li><a href="https://meatechwatch.com/2026/01/25/pif-backed-humain-secures-up-to-1-2bn-to-expand-ai-infrastructure/">PIF-backed Humain secures up to $1.2bn to expand AI infrastructure ...</a></li>
<li><a href="https://www.linkedin.com/posts/datapro-plus_saudi-infra-fund-humain-agree-up-to-12-activity-7420458498750148609-oqTq">Saudi Arabia&#x27;s Humain Secures $1.2B for AI Data Center ... | LinkedIn</a></li>
<li><a href="https://www.bernama.com/en/news.php?id=2516766">Infra , HUMAIN Seal US$1.2 Bln Saudi AI Infrastructure Deal</a></li>
<li><a href="https://alarabiantimes.com/saudi-arabias-12-billion-bet-on-ai-infra-humain-seal-major-deal-at-davos-2026">Saudi Arabia&#x27;s $1.2 Billion Bet on AI : Infra &amp; Humain Seal Major Deal.....</a></li>

</ul>
</details>

**标签**: `#AI infrastructure`, `#startup financing`, `#Saudi Arabia`, `#compute infrastructure`

---