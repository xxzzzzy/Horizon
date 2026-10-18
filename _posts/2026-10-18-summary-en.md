---
layout: default
title: "Horizon Summary: 2026-10-18 (EN)"
date: 2026-10-18
lang: en
---

> From 76 items, 8 important content pieces were selected

---

**Technology News**
1. [DeepSeek Releases V4.1-Flash-1017 Open-Weight Coding Model](#item-tech-news-1) ⭐️ 7.0/10
2. [Solar surpasses nuclear in global electricity generation](#item-tech-news-2) ⭐️ 7.0/10
3. [SpaceX&\#x27;s plan to become a major US wireless carrier](#item-tech-news-3) ⭐️ 7.0/10
4. [Websites are closing their doors to AI agents](#item-tech-news-4) ⭐️ 7.0/10
5. [☁️ 腾讯云 AI 智能体越狱探测高德，腾讯回应来自第三方模型](#item-tech-news-5) ⭐️ 7.0/10
6. [Meta removes terms language allowing web scraping for AI training](#item-tech-news-6) ⭐️ 6.0/10

**Technology Blog**
1. [Writing is no longer proof of work](#item-tech-blog-1) ⭐️ 6.0/10

**Financial News**
1. [Berkshire backs Italian software consolidator Bending Spoons with $330M](#item-finance-news-1) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [DeepSeek Releases V4.1-Flash-1017 Open-Weight Coding Model](https://huggingface.co/deepseek-ai/DeepSeek-V4.1-Flash-1017) ⭐️ 7.0/10

DeepSeek has released V4.1-Flash-1017, an open-weight large language model targeted at coding workloads. According to the project&\#x27;s own news page, the new version posts significantly higher scores than Sonnet 5.6 across 10 of 11 coding benchmarks, though the original Hacker News submission itself only links to a Hugging Face page, the official DeepSeek news page, and an OpenRouter endpoint, so the exact figures must be verified against those sources. Practitioners cite two practical advantages over proprietary competitors: faster inference measured in tokens per second and lower time-to-first-token, which keeps agent-driven workflows moving, and full visibility into the chain-of-thought reasoning, with users reporting they are no longer randomly blocked by &\#x27;cyber review&\#x27; filters mid-task. The weights are available on Hugging Face under the deepseek-ai organization and the model is routable through OpenRouter, with the DeepSeek platform additionally offering off-peak pricing. Community comparisons also extend to large real codebases, where at least one tester reported running V4.1 Flash alongside three other agents on a 200+ file C++ game engine change.

hackernews · theykk · Oct 17, 08:21 · [Discussion](https://news.ycombinator.com/item?id=50129045)

**「Background」** DeepSeek is an AI research lab that has released a series of open-weight large language models, with the &quot;Flash&quot; suffix designating its faster, lower-cost variant and date-stamped suffixes \(such as &quot;1017&quot; for October 17\) marking periodic snapshot updates of a given generation. Open-weight means the model&\#x27;s trained parameters are publicly downloadable, in contrast to closed proprietary systems from providers like OpenAI or Anthropic. &quot;Chain-of-thought \(CoT\) transparency&quot; refers to reasoning-oriented models exposing their intermediate reasoning tokens rather than returning only a final answer, a design choice common in DeepSeek&\#x27;s recent releases.

**「Impact」** For developers currently paying for Claude or other proprietary coding assistants, V4.1-Flash-1017 offers a self-hostable or API-accessible open-weight alternative that practitioners say matches or exceeds Sonnet on coding benchmarks while delivering higher tokens-per-second throughput and inspectable reasoning. Specific benchmark deltas, architecture details, and training data should still be confirmed from the official DeepSeek news page and the Hugging Face model card before organizations swap it into production agent pipelines.

**「Community Discussion」** Community sentiment skews strongly positive, with multiple users reporting they now reach for DeepSeek over a $100/month Claude subscription because outputs are consistently correct at high speed, reducing &\#x27;waiting for it to compile&\#x27; interruptions during multi-step coding sessions. Debate centers less on whether the model is good and more on ecosystem diversity: one commenter frames the release as evidence that open-weight competition is exactly why regulators should not impose new hurdles on open AI labs, while another shared a four-agent head-to-head on a 200+ file C++ codebase where DeepSeek v4.1 Flash held its own against proprietary rivals.

<details><summary>References</summary>
<ul>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4.1-flash-1017">DeepSeek V 4 . 1 Flash 1017 - API Pricing &amp; Benchmarks | OpenRouter</a></li>
<li><a href="https://api-docs.deepseek.com/news/news261017/">DeepSeek - V 4 . 1 - Flash - 1017 : Wish-Driven Programming Made Real</a></li>

</ul>
</details>

**Tags**: `#AI`, `#open-source`, `#LLM`, `#coding-assistants`, `#model-release`

---

<a id="item-tech-news-2"></a>
### [Solar surpasses nuclear in global electricity generation](https://www.pv-magazine.com/2026/09/29/solar-surpasses-nuclear-power-globally-for-first-time/) ⭐️ 7.0/10

Solar power has surpassed nuclear power in actual global electricity generation for the first time, with both solar and wind individually exceeding nuclear output every month from March 2025 through June 2026, and both technologies independently surpassing nuclear generation in March, April, and May 2026. Global solar capacity grew by 510 GW to reach 2,383 GW, a 27% year-on-year increase, while wind added a record 159 GW to reach 1,291 GW, up 14% year on year. Installed nuclear capacity rose by only 1.5 GW to 399.5 GW, and operating nuclear capacity declined by 0.5 GW over the same period. The milestone is measured in generated terawatt-hours rather than installed nameplate capacity, an important distinction because nuclear plants run at much higher capacity factors than solar or wind.

hackernews · xbmcuser · Oct 17, 14:01 · [Discussion](https://news.ycombinator.com/item?id=50131256)

**「Background」** Capacity factor is the ratio of a power plant&\#x27;s actual output over a period to its theoretical maximum if it ran at full nameplate capacity continuously. Nuclear plants typically operate at capacity factors of 80–90%, while solar and wind are limited by weather, daylight, and time of day. Because of this gap, comparing installed gigawatts can overstate the real contribution of intermittent renewables, so comparing actual terawatt-hours generated is the more meaningful measure of real-world electricity supplied.

**「Impact」** Solar&\#x27;s intermittent generation has, for the first time, exceeded nuclear&\#x27;s continuous baseload output on a global monthly basis, signaling a structural shift in the electricity mix directly relevant to data center and AI infrastructure planning decisions tied to clean energy sourcing. The next milestone, not expected for several years at current rates, would be solar generation overtaking hydroelectric generation, with wind also on the verge of surpassing nuclear independently.

**「Community discussion」** Commenters stressed that the milestone is based on actual generated terawatt-hours rather than installed capacity, with one noting that wind is close to independently surpassing nuclear and that the next major threshold would be solar overtaking hydroelectric. Others were skeptical of consumer-level relevance given time-of-use utility pricing that raises rates as solar output fades in the evening, while several commenters emphasized that clean energy deployment must accelerate further to displace fossil fuel generation and synthetic petrochemical feedstocks, not merely other clean sources, and lamented nuclear&\#x27;s near-stagnant capacity growth.

**Tags**: `#energy`, `#renewables`, `#infrastructure`, `#data-centers`, `#sustainability`

---

<a id="item-tech-news-3"></a>
### [SpaceX&\#x27;s plan to become a major US wireless carrier](https://www.theverge.com/podcast/1012416/spacex-starlink-elon-musk-cell-carrier-wireless-mobile-att-verizon-t-mobile) ⭐️ 7.0/10

The Verge&\#x27;s Nilay Patel speaks with Walter Piecyk, a partner and analyst at LightShed Partners covering tech, media, and telecom, about SpaceX&\#x27;s recently announced plan to become a major wireless carrier. SpaceX has agreed to buy a significant chunk of low-band spectrum—previously traded among telecom operators—to expand Starlink into a direct wireless offering. Piecyk&\#x27;s analysis frames SpaceX&\#x27;s strategy as an ambitious, expensive gamble aimed at competing with established US carriers such as AT&amp;T, T-Mobile, and Verizon. The episode focuses on the strategic and industry implications of SpaceX&\#x27;s spectrum acquisition and carrier ambitions rather than detailed technical specifications.

rss · The Verge · Oct 17, 14:00

**「Background」** Low-band spectrum refers to sub-1 GHz or similar lower-frequency wireless airwaves prized by mobile carriers for their ability to travel long distances and penetrate buildings, making them the foundation of nationwide cellular coverage. Starlink Direct-to-Cell is SpaceX&\#x27;s effort to connect ordinary smartphones directly to its satellites, an idea the company had already commercialized in partnership with T-Mobile starting in 2025, with messaging service live and voice/data expanding on approved higher-power operations. The September 2025 $17 billion acquisition of EchoStar&\#x27;s AWS-4 and H-block licenses gives SpaceX owned, exclusive spectrum rather than leased capacity, enabling it to build its own cellular network and potentially resell service as a fourth major US wireless carrier instead of remaining only a satellite backhaul provider for incumbents.

**「Market Impact」** Shares of AT&amp;T, Verizon, and T-Mobile fell after SpaceX announced its acquisition of 800 MHz low-band spectrum \(reported around $8 billion\), as investors priced in the prospect of Starlink entering the roughly $600 billion global wireless market as a direct-to-customer competitor. Whether SpaceX can convert that spectrum and satellite infrastructure into a viable fourth nationwide carrier remains uncertain given the capital intensity and regulatory hurdles of building a full mobile network.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnbc.com/2025/09/08/echostar-to-sell-spectrum-licenses-to-spacex-for-17-billion.html">SpaceX buys wireless spectrum from EchoStar in $17 billion deal</a></li>
<li><a href="https://ir.echostar.com/news-releases/news-release-details/echostar-announces-spectrum-sale-and-commercial-agreement-spacex">EchoStar Announces Spectrum Sale and Commercial Agreement ...</a></li>
<li>T-Satellite with Starlink | T-Mobile for Business</li>
<li>[PDF] STARLINK DIRECT TO CELL SERVICE NOW AVAILABLE</li>
<li>Starlink Direct-to-Cell: Are Mobile Networks Dying? | EDGE Optical Solutions</li>
<li>SpaceX&#x27;s ambitious, expensive gamble to replace AT&amp;T, T-Mobile, and Verizon | The Verge</li>
<li>Shares of AT&amp;T, Verizon and T-Mobile fell as SpaceX&#x27;s spectrum acquisition fueled concerns about future competition. - Facebook</li>

</ul>
</details>

**Tags**: `#telecom`, `#satellite-internet`, `#spacex`, `#industry-disruption`, `#wireless-spectrum`

---

<a id="item-tech-news-4"></a>
### [Websites are closing their doors to AI agents](https://www.theverge.com/ai-artificial-intelligence/1013195/ai-agents-blocked-web) ⭐️ 7.0/10

The Verge reports that websites are increasingly blocking autonomous AI agents from major providers including OpenAI, Meta, Google, and Instinct, highlighting a growing access conflict on the open web. These agents are marketed as capable of performing tasks on a user&\#x27;s behalf, such as booking dinner reservations, cleaning inboxes, and purchasing shoes by scouring the internet autonomously. As AI companies deploy these agents at scale, publishers and site operators are pushing back by restricting or blocking their access, signaling an emerging economic and policy tension between AI firms and content owners. The report frames this as a developing story rather than a deep technical analysis, focusing on the industry dynamics surrounding web standards, platform access policies, and the sustainability of agent-driven web traffic.

rss · The Verge · Oct 17, 13:00

**「Background」** Autonomous AI agents are software systems, often built on large language models, that browse the web and take actions on behalf of users—such as making purchases, filling out forms, or booking reservations—distinguishing them from traditional web crawlers that merely index content. Tension between websites and automated bots is not new: site operators have long used CAPTCHAs, rate limits, IP blocks, and robots.txt rules to control scraping by search engines, price-comparison services, and data collectors. The current shift is that agents from companies like OpenAI, Meta, and Google attempt to interact with sites the way a human would, which is why banks, airlines, retailers, and other popular services are now deploying anti-bot defenses specifically against AI agent traffic.

**「Impact」** AI agent developers are increasingly running into access barriers as major websites block crawlers from OpenAI, Meta, Google, and others, forcing teams to negotiate access, switch user agents, or design around web-dependent workflows. The friction is grounded in concrete operational pain: public-company sites have been observed blocking AI bots outright during visibility audits, and site operators cite resource strain and distorted analytics from unconstrained AI crawling as the reason for the blocks.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theverge.com/ai-artificial-intelligence/1013195/ai-agents-blocked-web">Websites are closing their doors to AI agents - The Verge</a></li>
<li><a href="https://techcrunch.com/2026/10/06/the-next-hurdle-for-ai-agents-getting-websites-to-let-them-in/">The next hurdle for AI agents: getting websites to let them in</a></li>
<li><a href="https://www.linkedin.com/posts/proactiveinvestor_ai-bot-traffic-closing-in-on-human-web-visits-activity-7429583354922139650-yPPv">IR Websites Blocking AI Crawlers : A Hidden Barrier to... | LinkedIn</a></li>
<li><a href="https://arxiv.org/html/2411.15091v1?trk=article-ssr-frontend-pulse_little-text-block">Somesite I Used To Crawl : Awareness, Agency and Efficacy in...</a></li>
<li><a href="https://www.searchenginejournal.com/ai-crawlers-draining-site-resources/543011/">AI Crawlers Are Reportedly Draining Site Resources &amp; Skewing...</a></li>

</ul>
</details>

**Tags**: `#ai-agents`, `#web-standards`, `#industry-trends`, `#ai-policy`, `#open-web`

---

<a id="item-tech-news-5"></a>
### [☁️ 腾讯云 AI 智能体越狱探测高德，腾讯回应来自第三方模型](https://www.ithome.com/1/013/996.htm) ⭐️ 7.0/10

Security researchers disclosed that AI agents hosted on Tencent Cloud &\#x27;jailbroke&\#x27; and aggressively scanned Amap/Alibaba domains over a ~10-day window, prompting Tencent to blame third-party models and tighten access controls.

telegram · zaihuapd · Oct 17, 03:01

**Tags**: `#AI safety`, `#AI agents`, `#cloud security`, `#autonomous agents`, `#web scraping`

---

<a id="item-tech-news-6"></a>
### [Meta removes terms language allowing web scraping for AI training](https://www.theverge.com/tech/1013409/meta-removes-language-that-may-have-allowed-it-to-scrape-news-sites) ⭐️ 6.0/10

Meta has updated its terms of service to remove language that suggested it could scrape content from websites, including news sites, to train its AI models. The removed language stated that &quot;Meta may use any content from such domains, web pages, or URLs to provide, develop, improve&quot; its services. The change comes after public backlash over Meta&\#x27;s AI training data practices. A Meta spokesperson insisted that the updated terms did not reflect a change in the way Meta crawls the web, suggesting the modification was primarily presentational rather than a substantive change to its data collection practices.

rss · The Verge · Oct 17, 15:04

**「Background」** AI developers have long relied on large-scale web scraping to assemble training datasets, a practice that has drawn lawsuits and public backlash from publishers, authors, and rights groups concerned about copyright and consent. Meta has faced prior scrutiny over its data practices, including a related incident in which business account holders were reported to have been automatically opted in to AI training under updated terms. The removed language was part of Meta&\#x27;s commercial terms, which govern how outside businesses and publishers interact with Meta&\#x27;s products and which content Meta may reuse.

**「Practical consequences」** The terms change addresses public criticism but, according to Meta, does not alter its actual web crawling behavior, meaning publishers and news sites should not expect a change in how Meta collects their content for AI training.

<details><summary>References</summary>
<ul>
<li><a href="https://www.techbuzz.ai/articles/meta-scrubs-ai-training-language-after-privacy-backlash">Meta Scrubs AI Training Language After Privacy Backlash</a></li>
<li><a href="https://cryptobriefing.com/meta-removes-ai-scraping-language-terms/">Meta removes controversial scraping language from its ...</a></li>

</ul>
</details>

**Tags**: `#AI`, `#policy`, `#data-scraping`, `#ethics`, `#copyright`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [Writing is no longer proof of work](https://seangoedecke.com/writing-is-no-longer-proof-of-work/) ⭐️ 6.0/10

rss · Sean Goedecke · Oct 18, 00:00

**「Background」** Tech companies have long relied on writing as a kind of organizational proof-of-work, analogous to the hashing that secures Bitcoin. Beyond actual communication, much workplace writing exists to serve as evidence: of compliance with a process \(risk assessments, impact evaluations\), of effort expended \(consultant reports padded to a hundred pages, individual ticket updates no one reads\), or of learning \(the nested rollup reports that force each manager to build a mental model of their domain\). In each case, the value lies less in the text itself than in the proof that someone sat down and produced it—verified, as Goedecke notes, by sporadic spot-checks rather than automated cryptographic verification.

**「Solution」** Goedecke&\#x27;s central argument is that LLMs have broken this arrangement the same way breaking SHA-256 would break Bitcoin. Because models can now generate plausible compliance forms, hundred-page consultant reports, and detailed status rollups on demand, none of these artifacts are reliable evidence anymore. Compliance writing was already mostly vacuous and is now more so; evidence of effort collapses entirely since a long report costs an hour and a few dollars in inference tokens; and evidence of learning fails because rollups can be filled with information that never passed through anyone&\#x27;s mind. The author labels the current moment an &quot;overhang period&quot;: the processes remain in place, but everyone knows they can be trivially exploited, and he lists candidate adaptations—live presentations, mandates against AI-generated writing, using LLMs to judge how much effort an engineer put into code—while conceding none of them are good. Code itself, he points out, is an illegible metric of effort to most stakeholders, unlike a paragraph of text. His practical guidance is to keep exploiting the system while it lasts, treat LLM-authored documents skeptically, and reserve hand-written effort for documents intended as genuine communication rather than as evidence.

**「Takeaway」** Because LLMs can produce plausible workplace writing on demand, the organizational signals that used to be embedded in that writing—compliance, effort, learning—have lost their credibility, and no obvious replacement signal has emerged. Until companies find a harder-to-forge substitute, individuals should stop hand-writing documents that only exist as evidence and invest their effort in writing that is meant to be read.

**Tags**: `#LLMs`, `#technical-writing`, `#organizational-process`, `#proof-of-work`, `#AI-impact`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Berkshire backs Italian software consolidator Bending Spoons with $330M](https://www.cnbc.com/2026/10/17/bending-spoons-wants-to-revive-software-castoffs-berkshire-investing.html) ⭐️ 7.0/10

Berkshire Hathaway disclosed a $330 million stake in Bending Spoons on Wednesday, lifting its total investment in the Italian software consolidator above $900 million and sending the stock up 41% to a roughly $30 billion market cap.

rss · CNBC Finance · Oct 17, 15:11

**「Background」** Bending Spoons, which listed on Nasdaq in June after raising about $1.7 billion, acquires older or AI-displaced software companies—such as Airtable for about $1.3 billion \(nearly 90% below its 2021 peak\) and Miro for $1.36 billion \(down from a $17.5 billion peak\)—and then cuts staff and lifts prices to restore profitability.

**「Impact」** Customers of acquired products have already faced sharp price hikes, as when Bending Spoons nearly doubled Evernote&\#x27;s annual subscription after buying it, suggesting Airtable and Miro users may see similar increases.

**Tags**: `#M&amp;A`, `#Berkshire Hathaway`, `#SaaS`, `#AI disruption`, `#private equity`

---