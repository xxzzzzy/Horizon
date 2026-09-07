---
layout: default
title: "Horizon Summary: 2026-09-07 (EN)"
date: 2026-09-07
lang: en
---

> From 68 items, 11 important content pieces were selected

---

**Technology News**
1. [Anubis Ports CAPTCHA to WebAssembly After a Year](#item-tech-news-1) ⭐️ 7.0/10
2. [OpenAI&\#x27;s &\#x27;Alien Mind&\#x27; Essay on AI Safety Sparks Debate](#item-tech-news-2) ⭐️ 7.0/10
3. [OpenAI shares internal coding-agent data, frames RSI as its AGI path](#item-tech-news-3) ⭐️ 7.0/10
4. [German Isar Aerospace launches Europe&\#x27;s first fully commercial orbital rocket](#item-tech-news-4) ⭐️ 7.0/10
5. [Around 1 in 5 new gTLD domains used for scams, Interisle data suggests](#item-tech-news-5) ⭐️ 6.0/10
6. [Seattle Times and Newsday sue OpenAI and Microsoft over AI training data](#item-tech-news-6) ⭐️ 6.0/10
7. [Time lords prepare to kick leap seconds into the next millennium](#item-tech-news-7) ⭐️ 6.0/10
8. [Meta FAIR Unveils Research Preference Models for Pre-Run ML Experiment Ranking](#item-tech-news-8) ⭐️ 6.0/10

**Financial News**
1. [Eight Chinese Central Financial Enterprises to Raise 360 Billion Yuan in Core Tier-1 Capital](#item-finance-news-1) ⭐️ 8.0/10
2. [Sugar Prices Surge Past Stocks in 2026 on Global Supply Woes](#item-finance-news-2) ⭐️ 7.0/10
3. [CXMT raises DRAM market share to 10%, H1 revenue up 873% YoY](#item-finance-news-3) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Anubis Ports CAPTCHA to WebAssembly After a Year](https://anubis.techaro.lol/blog/2026/anubis-wasm/) ⭐️ 7.0/10

The article recounts a year-long engineering effort to port Anubis, a proof-of-work CAPTCHA used by open-source projects including GNOME and SourceHut, to WebAssembly. The WebAssembly version is intended to make automated solving by AI scrapers more difficult by reducing reliance on JavaScript-based solver paths. The change strengthens anti-bot resistance but can reduce compatibility with legacy browsers, including some smart-TV browsers, and may create accessibility and user-experience concerns. The effort also focused on preserving compatibility where practical, including work related to older browser targets such as Chrome 66.

hackernews · xena · Sep 6, 20:32 · [Discussion](https://news.ycombinator.com/item?id=49590611)

**「Background」** Anubis is a proof-of-work CAPTCHA system that requires a browser to compute SHA-256 hashes until a target difficulty is met, and it has been adopted by open-source projects such as GNOME and SourceHut to deter large-scale AI scrapers. WebAssembly \(WASM\) is a low-level binary instruction format that browsers can execute at near-native speed, typically compiled from languages like Rust or C/C++. Porting Anubis&\#x27;s challenge computation from JavaScript to WASM raises the engineering bar for would-be solvers, since they can no longer rely on simple JS automation, but it also drops support for legacy browsers that lack WASM capability.

**「Impact」** Anubis deployments that adopt the WASM proof-of-work challenge significantly raise the cost for AI scrapers that rely on JavaScript-based or LLM-generated \(e.g., &quot;Claude vibeslop me a CUDA solver&quot;\) automated solvers, but users on browsers without WASM support such as older smart TVs and security-hardened Firefox configurations can no longer pass the challenge at all.

**「Community Discussion」** Commenters broadly praised the project’s emphasis on backward compatibility and the maintainers’ approach, while raising concerns about users who disable WebAssembly and clients running browsers too old to support it. One commenter recommended Rust’s wasm32v1-none target for baseline WebAssembly compatibility, noting that it requires a no-std environment.

<details><summary>References</summary>
<ul>
<li><a href="https://anubis.techaro.lol/blog/2026/anubis-wasm/">It took a year to ship WebAssembly in Anubis | Anubis</a></li>
<li><a href="https://www.scien.cx/2025/06/07/weighing-souls-with-anubis-at-home/">Weighing Souls with Anubis at Home – Sciencx</a></li>
<li><a href="https://detect.expert/blog/webassembly/">WebAssembly Fingerprinting vs. Anti-Detect Browsers: Why WASM ...</a></li>
<li><a href="https://incidentdatabase.ai/cite/1001/">Incident 1001: LLM Scrapers Allegedly Target Multiple Open Source ...</a></li>
<li><a href="https://tildes.net/~comp/1mqd/block_ai_scrapers_with_anubis">Block AI scrapers with Anubis - ~comp - Tildes</a></li>

</ul>
</details>

**Tags**: `#webassembly`, `#captcha`, `#anti-scraping`, `#open-source-infrastructure`, `#systems-engineering`

---

<a id="item-tech-news-2"></a>
### [OpenAI&\#x27;s &\#x27;Alien Mind&\#x27; Essay on AI Safety Sparks Debate](https://openai.com/index/an-alien-mind/) ⭐️ 7.0/10

OpenAI published a blog post titled &\#x27;An Alien Mind&\#x27; that discusses AI alignment, recursive self-improvement \(RSI\), and the strategic rationale for advancing AI capabilities rapidly. The post frames continued progress toward more capable AI systems as necessary both to remain at the research frontier and to build defensive systems against risks from competing AI development. It argues that automated AI research represents a more dramatic form of scaling intelligence with compute and positions OpenAI&\#x27;s research direction around RSI accordingly. The essay generated substantial discussion on Hacker News, drawing 341 points and 292 comments, with critics raising concerns about the arms-race framing and questions about OpenAI&\#x27;s corporate positioning ahead of a potential IPO. The post is more of a strategic and philosophical statement from a leading AI lab than a technical breakthrough, but it has been read as a notable signal of how OpenAI is publicly framing its approach to safety and capability development.

hackernews · OpenAI News · Sep 6, 16:27 · [Discussion](https://news.ycombinator.com/item?id=49588080)

**「Background」** AI alignment refers to the research problem of ensuring that advanced AI systems act in accordance with human intentions and values, particularly as systems grow more capable than their creators. Recursive self-improvement \(RSI\) describes a scenario in which an AI system helps design or train its successors, potentially leading to rapid, compounding capability gains. OpenAI operates under a hybrid structure with a non-profit parent governing a capped-profit subsidiary, a setup that has repeatedly drawn scrutiny over how its public-benefit mission is reconciled with commercial activities.

**「Impact」** OpenAI Chief Scientist Jakub Pachocki&\#x27;s essay explicitly calls for voluntary slowdowns by AI labs until shared safety bars are established and frames international coordination on future AI development as needing to become a top government priority. The most concrete consequence is a direct tension between this call for restraint and OpenAI&\#x27;s stated pursuit of recursive self-improvement as the only way to remain at the frontier, which commenters read as self-interested arms-race logic rather than a credible safety stance, with some additionally characterizing the messaging as pre-IPO positioning inconsistent with continued aggressive capability scaling.

**「Community Discussion」** Hacker News commenters were broadly skeptical and concerned. Several critiques focused on the arms-race logic in the essay, with one reader summarizing the strongest argument for pushing capability boundaries as essentially defensive, while questioning whether open-source and Chinese models would in fact keep advancing independently. Others criticized the framing of recursive self-improvement as reckless, characterizing the rationale as &\#x27;we need to do dangerous things as quickly as possible so we can do them first.&\#x27; A recurring line of criticism targeted OpenAI&\#x27;s positioning, with one commenter suggesting the post reflects pre-IPO framing, and a charity&\#x27;s pivot toward floating part of its mission on public markets. Discussion also touched on the near-term arrival of AI-driven breakthroughs outside pure math and software, suggesting the essay landed amid broader expectations that frontier AI is approaching material real-world impact.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/an-alien-mind/">An Alien Mind | OpenAI</a></li>
<li><a href="https://ai-tldr.dev/releases/openai-an-alien-mind/">An Alien Mind — OpenAI&#x27;s chief scientist calls… | AI/TLDR</a></li>
<li><a href="https://www.unite.ai/in-an-alien-mind-openais-jakub-pachocki-urges-shared-safety-bars/">In “An Alien Mind,” OpenAI’s Jakub Pachocki Urges Shared Safety Bars – Unite.AI</a></li>
<li><a href="https://cryptobriefing.com/openai-chief-scientist-ai-risks-warning/">OpenAI&#x27;s chief scientist warns that advanced AI models are becoming harder to align and control</a></li>

</ul>
</details>

**Tags**: `#AI safety`, `#AI strategy`, `#alignment`, `#OpenAI`, `#recursive self-improvement`

---

<a id="item-tech-news-3"></a>
### [OpenAI shares internal coding-agent data, frames RSI as its AGI path](https://simonwillison.net/2026/Sep/6/research-acceleration-the-view-inside-openai/) ⭐️ 7.0/10

OpenAI published &quot;Research acceleration: The view inside OpenAI,&quot; sharing internal data on how its research team uses coding agents and introducing &quot;RSI&quot; \(Recursive Self-Improvement\) as the company&\#x27;s framing for AGI, alongside Chief Scientist Jakub Pachocki&\#x27;s companion essay &quot;An Alien Mind.&quot; A chart in the post tracks median daily AI spending per researcher from February through August 2026, showing slow growth from near $0 to roughly $150 by June, a plateau through July, and a steep climb to about $600 by late August. Simon Willison speculates the late-summer jump reflects OpenAI researchers gaining internal access to a model later released publicly as GPT-6 Astra. Because the underlying post is partly promotional and the supplied excerpt is truncated, the chart&\#x27;s methodology, sample, and full claims cannot be independently verified from this source alone.

rss · Simon Willison · Sep 6, 23:57

**「Background」** Recursive Self-Improvement \(RSI\) is the idea that an AI system can iteratively improve its own weights, training pipeline, or capabilities, and OpenAI is now using the term as a label for its AGI goal rather than older &quot;superintelligence&quot;-style framings. Coding agents are LLM-based systems that autonomously write, edit, test, and execute code on a user&\#x27;s behalf, and &quot;agentic engineering&quot; refers to workflows in which these agents take on substantial portions of software work rather than only completing individual lines of code.

**「Impact」** For AI and software engineering audiences, the chart offers rare quantitative evidence of how quickly coding agents are being adopted inside a frontier lab, though because the figures are self-reported by OpenAI they should be read as illustrative rather than independently audited.

**Tags**: `#AI`, `#OpenAI`, `#Coding Agents`, `#Agentic Engineering`, `#AGI`

---

<a id="item-tech-news-4"></a>
### [German Isar Aerospace launches Europe&\#x27;s first fully commercial orbital rocket](https://arstechnica.com/space/2026/09/german-company-becomes-first-in-europe-to-launch-fully-commercial-orbital-rocket/) ⭐️ 7.0/10

Isar Aerospace, founded in 2018 by three students at the Technical University of Munich, successfully launched its privately developed Spectrum rocket into low-Earth orbit on Saturday from Andøya Spaceport in northern Norway, inside the Arctic Circle. The two-stage, 92-foot-tall \(28-meter\) Spectrum vehicle lifted off at 4:12 pm EST \(20:12 UTC, 10:12 pm local time\) and reached orbit seven minutes later, deploying five small satellites and an experimental payload, making it the first fully commercial launch vehicle in Europe to reach orbit. CEO Daniel Metzler, who co-founded Isar along with classmates Josef Fleischmann and Markus Brandl—naming the company after the river running through Munich—declared that &quot;Europe now has sovereign access to space&quot; and positioned Spectrum as an alternative for commercial and institutional customers constrained by Europe&\#x27;s stagnant launch market. The company plans to focus next on scaling launch vehicle production and fulfilling its existing order pipeline to meet what it describes as surging global demand.

rss · Ars Technica · Sep 6, 11:55

**「Background」** Europe&\#x27;s orbital launch capability has historically been dominated by state-backed vehicles developed through the European Space Agency and operated commercially by Arianespace, primarily the Ariane family of rockets and the smaller Italian-built Vega. Isar Aerospace, founded in 2018 by students at the Technical University of Munich, is part of a new wave of European launch startups—including PLD Space and HyImpulse—seeking to introduce private-sector competition into the region&\#x27;s space launch market. The designation &quot;fully commercial&quot; distinguishes Spectrum from these prior European orbital efforts, which were developed with substantial public funding and institutional backing, and Isar&\#x27;s Saturday flight was the second in the Spectrum program.

**「Why it matters」** Isar Aerospace becomes the first European startup to deliver a fully commercial rocket to orbit, giving European commercial and institutional customers a new alternative to existing launch providers and a concrete step toward breaking the region&\#x27;s long-standing launch monopoly. The launch positions Isar as the current leader among a pack of competing European launch startups, though it does not yet displace established non-European commercial launch providers.

<details><summary>References</summary>
<ul>
<li><a href="https://www.orbitalintel.org/powers/european-launch-startups/">European Launch Startups: PLD Space, HyImpulse, Isar Aerospace ...</a></li>
<li><a href="https://defence-industry.eu/isar-aerospace-reaches-orbit-on-second-spectrum-flight-opening-new-european-launch-option-for-commercial-and-institutional-customers/">Isar Aerospace reaches orbit on second Spectrum flight, opening new ...</a></li>
<li><a href="https://www.spaceinsights.io/insights/isar-aerospace-planet-labs-germany-w28">Isar Aerospace and Planet Labs Germany: The All-German Mission and the ...</a></li>

</ul>
</details>

**Tags**: `#commercial space`, `#launch industry`, `#Europe`, `#orbital rockets`, `#Isar Aerospace`

---

<a id="item-tech-news-5"></a>
### [Around 1 in 5 new gTLD domains used for scams, Interisle data suggests](https://simonwillison.net/2026/Sep/6/the-purpose-of-dns-is-to-spread-scams/) ⭐️ 6.0/10

A blog post by Terence Eden, surfaced via Simon Willison&\#x27;s linkblog, argues that the Domain Name System is functioning at scale as a vector for online scams. Drawing on an Interisle report on cybercriminal domain demand, Eden notes that approximately 85 million new generic top-level domain \(gTLD\) registrations occurred in 2025, of which roughly 8.5 million had been added to blocklists by May 2025. The report estimates a 10% abuse rate as the likely floor, with the true figure closer to 20%, meaning about one in five newly registered gTLD domains are scams. Eden characterizes this level of abuse as &quot;a bloody crisis&quot; and notes that ICANN has reportedly been discussing the problem for years without apparent resolution. The post is short commentary rather than original analysis, but it draws attention to data points many readers, including Willison, found surprisingly high.

rss · Simon Willison · Sep 6, 14:40

**「Background」** The Domain Name System \(DNS\) translates human-readable domain names into IP addresses and is foundational to how the web is accessed. Generic top-level domains \(gTLDs\) such as .com, .net, and newer options like .app or .xyz are overseen by ICANN through a network of accredited registrars. Blocklists are maintained by security researchers and organizations to flag domains associated with spam, phishing, and other abuse, though inclusion criteria vary between lists.

**「Impact」** Operators of legitimate new gTLD domains may face increased scrutiny, filtering, or delivery problems as blocklists absorb a growing share of fresh registrations. End users navigating the web are likely to encounter fraudulent sites at a meaningful rate, reinforcing the need for cautious evaluation of unfamiliar links and domains.

**Tags**: `#DNS`, `#cybersecurity`, `#internet infrastructure`, `#web development`, `#security`

---

<a id="item-tech-news-6"></a>
### [Seattle Times and Newsday sue OpenAI and Microsoft over AI training data](https://www.theverge.com/ai-artificial-intelligence/990932/seattle-times-newsday-lawsuit-openai-microsoft) ⭐️ 6.0/10

The Seattle Times and Newsday have filed copyright infringement lawsuits against OpenAI and Microsoft, alleging their journalism was used without permission to train AI models. The two outlets claim that their reporting was scraped as training data and that passages from their articles are frequently reproduced in chatbot responses to user queries. These filings follow a similar pattern to earlier actions brought by The New York Times and other publishers against OpenAI over alleged unauthorized use of news content. The cases add to a growing body of legal pressure on generative AI providers over the sourcing of training data from copyrighted media.

rss · The Verge · Sep 6, 23:36

**「Background」** The Seattle Times and Newsday lawsuit is the latest in a growing wave of copyright actions by news organizations against OpenAI and Microsoft. The New York Times set the precedent in late 2023 by filing the first major suit alleging that OpenAI&\#x27;s models were trained on its journalism without permission and that ChatGPT could reproduce its reporting nearly verbatim. Since then, nearly 400 local newspapers have joined the legal effort, and the Seattle Times and Newsday filings extend that pattern to two more regional outlets while expanding the dispute to include Microsoft because its Copilot product is built on OpenAI&\#x27;s technology.

**「Impact」** The lawsuits add to mounting legal pressure on OpenAI and Microsoft over the use of copyrighted journalism in AI training, potentially accelerating publisher litigation or formal licensing deals across the generative AI industry.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theverge.com/ai-artificial-intelligence/990932/seattle-times-newsday-lawsuit-openai-microsoft">Seattle Times and Newsday sue OpenAI and Microsoft ... | The Verge</a></li>
<li><a href="https://www.engadget.com/2251707/seattle-times-newsday-sue-openai-microsoft-for-copyright-infringement/">Two More News Organizations Sue OpenAI And Microsoft For...</a></li>

</ul>
</details>

**Tags**: `#AI Legal`, `#Copyright`, `#OpenAI`, `#Generative AI`, `#Media Industry`

---

<a id="item-tech-news-7"></a>
### [Time lords prepare to kick leap seconds into the next millennium](https://www.theregister.com/offbeat/2026/09/06/time-lords-prepare-to-kick-leap-seconds-into-the-next-millennium/5294538) ⭐️ 6.0/10

Proposals are advancing that would eliminate or defer leap seconds and allow Coordinated Universal Time \(UTC\) to drift by as much as an hour from mean solar time, a shift prompted by the unprecedented prospect of a negative leap second. The risk of a negative adjustment — subtracting a second rather than adding one — is the immediate trigger for revisiting long-standing leap-second policy, since current insertion practices have not previously required subtracting time. Allowing UTC to drift by up to an hour represents a dramatic expansion of tolerated divergence from astronomical time, which has historically been kept within roughly one second. Such a change would affect software engineers, distributed systems, and time-sensitive infrastructure that currently must handle occasional leap-second insertions, and the plan frames deferral as a multi-millennium solution to sidestep the insertion problem entirely.

rss · The Register · Sep 6, 08:09

**「Background」** Leap seconds are one-second adjustments inserted into Coordinated Universal Time \(UTC\) to keep it within 0.9 seconds of mean solar time, which is based on Earth&\#x27;s slightly variable rotation; since the system was introduced in 1972, 27 positive leap seconds have been added, but a negative leap second has never occurred. Past positive insertions have triggered outages at services including Reddit, Cloudflare, and several airlines, which is why metrology bodies have been debating whether to retire the mechanism entirely.

**「Impact」** Should the proposal be adopted, operators of time-sensitive infrastructure and distributed systems would no longer need to handle leap-second insertions \(or the novel case of a negative leap second\), at the cost of accepting up to an hour of accumulated drift between civil UTC and solar time over the coming centuries.

**「Community discussion」** No community comments are available for this item.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theregister.com/offbeat/2026/09/06/time-lords-prepare-to-kick-leap-seconds-into-the-next-millennium/5294538">Time lords prepare to kick leap seconds into the next millennium</a></li>
<li><a href="https://theintelligent.co.uk/science/2026/nature-proposes-ending-leap-seconds-negative-leap-second-risk-rises">Nature proposes ending leap seconds as negative ... | The Intelligent</a></li>
<li><a href="https://theuniverseepisodes.com/how-fast-does-the-earth-spin/">How Fast Does the Earth Spin? Speed by Latitude ( 2026 )</a></li>

</ul>
</details>

**Tags**: `#timekeeping`, `#infrastructure`, `#utc`, `#standards`, `#distributed-systems`

---

<a id="item-tech-news-8"></a>
### [Meta FAIR Unveils Research Preference Models for Pre-Run ML Experiment Ranking](https://news.google.com/rss/articles/CBMi4wFBVV95cUxPYXZzVU94NzFvWkZNZmNTLWYxNjFaRmJCR0g2emRYdUxTeTdCcFhOMWh3M0pIcFZRRG12Zi1WNFp3Y0EwRkxnM1h3VjY2TFlUSmZMa2ctd3hOaG44RHFFZE5sSVFOYkFLQW5YWHptaHp1cXVLZjlMSl9LTVA3emFtaVdsb204a25kandyY3R5NndfTWRNYkZ3VHhialY1NDZvcU5xNGxDYXhPQ3MtdGRyal8yN1A5OWpTNGlxRjZyLWRHMEFkVUxXeFgtWmh4eGdrLWZkSmhnaFJhb3poWEFnZTYyRdIB4wFBVV95cUxPYXZzVU94NzFvWkZNZmNTLWYxNjFaRmJCR0g2emRYdUxTeTdCcFhOMWh3M0pIcFZRRG12Zi1WNFp3Y0EwRkxnM1h3VjY2TFlUSmZMa2ctd3hOaG44RHFFZE5sSVFOYkFLQW5YWHptaHp1cXVLZjlMSl9LTVA3emFtaVdsb204a25kandyY3R5NndfTWRNYkZ3VHhialY1NDZvcU5xNGxDYXhPQ3MtdGRyal8yN1A5OWpTNGlxRjZyLWRHMEFkVUxXeFgtWmh4eGdrLWZkSmhnaFJhb3poWEFnZTYyRQ?oc=5) ⭐️ 6.0/10

Meta FAIR has introduced AI Research Preference Models \(RPMs\), a system intended to rank machine learning experiments before any GPU compute is committed to running them. The headline-level description suggests the models predict which experimental ideas are most promising so research teams can allocate expensive GPU hours to higher-priority candidates instead of speculative runs. However, the available reporting, sourced from the secondary aggregator MarkTechPost, contains no technical details such as the underlying model architecture, training data, evaluation benchmarks, quantitative results, release status, or author attribution, so claims about RPMs&\#x27; methodology and effectiveness cannot yet be independently verified. Until Meta FAIR&\#x27;s primary publication, code release, or official documentation is reviewed, the depth, maturity, and reproducibility of the approach remain unclear.

google\_news · MarkTechPost · Sep 6, 20:25

**「Background」** Machine learning research typically involves running many experimental candidates, and deciding which ones justify spending limited GPU compute has long been handled through researcher intuition, ablation studies, and increasingly through autonomous research agents. Preference models, familiar from alignment work such as Reinforcement Learning from Human Feedback \(RLHF\), learn to rank or score options based on comparative judgments rather than absolute ground-truth labels. Meta FAIR&\#x27;s Research Preference Models \(RPMs\) adapt this ranking idea to the pre-experiment stage, comparing candidate ML experiment descriptions before any training run is launched.

**「Impact」** For ML research teams constrained by GPU compute, RPMs could, if the underlying claims hold, reduce the number of low-yield experiments executed, but no quantitative performance, savings, or benchmark figures have been disclosed in the available source material.

<details><summary>References</summary>
<ul>
<li><a href="https://www.marktechpost.com/2026/09/06/meta-fair-introduces-ai-research-preference-models-rpms-ranking-ml-experiments-before-spending-gpu-hours/">Meta FAIR Introduces AI Research Preference Models ( RPMs )...</a></li>
<li><a href="https://korshunov.ai/en/article/23541-fair-introduces-rpms-to-rank-ml-experiments-before-execution/">FAIR introduces RPMs to rank ML experiments before execution</a></li>
<li><a href="https://www.aoyii.com/en/ai-research-preference-models-rpm/">Research Preference Models : Meta Prioritizes AI Experiments</a></li>

</ul>
</details>

**Tags**: `#machine-learning`, `#meta-fair`, `#research-tools`, `#gpu-optimization`, `#experiment-management`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Eight Chinese Central Financial Enterprises to Raise 360 Billion Yuan in Core Tier-1 Capital](https://www.news.cn/fortune/20260906/1633e4121bf14b52859aff2dffa36888/c.html) ⭐️ 8.0/10

On September 6, eight Chinese central financial enterprises announced coordinated capital-raising plans totaling 360 billion yuan to bolster core tier-1 capital. ICBC and ABC plan to issue A-shares to the Ministry of Finance and China National Tobacco Corporation, raising up to 100 billion yuan and 160 billion yuan respectively. The Ministry of Finance will inject 30 billion yuan into the Export-Import Bank and 10 billion yuan into China Export &amp; Credit Insurance Corporation, while PICC plans to raise up to 15 billion yuan, China Re 3 billion yuan, and the Ministry will additionally inject 35 billion yuan into China Life Insurance Group and 7 billion yuan into China Taiping.

telegram · zaihuapd · Sep 6, 10:47

**Tags**: `#Banking`, `#China financial system`, `#Capital markets`, `#Government policy`, `#Insurance`

---

<a id="item-finance-news-2"></a>
### [Sugar Prices Surge Past Stocks in 2026 on Global Supply Woes](https://www.cnbc.com/2026/09/06/sugar-is-outperforming-the-stock-market-this-year-whats-driving-it.html) ⭐️ 7.0/10

Sugar futures jumped 21.5% in August, their biggest monthly gain since October 2010, lifting the commodity&\#x27;s 2026 return to about 20% and outpacing the S&amp;P 500&\#x27;s nearly 13% advance.

rss · CNBC Finance · Sep 6, 13:19

**「Background」** Prices reflect multiple supply shocks: a heat wave damaged the EU&\#x27;s sugar beet crop \(production forecast to fall 19% to 13.4 million metric tons\), El Niño threatens harvests in Brazil, India and Thailand, oil prices above $90 a barrel are pushing Brazilian mills toward ethanol, and India authorized its first duty-free raw-sugar imports since 2017-18.

**「Impact」** The rally raises costs for sugar-using food and beverage companies while supporting margins for ethanol-linked producers in Brazil, where mills are shifting more cane to biofuel output.

**Tags**: `#commodities`, `#agricultural-commodities`, `#sugar`, `#food-prices`, `#weather-impact`

---

<a id="item-finance-news-3"></a>
### [CXMT raises DRAM market share to 10%, H1 revenue up 873% YoY](https://www.zaobao.com.sg/news/china/story20260906-9633523) ⭐️ 7.0/10

China&\#x27;s DRAM maker ChangXin Memory Technologies \(CXMT\) raised its global revenue share to 10% in Q2 2026, up from 4% a year earlier to rank fourth, according to Counterpoint Research. The company reported first-half revenue of 150.31 billion yuan, up 873.64% year-on-year, and swung to a 77.605 billion yuan net profit, attributed to AI-driven memory demand and rising prices.

telegram · zaihuapd · Sep 6, 06:43

**「background」** CXMT \(ChangXin Memory Technologies\) is China&\#x27;s largest domestic DRAM producer, founded in 2016 in Hefei, and ranks behind global leaders Samsung, SK Hynix, and Micron. The 873% revenue jump partly reflects a low comparison base following the 2023–2024 DRAM downcycle, when CXMT&\#x27;s heavy DDR4 and LPDDR4X supply had weighed on spot prices.

**「Impact」** The share gain puts direct pressure on the three leading DRAM suppliers — Samsung, SK Hynix, and Micron — as Chinese capacity expands during the current AI-led memory upcycle.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bybit.com/en/wiki/article/what-is-cxmt-china-s-dram-chip-maker-explained/">What Is CXMT? China&#x27;s DRAM Chip Maker Explained | Bybit Wiki</a></li>
<li><a href="https://aiwiki.ai/wiki/cxmt">CXMT (ChangXin Memory Technologies) | AI Wiki</a></li>

</ul>
</details>

**Tags**: `#semiconductors`, `#DRAM`, `#market share`, `#AI infrastructure`, `#Chinese tech`

---