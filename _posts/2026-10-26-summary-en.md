---
layout: default
title: "Horizon Summary: 2026-10-26 (EN)"
date: 2026-10-26
lang: en
---

> From 59 items, 5 important content pieces were selected

---

**Technology News**
1. [Apple to Unveil First Touchscreen MacBook Pro](#item-tech-news-1) ⭐️ 8.0/10
2. [Why OpenAI and Anthropic Cut LLM API Prices](#item-tech-news-2) ⭐️ 7.0/10
3. [Nanbeige releases open 33B teacher model](#item-tech-news-3) ⭐️ 7.0/10
4. [Possible hinge flaw emerges from iPhone Duo teardown](#item-tech-news-4) ⭐️ 6.0/10
5. [r/opensource adds AI ban and language restrictions](#item-tech-news-5) ⭐️ 6.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Apple to Unveil First Touchscreen MacBook Pro](https://www.bloomberg.com/news/newsletters/2026-10-25/apple-to-unveil-touch-screen-macbook-pro-executive-promotions-in-box-checker) ⭐️ 8.0/10

Bloomberg reports that Apple will unveil its first touchscreen MacBook Pro on Wednesday, bringing touch input and an OLED display to the Mac lineup. The reported models come in 14-inch and 16-inch sizes, include a Dynamic Island, and will cost more than the current MacBook Pro, which starts at $2,499. The launch marks a reversal of Apple&\#x27;s long-standing position, in which executives rejected touchscreen laptops on ergonomic grounds; the source characterizes the change as being driven more by revenue and marketing, with touch serving as a complement to the keyboard and trackpad. Specific interaction details, compatibility, and other official launch information were not provided and remain to be confirmed by Apple.

telegram · zaihuapd · Oct 25, 14:25

**「A notable MacBook Pro design shift」** Apple executives have long resisted touchscreen laptops on ergonomic grounds, while MacBook Pro traditionally emphasized keyboard-and-trackpad use; a touch-enabled model would therefore represent a notable change in the line’s interaction model. Reports describe the planned 14- and 16-inch machines as the first MacBook Pros with OLED and touch input, with testing reportedly underway alongside the macOS 27.2 beta. The proposed move also follows a broader shift from the existing $2,499 starting-price tier, although pricing, compatibility, and software behavior remain subject to Apple’s official announcement.

**「Impact on Mac users and developers」** Mac users would gain touch as a supplementary input on premium 14- and 16-inch MacBook Pros, while developers may need to support reported macOS interface changes associated with the Dynamic Island. Apple’s final interaction model, APIs, and compatibility requirements remain unconfirmed.

<details><summary>References</summary>
<ul>
<li><a href="https://www.macrumors.com/2026/10/25/macbook-pro-with-touchscreen-on-wednesday/">Apple Reportedly Announcing MacBook Pro With OLED Touchscreen ...</a></li>
<li><a href="https://www.macrumors.com/2026/10/01/oled-macbook-pro-release-date/">MacBook Pro With OLED Touch Screen Rumored to Launch in ...</a></li>
<li><a href="https://www.bloomberg.com/news/articles/2026-02-24/apple-s-touch-screen-macbook-pro-to-have-dynamic-island-new-interface">Apple’s Touch-Screen Laptop to Have Dynamic Island, New Mac ...</a></li>
<li><a href="https://www.macworld.com/article/3070324/touchscreen-macbook-pro-to-feature-dynamic-island-and-big-macos-changes.html">Apple’s touchscreen MacBook Pro might get its own Dynamic Island</a></li>

</ul>
</details>

**Tags**: `#苹果`, `#MacBook Pro`, `#触控屏`, `#OLED`, `#硬件`

---

<a id="item-tech-news-2"></a>
### [Why OpenAI and Anthropic Cut LLM API Prices](https://minimaxir.com/2026/10/cheap-llms/) ⭐️ 7.0/10

The article examines reports that OpenAI and Anthropic reduced prices for some LLM APIs by as much as 80% within a few months. It explores competitive pressure, inference-cost efficiency, and hardware economics as factors behind the declines. The analysis also considers the implications for provider pricing, data policies, and regulation, while characterizing cheaper access as an industry trend rather than a single technical breakthrough. Exact model-by-model price changes and supporting cost calculations are not available in the supplied source material, so the scope and causes of the reductions remain unverified.

hackernews · minimaxir · Oct 25, 21:11 · [Discussion](https://news.ycombinator.com/item?id=50236102)

**「API Pricing and Inference Economics」** LLM API pricing is generally measured per input and output token, with providers sometimes charging less for cached prompts because reusing processed context reduces inference work. The cuts discussed here date from mid-2026: the supplied results say GPT-5.6 Luna dropped 80% in July, while Opus 5.5’s deeper cache-read discounts reduced total costs by 40–60% relative to Opus 5. Developers therefore need to compare total workload cost—including token mix, cache use, latency, and output quality—rather than relying on headline per-token prices alone.

**「Practical impact」** Developers and organizations able to switch providers can materially lower inference costs—by as much as 80% on the affected prices—making high-volume, production-scale LLM applications more economical. Actual savings depend on the selected model, usage pattern, and applicable pricing terms.

**「Community Reactions」** Commenters broadly connect lower prices to competition and serving efficiency, with one user saying Kimi and GLM were cheaper and avoided OpenAI or Anthropic cybersecurity refusals that blocked their work. Others raise less settled concerns about demand, GPU utilization, regulation, zero-data-retention policies, and whether user outputs subsidize pricing; DeepSeek’s claimed revenue-per-GPU economics was cited as a rough comparison rather than verified OpenAI or Anthropic data.

<details><summary>References</summary>
<ul>
<li><a href="https://minimaxir.com/2026/10/cheap-llms/">OpenAI and Anthropic cut their LLM prices by up to 80% within ...</a></li>
<li><a href="https://daily.dev/posts/openai-and-anthropic-cut-their-llm-prices-by-up-to-80-within-a-few-months-why--qwjt9m0rl">OpenAI and Anthropic cut their LLM prices by up to 80%...</a></li>

</ul>
</details>

**Tags**: `#large-language-models`, `#inference-economics`, `#api-pricing`, `#openai`, `#anthropic`

---

<a id="item-tech-news-3"></a>
### [Nanbeige releases open 33B teacher model](https://www.reddit.com/r/MachineLearning/comments/1xf6x35/nanbeige_releases_nanbeige4333b_an_apache_20/) ⭐️ 7.0/10

Nanbeige released Nanbeige4.3-33B under the Apache 2.0 license as a teacher model for agent tasks and planned smaller models, including an upcoming 3B agent. The model card lists a 512K context window and reports 80.9 on Terminal-Bench 2.1, compared with 73.0 for Qwen3.8-27B under the same harness and inference settings for that benchmark. It does not lead on every evaluation: the reported SWE-Bench Pro score is 60.3 versus 61.7 for Qwen3.8-27B. These results come from the releasing team rather than independent replication, and the agent evaluations retain prior reasoning with preserve\_thinking=true, a setting recommended for multi-turn tool use but not general chat.

reddit · r/MachineLearning · /u/jatingargiitk · Oct 25, 16:32

**「Teacher Models and Distillation」** In model distillation, a larger “teacher” model supplies reasoning or task trajectories for training a smaller “student” model, with the goal of transferring capabilities to a more compact agent. Nanbeige4.3-33B is a 33B dense, Apache 2.0-licensed model with a 512K context window, intended to serve as the teacher for future smaller agents, including a planned 3B model. For multi-turn tool use, \`preserve\_thinking=true\` retains earlier reasoning between turns; because this setting can influence task success and token consumption, benchmark comparisons should hold it and other inference conditions fixed.

**「Impact」** Developers can download, modify, and deploy the 33B dense model under Apache 2.0, giving smaller-agent teams an openly licensed teacher for planned distillation work, including a 3B model. Its benchmark advantage remains provisional because the results are self-reported, agent reproduction depends on preserve\_thinking=true, and its SWE-Bench Pro score trails Qwen3.8-27B.

<details><summary>References</summary>
<ul>
<li><a href="https://www.datastudios.org/post/nanbeige-4-3-33b-open-weight-dense-agentic-model-512k-context">Nanbeige4.3-33B: Apache 2.0 dense agentic coding model with ...</a></li>
<li><a href="https://www.marktechpost.com/2026/10/25/nanbeige-releases-nanbeige4-3-33b-open-agentic-coding-model/">Nanbeige Releases Nanbeige 4 . 3 - 33 B , a 33 B Open... - MarkTechPost</a></li>
<li><a href="https://aiweekly.co/alerts/nanbeige-opens-33b-model-under-apache-20-with-512k-context">Nanbeige Opens 33 B Model Under Apache 2 . 0 With... | AI Weekly</a></li>

</ul>
</details>

**Tags**: `#LLM agents`, `#open-source models`, `#model distillation`, `#benchmarking`

---

<a id="item-tech-news-4"></a>
### [Possible hinge flaw emerges from iPhone Duo teardown](https://www.theverge.com/tech/1018290/dissected-iphone-duo-crackgate-hinge-screen) ⭐️ 6.0/10

A YouTuber’s teardown of the foldable “iPhone Duo” may have identified a design flaw connected to reports that its screen cracks shortly after use. Some owners reportedly experienced failure within only a few hours, with the hinge appearing to catch on something before an audible crack and a broken screen. The excerpt says the reported cracks appeared to share a common characteristic, but it is truncated before explaining the pattern or the YouTuber’s proposed mechanism. Because the supplied account provides no complete methodology, evidence, or independent confirmation, the claimed cause remains a preliminary teardown finding rather than a settled explanation of “crackgate.”

rss · The Verge · Oct 25, 20:16

**「Background」** &quot;Crackgate&quot; refers to reports that the foldable iPhone Duo’s screen can crack soon after use, with damage apparently occurring near the hinge. YouTuber CuriousHagi reproduced the failure during durability testing and then disassembled the device to investigate whether its hinge or another design feature was responsible.

**「Early buyers face elevated display-failure risk」** Early iPhone Duo buyers have reported cracked inner displays, vertical cracks near the hinge, bright lines, and dead pixels within hours or after fewer than 20 openings, creating immediate durability and potential replacement concerns for the $1,999 device. The proposed design flaw is not yet confirmed, but the clustered failures indicate a material reliability risk if the pattern persists beyond these isolated reports.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theverge.com/tech/1018290/dissected-iphone-duo-crackgate-hinge-screen">A YouTuber dissected an iPhone Duo and thinks he... | The Verge</a></li>
<li><a href="https://www.notebookcheck.net/Apple-s-2-000-foldable-iPhone-reportedly-cracks-within-hours-as-owners-report-display-failures.1432971.0.html">Apple&#x27;s $2,000 foldable iPhone reportedly cracks within hours as...</a></li>
<li><a href="https://www.thenationalnews.com/future/technology/2026/10/25/apples-iphone-duo-faces-screen-damage-complaints-as-first-buyers-report-cracks/">iPhone Duo buyers complain of cracks and display failures after just...</a></li>
<li><a href="https://www.macrumors.com/2026/10/23/iphone-duo-screen-cracks/">Crackgate ? iPhone Duo Owners Report Screens... - MacRumors</a></li>

</ul>
</details>

**Tags**: `#Apple`, `#foldable smartphones`, `#hardware reliability`, `#teardown analysis`

---

<a id="item-tech-news-5"></a>
### [r/opensource adds AI ban and language restrictions](https://www.theverge.com/ai-artificial-intelligence/1018217/reddit-opensource-ai-ban) ⭐️ 6.0/10

The moderators of Reddit’s r/opensource announced new submission rules that reject projects that use AI, are made by AI, or are intended for AI. The announcement describes AI as incompatible with open source today, although the supplied excerpt cuts off the full rationale. The item also reports additional restrictions affecting non-English speakers, but does not provide the complete rule set or explain how it will be enforced. The change applies to one subreddit rather than to open-source software or Reddit as a whole.

rss · The Verge · Oct 25, 13:25

**「Subreddit governance context」** Reddit communities are governed through subreddit-specific rules, so a policy change in r/opensource affects participation there rather than open-source practices across Reddit. The stated rationale treats AI projects as inconsistent with the community’s interpretation of “Open Source,” while the reported restriction on non-English speakers is a separate participation rule; the supplied excerpt does not provide the full policy or enforcement history.

**「Project and contributor eligibility changes」** AI-related projects are no longer eligible for submission to r/opensource, while the reported language restrictions may also narrow who can participate in the community.

**Tags**: `#open source`, `#AI policy`, `#Reddit`, `#community governance`

---