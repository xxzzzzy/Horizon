---
layout: default
title: "Horizon Summary: 2026-11-08 (EN)"
date: 2026-11-08
lang: en
---

> From 82 items, 12 important content pieces were selected

---

**Technology News**
1. [Does DeepSWE Scores Survive Task-Specification Changes?](#item-tech-news-1) ⭐️ 8.0/10
2. [Qwen3.8 27B KV-Cache Quantization Results](#item-tech-news-2) ⭐️ 8.0/10
3. [Claude Code settings exposed secrets in 1,122 public files](#item-tech-news-3) ⭐️ 7.0/10
4. [China’s 800MW AI Campus: 800V DC Pilot and Chiller-Free Cooling](#item-tech-news-4) ⭐️ 7.0/10
5. [Questions Raised Over Nvidia H200 Vetting for Chinese Firms](#item-tech-news-5) ⭐️ 7.0/10
6. [Why a new report on Anthropic automating AI development is alarming researchers](#item-tech-news-6) ⭐️ 7.0/10
7. [Tesla winds down Cybertruck for Cybercab](#item-tech-news-7) ⭐️ 6.0/10
8. [U.S. Memo Alleges Chinese Recruitment to Spy on Nvidia CEO](#item-tech-news-8) ⭐️ 6.0/10
9. [Sequoia Ends Its Scouts Program](#item-tech-news-9) ⭐️ 6.0/10
10. [Big Tech Courts Democrats Ahead of the Midterms](#item-tech-news-10) ⭐️ 6.0/10
11. [OpenAI Reportedly Raises $11B at $1.25T Valuation](#item-tech-news-11) ⭐️ 6.0/10

**Financial News**
1. [Berkshire doubles buybacks as quarterly earnings fall](#item-finance-news-1) ⭐️ 8.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Does DeepSWE Scores Survive Task-Specification Changes?](https://maxxbench.unlap.ai/research/why-maxxbench/) ⭐️ 8.0/10

MaxxBench tests whether strong DeepSWE benchmark results remain reliable when task specifications change, asking whether models genuinely solve software-engineering tasks or merely fit the benchmark’s original framing. The analysis finds that performance can shift substantially under specification changes, with the sensitivity varying across models, and also identifies bugs in the benchmark itself. These flaws make a high DeepSWE score an unreliable standalone measure of general software-engineering ability and support testing models across meaningfully varied task setups. The Hacker News discussion received 226 points and 67 comments, reflecting broad technical interest in the critique.

hackernews · antiuniverse · Nov 7, 17:19 · [Discussion](https://news.ycombinator.com/item?id=50406222)

**「Background」** DeepSWE is a coding benchmark whose scores may depend on how closely models match benchmark-specific task expectations, so varying those expectations tests whether performance generalizes. MaxxBench modifies the instructions or starter code in 89 DeepSWE tasks—such as requiring lowercase filenames or UTC timestamps—while keeping median patch growth to 17 lines \(3.5%\), exposing model sensitivity that an unmodified leaderboard score can conceal.

**「Deployment implication」** Developers and organizations evaluating coding agents should not treat a headline DeepSWE score as robust standalone evidence of capability, because specification changes and benchmark bugs can materially affect model performance; they should stress-test tasks with varied specifications before making model-selection decisions.

**「Community Reaction」** Commenters broadly viewed varying task specifications as a useful first-order generalization test, while expressing concern about DeepSWE bugs and arguing that labs should vary their RL training environments rather than assume benchmark-like conditions. One commenter interpreted the results as smaller “-flash” models collapsing fastest—highlighting GPT-5.6-Sol versus GPT-5.6-Luna—while noting that GLM-5.3 and GLM-5.3-flash are distinct lineages and should not be treated as a simple size-versus-quality comparison.

<details><summary>References</summary>
<ul>
<li><a href="https://daily.dev/posts/maxxbench-nice-deepswe-score-but-is-it-true--ue9ulip60">MaxxBench – &quot;Nice DeepSWE score. But is it true?&quot;</a></li>
<li><a href="https://maxxbench.unlap.ai/research/why-maxxbench/">Introducing MaxxBench: Benchmarking Task Adaptation and ...</a></li>
<li><a href="https://news.ycombinator.com/item?id=50406222">MaxxBench – &quot;Nice DeepSWE score. But is it true?&quot; | Hacker News</a></li>

</ul>
</details>

**Tags**: `#LLM benchmarks`, `#benchmark validity`, `#AI evaluation`, `#DeepSWE`, `#software engineering`

---

<a id="item-tech-news-2"></a>
### [Qwen3.8 27B KV-Cache Quantization Results](https://www.reddit.com/r/LocalLLaMA/comments/1xqbesv/effects_of_kv_cache_quantization_on_qwen38_27b/) ⭐️ 8.0/10

A study testing Qwen3.8 27B across 35 weight quantizations in llama.cpp, ExLlamaV3, and vLLM found that 8-bit KV-cache quantization provides a strong memory-saving and output-quality tradeoff for contexts up to 64k tokens. In llama.cpp and ExLlamaV3, 8-bit caches reduce storage from 64 to 34 KiB per token—saving about 1.9 GiB at 64k—while changing KL divergence by less than 0.00012; vLLM&\#x27;s 32-KiB FP8 cache saves 2.0 GiB and increases KL divergence by 0.0004 to 0.0006. Four-bit caches use 18 KiB per token and save 2.9 GiB at 64k, but their measurable impact grows with context, including 15–30% more added KL divergence at 16k–32k tokens than during the first 4k, so the author does not recommend them. The 4-bit penalty is particularly pronounced with precise weights: for example, Q8\_0 weights rise from about 0.0007 KL divergence with a 16-bit cache to 0.0034, while the author suggests 4-bit caching may only merit consideration for Q3-class or lower-weight quants. These results are useful for VRAM-constrained local inference, but they are based on one model and a KL-divergence-focused dataset and therefore require broader validation.

reddit · r/LocalLLaMA · /u/Hefty\_Wolverine\_553 · Nov 7, 17:09

**「Background」** In autoregressive LLM inference, the key/value \(KV\) cache stores attention state for previously generated tokens, so its memory use grows with context length; quantizing that cache reduces per-token precision and memory without changing the model weights. The study evaluates llama.cpp, ExLlamaV3, and vLLM using KL divergence between each quantized model and an unquantized bf16 reference to measure changes in next-token probability distributions, alongside top-1 agreement. Its 35 weight quantizations and contexts up to 64k tokens extend earlier anecdotal debate over whether cache precision should be reduced.

**「Practical impact」** Local Qwen3.8 27B users can use 8-bit KV caches in llama.cpp or ExLlamaV3 to reduce 64k-context cache memory by about 1.9 GiB—roughly half—with effectively negligible measured distributional drift, making them a practical VRAM-saving option; 4-bit caches remain a poor trade-off because their divergence grows with context and vLLM does not offer them.

<details><summary>References</summary>
<ul>
<li><a href="https://designprincipia.com/post/qwen3.8-kv-quantization-analysis/">Measuring impact of KV quantization on Qwen3.8</a></li>

</ul>
</details>

**Tags**: `#KV-cache quantization`, `#Qwen3.8 27B`, `#LLM inference`, `#llama.cpp`, `#vLLM`

---

<a id="item-tech-news-3"></a>
### [Claude Code settings exposed secrets in 1,122 public files](https://apiiro.com/blog/coding-agents-leaking-secrets-github-dont-ask-again) ⭐️ 7.0/10

A study scanning public GitHub repositories found embedded credentials in 1,122 files associated with committed Claude Code local settings, highlighting a secret-leakage risk in AI coding-agent workflows. The exposure does not appear to result from clicking “Don&\#x27;t Ask Again” by itself; it requires secrets to be embedded in approved commands saved in \`.claude/settings.local.json\`, for that local file to be manually committed, and for the repository to be published. Claude Code automatically gitignores the file when Claude creates it and intends it to remain local, but the team said it historically has not performed secret scrubbing and is considering ways to prevent such leaks. Developers can reduce risk by keeping local settings out of version control, using secret-scanning tools, and limiting agent access through private repositories, allowlisted release pipelines, isolated VMs, or restricted API proxies.

hackernews · shmulc · Nov 7, 20:45 · [Discussion](https://news.ycombinator.com/item?id=50407882)

**「How Claude Code stores permissions」** Claude Code, Anthropic’s AI coding agent, normally asks permission before running most shell commands. Selecting “Yes, and don’t ask again” writes an allow rule to \`.claude/settings.local.json\` so matching commands can run without further prompts; if an approved command contains a literal password or API key, that secret can be stored in plaintext in the project. The settings file is intended to remain local and is automatically gitignored when Claude creates it, so public exposure requires it to be manually committed or otherwise published rather than resulting from the button alone.

**「Impact」** Developers who use “Don’t Ask Again” for commands containing secrets must keep \`.claude/settings.local.json\` untracked and rotate any credentials already published, because committing that file can expose them in a repository. The risk requires manually created local settings to be committed—the button alone does not publish secrets—and permission deny rules can further restrict Claude Code from reading \`.env\`, secret, and credential files.

**「Community Discussion」** Discussion centered on the headline being misleading because the vulnerable chain depended on committing manually created local settings containing secret-bearing approved commands, not on the permission button alone. The Claude Code team said \`.claude/settings.local.json\` is meant to remain local and is automatically gitignored when created, while commenters suggested private development repositories, allowlisted public release flows, ephemeral VMs, and restricted API proxies as additional safeguards.

<details><summary>References</summary>
<ul>
<li><a href="https://madrobot.blog/2026/11/07/claude-code-dont-ask-again-secrets-github/">Claude Code “Don’t ask again” left secrets in 1,122 GitHub files</a></li>
<li><a href="https://thehackernews.com/2026/11/claude-codes-dont-ask-again-file.html">Claude Code&#x27;s “Don&#x27;t Ask Again” File Exposes Passwords and ...</a></li>
<li><a href="https://github.com/chuckreynolds/claude-secret-guardrails">GitHub - chuckreynolds/ claude - secret -guardrails: Permission deny...</a></li>
<li><a href="https://dev.to/vildandenai/keep-personal-claude-code-settings-out-of-git-with-settingslocaljson-3hld">Keep personal Claude Code settings out of git with settings . local . json</a></li>

</ul>
</details>

**Tags**: `#AI coding agents`, `#secret leakage`, `#GitHub security`, `#Claude Code`, `#developer tooling`

---

<a id="item-tech-news-4"></a>
### [China’s 800MW AI Campus: 800V DC Pilot and Chiller-Free Cooling](https://newsletter.semianalysis.com/p/we-visited-chinas-stargate-in-inner) ⭐️ 7.0/10

The article reports a visit to an AI data-center campus in Inner Mongolia, China, described as wind-powered and sized at 800MW. The site had built out 120MW within a year, demonstrating a rapid construction pace. It includes a 5MW SST-native 800V DC pilot and a cooling architecture that operates without central chillers. The visit presents concrete design choices for scaling AI infrastructure, although the supplied excerpt does not provide enough data to verify efficiency, cost, reliability, or other performance claims.

rss · Semianalysis · Nov 7, 19:01

**「Background」** The project is in Inner Mongolia, a northern Chinese autonomous region that borders Mongolia and Russia and provides large areas for wind generation and data-center construction. In data centers, 800V DC is a higher-voltage direct-current distribution architecture, while an “SST-native” pilot uses solid-state transformers designed to support it; the chiller-free approach operates without the centralized chilled-water plant commonly used for large-scale rack cooling.

**「Implications for AI Infrastructure」** For AI data-center operators and hardware designers, the project provides a reported reference case for combining large-scale wind power, an 800V DC pilot, and cooling without central chillers, while the available excerpt leaves deployment economics and measured performance unestablished.

<details><summary>References</summary>
<ul>
<li><a href="https://www.travelchinaguide.com/cityguides/inner_mongolia/">Inner Mongolia China : Third Largest Province with Prairie Scenery</a></li>

</ul>
</details>

**Tags**: `#AI data centers`, `#800V DC power`, `#data-center cooling`, `#renewable energy`, `#China`

---

<a id="item-tech-news-5"></a>
### [Questions Raised Over Nvidia H200 Vetting for Chinese Firms](https://www.theverge.com/ai-artificial-intelligence/1029483/nvidia-ai-chips-china-blacklist-government) ⭐️ 7.0/10

The New York Times reports that New Matrix appears on a list of Chinese firms approved to receive Nvidia H200 AI chips, despite having empty offices and being described as a &quot;hollow gray shell.&quot; The report raises concerns about the due diligence performed by both Nvidia and the U.S. Commerce Department before approving Chinese firms to handle the chips. If legitimate customers are not properly identified, the process could undermine efforts to track AI hardware and enforce U.S. export restrictions. The supplied account does not include New Matrix&\#x27;s response, details of the vetting process, or evidence that other approved firms are similarly empty.

rss · The Verge · Nov 7, 15:43

**「H200 export controls」** Nvidia’s H200 is an AI accelerator whose export to China requires approval under U.S. export controls. The Commerce Department reportedly approved dozens of Chinese companies to buy or handle the chips, while The New York Times said some had ties to entities sanctioned on national-security grounds. New Matrix appeared on the approved list, but reporters visiting its registered Beijing address found vacant premises, raising questions about how recipients were vetted.

**「Export-control risk」** If an apparently hollow company was cleared without meaningful due diligence, the reported approval could weaken safeguards on Nvidia H200 sales to China and expose Nvidia and the Commerce Department to greater regulatory and national-security scrutiny.

<details><summary>References</summary>
<ul>
<li><a href="https://www.nytimes.com/2026/11/07/business/economy/nvidia-chips-chinese-firms.html">U.S. Cleared Nvidia Chips to Chinese Firms With Empty Offices ...</a></li>
<li><a href="https://tech-insider.org/nvidia-h200-new-matrix-empty-beijing-office-commerce-approval-2026/">Nvidia H200 China Approval Hits an Empty Office [2026]</a></li>

</ul>
</details>

**Tags**: `#AI chips`, `#export controls`, `#Nvidia`, `#China`, `#AI policy`

---

<a id="item-tech-news-6"></a>
### [Why a new report on Anthropic automating AI development is alarming researchers](https://www.theverge.com/ai-artificial-intelligence/1029126/anthropic-metr-report-accelerating-ai-development) ⭐️ 7.0/10

METR&\#x27;s 11-week investigation reports that Anthropic&\#x27;s models appear to be improving roughly twice as fast as a year earlier, raising concerns about accelerating AI development.

rss · The Verge · Nov 7, 12:30

**Tags**: `#Anthropic`, `#AI development`, `#AI safety`, `#METR`, `#model scaling`

---

<a id="item-tech-news-7"></a>
### [Tesla winds down Cybertruck for Cybercab](https://www.theverge.com/transportation/1029460/elon-musk-cybertruck-death-election-backlash) ⭐️ 6.0/10

The Verge reports that Elon Musk announced on Friday that Tesla would &quot;winding down&quot; Cybertruck production next year to make room for the Cybercab. The outlet frames the decision as a humiliating end for a vehicle once highly hailed, with its &quot;time of death&quot; marked as November 6 at 1:30 a.m. &quot;by tweet.&quot; Strategically, the move shifts Tesla’s manufacturing attention from Cybertruck toward Cybercab, although the supplied excerpt provides little detail on production volumes, timing, or support for existing vehicles. Because the article is primarily opinionated commentary, the announcement is its central reported fact rather than a broader conclusion about the vehicles’ commercial performance.

rss · The Verge · Nov 7, 14:40

**「Product Context」** The Cybertruck is Tesla’s battery-electric pickup, while the Cybercab is the company’s planned autonomous ride-hailing vehicle. Winding down the former to make room for the latter signals a shift in Tesla’s product priorities and use of manufacturing capacity.

**「Practical Consequence」** Tesla is reallocating production capacity from Cybertruck to Cybercab, potentially giving prospective Cybertruck buyers a narrower window to obtain one. The reported announcement does not specify what happens to sales, service, parts, or support for existing owners after production ends.

**Tags**: `#Tesla`, `#Cybertruck`, `#Cybercab`, `#electric vehicles`, `#automotive industry`

---

<a id="item-tech-news-8"></a>
### [U.S. Memo Alleges Chinese Recruitment to Spy on Nvidia CEO](https://techcrunch.com/2026/11/07/chinese-exec-was-recruited-to-spy-on-nvidia-ceo-according-to-us-intelligence-memo/) ⭐️ 6.0/10

A U.S. intelligence memo circulated earlier in 2026 reportedly alleged that China’s Ministry of State Security recruited a female Megaspeed executive to spy on Nvidia’s CEO. The supplied account does not identify the executive, explain what information was sought, or reproduce the memo’s supporting details. It also provides no independent verification of the allegation or responses from Nvidia, Megaspeed, or the executive. The claim raises concerns about state-sponsored corporate espionage involving a major AI-chip company, but the limited reporting does not establish whether the alleged operation occurred or its scope.

rss · TechCrunch · Nov 7, 21:17

**「Context」** Jensen Huang is the CEO of Nvidia, the company central to the allegation. The cited memo reportedly identified Alice Huang, a Chinese technology executive who developed a relationship with Jensen Huang, as an asset of China’s Ministry of State Security, described in supporting reports as the country’s main civilian intelligence agency. The accounts present the recruitment as an intelligence allegation rather than an independently established finding in the supplied material.

**「Impact on Nvidia and chip controls」** If the memo’s allegation is accurate, the Ministry of State Security effort sought intelligence on U.S. AI chips and influence over Nvidia’s access to advanced chips for China. Because the memo’s details and the executive’s identity remain unverified, the concrete consequence is heightened potential insider-threat and export-control scrutiny, not a demonstrated change in Nvidia’s operations or chip availability.

<details><summary>References</summary>
<ul>
<li><a href="https://techcrunch.com/2026/11/07/chinese-exec-was-recruited-to-spy-on-nvidia-ceo-according-to-us-intelligence-memo/">Megaspeed exec was recruited to spy on Nvidia CEO, according ...</a></li>
<li><a href="https://www.nytimes.com/2026/11/06/us/politics/chinese-spy-agency-nvidia-jensen-huang.html">China’s Top Spy Agency Recruited Woman Who Targeted Jensen ...</a></li>
<li><a href="https://www.yahoo.com/news/politics/articles/nvidia-ceo-jensen-huang-alleged-103955689.html?fr=sycsrp_catchall">Nvidia CEO Jensen Huang’s Alleged Chinese Spy ... - Yahoo</a></li>
<li><a href="https://www.theverge.com/tech/1029338/nvidia-ceo-jensen-huang-china-spy">China reportedly recruited AI exec to spy on Jensen Huang | The Verge</a></li>
<li><a href="https://www.globaltimes.cn/page/202611/1373811.shtml">China ‘isn&#x27;t buying’ Nvidia chips . Why are some... - Global Times</a></li>

</ul>
</details>

**Tags**: `#Nvidia`, `#corporate espionage`, `#AI chips`, `#US-China technology security`

---

<a id="item-tech-news-9"></a>
### [Sequoia Ends Its Scouts Program](https://techcrunch.com/2026/11/06/sequoia-shutting-down-its-scouts-program-marks-the-end-of-an-era/) ⭐️ 6.0/10

Sequoia is shutting down its Scouts program, ending the prominent venture-capital scouting model that the firm pioneered and many other firms subsequently adopted. The move reflects growing doubts about scouting’s effectiveness, with a consensus appearing to form that the model has reached its limits in its current form. The supplied report does not specify the shutdown timeline, reasons, staffing effects, or broader consequences, so the change is best understood as a signal that venture firms may be reconsidering how they identify and engage early-stage founders rather than definitive evidence that scouting is ending across the industry.

rss · TechCrunch · Nov 7, 05:01

**「Background」** Sequoia Capital is a Menlo Park venture-capital firm investing from seed through growth stage. It pioneered the scouts model, in which scouts identify and engage early-stage founders, and is now closing that program as it consolidates after 20 years of expansion.

**「Impact」** For founders approached through Sequoia Capital’s Scouts network, the closure eliminates a prominent early-stage sourcing channel and gives other venture firms a reason to reassess scout-led talent discovery. The reported stasis in Europe’s scout-program membership suggests Sequoia’s retreat is part of a broader model reaching its limits, though it does not establish that other firms will abandon the approach.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Sequoia_Capital">Sequoia Capital - Wikipedia</a></li>
<li><a href="https://techcrunch.com/2026/11/04/sequoia-hits-rewind-undoing-20-years-of-expansion/">Sequoia hits rewind, undoing 20 years of expansion | TechCrunch</a></li>
<li><a href="https://techcrunch.com/2026/11/04/sequoia-hits-rewind-undoing-20-years-of-expansion/">Sequoia hits rewind, undoing 20 years of expansion | TechCrunch</a></li>
<li><a href="https://sifted.eu/articles/sequoia-scouts-programme-europe">Meet the Sequoia scouts currently looking to invest in... | Sifted</a></li>

</ul>
</details>

**Tags**: `#venture capital`, `#startup ecosystem`, `#talent pipeline`, `#industry analysis`

---

<a id="item-tech-news-10"></a>
### [Big Tech Courts Democrats Ahead of the Midterms](https://techcrunch.com/2026/11/06/from-the-front-row-to-the-hot-seat-what-the-midterms-mean-for-big-tech/) ⭐️ 6.0/10

Big Tech is attempting to regain Democratic favor ahead of the U.S. midterms after spending two years closely aligned with the White House. The article presents this political pivot as an image strategy that will be tested by developments involving state governments, local communities, and markets. Its central question is whether stronger ties with Democrats can withstand those broader pressures. The supplied excerpt offers no company-specific commitments, proposed policies, or measurable indicators of political support, so it provides strategic context rather than detailed technical or policy analysis.

rss · TechCrunch · Nov 7, 04:16

**「Background」** U.S. midterms are the halfway elections for Congress, and Democrats appeared likely to gain seats in 2026 after Big Tech spent two years cultivating close ties with the White House. That federal political realignment is unfolding alongside separate pressure from state and local governments: an Ohio county passed a data-center ban affecting a planned 700,000-square-foot Meta facility, while communities across the state overwhelmingly rejected data centers. These developments help explain why companies such as Meta are reaching toward Democrats even as their infrastructure plans face growing resistance closer to home.

**「Impact on Big Tech」** For Big Tech, regaining Democratic favor may not offset mounting pressure from state and local governments and markets, leaving the industry more exposed to regulatory and legal actions as it loses federal benefits such as tax breaks, paused investigations, and looser AI rules. The article does not specify which new policies or enforcement actions will materialize.

<details><summary>References</summary>
<ul>
<li><a href="https://techcrunch.com/2026/11/06/from-the-front-row-to-the-hot-seat-what-the-midterms-mean-for-big-tech/">From the front row to the hot seat — what the midterms mean ...</a></li>
<li><a href="https://techcrunch.com/2026/11/04/after-the-midterms-a-bigger-clash-over-data-centers-could-be-coming/">After the midterms, a bigger clash over data ... - TechCrunch</a></li>
<li><a href="https://www.newsbreak.com/techcrunch-com-332114314/4991679703344-from-the-front-row-to-the-hot-seat-what-the-midterms-mean-for-big-tech">From the front row to the hot seat — what the midterms mean ...</a></li>
<li><a href="https://techcrunch.com/2026/11/06/from-the-front-row-to-the-hot-seat-what-the-midterms-mean-for-big-tech/">From the front row to the hot seat — what the midterms mean for Big ...</a></li>

</ul>
</details>

**Tags**: `#Big Tech`, `#technology policy`, `#US elections`, `#regulation`, `#industry analysis`

---

<a id="item-tech-news-11"></a>
### [OpenAI Reportedly Raises $11B at $1.25T Valuation](https://news.google.com/rss/articles/CBMiyAFBVV95cUxPcXl2OWY2ZWYtYmVna0o0dEtfd29hWHJVZFRYbDdFVHZaOGVQNHhQYWdzcU0zMUVnVW9LSmNVOW5ya3dZY0lJSDZDSkF6TUJvTUh0QTR0d1VGM0s1VlJTOXZEZmk5NWVpb0xCTEJ2ajllTzNJRHh1MzVydldjVTVpUWVlVDJvY2hER3hhRXhyeTE4T0hSZXBYdVRxcVhZa25udFA3MkkzcEVJVmtTcW95M0FjV3hRLVMwb1pvNE9VNDVhQjdlYmNjRw?oc=5) ⭐️ 6.0/10

Forbes Middle East reports that OpenAI secured $11 billion in new funding at a valuation of $1.25 trillion. The reported raise would provide substantial capital for the company’s AI research, infrastructure, and commercial expansion. It also places OpenAI’s valuation among the highest reported for a private AI company, underscoring the scale of investor expectations around the sector. However, the supplied headline does not identify investors, deal terms, timing, or whether the valuation was measured before or after the funding.

google\_news · Forbes Middle East · Nov 7, 16:09

**「Funding and valuation context」** A funding round supplies capital to a company, whereas its valuation is the total equity value assigned in that transaction; the $11 billion raise and $1.25 trillion valuation therefore measure different things. OpenAI had previously raised $122 billion in March at an $852 billion valuation, according to The Verge, so the new reported round would add capital while marking another substantial increase in valuation.

**「Impact on OpenAI」** OpenAI’s closed $11 billion funding tranche increases its capacity to invest in AI models, compute, and service expansion. However, the available reporting does not specify the use of proceeds or predict resulting changes to pricing, model capabilities, or product availability.

<details><summary>References</summary>
<ul>
<li><a href="https://techcrunch.com/2026/11/06/openai-reportedly-raises-an-additional-11-billion-at-a-1-25-trillion-valuation/">OpenAI reportedly raises an additional $ 11 billion at a $ 1 . 25 trillion ...</a></li>
<li><a href="https://www.theverge.com/ai-artificial-intelligence/1029380/openai-1-25-trillion-investment-valuation">OpenAI valued at $ 1 . 25 trillion , as rival Anthropic nears... | The Verge</a></li>
<li><a href="https://www.reuters.com/business/openai-secures-11-billion-funding-125-trillion-valuation-bloomberg-news-reports-2026-11-06/">OpenAI gets $11 billion funding at $1.25 trillion valuation ...</a></li>
<li><a href="https://www.bloomberg.com/news/articles/2026-11-06/openai-completes-11-billion-portion-of-funding-at-1-25-trillion-value">OpenAI Completes $11 Billion Portion of Funding at $1.25 ...</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#AI funding`, `#venture capital`, `#valuation`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Berkshire doubles buybacks as quarterly earnings fall](https://www.cnbc.com/2026/11/07/berkshire-hathaway-q3-2026-earnings-buybacks.html) ⭐️ 8.0/10

Berkshire Hathaway repurchased $9.6 billion of stock in the third quarter of 2026, more than double the $4.5 billion bought in the second quarter, while operating earnings fell 5.8% year over year to $12.705 billion and insurance underwriting profit dropped 43%.

rss · CNBC Finance · Nov 7, 15:23

**「Background」** Berkshire repurchased $4.5 billion of stock in the second quarter before increasing that pace in the third quarter as operating earnings from its wholly owned businesses fell 5.8% year over year, led by weaker insurance profits.

**「Impact」** For Berkshire shareholders, the $9.6 billion third-quarter buyback returned capital directly, while the company’s $377.4 billion cash position left it with substantial capacity for further repurchases or other investments.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/11/07/berkshire-hathaway-q3-2026-earnings-buybacks.html">Berkshire Hathaway (BRK.A) earnings Q3 2026</a></li>
<li><a href="https://portfoliotrackr.com/blog/berkshire-buybacks-rise-operating-profit-falls-q3">Berkshire Buybacks Rise as Operating Profit Falls 6% in Q3</a></li>

</ul>
</details>

**Tags**: `#Berkshire Hathaway`, `#share buybacks`, `#quarterly earnings`, `#insurance`, `#capital allocation`

---