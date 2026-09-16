---
layout: default
title: "Horizon Summary: 2026-09-16 (EN)"
date: 2026-09-16
lang: en
---

> From 125 items, 14 important content pieces were selected

---

**Technology News**
1. [Mozilla: Open Chinese AI Models Trail US Frontier by 4 Months at One-Third Cost](#item-tech-news-1) ⭐️ 8.0/10
2. [Cisco email security flaw allows root access via email](#item-tech-news-2) ⭐️ 8.0/10
3. [Typesafe.ai launches Jev for fast typed inference](#item-tech-news-3) ⭐️ 7.0/10
4. [Wayback Machine Faces Access Restrictions Amid Scraper Abuse](#item-tech-news-4) ⭐️ 7.0/10
5. [Google Releases Gemini 3.8 Live and 3.8 Live Extended Thinking](#item-tech-news-5) ⭐️ 7.0/10
6. [SemiAnalysis: Datacenter Moratoriums Less Constraining Than Claimed](#item-tech-news-6) ⭐️ 7.0/10
7. [SpaceX sets Starship orbital flight attempt for September 22](#item-tech-news-7) ⭐️ 7.0/10
8. [US Air Force confirms deployment of space control weapons in orbit](#item-tech-news-8) ⭐️ 7.0/10
9. [US data centers projected to outpace Germany and Japan in natural gas use by 2035](#item-tech-news-9) ⭐️ 7.0/10
10. [OpenAI, Anthropic, Google DeepMind hold weeks of AI safety talks](#item-tech-news-10) ⭐️ 7.0/10
11. [America is building datacenters faster than the grid can power them](#item-tech-news-11) ⭐️ 7.0/10
12. [PostgreSQL 19 graph queries fail the &\#x27;would you ship this?&\#x27; test](#item-tech-news-12) ⭐️ 7.0/10
13. [IBM Research Adds Consistency-Aware Evaluation to ALTK-Evolve](#item-tech-news-13) ⭐️ 7.0/10

**Financial News**
1. [China&\#x27;s August retail sales miss forecast as investment slump deepens](#item-finance-news-1) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Mozilla: Open Chinese AI Models Trail US Frontier by 4 Months at One-Third Cost](https://arstechnica.com/ai/2026/09/exclusive-open-chinese-models-close-gap-with-silicon-valleys-frontier-ai-models/) ⭐️ 8.0/10

Mozilla&\#x27;s State of Open Source AI report, published on September 15 and shared with Ars Technica ahead of publication, finds the performance gap between leading US closed frontier AI models and the best Chinese open-weights models has narrowed to just 4.4 months. The report highlights that Moonshot AI&\#x27;s Kimi K3 scores only three points behind Anthropic&\#x27;s Fable 5 on the Artificial Analysis Intelligence Index while costing roughly 30 percent as much, using that composite benchmark as its primary comparison. Mozilla CTO Raffi Krikorian recommends that most organizations default to open models for the bulk of their work, arguing that the decision to pay for closed frontier models should be workload-specific rather than organization-specific. Closed models still earn their premium in three narrow areas—expert professional work, high-intensity retrieval, and long context—according to Krikorian, while organizations also pay extra for &quot;compliance packaging, support, and accountability&quot; that closed providers bundle in, a tradeoff many lack the internal staff to replicate with open-weights models.

rss · Ars Technica · Sep 15, 12:00

**「Background」** Open-weights AI models let anyone download the main model components and run them on their own hardware, but developers typically still withhold training data, data pipeline details, and training code, leaving the models partially opaque. By contrast, US companies such as Anthropic and OpenAI predominantly offer closed frontier models that keep weights and training details proprietary and charge customers for API access. The Artificial Analysis Intelligence Index is a composite benchmark that combines multiple evaluations to produce a single performance score, which Mozilla used as the basis for its head-to-head comparison.

**「Impact」** Organizations making AI procurement and architecture decisions now have quantitative evidence from Mozilla to default to open-weights models for routine workloads and reserve paid closed frontier access for the specific use cases of expert professional work, high-intensity retrieval, and long-context tasks.

**Tags**: `#ai`, `#open-source`, `#machine-learning`, `#industry-analysis`, `#ai-economics`

---

<a id="item-tech-news-2"></a>
### [Cisco email security flaw allows root access via email](https://www.theregister.com/security/2026/09/15/cisco-email-security-boxes-can-be-rooted-by-an-email/5296604) ⭐️ 8.0/10

A critical vulnerability in Cisco email security appliances lets attackers obtain root-level access on the devices simply by sending an email, according to a report from The Register. Cisco has confirmed that the flaw is already being actively exploited in the wild, raising the severity beyond a theoretical risk. The vendor is additionally warning that, once inside, attackers may be able to cover their tracks by erasing forensic traces, which complicates incident response and post-breach analysis. Organizations running affected Cisco email security appliances should treat this as an urgent patching priority and review their detection and logging capabilities given the potential for evidence tampering.

rss · The Register · Sep 15, 16:01

**「Background」** Cisco Secure Email Gateway \(formerly known as Cisco Email Security Appliance, or ESA\) is an on-premises email security product that runs Cisco&\#x27;s AsyncOS software to filter spam, malware, and other threats at the network perimeter for organizations. The vulnerability at issue, CVE-2026-76461, is an SQL injection flaw in the appliance&\#x27;s email parsing logic carrying a CVSS v3.1 base score of 9.8, and it was disclosed by Cisco on September 14, 2026 with confirmation of active in-the-wild exploitation. Because the flaw lets an unauthenticated remote attacker send a single crafted email to obtain root-level command execution on the appliance, it sits in the same family of perimeter-device weaknesses that have historically made email and web gateways high-value targets for attackers.

**「Impact」** Organizations running Cisco Secure Email Gateway \(formerly ESA\), Secure Email Cloud Gateway, or Secure Email Essentials face an immediate, actively exploited remote root compromise that can be triggered simply by sending an email, with CISA adding CVE-2026-76461 to the Known Exploited Vulnerabilities catalog with a remediation deadline of September 17, 2026. Compounding the risk, Cisco warns attackers may be able to erase forensic traces once inside, making intrusion detection and post-incident response materially harder for affected security teams.

<details><summary>References</summary>
<ul>
<li><a href="https://sec.cloudapps.cisco.com/security/center/content/CiscoSecurityAdvisory/cisco-sa-esa-inj-2bLVGmhX">Cisco Secure Email Gateway SQL Injection Vulnerability</a></li>
<li><a href="https://www.rapid7.com/blog/post/etr-cve-2026-76461-critical-cisco-secure-email-gateway-vulnerability-exploited-in-the-wild/">CVE-2026-76461: Critical Cisco Secure Email Gateway ... - Rapid7</a></li>
<li><a href="https://www.sophos.com/en-us/blog/cisco-secure-email-gateway-vulnerability-cve-2026-76461-in-active-exploitation">Cisco Secure Email Gateway vulnerability (CVE-2026 ... - Sophos</a></li>
<li><a href="https://zerohour.day/item/9362e6e89c5f54762679a22f8c0cb73761828ab7">Cisco Secure Email Gateway Vulnerability Exploited in Attacks...</a></li>
<li><a href="https://beazley.security/alerts-advisories/critical-vulnerability-in-cisco-secure-email-gateway-under-active-exploitation">Critical Vulnerability in Cisco Secure Email Gateway Under Active...</a></li>
<li><a href="https://www.rapid7.com/blog/post/etr-cve-2026-76461-critical-cisco-secure-email-gateway-vulnerability-exploited-in-the-wild/">CVE -2026-76461: Critical Cisco Secure Email Gateway Vulnerability ...</a></li>

</ul>
</details>

**Tags**: `#security`, `#vulnerability`, `#cisco`, `#email-security`, `#active-exploitation`

---

<a id="item-tech-news-3"></a>
### [Typesafe.ai launches Jev for fast typed inference](https://typesafe.ai/blog/introducing-system-one-models-and-jev) ⭐️ 7.0/10

Typesafe.ai has launched Jev, a model architecture purpose-built for fast, low-cost typed inference rather than general text generation. Jev takes arbitrary text input together with structured questions \(yes/no, multiple-choice, or numeric score\) and returns answers in milliseconds at a listed price of $0.042 per million tokens. The system targets classification, extraction, and scoring workloads where developers need reliable structured outputs with predictable latency. By trading the flexibility of generative models for speed and type safety, Jev is positioned for pipelines where conventional LLMs are overpowered and overpriced.

hackernews · albelfio · Sep 15, 19:25 · [Discussion](https://news.ycombinator.com/item?id=49717558)

**「Background」** Large language models typically generate free-form text one token at a time, so producing machine-usable values \(booleans, enums, scores, JSON objects\) usually requires constrained decoding or post-hoc parsing and can still produce type errors. &\#x27;Typed inference&\#x27; or &\#x27;structured output&\#x27; refers to models whose possible responses are defined in advance as a fixed schema, so the model returns values—and often associated probabilities—that downstream software can consume directly without parsing ambiguity. The &\#x27;System One&\#x27; label borrows from Daniel Kahneman&\#x27;s dual-process theory of cognition, where System 1 denotes fast, automatic processing in contrast to the slower, deliberative step-by-step generation of general-purpose LLMs.

**「Impact」** Developers building classification, extraction, and scoring pipelines can potentially replace slower, more expensive general-purpose LLM calls with millisecond-latency typed inference at $0.042/MTok, accepting the loss of free-form generation as the tradeoff.

**「Community discussion」** Commenters generally view Jev as a promising and differentiated idea, noting that the documentation explains the concept more clearly than the launch announcement itself. Discussion centers on whether direct speed comparisons against generative models are fair, excitement about combining Jev with design-by-contract patterns in Python, and curiosity about real-world demos such as a home-assistant integration.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.typesafe.ai/concepts/system-one">System One - TypeSafe AI</a></li>
<li><a href="https://typesafe.ai/blog/introducing-system-one-models-and-jev">Introducing System One Models &amp; Jev - TypeSafe AI Blog</a></li>

</ul>
</details>

**Tags**: `#ai`, `#llm-inference`, `#structured-output`, `#machine-learning`, `#product-launch`

---

<a id="item-tech-news-4"></a>
### [Wayback Machine Faces Access Restrictions Amid Scraper Abuse](https://blog.archive.org/2026/09/15/an-update-on-wayback-machine-access/) ⭐️ 7.0/10

The Internet Archive has implemented protective access restrictions on the Wayback Machine after waves of high-volume automated traffic overwhelmed the service, which the organization attributes to scrapers using archived copies to bypass blocks on original sites. Commenters familiar with the situation describe the behavior as a workaround: when a site blocks scraping, automated systems instead retrieve the same content from the Internet Archive&\#x27;s cached pages, shifting the load onto the non-profit preservation service. As a result, the Wayback Machine is returning rate-limit responses such as HTTP 429 to users, and some site owners have begun opting their content out of archiving altogether. The episode has renewed debate about the sustainability of open web preservation infrastructure when faced with abusive bulk-access patterns.

hackernews · ChrisArchitect · Sep 15, 17:52 · [Discussion](https://news.ycombinator.com/item?id=49716176)

**「Background」** The Wayback Machine, operated by the non-profit Internet Archive, preserves snapshots of web pages and serves them to anyone who wants to see historical versions of sites. Because its copies are publicly accessible, automated scrapers that are blocked by an original site can sometimes fetch the same content from an archived snapshot instead, effectively using the Archive as a bypass for site-level access controls. The Internet Archive has long been funded largely by donations and grants while offering free, anonymous access to its holdings.

**「Impact」** Legitimate users of the Wayback Machine, including researchers and casual visitors, are encountering rate-limit errors that restrict how much they can access, and some originating sites are choosing to opt out of archiving in response to the redirected scraping traffic.

**「Community Discussion」** Commenters broadly express support for the Internet Archive and frame the scrapers&\#x27; behavior as abusive and short-sighted, with several calling for donations to help sustain the service. Some users report inconsistent access \(such as HTTP 429 errors from work machines but not personal devices\), while others suggest voluntary paid tiers or higher donation-based rate limits as a way to fund capacity without abandoning the open-access model.

**Tags**: `#Internet Archive`, `#Web Infrastructure`, `#Scraping`, `#Digital Preservation`, `#Open Web`

---

<a id="item-tech-news-5"></a>
### [Google Releases Gemini 3.8 Live and 3.8 Live Extended Thinking](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-8-live-gemini-3-8-live-extended-thinking/) ⭐️ 7.0/10

Google announced Gemini 3.8 Live and Gemini 3.8 Live Extended Thinking, two new models aimed at powering near real-time voice agents and more intuitive voice interactions. Gemini 3.8 Live is positioned for scale and cost efficiency, combining conversational intelligence with fluid dialogue and visual grounding, while Gemini 3.8 Live Extended Thinking is targeted at high-complexity tasks with increased reasoning capability. The release extends Google&\#x27;s Gemini family with a dedicated live voice modality and an explicit reasoning mode, available to consumers and, according to early testers, supported on Google Workspace accounts that previously lacked access. Practitioner reports cited in the discussion highlight strong multilingual voice quality \(including for lower-resource languages such as Afrikaans\), low latency, and tolerance of thick accents, though the accompanying demo video was criticized for showing the model falling to a basic chess checkmate pattern.

hackernews · leumon · Sep 15, 17:38 · [Discussion](https://news.ycombinator.com/item?id=49715947)

**「Background」** Google previously launched Gemini 3.1 Flash Live in March as its earlier generation of real-time voice conversational models, and more recently expanded the Gemini Audio family with Gemini 3.5 Transcribe for transcription tasks. Gemini 3.8 Live and 3.8 Live Extended Thinking are described as native speech-to-speech models built specifically for real-time voice agents that need to reason and invoke tools mid-conversation without breaking the dialogue flow. The release is positioned as Google&\#x27;s most advanced live dialogue lineup to date, targeting production-grade voice agent use cases across Workspace, Search, and the Gemini app.

**「Impact」** For Google Workspace users, the release restores live voice access on accounts that were previously unsupported, broadening who can use Gemini&\#x27;s live mode for everyday work and personal tasks. The model&\#x27;s apparent weakness on a common chess pattern in the launch demo, however, signals that the Extended Thinking mode should be evaluated carefully on structured reasoning tasks before being relied upon for high-stakes applications.

**「Community Discussion」** Early testers on Hacker News were broadly positive, praising the model&\#x27;s accent handling, pleasant voices, and workspace account support, with one Afrikaans speaker calling the multilingual voice quality the most enjoyable LLM use case they had encountered. Several commenters expressed skepticism about Google&\#x27;s competitive position relative to peers like Fable and Astra despite Google&\#x27;s data, TPU, and advertising advantages, and one user sharply criticized the launch video in which the model lost to a basic chess checkmate pattern.

<details><summary>References</summary>
<ul>
<li><a href="https://9to5google.com/2026/09/15/gemini-3-8-live-announced/">Gemini 3.8 Live Extended Thinking powers Gemini Live, Gmail</a></li>
<li><a href="https://www.marktechpost.com/2026/09/15/google-releases-gemini-3-8-live-and-3-8-live-extended-thinking-for-production-grade-voice-agents/">Google Releases Gemini 3.8 Live and 3.8 Live Extended Thinking for ...</a></li>

</ul>
</details>

**Tags**: `#AI`, `#LLMs`, `#Google`, `#voice-AI`, `#model-release`

---

<a id="item-tech-news-6"></a>
### [SemiAnalysis: Datacenter Moratoriums Less Constraining Than Claimed](https://newsletter.semianalysis.com/p/everyone-says-datacenter-moratoriums) ⭐️ 7.0/10

SemiAnalysis published an analysis arguing that datacenter moratoriums are a less significant constraint on US AI infrastructure buildout than commonly claimed, with author Maya Barkin citing specific capacity figures to challenge prevailing narratives. The piece highlights that while 20GW of datacenter capacity sits within restricted local boundaries, only 1,525MW actually slips, and just 2.3GW is affected nationwide including New York. This framing suggests that headline fears about moratoriums stalling US datacenter expansion may overstate the practical impact on near-term capacity. Because only a teaser snippet of the analysis is available, the full quantitative methodology, underlying assumptions, and time horizon behind the 20GW, 1,525MW, and 2.3GW figures cannot be verified from the supplied content.

rss · Semianalysis · Sep 15, 20:54

**「Background」** Datacenter moratoriums are local or state-level pauses or bans on new datacenter construction, typically enacted in response to community backlash over energy use, water consumption, and rising electricity costs. The conventional framing focuses on the raw count of restrictions, but understanding SemiAnalysis&\#x27;s contrarian argument requires distinguishing nominal moratoriums from the actual MW capacity they delay or block, since the two metrics diverge sharply.

**「Impact」** Even though more than 300 datacenter moratoriums have been documented across the US, SemiAnalysis quantifies the real-world drag on AI infrastructure buildout as just 2.3GW nationwide once local restrictions are filtered down to projects that actually slip, suggesting the moratorium narrative overstates the bottleneck relative to the GW-scale expansion hyperscalers are planning.

<details><summary>References</summary>
<ul>
<li><a href="https://sechub.in/view/3291756">Everyone Says Datacenter Moratoriums Are Killing the US Buildout .</a></li>
<li><a href="https://newsletter.semianalysis.com/p/everyone-says-datacenter-moratoriums">Everyone Says Datacenter Moratoriums Are Killing the US Buildout.</a></li>
<li><a href="https://builtin.com/articles/state-data-center-moratoriums">States Push Data Center Moratoriums as AI Growth Surges | Built In</a></li>
<li><a href="https://newsletter.semianalysis.com/p/everyone-says-datacenter-moratoriums">Everyone Says Datacenter Moratoriums Are Killing the US Buildout. We ...</a></li>
<li><a href="https://www.networkworld.com/article/4200222/data-center-energy-constraints-and-moratoriums-are-mounting-expect-to-see-stalled-ai-projects.html">Data center energy constraints, moratoriums forebode stalled AI ...</a></li>

</ul>
</details>

**Tags**: `#ai-infrastructure`, `#datacenters`, `#semiconductors`, `#energy`, `#policy`

---

<a id="item-tech-news-7"></a>
### [SpaceX sets Starship orbital flight attempt for September 22](https://arstechnica.com/space/2026/09/spacex-sets-launch-date-for-first-starship-orbital-flight/) ⭐️ 7.0/10

SpaceX announced a target launch date of September 22, pending regulatory approval, for the 14th Starship mission and its first attempt to reach orbit, with a liftoff time of 7:15 am local time in Texas \(12:15 UTC\) and a 75-minute window. The super heavy lift rocket will carry 26 V3 Starlink satellites into a 275 km orbit, with the upper stage seeking to complete six orbits over roughly 10 hours. The flight follows a July 24 test in which the Super Heavy booster&\#x27;s three center engines showed signs of ice clogging during the boostback burn, prompting an early cutoff and a hard splashdown in the Gulf of Mexico after only 8 of 13 planned engines reignited for the landing burn. SpaceX stated that the upcoming Super Heavy includes hardware modifications to improve engine filtering and software changes to enhance relight reliability.

rss · Ars Technica · Sep 15, 18:48

**「Background」** Starship is SpaceX&\#x27;s fully reusable, super heavy lift launch vehicle, whose development campaign began with its first integrated test flight on April 20, 2023. Reaching orbit has been a long-stated threshold for the program, distinguishing suborbital test flights from a flight profile capable of supporting operational missions such as Starlink satellite deployment at scale.

**「Impact」** A successful orbital insertion on September 22 would validate Starship as a functional heavy-lift platform for deploying next-generation V3 Starlink satellites and bring SpaceX closer to fielding a fully reusable super heavy lift rocket. Whether the booster&\#x27;s revised hardware and software resolve the July ice-clogging issue will directly determine the mission&\#x27;s reusability goals.

**Tags**: `#aerospace`, `#hardware`, `#technology-industry`, `#space-launches`

---

<a id="item-tech-news-8"></a>
### [US Air Force confirms deployment of space control weapons in orbit](https://arstechnica.com/space/2026/09/for-the-first-time-the-us-military-confirms-it-has-deployed-weapons-in-orbit/) ⭐️ 7.0/10

Air Force Secretary Troy Meink publicly confirmed for the first time that the United States has placed &quot;space control weapons&quot; in orbit, delivering the announcement in prepared remarks at the Air and Space Forces Association&\#x27;s annual Air, Space &amp; Cyber Conference near Washington, DC. &quot;Today, we continue to ensure we remain ready to meet the challenges of evolving threats, wherever they exist. This is why the United States now has on-orbit space control weapons capable of defending the joint force against hostile adversary action,&quot; Meink said, declining to disclose any technical details about the systems, including whether they have been tested. The disclosure marks a notable shift in Pentagon posture, since senior officials had previously avoided public discussion of orbital warfare; in recent years, however, military leaders have openly discussed orbital combat, satellite defensive countermeasures, and a new ground-based weapon designed to disable adversary satellites in orbit. Meink framed the silence on specifics as deliberate, telling attendees, &quot;me talking about the details of what we&\#x27;re doing would actually not benefit deterrence, so we&\#x27;re not going to talk about the specifics of what we&\#x27;re doing.&quot;

rss · Ars Technica · Sep 15, 03:47

**「Background」** US military doctrine distinguishes &\#x27;space control&\#x27; from broader &\#x27;space warfare,&\#x27; covering defensive measures and counterspace capabilities intended to protect friendly satellites while denying adversaries use of orbit, and US officials have repeatedly said they prefer counterspace weapons that do not generate debris. For decades, senior Pentagon leaders avoided publicly discussing weapons placed in orbit, though the US military has previously demonstrated a ground-based anti-satellite weapon and has more recently spoken openly about orbital combat and on-satellite defensive countermeasures. The disclosure comes as the US Space Force cites Chinese and Russian development and fielding of sophisticated counterspace systems designed to disrupt American space-enabled military capabilities.

**「Impact」** Air Force Secretary Troy Meink&\#x27;s first public confirmation that the US now has &\#x27;on-orbit space control weapons&\#x27; marks a deliberate shift in Pentagon transparency about orbital warfare capabilities, with the disclosure framed both by Meink and by outside reporting as a direct response to Chinese and Russian development of advanced space weapons.

<details><summary>References</summary>
<ul>
<li><a href="https://arstechnica.com/space/2026/09/for-the-first-time-the-us-military-confirms-it-has-deployed-weapons-in-orbit/">For the first time, the US military confirms it has deployed weapons in orbit - Ars Technica</a></li>
<li><a href="https://www.aljazeera.com/features/2026/9/15/what-are-space-weapons-which-us-says-it-has-deployed-into-orbit">What are ‘space weapons’, which US says it has deployed into orbit? | Weapons | Al Jazeera</a></li>
<li><a href="https://www.cnbc.com/2026/09/15/weapons-in-space-us-air-force-meink.html">U.S. confirms for first time it has weapons deployed in space</a></li>
<li><a href="https://www.facebook.com/cnbc/posts/the-us-said-for-the-first-time-monday-that-the-space-force-has-deployed-weapons-/1479593890708666/">The U.S. said for the first time Monday that the Space Force has deployed ...</a></li>

</ul>
</details>

**Tags**: `#space-technology`, `#defense-technology`, `#military-hardware`, `#policy`, `#geopolitics`

---

<a id="item-tech-news-9"></a>
### [US data centers projected to outpace Germany and Japan in natural gas use by 2035](https://techcrunch.com/2026/09/15/us-data-centers-could-consume-more-natural-gas-than-germany-and-japan-combined-by-2035/) ⭐️ 7.0/10

According to a TechCrunch report by Tim De Chant, the AI buildout could push U.S. data centers to become one of the largest consumers of natural gas in the world by 2035, with projected demand potentially exceeding the combined consumption of Germany and Japan. The framing positions American data centers as an energy consumer comparable to major industrial nations rather than a single industry sector, signaling a paradigm-level shift in global energy markets. The trajectory highlights the rapidly expanding energy footprint of frontier AI compute demand and its implications for infrastructure planning, grid capacity, and sustainability commitments tied to the AI sector. The available excerpt does not detail the underlying methodology, data sources, or potential mitigation strategies that could alter these projections.

rss · TechCrunch · Sep 15, 18:29

**「Background」** The explosive growth of AI workloads has made data centers one of the fastest-rising electricity demand categories in the United States, with utilities and analysts projecting that these facilities could account for roughly one-fifth of all US power consumption by 2035. Natural gas has become the preferred marginal and backup fuel for this buildout because combined-cycle plants and on-site gas turbines can be commissioned far faster than nuclear or large renewable projects, letting operators bridge multi-year grid interconnection queues. Comparing a single industry&\#x27;s projected gas burn to the combined national consumption of major industrial economies illustrates just how concentrated and unprecedented the current AI infrastructure expansion has become.

**「Impact」** Energy utilities, grid operators, AI infrastructure providers, and policymakers face the prospect of accommodating data center gas demand on par with major industrial economies, complicating emissions targets and long-term infrastructure investment decisions.

<details><summary>References</summary>
<ul>
<li><a href="https://techcrunch.com/2026/09/15/us-data-centers-could-consume-more-natural-gas-than-germany-and-japan-combined-by-2035/">US data centers could consume more natural gas than Germany and ...</a></li>
<li><a href="https://www.facebook.com/wtrf7news/posts/data-centers-to-use-15-of-us-power-by-2035-report-full-story-in-the-comments/1512159117620005/">Data centers to use 1/5 of US power by 2035: Report. Full story in the ...</a></li>

</ul>
</details>

**Tags**: `#ai-infrastructure`, `#data-centers`, `#energy-policy`, `#sustainability`, `#industry-analysis`

---

<a id="item-tech-news-10"></a>
### [OpenAI, Anthropic, Google DeepMind hold weeks of AI safety talks](https://techcrunch.com/2026/09/15/openai-anthropic-google-have-been-in-talks-on-ai-safety-for-weeks/) ⭐️ 7.0/10

OpenAI has confirmed that it has been engaged in weeks of AI safety discussions with Anthropic and Google DeepMind. The cross-competitor coordination between three of the most prominent AI labs is occurring against a backdrop of the Trump administration pushing to deprioritize safety concerns in favor of maintaining a competitive pace with China. The Trump team&\#x27;s team has dismissed safety concerns, framing AI development primarily through a US-China competitive lens. Beyond the confirmation of the ongoing talks and the geopolitical context, the source content does not specify which topics were discussed, whether any frameworks or agreements were reached, or what concrete safety measures are being coordinated.

rss · TechCrunch · Sep 15, 15:47

**「Background」** OpenAI, Anthropic, and Google DeepMind are three of the leading AI research labs developing frontier models, and despite their competitive relationship in talent, compute, and product markets, they have periodically engaged in shared discussions about AI risks and safety practices. Cross-company safety coordination has been a recurring theme in the AI industry, with executives and researchers from rival organizations occasionally calling for common standards on model evaluation, deployment, and oversight. The reported talks come amid the Trump administration&\#x27;s public stance that AI safety concerns are overstated and that US competitive advantage over China in AI should take precedence over additional regulation.

**「Impact」** Cross-competitor coordination among OpenAI, Anthropic, and Google DeepMind on AI safety—reportedly including discussions of an industry standards body and voluntary model evaluations by the US government—creates the possibility of shared safety commitments among leading labs, but directly conflicts with the Trump administration&\#x27;s push to deprioritize safety in favor of competing with China, putting the labs in tension with federal policy. Whether any binding framework emerges remains unclear given that researchers have publicly warned AI extinction risk is likely without a coordinated slowdown or regulation.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/09/15/open-ai-google-anthropic-safety.html">OpenAI, Google, Anthropic discussing collaboration on AI ...</a></li>
<li><a href="https://finance.yahoo.com/technology/ai/articles/openai-anthropic-google-deepmind-discuss-171923921.html?fr=sycsrp_catchall">OpenAI, Anthropic And Google DeepMind Discuss AI Safety As ...</a></li>
<li><a href="https://www.the-independent.com/news/world/americas/trump-ai-safety-us-china-b3049484.html">Trump dismisses AI safety fears to keep America ahead of China | The Independent</a></li>
<li><a href="https://cryptobriefing.com/trump-dismisses-ai-safety-china-competition/">Donald Trump dismisses AI safety concerns, prioritizes competition with China</a></li>
<li><a href="https://www.facebook.com/KRDO13/posts/anthropic-google-and-openai-have-discussed-creating-an-ai-industry-standards-bod/1575692261268243/">Anthropic, Google, and OpenAI have discussed creating an AI industry ...</a></li>
<li><a href="https://time.com/article/2026/09/15/ai-anthropic-researcher-quits-coxon-slowdown/">OpenAI and Anthropic Researchers Are Warning About AI Risks - TIME</a></li>

</ul>
</details>

**Tags**: `#ai-safety`, `#ai-policy`, `#openai`, `#anthropic`, `#google-deepmind`

---

<a id="item-tech-news-11"></a>
### [America is building datacenters faster than the grid can power them](https://www.theregister.com/on-prem/2026/09/15/america-is-building-datacenters-faster-than-the-grid-can-power-them/5296608) ⭐️ 7.0/10

The Register reports that U.S. datacenter construction is currently outpacing the electrical grid&\#x27;s capacity to power new facilities, creating a structural bottleneck for the country&\#x27;s compute buildout. According to the source, meeting projected energy consumption through 2030 will require an estimated $110 billion in new power generation resources to close the gap between demand and supply. The headline framing positions the mismatch between rapid datacenter deployment and slower grid expansion as a critical infrastructure issue for the broader technology industry, with consequences for site selection, project timelines, and energy planning. Because the provided source content is limited to a headline and subhead, further technical detail from the underlying report, including methodology, regional breakdowns, and specific generation types, is not available in the supplied material.

rss · The Register · Sep 15, 16:37

**「Background」** U.S. datacenters have expanded rapidly since the early 2020s as cloud computing and, more recently, generative AI workloads have driven unprecedented demand for compute capacity, making the country the global center of datacenter construction. The U.S. electrical grid, much of which was built decades ago around more stable demand patterns, is now straining to keep pace with these clustered, high-density loads that require continuous, large-scale power. Industry analysts such as Moody&\#x27;s Ratings and Boston Consulting Group have begun quantifying the gap between planned datacenter capacity and available generation, projecting multi-gigawatt shortfalls and tens of billions of dollars in required investment through the end of the decade.

**「Impact」** U.S. datacenter operators, cloud providers, and AI builders now face an estimated $110 billion bill for new power generation resources by 2030, with grid availability poised to dictate site selection, construction pacing, and capital deployment across the sector.

<details><summary>References</summary>
<ul>
<li><a href="https://cryptobriefing.com/moodys-110b-us-data-center-power-2030/">US data center boom faces $110 billion power buildout by 2030</a></li>
<li><a href="https://www.theregister.com/on-prem/2026/09/15/america-is-building-datacenters-faster-than-the-grid-can-power-them/5296608">America is building datacenters faster than the grid can power them</a></li>
<li><a href="https://www.bcg.com/publications/2026/solving-the-us-data-center-power-crunch">Solving the US Data Center Power Crunch | BCG</a></li>
<li><a href="https://enkiai.com/ai-market-intelligence/ai-data-center-power-grid-limits-reshape-energy-in-2026/">AI Data Center Power: Grid Limits Reshape Energy in 2026</a></li>
<li><a href="https://www.datacenterknowledge.com/operations-and-management/2026-predictions-ai-sparks-data-center-power-revolution">2026 Predictions: AI Sparks Data Center Power Revolution</a></li>
<li><a href="https://enkiai.com/data-center/ai-data-center-grid-strain-power-halts-growth-in-2026/">AI Data Center Grid Strain: Power Halts Growth in 2026 - Enki.AI</a></li>

</ul>
</details>

**Tags**: `#datacenter`, `#infrastructure`, `#energy`, `#AI-infrastructure`, `#cloud-computing`

---

<a id="item-tech-news-12"></a>
### [PostgreSQL 19 graph queries fail the &\#x27;would you ship this?&\#x27; test](https://www.theregister.com/databases/2026/09/15/postgresql-19-graph-queries-fail-the-would-you-ship-this-test/5296343) ⭐️ 7.0/10

The Register reports that PostgreSQL 19&\#x27;s SQL/PGQ graph query support faces unresolved bugs blocking a &\#x27;ship it&\#x27; verdict, while concurrent REPACK promises to reduce maintenance windows for DBAs.

rss · The Register · Sep 15, 09:42

**Tags**: `#PostgreSQL`, `#databases`, `#open-source`, `#SQL`, `#database-administration`

---

<a id="item-tech-news-13"></a>
### [IBM Research Adds Consistency-Aware Evaluation to ALTK-Evolve](https://huggingface.co/blog/ibm-research/altk-evolve-consistency) ⭐️ 7.0/10

IBM Research introduced a consistency-aware evaluation extension for its ALTK-Evolve toolkit, targeting the gap between average agent benchmark scores and run-to-run repeatability of LLM agents. The post defines a new metric, Pass^k \(the fraction of tasks where an agent succeeds on all k runs\), distinct from the optimistic Pass@k, and reports a 24.4-point consistency gap on AppWorld test\_normal \(168 tasks\) for a ReAct agent on GPT-4.1, where Mean@5 reached 77.4% but Pass^5 was only 53.0%, widening to roughly 30 points on hard tasks. To address this, IBM added a Consistency Analyzer that resamples each decision step in a single recorded trajectory using k=5 completions \(default\) to flag flat, flip-prone probability distributions, and converts those flags into consistency guidelines in the existing ALTK-Evolve format. Injecting these guidelines at inference time cut the consistency gap roughly in half, raising Pass^5 from 53.0% to 69.0% \(+16.0pp\) and Mean@5 from 77.4% to 81.0%, with the largest gains on medium \(+22.9pp\) and hard \(+14.3pp\) tiers and no loss in average accuracy; the full methodology is documented in an arXiv technical report. The diagnostic is fully black-box, requiring only one trajectory and no logits or model internals, and the guidelines target instability rather than failure.

rss · Hugging Face Blog · Sep 15, 16:00

**「Background」** Standard agent benchmarks typically report Mean@k or Pass@k, averaging success across k runs or counting any-of-k success respectively; these metrics obscure how often a model succeeds on every repetition, which is the property production users care about. ALTK-Evolve is an IBM Research system that distills an agent&\#x27;s past trajectories into reusable guidelines injected at inference time to raise task success. Pass^k, the pessimistic variant introduced here, requires all k attempts to succeed and is bounded by Pass^k ≤ Mean@k ≤ Pass@k.

**「Impact」** Practitioners deploying LLM agents on mission-critical workflows now have a black-box diagnostic and guideline-generation pipeline that nearly halves run-to-run inconsistency on AppWorld without sacrificing average accuracy, with the largest absolute gains on harder tasks.

**Tags**: `#AI Agents`, `#Agent Evaluation`, `#LLM Reliability`, `#Benchmarking`, `#IBM Research`

---

## Financial News

<a id="item-finance-news-1"></a>
### [China&\#x27;s August retail sales miss forecast as investment slump deepens](https://www.cnbc.com/2026/09/15/china-august-retail-sales-industrial-output-investment-exports-.html) ⭐️ 7.0/10

China&\#x27;s August economic data showed retail sales growing just 0.4% year-on-year, missing the 0.8% forecast and slowing from 0.6% in July, while fixed-asset investment shrank 7.2% in the first eight months \(worse than the 6.7% decline in January–July\) and new bank loans fell to 60 billion yuan versus a roughly 400 billion yuan forecast.

rss · CNBC Finance · Sep 15, 09:46

**「Background」** Beijing has set an annual growth target of 4.5% to 5%, but Q2 GDP slowed to 4.3% — the weakest in more than three years — and Oxford Economics now estimates Q3 growth at just 4.3%, signalling downside risks to the annual target.

**「Impact」** The data piles pressure on Beijing for more fiscal support, with Pinpoint Asset Management saying markets are waiting for more supportive policy in Q3, though ANZ Research analysts expect a policy rate cut remains unlikely as long as exports power growth within the target range.

**Tags**: `#China economy`, `#economic data`, `#retail sales`, `#investment`, `#fiscal policy`

---