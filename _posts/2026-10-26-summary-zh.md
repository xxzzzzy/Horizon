---
layout: default
title: "Horizon Summary: 2026-10-26 (ZH)"
date: 2026-10-26
lang: zh
---

> 从 59 条内容中筛选出 5 条重要资讯。

---

**科技新闻**
1. [苹果将发布首款触屏 MacBook Pro](#item-tech-news-1) ⭐️ 8.0/10
2. [OpenAI 与 Anthropic 大幅下调 API 价格](#item-tech-news-2) ⭐️ 7.0/10
3. [Nanbeige 4.3-33B 发布为 Apache 2.0 教师模型](#item-tech-news-3) ⭐️ 7.0/10
4. [iPhone Duo 拆解指向“裂屏门”潜在原因](#item-tech-news-4) ⭐️ 6.0/10
5. [r/opensource 禁止 AI 项目并收紧投稿规则](#item-tech-news-5) ⭐️ 6.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [苹果将发布首款触屏 MacBook Pro](https://www.bloomberg.com/news/newsletters/2026-10-25/apple-to-unveil-touch-screen-macbook-pro-executive-promotions-in-box-checker) ⭐️ 8.0/10

据 Bloomberg 报道，苹果计划于本周三发布旗下首款触屏 MacBook Pro，提供 14 英寸和 16 英寸版本，采用 OLED 屏幕并加入“灵动岛”。这款产品将让 Mac 首次支持触摸操作，触控将作为键盘和触控板的补充，而非取代传统输入方式；其起售价将高于现款 2499 美元。此次变化表明苹果在多年以人体工学为由拒绝触屏笔记本后开始重新评估产品路线，报道认为这更多与营收和营销诉求有关。具体兼容性、交互设计、售价及最终发布信息仍需苹果官方确认。

telegram · zaihuapd · 10月25日 14:25

**「背景」** 苹果此前长期未在 MacBook 上加入触摸屏，并以人体工学等理由否定触控笔记本，因此此次产品动向被视为其交互路线的明显调整。相关报道称，苹果可能同时推出 14 英寸和 16 英寸机型，并测试仍处于测试阶段的 macOS 27.2，但触屏的具体用途及软件兼容性仍待官方说明。

**「生态与购机成本影响」** 若发布传闻属实，潜在用户将获得键盘和触控板之外的 OLED 触控交互，但高于现行 2,499 美元起售价的定价会提高购机成本，开发者也需为灵动岛带来的 macOS 界面变化预留适配工作。具体触控兼容要求仍待苹果官方说明。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.macrumors.com/2026/10/25/macbook-pro-with-touchscreen-on-wednesday/">Apple Reportedly Announcing MacBook Pro With OLED Touchscreen ...</a></li>
<li><a href="https://www.macrumors.com/2026/10/01/oled-macbook-pro-release-date/">MacBook Pro With OLED Touch Screen Rumored to Launch in ...</a></li>
<li><a href="https://www.bloomberg.com/news/articles/2026-02-24/apple-s-touch-screen-macbook-pro-to-have-dynamic-island-new-interface">Apple’s Touch-Screen Laptop to Have Dynamic Island, New Mac ...</a></li>
<li><a href="https://www.macworld.com/article/3070324/touchscreen-macbook-pro-to-feature-dynamic-island-and-big-macos-changes.html">Apple’s touchscreen MacBook Pro might get its own Dynamic Island</a></li>

</ul>
</details>

**标签**: `#苹果`, `#MacBook Pro`, `#触控屏`, `#OLED`, `#硬件`

---

<a id="item-tech-news-2"></a>
### [OpenAI 与 Anthropic 大幅下调 API 价格](https://minimaxir.com/2026/10/cheap-llms/) ⭐️ 7.0/10

文章称，OpenAI 与 Anthropic 在数月内将其大语言模型 API 价格下调最多 80%，但现有材料未列出具体模型、版本和调价表，无法独立核验降幅及适用范围。文章主要从模型服务竞争加剧、推理与硬件利用效率提升，以及边际服务成本下降等方面解释这一变化，认为它更像行业竞争和成本结构演进，而非模型能力的突破。降价可能降低开发者调用和迁移模型的成本，并提高推理算力的商业利用率，但能否持续仍取决于需求、GPU 供给、补贴方式及数据政策。关于具体定价、零数据保留或监管策略的判断，因原文内容缺失而仍待核实。

hackernews · minimaxir · 10月25日 21:11 · [社区讨论](https://news.ycombinator.com/item?id=50236102)

**「背景」** 大语言模型 API 通常按输入与输出 token、缓存读取等项目计费，因此降价既可能来自单位推理成本下降，也可能来自折扣或计费结构调整。相关报道将 OpenAI 和 Anthropic 自 2026 年 6 月以来最高约 80% 的降价置于提供商竞争、硬件利用率、批处理与缓存优化等推理经济因素之下。

**「对开发者的实际影响」** 对使用托管大模型 API 的开发者而言，OpenAI 和 Anthropic 最高达 80% 的降价会直接降低推理成本，并扩大在 Kimi、GLM 等更便宜模型之间切换的余地；一名用户还称替代模型减少了网络安全类请求被拒绝的情况。降价能否持续仍不明确，社区对需求、GPU 产能利用率、模型优化空间以及价格是否受补贴影响存在分歧。

**「社区讨论」** 评论者普遍将降价归因于竞争和推理成本下降；一位用户称，在 OpenAI 和 Anthropic 因“网络安全”提示阻断任务后，改用更便宜的 Kimi 与 GLM 模型顺利完成工作，说明价格与可用性会共同影响模型选择。也有人质疑降价背后的数据政策、零数据保留承诺、潜在补贴和监管动机，并以 DeepSeek Flash V4 的单 GPU 收入估算说明成本优化空间；另有观点认为需求有限和 GPU 固定容量带来的利用率压力会推动价格继续下降，这些数字与推断均未在原文中得到验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://minimaxir.com/2026/10/cheap-llms/">OpenAI and Anthropic cut their LLM prices by up to 80% within ...</a></li>
<li><a href="https://daily.dev/posts/openai-and-anthropic-cut-their-llm-prices-by-up-to-80-within-a-few-months-why--qwjt9m0rl">OpenAI and Anthropic cut their LLM prices by up to 80%...</a></li>

</ul>
</details>

**标签**: `#large-language-models`, `#inference-economics`, `#api-pricing`, `#openai`, `#anthropic`

---

<a id="item-tech-news-3"></a>
### [Nanbeige 4.3-33B 发布为 Apache 2.0 教师模型](https://www.reddit.com/r/MachineLearning/comments/1xf6x35/nanbeige_releases_nanbeige4333b_an_apache_20/) ⭐️ 7.0/10

Nanbeige 发布 Nanbeige4.3-33B，将其作为智能体任务及后续更小型模型（包括计划中的 3B 版本）的教师模型；模型权重采用 Apache 2.0 许可证，模型卡标注支持 512K 上下文窗口。发布团队的评测显示，Nanbeige4.3-33B 在 Terminal-Bench 2.1 上得分 80.9，高于 Qwen3.8-27B 的 73.0，两者在该项基准中使用相同的评测框架和推理设置。其表现并非全面领先，团队报告的 SWE-Bench Pro 得分为 60.3，低于 Qwen3.8-27B 的 61.7。上述成绩均为发布方自报，尚无独立复现；复现智能体评测时应固定 preserve\_thinking=true，因为模型卡建议多轮工具使用采用该设置、但一般聊天不采用，并同时比较任务成功率和生成令牌总量，而不应仅凭标题分数判断部署表现。

reddit · r/MachineLearning · /u/jatingargiitk · 10月25日 16:32

**「教师模型与蒸馏」** 模型蒸馏通常利用大型“教师模型”的输出或推理轨迹训练较小的“学生模型”，以较低部署成本迁移代理和工具调用能力；Nanbeige 计划以 33B 教师模型支持后续 3B 代理模型。Nanbeige4.3-33B 是采用 Apache 2.0 许可的 33B 稠密开放权重模型，提供 512K 上下文；其多轮工具调用评测使用 preserve\_thinking=true 来保留此前的推理内容，但该设置并非面向一般聊天的推荐默认值。

**「对智能体开发的影响」** 开发者现在可以在 Apache 2.0 许可下利用 Nanbeige4.3-33B，将这个支持 512K 上下文的 33B 教师模型作为包括后续 3B 模型在内的小型智能体蒸馏起点。其实际优势仍需独立验证：发布方的 Terminal-Bench 2.1 得分较高，但 SWE-Bench Pro 低于 Qwen3.8-27B，且评测依赖 preserve\_thinking=true 等特定设置。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://aicoder.com/news/news-20261025-nanbeige-4-3-33b-open-agentic-model">BOSS Zhipin&#x27;s Nanbeige lab open-sources Nanbeige4.3-33B, a ...</a></li>
<li><a href="https://www.datastudios.org/post/nanbeige-4-3-33b-open-weight-dense-agentic-model-512k-context">Nanbeige4.3-33B: Apache 2.0 dense agentic coding model with ...</a></li>
<li><a href="https://aiweekly.co/alerts/nanbeige-opens-33b-model-under-apache-20-with-512k-context">Nanbeige Opens 33B Model Under Apache 2.0 With 512K Context</a></li>
<li><a href="https://www.marktechpost.com/2026/10/25/nanbeige-releases-nanbeige4-3-33b-open-agentic-coding-model/">Nanbeige Releases Nanbeige 4 . 3 - 33 B , a 33 B Open... - MarkTechPost</a></li>
<li><a href="https://aiweekly.co/alerts/nanbeige-opens-33b-model-under-apache-20-with-512k-context">Nanbeige Opens 33 B Model Under Apache 2 . 0 With... | AI Weekly</a></li>

</ul>
</details>

**标签**: `#LLM agents`, `#open-source models`, `#model distillation`, `#benchmarking`

---

<a id="item-tech-news-4"></a>
### [iPhone Duo 拆解指向“裂屏门”潜在原因](https://www.theverge.com/tech/1018290/dissected-iphone-duo-crackgate-hinge-screen) ⭐️ 6.0/10

一名 YouTuber 拆解 iPhone Duo 后认为，设备的设计缺陷可能是近期“裂屏门”问题的原因。社交媒体和 iPhone Duo 社群中出现了大量故障报告，部分用户称手机仅使用数小时，铰链便像是卡住异物，随后传出明显的断裂声并导致屏幕破裂。这项拆解调查为相关故障提供了一个潜在解释，但现有原文内容被截断，未包含完整测试方法、具体证据或苹果方面的确认，因此尚不能视为已经证实的根本原因。

rss · The Verge · 10月25日 20:16

**「“裂纹门”调查背景」** 此前多名 iPhone Duo 用户报告，设备使用数小时后，铰链似乎夹住异物并伴随明显声响，随后屏幕在同一位置出现裂纹。YouTuber CuriousHagi 在耐久性测试中复现了开裂现象，并通过拆解设备寻找可能原因；这些结果用于提出设计缺陷假说，并不等同于苹果已确认存在硬件缺陷。

**「早期耐用性风险」** 已有 iPhone Duo 早期用户报告内屏在购机后数小时内出现铰链附近纵向裂纹、亮线或坏点，个别设备甚至在开启不足 20 次后损坏，令这款 1,999 美元折叠机面临现实的耐用性风险，但拆解提出的设计缺陷与事故之间的因果关系尚未得到确认。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theverge.com/tech/1018290/dissected-iphone-duo-crackgate-hinge-screen">A YouTuber dissected an iPhone Duo and thinks he... | The Verge</a></li>
<li><a href="https://www.notebookcheck.net/Apple-s-2-000-foldable-iPhone-reportedly-cracks-within-hours-as-owners-report-display-failures.1432971.0.html">Apple&#x27;s $2,000 foldable iPhone reportedly cracks within hours as...</a></li>
<li><a href="https://www.thenationalnews.com/future/technology/2026/10/25/apples-iphone-duo-faces-screen-damage-complaints-as-first-buyers-report-cracks/">iPhone Duo buyers complain of cracks and display failures after just...</a></li>
<li><a href="https://www.macrumors.com/2026/10/23/iphone-duo-screen-cracks/">Crackgate ? iPhone Duo Owners Report Screens... - MacRumors</a></li>

</ul>
</details>

**标签**: `#Apple`, `#foldable smartphones`, `#hardware reliability`, `#teardown analysis`

---

<a id="item-tech-news-5"></a>
### [r/opensource 禁止 AI 项目并收紧投稿规则](https://www.theverge.com/ai-artificial-intelligence/1018217/reddit-opensource-ai-ban) ⭐️ 6.0/10

r/opensource 管理员发布新的投稿规则，明确表示：如果项目使用 AI、由 AI 生成或旨在服务 AI，就不允许在该社区发布。管理员称，就当前发展状况而言，AI 与该社区所认同的开放源代码理念不相容。此次更新还增加了其他限制，其中包括针对非英语发言者的限制，但现有材料没有完整说明具体条件或执行方式。该变更目前仅适用于 r/opensource，没有证据表明 Reddit 整体或更广泛的开源生态也禁止了 AI 相关项目。

rss · The Verge · 10月25日 13:25

**「背景」** r/opensource 是 Reddit 上围绕开源项目与理念建立的社区，其版主规则用于决定该子版块接受哪些投稿以及如何审核。此次调整属于单个子版块的社区治理决定，并不等同于 Reddit 全站政策，也不能直接理解为所有开源项目都被禁止使用 AI。

**「影响范围」** 使用 AI、由 AI 生成或面向 AI 的项目将无法再向 r/opensource 投稿，非英语发言者则需要遵守新增限制。其直接影响集中在该 subreddit 的审核和投稿流程，并不代表整个开源领域统一禁止 AI。

**标签**: `#open source`, `#AI policy`, `#Reddit`, `#community governance`

---