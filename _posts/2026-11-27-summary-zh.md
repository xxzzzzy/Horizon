---
layout: default
title: "Horizon Summary: 2026-11-27 (ZH)"
date: 2026-11-27
lang: zh
---

> 从 87 条内容中筛选出 12 条重要资讯。

---

**科技新闻**
1. [1Password 源码与客户数据遭窃](#item-tech-news-1) ⭐️ 8.0/10
2. [英伟达暂停向东南亚四国发运 AI 服务器](#item-tech-news-2) ⭐️ 8.0/10
3. [AMD 专用 llama.cpp 推理分支](#item-tech-news-3) ⭐️ 7.0/10
4. [Google Will Make AI Agents Use Its MCP Servers. The Gmail One Can&\#x27;t Send Email](#item-tech-news-4) ⭐️ 7.0/10
5. [服务十国的印度政务平台曝严重 SQL 注入漏洞](#item-tech-news-5) ⭐️ 7.0/10
6. [微软称 ARTEX 加速全球科技系统入侵](#item-tech-news-6) ⭐️ 7.0/10
7. [Rackspace 因安全入侵终止 Spot 云服务](#item-tech-news-7) ⭐️ 7.0/10
8. [可感知压力的新一代仿生手](#item-tech-news-8) ⭐️ 7.0/10
9. [独立浏览器 Ladybird 进入 Alpha 测试](#item-tech-news-9) ⭐️ 6.0/10
10. [怀俄明铀矿运营因网络攻击停摆](#item-tech-news-10) ⭐️ 6.0/10
11. [英国边境系统数据纠错失效获 ICO 训诫](#item-tech-news-11) ⭐️ 6.0/10
12. [llama.cpp 发布 AMD 推理基准面板](#item-tech-news-12) ⭐️ 6.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [1Password 源码与客户数据遭窃](https://www.theregister.com/security/2026/11/26/hackers-help-themselves-to-1passwords-source-code-and-customer-data/5312317) ⭐️ 8.0/10

据 The Register 于 2026 年 11 月 26 日报道，攻击者入侵了 1Password 的后端服务并植入恶意代码，随后窃取了该公司的源代码和客户数据，表明风险可能同时覆盖服务端、开发资产和用户信息。后端及代码供应链因此成为此次事件的关键攻击面，但现有材料未披露具体数据类别、攻击入口或受影响范围。1Password 坚称用户密码仍然安全，不过这一说法来自公司自身，现有信息不足以独立验证密码、加密密钥或其他敏感数据是否未受影响。文章也未说明完整时间线、受害者数量及处置进展，具体影响仍需等待进一步技术调查。

rss · The Register · 11月26日 11:02

**「事件背景」** 这起事件的背景是，1Password 于 2026 年 11 月 19 日开始调查攻击者可能取得其员工企业 GitHub 账户的迹象；攻击者据称利用该账户访问源代码，并向后端服务植入恶意代码。1Password 表示源代码不包含客户数据或用户秘密，但其 CI/CD 系统包含服务运行所需的基础设施机密；报道还称有与客户有关的管理数据被下载，因此事件涉及代码、部署链路和客户数据多个层面，而公司所称用户密码仍然安全并不代表其他数据未受影响。

**「用户影响」** 此次入侵已导致部分客户信息被未授权访问，但据 1Password 称，其后端无法访问客户密码、秘密密钥或保险库内容，因此用户目前无需更新 1Password 账户。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://1password.com/blog/update-on-nov-2026-security-incident">Update on a security incident involving 1 Password ’s backend systems.</a></li>
<li><a href="https://www.macrumors.com/2026/11/25/1password-security-breach/">1 Password Security Breach : What Was Accessed and... - MacRumors</a></li>
<li><a href="https://thehackernews.com/2026/11/1password-hacked-customer-data-and.html">1 Password Hacked, Customer Data and Source Code Stolen in...</a></li>
<li><a href="https://1password.com/blog/update-on-nov-2026-security-incident">Update on a security incident involving 1 Password ’s backend systems.</a></li>
<li><a href="https://thehackernews.com/2026/11/1password-hacked-customer-data-and.html">1 Password Hacked, Customer Data and Source Code Stolen in...</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#1Password`, `#data breach`, `#supply-chain security`, `#credential security`

---

<a id="item-tech-news-2"></a>
### [英伟达暂停向东南亚四国发运 AI 服务器](https://www.ft.com/content/7838a715-07d4-4605-aa60-21f5af2b2370) ⭐️ 8.0/10

据《金融时报》报道，英伟达已要求主要制造伙伴暂停向马来西亚、新加坡、泰国和印度尼西亚发运 AI 服务器，戴尔、美超微等整机厂商已通知四国买家相关订单不能出厂。三名知情人士称，此举与美方新一轮出口管制有关，但尚不清楚冻结是否只是临时措施。报道指出，这四国是中国 AI 公司获取英伟达最先进处理器的中转地，而相关芯片不得直接出口中国大陆。美国商务部上周发布的新规要求区域云服务商在 90 天内取得出口许可，并核查客户是否包含受限制的中国实体。

telegram · zaihuapd · 11月26日 07:38

**「背景」** 此次暂停针对的是由戴尔、美超微等厂商组装、搭载英伟达芯片的 AI 服务器。触发措施的美国新规将许可期限设为 90 天，并要求区域云服务商识别受限中国实体，以审查先进 AI 芯片的最终流向。

**「影响」** 四国买家可能因此推迟服务器接收、数据中心部署和 AI 算力扩容，云服务商则需重新确认客户与许可合规状态。由于报道未说明冻结持续时间，相关交付何时恢复仍不确定。

**标签**: `#AI芯片`, `#出口管制`, `#AI服务器`, `#东南亚`, `#供应链`

---

<a id="item-tech-news-3"></a>
### [AMD 专用 llama.cpp 推理分支](https://devnull.land/amd-specific-llama-cpp) ⭐️ 7.0/10

一份 AMD 专用 llama.cpp 分叉在 Hacker News 引发关注，目标是让本地大语言模型推理更充分地利用高内存带宽但计算能力有限的 AMD 加速器。讨论主要围绕 circa 2018 年的 gfx906 数据中心卡；这些卡没有张量核心或原生 BF16，却可搭载 HBM2，社区称 32GB 版本拥有约 1TB/s 带宽且二手成本约 200 美元。评论者称，在 Radeon Pro 9700 上运行量化后的 Qwen3.8-27B 可达到约 2400 token/s 的预填充和 150 token/s 的解码速度，并能同时承载 3 路、每路 20 万 token 上下文的代理任务；MI100 用户则称，移植 NVIDIA 内核至 ROCm 后可将性能提高到 Qwen3.8 的两至三倍。这些速度、价格和稳定性结果均来自社区经验，当前条目没有提供完整实现、基准方法或硬件配置，因而不能视为经独立验证的性能承诺。

hackernews · julianlam · 11月26日 17:11 · [社区讨论](https://news.ycombinator.com/item?id=50657265)

**「AMD 专用分支背景」** llama.cpp 是用于本地大语言模型推理的开源框架，而这个分支主要针对 AMD gfx906 架构的 Radeon VII、MI50 和 MI60，弥补上游缺少该架构专用调优，以及在 ROCm 与 Vulkan 混合、显存紧张时缺少可控流水线并行的不足。相关页面还推荐了独立的 llama-cpp-rdna-boosts，并给出生成速度从 35 提升至 55 token/s、预填充速度从 700 提升至 1,300 token/s 的个案结果，但这些并非独立基准测试数据。

**「实际影响」** 对于使用 Radeon VII、MI50、MI60 等 gfx906 加速器的用户，该专用 llama.cpp 分支可提供上游尚缺失的硬件调优、混合 ROCm/Vulkan 配置和可控流水线并行，提升显存紧张场景下的本地大模型推理效率与部署可行性。不过，具体吞吐量提升主要来自社区实测，实际表现仍取决于模型、量化和硬件组合。

**「社区讨论」** 实际使用反馈总体积极：Radeon Pro 9700 用户称量化模型的 KLD 为 0.006、top-1 为 0.972，并已用其处理代理和编程任务；MI100 用户称移植并数值校验 NVIDIA 内核后方案稳定，性能达到 Qwen3.8 的两至三倍。不过这些多为不同硬件、模型和量化配置下的个案报告，缺少统一测试条件，不能直接横向比较。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/milpster/gfx906-llama-cpp">GitHub - milpster/gfx906-llama-cpp</a></li>
<li><a href="https://devnull.land/amd-specific-llama-cpp">AMD-specific fork of llama.cpp - devnull.land</a></li>
<li><a href="https://github.com/milpster/gfx906-llama-cpp">GitHub - milpster/gfx906-llama-cpp</a></li>
<li><a href="https://grafy.ai/news/amd-specific-llama-cpp-patches-boost-inference-speeds">AMD-specific llama.cpp patches boost speeds — Grafy News</a></li>

</ul>
</details>

**标签**: `#llama.cpp`, `#AMD GPUs`, `#local LLM inference`, `#open-source AI`, `#HBM2`

---

<a id="item-tech-news-4"></a>
### [Google Will Make AI Agents Use Its MCP Servers. The Gmail One Can&\#x27;t Send Email](https://techstackups.com/articles/google-workspace-ai-agents-mcp/) ⭐️ 7.0/10

Google appears to require partner-mediated MCP integrations for Workspace agents, while a Gmail MCP server cannot send email, exposing practical questions about confirmation, automation, and platform control.

hackernews · ritzaco · 11月26日 09:44 · [社区讨论](https://news.ycombinator.com/item?id=50653477)

**标签**: `#MCP`, `#AI agents`, `#Google Workspace`, `#email automation`, `#developer platforms`

---

<a id="item-tech-news-5"></a>
### [服务十国的印度政务平台曝严重 SQL 注入漏洞](https://www.theregister.com/security/2026/11/27/free-e-government-platform-that-serves-two-billion-people-in-ten-countries-has-critical-sql-injection-bug/5312449) ⭐️ 7.0/10

报道称，免费的印度政务平台 Digital Infrastructure for Governance Impact and Transformation 被曝存在严重 SQL 注入漏洞，攻击者可能借此读取并泄露平台中的数据。该平台据称覆盖 10 个国家、服务约 20 亿人口，因此漏洞若能被实际利用，可能波及多个国家的公共服务和敏感政务数据。当前材料未披露受影响版本、漏洞位置、利用前提、是否已遭攻击或官方修复措施，尚无法确定具体影响范围。相关运营方应尽快确认受影响的部署，检查漏洞能否被远程利用，并采取适当的修复或缓解措施。

rss · The Register · 11月27日 01:19

**「DIGIT 平台与 SQL 注入背景」** DIGIT（Digital Infrastructure for Governance Impact and Transformation）是印度推出的开源模块化电子政务平台，据报道已用于 10 个国家，服务规模可达约 20 亿人。SQL 注入是一类将恶意 SQL 语句带入应用数据库查询的漏洞；当输入与查询未被安全隔离时，攻击者可能读取、泄露或篡改数据。

**「潜在影响」** 如果被利用，DIGIT 平台的严重 SQL 注入漏洞可能使攻击者读取该十国政务生态中约二十亿人口相关的敏感公共部门数据。现有报道未说明受影响版本、是否已遭利用或修复状态，因此实际暴露范围仍不确定。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theregister.com/security/2026/11/27/free-e-government-platform-that-serves-two-billion-people-in-ten-countries-has-critical-sql-injection-bug/5312449">Free e-government platform that serves two billion people in ...</a></li>
<li><a href="https://securityelites.com/news/digit-egovernment-platform-critical-sql-injection-flaw/">Critical SQL Injection Bug In India&#x27;s DIGIT Platform</a></li>
<li><a href="https://www.broadvision.co.za/news/critical-sql-injection-bug-identified-in-digit-e-government-platform-3860c0">Critical SQL Injection Bug Identified in DIGIT e-Government ...</a></li>
<li><a href="https://appsource.microsoft.com/en-us/product/saas/egovernmentsfoundation.egov-digit-nus?tab=overview">DIGIT - Urban Governance Platform</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#SQL injection`, `#e-government`, `#vulnerability`

---

<a id="item-tech-news-6"></a>
### [微软称 ARTEX 加速全球科技系统入侵](https://www.theregister.com/security/2026/11/26/microsoft-hackers-in-china-n-korea-using-artex-ai-tool-to-break-into-global-tech-systems/5312433) ⭐️ 7.0/10

微软称，来自中国和朝鲜的黑客正在使用名为 ARTEX 的智能体式 AI 攻击框架，针对全球科技系统实施入侵。ARTEX 并未创造全新的攻击方法，而是自动执行成熟且常见的网络攻击技术，以减少人工操作并提高攻击效率。微软指出，该工具可能在数分钟内突破薄弱防御，显示智能体式 AI 正被用于加速国家级网络攻击。目前公开信息尚未说明具体受影响系统、完整技术细节或缓解措施，其实际影响范围仍有待确认。

rss · The Register · 11月26日 19:04

**「ARTEX 框架背景」** ARTEX 是一种代理式 AI 渗透测试框架，可自动执行网络侦察、凭据攻击和 Web 应用漏洞利用等既有流程，因此其核心作用是减少实施熟悉攻击技术所需的人工和时间。微软披露，Storm-0940 已利用 ARTEX 加速针对 ConnectWise 的供应链入侵，并在 Microsoft 365 环境中滥用应用凭据；后续研究还列出了 Storm-3358、Onyx Sleet、Pearl Sleet、Crystal Typhoon 和 Salt Typhoon 等使用该框架的威胁组织。

**「实际影响」** 对仍暴露客户端密钥或采用薄弱防御的组织而言，ARTEX 可把已知攻击步骤自动化，令部分系统在数分钟内遭突破，防守方因此面临更短的发现与响应窗口。防守方应按具体入侵行为和失陷指标进行检测，而不能仅凭 ARTEX 的使用将攻击归因于中国或朝鲜黑客。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.microsoft.com/en-us/security/blog/2026/10/21/storm-0940-uses-artex-agentic-ai-connectwise-supply-chain-compromise/">AI-driven, large-scale nation-state campaign using ARTEX ...</a></li>
<li><a href="https://www.microsoft.com/en-us/security/blog/2026/11/25/what-defenders-need-to-know-artex-agentic-ai-framework-threat-actors-abuse/">What defenders need to know about ARTEX, the agentic AI ...</a></li>
<li>Microsoft finds 2 North Korean groups using ARTEX, a tool that alone ...</li>
<li>Why ARTEX Became a Threat - Aviatrix</li>

</ul>
</details>

**标签**: `#AI security`, `#agentic AI`, `#cybersecurity`, `#nation-state threats`, `#ARTEX`

---

<a id="item-tech-news-7"></a>
### [Rackspace 因安全入侵终止 Spot 云服务](https://www.theregister.com/cyber-crime/2026/11/26/rackspace-pulls-plug-on-spot-cloud-service-after-security-breach/5312352) ⭐️ 7.0/10

Rackspace 在发生安全入侵事件后，已停止其 Spot 云服务。相关客户必须迁移原本运行在 Spot 上的工作负载，并轮换可能受到入侵影响的访问凭据。现有摘录未披露入侵方式、受影响系统范围、凭据类型或数据是否被外传，因此事件的暴露程度仍不明确。客户需要尽快盘点服务依赖、完成工作负载迁移并轮换凭据，以降低服务中断和未授权访问风险。

rss · The Register · 11月26日 14:45

**「事件背景」** Rackspace Spot 是 Rackspace 运营的低成本云服务，此次安全事件涉及客户 Kubernetes 集群及其中保存的密钥。外部报道将事件起点追溯至 2026 年 11 月 17 日凌晨，攻击者使用窃取的登录凭据进入 Spot 的部分环境；Rackspace 随后宣布让该平台于 12 月 8 日停止运行。

**「直接影响」** Rackspace Spot 客户需要迁移已停止服务的工作负载、检查未授权部署并更换可能暴露的 Kubernetes 密钥。此次入侵中，攻击者利用受损凭据访问了客户集群的 Kubernetes 密钥，因此相关组织还应立即轮换在此次事件中可能泄露的凭据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/rackspace-shuts-down-spot-cloud-platform-after-security-breach/">Rackspace shuts down Spot cloud platform after security breach</a></li>
<li><a href="https://tech.yahoo.com/cybersecurity/articles/rackspace-forced-shut-down-spot-160500392.html">Rackspace forced to shut down Spot cloud platform following ...</a></li>
<li><a href="https://www.theregister.com/cyber-crime/2026/11/26/rackspace-pulls-plug-on-spot-cloud-service-after-security-breach/5312352">Rackspace pulls plug on Spot cloud service after security breach</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/rackspace-spot-breach-let-hackers-access-customer-kubernetes-secrets/">Rackspace Spot breach let hackers access customer Kubernetes...</a></li>

</ul>
</details>

**标签**: `#cloud security`, `#security breach`, `#workload migration`, `#credential rotation`, `#Rackspace Spot`

---

<a id="item-tech-news-8"></a>
### [可感知压力的新一代仿生手](https://www.technologyreview.com/2026/11/26/1149923/the-next-generation-of-bionic-hands-is-here-and-they-can-feel/) ⭐️ 7.0/10

犹他大学团队在临床试验中为参与者 Avi Davidson 植入一种连接前臂神经的新接口，使仿生 LUKE 机械臂既能由神经活动控制，也能将接触压力反馈回手臂。手术在三条神经中各植入含 100 根针的电极阵列，并在肌肉周围植入 24 个电极；研究人员通过双向训练，将运动意图转换为手、腕和手指动作，同时建立压力感与电刺激之间的映射。Davidson 是第九名接受植入者，也是首位将设备带回家独立使用的参与者；自 7 月 10 日起，他已能抓握葡萄、鸡蛋和妻子的手，完成烹饪与书写，通常每周佩戴约 6 天，设备重约 5 磅，充电或更换电池一至两次。相比仅能控制动作或缺少触觉的既有假肢，这种压力反馈为更自然、更精细的日常操作提供了关键能力，但该技术仍处于小规模实验阶段，目前仅 9 人接受植入，参与者不能保留设备且需接受植入和移除两次手术，其长期实用性以及对手臂神经、脑功能和心理状态的影响仍待研究。

rss · MIT Technology Review · 11月26日 09:59

**「技术背景」** 这类假肢依靠双向神经接口：一方面解读残肢神经信号来控制手、腕和手指动作，另一方面通过电刺激把接触压力等感觉反馈给使用者。犹他大学的原型以 DEKA 已商业化的 LUKE 机械臂为基础，并加入 BIOS 直接神经接口；LUKE 早在 2000 年代已开发并于 2014 年获 FDA 批准，因此这项临床试验主要验证新的神经连接在真实居家环境中的效用与局限。

**「实际影响」** 对参与犹他大学临床试验的上肢截肢者，神经压力反馈已让首位居家使用者能够更精细地抓握和操作易碎物品，但设备目前仍属实验性、仅有九人植入，距离普遍临床应用尚远。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.price.utah.edu/2026/09/18/from-lab-to-living-room-revolutionary-utah-bionic-arm-enters-first-home-trial">From Lab to Living Room: Revolutionary Utah Bionic Arm Enters ...</a></li>

</ul>
</details>

**标签**: `#bionic prosthetics`, `#neural interfaces`, `#sensory feedback`, `#robotics`, `#clinical trials`

---

<a id="item-tech-news-9"></a>
### [独立浏览器 Ladybird 进入 Alpha 测试](https://www.theregister.com/software/2026/11/26/indie-web-browser-ladybird-enters-alpha-testing/5311914) ⭐️ 6.0/10

独立浏览器引擎项目 Ladybird 已进入 Alpha 测试阶段，并开始提供可下载的 macOS 与 Linux 构建版本。开发者和技术用户现在可以在两大桌面平台抢先试用并测试这一浏览器引擎。项目明确不提供安全保证，因此此次发布更适合作为开发与反馈里程碑，而非用于日常或生产环境的正式版本。现有报道未说明具体兼容性、性能表现或后续稳定化计划，其实际成熟度仍无法据此判断。

rss · The Register · 11月26日 18:15

**「背景」** Ladybird 由 Ladybird Browser Initiative 开发，这是一个专注于浏览器项目的 501\(c\)\(3\) 非营利组织。与 Chromium、Gecko 或 WebKit 等现有引擎不同，Ladybird 的浏览器引擎从零编写，并非上述引擎的分支，因此被定位为一款独立浏览器。

**「实际影响」** macOS 和 Linux 的开发者及早期测试者现在可以下载 Ladybird alpha 版，试用其不依赖 Chromium、Gecko 或 WebKit 的自研浏览器引擎，从而获得测试独立浏览器技术的新平台。由于项目明确不提供安全保证，该版本尚不适合日常或生产环境使用，尤其不应处理敏感数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Ladybird_%28web_browser%29">Ladybird (web browser ) - Wikipedia</a></li>
<li><a href="https://ladybird.org/">Ladybird is a truly independent web browser , backed by a non-profit.</a></li>
<li><a href="https://en.wikipedia.org/wiki/Ladybird_%28web_browser%29">Ladybird (web browser ) - Wikipedia</a></li>
<li><a href="https://www.omgubuntu.co.uk/2026/11/ladybird-browser-enters-alpha">Ladybird browser reaches alpha after four years of... - OMG! Ubuntu</a></li>
<li><a href="https://blog.openreplay.com/ladybird-non-chromium-browser/">Exploring Ladybird , the Non-Chromium Browser Project</a></li>

</ul>
</details>

**标签**: `#web browsers`, `#browser engines`, `#alpha testing`, `#macOS`, `#Linux`

---

<a id="item-tech-news-10"></a>
### [怀俄明铀矿运营因网络攻击停摆](https://www.theregister.com/security/2026/11/26/wyoming-uranium-operation-shuts-down-after-cyberattack/5312323) ⭐️ 6.0/10

Peninsula Energy 表示，一次网络攻击影响了其位于怀俄明州的铀矿运营设施，包括工厂和井场控制系统。运营因此停摆，目前尚无恢复启动的日期。现有报道未披露攻击入口向量、受影响的具体系统或是否存在更广泛影响。

rss · The Register · 11月26日 14:02

**「项目背景」** 该设施采用原地浸出（ISL）工艺回收铀，此前使用的高 pH 流程出现了铀回收率低于预期的情况。Peninsula Energy 的怀俄明州 Lance 项目自 2019 年 7 月上一次产铀后开展研究和现场试验，并计划改用低 pH 回收流程恢复运营；此次停运发生在该项目计划重启的背景下。

**「运营影响」** 这次网络攻击已导致 Peninsula Energy 在怀俄明州的 Lance 铀项目停产，工厂和井场控制系统均受影响，运营方尚未公布重启日期，因此目前无法评估事件对 2027 年产量指引的影响。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.world-nuclear-news.org/Articles/Peninsula-Energy-to-restart-Wyoming-uranium-operat?feed=feed">Peninsula Energy to restart Wyoming uranium operation</a></li>
<li><a href="https://sprottetfs.com/insights/the-optimistic-news-continues/">Sprott Uranium Report: The Optimistic News Continues | Precious...</a></li>
<li>Wyoming uranium operation shuts down after cyberattack - The Register</li>
<li>Lance operations suspended after cybersecurity incident</li>
<li>Peninsula Energy cyber-attack stops Lance uranium mine - TechBag</li>

</ul>
</details>

**标签**: `#cybersecurity`, `#industrial control systems`, `#critical infrastructure`, `#uranium mining`

---

<a id="item-tech-news-11"></a>
### [英国边境系统数据纠错失效获 ICO 训诫](https://www.theregister.com/security/2026/11/26/uk-home-office-waved-through-border-system-without-a-working-fix-for-bad-data/5312162) ⭐️ 6.0/10

英国《The Register》报道称，内政部在一套边境系统尚无有效的错误数据修复方案时便予放行，相关做法随后受到英国信息专员办公室（ICO）训诫。临时纠错流程耗时一年以上才到位，暴露出该系统在数据质量和可靠性支持方面的明显不足。ICO 指出，这些失误可能造成错误拘留，但现有摘要未披露具体系统、错误数据类型、审批程序及影响范围。事件凸显了公共部门边境技术在上线审查、数据治理和问责机制方面的风险。

rss · The Register · 11月26日 09:30

**「背景」** 英国信息专员办公室（ICO）是负责数据保护监管的英国机构，其职责包括监督《英国通用数据保护条例》（UK GDPR）的遵循情况并提供相关指引。边境控制决策依赖个人身份和移民记录，因此错误数据不仅构成数据质量问题，也可能影响拘留等行政决定的可靠性；本案中受到质疑的是临时纠错流程能否真正解决这一风险。

**「边检数据故障的影响」** Helios 的数据完整性故障曾导致旅客被错误拘留，并在系统切换后造成约 800 人边检延误；在临时纠正流程一年多后才到位期间，数据质量问题直接影响了旅行者权益和通关可靠性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ico.org.uk/">Information Commission&#x27;s Office</a></li>
<li><a href="https://www.infosecurity-magazine.com/news/home-office-reprimanded-gdpr/">Home Office Reprimanded After GDPR Failure at the Border</a></li>
<li><a href="https://www.civilserviceworld.com/professions/article/home-office-reprimanded-over-data-failings-linked-to-hundreds-of-border-delays">Information Commission reprimands Home Office over data ...</a></li>
<li><a href="https://cy.ico.org.uk/about-the-ico/media-centre/news-and-blogs/2026/11/home-office-reprimanded-after-personal-information-failings-at-uk-border/">Home Office reprimanded after personal information failings ...</a></li>

</ul>
</details>

**标签**: `#public-sector IT`, `#border control systems`, `#data quality`, `#ICO`, `#software reliability`

---

<a id="item-tech-news-12"></a>
### [llama.cpp 发布 AMD 推理基准面板](https://huggingface.co/blog/ggml-org/llamacpp-amd-bench) ⭐️ 6.0/10

Hugging Face 发布了公共的 llama.cpp × AMD Benchmark 面板，用于在 AMD Ryzen 和 Radeon 硬件上跟踪并比较不同 llama.cpp 构建、模型及量化的本地 LLM 推理性能。用户可按硬件、模型和构建筛选，查看量化对比、构建历史及上下文扩展结果；目前列出的硬件是采用 gfx1151 的 Radeon 8060S 和采用 gfx1201 的 Radeon AI Pro R9700S。公开的 gfx1151 与 gfx1201 工作流每周运行，使用 llama-install.sh 分发的预编译二进制文件、llama-bench 工具、开启和关闭 Flash Attention 的配置以及每种配置 10 次重复测试。当前模型涵盖 Inkling 2 Mini、Qwen、Gemma、gpt-oss 和 LFM，GGUF 格式包括 Q4\_K\_M、Q8\_0、BF16、F16 等；面板直接读取 Hugging Face 上公开的 ggml-org/install.sh-benches-data 存储桶，并提供 JSONL 原始结果供复查、复现或制作自定义图表。

rss · Hugging Face Blog · 11月26日 11:37

**「基准指标含义」** 面板使用两个以每秒 token 数表示的固定负载：PP512 处理 512 个输入 token 而不生成内容，用于衡量提示处理速度；TG128 在没有既有上下文时生成 128 个 token，用于衡量输出生成速度。两项测试均从上下文深度零（n\_depth=0）开始，图中绘制的是平均吞吐量（avg\_ts）；上下文扩展测试则用于观察已有上下文增长时的生成吞吐量变化。

**「为本地推理选型提供依据」** AMD 开发者和本地 LLM 用户现在可以针对具体 Radeon 硬件、模型与量化比较 llama.cpp 构建，并利用公开历史数据发现版本更新带来的性能变化。

**标签**: `#llama.cpp`, `#AMD Radeon`, `#local LLM inference`, `#benchmarking`, `#quantization`

---