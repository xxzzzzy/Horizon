---
layout: default
title: "Horizon Summary: 2026-11-05 (EN)"
date: 2026-11-05
lang: en
---

> From 134 items, 17 important content pieces were selected

---

**Technology News**
1. [A thousand fewer paths to root](#item-tech-news-1) ⭐️ 8.0/10
2. [Kimi K3.1 Pro model weights are out](#item-tech-news-2) ⭐️ 8.0/10
3. [Go&\#x27;s Experimental JSON v2 API](#item-tech-news-3) ⭐️ 8.0/10
4. [Anthropic advances provable inference for closed LLMs](#item-tech-news-4) ⭐️ 8.0/10
5. [Researchers Assess Russian-Linked Mobile Exploit Campaign](#item-tech-news-5) ⭐️ 8.0/10
6. [AMD&\#x27;s record quarter: Data center business doubles, while gaming craters](#item-tech-news-6) ⭐️ 8.0/10
7. [OpenAI Plans to Acquire Pierre Computer](#item-tech-news-7) ⭐️ 7.0/10
8. [Binance Details Months-Long $6.34 Billion Crypto Heist](#item-tech-news-8) ⭐️ 7.0/10
9. [Apple to check shared iCloud links for harmful content](#item-tech-news-9) ⭐️ 7.0/10
10. [OpenAI’s AI Social Contract and the 2028 Election](#item-tech-news-10) ⭐️ 7.0/10
11. [Meta acquires AI coding startup Conductor](#item-tech-news-11) ⭐️ 7.0/10
12. [DreamHost reports data breach from months-long attack](#item-tech-news-12) ⭐️ 7.0/10
13. [Sequoia retrenches after two decades of expansion](#item-tech-news-13) ⭐️ 7.0/10
14. [Dharma Field Extractor Turns Documents into Structured JSON](#item-tech-news-14) ⭐️ 6.0/10
15. [Four layers of context engineering for production AI agents: How Deep Insight applies them in working code - Amazon Web Services \(AWS\)](#item-tech-news-15) ⭐️ 6.0/10

**Financial News**
1. [After-hours stocks swing on earnings and guidance surprises](#item-finance-news-1) ⭐️ 7.0/10
2. [Treasury yields and oil prices fall after Democratic wins](#item-finance-news-2) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [A thousand fewer paths to root](https://openai.com/index/a-thousand-fewer-paths-to-root/) ⭐️ 8.0/10

OpenAI presents a large Linux-kernel security effort aimed at eliminating hundreds to roughly a thousand paths to local privilege escalation.

hackernews · OpenAI News · Nov 4, 23:33 · [Discussion](https://news.ycombinator.com/item?id=50372929)

**Tags**: `#linux-kernel`, `#privilege-escalation`, `#vulnerability-research`, `#cybersecurity`

---

<a id="item-tech-news-2"></a>
### [Kimi K3.1 Pro model weights are out](https://huggingface.co/moonshotai/Kimi-K3.1-Pro) ⭐️ 8.0/10

Moonshot AI released Kimi K3.1 Pro model weights, prompting strong interest in its capabilities, deployment requirements, and potential competitive impact on inference providers.

hackernews · abrarthought · Nov 4, 15:30 · [Discussion](https://news.ycombinator.com/item?id=50366999)

**Tags**: `#open-weight-models`, `#LLM-inference`, `#Kimi`, `#AI-model-releases`

---

<a id="item-tech-news-3"></a>
### [Go&\#x27;s Experimental JSON v2 API](https://go.dev/blog/jsonv2) ⭐️ 8.0/10

Go has introduced \`encoding/json/v2\`, an experimental standard-library JSON API that is opt-in through \`GOEXPERIMENT=jsonv2\`, while the existing \`encoding/json\` package remains unchanged for compatibility. It combines configurable, struct-oriented value conversion with token-level parsing and formatting in \`jsontext\`, including stricter handling options such as case-sensitive matching and rejection of unknown members. The goal is to improve correctness, diagnostics, and performance without forcing immediate migration from v1. Developers can evaluate the new API for demanding workloads, but adoption requires testing changed semantics and replacing conventions that v1 handled directly.

hackernews · olexsmir · Nov 4, 17:52 · [Discussion](https://news.ycombinator.com/item?id=50369106)

**「Background」** Go’s existing ... . The Go team first introduced ... experimentally; Go 1.27 expands that work into ... .

**「Migration impact」** Go 1.27’s encoding/json/v2 is a major revision, so adopters should test migrations because existing encoding/json imports continue to work but the underlying engine and some behaviors have changed. Applications requiring strict object validation must explicitly enable RejectUnknownMembers because v2 still ignores unknown members by default.

**「Community Reaction」** Support for \`encoding/json/v2\` was positive, and one user reported that \`jsontext\` handles difficult production clients with precise, error-specific diagnostics and excellent performance. Migration ergonomics drew more criticism—\`MarshalIndent\` was absent and its replacement was called unnecessarily complicated—while schema-guided parser generation was proposed as a way to make SIMD parsing of constrained JSON subsets practical.

<details><summary>References</summary>
<ul>
<li><a href="https://go.dev/blog/jsonv2">A new Go API for JSON - The Go Programming Language</a></li>
<li><a href="https://go.dev/blog/jsonv2-exp">A new experimental Go API for JSON</a></li>
<li><a href="https://go.dev/doc/jsonv2-migration">encoding/json/v2 Migration Guide - The Go Programming Language</a></li>
<li><a href="https://www.aijsonmedic.com/blog/go-1-27-encoding-json-v2-migration-guide">Go 1.27 encoding/json/v2 Migration Guide: Breaking Changes ...</a></li>
<li><a href="https://pkg.go.dev/encoding/json/v2">json package - encoding/json/v2 - Go Packages</a></li>

</ul>
</details>

**Tags**: `#Go`, `#encoding/json`, `#JSON parsing`, `#API design`, `#serialization`

---

<a id="item-tech-news-4"></a>
### [Anthropic advances provable inference for closed LLMs](https://www.anthropic.com/research/provable-inference) ⭐️ 8.0/10

Anthropic reports progress on cryptographically verifiable inference for closed-model providers, allowing clients to check that a provider used committed model weights and produced the claimed inference result. The approach uses a weight commitment and a zero-knowledge proof for each request, improving on earlier ZK inference techniques while addressing the harder case where users cannot simply rerun an open model. The reported design uses a roughly 6.5 MB commitment that must be refreshed after about 16 million requests; proof verification takes about 17 seconds on 24 threads or 21 seconds on one thread, including the offline phase. Proof generation adds roughly 90–100x inference compute, making this a meaningful verifiability milestone but not yet a low-overhead mainstream deployment path.

hackernews · ltononro · Nov 4, 17:17 · [Discussion](https://news.ycombinator.com/item?id=50368626)

**「Background」** A zero-knowledge succinct non-interactive argument of knowledge \(zkSNARK\) allows a client to verify that a provider ran the claimed model and produced the requested output without revealing the provider&\#x27;s proprietary weights or requiring every computation step to be replayed. For closed models, cryptographic commitments bind the provider to a specific set of weights, while per-request proofs demonstrate that inference used those committed weights; open-weight models instead permit clients to reproduce inference locally. This work builds on VerInf, which demonstrated zero-knowledge inference for a 400-billion-parameter model on a single NVIDIA DGX Spark using hash-based commitments without a trusted setup; Anthropic&\#x27;s implementation uses Llama 4 Maverick with 4-bit weights and integer-arithmetic prefill, generating about 19 MB of proof per 1,024-token request at roughly 110 tokens per second on one H100 GPU.

**「Provable verification remains costly」** For closed-model API users, FlashProve offers independently checkable evidence that a provider used its committed model and produced the response without exposing proprietary weights. Anthropic reports roughly 90–100× compute overhead; its implementation reaches 110 tokens per second on one H100 with 19 MB proofs that verify in seconds, making verification more practical but still materially more expensive than ordinary inference.

**「Promising result, disputed lineage」** Commenters generally welcomed the work as a significant improvement over prior zero-knowledge inference results, while noting that its 90–100x overhead may be less attractive than obtaining probabilistic checks from several independent providers. One commenter alleged that Anthropic built closely on VerInf with little attribution; others noted that open-weight models can be checked through deterministic reruns, whereas closed-model verification requires cryptography and could help detect unexpected model routing.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/research/provable-inference">Progress on provable inference for large language models</a></li>
<li><a href="https://github.com/JamesPetrie/VerInf">GitHub - JamesPetrie/VerInf</a></li>
<li><a href="https://www.anthropic.com/research/provable-inference">Progress on provable inference for large language models</a></li>
<li><a href="https://www.anthropic.com/research/provable-inference">Progress on provable inference for large language models \ Anthropic</a></li>
<li><a href="https://interestingengineering.com/ai-robotics/anthropic-flashprove-cryptographic-model-verification">Anthropic unveils cryptographic tool to verify model outputs</a></li>

</ul>
</details>

**Tags**: `#provable inference`, `#large language models`, `#zero-knowledge proofs`, `#cryptography`

---

<a id="item-tech-news-5"></a>
### [Researchers Assess Russian-Linked Mobile Exploit Campaign](https://arstechnica.com/security/2026/11/hackers-exploited-ios-and-android-flaws-to-infect-phones/) ⭐️ 8.0/10

Researchers at Sekoia assessed with moderate-to-high confidence that operators linked to Russia’s Foreign Intelligence Service exploited previously patched iOS and Android vulnerabilities through malicious JavaScript served to visitors of potentially hundreds of targeted websites. The injected scripts profiled each device and launched platform-specific payloads intended to steal browser cookies and, in some cases, Wi-Fi passwords and full mobile-device data. One operation used america250\[.\]holiday as a reverse proxy for america250.org, while theowo\[.\]club proxied the Raffles of London OWO website, allowing legitimate content to carry malicious scripts. The report does not establish how many devices were successfully compromised or whether all targeted data was stolen.

rss · Ars Technica · Nov 4, 22:26

**「Attack context」** The activity is a “watering-hole” attack: compromised, impersonated, or proxied sites serve JavaScript that fingerprints a visitor’s device and selects a platform-specific exploit, rather than relying on users to install malware. Related reporting has linked the broader operation to APT29 and the Roaming Mantis mobile-intrusion campaign, which has targeted iOS and Android users across multiple countries. Because the abused iOS and Android vulnerabilities were already patched, successful exploitation would have depended on the victim visiting a targeted site while running an affected, unpatched device configuration.

**「Impact」** The campaign placed browser cookies, Wi-Fi passwords, and full mobile-device data at risk for visitors exposed to the targeted website exploit chain, although the scale of successful compromise and confirmed data theft remains unknown.

<details><summary>References</summary>
<ul>
<li><a href="https://www.helpnetsecurity.com/2026/11/04/apt29-watering-hole-mobile-devices-n-day-exploits/">Russian hackers target iOS and Android users... - Help Net Security</a></li>
<li><a href="https://www.scworld.com/brief/sekoia-android-ios-users-hit-by-roaming-mantis">SEKOIA : Android , iOS users hit by Roaming Mantis | brief | SC Media</a></li>

</ul>
</details>

**Tags**: `#iOS security`, `#Android security`, `#nation-state hacking`, `#mobile malware`, `#web-based exploitation`

---

<a id="item-tech-news-6"></a>
### [AMD&\#x27;s record quarter: Data center business doubles, while gaming craters](https://arstechnica.com/gadgets/2026/11/amds-record-quarter-data-center-business-doubles-while-gaming-craters/) ⭐️ 8.0/10

AMD reported record quarterly revenue driven by near-doubling data-center sales and issued guidance suggesting it could surpass Intel&\#x27;s revenue.

rss · Ars Technica · Nov 4, 21:29

**Tags**: `#AMD`, `#semiconductors`, `#data-center hardware`, `#server CPUs`, `#earnings`

---

<a id="item-tech-news-7"></a>
### [OpenAI Plans to Acquire Pierre Computer](https://openai.com/index/openai-to-acquire-pierre/) ⭐️ 7.0/10

OpenAI plans to acquire Pierre Computer Company, whose Git-based Code.Storage is used to manage generated code, memory files, design artifacts, legal documents, and other changing product resources at scale. The acquisition is intended to expand Codex’s capabilities for building, understanding, and reviewing code by adding developer tooling and code-infrastructure expertise relevant to AI coding and agent workloads. Pierre says Lovable, Poke, Anything, Bolt, Amp, and Parahelp rely on Code.Storage, but the available material does not specify the deal’s value, closing timeline, contract structure, or technical integration plans.

hackernews · OpenAI News · Nov 4, 15:21 · [Discussion](https://news.ycombinator.com/item?id=50366863)

**「Relevant Context」** Pierre Computer Company develops developer tools for AI-assisted coding, including the Code Storage repository and Diffs, whose Edit mode lets reviewers fix code directly where they identify a problem. OpenAI had already integrated some Pierre tools into Codex, so the acquisition is intended to expand Codex’s capabilities for building, understanding, and reviewing code.

**「Impact」** The acquisition should bring Pierre&\#x27;s programmable Git and code-storage capabilities into Codex, strengthening OpenAI&\#x27;s infrastructure for agentic workflows that build, understand, and review code. No integration timeline or compatibility changes are specified, so the practical effect on current Codex users remains unclear.

**「Community Reactions」** Commenters connected the acquisition to OpenAI’s work on scaling Git, noted that Mitchell Hashimoto has promoted Pierre and may be an investor, and praised Pierre’s diffs library. Some expressed skepticism about whether OpenAI is primarily acquiring scalable infrastructure, reusable engineering talent, or insight into how successful developer products are built.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/openai-to-acquire-pierre/">OpenAI to acquire Pierre Computer Company , Inc. | OpenAI</a></li>
<li><a href="https://www.theverge.com/openai">OpenAI | The Verge</a></li>
<li><a href="https://openai.com/index/openai-to-acquire-pierre/">OpenAI to acquire Pierre Computer Company, Inc. | OpenAI</a></li>
<li><a href="https://vc.ru/dev/3235978-openai-priobretayet-pierre-computer">«Бросает вызов GitHub»: OpenAI объявила о планах купить Pierre ...</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#acquisitions`, `#developer tools`, `#Git infrastructure`, `#AI coding agents`

---

<a id="item-tech-news-8"></a>
### [Binance Details Months-Long $6.34 Billion Crypto Heist](https://arstechnica.com/information-technology/2026/11/binance-says-hackers-who-stole-billions-in-crypto-spent-months-planning-heist/) ⭐️ 7.0/10

Binance reported that a sophisticated, multi-stage campaign targeting $6.34 billion in cryptocurrency was attributed by the FBI and TRM to North Korean actors, making it the largest amount ever targeted in a crypto theft. The operation reportedly began no later than June and culminated in the compromise of an engineer’s laptop and withdrawals from several Binance wallets. Attackers combined fake recruitment interviews, tampered Homebrew downloads, malicious software, compromised internal AI tooling, endpoint compromise, and an advanced transaction-authorization method. Binance has frozen or intercepted $2.85 billion, set aside funds to cover losses, and published a Proof of Reserves page, but the source does not specify the amount ultimately stolen.

rss · Ars Technica · Nov 4, 16:06

**「Attack context」** An advanced persistent threat \(APT\) is a sustained, targeted intrusion rather than a one-off phishing attempt. Binance said this campaign began no later than June and progressed from fake recruitment interviews and a tampered Homebrew download on an engineer’s laptop to compromised internal tooling and transaction-authorization systems before assets were withdrawn. The FBI and TRM attributed the operation to North Korean actors.

**「Impact on Binance users and reserves」** Although Binance said it had replenished 98% of affected tokens by October 31 and reserved $6.34 billion to cover the breach, TRM estimated that $2.4 billion remained beyond issuers’ reach, leaving customers exposed to incomplete recovery and possible losses.

<details><summary>References</summary>
<ul>
<li><a href="https://www.wired.com/story/binance-says-hackers-used-well-known-tricks-to-carry-out-a-dollar634-billion-heist/">Binance Says Hackers Used Well-Known Tricks to Carry Out a $ 6 . 34 ...</a></li>
<li><a href="https://www.theregister.com/security/2026/11/03/north-korean-fake-job-interview-led-to-63b-binance-heist/5307398">North Korean fake job interview led to $ 6 .3B Binance heist</a></li>
<li><a href="https://www.binance.com/en/square/post/11-03-2026-binance-posts-initial-findings-on-29-oct-hack-98-of-6-34b-stolen-assets-replenished-multi-stage-attack-detailed-384312984895952">Binance Posts Initial Findings on 29 Oct Hack: 98% of $ 6 . 34 B Stolen...</a></li>
<li><a href="https://www.nytimes.com/2026/10/31/technology/binance-hack-crypto-north-korea.html">How Binance ’s $ 6 .3 Billion Hack Went Down - The New York Times</a></li>

</ul>
</details>

**Tags**: `#cryptocurrency security`, `#advanced persistent threat`, `#malware`, `#social engineering`

---

<a id="item-tech-news-9"></a>
### [Apple to check shared iCloud links for harmful content](https://www.theverge.com/tech/1026604/apple-icloud-links-harmful-content-27-3) ⭐️ 7.0/10

Apple says version 27.3 will begin checking iCloud items accessible through shared links for “harmful content.” The change covers iOS, iPadOS, macOS, and visionOS when an item is shared using “Anyone with the Link.” This extends content-moderation checks to link-accessible iCloud content, with potential implications for privacy, enforcement, and false positives. The supplied announcement excerpt does not explain whether the checks are automated, what data is examined, how errors are handled, or whether previously shared links are reevaluated.

rss · The Verge · Nov 4, 18:23

**「Public iCloud link sharing」** iCloud’s “Anyone with the Link” option makes supported photos and files accessible through a URL without restricting access to named collaborators. Apple’s policy applies to this public-link sharing model across the iOS, iPadOS, macOS, and visionOS 27.3 releases, rather than to all iCloud content.

**「Impact on shared iCloud content」** Users sharing iCloud items through “Anyone with the Link” will have those publicly accessible items checked for harmful content in iOS 27.3 and the corresponding iPadOS, macOS, and visionOS 27.3 updates, bringing shared links under Apple’s content moderation. Apple has not specified the checking process, criteria, privacy implications, or appeal process, so the likelihood of false positives remains unclear.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theverge.com/tech/1026604/apple-icloud-links-harmful-content-27-3">Apple will check shared iCloud links for ‘harmful content’</a></li>
<li><a href="https://www.macrumors.com/2026/11/04/ios-27-3-icloud-link-check/">Apple Will Check Public iCloud Links for Harmful Content ...</a></li>
<li><a href="https://9to5mac.com/2026/11/04/with-ios-27-3-apple-will-start-checking-icloud-public-links-for-harmful-content/">With iOS 27.3, Apple will start checking iCloud public links ...</a></li>
<li><a href="https://itzine.ru/news/services/ios-27-3-apple-nachnjot-proverjat-kontent-ssylkam-icloud.html">В iOS 27 . 3 Apple начнёт проверять контент по ссылкам iCloud</a></li>

</ul>
</details>

**Tags**: `#Apple`, `#iCloud`, `#content moderation`, `#privacy`, `#platform security`

---

<a id="item-tech-news-10"></a>
### [OpenAI’s AI Social Contract and the 2028 Election](https://techcrunch.com/2026/11/04/openai-is-already-trying-to-shape-the-2028-election/) ⭐️ 7.0/10

OpenAI executive Chris Lehane is promoting an AI-centered social contract as a framework for American society and the 2028 U.S. election. TechCrunch says the proposal could shape election discourse while also advancing OpenAI’s business interests. The framing places the company’s corporate strategy alongside potential public benefits from AI, raising questions about how OpenAI may seek influence over political debate. The supplied account does not describe specific policies, interventions, or implementation plans, so the extent and mechanics of that influence remain unclear.

rss · TechCrunch · Nov 4, 21:25

**「Policy context」** An AI-centered social contract is a broad framework for defining the responsibilities and public rules governing AI’s role in society. Chris Lehane, OpenAI’s chief global affairs officer and a former Clinton-era political operative, is advancing the idea alongside other policies such as safety requirements for advanced AI systems and the proposed “AI compute campuses” label for data centers. Lehane has described the 2026 U.S. midterms as a preview of the 2028 presidential election, where he expects AI to become a central issue.

**「Impact on the 2028 Election」** If OpenAI’s proposed AI social contract gains traction, AI policy and the company’s role in voter information, public services, and policy research could become major issues in the 2028 U.S. election, giving OpenAI an opportunity to shape election discourse and public policy. The effect remains uncertain because the proposal is an agenda rather than an implemented election program, and critics question whether it serves the public or introduces risks involving manipulation, bias, privacy, and democratic accountability.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Chris_Lehane">Chris Lehane - Wikipedia</a></li>
<li><a href="https://forklog.com/en/openai-proposes-renaming-data-centers-to-ai-compute-campuses/">OpenAI Proposes Renaming Data Centers to ‘ AI Compute... | ForkLog</a></li>
<li><a href="https://techcrunch.com/2026/11/01/openai-might-rebrand-its-data-centers-as-ai-compute-campuses/">OpenAI might rebrand its data centers as ‘ AI compute... | TechCrunch</a></li>
<li><a href="https://techcrunch.com/2026/11/04/openai-is-already-trying-to-shape-the-2028-election/">OpenAI is already trying to shape the 2028 election - TechCrunch</a></li>
<li><a href="https://tradersunion.com/news/companies/show/4102708-openai-ai-2028-election-policy/">OpenAI pushes policy agenda as AI emerges in 2028 election debate</a></li>
<li><a href="https://www.androguider.com/2026/11/openai-and-2028-election-chris-lehanes.html">OpenAI and the 2028 Election: Chris Lehane’s Vision for AI ...</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#AI policy`, `#elections`, `#corporate strategy`

---

<a id="item-tech-news-11"></a>
### [Meta acquires AI coding startup Conductor](https://techcrunch.com/2026/11/04/meta-acquires-ai-coding-startup-conductor/) ⭐️ 7.0/10

Meta acquired Conductor, a startup whose product lets engineers deploy multiple AI agents to work on different parts of a software project simultaneously.

rss · TechCrunch · Nov 4, 21:10

**Tags**: `#AI coding agents`, `#startup acquisition`, `#software engineering`, `#Meta`

---

<a id="item-tech-news-12"></a>
### [DreamHost reports data breach from months-long attack](https://techcrunch.com/2026/11/04/hackers-stole-dreamhost-customer-files-and-inboxes-during-months-long-attack/) ⭐️ 7.0/10

DreamHost said hackers exploited a vulnerability during a deliberate, months-long attack, gaining access to customer email accounts and hosted files. The reported intrusion means customer inbox contents and stored files may have been exposed to unauthorized access. The supplied report does not identify the vulnerability, number of affected customers, precise attack dates, or remediation steps, leaving the incident&\#x27;s full scope and containment status unclear.

rss · TechCrunch · Nov 4, 20:36

**「Background」** DreamHost provides web-hosting and webmail services, so compromising its infrastructure can expose both customer-hosted files and email inboxes. In this context, vulnerability exploitation means attackers used a software weakness to gain unauthorized access, while the months-long timeline indicates that the intrusion continued for an extended period.

**「Customer impact」** DreamHost customers whose email accounts or files were accessed may have had sensitive inbox contents and hosted files exposed, though the affected customer count is not specified.

<details><summary>References</summary>
<ul>
<li><a href="https://webmail.dreamhost.com/">DreamHost Webmail :: Welcome to DreamHost Webmail</a></li>

</ul>
</details>

**Tags**: `#cybersecurity`, `#data breach`, `#web hosting`, `#vulnerability exploitation`

---

<a id="item-tech-news-13"></a>
### [Sequoia retrenches after two decades of expansion](https://techcrunch.com/2026/11/04/sequoia-hits-rewind-undoing-20-years-of-expansion/) ⭐️ 7.0/10

Sequoia is retrenching from two decades of expansion, consolidating into a smaller firm centered in the Bay Area. The venture capital firm is shutting down programs and offices built during that 20-year period. At the same time, Sequoia announced roughly $10 billion in new funds. The move marks a significant shift in Sequoia’s operating model and the broader technology-investment ecosystem, although the supplied account does not identify the affected offices and programs, fund structures, or implementation timeline.

rss · TechCrunch · Nov 4, 17:11

**「Historical context」** Venture-capital firms raise capital from investors and allocate it to companies they expect to grow in value. Sequoia Capital has a long record of backing technology companies, including an $11.5 million investment in YouTube from November 2005 through April 2006; its stake was later estimated at about 30% when Google acquired YouTube. The retrenchment described in the item reverses the broad build-out of programs and offices from Sequoia’s two-decade expansion even as the firm announces roughly $10 billion in new funds.

**「Impact」** Founders served by Sequoia’s expansion-era regional offices and programs will lose those support channels as the firm narrows to a Bay Area–centered model, though roughly $10 billion in newly announced funds may sustain substantial startup financing.

<details><summary>References</summary>
<ul>
<li><a href="https://www.nytimes.com/2006/10/10/technology/venture-firm-shares-a-youtube-jackpot.html">Venture Firm Shares a YouTube Jackpot - The New York Times</a></li>

</ul>
</details>

**Tags**: `#venture capital`, `#Sequoia`, `#startup funding`, `#tech industry`

---

<a id="item-tech-news-14"></a>
### [Dharma Field Extractor Turns Documents into Structured JSON](https://huggingface.co/blog/Dharma-AI/dharma-field-extractor) ⭐️ 6.0/10

Hugging Face announced Dharma Field Extractor, a 2-billion-parameter document-understanding model that converts document images into typed, structured JSON across invoices, IDs, medical forms, contracts, receipts, statements, and other layouts without per-type fine-tuning. In open mode, it infers fields from context and layout; in schema-directed mode, it follows supplied keys and string, number, or boolean types, fills nested tables row by row, emits no extra keys, and returns null for missing values. It is based on DharmaOCR-LITE v1.1 and was trained with a LoRA adapter on 43,384 field-annotated English, Brazilian Portuguese, and other multilingual examples. In Dharma&\#x27;s own 546-document, 1,638-case benchmark, it scored 0.834 under a metric combining field-level F1, matched-value Levenshtein similarity, and valid-JSON rate, ahead of four frontier configurations, including Claude Opus 5 at 0.816 and GPT-5.6 Luna at 0.741; showcased held-out SROIE and FUNSD examples were also extracted correctly. The company estimates that self-hosted inference on one L40S, priced at $2.24 per hour, is about 6 to 147 times cheaper per page than the tested APIs, but notes that this is not a sales price and that token pricing, reasoning settings, hardware, volume, and latency affect the comparison; the benchmark and performance claims are vendor-reported rather than independently verified.

rss · Hugging Face Blog · Nov 4, 17:50

**「Background」** Document OCR reproduces the text and formatting of a page, while document field extraction locates specific values and organizes them into machine-readable JSON. Dharma Field Extractor builds on the earlier DharmaOCR-LITE model with two modes: open extraction, which infers fields from the document’s context and layout, and schema-directed extraction, which follows user-supplied field names and types. In schema-directed mode, fields absent from the document are returned as null, allowing downstream systems to distinguish missing information from extracted content.

**「Deployment Impact」** Teams needing high-volume, schema-specific document extraction can self-host the 2-billion-parameter model on a single L40S and receive schema-conformant JSON with null for absent fields, potentially replacing OCR-plus-mapping pipelines and costly frontier API calls. However, the reported quality and cost advantages come from Dharma&\#x27;s own 546-document benchmark, so adopters should still validate performance on their own document types.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/blog">Hugging Face – Blog</a></li>
<li><a href="https://ai-manual.ru/article/dharma-field-extractor-kak-model-na-2-mlrd-parametrov-izvlekaet-polya-iz-dokumentov-v-json-i-obhodit-frontier-llm/">Dharma Field Extractor : как модель на 2 млрд... | AiManual</a></li>
<li><a href="https://huggingface.co/blog/Dharma-AI/dharma-field-extractor">Dharma Field Extractor: Any Document In, Structured Fields in ...</a></li>
<li><a href="https://lancartech.co.id/en/blog/dharma-field-extractor-ekstraksi-field-json-evaluasi-tim">Dharma Field Extractor: How to Evaluate Document-to-JSON ...</a></li>
<li><a href="https://daily.dev/posts/dharma-field-extractor-any-document-in-structured-fields-in-json-out-7it2nmv74">Dharma Field Extractor: Any Document In, Structured...</a></li>

</ul>
</details>

**Tags**: `#document AI`, `#information extraction`, `#JSON`, `#small language models`, `#OCR`

---

<a id="item-tech-news-15"></a>
### [Four layers of context engineering for production AI agents: How Deep Insight applies them in working code - Amazon Web Services \(AWS\)](https://news.google.com/rss/articles/CBMi5wFBVV95cUxNckI2RW5SeGRMQmt0NlVlRUhPT3lLdFRLVldSelVscGg4eWZIYmtDWkp4STlmbXJVRWFhcWRpV0tOZ3ZwSTJ6TmtxY2tNclF6dnJUZnVCdWt3cVB4N0tLc0lzbFZLUDRMMWJzaUNWbHVNZkpMTDJ4S0gtZ1o3bU5XS3lCeHVZVW9YNnRmVG5Udzg1d253aWdEVS16QnNqcnkwUE9LMUItaGJjY1V4TkI3bmp5NlR4bG4xTjljTWFzWWF0RGpHY0VMQ1RpTjNMRWtDWnl4a3RuOXRSaDZ0allHR04ybUV3cXM?oc=5) ⭐️ 6.0/10

AWS presents a four-layer context-engineering framework for building production AI agents, illustrated with working code.

google\_news · Amazon Web Services \(AWS\) · Nov 4, 16:30

**Tags**: `#AI agents`, `#context engineering`, `#production AI`, `#AWS`, `#LLM applications`

---

## Financial News

<a id="item-finance-news-1"></a>
### [After-hours stocks swing on earnings and guidance surprises](https://www.cnbc.com/2026/11/04/stocks-making-the-biggest-moves-after-hours-cohr-app-expe-more.html) ⭐️ 7.0/10

Shares swung after hours as quarterly results and guidance from Qualcomm, AppLovin, Expedia, Coherent, Zillow and other companies diverged from analyst expectations. AppLovin rose more than 20% after third-quarter revenue of $2.18 billion exceeded the $2.07 billion FactSet estimate, while Zillow fell more than 16% after revenue of $724 million missed the $754 million LSEG estimate.

rss · CNBC Finance · Nov 4, 22:04

**「Background」** The moves reflect investors’ comparisons of reported earnings and forward guidance with consensus estimates, including expectations for revenue, users and same-store sales.

**Tags**: `#earnings results`, `#after-hours trading`, `#semiconductors`, `#software and e-commerce`, `#corporate guidance`

---

<a id="item-finance-news-2"></a>
### [Treasury yields and oil prices fall after Democratic wins](https://www.cnbc.com/2026/11/03/treasury-yields-fall-as-democrats-win-big-in-us-midterm-elections.html) ⭐️ 7.0/10

The 10-year U.S. Treasury yield fell more than 6 basis points \(0.06 percentage points\) to 4.884% after Democrats won both chambers, with JPMorgan traders saying Wall Street was focused on the possibility of reduced deficit spending. U.S. oil futures also fell, with West Texas Intermediate down 8.29% to close at $88.12 per barrel, as there was no immediate sign of escalating U.S.-Iran tensions.

rss · CNBC Finance · Nov 4, 21:18

**「Background」** Democratic control of Congress could make it harder for the White House to pass spending legislation, potentially limiting deficit growth; however, this is an outlook rather than an enacted policy change.

**Tags**: `#U.S. Treasury yields`, `#U.S. midterm elections`, `#fiscal policy`, `#oil prices`, `#Iran geopolitics`

---