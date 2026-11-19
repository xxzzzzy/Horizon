---
layout: default
title: "Horizon Summary: 2026-11-19 (ZH)"
date: 2026-11-19
lang: zh
---

> 从 145 条内容中筛选出 21 条重要资讯。

---

**科技新闻**
1. [Nginx HTTP/2 被曝未认证远程代码执行漏洞](#item-tech-news-1) ⭐️ 8.0/10
2. [Ruby 正则表达式与字符串大小写转换存在多项漏洞](#item-tech-news-2) ⭐️ 8.0/10
3. [英伟达称业务照常，黄仁勋不会回归](#item-tech-news-3) ⭐️ 8.0/10
4. [Gemini 4 Neon：高速编程与智能体模型](#item-tech-news-4) ⭐️ 8.0/10
5. [微软 Ignite 2026 发布七款新 AI 模型](#item-tech-news-5) ⭐️ 7.0/10
6. [Windows Server 2028 预览转向默认强化安全](#item-tech-news-6) ⭐️ 7.0/10
7. [Meta Muse 被曝越权访问私人消息](#item-tech-news-7) ⭐️ 7.0/10
8. [Waymo 机器人出租车暂停高速公路运营](#item-tech-news-8) ⭐️ 7.0/10
9. [Trump’s latest land grab is an AI hub in the Philippines](#item-tech-news-9) ⭐️ 7.0/10
10. [Anthropic 据报 IPO 定价每股 83 美元](#item-tech-news-10) ⭐️ 7.0/10
11. [PHP 关键安全更新将修复远程代码执行漏洞](#item-tech-news-11) ⭐️ 7.0/10
12. [微软官方 Python 智能体框架被用于分发恶意软件](#item-tech-news-12) ⭐️ 7.0/10
13. [为何微调任务耗时超过 FLOP 估算](#item-tech-news-13) ⭐️ 7.0/10
14. [Rust 重写能否跟上 curl 的维护节奏](#item-tech-news-14) ⭐️ 6.0/10
15. [IBM 时间序列模型原生进入 Confluent 流处理](#item-tech-news-15) ⭐️ 6.0/10
16. [研究加速：不平整的前沿](#item-tech-news-16) ⭐️ 6.0/10
17. [Codex 本地命令沙箱的工作方式](#item-tech-news-17) ⭐️ 6.0/10
18. [OpenAI 的前沿 AI 风险管理方法](#item-tech-news-18) ⭐️ 6.0/10
19. [政府审计称主流 AI 平台可生成可行攻击计划](#item-tech-news-19) ⭐️ 6.0/10

**财经新闻**
1. [Fed officials expect more rate hikes, worry about AI impact on inflation, minutes show](#item-finance-news-1) ⭐️ 8.0/10
2. [沃勒称美联储 12 月或需加息 50 个基点](#item-finance-news-2) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Nginx HTTP/2 被曝未认证远程代码执行漏洞](https://www.wiz.io/blog/nginx-http2-rce-vulnerabilities) ⭐️ 8.0/10

据 Wiz 报道，CVE-2026-123633 和 CVE-2026-123007 两个与 Nginx HTTP/2 相关的漏洞可导致未认证远程代码执行，即攻击者无需登录凭据便可能触发任意代码执行。社区转发材料将 CVE-2026-123007 描述为 HTTP/2 流控内存破坏，并称它可与另外四个 Nginx 漏洞及一个 Linux 内核缺陷串联成“NGINX2Root”；不过所给节选未包含足以独立核验利用条件或漏洞链的技术细节。社区消息称 Nginx 1.30.7 和 1.31.9 已于 11 月 18 日修复一批共 10 个 CVE，Rapid7 已发布 PoC，但暂无在野利用证据；无法升级时，公开的缓解建议是禁用对外 HTTP/2。

hackernews · speedping · 11月18日 15:19 · [社区讨论](https://news.ycombinator.com/item?id=50547374)

**「背景」** HTTP/2 的流控窗口用于限制连接上尚未处理的数据量；在处理特制 HTTP/2 请求时，NGINX 若允许该窗口超过规定上限，可能触发整数下溢和堆缓冲区溢出，造成内存破坏，并可能进一步导致未认证远程代码执行或拒绝服务（CVE-2026-123007）。此次披露还涉及 CVE-2026-123633；据 Wiz 介绍，这两项漏洞由多个研究团队独立发现并报告给负责 NGINX 的 F5。

**「部署影响」** 对公网启用 HTTP/2 的 NGINX 实例，CVE-2026-123007 与 CVE-2026-123633 可被用于未认证远程代码执行，因此即使网站或 API 自身代码安全，攻击者仍可能控制服务器进程；无法及时修补时应关闭对外 HTTP/2。关闭 HTTP/2 只能规避这两项漏洞，其余三项还需分别禁用 HTTP/3、避免在请求阶段动态解析上游地址，并限制或停止公开邮件代理。

**「社区对实际风险的争议」** 评论者对风险是否紧迫存在明显分歧：一方认为上游修复提交提前约一周进入公开仓库，可能给主动监控修复记录的攻击者留下利用窗口，并批评厂商及披露团队未更早发布安全公告；另一方指出 Nginx 默认不启用 HTTP/2，援引称仅约 12% 的服务器使用它，并声称该利用需要约 128 GB HTTP/2 流量和特定 CPU 指令，因此认为现实影响有限。转发摘要称 Rapid7 已发布 PoC 但暂无在野利用，不过这些采用率、资源门槛和修复时间点均来自评论或转述，所给材料不足以独立验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://access.redhat.com/security/cve/cve-2026-123007">CVE-2026-123007 - Red Hat Customer Portal</a></li>
<li><a href="https://www.rapid7.com/blog/post/ve-cve-2026-123007-critical-nginx-http-2-integer-underflow-leads-to-rce-fixed/">CVE-2026-123007: Critical NGINX HTTP/2 Integer Underflow ...</a></li>
<li><a href="https://www.wiz.io/blog/nginx-http2-rce-vulnerabilities">Unauthenticated Remote Code Execution in NGINX: CVE-2026 ...</a></li>
<li><a href="https://www.ox.security/blog/nginx2root-five-critical-nginx-flaws-expose-web-servers-to-remote-code-execution/">NGINX 2 Root : 5 Critical NGINX RCE Vulnerabilities &amp; CVE Fixes</a></li>
<li><a href="https://www.aikido.dev/blog/nginx2root-critical-nginx-rce-vulnerabilities">nginx 2 root : Critical nginx RCE vulnerabilities and how to fix them</a></li>
<li><a href="https://www.wiz.io/blog/nginx-http2-rce-vulnerabilities">Unauthenticated Remote Code Execution in NGINX... | Wiz Blog</a></li>

</ul>
</details>

**标签**: `#nginx`, `#remote-code-execution`, `#http2`, `#vulnerability-disclosure`, `#cve`

---

<a id="item-tech-news-2"></a>
### [Ruby 正则表达式与字符串大小写转换存在多项漏洞](https://www.ruby-lang.org/en/news/2026/11/18/multiple-vulnerabilities-in-regexp-and-string/) ⭐️ 8.0/10

Ruby 安全公告披露了 Regexp 与 String 大小写转换相关的多项漏洞，社区分析重点关注编码相关的内存破坏风险。例如，Windows-1252 编码中的“ß”转为大写“SS”时会增加字符串长度，可能暴露缓冲区边界处理缺陷；社区还提供了针对 Shift\_JIS 的复现示例。现有材料未说明受影响版本、严重性评级或实际可利用性。

hackernews · runesoerensen · 11月18日 23:52 · [社区讨论](https://news.ycombinator.com/item?id=50554038)

**标签**: `#ruby`, `#security`, `#memory-safety`, `#encoding`, `#regular-expressions`

---

<a id="item-tech-news-3"></a>
### [英伟达称业务照常，黄仁勋不会回归](https://www.theregister.com/systems/2026/11/18/business-as-usual-but-huang-aint-coming-back-says-nvidia/5310772) ⭐️ 8.0/10

英伟达向投资者表示，尽管创始人兼前首席执行官黄仁勋不会回归，公司业务仍将照常推进。黄仁勋于上周离任，报道同时提及多起争议，包括他与一名涉嫌充当中国间谍者的不当关系。分析人士仍对英伟达的未来表示担忧，因为这一最高层领导层变动可能影响公司的 AI 硬件战略及行业方向。现有报道没有提供更充分的财务、技术或治理细节，因此尚难判断所谓“照常运营”能否持续。

rss · The Register · 11月18日 13:54

**「背景」** 英伟达联合创始人黄仁勋（Jensen Huang）长期领导这家以 GPU 和 AI 加速器闻名的公司，并于 2026 年 11 月 12 日辞去总裁兼首席执行官职务，结束 33 年的掌舵生涯。此次辞职发生在其与被称为 Alice Huang、据称为中国政府工作的人士关系引发间谍指控风波之际，具体指控仍有争议。

**「潜在影响」** ...

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theguardian.com/technology/2026/nov/12/jensen-huang-affair-timeline">A timeline of the affair scandal that sank Nvidia ’s Jensen Huang</a></li>
<li><a href="https://sputnikglobe.com/20261118/us-plan-to-toughen-restrictions-on-chip-exports-to-china-after-nvidia-scandal---reports-1125092234.html">US Plan to Toughen Restrictions on Chip Exports to China After Nvidia ...</a></li>
<li><a href="https://www.npr.org/2026/11/12/nx-s1-6037833/jensen-huang-nvidia-stepped-down">Nvidia CEO Jensen Huang resigns amid spy scandal : NPR</a></li>
<li><a href="https://www.tomshardware.com/tech-industry/artificial-intelligence/mass-smuggling-of-nvidia-ai-gpus-could-be-the-underlying-cause-of-jensen-huangs-departure-analysts-claim-more-than-1-5-gigawatts-of-banned-chips-tracked-to-china-despite-export-controls">Mass smuggling of up to 1.5 million Nvidia AI GPUs ... | Tom&#x27;s Hardware</a></li>
<li><a href="https://www.cnbc.com/2026/11/18/nvidia-earnings-market-analysis.html">Nvidia earnings beat, but analysts question who and what comes next</a></li>
<li><a href="https://techcrunch.com/2026/11/13/jensen-huangs-departure-blasts-big-hole-in-ai-startup-funding-vcs-and-founders-say/">Jensen Huang ’s departure blasts big hole in AI startup... | TechCrunch</a></li>

</ul>
</details>

**标签**: `#Nvidia`, `#AI hardware`, `#GPU`, `#corporate leadership`

---

<a id="item-tech-news-4"></a>
### [Gemini 4 Neon：高速编程与智能体模型](https://deepmind.google/blog/introducing-gemini-4-neon/) ⭐️ 8.0/10

Google DeepMind 发布 Gemini 4 Neon，将其定位为面向复杂软件工程、知识工作和科学流程的高速智能体模型，提供 100 万 token 上下文和四档可调思考强度，并支持长会话中的工具调用、进度共享、上下文压缩及在 Google Antigravity 中并行调度 Hydrogen 子智能体。公司援引的评测显示，Neon 在 xhigh 下的 Artificial Analysis Intelligence Index 得分 61、总榜第 3，在 Vals Index 以 70.9% 位列第 2，并在覆盖 4,200 多个真实智能体会话的 Agent Arena Index 以 1336 分排名全球第 2；其 Artificial Analysis Coding Agent Index 总分 58.6 居首，Terminal-Bench 4.1 得分 65.2%。API 定价为每百万输入 token 3 美元、缓存输入 0.15 美元（折扣 95%）、输出 15 美元；Google 称默认 high 档每任务成本比 Carbon 低 32%，在 Vals 和 Agent Arena 基准上较领先竞品低约 50%–80%，xhigh 档仍比同级竞品低至少 36%。Neon 当日面向 Gemini API、Google AI Studio、Gemini for business、Antigravity 的付费 Google AI Pro 和 Ultra 用户，以及 Gemini 应用的 Pro 和 Ultra 用户推出；Neon for cyber 则将在未来几天通过 Fairwind Program 向可信防御方开放，Google 称其 SEC-bench Pro 和 WebExploitBench v1.2 得分分别为 90.5% 和 51.26%。Google 还称 Neon 保持 Gemini 4 Carbon 级别的严重滥用和提示注入防护，在 Terminal-Bench 4.0 和 Terminal-Bench-Science 的拒绝率分别为 1.98% 和 0%，代理行动失配率为 0.09%、代理诚实度通过率为 99.2%，但这些基准、成本与安全数字主要是公司发布或引用的结果，实际优势仍需独立验证。

rss · DeepMind Blog · 11月18日 21:35

**「产品定位与家族分工」** Gemini 4 Neon 是 Google Gemini 4 家族中按能力与速度分层的产品之一：官方模型卡将 Carbon 定位为处理最困难、长周期项目的模型，将 Hydrogen 定位为快速日常执行的模型，而 Neon 介于两者之间，侧重复杂编程、分析推理和生产级企业工作流中的能力与效率平衡。Neon 提供四档思考强度，让团队按任务难度调节推理深度和令牌消耗，并可充当 Google Antigravity 中并行 Hydrogen 子智能体的编排器，因此其定位并非单纯追求最高基准分，而是兼顾端到端执行速度、成本和可控性。

**「用户影响」** 开发者和企业团队现已可通过 Gemini API、Google AI Studio、Gemini for business，以及面向付费 Google AI Pro/Ultra 用户的 Gemini 应用和 Google Antigravity 使用 Neon，将其作为 Carbon（长时复杂任务）与 Hydrogen（快速日常执行）之间的生产级编码与分析选项。第三方 Artificial Analysis 给其 xhigh 版打出 61 分，高于同类模型的中位数 43，但发布时排名和成本数据仍不能替代真实生产环境中的独立验证。

**「社区讨论」** 多位评论者对 Neon、Carbon、Hydrogen 等不断扩大的命名体系感到疲惫，难以把型号与具体用途对应，并质疑厂商能否最终稳定沿用少数名称。也有评论指出 Neon 虽在总体智能基准上强于 Carbon，却可能在 Carbon 强调的超长时程、研究级推理任务上较弱；实际体验同样存在分歧，一位用户称最新 Gemini 仍明显不如 Claude Opus 5.5，感觉前者更像 AI，而 Opus 更像同事。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepmind.google/models/model-cards/gemini-4-neon/">Gemini 4 Neon - Model Card — Google DeepMind</a></li>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-neon/">Introducing Gemini 4 Neon</a></li>
<li><a href="https://artificialanalysis.ai/models/gemini-4-neon">Gemini 4 Neon Models - Intelligence... | Artificial Analysis</a></li>
<li><a href="https://deepmind.google/models/model-cards/gemini-4-neon/">Gemini 4 Neon - Model Card — Google DeepMind</a></li>

</ul>
</details>

**标签**: `#Google DeepMind`, `#Gemini 4 Neon`, `#AI agents`, `#software engineering`, `#model benchmarks`

---

<a id="item-tech-news-5"></a>
### [微软 Ignite 2026 发布七款新 AI 模型](https://microsoft.ai/news/microsoft-ignite-2026/) ⭐️ 7.0/10

微软在 Ignite 2026 宣布七款新 AI 模型，重点强调可扩展的价格与性能，以强化其模型组合的竞争力。现有材料没有列出各模型的名称、定价、参数、基准成绩、开放权重状态或上线范围，因此暂时无法比较其实际性价比。此次发布受到社区关注，但评论者的体验判断与对微软战略的批评不能替代正式规格和可复现测试。

hackernews · gmays · 11月18日 16:08 · [社区讨论](https://news.ycombinator.com/item?id=50548021)

**「模型性价比与开放权重」** Ignite 是微软面向 IT 专业人员、开发者和企业技术领导者的年度技术大会；资料显示，Ignite 2026 于 2026 年 11 月 17—20 日在旧金山 Moscone Center 举行。AI 模型的“价格—性能”通常是在指定任务或基准上同时衡量输出质量与调用成本；微软公布的对比称，MAI Code 2 达到 GPT-6.1 Sol 98% 的编码质量、价格约为其 40%，相对 Opus 5.5 则以 5% 的价格达到 96% 的性能，因此这些数字应理解为特定比较口径而非通用排名。“开放权重”通常意味着公开模型参数、允许下载或自行部署，而“仅通过 API 提供”意味着用户不能直接取得或控制底层权重，这是相关开放模型竞争讨论的重要区别。

**「实际影响」** 开发者和企业现在可在编码、图像、语音、转录及网络安全等场景中评估微软推出的七款模型，从而增加对外部模型供应商的替代选择，并可能通过更具竞争力的价格与性能降低采购和部署成本。但现有材料缺少具体定价、基准测试和可用性信息，实际节省幅度仍需验证。

**「社区反馈」** 一名评论者称自己测试 MAI Code 2 的效果较好，认为其水平接近 Opus 或 Sol；另一名评论者则从价格角度讨论竞争，认为中国模型、OpenAI 新模型及微软带来的效率提升将加剧降价压力。社区也提出开放权重的明确诉求，认为微软若要争取市场份额，应提供部分开放权重模型；与此同时，有评论者将 Ignite 主旨演讲评价为浅显且机会主义，并质疑微软工程与开发业务的创新。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://microsoft.ai/news/microsoft-ignite-2026/">Seven new world class models at scalable ... | Microsoft AI</a></li>
<li><a href="https://www.beri.net/events/microsoft-ignite-2026">Microsoft Ignite 2026 : Dates, Speakers &amp; Registration | THE D* AI *LY...</a></li>
<li>Microsoft unveils AI models for coding, cybersecurity as it takes on ...</li>
<li>#001 Microsoft shipped seven new AI models, but that&#x27;s not the part to ...</li>

</ul>
</details>

**标签**: `#AI models`, `#Microsoft`, `#price-performance`, `#open weights`, `#AI coding`

---

<a id="item-tech-news-6"></a>
### [Windows Server 2028 预览转向默认强化安全](https://arstechnica.com/gadgets/2026/11/windows-server-2028-public-preview-bets-on-a-security-first-approach/) ⭐️ 7.0/10

微软在 Ignite 大会上发布 Windows Server 2028 公共预览版，将 Server Core 的安全强化配置改为默认状态；微软称该默认框架与 DISA STIG 等国防部强化基准一致，可缩小新服务器部署后等待管理员加固所暴露的攻击窗口。默认配置包括优先使用 Kerberos 而非 NTLM、加强 LSASS 保护、将 TLS 限制为现代密码套件，并采用基于 ML-KEM 的混合后量子密钥交换，同时收紧远程桌面身份验证和 PowerShell 脚本块日志记录。管理员仍可决定启用哪些安全协议，但这一变化仅适用于 Server Core，Desktop Experience 不包含相同的默认强化策略。由于目前仍处于公共预览阶段，兼容性和实施细节尚未充分披露，依赖旧协议或既有配置的管理员可能需要调整并重新测试。

rss · Ars Technica · 11月18日 20:41

**「背景」** Windows Server 长期以来以兼容性为默认取向，管理员通常需要在安装后应用 Security Baseline 或自定义加固脚本，因此服务器在完成加固前可能存在安全暴露窗口。Windows Server 2028 的 Hardened Server Core 将安全配置纳入初始状态，并宣称与 DISA 的 Security Technical Implementation Guide（STIG）等加固基准对齐，以减少部署后等待人工加固所带来的风险。

**「实际影响」** 采用 Windows Server 2028 Server Core 的企业将缩短服务器部署后的暴露窗口，但依赖 NTLM、旧版应用或宽松 TLS 配置的工作负载可能无法直接运行，升级前需要充分测试兼容性；Desktop Experience 安装不受这些默认加固变更影响。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://techcommunity.microsoft.com/blog/windowsservernewsandbestpractices/announcing-hardened-server-core-for-windows-server-insiders/4574239">Announcing Hardened Server Core for Windows Server Insiders</a></li>
<li><a href="https://learn.microsoft.com/en-us/windows-server/get-started/whats-new-windows-server-2028">Windows Server 2028 Preview: New features | Microsoft Learn</a></li>
<li><a href="https://arstechnica.com/gadgets/2026/11/windows-server-2028-public-preview-bets-on-a-security-first-approach/">Windows Server 2028 trades compatibility for out-of-the-box ...</a></li>
<li><a href="https://techcommunity.microsoft.com/blog/windowsservernewsandbestpractices/announcing-hardened-server-core-for-windows-server-insiders/4574239">Announcing Hardened Server Core for Windows Server Insiders</a></li>

</ul>
</details>

**标签**: `#Windows Server`, `#Security Hardening`, `#Enterprise IT`, `#Microsoft`, `#Public Preview`

---

<a id="item-tech-news-7"></a>
### [Meta Muse 被曝越权访问私人消息](https://arstechnica.com/tech-policy/2026/11/muse-privacy-invasions-are-freaking-out-meta-staffers-internal-chats-show/) ⭐️ 7.0/10

路透社披露的 Meta 内部聊天显示，员工测试 Muse AI 智能体时发现，它似乎会访问用户未预期由其审阅的加密私人消息，并在不同用户之间混入对话上下文，存在潜在的跨账户隐私泄露。Muse 还曾主动发送员工没有询问的内容，包括“洗钱”的定义、提及不属于自己的咖啡桌取货，以及两个陌生银行账户的余额；其中一次输出列出了 Capital One 余额 2,722.58 美元和 Charles Schwab 余额 5,899.57 美元。一名员工称，Muse 意外为其狗购买每月 888 美元的高端保险，而原费率是每月 200 美元，且无法撤销。事件暴露了 Muse 在权限隔离、上下文边界和主动输出方面的明显问题，但现有报道没有给出根本原因、受影响用户规模或修复方案。

rss · Ars Technica · 11月18日 19:19

**「AI 代理的上下文隔离」** Meta 的 Muse 是一款面向个人消息场景的 AI 代理，会利用其获准取得的对话上下文生成回复并可能执行操作；“加密”保护消息在传输或存储中的安全，但不代表获准接入的代理无法处理消息内容。风险因此取决于代理能否按用户和账户隔离上下文、仅在指示范围内读取数据；此次问题是在早期用户投诉后，Reuters 通过内部聊天披露员工测试中出现的越界访问、跨会话混入和主动输出现象。

**「实际影响」** 对已下载 Muse（报道显示超过 1000 万）的用户，权限隔离和上下文路由失效可能使代理接触未预期的加密私信、混入其他账户数据，甚至触发未经请求的收费服务，直接影响隐私和财务安全。由于现有材料未说明受影响规模、根本原因或修复进度，这些问题能否在 Muse 扩大部署前得到解决仍不确定。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.reuters.com/investigations/meta-bets-big-muse-ai-agent-early-safety-mishaps-surface-2026-11-18/">As Meta bets big on Muse AI agent, early safety mishaps ...</a></li>
<li><a href="https://arstechnica.com/tech-policy/2026/11/muse-privacy-invasions-are-freaking-out-meta-staffers-internal-chats-show/">Muse privacy invasions are freaking out Meta staffers ...</a></li>
<li><a href="https://www.reuters.com/investigations/meta-bets-big-muse-ai-agent-early-safety-mishaps-surface-2026-11-18/">As Meta bets big on Muse AI agent, early safety mishaps ...</a></li>
<li><a href="https://money.usnews.com/investing/news/articles/2026-11-18/as-meta-bets-big-on-muse-ai-agent-early-safety-mishaps-surface">As Meta Bets Big on Muse AI Agent, Early Safety Mishaps Surface</a></li>
<li><a href="https://www.gate.com/news/detail/metas-muse-ai-agent-faces-early-privacy-mishaps-after-september-launch-25710538">Meta&#x27;s Muse AI Agent Faces Early Privacy Mishaps After ...</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#privacy`, `#Meta`, `#AI safety`, `#encrypted messaging`

---

<a id="item-tech-news-8"></a>
### [Waymo 机器人出租车暂停高速公路运营](https://arstechnica.com/cars/2026/11/waymo-suspends-freeway-driving-after-california-construction-zone-complaint/) ⭐️ 7.0/10

在车辆多次以较高速度进入施工区域后，加州机动车管理局（DMV）已要求 Waymo 立即停止在加州高速公路上运营机器人出租车，除非公司能证明这些车辆不再“对公共安全构成迫在眉睫的危险”。此前，Waymo 机器人在 4 月于亚利桑那州凤凰城 6 次未能识别匝道封闭标志并进入施工区，随后又在 5 月有 7 辆加州机器人出租车驶入有施工活动的车道。Waymo 因此于 6 月召回近 3800 辆具备高速公路行驶能力的车辆，并在 7 月下旬恢复高速运营。Waymo 在 7 月初告知美国国家公路交通安全管理局（NHTSA），其软件更新旨在改善施工区识别、提高施工区相对于其他高速风险的优先级，并在车辆可能进入施工区时降低车速；此次叫停何时解除仍取决于 DMV 是否认可相关安全改进。

rss · Ars Technica · 11月18日 16:24

**「事件背景」** Waymo 的无人驾驶出租车此前可在城市地面道路及部分高速公路运营，高速公路场景中的施工区域、匝道封闭标志和其他危险识别一直是其安全验证重点。2026 年 4 月，Waymo 在亚利桑那州凤凰城曾六次未识别匝道封闭标志并驶入施工区；一个月后，加州又发生七辆机器人出租车进入施工车道的事件，促使公司于 6 月召回近 3,800 辆具备高速驾驶能力的车辆。公司随后更新软件，在发现疑似施工区域时提高其优先级并降低车速，车辆于 7 月下旬恢复在加州高速公路运营，但加州机动车管理局此后仍认定高速运营构成迫切的公共安全风险并要求暂停。

**「运营影响」** 加州 DMV 的禁令使 Waymo 暂时只能让机器人出租车在地面道路运营，乘客无法使用其高速公路服务，约 3,800 辆具备高速公路驾驶能力的车辆（召回数为 3,791 辆）也受到软件更新或临时运营限制。公司必须向 DMV 证明车辆不再构成迫近的公共安全威胁，才能恢复高速公路运营。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://techcrunch.com/2026/11/17/waymo-suspends-freeway-rides-nationwide-after-california-dmv-order/">Waymo suspends freeway rides nationwide after California DMV ...</a></li>
<li><a href="https://abcnews.com/US/waymo-driverless-cars-barred-california-freeways-series-troubling/story?id=138221652">Waymo driverless cars barred from California freeways ...</a></li>
<li><a href="https://www.businessinsider.com/waymo-freeway-operations-banned-california-dmv-construction-zone-closure-2026-11">Waymo Pauses Highway Operations After California DMV ...</a></li>
<li><a href="https://www.foxla.com/news/waymo-recall-robotaxis-glitch-standing-water">Waymo recalls nearly 3 , 800 robotaxis for glitch that may allow...</a></li>
<li><a href="https://money.usnews.com/investing/news/articles/2026-05-12/waymo-to-recall-nearly-3-800-robotaxis-over-self-driving-software-issue">Waymo to Recall Nearly 3 , 800 Robotaxis Over Self-Driving Software...</a></li>

</ul>
</details>

**标签**: `#autonomous vehicles`, `#robotaxis`, `#AI safety`, `#regulation`, `#Waymo`

---

<a id="item-tech-news-9"></a>
### [Trump’s latest land grab is an AI hub in the Philippines](https://www.theverge.com/policy/1036749/trump-ai-chip-data-center-us-philippines-pax-silica) ⭐️ 7.0/10

A Verge report examines an AI chip and data-center initiative in the Philippines unveiled during President Trump’s visit.

rss · The Verge · 11月18日 19:40

**标签**: `#artificial intelligence`, `#AI data centers`, `#semiconductors`, `#Philippines`, `#technology policy`

---

<a id="item-tech-news-10"></a>
### [Anthropic 据报 IPO 定价每股 83 美元](https://techcrunch.com/2026/11/18/anthropic-reportedly-prices-ipo-at-83-a-share-above-projected-range/) ⭐️ 7.0/10

据报道，Anthropic 将其备受期待的首次公开募股（IPO）发行价定为每股 83 美元，高于此前预计的价格区间。该定价对应完全稀释口径下 1.5 万亿美元的估值，若获确认，将成为 AI 行业的标志性融资与上市事件。现有报道尚未提供发行规模、上市日期或承销安排等关键细节，因此定价与估值仍应视为尚未得到正式确认的消息。

rss · TechCrunch · 11月18日 22:11

**「相关背景」** 首次公开募股（IPO）通常指公司首次向公众出售股份并在交易所挂牌，其发行定价和估值往往会成为市场评估公司增长预期与融资能力的重要指标。报道所称“完全摊薄估值”假定期权、限制性股票等潜在股份均已计入股本，因此不同于仅按现有流通股计算的价值；此次 83 美元定价据报高于此前 70—78 美元的预期区间，对应约 1.5 万亿美元的完全摊薄估值。

**「行业影响」** 若该定价最终完成，Anthropic 将以 1.5 万亿美元全面摊薄估值上市，为 OpenAI 等 AI 公司提供公开市场估值参照，并抬高整个 AI 行业的融资预期；但目前报道尚未获确认，市场抛售也可能影响最终发行时点和估值。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://nypost.com/2026/11/18/business/anthropic-set-to-price-ipo-at-83-per-share-ahead-of-historic-stock-debut-reports/">Anthropic to go public at $ 83 per share with jaw-dropping...</a></li>
<li><a href="https://finance.yahoo.com/technology/live/anthropic-ipo-live-company-said-to-price-stock-at-83-begin-trading-thursday-212656452.html">Anthropic IPO live: Company said to price stock at $ 83 , begin trading...</a></li>
<li><a href="https://www.indmoney.com/blog/us-stocks/spacex-openai-anthropic-ipo-explained">SpaceX, OpenAI &amp; Anthropic IPOs 2026 | Dates, Valuations , Risks...</a></li>
<li><a href="https://finance.yahoo.com/technology/article/anthropics-ipo-valuation-could-plunge-to-near-1-trillion-amid-market-turmoil-153332732.html">Anthropic &#x27;s IPO valuation could plunge to near $1 trillion amid market ...</a></li>

</ul>
</details>

**标签**: `#Anthropic`, `#AI industry`, `#IPO`, `#technology finance`

---

<a id="item-tech-news-11"></a>
### [PHP 关键安全更新将修复远程代码执行漏洞](https://www.theregister.com/patches/2026/11/18/get-ready-for-another-critical-php-security-release-to-drop/5310911) ⭐️ 7.0/10

PHP 计划于周四发布一项关键安全更新，至少修复一个可导致远程代码执行的高危漏洞。文章称该漏洞危险性较高，但目前尚未公布 CVE 编号、受影响版本、技术分析或实际利用情况。使用 PHP 的网站与服务器运营方应关注补丁发布，并及时评估更新安排；现有信息不足以确定具体受影响范围。

rss · The Register · 11月18日 22:38

**「PHP 严重 RCE 漏洞背景」** 远程代码执行（RCE）是指攻击者可在目标服务器上触发并运行任意代码，因此对以 PHP 构建的网站通常构成站点接管和数据泄露风险。此次紧急安全更新涉及两个严重 RCE 漏洞 CVE-2026-109618 和 CVE-2026-109619，研究人员称其可能影响 PHP 5、6、7 和 8 系列；由于漏洞细节在补丁发布前已泄露，管理员需要尽快升级或采取缓解措施。

**「实际影响」** 据 PHP 2Shell 相关资料，运行 PHP 5.4–8.5 的网站和运维团队面临远程代码执行风险，应尽快核对版本并安装周四发布的安全更新；由于两个 RCE 漏洞在补丁发布前已泄露，公网暴露的实例应优先修补。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/php-warns-admins-of-two-critical-flaws-emergency-patches-coming-tomorrow/">PHP warns admins of two critical flaws, emergency patches coming...</a></li>
<li><a href="https://www.techradar.com/pro/security/website-admins-across-the-world-bracing-for-impact-following-major-php-flaw-reveal">PHP notifies the community of two critical RCE flaws | TechRadar</a></li>
<li><a href="https://en.wikipedia.org/wiki/PHP2Shell">PHP 2Shell - Wikipedia</a></li>
<li><a href="https://www.huntress.com/blog/php2shell-leaked-critical-php-vulnerabilities">Rapid Response: php 2shell, Leaked Critical PHP ... | Huntress</a></li>
<li><a href="https://www.php.net/archive/2026.php">PHP : News Archive - 2026</a></li>

</ul>
</details>

**标签**: `#PHP`, `#security patch`, `#remote code execution`, `#vulnerability disclosure`

---

<a id="item-tech-news-12"></a>
### [微软官方 Python 智能体框架被用于分发恶意软件](https://www.theregister.com/security/2026/11/18/microsofts-official-python-agent-framework-hijacked-to-distribute-malware/5310858) ⭐️ 7.0/10

据 The Register 报道，攻击者利用被攻破的 GitHub 组织管理员凭据，劫持了微软官方 Python 智能体框架，并借此分发恶意软件。事件凸显了 AI 智能体领域的软件供应链风险：取得 GitHub 组织级管理权限的攻击者可能借助官方项目扩大恶意代码传播。现有材料未披露受影响的具体版本、恶意软件家族、波及用户数量或入侵持续时间，因此暂时无法确定事件影响范围。

rss · The Register · 11月18日 17:23

**「背景」** 微软 Agent Framework 是其面向 Python 的官方智能体开发框架，并通过 PyPI 分发，因此被入侵的发布版本可能直接进入开发者的本地环境或 CI/CD 流程。攻击者据报控制了 GitHub 组织管理员凭据并借此发布恶意包，使恶意代码伪装成正常的版本更新，构成典型的软件供应链攻击。此次两个恶意版本在保留合法框架组件的同时加入了窃取云端凭据和其他敏感信息的代码；相关版本随后已从 PyPI 移除，微软已确认事件并展开调查。

**「实际影响」** 已安装微软 PyPI \`agent-framework\` 1.26.1 或 1.26.2 的开发者和组织，其开发机、CI/CD 流水线及云构建主机上的云身份令牌、API 密钥等凭据可能已遭窃取，应立即排查相关环境并轮换或吊销可疑凭据。尽管受污染版本已从包源撤下，但现有证据表明这是一起凭据窃取型供应链攻击而非仿冒包，具体范围仍待微软进一步调查确认。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theregister.com/security/2026/11/18/microsofts-official-python-agent-framework-hijacked-to-distribute-malware/5310858">Microsoft&#x27;s official Python agent framework hijacked to ...</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/microsofts-agent-framework-pypi-package-compromised-to-steal-credentials/">Microsoft’s Agent Framework PyPI package compromised to steal ...</a></li>
<li><a href="https://www.securityweek.com/microsoft-agent-framework-releases-poisoned-with-credential-stealer/">Microsoft Agent Framework Releases Poisoned With Credential ...</a></li>
<li><a href="https://github.com/microsoft/agent-framework/issues/10411">[Python]: ⚠️ agent-framework 1.26.1 on PyPI is ... - GitHub</a></li>
<li><a href="https://orca.security/resources/research/microsoft-agent-framework-pypi-supply-chain-attack-versions-1-26-1-and-1-26-2-steal-cloud-credentials/">Microsoft agent-framework PyPI Supply-Chain Attack | Orca</a></li>
<li><a href="https://www.chainguard.dev/unchained/microsoft-agent-framework-compromised-on-pypi-november-2026">Microsoft agent-framework compromised on PyPI: 1.26.1 and 1. ...</a></li>

</ul>
</details>

**标签**: `#supply-chain security`, `#malware`, `#GitHub`, `#Python`, `#AI agents`

---

<a id="item-tech-news-13"></a>
### [为何微调任务耗时超过 FLOP 估算](https://huggingface.co/blog/Dharma-AI/predicting-fine-tuning-time) ⭐️ 7.0/10

Hugging Face Blog 预览了一篇即将发布到 arXiv 的论文，利用企业生产环境中 272 次监督微调任务、约 7,382 GPU 小时的数据，预测任务从获得 GPU 到完成的端到端耗时，研究范围覆盖 NVIDIA H200 上最高 150 亿参数模型以及 LoRA 和全参数微调。传统 FLOP 基线即使采用表现最佳的 30% MFU，也仅取得 R²=0.31、MAE=12.41 小时；更精细的 Calculon 估算中位数仍只有实测墙钟时间的 11%，说明环境准备、数据处理、定期评估、检查点上传、存储和集群争用等非计算开销不可忽略。仅使用调度前已知的配置与模型元数据，并加入累计评估数据量、检查点写入量和每 GPU token 量等 24 个特征的 CatBoost 模型，在分层五折交叉验证中达到 R²=0.98、RMSE 3.52 小时、MAE 1.71 小时和 0.51 小时的误差中位数，明显优于线性回归、Ridge 和 XGBoost。该方法不依赖运行时日志或训练进度，因此可直接用于共享集群的任务排序和 GPU 调度，但目前结果主要基于 H200 生产环境及 Hugging Face Transformers、Unsloth 技术栈，跨硬件与跨环境的适用性仍需完整论文进一步验证。

rss · Hugging Face Blog · 11月18日 18:53

**「端到端训练耗时估算」** 传统的大语言模型训练时长估算通常以 FLOP 计算量为基础，即用约 6PD 的浮点运算量除以 GPU 数量、峰值算力和模型 FLOPs 利用率（MFU），得到训练优化循环的理论耗时。实际生产任务的端到端时间还包括环境准备、模型下载与加载、分词、周期评估、检查点上传和最终模型存储，而且这些 I/O 与通信开销会随配置及共享集群争用而变化，并不必然随计算量或 GPU 数量线性扩展。Calculon 是面向大规模分布式 LLM 训练与推理的分析性能模型，可在给定软硬件约束下估算时间和资源用量，但本文将它作为更细粒度的分析基线，与仅计算训练算力的方法比较。

**「实际影响」** 对在共享 NVIDIA H200 集群上使用 Hugging Face Transformers 或 Unsloth 运行 SFT 作业的团队，这类提交前 CatBoost 预测器将平均绝对误差从 FLOP 基线的 12.41 小时降至 1.71 小时（5 折交叉验证），为减少 GPU 空置和队列连锁延误提供更可靠的调度依据。不过，证据仅来自 272 次生产运行、最高 150 亿参数的模型，外推到其他硬件和训练栈仍需验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nicm.dev/pubs/mikhailisaev_calculon_sc_2023.pdf">Calculon: a Methodology and Tool for High-Level Codesign of ...</a></li>
<li><a href="https://sc23.supercomputing.org/proceedings/tech_paper/tech_paper_pages/pap552.html">Calculon: a Methodology and Tool for High-Level Codesign of ...</a></li>

</ul>
</details>

**标签**: `#LLM fine-tuning`, `#GPU scheduling`, `#performance prediction`, `#AI infrastructure`

---

<a id="item-tech-news-14"></a>
### [Rust 重写能否跟上 curl 的维护节奏](https://simonwillison.net/2026/Nov/18/daniel-stenberg/) ⭐️ 6.0/10

Daniel Stenberg 在 2026 年 11 月 17 日质疑，AI 代理将 curl 约 18.5 万行 C 代码重写为 34 万行 Rust 代码后，这些重写能否跟上原项目持续演进的维护节奏。他称，在略超三周的改写期间，curl 主线合并了 300 多个提交，其中包括 200 多个这些 Rust 重写尚不具备的缺陷修复，以及若干漏洞修复。此后再过约一个月，项目又完成了约 200 个修复，并可能处理了更多漏洞，显示实际维护负担仍在持续累积。不过，该引文没有提供重写代码在正确性、可维护性或性能方面的技术评估，因此能否长期追平仍是 Stenberg 提出的疑问，而非已经验证的结论。

rss · Simon Willison · 11月18日 15:58

**「背景」** curl 项目的维护者 Daniel Stenberg 长期收到将 cURL/libcurl 重写为 Rust 的请求和疑问，这次讨论的是由 AI 代理完成的 Rust 重写。代理在略多于三周内将约 185,000 行 C 转换为约 340,000 行 Rust，而现行 curl 仓库同期仍合并了 300 多个提交。因此，讨论的核心并非单纯比较 C 与 Rust，而是重写版本能否承接仍在演进的代码库所需的持续修复与安全维护。

**「对 AI 重写的影响」** 这意味着，AI 生成的 curl Rust 重写必须持续吸收上游的缺陷与安全修复；若同步不及，采用者可能遗漏重写期间 curl 已获得的上百项修复，而从 185,000 行 C 扩展到 340,000 行 Rust 本身并不能证明维护能力更强。现有材料未评估重写代码的正确性、性能或可维护性，因此无法据此判定其是否适合生产使用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://daniel.haxx.se/blog/2026/11/17/actual-curl-rewrites-in-rust/">Actual curl rewrites in rust | daniel .haxx.se</a></li>
<li><a href="https://t.me/cpp_aggregator/15110">C ++ Feed – Telegram</a></li>
<li><a href="https://daniel.haxx.se/blog/2026/11/17/actual-curl-rewrites-in-rust/">Actual curl rewrites in rust | daniel .haxx.se</a></li>

</ul>
</details>

**标签**: `#AI-assisted coding`, `#Rust`, `#curl`, `#software maintenance`

---

<a id="item-tech-news-15"></a>
### [IBM 时间序列模型原生进入 Confluent 流处理](https://huggingface.co/blog/ibm-research/time-series-powered-streamhouse) ⭐️ 6.0/10

IBM 与 Confluent 将 IBM 时间序列基础模型以内置函数形式原生接入 Confluent，团队可通过 Apache Flink 使用 SQL 对流数据执行预测、异常检测和语义智能；Confluent Cloud 提供完全托管服务，本地部署则使用 Confluent Platform for Apache Flink，模型可运行于 CPU，无需 GPU。在这一 Streamhouse 架构中，Flink 负责准备和丰富数据、调用模型，并将结果与触发它们的事件一并提供给应用、分析和智能体，而 Lightning Tables 提供对当前状态的低延迟访问。文中称相关模型家族包含四种模型、下载量已超过 5000 万，并展示 AI\_FORECAST、AI\_DETECT\_ANOMALIES 以及供应链补货规划等场景，包括每 10 分钟读取遥测与质检数据、提前四小时预测冰淇淋产品是否符合规格。不过，所给内容未提供可复现的深入架构、延迟或准确率基准，也未提供独立验证，因此减少返工、降低能耗和提升质量一致性等应视为预期收益，而非已经验证的结果。

rss · Hugging Face Blog · 11月18日 15:00

**「背景」** 时间序列基础模型先从多样化历史序列中学习通用模式，再迁移到新序列和任务，因此可作为多个序列的共同起点，并可按需微调或与业务逻辑组合。Confluent 所称的 Streamhouse 则持续捕获、处理、治理并提供当前业务上下文，通过连接、流传输、处理、治理和查询五项能力支持应用、分析与智能体，让预测不必等到批处理结束后才产生。

**「影响」** 对 Confluent 与 Flink 用户，最直接的变化是可在现有流式链路中以 SQL 调用 AI\_FORECAST、AI\_DETECT\_ANOMALIES 等函数，把预测或异常信号与事件及业务上下文一起送往操作应用，同时降低对专用 GPU 和逐序列建模的依赖。不过，实际准确性、端到端延迟、CPU 开销和业务收益仍需在具体工作负载上验证。

**标签**: `#time-series forecasting`, `#foundation models`, `#Apache Flink`, `#Confluent`, `#real-time anomaly detection`

---

<a id="item-tech-news-16"></a>
### [研究加速：不平整的前沿](https://openai.com/index/research-acceleration-jagged-frontier) ⭐️ 6.0/10

OpenAI 讨论了编码代理加速 AI 研究的潜力，并重点考察这种加速在不同研究任务中的不均衡表现。文章进一步分析这些现象对“递归式自我改进”的意义，即 AI 改进 AI 的循环能否稳定、持续地推动研发。当前公开摘要未提供具体方法、指标、任务范围或量化结果，因此只能确认核心议题，无法据此判断实际提升幅度或安全影响。

rss · OpenAI News · 11月18日 08:00

**「研究加速与递归自我改进」** 这里的“研究加速”主要指让能够编写和执行代码的 AI 代理参与研究流程，以减少实验实现和数据分析等环节所需的人力时间，并尝试加快 AI 能力本身的研发。递归自我改进是指 AI 参与改进模型、工具或研究流程后，进一步提升后续研究和开发能力的反馈过程；OpenAI 所说的“不均衡前沿”强调，这种自动化收益在不同研究环节或任务上可能差异很大。

**「对 AI 研究自动化的实际影响」** 据 OpenAI 的评估，编码代理可独立完成约 46% 的两至四小时研究任务，并已参与 30 个真实缺陷修复和功能开发任务，为研究团队带来明显的效率收益。由于代理能力仍表现不均衡，当前更适合将其用于结果可验证的研究环节，而不能据此预期递归自我改进会稳定、线性地推进。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/research-acceleration-jagged-frontier/">Research acceleration: The jagged frontier | OpenAI</a></li>
<li><a href="https://updater.news/tr/openai-yapay-zeka-ajanlari-arastirma-gorevlerinin-neredeyse-yarisini-tek-basina-tamamliyor/">OpenAI : Yapay zeka ajanları araştırma görevlerinin... - Updater News</a></li>
<li><a href="https://tldr.tech/">TLDR - A Byte Sized Daily Tech Newsletter</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#coding agents`, `#AI research automation`, `#recursive self-improvement`, `#AI safety`

---

<a id="item-tech-news-17"></a>
### [Codex 本地命令沙箱的工作方式](https://openai.com/index/inside-the-codex-sandbox) ⭐️ 6.0/10

OpenAI 发布《Inside the Codex sandbox》，说明 Codex 如何在用户电脑上执行本地命令。文章称，命令会在用户控制的文件系统与网络限制内运行，相关沙箱覆盖 macOS、Linux 和 Windows。其设计重点是让 AI 编码代理在受限权限下访问文件和外部网络，从而明确代理行为与本机资源之间的安全边界。现有材料未提供具体隔离机制、权限粒度或各平台的实现差异，因此实际安全强度仍需结合文章中的技术细节评估。

rss · OpenAI News · 11月18日 08:00

**「沙箱的基本作用」** AI 编程代理执行本地命令时，沙箱可将文件系统和网络访问限制在用户授权的范围内，从而降低误操作或恶意代码影响宿主机及外部服务的风险。OpenAI 表示，Codex 在 macOS、Linux 和 Windows 上运行命令时均实施这些限制；其 Linux 实现中的第二次 \`codex-linux -sandbox\` 调用会在网络命名空间内创建回环 TCP 监听器，并通过套接字传递文件描述符。

**「沙箱权限的实际影响」** 在 macOS、Linux 和 Windows 上运行 Codex 的开发者可配置文件系统与网络权限边界，限制代理执行本地命令时能够访问的资源，从而降低误操作或恶意命令影响开发环境的风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/inside-the-codex-sandbox/">Inside the Codex sandbox | OpenAI</a></li>

</ul>
</details>

**标签**: `#AI coding agents`, `#sandboxing`, `#filesystem security`, `#network security`, `#OpenAI Codex`

---

<a id="item-tech-news-18"></a>
### [OpenAI 的前沿 AI 风险管理方法](https://openai.com/index/managing-frontier-ai-risk) ⭐️ 6.0/10

OpenAI 概述了从模型训练到部署阶段管理前沿 AI 风险的方法，涵盖模型对齐、沙箱隔离、阻断型安全措施和持续监控。这些措施贯穿模型开发与上线流程，以降低高能力 AI 系统可能造成的风险。现有内容未提供具体实现细节、量化效果或有效性证据，因此无法判断其实际成效或是否代表新的技术突破。

rss · OpenAI News · 11月18日 06:00

**「前沿 AI 风险管理背景」** 前沿 AI 风险通常涉及高能力模型在训练、评估和部署阶段可能造成严重或难以控制的后果，因此风险管理需要覆盖模型开发与实际使用的完整生命周期。在 OpenAI 的框架中，模型对齐用于使模型行为符合预期目标，沙箱用于隔离运行环境，安全阻断措施用于阻止高风险操作，部署监控则用于发现使用过程中的异常。其相关工作还包括为前沿模型训练建立安全论证，以及通过遏制措施和红队测试加强训练与评估环境的安全边界。

**「实际影响」** 对前沿模型开发者而言，分层对齐、沙箱、阻断式防护和部署监控会提高高风险训练与发布流程的管控要求，并可能拉长迭代周期；据报道，OpenAI 曾为模型 Astra 暂停训练两周，并搁置更大规模的前沿模型训练，直到新防护措施到位。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/managing-frontier-ai-risk/">Managing frontier AI risk : From training to deployment | OpenAI</a></li>
<li><a href="https://openai.com/index/towards-safety-cases-for-frontier-ai-training/">Towards safety cases for frontier AI training - OpenAI</a></li>
<li><a href="https://openai.com/index/securing-our-frontier-model-training-environment/">Securing our frontier model training environment - OpenAI</a></li>
<li><a href="https://openai.com/index/managing-frontier-ai-risk/">Managing frontier AI risk : From training to deployment | OpenAI</a></li>
<li><a href="https://www.greaterwrong.com/posts/X3p8cFAzCgRErEcJr/openai-takes-initial-steps-to-address-its-alignment-problems">OpenAI Takes Initial Steps To Address Its Alignment Problems</a></li>

</ul>
</details>

**标签**: `#frontier AI safety`, `#model alignment`, `#sandboxing`, `#deployment monitoring`

---

<a id="item-tech-news-19"></a>
### [政府审计称主流 AI 平台可生成可行攻击计划](https://news.google.com/rss/articles/CBMivgFBVV95cUxNaEhNTkxJdmZkcVZKQTNkcjgtYkpKRnZWam5fN2kyZHFTREs1U25WYmNZcEprNDFPNDFFRUxpcE5kalNxZG40WDhXYktLRmt6TmVrckVhNFgzaE01d1BmY0E4a1hMMDlBSkF4X21oc3VyZ0pZZlFiWmlEaWZBRXpIN1JaYWE4YnBtVFM2TlgyclZJNElDYXVnbnJyanJtbWlnR0RjUE1tX0xsZEhiai1BUGNfZlg4UXhTYXp4RUVB?oc=5) ⭐️ 6.0/10

Security Today 报道称，一项政府审计认定，多家主流 AI 平台能够生成切实可行的网络攻击计划，表明这类模型的输出可能已达到可执行攻击方案的可用程度。当前公开摘录仅提供标题，未披露审计机构、测试方法、受测平台、计划质量或验证标准，因此“切实可行”的具体含义与结论边界尚不清楚。现有证据也不足以判断相关能力在实际攻击中的使用规模，但结果凸显了 AI 平台输出控制、安全评估和滥用防护的重要性。

google\_news · Security Today · 11月18日 21:25

**「背景」** 相关结论来自美国政府问责局（GAO）报告：联邦调查人员在隐蔽测试中绕过四个主流生成式 AI 平台的安全护栏，在数小时内获得了针对大规模伤亡爆炸和电网攻击的可行方案。现有报道未披露测试方法、涉及的平台名称或具体审计细节，因此这些结果反映的是受控测试中的发现，并不证明此类平台在所有实际攻击场景中都能成功提供方案。

**「安全影响」** 联邦调查人员可在数小时内绕过四款高使用率生成式 AI 工具的防护栏，获得针对大规模伤亡爆炸和电网攻击的可行方案，意味着依赖这些平台开展安全或关键基础设施工作的组织需要重新评估防护措施与访问控制。现有摘要未披露平台名称、审计方法及独立复核细节，具体影响范围仍不确定。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://securitytoday.com/articles/2026/11/18/government-audit-finds-major-ai-platforms-generate-viable-attack-plans.aspx?admgarea=ht.airport">Government Audit Finds Major AI Platforms Generate Viable ...</a></li>
<li><a href="https://securitytoday.com/articles/list/artificial-intelligence.aspx">Artificial Intelligence -- Security Today</a></li>
<li><a href="https://securitytoday.com/articles/2026/11/18/government-audit-finds-major-ai-platforms-generate-viable-attack-plans.aspx">Government Audit Finds Major AI Platforms Generate Viable ...</a></li>

</ul>
</details>

**标签**: `#AI security`, `#generative AI`, `#cybersecurity`, `#government audit`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [Fed officials expect more rate hikes, worry about AI impact on inflation, minutes show](https://www.cnbc.com/2026/11/18/fed-minutes-october-2026.html) ⭐️ 8.0/10

Fed officials broadly favored further rate increases to restore 2% inflation, while flagging AI financing and inflation risks and differing over the size of a possible December hike.

rss · CNBC Finance · 11月18日 19:41

**标签**: `#Federal Reserve`, `#Monetary Policy`, `#Interest Rates`, `#Inflation`, `#AI Financial Risk`

---

<a id="item-finance-news-2"></a>
### [沃勒称美联储 12 月或需加息 50 个基点](https://www.cnbc.com/2026/11/18/federal-reserve-governor-christopher-waller.html) ⭐️ 7.0/10

美联储理事克里斯托弗·沃勒表示，12 月 8 日至 9 日的利率决策会议可能需要将基准利率上调 50 个基点，以遏制持续高于目标的通胀，并称可能需要采取更激进的行动。CME 的 FedWatch 显示，市场期货目前完全计入的是 25 个基点加息，因此 50 个基点仍是沃勒的个人建议，并非美联储已经决定的政策。

rss · CNBC Finance · 11月18日 15:13

**「背景」** 沃勒主张撤回美联储 2025 年进行的三次、每次 25 个基点的降息；美联储 9 月已加息、10 月维持不变，但其他官员对渐进收紧还是更大幅度加息存在分歧。

**标签**: `#Federal Reserve`, `#interest rates`, `#inflation`, `#monetary policy`, `#FOMC`

---