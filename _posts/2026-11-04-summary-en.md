---
layout: default
title: "Horizon Summary: 2026-11-04 (EN)"
date: 2026-11-04
lang: en
---

> From 128 items, 19 important content pieces were selected

---

**Technology News**
1. [The Internals of PostgreSQL: A Deep Dive into Storage, Concurrency, and Indexing](#item-tech-news-1) ⭐️ 8.0/10
2. [Postman accused of silently installing AI plugins and sharing API data](#item-tech-news-2) ⭐️ 8.0/10
3. [BlackX Bootkit Bypasses Secure Boot on Patched Windows](#item-tech-news-3) ⭐️ 8.0/10
4. [Publishers Sue Brave Over Paywall Bypassing and AI Content Deals](#item-tech-news-4) ⭐️ 7.5/10
5. [Local Qwen 3.8 27B Interprets Model Weights](#item-tech-news-5) ⭐️ 7.0/10
6. [Mac at Any Scale](#item-tech-news-6) ⭐️ 7.0/10
7. [Aircraft Noise Can Reveal a Video&\#x27;s Exact Location](#item-tech-news-7) ⭐️ 7.0/10
8. [Russia Moves to Protect Data Centers Amid Drone Strikes](#item-tech-news-8) ⭐️ 7.0/10
9. [Google Dismantles x.cpe Botnet on 1.3 Million Android TV Boxes](#item-tech-news-9) ⭐️ 7.0/10
10. [Binance Details a Multistage $6.3B Crypto Heist](#item-tech-news-10) ⭐️ 7.0/10
11. [CrowdStrike to Buy Fiddler AI and Dreadnode](#item-tech-news-11) ⭐️ 7.0/10
12. [Raspberry Pi raises 16GB Pi 5 price to $385](#item-tech-news-12) ⭐️ 7.0/10
13. [OpenVDDK emerges as an alternative to undisclosed VMware migration tooling](#item-tech-news-13) ⭐️ 7.0/10
14. [StateBench Tests Long-Context State Tracking](#item-tech-news-14) ⭐️ 7.0/10
15. [Antigravity Agent Accelerates Macrocycle Design for Lung-Cancer Drug Discovery](#item-tech-news-15) ⭐️ 7.0/10
16. [Palette fine-tunes a 20B model for private deck generation](#item-tech-news-16) ⭐️ 6.0/10
17. [Nature article examines AI predictive modeling in precision medicine](#item-tech-news-17) ⭐️ 6.0/10

**Financial News**
1. [Major stocks diverge after earnings](#item-finance-news-1) ⭐️ 7.0/10
2. [AI Infrastructure Buildout Seen Needing More Equity](#item-finance-news-2) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [The Internals of PostgreSQL: A Deep Dive into Storage, Concurrency, and Indexing](https://www.interdb.jp/pg/index.html) ⭐️ 8.0/10

This detailed reference explains PostgreSQL internals, including HoT updates, zHeap and TOAST, SSI, MVCC, indexing, and version-specific behavior. It also highlights PostgreSQL 18 changes to full-text search, collation handling, and index requirements after pg\_upgrade. The recurring Hacker News discussion and implementation-level commentary suggest substantial value for database engineers.

hackernews · ibobev · Nov 3, 21:51 · [Discussion](https://news.ycombinator.com/item?id=50358702)

**Tags**: `#postgresql`, `#database-internals`, `#mvcc`, `#concurrency`, `#indexing`

---

<a id="item-tech-news-2"></a>
### [Postman accused of silently installing AI plugins and sharing API data](https://github.com/postmanlabs/postman-app-support/issues/14370) ⭐️ 8.0/10

A Postman support issue alleges that the app silently installed AI plugins and transmitted detailed API request data, potentially exposing templated secret values and raising compliance concerns. Community commenters say blocking the related telemetry can break the app and report that some healthcare teams discontinued or were decertified from using Postman. The evidence is largely user-reported, and the exact scope and intent of the behavior remain unresolved.

hackernews · sidgarimella · Nov 3, 17:22 · [Discussion](https://news.ycombinator.com/item?id=50354960)

**Tags**: `#Postman`, `#API security`, `#data privacy`, `#AI plugins`, `#developer tools`

---

<a id="item-tech-news-3"></a>
### [BlackX Bootkit Bypasses Secure Boot on Patched Windows](https://arstechnica.com/security/2026/11/uefi-bootkit-infected-fully-patched-windows-machines-is-microsoft-to-blame/) ⭐️ 8.0/10

BlackX is a UEFI bootkit that infected fully patched Windows systems by exploiting Baton Drop \(CVE-2022-21894\), a logic flaw in the Windows boot manager that can bypass Secure Boot and, under certain conditions, extract BitLocker encryption keys. It builds on BlackLotus, which became the first publicly documented in-the-wild UEFI bootkit to bypass Secure Boot on fully updated Windows 11 systems in 2023. Microsoft fixed the vulnerability in 2022 and issued further updates in 2023 and 2024 to block trust in vulnerable boot managers, including enabling revocation of the certificate used to sign older vulnerable Windows boot managers, yet every BlackX-infected organization had installed these updates. The supplied account is truncated before it explains precisely how BlackX overcame those mitigations, so it does not establish whether Microsoft is responsible.

rss · Ars Technica · Nov 3, 16:03

**「Background」** UEFI firmware initializes a computer’s hardware and loads the operating system, while Secure Boot verifies the digital signatures of boot components to prevent unauthorized code from running before Windows starts. BlackLotus became the first publicly documented in-the-wild UEFI bootkit to bypass Secure Boot on fully updated Windows 11 systems by exploiting “Baton Drop” \(CVE-2022-21894\), a Windows boot-manager flaw patched in 2022. Although Microsoft later revoked trust in certificates that had signed vulnerable boot managers, BlackX continued to exploit the same class of trust gap on systems that had installed those updates.

**「Patching Alone Did Not Close the Trust Gap」** For organizations retaining affected vulnerable boot managers, Windows updates alone did not restore the Secure Boot trust chain, allowing malicious code to run before Windows security defenses were fully operational and potentially exposing BitLocker keys under the stated conditions.

<details><summary>References</summary>
<ul>
<li><a href="https://arstechnica.com/security/2026/11/uefi-bootkit-infected-fully-patched-windows-machines-is-microsoft-to-blame/">UEFI bootkit infected fully patched Windows machines. Is ...</a></li>
<li><a href="https://securelist.com/uefi-bootkit-blackx/121539/">New BlackX UEFI bootkit exploiting Baton Drop | Securelist</a></li>

</ul>
</details>

**Tags**: `#UEFI security`, `#bootkits`, `#Windows security`, `#Secure Boot`, `#malware analysis`

---

<a id="item-tech-news-4"></a>
### [Publishers Sue Brave Over Paywall Bypassing and AI Content Deals](https://arstechnica.com/tech-policy/2026/11/nyt-demands-brave-shut-down-its-paywall-blocker-and-end-deals-with-ai-firms/) ⭐️ 7.5/10

The New York Times and other newspaper companies sued Brave Software in the U.S. District Court for the Southern District of New York, alleging that Brave scraped protected journalism, bypassed publisher paywalls, and supplied unlicensed news content through its search index to AI companies. The complaint alleges that Anthropic, Perplexity, Mistral, xAI, and Cohere pay Brave for real-time Brave Search index content used to train their models and answer specific user queries, while Brave’s website also lists You.com as an API customer. It further alleges that Brave’s browser can automatically get behind paywalls, replace publisher-supported advertising with Brave ads, and give users a share of the resulting revenue. The NYT asserts direct, contributory, and vicarious copyright infringement and Digital Millennium Copyright Act violations, citing third-party estimates that Brave earned more than $100 million while publishers received nothing; these liability and financial claims remain allegations rather than judicial findings.

rss · Ars Technica · Nov 3, 18:30

**「Relevant context」** Brave operates a privacy-focused web browser and a search service whose index is accessible to AI companies through the Brave Search API; the lawsuit alleges that these services enabled the scraping and redistribution of copyrighted journalism. The dispute follows the Times’ 2023 lawsuit against OpenAI and Microsoft and reflects publishers’ broader efforts to control how their content is used in AI systems, while the claims against Brave remain unadjudicated allegations.

**「Potential licensing and compliance impact」** If the publishers prevail, Brave could face restrictions on paywall bypass and unlicensed redistribution of protected articles through its search index and API, forcing changes to its browser/search business and potentially requiring AI companies to secure publisher licenses for indexed news content. The claims remain allegations, and the suit&\#x27;s outcome and remedies are not yet established.

<details><summary>References</summary>
<ul>
<li><a href="https://techcrunch.com/2026/11/02/new-york-times-and-other-outlets-sue-web-browser-brave-over-alleged-content-scraping/">New York Times and other outlets sue web browser Brave over...</a></li>
<li><a href="https://kod.ru/nyt-brave-isk-ii">The New York Times подала в суд на Brave за сбор статей для ИИ</a></li>
<li><a href="https://techcrunch.com/2026/11/02/new-york-times-and-other-outlets-sue-web-browser-brave-over-alleged-content-scraping/">New York Times and other outlets sue web browser Brave over...</a></li>
<li><a href="https://www.theverge.com/tech/1024588/brave-lawsuit-ai-scraping-new-york-times">The New York Times sues Brave web browser for AI ... | The Verge</a></li>
<li><a href="https://dzen.ru/a/aujp9-AcSRbSGDhK">Газеты подали в суд на Brave из-за доступа к платным... | Дзен</a></li>

</ul>
</details>

**Tags**: `#AI content licensing`, `#copyright law`, `#Brave Search`, `#publishing`

---

<a id="item-tech-news-5"></a>
### [Local Qwen 3.8 27B Interprets Model Weights](https://simonwillison.net/2026/Nov/3/qwen-can-interpret-model-weights/) ⭐️ 7.0/10

Simon Willison reports that Qwen 3.8 27B, running locally through LM Studio, interpreted the raw floating-point weights of small reinforcement-learning policy networks without executing code and correctly identified Pac-Man and Pong from prompts that differed only in their weight data. The 17GB Q4\_K\_M model required a longer context window because the default 8,192-token setting produced errors, while the Pac-Man attempt took 46 minutes 12 seconds and 43,506 reasoning tokens. This extends the “Weight-Space Programming” paper’s claimed interpretation ability for frontier model GPT-6 Astra to a laptop-scale 27B model, but Willison&\#x27;s test concerns interpretation rather than the paper&\#x27;s more demanding code-assisted or direct weight-modification claims. The paper additionally reported Astra editing 0.016% of Qwen3.5-0.8B&\#x27;s weights to address reasoning loops, raising MATH-500 from 7.9% to 48.1% and tripling IFEval. Willison&\#x27;s result is promising for private, local model analysis, but it does not establish that a local model can reliably diagnose or edit arbitrary production networks.

rss · Simon Willison · Nov 3, 16:29 · [Discussion](https://news.ycombinator.com/item?id=50355251)

**「Weight-space programming」** Weight-space programming describes a language model reasoning directly over a neural network’s raw floating-point weights to infer what the network has learned and, in some experiments, write or edit those weights without running a conventional training loop. It differs from tool-assisted model editing, in which a model generates and executes code to manipulate parameters; Simon Willison’s local Qwen 3.8 27B test focuses on the no-tools ability to interpret weights.

**「Practical impact」** For local AI developers, the experiment makes exploratory weight-space analysis accessible without a frontier-model API: a 17GB Qwen 3.8 27B Q4\_K\_M model running in LM Studio identified a Pac-Man policy from raw weights without code or calculator tools. It does not establish reliable weight editing, because the successful inference required extended context, a 900-second timeout, and 46 minutes 12 seconds with 43,506 reasoning tokens, while commenters questioned whether the interpretation was genuinely correct or merely plausible pattern matching.

**「Enthusiasm meets skepticism」** Commenters were divided: one praised Qwen 3.8 27B as a capable local “higher-level architect,” while others argued that producing a plausible interpretation does not prove that a model correctly understands what the weights encode. Questions also remained about whether it could alter its own weights reliably, how steering vectors, J-spaces, and LoRAs affect the comparison, and what benchmark could demonstrate useful weight editing.

<details><summary>References</summary>
<ul>
<li><a href="https://rikiyat.github.io/blog/weight-space-programming/">Sparks of Weight - Space Programming : LLMs can natively read ...</a></li>
<li><a href="https://simonwillison.net/2026/Nov/3/qwen-can-interpret-model-weights/">Qwen 3 .8 27 B on my laptop can interpret model weights , too</a></li>
<li><a href="https://simonwillison.net/2026/Nov/3/qwen-can-interpret-model-weights/">Qwen 3.8 27B on my laptop can interpret model weights, too</a></li>

</ul>
</details>

**Tags**: `#weight-space programming`, `#LLMs`, `#model-weight interpretation`, `#Qwen`, `#AI research`

---

<a id="item-tech-news-6"></a>
### [Mac at Any Scale](https://namespace.so/blog/mac-at-any-scale) ⭐️ 7.0/10

The article examines how organizations can operate Mac hardware and Apple’s developer toolchain at data-center scale for software build-and-test workloads, particularly iOS applications. It highlights the practical constraints imposed by iOS build requirements, cross-compilation, code signing, and the operational cost of managing Mac fleets. Rather than presenting a new technology, the piece frames Mac scaling as an infrastructure-engineering problem created by Apple’s tightly integrated hardware and software ecosystem, with no evidence of a major industry-changing breakthrough.

hackernews · anner\_ · Nov 3, 14:53 · [Discussion](https://news.ycombinator.com/item?id=50352758)

**「Background」** Apple’s iOS development workflow is closely tied to macOS and Xcode, so organizations that must produce signed apps or run Apple-supported simulator tests have traditionally needed physical Macs rather than conventional Linux build servers. Scaling that requirement means treating Mac hardware as managed data-center infrastructure; Namespace says it uses racks of Macs equipped with macOS, Xcode, and multiple iOS testing runtimes because Apple has not offered an alternative.

**「Infrastructure Impact」** Organizations operating large iOS and macOS build-and-test fleets must design specialized infrastructure—including custom Mac hardware, macOS virtualization, and fleet-wide image distribution—making Apple’s controlled toolchain a significant operational barrier at data-center scale.

**「Community Discussion」** Commenters broadly agreed that Apple’s restrictive tooling, signing workflow, and hardware model make large-scale Mac automation unusually painful; one suggested a premium, Mac mini-class data-center product could still find buyers because operations are expensive. A counterexample challenged the claim that iOS apps cannot be built without a Mac by pointing to a Linux-hosted cross-compiler for C, C++, and Fortran, while other contributors recalled using MacBooks and iMacs as headless servers for iOS code-review and build workflows.

<details><summary>References</summary>
<ul>
<li><a href="https://namespace.so/blog/mac-at-any-scale">Mac at any scale | Namespace</a></li>
<li><a href="https://dzen.ru/b/auobbcRL2iIDzEZm">Namespace поставила сотни MacBook в стойки вместо Mac ... | Дзен</a></li>
<li><a href="https://namespace.so/blog/mac-at-any-scale">Mac at any scale - Namespace</a></li>

</ul>
</details>

**Tags**: `#macOS infrastructure`, `#iOS toolchains`, `#build automation`, `#Apple ecosystem`, `#data centers`

---

<a id="item-tech-news-7"></a>
### [Aircraft Noise Can Reveal a Video&\#x27;s Exact Location](https://simonwillison.net/2026/Nov/3/a-sound-that-leaks-your-exact-location/) ⭐️ 7.0/10

A video by Colsto demonstrates an OSINT technique for inferring a video&\#x27;s exact location from barely perceptible aircraft noise in its soundtrack. The method extracts Doppler curves from the audio and cross-references them with ADS-B flight data, using flight speed, distance, and gaps between aircraft to narrow down the recording position. The technique highlights a privacy risk because ordinary background audio in videos can contain location-revealing signals. Simon Willison&\#x27;s post summarizes the demonstration but does not provide implementation details or independently verify the precision of the results.

rss · Simon Willison · Nov 3, 05:32

**「How the geolocation method works」** Aircraft noise undergoes a Doppler shift as an aircraft approaches or recedes, so its pitch changes over time can reveal the relative motion of nearby aircraft. Automatic Dependent Surveillance–Broadcast \(ADS-B\) supplies flight-position and velocity data, allowing investigators to model the Doppler curves expected at candidate recording locations and compare them with the soundtrack.

**「Impact」** ...

<details><summary>References</summary>
<ul>
<li><a href="https://maxintel.org/aircraft-doppler-audio-geolocation-2026.html">Planes Leak Your Location: Doppler Audio Geolocation Explained</a></li>
<li><a href="https://www.techradar.com/computing/cyber-security/youtuber-discovers-aircraft-noise-trick-that-can-geolocate-your-videos-to-within-100m-doppler-effect-pinpoints-locations-from-just-60-seconds-of-audio">YouTuber discovers aircraft noise trick that can geolocate ...</a></li>
<li><a href="https://www.youtube.com/watch?v=UytYrhYLOKI">I discovered a sound that leaks your exact location (and it&#x27;s ... YouTuber Reveals How Sounds Humans Cannot Hear Can Expose a ... I discovered a sound that leaks your exact location (and it&#x27;s ... GitHub - AlanBacker/audio-flyover-geolocation: Locate where a ... aircraft-doppler-geolocation · Plugin Catalog | Hermes Agent</a></li>
<li><a href="https://github.com/1337isnot1337/DOPPLERGEIST">GitHub - 1337isnot1337/DOPPLERGEIST: A tool to geolocate audio ...</a></li>

</ul>
</details>

**Tags**: `#OSINT`, `#privacy`, `#geolocation`, `#audio analysis`, `#ADS-B`

---

<a id="item-tech-news-8"></a>
### [Russia Moves to Protect Data Centers Amid Drone Strikes](https://arstechnica.com/ai/2026/11/russia-looks-to-hide-data-centers-underground-as-ukrainian-drones-strike-back/) ⭐️ 7.0/10

Ukrainian drone strikes have damaged Russian data-center facilities housing AI supercomputers and disrupted cloud services for millions of users, prompting operators to harden facilities and consider underground construction. Rostelcom has discussed moving some data centers underground with Norilsk, while a regional governor has proposed building facilities in open-pit coal mines and covering them with public parks as camouflage. On November 2, President Vladimir Putin ordered Russian data-center operators to reserve 10% of their available space and computing capacity for emergency government needs, with access required within 24 hours after notification. The decree also allows the government, with Federal Security Service approval, to temporarily use foreign data-center resources, as strikes have degraded or knocked out facilities operated by Yandex, Sberbank, VKontakte, and the Russian Ministry of Finance.

rss · Ars Technica · Nov 3, 20:39

**「War and data-center resilience」** Cloud and AI services depend on physical data-center sites as well as electricity, cooling, and network links, making them vulnerable to drone or missile attacks on infrastructure. In the Russia–Ukraine context, underground or repurposed-mine construction is intended to improve physical protection, while the November 2 decree requiring private data-center operators to reserve 10% of available space and capacity represents a broader continuity-of-government measure.

**「Cloud and AI services face heightened disruption risk」** Russian cloud and AI users face acute availability risks because strikes seriously damaged Yandex’s Sasovo data center, hit three of its five Russian facilities, forced shutdowns, and left many Yandex Cloud services offline. Underground construction and mandated emergency capacity remain prospective resilience measures rather than immediate protection from further outages.

<details><summary>References</summary>
<ul>
<li><a href="https://understandingwar.org/research/russia-ukraine/russian-offensive-campaign-assessment-november-2-2026/">Russian Offensive Campaign Assessment, Nov 2 , 2026 | ISW</a></li>
<li><a href="https://www.techradar.com/pro/data-centers-can-be-located-in-exhausted-open-pits-russia-eyes-300-meter-deep-coal-mines-to-shield-server-infrastructure-from-ukrainian-drones">Russia eyes abandoned coal mines for underground data centers</a></li>
<li><a href="https://www.theregister.com/security/2026/10/12/ukrainian-drone-strikes-on-yandex-datacenters-knock-cloud-and-payments-offline/5302577">Ukrainian drone strikes on Yandex datacenters knock cloud and...</a></li>
<li><a href="https://www.tomshardware.com/tech-industry/data-centers/ukrainian-drones-hit-russias-yandex-data-centers-housing-two-top-supercomputers-major-outage-follows-retaliatory-strike">Ukrainian drones hit Russia &#x27;s Yandex data centers housing two top...</a></li>

</ul>
</details>

**Tags**: `#AI infrastructure`, `#data centers`, `#cloud computing`, `#infrastructure resilience`, `#geopolitics`

---

<a id="item-tech-news-9"></a>
### [Google Dismantles x.cpe Botnet on 1.3 Million Android TV Boxes](https://arstechnica.com/google/2026/11/google-dismantles-botnet-secretly-running-on-1-3-million-android-tv-boxes/) ⭐️ 7.0/10

Google’s Threat Intelligence Group said it dismantled x.cpe, a modular botnet that reached more than 1.3 million Android TV devices at its height. Most infected devices were Google-certified MECOOL boxes made by Shenzhen-based Videostrong Technology; the malware evaded certification screening by being remotely installed through a backdoor after the devices were set up. The malware evolved from a single-stage dropper into a three-stage platform, with an initial x.cpe/com.oemservice stub using system-level permissions to install modules and disable Play Protect. Google observed most compromised boxes running residential proxies or ad-fraud modules, while Videostrong retained remote capabilities including terminal commands, screen capture, and local-network probing, exposing a significant failure in certification and post-sale security controls.

rss · Ars Technica · Nov 3, 17:08

**「Background」** Android TV devices seeking access to Google apps and branding undergo Google&\#x27;s certification process, while Play Protect normally checks installed apps for malicious behavior. The x.cpe operation exploited the gap between factory certification and later operation: after compromised Videostrong boxes—mostly sold under the MECOOL brand—came online, a system-level stub disabled Play Protect and installed additional malware modules on command. Google said it would improve firmware-integrity checks for certified Android TV devices and barred Videostrong and future subsidiaries or affiliates from building certified products or supplying software to certified vendors.

**「Impact」** Google’s takedown disrupted x.cpe and deprived its operators of access to more than 1.3 million infected Android TV boxes, reducing their use as residential proxies and ad-fraud nodes. The compromise may not be over, however, because the Videostrong firmware backdoor reportedly remains on affected devices, leaving owners exposed until the firmware is remediated or the boxes are replaced.

<details><summary>References</summary>
<ul>
<li><a href="https://cloud.google.com/blog/topics/threat-intelligence/shutting-the-door-on-the-xcpe-botnet">Shutting the Door on the XCPE Botnet | Google Cloud Blog</a></li>
<li><a href="https://cybernews.com/security/videostrong-android-tv-box-backdoor-botnet-dismantled-by-google/">Videostrong Android TV botnet hit 1.3M devices, Google says ...</a></li>
<li><a href="https://thehackernews.com/2026/11/google-disrupts-13-million-device.html">Google Disrupts 1 . 3 Million - Device Android Botnet, Says TV Box...</a></li>
<li><a href="https://www.malwarebytes.com/blog/mobile/2026/11/a-hidden-backdoor-put-1-3-million-tv-boxes-to-work-for-criminals">A hidden backdoor put 1 . 3 million TV boxes to work for... | Malwarebytes</a></li>
<li><a href="https://www.theverge.com/tech/1024807/google-botnet-android-tv-shut-down">One of Google ’s Android partners turned 1 . 3 million ... | The Verge</a></li>

</ul>
</details>

**Tags**: `#Android TV`, `#botnet`, `#malware analysis`, `#cybersecurity`, `#supply-chain security`

---

<a id="item-tech-news-10"></a>
### [Binance Details a Multistage $6.3B Crypto Heist](https://www.theverge.com/news/1025576/binance-cyrpto-theft-explained) ⭐️ 7.0/10

Binance says a reported $6.3 billion crypto theft—the largest to date—resulted from a months-long intrusion rather than a single breach or phishing attempt. The operation began with fake recruiting and job interviews, followed by the compromise of a developer who downloaded a tampered installer apparently distributed through a malicious Google advertisement. The exposed information helped attackers target engineers, while malicious software distribution and possible misuse of an internal AI tool expanded the operation. Binance characterizes the case as a combination of persistent social engineering and supply-chain techniques that the exchange was not prepared to stop.

rss · The Verge · Nov 3, 22:04

**「Attack-chain context」** The incident combines social engineering with a software-supply-chain compromise: fake recruiting outreach induced a developer to install tampered software distributed through a malicious Google advertisement, exposing engineering systems to the attackers. Binance describes it as a months-long, multi-stage intrusion rather than an isolated phishing event, with reports also identifying misuse of an internal AI tool, although the supplied material does not specify its exact function. This approach reflects the cybersecurity concern that patient, long-running campaigns can combine recruitment lures, developer targeting, and poisoned software distribution.

**「Impact」** ...

<details><summary>References</summary>
<ul>
<li><a href="https://www.foxbusiness.com/fox-news-tech/binance-details-how-fake-job-interview-led-6-3b-crypto-heist">Binance details how a fake job interview led to a $6.3B ...</a></li>
<li><a href="https://www.reuters.com/world/binance-says-hackers-used-fake-job-interview-compromise-computer-before-63-2026-11-03/">Binance hackers used fake job interview in $6.3 billion ...</a></li>
<li><a href="https://www.cnbc.com/2026/11/03/binance-co-ceo-teng-says-hackers-used-fake-job-interviews-to-steal-6point3-billion-in-crypto.html">Binance co-CEO Teng says hackers used fake job interviews to ...</a></li>
<li><a href="https://coinpedia.org/research-report/binance-hack-detailed-report-what-happened-how-6-3-billion-was-stolen-and-whats-next/">Binance Hack 2026: The $6.3 Billion Crypto Theft, How It ...</a></li>
<li><a href="https://www.businessinsider.com/binance-hack-heist-crypto-security-2026-10">Binance Says 90% of $6.3 Billion in Crypto Stolen in Hack ...</a></li>
<li><a href="https://www.forbes.com/sites/digital-assets/2026/11/03/the-63-billion-binance-hack-exposes-cryptos-biggest-internal-control-problem/">The $6.3 Billion Binance Hack Exposes Crypto&#x27;s Biggest ...</a></li>

</ul>
</details>

**Tags**: `#cybersecurity`, `#supply-chain attack`, `#AI security`, `#social engineering`, `#cryptocurrency`

---

<a id="item-tech-news-11"></a>
### [CrowdStrike to Buy Fiddler AI and Dreadnode](https://techcrunch.com/2026/11/03/crowdstrike-to-shell-out-nearly-500m-for-2-ai-security-startups-as-the-market-for-securing-agents-takes-off/) ⭐️ 7.0/10

CrowdStrike plans to acquire Fiddler AI and Dreadnode in a deal reported to total nearly $500 million. Fiddler AI provides observability software for AI agents, while Dreadnode helps organizations automate AI security testing. The acquisitions would strengthen CrowdStrike’s capabilities across the monitoring and testing of AI agents as the market for agent-security tools expands. The supplied report does not specify the deal breakdown, closing conditions, product integration plans, or performance benchmarks.

rss · TechCrunch · Nov 3, 17:56

**「Acquisition and AI-security context」** CrowdStrike has an established acquisition history, including Payload Security in 2017, which developed automated malware-analysis sandbox technology, and Preempt Security in 2020 for $96 million, a zero-trust and conditional-access provider. In this deal, Fiddler AI supplies software for monitoring AI agents within enterprises, while Dreadnode focuses on automated security testing to identify flaws in AI models, applications, and agents before deployment.

**「Impact on AI-agent security」** If completed, CrowdStrike&\#x27;s planned acquisitions of Fiddler AI and Dreadnode would add enterprise AI-agent observability and automated pre-deployment security testing for AI models, applications, and agents to the Falcon platform.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/CrowdStrike">CrowdStrike - Wikipedia</a></li>
<li><a href="https://techcrunch.com/2026/11/03/crowdstrike-to-shell-out-nearly-500m-for-2-ai-security-startups-as-the-market-for-securing-agents-takes-off/">CrowdStrike to shell out nearly $ 500 M for 2 AI security ... | TechCrunch</a></li>
<li><a href="https://techcrunch.com/2026/11/03/crowdstrike-to-shell-out-nearly-500m-for-2-ai-security-startups-as-the-market-for-securing-agents-takes-off/">CrowdStrike to shell out nearly $500M for 2 AI security ... | TechCrunch</a></li>
<li><a href="https://www.crowdstrike.com/en-us/blog/">Cybersecurity Blog | CrowdStrike</a></li>

</ul>
</details>

**Tags**: `#AI security`, `#AI agents`, `#acquisitions`, `#observability`, `#security testing`

---

<a id="item-tech-news-12"></a>
### [Raspberry Pi raises 16GB Pi 5 price to $385](https://www.theregister.com/personal-tech/2026/11/03/raspberry-pi-hikes-prices-again-barely-a-month-after-the-last-round/5307004) ⭐️ 7.0/10

Raspberry Pi has reportedly raised the price of the 16GB Pi 5 to $385 amid a memory-market crunch. The price is more than triple the model’s launch price and comes barely a month after another round of increases. The rapid repricing could materially affect hobbyists, educators, and edge-computing buyers, although the supplied report provides little technical or broader market context.

rss · The Register · Nov 3, 09:30

**「Pricing and supply context」** The 16GB Raspberry Pi 5 uses high-density DRAM for which Raspberry Pi says alternative supply is unavailable, while other component shortages continue. The company raised the model by $80 to $385 on November 2, 2026, following a previous increase to $305; this is more than triple its January 2025 launch price.

**「Impact」** Buyers requiring a 16GB Raspberry Pi 5 now pay $385 after an $80 increase, sharply raising the cost of high-memory single-board computing and encouraging consideration of mini PCs or rival boards, though competitors also face RAM-related price hikes.

<details><summary>References</summary>
<ul>
<li><a href="https://www.techtroduce.com/raspberry-pi-5-16gb-price-increase-november-2026/">Raspberry Pi 5 16GB Price Rises to $385 Amid Memory Shortage</a></li>
<li><a href="https://www.raspberrypi.com/news/price-rises-for-some-16gb-raspberry-pi-products/">Price rises for some 16GB Raspberry Pi products</a></li>
<li><a href="https://tech.yahoo.com/computing/articles/16gb-raspberry-pi-5-hiked-161735763.html">16GB Raspberry Pi 5 hiked to $385, more than triple its ...</a></li>
<li><a href="https://windowsreport.com/raspberry-pi-5-16gb-now-costs-385-after-another-price-increase/">Raspberry Pi 5 16GB Now Costs $385 After Another Price Increase</a></li>
<li><a href="https://www.raspberrypi.com/news/price-rises-for-some-16gb-raspberry-pi-products/">Price rises for some 16GB Raspberry Pi products</a></li>
<li><a href="https://www.zdnet.com/tech/16gb-raspberry-pi-5-price-increase/">Why the 16GB Raspberry Pi 5 costs $385 now - ZDNET</a></li>

</ul>
</details>

**Tags**: `#Raspberry Pi`, `#hardware pricing`, `#memory shortages`, `#single-board computers`

---

<a id="item-tech-news-13"></a>
### [OpenVDDK emerges as an alternative to undisclosed VMware migration tooling](https://www.theregister.com/virtualization/2026/11/03/architect-creates-open-source-replacement-for-vm-migration-tool-vmware-has-hidden/5307124) ⭐️ 7.0/10

An architect has created OpenVDDK as an open-source alternative to VM-migration tooling that VMware kept undisclosed. The project is reportedly already being used in production at scale, making it more consequential than an experimental release. OpenVDDK may give infrastructure teams a transparent option for VM migration workflows rather than requiring reliance on an opaque VMware component. However, the supplied excerpt does not specify supported platforms, VMware compatibility, feature parity, licensing terms, or the evidence behind the production-use claim.

rss · The Register · Nov 3, 04:45

**「Background」** VMware&\#x27;s Virtual Disk Development Kit \(VDDK\) is a collection of libraries and utilities that lets backup and migration software access virtual disks; VMware recently withdrew it from public downloads, prompting the creation of an independent alternative. OpenVDDK is an Apache 2.0-licensed implementation written from public documentation and black-box testing, without VMware code, designed as a drop-in replacement for libvixDiskLib.so.8.0.3. It has been tested against four vSphere releases, establishing a stated compatibility baseline for VMware backup and migration workflows.

**「Practical impact」** Organizations migrating VMware virtual machines without access to VDDK gain an open-source alternative in OpenVDDK, a clean-room GPL-3.0 implementation positioned as a drop-in replacement and reportedly already used at production scale. OpenVDDK is not the only option: OpenNebula OneSwap advertises a 96% success rate, while Nutanix has updated Move to support migrations without VDDK.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theregister.com/virtualization/2026/11/03/architect-creates-open-source-replacement-for-vm-migration-tool-vmware-has-hidden/5307124">Architect creates open source replacement for VM migration ...</a></li>
<li><a href="https://shattered.io/openvddk-open-source-vmware-vddk-replacement-4-vsphere-versions-2026/">OpenVDDK Replaces VMware&#x27;s VDDK, Tested on 4 vSphere [2026]</a></li>
<li><a href="https://openvddk.com/">OpenVDDK – Independent Virtual Disk Library</a></li>
<li><a href="https://www.theregister.com/virtualization/2026/11/03/architect-creates-open-source-replacement-for-vm-migration-tool-vmware-has-hidden/5307124">Architect creates open source replacement for VM migration tool...</a></li>
<li><a href="https://github.com/jimmyma-zhanwei/openvddk">GitHub - jimmyma-zhanwei/ openvddk : Clean-room, high-performance...</a></li>

</ul>
</details>

**Tags**: `#virtualization`, `#VM migration`, `#open source`, `#VMware`

---

<a id="item-tech-news-14"></a>
### [StateBench Tests Long-Context State Tracking](https://huggingface.co/blog/allenai/statebench) ⭐️ 7.0/10

StateBench is a new benchmark that measures whether language models can track entity and variable states through long sequences, with four controlled difficulty levels: r-trivial, aperiodic, soluble, and general finite. Each level adds progressively richer assignments—from immutable values and latest-value replacement to self-referential updates and references between variables—while comparable problems retain the same variables, values, and update positions. In open pretrained models, including 7-billion-parameter Olmo 3 and Olmo Hybrid with Gated DeltaNet layers, performance was strong on r-trivial, declined on aperiodic tasks as inputs grew, and remained near chance on general finite tasks; representation also mattered, with a 275-million-parameter hybrid near the ceiling on RULER-style tasks but near chance on spreadsheet-edit versions. The tested frontier models—Gemini 3.8 Flash, Claude Opus 5.5, and GPT-6 Sol and Luna—handled the two easiest levels well but deteriorated sharply on soluble and general finite problems as inputs lengthened, falling to 13% or lower on the longest general finite problems. When 275-million-parameter models were trained directly on sequences of up to 256 assignments and tested with as many as 64,000 assignments, Gated DeltaNet and hybrid models generalized almost perfectly through the soluble level, while transformers degraded with length and never learned general finite problems.

rss · Hugging Face Blog · Nov 3, 17:15

**「Why State Tracking Matters」** State tracking is the ability to preserve and update facts about entities as a document evolves, such as variable reassignment in code or object possession in a story. Transformers have documented theoretical limits on difficult dependency-chain state tracking, motivating recurrent and hybrid architectures such as Gated DeltaNet that maintain a running memory, and StateBench is designed to distinguish both where architectures fail and which simpler patterns they can handle.

**「Practical Evaluation Impact」** StateBench gives researchers a controlled way to compare long-context reliability by architecture, task complexity, and input format rather than treating it as one undifferentiated capability. Its results suggest that recurrent and hybrid memory designs can scale better on dependency-heavy updates in these experiments, while the format sensitivity shows that wording and representation can materially change benchmark results.

**Tags**: `#large language models`, `#long-context evaluation`, `#state tracking`, `#AI benchmarks`

---

<a id="item-tech-news-15"></a>
### [Antigravity Agent Accelerates Macrocycle Design for Lung-Cancer Drug Discovery](https://deepmind.google/blog/agentic-cheminformatics-with-google-antigravity/) ⭐️ 7.0/10

Google DeepMind says its new Cheminformatics Skills for Google Antigravity let an AI agent search thousands of lung-cancer compounds, perform matched molecular pair analysis, train and validate multiple molecular potency models, and propose rigidified macrocycles with reaction and synthesis routes in about an hour rather than the multiple days such a workflow previously required. The skills use the underlying language model for orchestration, database navigation, and scientific reasoning while deterministic RDKit-based tools perform chemistry calculations and connectors bring in ChEMBL and PubChem data; results can be exported to standard chemistry packages, and designs can be prepared for AlphaFold or molecular-dynamics analysis. Guided by the rigidification of crizotinib into the more potent lorlatinib, the demonstration found that cyclization generally reduced rotatable bonds and increased potency, matching the intended medicinal-chemistry relationship. Google says the skills are available through the Antigravity Science plugin, with an Enterprise route using Google Cloud credentials and 10,000 scientists offered the highest usage tier free for six months on a rolling basis. The designs remain hypotheses: sparse data, inter-laboratory assay noise, narrow dynamic ranges, and limited predictive precision mean every candidate still requires synthesis and experimental validation.

rss · DeepMind Blog · Nov 3, 17:01

**「Cheminformatics foundations」** Cheminformatics applies computational methods to molecular structures and activity data, but a single drug-discovery iteration can require reconciling literature, assay records, and inconsistent chemical representations before candidates can be evaluated. Matched molecular pair analysis isolates the effects of small structural changes by comparing closely related molecules, while molecular rigidification adds bonds to reduce conformational freedom and can improve target-binding potency. In Google Antigravity, a language model orchestrates these workflows and delegates calculations to deterministic tools such as RDKit, but its molecular designs remain hypotheses that must be synthesized and experimentally validated.

**「Impact」** For drug-discovery scientists using Google Antigravity, the new Cheminformatics Skills can compress a multi-day literature-to-molecular-design workflow into roughly an hour of data curation, analysis, macrocycle proposal, and synthesis-route planning, potentially shortening research iterations. The outputs remain hypotheses requiring synthesis and experimental validation, and independent laboratory confirmation of predicted potency and proposed routes is still needed.

<details><summary>References</summary>
<ul>
<li><a href="https://deepmind.google/blog/agentic-cheminformatics-with-google-antigravity/">Agentic Cheminformatics with Google ... — Google DeepMind</a></li>
<li><a href="https://deepmind.google/blog/agentic-cheminformatics-with-google-antigravity/">Agentic Cheminformatics with Google Antigravity</a></li>
<li><a href="https://aiunderstanding.org/news/google-antigravity-adds-cheminformatics-skills-for-drug-discovery">Google Antigravity adds cheminformatics skills for drug discovery</a></li>

</ul>
</details>

**Tags**: `#agentic AI`, `#cheminformatics`, `#drug discovery`, `#molecular generation`, `#Google DeepMind`

---

<a id="item-tech-news-16"></a>
### [Palette fine-tunes a 20B model for private deck generation](https://huggingface.co/blog/ibm-research/palette-deck-building) ⭐️ 6.0/10

IBM Research&\#x27;s Palette fine-tunes a 20B open-weight model with a LoRA adapter to generate PowerPoint decks that follow an organization’s design language while remaining self-hosted, allowing confidential material to stay within internal systems. It separates editorial planning from rendering: a designer role creates a structured JSON brief, while parallel coder calls produce PptxGenJS code for each slide, reportedly making the coding stage about 6–7× faster and allowing individual slide specs to be edited or steered through plain-English directives. Training used roughly 1,000 synthetic IBM Design Language decks covering about 10,000 slides, with counterfactual reasoning, rendered feedback, and 5× oversampling of shorter designer examples; reference decks proved more reliable than prompt rules for preventing fabricated content. A check-and-repair harness applies rule-based fixes, detects overlapping, clipped, or overflowing elements, and invokes a separate editor model to rewrite failing slides; Palette ranked first in two of three measured PresentBench domains, although the article provides no detailed benchmark results, release information, or evidence that it matches frontier models overall.

rss · Hugging Face Blog · Nov 3, 16:35

**「Context」** Slide-generation models must solve two coupled problems: making editorial decisions about a deck’s story and visual form, then calculating the geometry needed to render text, charts, and shapes without clipping or overlap. Palette separates these tasks into a designer, which produces an editable JSON brief, and a coder, which converts each slide specification into pptxgenjs code; a LoRA adapter teaches a 20B open-weight base model both roles, while a rendering-and-repair harness checks the output. PresentBench provides the evaluation context for the authors’ claim that Palette ranks first in two of three measured domains, although the supplied excerpt does not include the domain-level scores.

**「Impact」** Organizations with confidential slide content can adapt the self-hosted 20B Palette model to generate decks in a chosen design language without sending source material to an external service, while a rendering harness checks and repairs layout defects. Palette scored 59.7 on IBM’s PresentBench versus NotebookLM’s 60.8 and led two of three domains, but the evaluation used a separate frontier model to create slide plans, so it demonstrates competitiveness in planned-deck workflows rather than end-to-end parity with frontier systems.

<details><summary>References</summary>
<ul>
<li><a href="https://explainx.ai/blog/ibm-research-palette-20b-open-weight-deck-builder-designer-coder-harness-presentbench-2026">IBM Palette: 20B Model Ranks 2nd on PresentBench Decks ...</a></li>
<li><a href="https://arxiv.org/abs/2603.07244">[2603.07244] PresentBench: A Fine-Grained Rubric-Based ... PresentBench: A Fine-Grained Rubric-Based Benchmark for Slide ... Palette: teaching a small model to build decks in your design ... IBM says its 20B slide-building model ranks second in a three ... IBM Research trains 20B model on its design language for ... Palette: teaching a small model to build decks in your ...</a></li>

</ul>
</details>

**Tags**: `#small language models`, `#open-weight AI`, `#slide generation`, `#fine-tuning`, `#privacy`

---

<a id="item-tech-news-17"></a>
### [Nature article examines AI predictive modeling in precision medicine](https://news.google.com/rss/articles/CBMiX0FVX3lxTE16NWIxdF9vMHNNVGpKbVl4V1dNc1V6VFFNaDU3czQ0TmFoTVFOTWk5RDhJT1N1WmJhVmpUVnl3M25ZazVndVFpYnNYOW5CVXZuMlI1emF3WW94dHdhUDdF?oc=5) ⭐️ 6.0/10

The Nature article examines emerging applications of machine learning and artificial intelligence in predictive modeling for precision medicine. The supplied excerpt contains only the headline and does not identify particular applications, models, datasets, validation methods, performance results, or clinical deployments. Its technical novelty, evidence quality, limitations, and immediate implications therefore cannot be assessed without the full article.

google\_news · Nature · Nov 3, 17:18

**「Context」** Precision medicine seeks to tailor treatments to individual variability in genetics, environment, and lifestyle, marking a departure from conventional one-size-fits-all care. In this setting, machine learning and AI support predictive modeling for patient-specific assessment and clinical decision-making; the Nature item is part of a Nature Digital Medicine special issue on emerging applications in this field.

**「Impact」** For precision-medicine researchers and AI practitioners, the Nature Digital Medicine special issue provides a curated view of emerging machine-learning and predictive-modeling approaches for tailoring care to patient-specific variability. However, the available material reports no clinical validation or deployment results, so it does not yet substantiate improved patient outcomes or immediate clinical adoption.

<details><summary>References</summary>
<ul>
<li><a href="https://medicine.net/news/TechnologyAI/Emerging-Applications-of-Machine-Learning-and-AI-for-Predictive-Modeling-in-Precision-Medicine.html">Emerging Applications of Machine Learning and AI ... - Medicine .net</a></li>
<li><a href="https://www.linkedin.com/posts/ravi-vaidyanathan-96267016_deep-learning-enabled-accurate-assessment-activity-7447649442033192960-QJ1_">Deep learning -enabled accurate assessment of gait impairments in...</a></li>
<li><a href="https://medicine.net/news/TechnologyAI/Emerging-Applications-of-Machine-Learning-and-AI-for-Predictive-Modeling-in-Precision-Medicine.html">Emerging Applications of Machine Learning and AI ... - Medicine .net</a></li>
<li><a href="https://www.linkedin.com/posts/ravi-vaidyanathan-96267016_deep-learning-enabled-accurate-assessment-activity-7447649442033192960-QJ1_">Deep learning -enabled accurate assessment of gait impairments in...</a></li>
<li><a href="https://www.nature.com/articles/s41746-026-03393-9">Emerging applications of machine learning and AI for ... - Nature</a></li>

</ul>
</details>

**Tags**: `#machine learning`, `#artificial intelligence`, `#predictive modeling`, `#precision medicine`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Major stocks diverge after earnings](https://www.cnbc.com/2026/11/03/stocks-making-the-biggest-moves-premarket-pfe-pltr-aapl-zbra.html) ⭐️ 7.0/10

Major stocks diverged in premarket trading after earnings: Revvity rose 7% after raising full-year pro forma adjusted EPS guidance to $5.40-$5.45 from $5.30-$5.40, while Apple fell nearly 4% after its margin forecast and fiscal fourth-quarter iPad sales missed estimates. Pfizer was flat after third-quarter adjusted EPS of $0.87 and revenue of $16.58 billion beat LSEG expectations of $0.73 and $15.87 billion; Palantir fell nearly 8% despite an earnings beat and 148% U.S. commercial revenue growth to $984 million, while Zebra Technologies dropped over 6% despite a quarterly beat because its free-cash-flow guidance was below estimates.

rss · CNBC Finance · Nov 3, 12:47

**「Background」** The premarket moves followed quarterly earnings reports, with investors comparing adjusted profits, revenue and full-year guidance against analyst forecasts before the U.S. trading day.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/11/03/stocks-making-the-biggest-moves-premarket-pfe-pltr-aapl-zbra.html">Stocks making the biggest moves premarket : PFE, PLTR, AAPL...</a></li>

</ul>
</details>

**Tags**: `#earnings results`, `#corporate guidance`, `#premarket trading`, `#technology stocks`, `#pharmaceuticals`

---

<a id="item-finance-news-2"></a>
### [AI Infrastructure Buildout Seen Needing More Equity](https://www.cnbc.com/2026/11/03/equity-ai-debt-blackstone-pimco-financing.html) ⭐️ 7.0/10

Blackstone President Jon Gray said the AI infrastructure buildout will require more equity financing as lenders become increasingly exposed to the companies funding it.

rss · CNBC Finance · Nov 3, 06:46

**「Background」** Pimco CEO Emmanuel Roman cited an estimate that AI-related capital spending could reach about $10 trillion over five years and said $550 billion in AI debt had been issued so far this year, compared with a global corporate bond market of roughly $20 trillion.

**「Impact」** AI infrastructure companies may face a heavier equity-funding burden, while lenders could remain concentrated in a small group of borrowers with unusually large financing needs.

**Tags**: `#AI infrastructure`, `#debt financing`, `#equity capital`, `#data-center spending`, `#financial concentration risk`

---