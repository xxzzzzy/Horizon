---
layout: default
title: "Horizon Summary: 2026-11-16 (EN)"
date: 2026-11-16
lang: en
---

> From 75 items, 12 important content pieces were selected

---

**Technology News**
1. [Qwen4-Max launches with sparse MoE and configurable reasoning](#item-tech-news-1) ⭐️ 8.0/10
2. [Vision Encoder Pretraining Is Optional for Multimodal Models](#item-tech-news-2) ⭐️ 8.0/10
3. [Meituan Releases LongCat-2.5 Open-Weight Agent Model](#item-tech-news-3) ⭐️ 8.0/10
4. [Vulcan rocket fails during launch, dealing major blow to SpaceX competitors](#item-tech-news-4) ⭐️ 7.0/10
5. [Congress Weighs Tighter AI Chip Export Rules](#item-tech-news-5) ⭐️ 7.0/10
6. [Datasette 0.65.6 Security Backport](#item-tech-news-6) ⭐️ 6.0/10
7. [Apple Smart Glasses Rumors Highlight No-AR First Model](#item-tech-news-7) ⭐️ 6.0/10
8. [Bharat Semi Raises $24M for AI Sensors](#item-tech-news-8) ⭐️ 6.0/10
9. [Microsoft Raises Azure Prices in India, Cuts China Costs](#item-tech-news-9) ⭐️ 6.0/10
10. [Toward a Nonperturbative Lattice Standard Model](#item-tech-news-10) ⭐️ 6.0/10

**Financial News**
1. [China’s slowdown deepens in October as industrial output, retail sales, investment miss estimates](#item-finance-news-1) ⭐️ 8.0/10
2. [Lutnick faces questions over Cantor Fitzgerald’s Nvidia ties amid China espionage concerns](#item-finance-news-2) ⭐️ 8.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Qwen4-Max launches with sparse MoE and configurable reasoning](https://qwen.ai/blog?id=qwen4-max) ⭐️ 8.0/10

Alibaba Tongyi Qianwen has launched Qwen4-Max, a flagship model that an announcement reposted in the discussion says uses a sparse mixture-of-experts architecture with 2.4 trillion total parameters, native visual understanding, and a 1-million-token context window. It targets programming, office work, and long-running tasks, with the announcement claiming a leading Code Arena blind-test position in frontend coding and four selectable reasoning efforts: none, low, high, and xhigh. The announcement reports that average task cost fell from RMB 26.58 to RMB 11.16, a reduction of nearly 58%, while token consumption dropped nearly 50% and API pricing was reduced. Smaller Qwen4 models and open-weight releases are planned, while commenters specifically ask about 27B and “Flash” versions, but no release dates were provided.

hackernews · ilreb · Nov 16, 02:14 · [Discussion](https://news.ycombinator.com/item?id=50513215)

**「Background」** ...

**「Deployment impact」** Qwen4-Max expands the feasible API workload for long-document, coding, and agentic applications through a 1-million-token context window and up to 393,216 output tokens, while its Artificial Analysis Intelligence Index score of 43 gives buyers a concrete quality baseline; high-volume deployments should still validate price and latency against alternatives.

**「Community discussion」** Reaction is broadly positive about Qwen4-Max’s quality and efficiency, but cost and serving speed remain important concerns: one cited Artificial Analysis listing gives it a score of 43 at an average $3.27, compared with 46 and $0.36 for GPT-6.1 Sol at medium reasoning. A practitioner says Qwen 3.8 Max performs well in an agent battle system when early voting is excluded and attributes its low score mainly to throughput of about 30 tokens per second versus roughly 80 for Opus; Simon Willison also notes that OpenRouter’s qwen3.8-max-prime runs faster but costs twice as much as the standard variant.

<details><summary>References</summary>
<ul>
<li><a href="https://artificialanalysis.ai/models/qwen4-max">Qwen 4 Max - Intelligence, Performance &amp; Price ... | Artificial Analysis</a></li>
<li><a href="https://openrouter.ai/qwen/qwen4-max">Qwen 4 Max - API Pricing &amp; Providers | OpenRouter</a></li>
<li><a href="https://www.qwencloud.com/models/qwen4-max?region=ap-southeast-1">Qwen 4 - Max - QwenCloud</a></li>
<li><a href="https://artificialanalysis.ai/models/qwen4-max">Qwen 4 Max - Intelligence, Performance &amp; Price... | Artificial Analysis</a></li>
<li><a href="https://www.eesel.ai/blog/qwen-4-max-review">Qwen 4 Max review (2026): the preview, tested against the... | eesel AI</a></li>

</ul>
</details>

**Tags**: `#large-language-models`, `#Qwen`, `#model-evaluation`, `#reasoning`, `#AI-infrastructure`

---

<a id="item-tech-news-2"></a>
### [Vision Encoder Pretraining Is Optional for Multimodal Models](https://www.reddit.com/r/MachineLearning/comments/1xx1k2o/meta_fair_nyu_unbundling_multimodal_vision/) ⭐️ 8.0/10

Meta FAIR and NYU researchers trained more than 200 multimodal models from scratch under matched data and lifetime-compute budgets to isolate three commonly bundled design choices: vision-encoder pretraining, vision-only parameters, and encoder placement. Separate encoder pretraining—including contrastive, self-supervised, and captioning objectives—provided no VQA advantage over training the encoder jointly with the LLM, even when pretraining was free or extended 6.5 times. Dedicated vision parameters remained important: encoder-free models underperformed across 0.6B-to-6.4B backbones and required roughly three times the compute to catch up, while sharing the encoder’s parameters with text tokens improved language performance but hurt VQA. Encoder placement was also optional; zero-initialized vision-only branches in the LLM’s first eight layers matched a conventional encoder from 1.7B to 6.4B parameters and reduced time to first token by about 13%. At 1.7B parameters, the first-eight-layer branches scored 45.0 on VQA versus 44.4 for the encoder, 42.3 when text shared the branches, and 35.1 when they were placed in the last eight layers; the post was disclosed by one of the study’s authors, and the supplied account does not include independent validation.

reddit · r/MachineLearning · /u/trungh98 · Nov 15, 17:38

**「Background」** Multimodal language models commonly use a pretrained vision encoder to turn images into visual tokens before a language model processes them, but recent approaches differ in whether that encoder is pretrained and whether visual processing has dedicated parameters. The Meta FAIR–NYU study disentangles three often-bundled design choices—an upstream visual prior, vision-only capacity, and pre-fusion placement—and evaluates them with matched training data and lifetime compute.

**「Practical impact」** For MLLM developers, the study indicates that vision-encoder pretraining can be omitted under a matched compute budget if vision-only parameters are retained, while fully encoder-free designs need roughly 3× the compute to catch up. The findings are limited to the authors’ controlled Qwen3-based setup and benchmark suite, so independent replication is needed before treating them as a universal architectural rule.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2611.17334">[2611.17334] Unbundling Multimodal Vision Encoding - arXiv.org</a></li>
<li><a href="https://arxiv.org/pdf/2611.17334v1">Unbundling Multimodal Vision Encoding - arXiv.org</a></li>
<li><a href="https://arxiv.org/pdf/2611.17334v1">Unbundling Multimodal Vision Encoding - arXiv.org</a></li>

</ul>
</details>

**Tags**: `#multimodal-language-models`, `#vision-encoders`, `#model-training`, `#ablation-studies`, `#AI-research`

---

<a id="item-tech-news-3"></a>
### [Meituan Releases LongCat-2.5 Open-Weight Agent Model](https://the-decoder.com/meituan-releases-a-1-6-trillion-parameter-agent-model-that-never-touched-an-nvidia-gpu/) ⭐️ 8.0/10

Meituan&\#x27;s LongCat team published the LongCat-2.5 model weights one week after its official release, targeting agents that can autonomously complete long, multistep tasks, particularly programming tasks. The 1.6-trillion-parameter model activates about 48 billion parameters per token and supports text, image, and video input. Meituan says the model was trained entirely on Huawei Ascend accelerators without using Nvidia GPUs, while its MIT-licensed weights permit commercial use. LongCat-2.5 scored 88.4 on Terminal Bench v2.1, narrowly below Claude Opus 5&\#x27;s 89.1, though the training provenance and benchmark result have not been independently verified.

telegram · zaihuapd · Nov 15, 11:08

**「Background」** LongCat-2.5 is an open-weight, multimodal agent model from Meituan’s LongCat team, designed for long-horizon tasks such as multi-step programming. Its 1.6 trillion total parameters but roughly 48 billion active per token reflect a sparse design that uses only part of the model for each token. Terminal-Bench v2.1 is the cited coding-agent benchmark, where LongCat-2.5 scored 88.4 versus Claude Opus 5’s 89.1; its MIT license allows commercial use, while Meituan says training ran entirely on Huawei Ascend accelerators rather than Nvidia GPUs.

**「Practical impact」** Developers and organizations can commercially use the MIT-licensed open weights of LongCat-2.5, a 1.6-trillion-parameter multimodal agent with 48 billion active parameters per token, for long-horizon programming; Meituan says it was trained entirely on Huawei Ascend accelerators rather than Nvidia GPUs, and the official results report 88.4 on Terminal Bench v2.1 versus 89.1 for Claude Opus 5. This provides a commercially accessible open-weight alternative for coding-agent deployments, but the hardware-training and benchmark claims still require independent validation.

<details><summary>References</summary>
<ul>
<li><a href="https://lmspeed.net/model/longcat-2-5">LongCat - 2 . 5 API Pricing &amp; Benchmarks | LMSpeed</a></li>
<li><a href="https://sumus.im/blog/longcat-2-5">LongCat 2 . 5 : Meituan &#x27;s AI Model , Benchmarks, Price &amp; API | Sumus</a></li>
<li><a href="https://thehype.news/meituan-longcat-2-5-model/">Meituan LongCat - 2 . 5 Benchmarks vs Claude Opus 5 and GPT- 5 .6</a></li>
<li><a href="https://www.longcatai.org/benchmarks/longcat-2-5">LongCat-2.5 Benchmarks - Full 33-Task Evaluation vs GPT-5.6 ...</a></li>
<li><a href="https://agentspulse.github.io/tutorials/longcat-2-5/">LongCat 2.5: Benchmarks, Pricing and Claude Code Setup ...</a></li>

</ul>
</details>

**Tags**: `#AI agents`, `#open-source models`, `#Huawei Ascend`, `#multimodal AI`, `#programming benchmarks`

---

<a id="item-tech-news-4"></a>
### [Vulcan rocket fails during launch, dealing major blow to SpaceX competitors](https://arstechnica.com/space/2026/11/vulcan-rocket-fails-during-launch-dealing-major-blow-to-spacex-competitors/) ⭐️ 7.0/10

ULA&\#x27;s Vulcan rocket and 40 Amazon Leo broadband satellites fell back to Earth shortly after liftoff, with an indefinite grounding and industry-wide consequences expected.

rss · Ars Technica · Nov 15, 23:11

**Tags**: `#Vulcan`, `#launch failure`, `#Amazon Leo`, `#satellite broadband`, `#space industry`

---

<a id="item-tech-news-5"></a>
### [Congress Weighs Tighter AI Chip Export Rules](https://www.theverge.com/ai-artificial-intelligence/1033984/congress-export-rules-ai-chips-china) ⭐️ 7.0/10

Congress is considering tighter restrictions on AI-chip exports following a scandal involving Nvidia and a suspected Chinese spy, with now-former CEO Jensen Huang reportedly at the center of the case. Democrats and Republicans have expressed support for various measures and bills that would tighten the rules. Lawmakers have also demanded that Huang and other Nvidia executives testify before Congress. The report does not identify the specific proposals or explain which chips, customers, or destinations would be affected, leaving the scope and timing of any restrictions uncertain.

rss · The Verge · Nov 15, 19:15

**「Policy Context」** U.S. export rules already regulate shipments of advanced AI chips to destinations such as China, and the alleged espionage case adds a national-security dimension to debates over tightening those restrictions. The case concerns Alice Huang, a suspected China spy linked to former Nvidia CEO Jensen Huang, who left her executive role at Megaspeed in August 2025. Huang has opposed tighter constraints on the AI race, while he and other Nvidia officials have agreed to testify before Congress, although no hearing date has been set.

**「Impact on chipmakers and chip supply chains」** If the proposed restrictions move forward, Nvidia and competing accelerator vendors would face further limits on selling advanced AI chips into China and other restricted markets, with effects propagating through the concentrated GPU supply chain to AI labs and data centers that depend on those chokepoints. The likely counter-effect is accelerated Chinese self-reliance and substitution of imported chips, while Beijing has warned that the espionage scandal must not be used as a &quot;pretext for imposing a technological blockade&quot; on AI technology.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bbc.com/news/articles/cmdx1vpprk9vo">Suspected China spy linked to Nvidia &#x27;s ex-boss left in 2025...</a></li>
<li><a href="https://www.theguardian.com/technology/2026/nov/16/elon-musk-tech-execs-open-letter-jensen-huang-return-nvidia-ceo">Elon Musk joins 158,000 others calling for Nvidia to bring back Jensen ...</a></li>
<li><a href="https://www.longtermwiki.com/wiki/E2054">AI Chip Governance Supply Chain | Longterm Wiki</a></li>
<li><a href="https://www.globaltimes.cn/page/202611/1374231.shtml">SMIC’s Q3 net profit more than doubles as domestic... - Global Times</a></li>
<li><a href="https://www.bbc.com/news/articles/cmdx1vpprk9vo">Suspected China spy linked to Nvidia &#x27;s ex-boss left in 2025...</a></li>

</ul>
</details>

**Tags**: `#AI chips`, `#export controls`, `#US Congress`, `#Nvidia`, `#semiconductor policy`

---

<a id="item-tech-news-6"></a>
### [Datasette 0.65.6 Security Backport](https://simonwillison.net/2026/Nov/15/datasette-2/) ⭐️ 6.0/10

Datasette 0.65.6 backports a minor security fix from version 1.0a43. The fix prevents a database registered with \`add\_database\(db, name=..., route=...\)\`, where the custom route differs from its name, from being downloaded at \`/&lt;route&gt;.db\` by actors who were denied access to it. The maintenance release makes the correction available to users of the 0.65 release line.

rss · Simon Willison · Nov 15, 23:18

**「Background」** Datasette supports registering a database with both a name and a custom route through \`add\_database\(db, name=..., route=...\)\`. The relevant access-control distinction is between that route and the database&\#x27;s registered name, because a mismatched route could expose the database at a downloadable URL despite an access denial.

**「Impact」** Operators running Datasette deployments with custom database routes should upgrade to 0.65.6 to prevent denied users from downloading affected databases through \`/&lt;route&gt;.db\`.

**Tags**: `#Datasette`, `#Security patch`, `#Access control`, `#Release notes`

---

<a id="item-tech-news-7"></a>
### [Apple Smart Glasses Rumors Highlight No-AR First Model](https://www.theverge.com/tech/1033968/apples-first-smart-glasses-are-coming-together) ⭐️ 6.0/10

Apple’s first smart glasses are reportedly being assembled, with Bloomberg’s Mark Gurman saying they may be unveiled at WWDC in June 2026, although the supplied reports conflict on timing: one cites shipments before the end of 2025, while another targets 2027 for the N50 model. The first device is expected to omit augmented-reality displays, focus on Siri and iPhone integration, require a newer iPhone, and offer no Android support, with third-party applications continuing to run on the phone. Prototypes are described as slightly thinner than Meta’s second-generation Ray-Ban glasses and using a three-pin magnetic charging system that can charge while worn. Apple reportedly faces schedule pressure because its software and AI work is lagging, making a delay possible.

rss · The Verge · Nov 15, 16:59

**「Background」** Apple’s first rumored smart glasses, internally codenamed N50, are reportedly targeted for a June 2027 WWDC unveiling and shipments before the end of 2027, although the schedule could still slip. Unlike augmented-reality glasses, the initial model is expected to have no AR display and instead emphasize Siri and iPhone app integration, requiring a recent iPhone and running third-party applications on the phone.

**「Practical impact」** If Apple’s rumored first-generation design is accurate, buyers would get an iPhone-dependent smart-glasses wearable without augmented-reality displays, making it unsuitable for users whose primary goal is AR; Apple has not confirmed the product, release date, or final compatibility requirements.

<details><summary>References</summary>
<ul>
<li><a href="https://www.macrumors.com/2026/11/15/apple-smart-glasses-hinge-on-siri/">Apple&#x27;s Smart Glasses Strategy Hinges on Siri and iPhone ...</a></li>
<li><a href="https://vr.org/articles/apple-smart-glasses-wwdc-2027-privacy-camera-decision-2026">Gurman Puts Apple&#x27;s First Smart Glasses at WWDC 2027, and the ...</a></li>

</ul>
</details>

**Tags**: `#smart glasses`, `#Apple`, `#wearables`, `#hardware rumors`, `#WWDC`

---

<a id="item-tech-news-8"></a>
### [Bharat Semi Raises $24M for AI Sensors](https://techcrunch.com/2026/11/15/indian-chip-startup-bharat-semi-lands-24m-seed-round-as-it-eyes-global-ai-sensor-market/) ⭐️ 6.0/10

Indian chip startup Bharat Semi has raised a $24 million seed round as it targets the global market for AI-enabled sensors. The company says it has secured design wins with organizations including General Atomics, indicating potential customer interest in its technology. The available report does not identify the investors, explain the sensor’s technical capabilities, or clarify whether the design wins are prototypes, commitments, or production deployments. As a result, the funding represents early-stage validation, but its near-term commercial impact remains uncertain.

rss · TechCrunch · Nov 15, 23:30

**「Context」** In hardware, a design win means a customer has selected a component or platform for a planned product or program; it does not necessarily mean production has begun or revenue has been realized. General Atomics&\#x27; Ranger and GA-Ray unmanned platforms use modular, open architectures that support mission payloads, autonomy software, acoustic sensors, and quantum-enabled sensors, which provides relevant context for Bharat Semi’s claim of AI-sensor design wins involving General Atomics. A seed round is early-stage financing typically used to develop a technology and validate initial commercial demand.

**「Defense sensor foothold」** The reported design win positions Bharat Semi to supply AI-enabled sensors to General Atomics, a defense and technology company involved in unmanned aircraft and related mission systems, while its $24 million seed round funds continued development. Production timing, volumes, and commercial terms were not disclosed, so immediate deployment remains unconfirmed.

<details><summary>References</summary>
<ul>
<li><a href="https://www.thedefensenews.com/General-Atomics-Unveils-Two-Long-Range-Underwater-Drones-Ranger-and-GA-Ray-at-Euronaval-2026/">General Atomics Unveils Two Long-Range Underwater Drones...</a></li>
<li><a href="https://www.ga.com/">Welcome to General Atomics | General Atomics</a></li>
<li><a href="https://www.ga-asi.com/">Welcome to General Atomics Aeronautical Systems (GA-ASI)</a></li>

</ul>
</details>

**Tags**: `#semiconductors`, `#AI sensors`, `#startup funding`, `#India`

---

<a id="item-tech-news-9"></a>
### [Microsoft Raises Azure Prices in India, Cuts China Costs](https://www.theregister.com/off-prem/2026/11/15/microsoft-lifts-indian-cloud-prices-by-15-percent-cuts-costs-in-china/5309993) ⭐️ 6.0/10

Microsoft reportedly increased prices for its Azure cloud services in India by 15% while reducing costs in China. The change represents a divergence in regional cloud pricing and could raise procurement and operating costs for organizations hosting workloads in India while benefiting customers in China. The supplied report does not specify which Azure services or SKUs changed, the new price levels, an effective date, or the reasons for the adjustments, so the scope of the increase and reduction remains unclear.

rss · The Register · Nov 15, 23:46

**「Cloud pricing context」** Microsoft&\#x27;s commercial cloud services are quoted in local currency in many markets, so the company periodically revisits those list prices to keep local-currency rates aligned with its global pricing levels. Starting in 2027, Microsoft says it will apply these revisions as a yearly cycle spanning five currencies, with the first round taking effect on January 1, 2027. That same first round also raised New Zealand prices by 10 percent, showing the adjustments run across several markets rather than affecting India alone.

**「Customer Cost Impact」** Indian Azure customers may face roughly 15% higher cloud-service bills, potentially encouraging workload optimization or relocation, while lower prices in China may make Chinese regions more attractive for affected deployments. The supplied report does not identify the affected services or regions, so customers should verify pricing for their specific Azure footprint before changing architecture.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theregister.com/off-prem/2026/11/15/microsoft-lifts-indian-cloud-prices-by-15-percent-cuts-costs-in-china/5309993">Microsoft lifts Indian cloud prices by 15 percent, cuts costs ...</a></li>
<li><a href="https://tbreak.com/microsoft-commercial-cloud-pricing-currency-2027/">Microsoft commercial cloud pricing rises 15.7% in India</a></li>
<li><a href="https://learn.microsoft.com/en-us/answers/questions/6025662/is-there-any-official-announcement-for-azure-vm-in">Is There any official announcement for Azure VM (in 7 regions ...</a></li>

</ul>
</details>

**Tags**: `#Microsoft Azure`, `#cloud pricing`, `#India`, `#China`

---

<a id="item-tech-news-10"></a>
### [Toward a Nonperturbative Lattice Standard Model](https://openai.com/index/step-toward-defining-the-standard-model) ⭐️ 6.0/10

OpenAI reports work toward a candidate nonperturbative lattice definition of the Standard Model, an approach intended to describe the theory without relying on perturbative expansions around continuous spacetime. The announcement says GPT-6 Astra assisted in turning the idea into a detailed proof. However, it provides no methodology, validation results, paper details, or independent corroboration, leaving the work&\#x27;s completeness and scientific significance uncertain. As presented, the item is a preliminary claim of progress rather than evidence that a fully established lattice formulation of the Standard Model has been achieved.

rss · OpenAI News · Nov 15, 22:00

**「Background」** A lattice formulation places quantum fields on a discrete spacetime grid, while a nonperturbative definition is intended to describe the theory without relying on expansions in small interaction strengths. Such a construction could enable controlled numerical study of the full Standard Model beyond conventional perturbative approximations. The proposal discussed here remains a candidate, with GPT-6 Astra contributing to the detailed proof work.

**「Impact」** Researchers in lattice field theory and AI-assisted science can now examine a candidate nonperturbative lattice formulation of the Standard Model and the detailed proof developed with GPT-6 Astra, providing a concrete starting point for further validation and implementation. Because the supplied account gives no peer review, methodology, or independent corroboration, it should not yet be treated as a validated definition of the Standard Model.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/step-toward-defining-the-standard-model/">A step toward defining the Standard Model on a lattice - OpenAI</a></li>
<li><a href="https://grafy.ai/news/openai-unveils-lattice-based-standard-model-proof-with-gpt-6-astra">OpenAI unveils lattice‑based Standard Model — Grafy News</a></li>
<li><a href="https://thedefiant.io/frontier/ai/openai-details-astra-s-role-in-standard-model-lattice-proof">OpenAI Details Astra&#x27;s Role in Standard Model Lattice Proof</a></li>
<li><a href="https://openai.com/index/step-toward-defining-the-standard-model/">A step toward defining the Standard Model on a lattice | OpenAI</a></li>

</ul>
</details>

**Tags**: `#lattice field theory`, `#Standard Model`, `#AI-assisted research`, `#scientific computing`

---

## Financial News

<a id="item-finance-news-1"></a>
### [China’s slowdown deepens in October as industrial output, retail sales, investment miss estimates](https://www.cnbc.com/2026/11/16/china-retail-sales-october-industrial-output-investment.html) ⭐️ 8.0/10

China&\#x27;s October data confirmed a broad domestic slowdown as weak consumption and collapsing investment outweighed strong exports, raising risks to global growth and intensifying trade tensions.

rss · CNBC Finance · Nov 16, 03:53

**Tags**: `#China`, `#Economic Data`, `#Domestic Demand`, `#Trade Surplus`, `#Global Growth`

---

<a id="item-finance-news-2"></a>
### [Lutnick faces questions over Cantor Fitzgerald’s Nvidia ties amid China espionage concerns](https://www.cnbc.com/2026/11/13/howard-lutnick-nvidia-jensen-huang-china-cantor-fitzgerald.html) ⭐️ 8.0/10

Commerce Secretary Howard Lutnick faced renewed scrutiny after Nvidia CEO Jensen Huang resigned and reports said Lutnick received a classified warning about Huang’s ties to a suspected Chinese spy. Cantor Fitzgerald, now led by Lutnick’s sons, cut its reported Nvidia share count by 49% between September 2025 and March 2026 while continuing to arrange financing for Nvidia business partners, raising government-ethics and conflict-of-interest concerns. CNBC found no evidence that the sons had advance knowledge, that the holdings changes were linked to intelligence warnings, or that the firm’s interests influenced Lutnick’s decisions; President Trump maintains “complete confidence” in the secretary.

rss · CNBC Finance · Nov 15, 19:58

**Tags**: `#Nvidia`, `#AI chip export controls`, `#China`, `#government ethics`, `#Cantor Fitzgerald`

---