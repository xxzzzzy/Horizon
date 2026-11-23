---
layout: default
title: "Horizon Summary: 2026-11-23 (EN)"
date: 2026-11-23
lang: en
---

> From 63 items, 8 important content pieces were selected

---

**Technology News**
1. [Perplexity as an Intelligence Benchmark](#item-tech-news-1) ⭐️ 8.0/10
2. [蚂蚁集团领投中国具身智能公司 1 亿美元，估值 16 亿美元](#item-tech-news-2) ⭐️ 7.0/10
3. [Major technology outages may continue amid infrastructure fragility](#item-tech-news-3) ⭐️ 6.0/10
4. [Anthropic Investors Detail Their Conviction Before a Potential IPO](#item-tech-news-4) ⭐️ 6.0/10
5. [GPT-5.1 Tokens Reportedly Find New Great Firewall Bypasses](#item-tech-news-5) ⭐️ 6.0/10
6. [Digital Vehicle Repair Tools Add $12 Billion in Annual US Costs](#item-tech-news-6) ⭐️ 6.0/10

**Technology Blog**
1. [Flailing Productively Under Uncertainty](#item-tech-blog-1) ⭐️ 7.0/10

**Financial News**
1. [U.S. Tech Rout Triggers Asian Market Safeguards](#item-finance-news-1) ⭐️ 8.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Perplexity as an Intelligence Benchmark](https://openai.com/index/perplexity-and-intelligence/) ⭐️ 8.0/10

OpenAI argues that lower language-model perplexity corresponds to greater intelligence and presents a simple next-token prediction benchmark as evidence that prediction quality tracks capability. Perplexity measures average surprise when predicting each token in a sequence: it is 1 for perfectly certain predictions and equals the vocabulary size for uniform random guessing. The article does not clearly define this metric, and the claimed relationship has not been independently validated, so it should not be taken as proof that perplexity alone captures reasoning or general intelligence. Even so, the proposal offers a compact, interpretable evaluation candidate that could complement task-specific and reasoning-focused benchmarks.

hackernews · acossta · Nov 22, 17:06 · [Discussion](https://news.ycombinator.com/item?id=50601525)

**「Understanding Perplexity」** Perplexity is a language-model evaluation metric that measures how surprising the actual next tokens are to a model, typically derived from the exponentiated average cross-entropy loss; lower values indicate better next-token prediction. In this context, it refers to held-out test-set performance for pretrained models whose basic training objective is next-token prediction, and the article tracks improvements from GPT-2-era systems onward as a simple signal of increasingly capable prediction and compression. The proposal treats this trend as relevant to broader intelligence, although perplexity measures predictive performance rather than reasoning, reliability, or every capability associated with general intelligence.

**「Practical implication」** Lower held-out perplexity can provide researchers with a simple common progress metric, but it cannot by itself rank advanced models by intelligence because GPT-4 and o3 have similar perplexity despite o3 representing a major capability improvement. Developers should therefore treat perplexity as a diagnostic signal rather than a complete substitute for task-level evaluations.

**「Community Discussion」** Commenters generally welcomed the simplicity of perplexity as a benchmark, noting surprise that cross-entropy remains informative despite reinforcement learning and connecting predictive performance to compression and world-model learning. Concerns centered on the article&\#x27;s missing definition and the need to distinguish prediction quality from reasoning, while one commenter cited Microsoft&\#x27;s reported MAI-2 Base log-perplexity of 0.819 as evidence that other organizations are pursuing comparable measurement.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/perplexity-and-intelligence/">Perplexity and Intelligence | OpenAI</a></li>
<li><a href="https://news.ycombinator.com/item?id=50601525">Perplexity and Intelligence | Hacker News</a></li>
<li><a href="https://openai.com/index/perplexity-and-intelligence/">Perplexity and Intelligence | OpenAI</a></li>
<li><a href="https://news.ycombinator.com/item?id=50601525">Perplexity and Intelligence | Hacker News</a></li>

</ul>
</details>

**Tags**: `#language-model-evaluation`, `#perplexity`, `#AI-research`, `#machine-learning`, `#AI-benchmarks`

---

<a id="item-tech-news-2"></a>
### [蚂蚁集团领投中国具身智能公司 1 亿美元，估值 16 亿美元](https://www.bloomberg.com/news/articles/2026-11-22/ant-group-bets-on-simplexity-to-thrive-in-china-s-humanoid-race) ⭐️ 7.0/10

Ant Group led a $100 million pre-A financing for Simplexity Robotics, valuing the humanoid-robotics startup at $1.6 billion.

telegram · zaihuapd · Nov 23, 02:02

**Tags**: `#embodied AI`, `#humanoid robotics`, `#venture funding`, `#China`

---

<a id="item-tech-news-3"></a>
### [Major technology outages may continue amid infrastructure fragility](https://www.theverge.com/tech/1039851/major-tech-outages) ⭐️ 6.0/10

The article highlights three recent nationwide disruptions: a FAA ground stop, a multi-day Microsoft Outlook outage that brought entire companies to a standstill, and a banking outage at JPMorgan Chase. It argues that these aviation, enterprise-software, and financial-system failures point to broader infrastructure fragility and that more major outages are likely to follow. The piece also cites Director of National Intelligence Jay Clayton while discussing the warning, but the supplied excerpt cuts off his remarks. The available account provides no root-cause analysis for the incidents and little technical evidence to substantiate the prediction that more outages are coming.

rss · The Verge · Nov 22, 22:48

**「Why outages are a recurring infrastructure concern」** The recent incidents ... ... Officials have said ... but evidence ... does not establish common root cause.

**「Operational and consumer impact」** The four-day sequence disrupted Microsoft services, FAA operations, JPMorgan Chase transactions, and Apple services, leaving dependent organizations, travelers, and consumers exposed to service, travel, and payment interruptions. It also increased consumer anxiety, with reports of emergency-supply purchases, although the available reporting does not establish a common technical cause.

<details><summary>References</summary>
<ul>
<li><a href="https://www.jpost.com/business-and-innovation/energy-and-infrastructure/article-915750">Chief of US intelligence , Jay Clayton , predicts more tech outages</a></li>
<li><a href="https://www.breitbart.com/tech/2026/11/19/wave-of-tech-outages-prompts-americans-prepare-for-doomsday/">Wave of Tech Outages Prompts Americans to Prepare for Doomsday</a></li>
<li><a href="https://www.cnbc.com/2026/11/17/apple-microsoft-faa-jpmorgan-outages.html">Apple outage follows Microsoft , FAA and JPMorgan disruptions</a></li>
<li><a href="https://www.foxbusiness.com/economy/walmart-shoppers-stocked-up-emergency-supplies-after-series-tech-outages-report">Americans stock up on emergency supplies after string of tech outages</a></li>

</ul>
</details>

**Tags**: `#technology outages`, `#infrastructure resilience`, `#Microsoft Outlook`, `#banking systems`

---

<a id="item-tech-news-4"></a>
### [Anthropic Investors Detail Their Conviction Before a Potential IPO](https://techcrunch.com/2026/11/22/how-notable-capital-gic-and-baillie-gifford-bet-big-on-anthropic-before-its-ipo/) ⭐️ 6.0/10

TechCrunch examines why Notable Capital, GIC, and Baillie Gifford invested billions in Anthropic ahead of a potential IPO. The article centers on the reported views of three significant backers about what gave them conviction to make those early bets. Their perspectives illuminate the financing and IPO strategy surrounding a major AI company, although the supplied source does not include the investors’ specific arguments. No valuation, deal terms, offering timetable, or evidence about IPO timing is provided in the available material.

rss · TechCrunch · Nov 23, 01:25

**「Private funding before the IPO」** Anthropic is a frontier AI lab that has raised private capital from investors including Notable Capital, GIC, and Baillie Gifford ahead of a potential public listing; Notable&\#x27;s investment was reportedly made at a $61.5 billion valuation. The article examines how those investors assessed Anthropic&\#x27;s developer demand and financial prospects before an IPO would shift the company from private financing to publicly traded shares.

**「Fund concentration risk」** For shareholders in the affected funds, Anthropic’s pre-IPO stakes create material concentration risk: it reportedly represents 7.5% of Baillie Gifford US Growth’s assets and 7.3% of Schiehallion Fund’s, so their returns could move materially with Anthropic’s eventual IPO valuation and trading performance.

<details><summary>References</summary>
<ul>
<li>Anthropic backers explain the developer demand and financial ...</li>
<li>Anthropic just launched tools to show companies what their AI spending ...</li>
<li><a href="https://www.abcmoney.co.uk/2026/06/anthropic-ipo-filing-edges-closer-as-965bn-ai-giant-submits-s-1-draft/">Anthropic IPO Filing Edges Closer as $965bn AI Giant... | ABC Money</a></li>

</ul>
</details>

**Tags**: `#Anthropic`, `#AI investment`, `#venture capital`, `#IPO`

---

<a id="item-tech-news-5"></a>
### [GPT-5.1 Tokens Reportedly Find New Great Firewall Bypasses](https://www.theregister.com/security/2026/11/23/1-of-gpt-51-tokens-finds-new-ways-around-chinas-great-firewall/5311532) ⭐️ 6.0/10

A roundup from The Register highlights research suggesting that about $1 worth of GPT-5.1 tokens can be used to discover new methods of bypassing China’s Great Firewall. The report points to a novel intersection between inexpensive large-language-model use and network-circumvention research, but the supplied teaser provides no methodology, specific findings, success rates, or operational limitations. As a result, the scale, reproducibility, and practical significance of the claim remain unclear.

rss · The Register · Nov 23, 00:23

**「Background」** China’s Great Firewall is an umbrella term for technical and policy controls that restrict access to certain online services and information within China. LLM tokens are units of processed text, and the report’s premise is that inexpensive GPT-5.1 queries allow researchers to automate large numbers of experiments against censorship controls, potentially revealing new circumvention methods.

**「Impact」** If the reported finding holds, spending about $1 in GPT-5.1 tokens could make Great Firewall circumvention methods cheaper and easier to refresh, potentially helping users who rely on blocked services. The brief roundup does not provide the methods, testing, or deployment evidence needed to establish practical reliability or scale.

**Tags**: `#AI security`, `#large language models`, `#network censorship`, `#cybersecurity`

---

<a id="item-tech-news-6"></a>
### [Digital Vehicle Repair Tools Add $12 Billion in Annual US Costs](https://www.theregister.com/personal-tech/2026/11/22/as-cars-go-digital-us-consumers-pay-an-extra-12-billion-a-year-for-repairs/5311412) ⭐️ 6.0/10

The Register reports that increasingly digital vehicles require proprietary software tools for repairs, contributing to an estimated $12 billion per year in additional US repair and insurance costs. Subscription-based repair tools add ongoing expenses for vehicle owners and service providers while also potentially increasing insurance premiums. The shift changes vehicle maintenance from primarily parts-and-labor work toward software-dependent services and access. However, the supplied account does not explain the estimate’s methodology or divide the $12 billion between repairs and insurance, so the figure should be treated as a reported estimate rather than an independently substantiated total.

rss · The Register · Nov 22, 16:08

**「Background」** Modern vehicle repair increasingly depends on proprietary, manufacturer-controlled software tools rather than mechanical work alone. Paid subscriptions for access to those tools can raise repair-shop costs, which may then be passed to consumers or reflected in insurance premiums.

<details><summary>References</summary>
<ul>
<li>AI will eat a fifth of tech budgets in 2027, but don&#x27;t expect it to pay for ...</li>
<li>&#x27;Vibe coding&#x27; is risky: Here&#x27;s why and what to do about it - Polaimath</li>

</ul>
</details>

**Tags**: `#software-defined vehicles`, `#automotive software`, `#repair subscriptions`, `#insurance`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [Flailing Productively Under Uncertainty](https://seangoedecke.com/when-in-doubt-flail-about/) ⭐️ 7.0/10

rss · Sean Goedecke · Nov 23, 00:00

**「Background」** Engineers often face product, systems, or organizational problems where there is no reliable guide, making patient analysis and caution less useful than immediate experimentation. But undirected flailing can damage credibility, so the challenge is to act without a clear answer while remaining responsive to evidence.

**「Solution」** Sean Goedecke recommends trying many speculative approaches to gather direct feedback from reality, paying close attention to user, technical, and peer signals, and immediately dropping options that do not earn a positive response. Running multiple approaches also prevents emotional or organizational overinvestment in one weak plan, since success means finding one promising path rather than making every attempt work. In product development, he points to GitHub Models, where several unsuccessful feature experiments eventually produced the AI-inference-from-a-GitHub-Actions-token integration that seeded Continuous AI. For tangled, large, or fast-changing systems, he favors speculative changes whose apparent effects can be observed; apparent improvements merit deeper investigation, while ineffective changes should be discarded. The same approach can address organizational friction by trying concrete interventions—such as automating work or taking over tasks—provided the engineer notices and responds to feedback so unsuccessful efforts do not deepen distrust. He also frames the discomfort of repeated failure as a psychological barrier: treating that feeling as a signal to continue experimenting, rather than proof of trouble, is part of making the method work. The argument is illustrated mainly through reasoning and personal experience, with limited quantitative evidence or detailed treatment of experimentation costs.

**「Takeaway」** Under uncertainty, progress comes from broad, feedback-driven experimentation and the willingness to abandon weak approaches quickly—not from waiting for certainty before acting.

**Tags**: `#decision-making under uncertainty`, `#experimentation`, `#engineering leadership`, `#product development`

---

## Financial News

<a id="item-finance-news-1"></a>
### [U.S. Tech Rout Triggers Asian Market Safeguards](https://news.bjd.com.cn/2026/11/22/12039852.shtml) ⭐️ 8.0/10

U.S. AI-related technology stocks were sold off sharply on Friday, with the Nasdaq Composite down 5.28% and the Philadelphia Semiconductor Index down nearly 11%. China, South Korea and Taiwan responded with tighter financing, short-selling and market-stability rules, including Taiwan’s increase in the securities-lending margin ratio from 130% to 150%.

telegram · zaihuapd · Nov 22, 13:24

**「Background」** The selloff came amid an AI-tech rout that a separate market report described as the Nasdaq 100’s worst week in more than six years, with a 5.6% one-day fall and a 10.4% weekly decline; Asian authorities responded by adjusting financing-collateral, short-selling and market-stabilization rules.

**「Impact on Asian investors」** Investors in Taiwan face tighter short-selling rules from Nov. 23, including an increase in the securities-lending margin ratio from 130% to 150%, while South Korea strengthens monitoring of short selling, credit trading and forced liquidations from Nov. 24; mainland China separately lowers its minimum financing-margin ratio to 80%.

<details><summary>References</summary>
<ul>
<li><a href="https://www.guancha.cn/GuoJi%C2%B7ZhanLue/2026_11_21_909399.shtml">AI 恐慌爆发，华尔街震荡， 美 国 科 技 股 跌 入熊 市</a></li>

</ul>
</details>

**Tags**: `#美股科技股`, `#半导体`, `#亚太股市`, `#卖空监管`, `#市场稳定`

---