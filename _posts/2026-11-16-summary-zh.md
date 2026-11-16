---
layout: default
title: "Horizon Summary: 2026-11-16 (ZH)"
date: 2026-11-16
lang: zh
---

> 从 75 条内容中筛选出 12 条重要资讯。

---

**科技新闻**
1. [Qwen4-Max 发布：稀疏 MoE 与百万 Token 上下文](#item-tech-news-1) ⭐️ 8.0/10
2. [多模态视觉编码器预训练可省，视觉专属参数不可少](#item-tech-news-2) ⭐️ 8.0/10
3. [美团开源 LongCat-2.5 智能体模型](#item-tech-news-3) ⭐️ 8.0/10
4. [Vulcan rocket fails during launch, dealing major blow to SpaceX competitors](#item-tech-news-4) ⭐️ 7.0/10
5. [国会拟因间谍案收紧 AI 芯片出口](#item-tech-news-5) ⭐️ 7.0/10
6. [Datasette 0.65.6 回移植访问控制修复](#item-tech-news-6) ⭐️ 6.0/10
7. [苹果智能眼镜进入组装阶段](#item-tech-news-7) ⭐️ 6.0/10
8. [Bharat Semi 获 2400 万美元种子轮融资](#item-tech-news-8) ⭐️ 6.0/10
9. [微软 Azure 印度涨价、中国降成本](#item-tech-news-9) ⭐️ 6.0/10
10. [标准模型晶格定义迈出新一步](#item-tech-news-10) ⭐️ 6.0/10

**财经新闻**
1. [China’s slowdown deepens in October as industrial output, retail sales, investment miss estimates](#item-finance-news-1) ⭐️ 8.0/10
2. [黄仁勋辞职加剧对卢特尼克与英伟达关系的审查](#item-finance-news-2) ⭐️ 8.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Qwen4-Max 发布：稀疏 MoE 与百万 Token 上下文](https://qwen.ai/blog?id=qwen4-max) ⭐️ 8.0/10

据随附发布说明，阿里通义千问已推出旗舰模型 Qwen4-Max，采用稀疏 MoE 架构，总参数量达到 2.4 万亿，并原生支持视觉理解和百万 Token 长上下文。模型重点面向编程、办公和长程任务，Code Arena 盲测成绩被描述为位居全球前列，同时支持 none、low、high、xhigh 四档推理强度。其单任务平均费用据称从上代的人民币 26.58 元降至 11.16 元，降幅接近 58%，Token 消耗也减少近 50%，API 定价同步下调；团队表示后续还将发布更小的 Qwen4 系列模型并开放模型权重。

hackernews · ilreb · 11月16日 02:14 · [社区讨论](https://news.ycombinator.com/item?id=50513215)

**「背景」** Qwen4-Max 是阿里通义千问 Qwen 4 系列的旗舰模型，定位为多模态推理模型，可接收文本、图像和视频输入并输出文本，默认启用推理；不同服务目录给出的上下文容量约为 98.4 万至 100 万 Token。相比社区讨论中提到的 Qwen 3.8 Max，Qwen4-Max 的评估重点是模型质量、可调推理强度、推理速度与任务成本之间的权衡。

**「对用户的实际影响」** ... 

**「社区反馈」** 社区关注其质量、成本与推理速度之间的权衡：有人援引 Artificial Analysis 称 Qwen4-Max 得分 43、平均成本 3.27 美元，并将其与平均成本 0.36 美元的 GPT-6.1 Sol（medium）对比。实践者反映 Qwen3.8 虽在排除投票机制后表现良好，但约 30 Token/秒的速度明显低于接近 80 Token/秒的 Opus，成为代理系统中的主要短板；评论者同时期待 Flash、27B 等更小版本及开放权重。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://artificialanalysis.ai/models/qwen4-max">Qwen 4 Max - Intelligence, Performance &amp; Price ... | Artificial Analysis</a></li>
<li><a href="https://openrouter.ai/qwen/qwen4-max">Qwen 4 Max - API Pricing &amp; Providers | OpenRouter</a></li>
<li><a href="https://www.qwencloud.com/models/qwen4-max?region=ap-southeast-1">Qwen 4 - Max - QwenCloud</a></li>
<li><a href="https://artificialanalysis.ai/models/qwen4-max">Qwen 4 Max - Intelligence, Performance &amp; Price... | Artificial Analysis</a></li>

</ul>
</details>

**标签**: `#large-language-models`, `#Qwen`, `#model-evaluation`, `#reasoning`, `#AI-infrastructure`

---

<a id="item-tech-news-2"></a>
### [多模态视觉编码器预训练可省，视觉专属参数不可少](https://www.reddit.com/r/MachineLearning/comments/1xx1k2o/meta_fair_nyu_unbundling_multimodal_vision/) ⭐️ 8.0/10

Meta FAIR 与纽约大学研究人员从头训练了 200 多个多模态模型，在相同数据和生命周期算力预算下，分别检验视觉编码器预训练、仅供视觉 token 使用的参数以及编码器相对 LLM 的位置三项设计选择。主要实验比较了采用 0.4B 视觉容量的 Qwen3-1.7B 和 4B 配置，并将骨干扩展至 0.6B 至 6.4B，在 Cambrian 的 16 个 VQA 基准（448 px）和 12 个语言基准上进行评估。研究报告称，视觉编码器单独预训练并非必要：对比学习、自监督及两种字幕式预训练在匹配算力下最多只能与随多模态训练从零开始的编码器打平；即使将 MetaCLIP 预训练时长增至 6.5 倍，使 ImageNet 线性探测准确率从 80.4% 升至 84.4%，也未带来 VQA 增益。相反，专属视觉参数至关重要：完全无编码器的模型在各规模均落后，需要约 3 倍算力才能追上，而把原编码器参数改由文本 token 使用虽能改善文本表现，却不能改善 VQA。编码器位置也可替换，“in-fusion”方案仅在前 8 层加入由视觉 token 独占的零初始化注意力投影和 FFN，1.7B 配置的 VQA 得分达到 45.0，高于编码器方案的 44.4 和末 8 层方案的 35.1，并在 1.7B 至 6.4B 规模间与编码器相当，首 token 延迟约低 13%；不过，这些结果目前主要来自研究作者发布的 Reddit 帖子所述研究，尚缺独立验证。

reddit · r/MachineLearning · /u/trungh98 · 11月15日 17:38

**「研究背景」** 当前多模态语言模型通常使用预训练视觉编码器将图像转换为视觉令牌，再将其输入大语言模型；近期一些方案则从头训练编码器或完全移除独立编码器，因此视觉编码器的使用方式仍存在争议。该研究将传统视觉编码器包含的三项设计选择分别拆解：上游预训练提供的视觉先验、仅供视觉令牌使用的专用参数，以及视觉容量在语言模型融合前的位置。

**「对 MLLM 设计的直接影响」** 对 MLLM 开发者而言，在相同计算预算下可以放弃单独的视觉编码器预训练，但应继续为视觉 token 保留专用参数，因为完全取消这些参数约需 3 倍计算才能追平。该结论目前主要基于 Qwen3 的受控配置及 0.6B—6.4B 模型扩展实验，尚不能直接外推到所有架构和训练配方。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2611.17334">[2611.17334] Unbundling Multimodal Vision Encoding - arXiv.org</a></li>
<li><a href="https://arxiv.org/pdf/2611.17334v1">Unbundling Multimodal Vision Encoding - arXiv.org</a></li>
<li><a href="https://arxiv.org/pdf/2611.17334v1">Unbundling Multimodal Vision Encoding - arXiv.org</a></li>

</ul>
</details>

**标签**: `#multimodal-language-models`, `#vision-encoders`, `#model-training`, `#ablation-studies`, `#AI-research`

---

<a id="item-tech-news-3"></a>
### [美团开源 LongCat-2.5 智能体模型](https://the-decoder.com/meituan-releases-a-1-6-trillion-parameter-agent-model-that-never-touched-an-nvidia-gpu/) ⭐️ 8.0/10

美团 LongCat 团队在正式发布一周后开源了 LongCat-2.5 权重，该模型面向自主执行长时间、多步骤任务，尤其是编程任务，总参数量达 1.6 万亿，每个 token 激活约 480 亿参数。团队称模型训练全程使用华为升腾加速卡，未使用英伟达 GPU，并支持文本、图像和视频输入。模型权重采用允许商业使用的 MIT 许可证发布；在 Terminal Bench v2.1 上，官方报告其得分为 88.4，略低于 Claude Opus 5 的 89.1，但目前尚缺乏独立验证。

telegram · zaihuapd · 11月15日 11:08

**「背景」** LongCat-2.5 是美团 LongCat 团队面向长时程智能体和仓库级编程任务推出的原生多模态模型，采用 1.6 万亿总参数、每个 token 激活约 480 亿参数的稀疏架构，可处理文本、图像和视频，并支持约 100 万 token 的上下文。此类模型侧重让智能体自主规划并连续完成冗长的多步骤工作，而不是仅处理单轮问答；LongCat-2.5 的官方测试也以 Terminal-Bench v2.1 衡量其编程智能体能力。

**「实际影响」** LongCat-2.5 以 MIT 许可开放权重，使开发者和企业能够将这一 1.6 万亿总参数、每 token 激活约 480 亿参数的模型用于商业部署和二次开发；官方评测显示其在 Terminal Bench v2.1 上得分 88.4，接近 Claude Opus 5 的 89.1。受英伟达采购限制的组织因此获得了可评估的非英伟达训练方案，但现有信息仅能说明训练硬件，不能推断其推理阶段也可完全不使用英伟达 GPU。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://lmspeed.net/model/longcat-2-5">LongCat - 2 . 5 API Pricing &amp; Benchmarks | LMSpeed</a></li>
<li><a href="https://sumus.im/blog/longcat-2-5">LongCat 2 . 5 : Meituan &#x27;s AI Model , Benchmarks, Price &amp; API | Sumus</a></li>
<li><a href="https://www.longcatai.org/benchmarks/longcat-2-5">LongCat-2.5 Benchmarks - Full 33-Task Evaluation vs GPT-5.6 ...</a></li>
<li><a href="https://www.longcatai.org/benchmarks/">Benchmarks - LongCat-2.5, LongCat-2.0, LongCat AI Performance</a></li>
<li><a href="https://agentspulse.github.io/tutorials/longcat-2-5/">LongCat 2.5: Benchmarks, Pricing and Claude Code Setup ...</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#open-source models`, `#Huawei Ascend`, `#multimodal AI`, `#programming benchmarks`

---

<a id="item-tech-news-4"></a>
### [Vulcan rocket fails during launch, dealing major blow to SpaceX competitors](https://arstechnica.com/space/2026/11/vulcan-rocket-fails-during-launch-dealing-major-blow-to-spacex-competitors/) ⭐️ 7.0/10

ULA&\#x27;s Vulcan rocket and 40 Amazon Leo broadband satellites fell back to Earth shortly after liftoff, with an indefinite grounding and industry-wide consequences expected.

rss · Ars Technica · 11月15日 23:11

**标签**: `#Vulcan`, `#launch failure`, `#Amazon Leo`, `#satellite broadband`, `#space industry`

---

<a id="item-tech-news-5"></a>
### [国会拟因间谍案收紧 AI 芯片出口](https://www.theverge.com/ai-artificial-intelligence/1033984/congress-export-rules-ai-chips-china) ⭐️ 7.0/10

美国国会正考虑进一步收紧 AI 芯片出口限制，背景是英伟达 CEO 黄仁勋卷入一宗涉嫌中国间谍的案件。民主党与共和党议员均对多项限制措施和法案表达支持，并要求黄仁勋及其他英伟达高管赴国会作证。新规可能影响英伟达、半导体供应链及依赖受限芯片的全球 AI 部署，但现有报道未披露具体法案、适用芯片、豁免条件或实施时间，因此政策范围与合规影响尚不明确。

rss · The Verge · 11月15日 19:15

**「背景」** 美国通过出口管制和许可制度限制先进 AI 芯片流向特定国家或客户；此次国会讨论是在这一框架下进一步收紧销售规则，并要求英伟达高管作证。相关风波源于对前英伟达 CEO 黄仁勋与一名疑似中国间谍之间联系的调查，目前仍属指控；英伟达管理层已同意赴国会作证，但尚未确定日期。

**「潜在影响」** 若出口限制最终落地，中国 AI 实验室、云服务商和数据中心获取英伟达先进 AI 芯片的渠道可能受限，并可能促使相关厂商加快采用国产替代方案。现有信息仅显示两党议员正在讨论多项措施，具体法案、许可范围及实施时间尚未明确。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bbc.com/news/articles/cmdx1vpprk9vo">Suspected China spy linked to Nvidia &#x27;s ex-boss left in 2025...</a></li>
<li><a href="https://www.theguardian.com/technology/2026/nov/16/elon-musk-tech-execs-open-letter-jensen-huang-return-nvidia-ceo">Elon Musk joins 158,000 others calling for Nvidia to bring back Jensen ...</a></li>
<li><a href="https://www.longtermwiki.com/wiki/E2054">AI Chip Governance Supply Chain | Longterm Wiki</a></li>
<li><a href="https://www.globaltimes.cn/page/202611/1374231.shtml">SMIC’s Q3 net profit more than doubles as domestic... - Global Times</a></li>
<li><a href="https://www.bbc.com/news/articles/cmdx1vpprk9vo">Suspected China spy linked to Nvidia &#x27;s ex-boss left in 2025...</a></li>

</ul>
</details>

**标签**: `#AI chips`, `#export controls`, `#US Congress`, `#Nvidia`, `#semiconductor policy`

---

<a id="item-tech-news-6"></a>
### [Datasette 0.65.6 回移植访问控制修复](https://simonwillison.net/2026/Nov/15/datasette-2/) ⭐️ 6.0/10

Datasette 0.65.6 是一项维护性安全更新，将 1.0a43 中的一项小型安全修复回移植到 0.65 系列。问题出现在通过 \`add\_database\(db, name=..., route=...\)\` 注册数据库且 \`route\` 与 \`name\` 不同时：已被拒绝访问该数据库的用户仍可能从 \`/&lt;route&gt;.db\` 下载数据库。0.65.6 修复了这种访问控制绕过行为。

rss · Simon Willison · 11月15日 23:18

**「相关机制」** Datasette 允许开发者为数据库设置独立于内部名称的自定义路由，并以该路由生成数据库下载地址。因此，在 \`name\` 与 \`route\` 不一致的配置中，权限检查必须覆盖 \`/&lt;route&gt;.db\` 这一下载入口。

**「升级建议」** 使用自定义路由注册数据库的 Datasette 部署者应升级到 0.65.6，以避免被拒绝访问的用户仍能下载数据库。

**标签**: `#Datasette`, `#Security patch`, `#Access control`, `#Release notes`

---

<a id="item-tech-news-7"></a>
### [苹果智能眼镜进入组装阶段](https://www.theverge.com/tech/1033968/apples-first-smart-glasses-are-coming-together) ⭐️ 6.0/10

据 Bloomberg 的 Mark Gurman，苹果首款智能眼镜已推进至组装阶段，可能在明年 6 月的 WWDC 上亮相，但不会立即出货，首代也没有 AR 显示功能。转述称产品内部代号为 N50，主打 Siri 与 iPhone 应用的深度整合，需要配对较新的 iPhone，不支持 Android，第三方应用仍将在手机上运行。其原型据称略薄于 Meta 第二代 Ray-Ban，采用三针磁吸充电并支持佩戴时充电，但软件与 AI 开发进度落后，存在延期可能。材料中的时间信息并不一致：一处称预计在 2025 年底前开始出货，另一处则称目标为 2027 年发布并在当年年底出货，因此相关规格和节点均属于未经苹果确认的预测。

rss · The Verge · 11月15日 16:59

**「背景」** 苹果目前的智能眼镜路线并非首代即提供增强现实显示，而是以 Siri 和 iPhone 应用联动为核心，相关功能仍主要由配对的手机运行。彭博社记者 Mark Gurman 称，苹果正瞄准在 2027 年 6 月的 WWDC 上公布内部代号为 N50 的首款眼镜，并于 2027 年底前开始出货，但这一时间表尚未得到苹果正式确认。

**「用户影响」** 如果这一传闻最终落地，首批用户将获得一副不带 AR 显示、需配对较新 iPhone 的配件，主要提供 Siri 与手机应用交互；它不支持 Android，也无法满足期待增强现实显示的用户。由于苹果尚未正式确认 N50 的发布时间和能力，且软件与 AI 进度可能继续导致延期，从现有信息看，这款眼镜将是 iPhone 的延伸，而非独立计算平台。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.macrumors.com/2026/11/15/apple-smart-glasses-hinge-on-siri/">Apple&#x27;s Smart Glasses Strategy Hinges on Siri and iPhone ...</a></li>
<li><a href="https://www.bloomberg.com/news/newsletters/2026-07-26/apple-glasses-may-debut-at-wwdc-2027-privacy-camera-features-versus-meta-ms1v7lta">Apple Glasses May Debut at WWDC 2027: Privacy, Camera ...</a></li>
<li><a href="https://vr.org/articles/apple-smart-glasses-wwdc-2027-privacy-camera-decision-2026">Gurman Puts Apple&#x27;s First Smart Glasses at WWDC 2027, and the ...</a></li>

</ul>
</details>

**标签**: `#smart glasses`, `#Apple`, `#wearables`, `#hardware rumors`, `#WWDC`

---

<a id="item-tech-news-8"></a>
### [Bharat Semi 获 2400 万美元种子轮融资](https://techcrunch.com/2026/11/15/indian-chip-startup-bharat-semi-lands-24m-seed-round-as-it-eyes-global-ai-sensor-market/) ⭐️ 6.0/10

印度芯片初创公司 Bharat Semi 已完成 2400 万美元种子轮融资，并将目标指向全球 AI 传感器市场。Bharat Semi 表示，其 AI 传感器技术已获得包括 General Atomics 在内公司的设计导入，为早期商业化提供了客户验证和扩张资源。不过，现有信息未披露投资方、传感器规格、量产计划或收入规模，因此这些设计导入能否转化为批量出货和持续营收仍不确定。

rss · TechCrunch · 11月15日 23:30

**「背景」** “设计赢单”通常表示客户选择某家芯片或传感器供应商参与产品开发，但不代表相关产品已经进入量产。General Atomics 正推进 Ranger 和 GA-Ray 两款远程水下无人机，这些平台采用模块化开放架构，可配置不同任务载荷、自主软件以及声学和量子传感器；现有来源尚未说明 Bharat Semi 的 AI 传感器具体应用于哪些平台。

**「潜在产业影响」** Bharat Semi 获得 2400 万美元种子轮融资并取得包括 General Atomics 在内的设计胜出，将为其 AI 传感器研发和商业化提供资金与早期客户验证，并可能加快相关技术进入 General Atomics 覆盖的国防、无人航空和雷达/光电系统；但“设计胜出”并不等于量产订单，公司仍处早期阶段，实际规模化影响尚不确定。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.thedefensenews.com/General-Atomics-Unveils-Two-Long-Range-Underwater-Drones-Ranger-and-GA-Ray-at-Euronaval-2026/">General Atomics Unveils Two Long-Range Underwater Drones...</a></li>
<li><a href="https://www.ga.com/">Welcome to General Atomics | General Atomics</a></li>
<li><a href="https://www.ga-asi.com/">Welcome to General Atomics Aeronautical Systems (GA-ASI)</a></li>

</ul>
</details>

**标签**: `#semiconductors`, `#AI sensors`, `#startup funding`, `#India`

---

<a id="item-tech-news-9"></a>
### [微软 Azure 印度涨价、中国降成本](https://www.theregister.com/off-prem/2026/11/15/microsoft-lifts-indian-cloud-prices-by-15-percent-cuts-costs-in-china/5309993) ⭐️ 6.0/10

据报道，微软将印度市场的 Azure 云服务价格上涨 15%，同时降低中国市场的云服务成本。这一调整令 Azure 在两个市场呈现相反的成本走势，印度客户将面对更高报价，而中国客户可能受益于成本下降。现有材料未说明受影响的具体 Azure 产品、中国市场的降幅、生效日期或现有合同如何处理，实际影响仍需以当地公布的定价细节为准。

rss · The Register · 11月15日 23:46

**「区域定价机制背景」** 微软 Azure 的商业云服务价格会因地区和结算币种而异，公司也会定期调整当地货币标价，使其与全球价格水平保持一致。从 2027 年 1 月 1 日生效的调整是新年度调价机制的首轮，覆盖五种货币；印度部分服务因此涨价，而中国部分服务降价，最高降幅约为 8.5%。

**「云客户成本影响」** 据报道，微软将印度云服务价格上调 15%，受影响 Azure 客户的同量使用成本和预算基准将随之上升，而中国客户可从降价中获得直接成本收益；由于材料未列明具体服务、区域与生效日期，实际账单影响仍需按地区和服务核算。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theregister.com/off-prem/2026/11/15/microsoft-lifts-indian-cloud-prices-by-15-percent-cuts-costs-in-china/5309993">Microsoft lifts Indian cloud prices by 15 percent, cuts costs ...</a></li>
<li><a href="https://tbreak.com/microsoft-commercial-cloud-pricing-currency-2027/">Microsoft commercial cloud pricing rises 15.7% in India</a></li>
<li><a href="https://opsiocloud.com/in/blogs/cloud-pricing-comparison-india-2026/">Cloud Pricing India 2026: AWS vs Azure vs GCP in INR</a></li>
<li><a href="https://learn.microsoft.com/en-us/answers/questions/6025662/is-there-any-official-announcement-for-azure-vm-in">Is There any official announcement for Azure VM (in 7 regions ...</a></li>

</ul>
</details>

**标签**: `#Microsoft Azure`, `#cloud pricing`, `#India`, `#China`

---

<a id="item-tech-news-10"></a>
### [标准模型晶格定义迈出新一步](https://openai.com/index/step-toward-defining-the-standard-model) ⭐️ 6.0/10

OpenAI 介绍了一项候选性的标准模型非微扰晶格定义，并称 GPT-6 Astra 参与了将这一构想发展为详细证明的过程。若该成果经得住审查，它将为标准模型提供一种以离散晶格而非微扰展开为核心的定义路径，因而可能具有重要科学意义。现有条目未披露证明采用的方法、关键假设、验证步骤、论文或预印本信息，也没有提供独立复核。报道由 OpenAI 发布，因此目前应视为一项研究进展声明，其科学影响以及 GPT-6 Astra 的具体贡献尚无法独立确认。

rss · OpenAI News · 11月15日 22:00

**「晶格定义的研究背景」** 标准模型描述基本粒子及其基本相互作用；“晶格定义”是把连续时空离散化，以便通过数值方法研究量子场论，而非依赖微扰展开的近似计算。现有材料将这项工作称为标准模型的候选非微扰晶格定义，并称 GPT-6 Astra 协助形成了详细证明，但这并不意味着该结果已经得到独立验证或成为最终确立的理论。

**「潜在影响」** 对从事格点场论与标准模型数值计算的物理学家而言，若这一候选的非微扰格点定义能够通过同行评审与数值验证，将为标准模型提供不依赖微扰展开的规范基址，使格点方法以更少假设计算标准模型现象成为可能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/step-toward-defining-the-standard-model/">A step toward defining the Standard Model on a lattice - OpenAI</a></li>
<li><a href="https://grafy.ai/news/openai-unveils-lattice-based-standard-model-proof-with-gpt-6-astra">OpenAI unveils lattice‑based Standard Model — Grafy News</a></li>
<li><a href="https://thedefiant.io/frontier/ai/openai-details-astra-s-role-in-standard-model-lattice-proof">OpenAI Details Astra&#x27;s Role in Standard Model Lattice Proof</a></li>
<li><a href="https://openai.com/index/step-toward-defining-the-standard-model/">A step toward defining the Standard Model on a lattice | OpenAI</a></li>

</ul>
</details>

**标签**: `#lattice field theory`, `#Standard Model`, `#AI-assisted research`, `#scientific computing`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [China’s slowdown deepens in October as industrial output, retail sales, investment miss estimates](https://www.cnbc.com/2026/11/16/china-retail-sales-october-industrial-output-investment.html) ⭐️ 8.0/10

China&\#x27;s October data confirmed a broad domestic slowdown as weak consumption and collapsing investment outweighed strong exports, raising risks to global growth and intensifying trade tensions.

rss · CNBC Finance · 11月16日 03:53

**标签**: `#China`, `#Economic Data`, `#Domestic Demand`, `#Trade Surplus`, `#Global Growth`

---

<a id="item-finance-news-2"></a>
### [黄仁勋辞职加剧对卢特尼克与英伟达关系的审查](https://www.cnbc.com/2026/11/13/howard-lutnick-nvidia-jensen-huang-china-cantor-fitzgerald.html) ⭐️ 8.0/10

英伟达首席执行官黄仁勋辞职后，美国商务部长霍华德·卢特尼克因家族掌控的坎特·菲茨杰拉德与英伟达的关系而面临新的审查；该投行披露的英伟达持股数量在 2025 年 9 月至 2026 年 3 月间下降 49%，但目前没有证据表明这一变化与情报警告有关或涉及内幕交易。

rss · CNBC Finance · 11月15日 19:58

**「背景」** 商务部长霍华德·卢特尼克于 2025 年 2 月离开其曾管理的华尔街公司 Cantor Fitzgerald，该公司现由其子布兰登和凯尔领导。美国商务部负责“实体清单”，可将受限制的境外实体加入名单并限制美国与其贸易，因此卢特尼克对英伟达芯片出口政策的决定受到关注。

**「影响」** 英伟达面向中国的先进 AI 芯片出口许可将面临更具体的国会审查：卢特尼克已获安排在参议院银行委员会作证，讨论商务部在放行相关芯片中的角色，Megaspeed 等涉嫌绕过出口限制的企业也将继续受到监管关注；现有证据并未证明存在利益冲突、内幕交易或不当出口许可。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Howard_Lutnick">Howard Lutnick - Wikipedia</a></li>
<li><a href="https://www.bbc.com/news/articles/cmdx1vpprk9vo">Suspected China spy linked to Nvidia &#x27;s ex-boss left in 2025...</a></li>
<li><a href="https://www.tomshardware.com/tech-industry/artificial-intelligence/billions-worth-of-export-restricted-ai-accelerators-sold-to-china-report-details-how-chinese-firms-skirt-trumps-regulations">Investigative report details how export - restricted Nvidia AI chips ...</a></li>
<li><a href="https://www.cnbc.com/2026/11/12/nvidia-megaspeed-alice-huang-jensen-.html">What we know so far about Nvidia partner Megaspeed ’s Asia footprint</a></li>
<li><a href="https://www.bbc.com/news/articles/cmdx1vpprk9vo">Suspected China spy linked to Nvidia &#x27;s ex-boss left in 2025...</a></li>

</ul>
</details>

**标签**: `#Nvidia`, `#AI chip export controls`, `#China`, `#government ethics`, `#Cantor Fitzgerald`

---