---
layout: default
title: "Horizon Summary: 2026-11-23 (ZH)"
date: 2026-11-23
lang: zh
---

> 从 63 条内容中筛选出 8 条重要资讯。

---

**科技新闻**
1. [困惑度能否成为智能的衡量指标](#item-tech-news-1) ⭐️ 8.0/10
2. [蚂蚁集团领投中国具身智能公司 1 亿美元，估值 16 亿美元](#item-tech-news-2) ⭐️ 7.0/10
3. [重大科技服务中断或仍将持续](#item-tech-news-3) ⭐️ 6.0/10
4. [Notable Capital 等机构重仓 Anthropic 的逻辑](#item-tech-news-4) ⭐️ 6.0/10
5. [低价 GPT-5.1 令牌被用于寻找绕过中国防火墙的新方法](#item-tech-news-5) ⭐️ 6.0/10
6. [数字化汽车每年增加 120 亿美元美国维修成本](#item-tech-news-6) ⭐️ 6.0/10

**科技博客**
1. [不确定时，以多种尝试寻找反馈](#item-tech-blog-1) ⭐️ 7.0/10

**财经新闻**
1. [美股科技股大跌，亚洲多地调整交易与稳定措施](#item-finance-news-1) ⭐️ 8.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [困惑度能否成为智能的衡量指标](https://openai.com/index/perplexity-and-intelligence/) ⭐️ 8.0/10

OpenAI 的文章《Perplexity and Intelligence》提出，模型在预测性基准上的困惑度持续下降，与其智能水平提升相对应，因而困惑度可能成为衡量先进 AI 的一种简洁指标。困惑度衡量模型预测下一个词元时的意外程度，数值越低通常表示预测越准确；但文章未明确定义这一概念，相关发现也尚缺少独立验证，因此目前更适合作为有待检验的关联，而非已经确立的智能度量。

hackernews · acossta · 11月22日 17:06 · [社区讨论](https://news.ycombinator.com/item?id=50601525)

**「困惑度与智能评估」** 困惑度（perplexity）衡量预训练语言模型对序列中下一个词元预测的不确定性：数值越低，模型在给定前文后对实际词元的预测越自信、整体预测表现通常越好；它本质上反映下一词元预测这一预训练任务，而不是直接等同于通用智能。OpenAI 将这一指标的历史变化与模型能力联系起来，例如指出 GPT‑2 在较早数据集上刷新困惑度纪录时，已能较稳定地组织连贯段落。当前争论的关键在于，持续降低同一留出评测集上的困惑度能否作为“预测—压缩”能力及智能进步的可靠代理指标，而非仅证明模型更善于拟合语言统计规律。

**「实际影响」** 困惑度可成为衡量基础模型预训练进展的简洁横向指标：OpenAI 称 GPT‑3.5 在其主评估集上的对数困惑度约为 0.99，并已能流畅对话及支撑原版 ChatGPT。但 Hacker News 讨论中有人指出，GPT‑4 与 o3 的困惑度相近却存在显著的推理能力差距，因此该指标只能作为补充信号，不能替代针对推理和任务表现的独立评测。

**「社区讨论」** 评论者既认为这种对应关系令人惊讶且具有吸引力，也指出文章没有定义困惑度；有人将其解释为模型从海量原始数据中构建世界模型并通过预测实现压缩的能力，且与一篇 2008 年论文相呼应。部分评论者不确定 GPT-4.5、o1 等模型在趋势中的位置，并转述 Mustafa Suleyman 称 Microsoft 将在共同留出评测集上报告 MAI 模型，其中 MAI-2 Base 的 log-perplexity 为 0.819，但所给材料未包含对此的独立验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/perplexity-and-intelligence/">Perplexity and Intelligence | OpenAI</a></li>
<li><a href="https://news.ycombinator.com/item?id=50601525">Perplexity and Intelligence | Hacker News</a></li>
<li><a href="https://openai.com/index/perplexity-and-intelligence/">Perplexity and Intelligence | OpenAI</a></li>
<li><a href="https://news.ycombinator.com/item?id=50601525">Perplexity and Intelligence | Hacker News</a></li>

</ul>
</details>

**标签**: `#language-model-evaluation`, `#perplexity`, `#AI-research`, `#machine-learning`, `#AI-benchmarks`

---

<a id="item-tech-news-2"></a>
### [蚂蚁集团领投中国具身智能公司 1 亿美元，估值 16 亿美元](https://www.bloomberg.com/news/articles/2026-11-22/ant-group-bets-on-simplexity-to-thrive-in-china-s-humanoid-race) ⭐️ 7.0/10

Ant Group led a $100 million pre-A financing for Simplexity Robotics, valuing the humanoid-robotics startup at $1.6 billion.

telegram · zaihuapd · 11月23日 02:02

**标签**: `#embodied AI`, `#humanoid robotics`, `#venture funding`, `#China`

---

<a id="item-tech-news-3"></a>
### [重大科技服务中断或仍将持续](https://www.theverge.com/tech/1039851/major-tech-outages) ⭐️ 6.0/10

近期美国接连发生全国性的 FAA 航空管制暂停、持续数天并导致多家企业运营受阻的 Microsoft Outlook 中断，以及 JPMorgan Chase 银行系统故障。航空、企业软件和金融服务的连续异常表明，大型技术基础设施仍存在明显韧性缺口。尽管文章援引观点认为此类中断尚未结束、后续可能继续发生，但现有内容没有提供根因分析或足够证据来验证这一预测。

rss · The Verge · 11月22日 22:48

**「近期重大技术中断的背景」** 本文所讨论的背景，是美国近期接连发生全国性航空管制暂停、持续数日的微软 Outlook 服务中断，以及摩根大通银行系统故障，这些事件分别影响了航空、企业办公和金融服务的运行。美国官员将未来可能出现的更多中断与政府机构和企业更换老化系统联系起来，同时强调近期事件并不意味着它们彼此存在关联。

**「影响」** 这轮全国性中断已产生可观测的实际后果：FAA 通信问题导致超过四小时的全国航班地面停飞，Microsoft 365/Outlook 故障持续整天并让企业运营停摆，JPMorgan Chase 交易和 Apple 服务也同时受扰，公众则出现囤购应急物资的焦虑行为；安全研究人员还指出，AI 正在加速漏洞发现，使各组织面临更快的补丁修复压力。需要限定的是，文章关于“还会有更多中断”的判断仍属共识性预期，来源本身未提供根因分析或支撑证据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.jpost.com/business-and-innovation/energy-and-infrastructure/article-915750">Chief of US intelligence , Jay Clayton , predicts more tech outages</a></li>
<li><a href="https://www.breitbart.com/tech/2026/11/19/wave-of-tech-outages-prompts-americans-prepare-for-doomsday/">Wave of Tech Outages Prompts Americans to Prepare for Doomsday</a></li>
<li><a href="https://www.cnbc.com/2026/11/17/apple-microsoft-faa-jpmorgan-outages.html">Apple outage follows Microsoft , FAA and JPMorgan disruptions</a></li>
<li><a href="https://www.newsweek.com/major-cities-update-emergency-advice-as-mass-outages-weather-events-hit-us-12742371">Major Cities Update Emergency Advice as Mass Outages ... - Newsweek</a></li>
<li><a href="https://www.foxbusiness.com/economy/walmart-shoppers-stocked-up-emergency-supplies-after-series-tech-outages-report">Americans stock up on emergency supplies after string of tech outages</a></li>

</ul>
</details>

**标签**: `#technology outages`, `#infrastructure resilience`, `#Microsoft Outlook`, `#banking systems`

---

<a id="item-tech-news-4"></a>
### [Notable Capital 等机构重仓 Anthropic 的逻辑](https://techcrunch.com/2026/11/22/how-notable-capital-gic-and-baillie-gifford-bet-big-on-anthropic-before-its-ipo/) ⭐️ 6.0/10

TechCrunch 梳理了 Notable Capital、GIC 和 Baillie Gifford 看好 Anthropic 的原因，以及三家重要机构在该公司可能进行 IPO 前进行的巨额投资。据报道，相关投资规模达到数十亿美元，反映出机构资本对 Anthropic 及其所处 AI 市场的高度信心。文章聚焦投资人的判断和押注逻辑，但现有材料未披露具体估值、融资轮次、持股比例、IPO 时间表或各机构给出的完整理由。

rss · TechCrunch · 11月23日 01:25

**「背景」** Anthropic 是一家前沿 AI 模型开发商；在其仍为非上市公司时，Notable Capital（风险投资机构）、GIC（主权财富基金）和 Baillie Gifford（投资管理机构）通过投资成为重要支持者。所谓“IPO 前下注”指参与私募市场融资并持有公司股份；资料显示，Notable 投资时 Anthropic 的估值约为 615 亿美元，而公司随后正推进 IPO 计划。

**「对投资者与 Anthropic 的影响」** Notable Capital、GIC 与 Baillie Gifford 的数十亿美元前期投资将直接为 Anthropic 的潜在 IPO 提供资本与估值背书，并让现有投资者获得更清晰的公开市场退出路径；不过，外部报道所示 Baillie Gifford US Growth 对 Anthropic 的持仓已占基金资产的 7.5%，意味着其基金投资者也将承受 IPO 定价和上市后波动风险。

<details><summary>参考链接</summary>
<ul>
<li>Anthropic backers explain the developer demand and financial ...</li>
<li>Anthropic just launched tools to show companies what their AI spending ...</li>
<li><a href="https://www.youtube.com/watch?v=IRzmfWMOL8g">Anthropic will be an exceptional growth stock as it enters... - YouTube</a></li>
<li><a href="https://www.abcmoney.co.uk/2026/06/anthropic-ipo-filing-edges-closer-as-965bn-ai-giant-submits-s-1-draft/">Anthropic IPO Filing Edges Closer as $965bn AI Giant... | ABC Money</a></li>

</ul>
</details>

**标签**: `#Anthropic`, `#AI investment`, `#venture capital`, `#IPO`

---

<a id="item-tech-news-5"></a>
### [低价 GPT-5.1 令牌被用于寻找绕过中国防火墙的新方法](https://www.theregister.com/security/2026/11/23/1-of-gpt-51-tokens-finds-new-ways-around-chinas-great-firewall/5311532) ⭐️ 6.0/10

《The Register》的一则新闻汇总援引研究称，价值约 1 美元的 GPT-5.1 令牌调用被用于寻找绕过中国“防火长城”的新方法。这一案例将大语言模型与网络审查规避研究联系起来，表明低成本 AI 资源可能成为探索安全边界和封锁绕过策略的工具。不过，现有报道只是简短预告，未披露实验方法、具体发现、成功率、适用条件或实际影响，因此无法判断结果的可复现性及其是否构成稳定且可规模化的方案。

rss · The Register · 11月23日 00:23

**「相关背景」** 中国“防火长城”（Great Firewall）通过网络过滤、DNS 操纵和连接阻断等机制限制跨境访问，代理与中转域名是常见的规避手段。本报道涉及的背景，是研究人员尝试以低成本调用 GPT-5.1，让大语言模型自动探索新的绕过路径，从而将 AI 的应用从内容生成延伸至网络审查与安全研究。

**「潜在影响」** 如果相关研究能够复现，以约 1 美元的 GPT-5.1 token 成本生成新的中国“防火长城”绕过方法，可能降低规避审查工具的开发和更新门槛；但现有报道仅为摘要，未提供具体方法、成功率或可复现性数据，实际影响尚无法确认。

**标签**: `#AI security`, `#large language models`, `#network censorship`, `#cybersecurity`

---

<a id="item-tech-news-6"></a>
### [数字化汽车每年增加 120 亿美元美国维修成本](https://www.theregister.com/personal-tech/2026/11/22/as-cars-go-digital-us-consumers-pay-an-extra-12-billion-a-year-for-repairs/5311412) ⭐️ 6.0/10

报道称，随着汽车数字化程度提高，维修工作越来越依赖专用软件工具，而部分工具采用订阅制，进一步推高维修支出。美国消费者因此可能每年为软件化汽车维修额外承担 120 亿美元，相关成本也会通过保险费用转嫁。现有说明未提供该估算的统计方法、技术依据或数据范围，因此 120 亿美元应视为报道中的估算，而非已充分验证的结论。

rss · The Register · 11月22日 16:08

**「软件维修成本进入保险」** 随着汽车功能更多由软件控制，维修不再只是更换或加工实体部件，还可能需要使用厂商专用的诊断与维修工具，以及订阅式软件服务。由此产生的数字工具费用可能计入维修成本，并通过保险定价转嫁给车主。

**「维修成本影响」** 如果报道中的估算成立，美国车主和保险方每年将多承担约 120 亿美元的车辆维修及保险成本，使专有诊断工具、订阅和维修权限制成为直接的财务负担。由于现有材料未披露估算方法、成本分摊及保险传导方式，这一数字仍应视为有待核实的估算。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Right_to_repair">Right to repair - Wikipedia</a></li>

</ul>
</details>

**标签**: `#software-defined vehicles`, `#automotive software`, `#repair subscriptions`, `#insurance`

---

## 科技博客

<a id="item-tech-blog-1"></a>
### [不确定时，以多种尝试寻找反馈](https://seangoedecke.com/when-in-doubt-flail-about/) ⭐️ 7.0/10

rss · Sean Goedecke · 11月23日 00:00

**「背景」** 面对产品方向不明、复杂系统无从下手或团队协作阻塞，作者认为等待更多指导往往无助于建立理解；真正危险的是章法混乱地提出坏方案、忽视反馈并损害声誉。

**「方案」** 作者把有效探索称为“摸索”：同时推进多个方案，密切听取专家意见以及延迟、用户指标等现实反馈，一旦没有积极甚至“惊喜”回应便立即放弃；多留几条路径，也能避免把成败绑定在单一计划上。在产品层面，他任职于现已退役的 GitHub Models 期间尝试过许多未奏效的功能与集成，但允许通过 GitHub Actions 令牌运行 AI 推理这一方向意外获得用户黏性，并成为 Continuous AI 的种子。工程上，面对纠缠、庞大或已经高度优化的系统，他主张提出多项推测性改动并直接观察效果，只在确有改善时继续深入，AI 智能体还可辅助快速生成多种重构方案。组织层面，他建议通过自动化手工工作、临时接管任务或提出长期方案主动破冰，但必须敏锐捕捉团队反馈，否则无视失败信号会把不满引向帮助者。之所以称为“摸索”，是因为过程主观上像反复失败；作者建议预先把这种不适感视为正在探索的信号，而非陷入困境的证据。

**「启示」** 作者的核心结论是：信息不足时，以多种尝试接触现实、快速响应反馈并及时止损，往往比等待或押注单一路径更有效；这一观点主要由实践推理和个案经验支撑。

**标签**: `#decision-making under uncertainty`, `#experimentation`, `#engineering leadership`, `#product development`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [美股科技股大跌，亚洲多地调整交易与稳定措施](https://news.bjd.com.cn/2026/11/22/12039852.shtml) ⭐️ 8.0/10

美国 AI 科技股周五遭遇大规模抛售，纳斯达克单日下跌 5.28%，费城半导体指数跌近 11%。与此同时，中国内地将融资保证金最低比例下调至 80%，韩国完善股市稳定基金机制，中国台湾地区禁止平盘以下卖空并将融券保证金比例提高至 150%。

telegram · zaihuapd · 11月22日 13:24

**「背景」** 此次抛售发生在 AI 恐慌加剧之际；以科技股为主的纳斯达克 100 指数单日下跌 5.6%、全周累计下跌 10.4%，创下六年多来最差单周表现。

**「市场影响」** 中国内地、韩国及中国台湾地区的投资者和券商面临不同方向的交易规则调整，分别涉及融资保证金、股票回购、卖空和强制平仓，直接改变杠杆资金与卖空交易的条件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.guancha.cn/GuoJi%C2%B7ZhanLue/2026_11_21_909399.shtml">AI 恐慌爆发，华尔街震荡， 美 国 科 技 股 跌 入熊 市</a></li>

</ul>
</details>

**标签**: `#美股科技股`, `#半导体`, `#亚太股市`, `#卖空监管`, `#市场稳定`

---