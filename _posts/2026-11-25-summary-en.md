---
layout: default
title: "Horizon Summary: 2026-11-25 (EN)"
date: 2026-11-25
lang: en
---

> From 111 items, 16 important content pieces were selected

---

**Technology News**
1. [Matrix Multiplication Exponent Reportedly Settled at 2.25](#item-tech-news-1) ⭐️ 9.0/10
2. [GPT-6 protein designs bind in lab but still rely on specialist tools](#item-tech-news-2) ⭐️ 8.0/10
3. [Active intrusion campaign against Check Point security management servers](#item-tech-news-3) ⭐️ 8.0/10
4. [AI-Assisted Riemann Hypothesis Proof Under Review](#item-tech-news-4) ⭐️ 8.0/10
5. [Amazon says hackers&\#x27; AI agents found and exploited 0-day with little human input](#item-tech-news-5) ⭐️ 8.0/10
6. [VMware vCenter 9.8 Authentication Bypass Fixed After Zero-Day Exploitation](#item-tech-news-6) ⭐️ 8.0/10
7. [Three LLM Capability Inflection Points in 2026](#item-tech-news-7) ⭐️ 7.0/10
8. [Microsoft declares “Code Red” overhaul after historic Microsoft 365 outage](#item-tech-news-8) ⭐️ 7.0/10
9. [Tidal Bans Fully AI-Generated Music and Deletes 27 Million Tracks](#item-tech-news-9) ⭐️ 7.0/10
10. [Nvidia Reinstates Jensen Huang After Political Pressure](#item-tech-news-10) ⭐️ 7.0/10
11. [Oil and Chemical Shipping Vessels Reportedly Targeted in Cyberattacks](#item-tech-news-11) ⭐️ 7.0/10
12. [Amazon’s Decart Deal Targets Trainium Software Performance](#item-tech-news-12) ⭐️ 7.0/10
13. [CrowdStrike’s reported $44B Zscaler acquisition raises integration and pricing concerns](#item-tech-news-13) ⭐️ 7.0/10
14. [Microduck Obstacle Avoidance with Isaac Lab and Newton](#item-tech-news-14) ⭐️ 6.0/10
15. [Astra and Codex Assist Amateur Exoplanet Searches](#item-tech-news-15) ⭐️ 6.0/10
16. [ByteDance Open-Sources Laminar for Async RL Post-Training](#item-tech-news-16) ⭐️ 6.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Matrix Multiplication Exponent Reportedly Settled at 2.25](https://github.com/openai/math/blob/main/preprints/The-matrix-multiplication-exponent-is-nine-fourths-November-24-2026/paper.pdf) ⭐️ 9.0/10

The linked OpenAI preprint, titled “The matrix multiplication exponent is nine fourths,” reportedly proves that the matrix-multiplication exponent is exactly 9/4, or 2.25. The exponent denotes the infimum of growth rates ω for algorithms that multiply n×n matrices, so an O\(n^2.25\) upper bound alone was not the breakthrough; according to the discussion, that bound was already known, while the claimed new result is a matching Ω\(n^2.25\) lower bound. If valid over every field, as a commenter asserts, the result would establish the exact exponent and rule out any algorithm with an exponent below 2.25. Because the supplied material contains only a link and comments rather than the paper text or independent verification, the theorem, its field scope, and broader claims should be treated as unconfirmed.

hackernews · E-Reverance · Nov 25, 01:19 · [Discussion](https://news.ycombinator.com/item?id=50637220)

**「Matrix Multiplication Bounds」** The matrix-multiplication exponent ω is the infimum of exponents achievable by algorithms for multiplying two n × n matrices using arithmetic operations. The upper bound ω ≤ 9/4 was already known; proving the exact value ω = 9/4 additionally requires showing that every arithmetic circuit needs Ω\(n^9/4\) multiplication or division gates. The supplied proof connects this lower bound to tensor-network compression and an obstruction involving testing whether entries in independent lists are distinct.

**「Impact」** If the preprint’s theorem is accepted, it proves an Ω\(n^2.25\) lower bound that matches the already-known O\(n^2.25\) upper bound, making existing matrix-multiplication algorithms asymptotically optimal and ruling out any o\(n^2.25\) algorithm in the standard arithmetic-operation model. The principal consequence is theoretical rather than a new practical speedup, since the upper-bound algorithms already existed.

**「Community Context」** Commenters recognized the result’s potential significance but corrected the framing: the O\(n^2.25\) upper bound was already known, making the claimed novelty the matching lower bound and exactness of the exponent rather than a new practical multiplication algorithm. One commenter asserts that the proof covers every field and connects it to several other claimed Top 500 problem resolutions, while another speculates that the work came from an unreleased model; none of these broader claims is independently verified in the supplied material.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2610.28627">[2610.28627] Matrix Multiplication from Polynomial Packings ...</a></li>
<li><a href="https://raw.githubusercontent.com/openai/math/main/preprints/The-matrix-multiplication-exponent-is-nine-fourths-November-24-2026/paper.pdf">The matrix multiplication exponent is nine fourths</a></li>
<li><a href="https://arxiv.org/html/2611.09716v1">Tensor value and the 9/4 bound for matrix multiplication</a></li>
<li><a href="https://interestingengineering.com/culture/openai-exact-2-25-matrix-multiplication-exponent">OpenAI establishes exact 2.25 exponent for matrix multiplication</a></li>

</ul>
</details>

**Tags**: `#matrix multiplication`, `#theoretical computer science`, `#algorithms`, `#complexity theory`, `#OpenAI`

---

<a id="item-tech-news-2"></a>
### [GPT-6 protein designs bind in lab but still rely on specialist tools](https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities) ⭐️ 8.0/10

OpenAI reports that its GPT-6 family can design protein structures and amino-acid sequences through reasoning and code without using specialized biology models to generate the designs. An internal research model matched or outperformed specialist systems on many computational tasks, and the latest models performed comparably to or better than specialists on most evaluated tasks, although complete protein-structure prediction remained a weakness. In laboratory work with Onava, proteins based on structural designs from a pre-release GPT-6.2 bound all five tested targets, with 35 of 322 minibinders testing positive \(10.9%\); however, SolubleMPNN supplied the sequences and other specialist models selected candidates. GPT-6.2-designed replacement sequences also showed binding in initial screens for MDM2, VEGF-A, and PD-1, at rates of 85%, 62%, and 14%, respectively, while redesigned antibodies retained binding. The preprint provides early evidence rather than proof of replacing specialist systems: the original RFdiffusion study reported higher hit rates, and results depend on candidate filtering and how binding is defined.

rss · OpenAI News · Nov 24, 13:00 · [Discussion](https://news.ycombinator.com/item?id=50634658)

**「How protein design works」** Protein design links an amino-acid sequence to the three-dimensional structure and molecular interactions that determine a protein’s function. Such workflows commonly divide the work among specialized systems: RFdiffusion generates candidate structures, while models such as SolubleMPNN and ProteinMPNN suggest amino-acid sequences and help select viable candidates. GPT‑6’s relevant distinction is that a general-purpose model can use natural-language instructions and generated code to propose or coordinate multiple design steps without being trained solely as a dedicated biology model.

**「Impact」** Protein researchers can now use GPT‑6.2 as a general-purpose design layer that generates protein structures and candidate sequences from natural-language constraints, potentially reducing the need to integrate many separate specialist models for each task. The practical advantage remains constrained: laboratory conversion still relied on specialist models for sequencing, folding, and candidate selection, and only 35 of 322 tested minibinders \(10.9%\) bound their intended targets across five targets.

**「Community discussion」** Commenters were impressed by code generation as a means for a general-purpose model to tackle protein design, but questioned what GPT-6.2 actually designed when specialist models supplied sequences and selected candidates. Several characterized the result as a promising “glue layer” between specialized systems rather than definitive evidence that GPT-6 surpasses them, and raised concerns about computation-heavy validation with limited biological controls.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/">GPT-6 models demonstrate intrinsic protein-design ... - OpenAI</a></li>
<li><a href="https://www.startuphub.ai/ai-news/ai-research/2026/gpt-6-designs-proteins-without-bio-models">GPT-6 Designs Proteins Without Bio Models | StartupHub.ai</a></li>
<li><a href="https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/">GPT - 6 models demonstrate intrinsic protein - design ... | OpenAI</a></li>

</ul>
</details>

**Tags**: `#protein-design`, `#AI-for-science`, `#foundation-models`, `#code-reasoning`, `#OpenAI`

---

<a id="item-tech-news-3"></a>
### [Active intrusion campaign against Check Point security management servers](https://www.greynoise.io/blog/check-point-security-management-servers-intrusion-campaign) ⭐️ 8.0/10

An active campaign reportedly reconstructs Check Point management-server session-signing keys from weak PRNG output, enabling forged administrator sessions.

hackernews · louiereederson · Nov 24, 16:32 · [Discussion](https://news.ycombinator.com/item?id=50630594)

**Tags**: `#Check Point`, `#active exploitation`, `#PRNG vulnerability`, `#session security`, `#cybersecurity`

---

<a id="item-tech-news-4"></a>
### [AI-Assisted Riemann Hypothesis Proof Under Review](https://arstechnica.com/ai/2026/11/whats-going-on-with-the-riemann-hypothesis/) ⭐️ 8.0/10

Mathematician Levent Alpöge, who works at Anthropic, announced a proof of the Riemann hypothesis that was developed with Claude, an LLM-based system. The claim concerns the mid-1800s problem formulated by Bernhard Riemann about the distribution of prime numbers, with implications for number theory and cryptography, so a valid proof would be a major mathematical result. The announcement links to a Mathlib initiative page with more information, but the supplied account provides no technical outline of the proof and says independent mathematicians are still digesting it. Alpöge&\#x27;s unusually florid language—and his apparent hints that some wording may have been in jest—also leave the status and seriousness of the announcement open to interpretation at this early stage.

rss · Ars Technica · Nov 24, 20:34

**「Historical and technical context」** The Riemann hypothesis, formulated by Bernhard Riemann in the mid-19th century, concerns the distribution of prime numbers and is regarded as one of mathematics’ most important open problems, with implications for number theory and cryptography. The announcement under discussion was Levent Alpöge’s formal proof, released on November 20, 2026; Alpöge is an Anthropic mathematician who used Claude in developing it, while independent mathematicians continued assessing the proof.

**「Potential impact」** If Alpöge’s Claude-assisted proof withstands independent scrutiny, it would settle one of mathematics’ most consequential open problems and mark a major advance in AI-assisted mathematical research. For now, it remains a claim under assessment rather than an accepted resolution.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Alp%C3%B6ge&#x27;s_proof_of_the_Riemann_hypothesis">Alpöge &#x27;s proof of the Riemann hypothesis - Wikipedia</a></li>
<li><a href="https://www.theguardian.com/technology/2026/nov/21/anthropic-riemann-hypothesis-solved-claude-ai">Two groups verify mathematician’s claim that Claude ... | The Guardian</a></li>
<li><a href="https://en.wikipedia.org/wiki/Alp%C3%B6ge&#x27;s_proof_of_the_Riemann_hypothesis">Alpöge &#x27;s proof of the Riemann hypothesis - Wikipedia</a></li>
<li><a href="https://www.independent.co.uk/tech/riemann-hypothesis-solved-levent-alpoge-b3088927.html">Anthropic mathematician claims to have proved Riemann hypothesis ...</a></li>
<li><a href="https://www.theguardian.com/technology/2026/nov/21/anthropic-riemann-hypothesis-solved-claude-ai">Two groups verify mathematician ’s claim that Claude ... | The Guardian</a></li>

</ul>
</details>

**Tags**: `#AI for mathematics`, `#Riemann hypothesis`, `#LLM-assisted proof`, `#mathematical research`

---

<a id="item-tech-news-5"></a>
### [Amazon says hackers&\#x27; AI agents found and exploited 0-day with little human input](https://arstechnica.com/security/2026/11/amazon-says-hackers-ai-agents-found-and-exploited-0-day-with-little-human-input/) ⭐️ 8.0/10

Amazon says attackers used Cairn AI agents to autonomously find and exploit a zero-day in a medical-imaging application and gain control of a university server.

rss · Ars Technica · Nov 24, 12:30

**Tags**: `#AI agents`, `#zero-day exploitation`, `#autonomous penetration testing`, `#Cairn`, `#AI security`

---

<a id="item-tech-news-6"></a>
### [VMware vCenter 9.8 Authentication Bypass Fixed After Zero-Day Exploitation](https://thehackernews.com/2026/11/vmware-vcenter-hit-by-another-critical.html) ⭐️ 8.0/10

Broadcom patched CVE-2026-123903, a CVSS 9.8 authentication-bypass vulnerability in VMware vCenter&\#x27;s vmdir directory service. The report says anyone able to reach vCenter could bypass authentication and enter the system directly. The flaw had reportedly been exploited as a zero-day days before Broadcom released patches covering 23 vulnerabilities across the VMware product line. The supplied report does not specify affected vCenter versions, exploitation details, or step-by-step remediation guidance.

telegram · zaihuapd · Nov 24, 14:50

**「Background」** vCenter’s VMware Directory Service \(vmdir\) handles directory and LDAP authentication for the virtualization management platform, so a flaw in this service can affect access controls before users are authenticated. CVE-2026-123903 is described as a 9.8/10 authentication bypass: a failed LDAP SASL bind can place the claimed identity’s access token on the connection, after which plaintext LDAP operations run as that identity without credentials. Broadcom addressed the issue in its VMware security update covering 23 vulnerabilities; its advisory directs administrators to the fixed versions in the response matrix and lists no workaround.

**「Operational impact」** Affected organizations with network-reachable VMware vCenter instances risk attackers bypassing authentication and gaining administrator access. Administrators should apply Broadcom’s relevant fixes and restrict vCenter access until the vulnerabilities are patched.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/dinosn/CVE-2026-123903">dinosn/ CVE - 2026 - 123903 : CVE - 2026 - 123903 : VMware vCenter vmdir ...</a></li>
<li><a href="https://support.broadcom.com/web/ecx/support-content-notification/-/external/content/SecurityAdvisories/0/39626">Support Content Notification - Support Portal - Broadcom support portal</a></li>
<li><a href="https://dzen.ru/a/awWqb8d-fTJLjsE8">VMware vCenter : новая критическая уязвимость обхода... | Дзен</a></li>
<li><a href="https://brandefense.io/knowledge-hub/vulnerabilities/cve-2026-123903/">CVE-2026-123903: vCenter Auth Bypass, Fix Status</a></li>

</ul>
</details>

**Tags**: `#vCenter`, `#鉴权绕过`, `#零日利用`, `#漏洞修复`, `#供应链安全`

---

<a id="item-tech-news-7"></a>
### [Three LLM Capability Inflection Points in 2026](https://simonwillison.net/2026/Nov/24/llm-inflection-points/) ⭐️ 7.0/10

Simon Willison identifies three inflection points in LLM and coding-agent capabilities during the twelve months preceding November 24, 2026, based on his keynote at the AI Engineer Code Summit. The first, in November 2025, was Claude Opus 4.5: it was the first model he used with Claude Code whose default result was generally correct, making the agent faster than manual work and reliably useful as a daily driver; OpenAI’s GPT-5.1 Instant, Thinking, Codex, and Codex-Max releases had a similar effect on Codex. The second, in June and July 2026, was the emergence of “Fable class” models—Fable 5, later Fable 5.1 and 5.2, Opus 5.5, and possibly GPT-6 Astra and Gemini 4 Neon—which Willison characterizes as able to pursue a stated goal with the right tools, even through brute force; his examples include autonomously instrumenting a Safari bug and triangulating a mysterious beep to within about 40 cm. The third, in September and October 2026, was much stronger 3D modeling and game development, especially with Blender and Three.js, culminating in Opus 5.5’s 12-hour playtesting and rebalancing that made a previously dull real-time strategy game fun. These are qualitative, experience-based assessments rather than benchmark-backed conclusions, and Willison notes that earlier game results could still be poor, export controls briefly blocked Fable 5, and the relationship between 3D modeling and the labs’ robotics focus remains unclear.

rss · Simon Willison · Nov 24, 23:02

**「Background」** An “inflection point” here denotes a qualitative change in how useful frontier LLMs and coding agents are, not a conventional benchmark threshold: the sequence runs from dependable coding-agent results with Claude Opus 4.5 in November 2025, to proactive tool use in June–July 2026, and then to credible 3D modeling and playable games in September–October 2026. “Fable class” is Willison’s informal term for models that, when given a goal and appropriate tools, pursue a solution through sustained experimentation rather than requiring step-by-step direction.

**「Impact on developers」** ...

<details><summary>References</summary>
<ul>
<li><a href="https://simonwillison.net/2026/Nov/24/llm-inflection-points/">Three LLM inflection points in twelve months - simonwillison.net</a></li>
<li><a href="https://injazai.com/en/news/llm-inflection-points-opus-fable">Three LLM inflection points in 12 months: from Opus 4.5 to ...</a></li>
<li><a href="https://injazai.com/en/news/llm-inflection-points-opus-fable">Three LLM inflection points in 12 months: from Opus 4.5 to ...</a></li>
<li><a href="https://www.learn.telusko.com/newsletter/three-llm-leaps-reliable-coding-agents-fable-class-initiative-and-3d-game-design">Three LLM leaps: Reliable coding agents, Fable-class ...</a></li>

</ul>
</details>

**Tags**: `#LLMs`, `#coding agents`, `#AI engineering`, `#software development`

---

<a id="item-tech-news-8"></a>
### [Microsoft declares “Code Red” overhaul after historic Microsoft 365 outage](https://arstechnica.com/gadgets/2026/11/microsofts-historic-cloud-outage-exposed-an-engineering-fog-of-war/) ⭐️ 7.0/10

Microsoft is overhauling its engineering practices after the November 12 disruption disrupted Exchange Online, Teams, and Outlook worldwide—the largest customer impact in Exchange Online’s history. Microsoft attributed the outage to an undetected Windows scalability defect that caused lock contention, compounded by a Teams failover and nearly 14 percent of gateway capacity being offline for maintenance. An urgent production fix took five to six days to deploy globally, far exceeding the company’s one-hour target.

rss · Ars Technica · Nov 24, 22:36

**Tags**: `#cloud reliability`, `#Microsoft 365`, `#incident response`, `#scalability`, `#deployment engineering`

---

<a id="item-tech-news-9"></a>
### [Tidal Bans Fully AI-Generated Music and Deletes 27 Million Tracks](https://arstechnica.com/ai/2026/11/tidal-will-ban-fully-ai-generated-music-on-december-9/) ⭐️ 7.0/10

Tidal announced that it will delete all 27 million fully AI-generated tracks in its catalog on December 9, escalating its July 2026 policy of labeling and demonetizing such music to an outright ban. The company said fully AI-generated uploads represented 43% of new uploads over the preceding 90 days and reached 60% on November 6. It estimated the removals would have essentially no negative business impact because 96% of AI-labeled tracks received zero plays during the prior 90 days. Tidal will continue accepting AI-assisted songs that contain human elements, while it said it had already removed about 66,000 tracks for impersonating artists.

rss · Ars Technica · Nov 24, 17:34

**「Background」** Streaming services have generally labeled AI-generated music rather than prohibited it, and Tidal initially introduced labels and demonetization for entirely AI-created songs in July 2026. The policy change responds to concerns that high-volume AI uploads can flood the catalog, mislead listeners, and divert royalties from human creators, including through artist impersonation.

**「Impact」** Listeners will lose access to 27 million AI-labeled songs, representing 6.3% of Tidal’s catalog, on December 9, while songs using AI assistance remain eligible if they include human-created elements.

**Tags**: `#generative AI`, `#music streaming`, `#AI policy`, `#copyright`, `#Tidal`

---

<a id="item-tech-news-10"></a>
### [Nvidia Reinstates Jensen Huang After Political Pressure](https://arstechnica.com/tech-policy/2026/11/how-trump-and-silicon-valley-forced-nvidia-to-take-jensen-huang-back/) ⭐️ 7.0/10

Nvidia abruptly reinstated founder and CEO Jensen Huang less than two weeks after his resignation, following reported affairs with a customer suspected of being a Chinese spy and with a subordinate. The board’s reversal followed pressure from President Donald Trump over the weekend and lobbying by Huang’s Silicon Valley allies, some of whom involved Trump and Vice President JD Vance. Huang returned to applause at Nvidia’s Santa Clara headquarters, and the company gained nearly $1 trillion in market value on the news. Nvidia nevertheless remains worth about one-fifth less than it was a month ago and faces FBI and SEC probes, congressional investigations, governance concerns, and questions about alleged chip-smuggling links to a suspected Chinese spy.

rss · Ars Technica · Nov 24, 14:56

**「Nvidia’s role in the AI boom」** Nvidia evolved from a video-game chip designer into a dominant supplier of AI processors, with Jensen Huang central to the company’s rise during the artificial-intelligence boom. His leadership has therefore become closely tied to Nvidia’s market position and the United States’ effort to maintain its lead over China in AI.

**「AI-chip market impact」** For Nvidia’s customers and the broader AI-chip ecosystem, Huang’s reinstatement reduced near-term leadership uncertainty, while the company’s shares rebounded 31% after falling 23% in the week following his exit.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theguardian.com/technology/2026/nov/23/jensen-huang-reinstated-as-nvidia-chief-executive">Jensen Huang reinstated as Nvidia CEO after Trump ... | The Guardian</a></li>
<li><a href="https://www.ft.com/content/20d2ebe3-e945-4659-a122-31bf85a4e4e5?syn-25a6b1a6=1">Jensen Huang ’s return as it happened: Nvidia gains nearly $1tn in...</a></li>
<li><a href="https://www.cnbc.com/2026/11/23/nvidia-jensen-huang-ceo.html">Jensen Huang reinstated as Nvidia CEO. Stock skyrockets 31%</a></li>
<li><a href="https://www.hindustantimes.com/ht-explainers/jensen-huang-returns-nvidia-ceo-trump-ai-bubble-stock-market-crash-101795499680720.html">Jensen Huang returns as Nvidia CEO: Did Trump save the &#x27;AI ...</a></li>

</ul>
</details>

**Tags**: `#Nvidia`, `#Jensen Huang`, `#AI chips`, `#tech policy`, `#corporate governance`

---

<a id="item-tech-news-11"></a>
### [Oil and Chemical Shipping Vessels Reportedly Targeted in Cyberattacks](https://techcrunch.com/2026/11/24/dozens-of-oil-and-shipping-tankers-hacked-in-recent-weeks-per-report/) ⭐️ 7.0/10

Dozens of oil and chemical shipping vessels were reportedly targeted in cyberattacks during recent weeks, with Iran identified as the chief suspect. The supplied report provides no details about the vessels, intrusion methods, affected operators, or operational consequences. If confirmed and coordinated, the reported campaign could have implications for maritime critical infrastructure and regional security, but the available evidence does not establish the extent or impact of the attacks.

rss · TechCrunch · Nov 24, 21:09

**「Context」** The reported cyberattacks target commercial oil and chemical tankers, whose disruption can affect energy supplies and shipping logistics. The allegations emerged amid heightened U.S.-Iran tensions over the Strait of Hormuz and alongside separate reports that three tankers struck naval mines, although the available material provides no technical details about how the alleged cyberattacks were carried out.

**「Maritime and energy supply risk」** Affected operators may need to coordinate breach mitigation with authorities, as two US-bound oil tankers reportedly sought FBI and Coast Guard assistance, including one carrying nearly 2.3 million barrels. If the suspected campaign reaches as many as 50 commercial vessels, it could increase security risks for global maritime trade and energy supplies, although the scale and alleged Iranian role remain under investigation.

<details><summary>References</summary>
<ul>
<li><a href="https://www.youtube.com/watch?v=93kTFBPDQGM">NEW: US probes possible Iran CYBERATTACKS targeting dozens of ...</a></li>
<li><a href="https://www.cnbc.com/2026/11/24/iran-trump-hormuz-crude-.html">Iran says three tankers hit mines in Hormuz despite U.S. escort</a></li>
<li><a href="https://www.yahoo.com/news/world/articles/iran-vows-end-u-naval-113037780.html">Iran vows to end U.S. naval blockade by &quot;all available means&quot;</a></li>
<li><a href="https://gulfnews.com/world/mena/cyber-threats-targeting-50-ships-spark-fears-of-escalating-us-iran-conflict-in-maritime-trade-1.500758663">Cyberattacks on 50 Ships Raise Alarms Over US-Iran Maritime ...</a></li>
<li><a href="https://cybernews.com/news/iran-oil-tanker-cyberattack-fbi-texas/">Tanker cyberattack hits two US-bound oil ships, Iran link ...</a></li>
<li><a href="https://www.ibtimes.com/us-investigates-cyberattacks-commercial-ships-3810121">US Probes Iran’s Possible Role In Cyberattacks On Up To 50 ...</a></li>

</ul>
</details>

**Tags**: `#cybersecurity`, `#maritime security`, `#critical infrastructure`, `#Iran`

---

<a id="item-tech-news-12"></a>
### [Amazon’s Decart Deal Targets Trainium Software Performance](https://techcrunch.com/2026/11/24/amazons-decart-acquisition-is-a-bet-on-using-software-to-narrow-the-gap-with-nvidia-in-the-ai-chip-race/) ⭐️ 7.0/10

Amazon has reportedly agreed to acquire Decart for $7.5 billion as part of an effort to improve the efficiency of its Trainium AI chips. The strategic rationale is that better software optimization could narrow the performance gap between Amazon’s accelerators and Nvidia’s hardware, making Trainium more competitive in the AI-chip market. The supplied report does not specify which Decart products or techniques Amazon plans to integrate, how the acquisition will affect Trainium performance, or whether any benchmarks are available. The reported price and broader technical implications therefore remain subject to additional detail and corroboration.

rss · TechCrunch · Nov 24, 15:51

**「Background」** Trainium is Amazon’s proprietary AI accelerator line, while Decart develops the Decart Optimization Stack \(DOS\), a software layer designed to run AI workloads efficiently across different accelerators, including Nvidia GPUs, Google TPUs, and Trainium. Reports indicated that Amazon was in talks to acquire Decart for around $7 billion, although a completed deal and final valuation had not been confirmed.

**「Trainium competitiveness」** Amazon’s reported $7.5 billion acquisition of Decart could improve Trainium’s inference efficiency and strengthen Amazon’s ability to sell its AI chips to external customers as a lower-cost Nvidia alternative, although the resulting performance and cost gains have not been quantified.

<details><summary>References</summary>
<ul>
<li><a href="https://www.agenticbrew.ai/news/e6c7ea0d-0de0-4648-8f9c-a1264143a131/amazon-in-talks-to-acquire-decart-for-7b">Amazon in talks to acquire Decart for ~$ 7 B — AI News | Agentic Brew</a></li>
<li><a href="https://www.earlybird.email/p/amazon-in-talks-to-buy-ai-startup-decart-for-about-7-billion">Amazon in Talks to Buy AI Startup Decart for About $ 7 Billion</a></li>
<li><a href="https://wirandhika.my.id/en/amazon-decart-7-billion-acquisition-talks/">Amazon Eyes $ 7 B Decart Acquisition | WiraNews</a></li>
<li><a href="https://techcrunch.com/2026/11/24/amazons-decart-acquisition-is-a-bet-on-using-software-to-narrow-the-gap-with-nvidia-in-the-ai-chip-race/">Amazon &#x27;s Decart acquisition is a bet on using software to narrow the...</a></li>
<li><a href="https://techcrunch.com/2026/11/23/amazon-snaps-up-decarts-ai-optimization-tech-for-7-5b-as-it-prepares-to-sell-trainium-chips/">Amazon snaps up Decart &#x27;s AI optimization tech for... | TechCrunch</a></li>
<li><a href="https://www.aboutamazon.com/news/company-news/amazon-decart-ai-optimization">Amazon to purchase Decart &#x27;s AI optimization technology</a></li>

</ul>
</details>

**Tags**: `#AI accelerators`, `#Amazon Trainium`, `#Decart acquisition`, `#chip optimization`, `#Nvidia competition`

---

<a id="item-tech-news-13"></a>
### [CrowdStrike’s reported $44B Zscaler acquisition raises integration and pricing concerns](https://www.theregister.com/security/2026/11/24/crowdstrike-splashes-44b-on-zscaler-customers-brace-for-the-bill/5311877) ⭐️ 7.0/10

CrowdStrike’s reported $44 billion acquisition of Zscaler promises tighter product integration but could give customers a broader security platform. Administrators fear that greater vendor consolidation could lead to higher prices and increased vendor lock-in, reducing their leverage over contract terms. The supplied report provides little detail about financing, compatibility, product-roadmap changes, or existing customer contracts, so the practical effects remain uncertain.

rss · The Register · Nov 24, 12:22

**「Background」** CrowdStrike has agreed to acquire network security provider Zscaler in an all-stock transaction valued at about $43.9 billion, with completion expected in the second half of CrowdStrike’s fiscal year 2028. The consolidation reflects growing cybersecurity concerns as advances in artificial intelligence increase fears of sophisticated attacks.

**「Impact」** If completed, CrowdStrike&\#x27;s $43.9 billion Zscaler acquisition could place endpoint and network security under one vendor and enable cross-selling to roughly 8,000 Zscaler customers, prompting concerns about higher renewal prices and increased vendor lock-in.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/11/23/crowdstrike-zscaler-aquisition-ai-cyberattacks.html">CrowdStrike to buy Zscaler in $ 44 B deal as AI supercharges...</a></li>
<li><a href="https://www.nytimes.com/2026/11/23/business/crowdstrike-zscaler-cybersecurity.html">Two Major Cybersecurity Firms to Combine in $ 44 Billion Deal</a></li>
<li><a href="https://www.bloomberg.com/news/articles/2026-11-23/crowdstrike-reaches-44-billion-cybersecurity-deal-for-zscaler">CrowdStrike Reaches $ 44 Billion Cyber Deal for Zscaler - Bloomberg</a></li>
<li><a href="https://www.forbes.com/sites/stevemcdowell/2026/11/23/what-crowdstrikes-439-billion-zscaler-acquisition-means-for-buyers/">What CrowdStrike’s $43.9 Billion Zscaler Acquisition Means ...</a></li>
<li><a href="https://www.theregister.com/security/2026/11/24/crowdstrike-splashes-44b-on-zscaler-customers-brace-for-the-bill/5311877">CrowdStrike splashes $44B on Zscaler, customers brace for the ...</a></li>
<li><a href="https://www.zscaler.com/press/crowdstrike-acquire-zscaler-bringing-network-security-and-zero-trust-falcon-platform">CrowdStrike to Acquire Zscaler for Zero Trust</a></li>

</ul>
</details>

**Tags**: `#cybersecurity`, `#acquisitions`, `#CrowdStrike`, `#Zscaler`, `#vendor lock-in`

---

<a id="item-tech-news-14"></a>
### [Microduck Obstacle Avoidance with Isaac Lab and Newton](https://huggingface.co/blog/nvidia/microduck-obstacle-avoidance) ⭐️ 6.0/10

This NVIDIA workflow adds local obstacle avoidance to Microduck while keeping its previously trained walking-policy weights fixed. In Isaac Lab, a navigation policy uses ToF history and body and controller state available on the real robot at 50 Hz to adjust gamepad-derived forward, lateral, and yaw velocity commands, which the frozen walking policy converts into joint actions; the critic’s additional simulation state is not required on hardware. Newton’s MicroDuckToFCamera models the VL53L5CX as an 8×8, 15 Hz sensor with a 45° field of view and 0.12–4 m range, while training varies mount pose and adds noise, delays, floor-reading offsets, and missing measurements near grid edges. The task samples obstacle layouts from primitives and pinned SimReady assets, then trains with PPO across 16,384 parallel environments for 1,500 iterations; a smaller NVIDIA DGX Spark run used 4,096 environments and 3,000 updates for approximately six hours, though fewer environments can mean more iterations and longer training. The tutorial also covers evaluation, ONNX export, and preparation for physical-robot testing with a supported ToF sensor, paired gamepad, and compatible Linux and NVIDIA setup.

rss · Hugging Face Blog · Nov 24, 16:34

**「Background」** Microduck’s earlier sim-to-real workflow trained and exported a walking policy for deployment on the physical biped; this follow-up treats that policy as fixed and adds a separate navigation layer. Isaac Lab provides the GPU-parallel reinforcement-learning environment, while Newton supplies physics and time-of-flight raycasting, allowing the navigation controller to use ToF observations to modify forward, lateral, and yaw velocity commands before the walking policy converts them into joint actions.

**「Impact」** The workflow enables Microduck developers to add local ToF-based obstacle avoidance without retraining the walking policy, using a separately trained Isaac Lab/Newton controller to adjust gamepad velocity commands for real-robot deployment.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/blog/nvidia/microduck-obstacle-avoidance">Microduck Obstacle Avoidance: A Sim2Real Workflow with Isaac ...</a></li>
<li><a href="https://huggingface.co/blog/nvidia/microduck-isaac-lab-sim-to-real">Train in Simulation, Deploy on a Real Robot: Microduck with ...</a></li>
<li><a href="https://developer.nvidia.com/blog/using-ai-agents-to-teach-robots-like-microduck-to-walk-in-simulation/">Using AI Agents to Teach Robots Like Microduck to Walk in ...</a></li>
<li><a href="https://huggingface.co/blog/nvidia/microduck-obstacle-avoidance">Microduck Obstacle Avoidance: A Sim2Real Workflow with Isaac ...</a></li>

</ul>
</details>

**Tags**: `#sim-to-real robotics`, `#obstacle avoidance`, `#NVIDIA Isaac Lab`, `#Newton physics simulation`, `#time-of-flight sensing`

---

<a id="item-tech-news-15"></a>
### [Astra and Codex Assist Amateur Exoplanet Searches](https://openai.com/index/searching-for-distant-planets-with-astra) ⭐️ 6.0/10

OpenAI reports ... . Bond&\#x27;s ... . Byrd&\#x27;s ... . The searches demonstrate ... but ... .

rss · OpenAI News · Nov 24, 11:00

**「Exoplanet Detection Basics」** Exoplanets can be detected by the transit method: when a planet crosses its star from Earth’s perspective, it blocks a small fraction of the starlight and creates a repeating dip in a light curve. Because eclipses between stars and changes in telescope instruments can mimic this pattern, candidates require statistical checks and additional observations, sometimes using radial-velocity measurements, before peer-reviewed confirmation. Astronomers have used AI in this work since at least 2017, when a neural network trained on 15,000 vetted Kepler signals helped identify an eighth planet around Kepler-90, building on a longer tradition of amateur astronomers analyzing public telescope data.

**「Impact」** Codex and Astra let amateur astronomers turn public Kepler and TESS data into prioritized exoplanet candidates that professional teams can validate and observe, strengthening the role of volunteers who do not own telescopes. The candidates are not confirmed planets, so independent follow-up remains necessary.

<details><summary>References</summary>
<ul>
<li><a href="https://finance.biggo.com/news/d50c1970-7f1a-46e8-badb-f4440a154883">Two Amateur Astronomers Use AI to Flag New Exoplanet ...</a></li>
<li><a href="https://openai.com/index/searching-for-distant-planets-with-astra/">Searching for distant planets with Astra | OpenAI</a></li>
<li><a href="https://science.nasa.gov/exoplanets/citizen-science/">Citizen Science - NASA Science</a></li>
<li><a href="https://github.com/nasa/ExoMiner">GitHub - nasa/ExoMiner: Automating the vetting and validation of...</a></li>

</ul>
</details>

**Tags**: `#AI for science`, `#exoplanet detection`, `#astronomy`, `#Codex`, `#Astra`

---

<a id="item-tech-news-16"></a>
### [ByteDance Open-Sources Laminar for Async RL Post-Training](https://news.google.com/rss/articles/CBMinAFBVV95cUxOREtoZmNWcnFoV0VTT2trNlBya2JEZllsaUFSYVgwcm9sMk5iZUJtR1FIVjJtRXhCaUh5ZjdFbE1SZFBzbC1yalZ2Y2dpMjY3X3ZOTTJhcG5fanJmTWZaQmptc3dEV3JtcGl5NExCeFh2QXVEVHZhSDczM0lBbERUeVliQzc3a0Utekx4ME0zUlJNckloYWtjTzZxUHjSAZwBQVVfeXFMTkRLaGZjVnJxaFdFU09razZQcmtiRGZZbGlBUmFYMHJvbDJOYmVCbUdRSFYybUV4QmlIeWY3RWxNUmRQc2wtcmpWdmNnaTI2N192Tk0yYXBuX2pyZk1mWkJqbXN3RFdybXBpeTRMQnhYdkF1RFR2YUg3MzNJQWxEVHlZYkM3N2tFLXpMeDBNM1JSTXJJaGFrY082cVB4?oc=5) ⭐️ 6.0/10

ByteDance researchers have reportedly open-sourced Laminar, an asynchronous reinforcement-learning framework designed for AI post-training. The project is presented as an open-source option for teams working with reinforcement-learning-based model training and post-training workflows. The supplied report does not specify Laminar&\#x27;s architecture, supported models or environments, benchmarks, license, repository location, hardware requirements, or adoption status, so its technical capabilities and practical impact cannot yet be assessed.

google\_news · MarkTechPost · Nov 25, 05:42

**「Asynchronous RL Post-Training」** Reinforcement-learning post-training uses generated trajectories to improve an existing model, while synchronized systems can tie trajectory generation to global parameter updates, creating a lockstep bottleneck. Laminar is ByteDance researchers’ proposed response: a fully decoupled, trajectory-level asynchronous system in which each trajectory is generated and consumed independently, while relay workers act as a distributed parameter service in place of global updates. The work was first posted to arXiv on October 14, 2025, and later listed as an ACM publication on April 26, 2026.

**「Practical impact」** Open-sourcing Laminar gives AI and machine-learning practitioners access to ByteDance&\#x27;s asynchronous reinforcement-learning tooling for model post-training. However, the supplied announcement provides no repository, license, compatibility details, benchmarks, or adoption evidence, so its practical advantage and production readiness cannot yet be established.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2510.12633">[2510.12633] Laminar: A Scalable Asynchronous RL Post ...</a></li>
<li><a href="https://arxiv.org/pdf/2510.12633">Laminar: A Scalable Asynchronous RL Post-Training Framework</a></li>
<li><a href="https://dl.acm.org/doi/10.1145/3767295.3803580">Laminar: A Scalable Asynchronous RL Post-Training Framework</a></li>

</ul>
</details>

**Tags**: `#reinforcement-learning`, `#AI-post-training`, `#open-source`, `#AI-frameworks`

---