---
layout: default
title: "Horizon Summary: 2026-11-10 (EN)"
date: 2026-11-10
lang: en
---

> From 130 items, 18 important content pieces were selected

---

**Technology News**
1. [Report Claims Consumer Gemini Data May Reach Human Review](#item-tech-news-1) ⭐️ 8.0/10
2. [OpenSSH-musl vulnerability exploited in Linux intrusions](#item-tech-news-2) ⭐️ 8.0/10
3. [Claude Code Settings Files Expose Secrets on GitHub](#item-tech-news-3) ⭐️ 8.0/10
4. [Researchers chain app flaws for remote vehicle control](#item-tech-news-4) ⭐️ 8.0/10
5. [Claude Fable 5.2 and Mythos 5.2 Draw Scrutiny](#item-tech-news-5) ⭐️ 7.0/10
6. [Watched Earth Maps a Week of Satellite Passes](#item-tech-news-6) ⭐️ 7.0/10
7. [Washington Bettor Seeks Refund From Kalshi](#item-tech-news-7) ⭐️ 7.0/10
8. [Jensen Huang’s Espionage Allegation Triggers Nvidia Probe](#item-tech-news-8) ⭐️ 7.0/10
9. [Wyndham App Credential Exposed Customer Data](#item-tech-news-9) ⭐️ 7.0/10
10. [Waymo robotaxis continued illegally passing school buses after fix](#item-tech-news-10) ⭐️ 7.0/10
11. [Anthropic&\#x27;s super bug-finding Mythos model is going into Cisco and IBM products](#item-tech-news-11) ⭐️ 7.0/10
12. [HOPE Improves Expert Pruning for Mixture-of-Experts Models](#item-tech-news-12) ⭐️ 7.0/10
13. [Ownership Prompts Encourage Claude Fable Refactoring](#item-tech-news-13) ⭐️ 6.0/10
14. [Locating a Mysterious Beep with Claude Code](#item-tech-news-14) ⭐️ 6.0/10
15. [NVIDIA and Elith Release Synthetic Japanese Financial Personas](#item-tech-news-15) ⭐️ 6.0/10
16. [OpenAI Introduces Control Room for Research Workload Control](#item-tech-news-16) ⭐️ 6.0/10
17. [AI Model Claims Simulation Across Materials and Proteins](#item-tech-news-17) ⭐️ 6.0/10
18. [HUMAIN and Infra Agree $666.7M Saudi AI Infrastructure Financing](#item-tech-news-18) ⭐️ 6.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Report Claims Consumer Gemini Data May Reach Human Review](https://github.com/thisisme6598/gemini_files/) ⭐️ 8.0/10

A third-party technical investigation published in the gemini\_files repository claims that Consumer Gemini using Connected Apps may route personal Google Drive files and Gmail content to human annotators. The reported concern applies specifically to consumer products that access authorized connected data; commenters say Google’s Workspace Gemini and Workspace Intelligence still claim not to use human review. If the report is accurate, this would extend access to sensitive emails and files beyond automated processing and create significant privacy and AI-governance concerns. The supplied evidence does not include official confirmation from Google or establish details such as review triggers, retention policies, safeguards, or whether reviewed data is used for training.

hackernews · gf74918 · Nov 9, 18:24 · [Discussion](https://news.ycombinator.com/item?id=50429426)

**「Background」** Consumer Gemini can retrieve personal Google Workspace content, including Gmail messages and Drive files, when users authorize relevant Connected Apps, whereas Workspace Gemini operates under separate organizational administration. Google’s privacy materials list human reviewers among several parties that may handle Gemini data, and disconnecting Workspace from Gemini also removes access to Drive, Docs, Keep, and other workspace apps.

**「Practical impact」** If the report is accurate, Consumer Gemini users who authorize Gmail or Drive may have personal content reviewed by humans; with Gemini Apps Activity enabled, interactions may be retained for up to three years and used to improve Google&\#x27;s AI systems. Users can reduce exposure by revoking unnecessary connected-app permissions and disabling Gemini Apps Activity.

**「Community Discussion」** Commenters emphasized the distinction between Consumer Gemini with Connected Apps and Workspace products, citing Google’s continued assurance that Workspace data is not subject to human review. Several described the practice as an unacceptable erosion of privacy, while one offered anecdotal evidence that unusually specific Gemini responses appeared connected to their emails; broader concerns about annotator access, model training, and photo-derived data were raised but do not independently verify the underlying claim.

<details><summary>References</summary>
<ul>
<li><a href="https://tech.yahoo.com/ai/gemini/articles/stop-gemini-accessing-emails-two-103013901.html">Stop Gemini from accessing your emails with these two hidden settings</a></li>
<li><a href="https://proton.me/lumo/ai/gemini-privacy-policy">Gemini ’s privacy policy explained | Proton</a></li>
<li><a href="https://proton.me/blog/turn-off-gemini-on-android">Google AI is watching: How to turn off Gemini on Android | Proton</a></li>
<li><a href="https://windowsforum.com/threads/gmail-privacy-and-ai-training-how-to-opt-out-of-gemini-data-use.390715/">Gmail Privacy and AI Training: How to Opt Out of Gemini Data Use</a></li>

</ul>
</details>

**Tags**: `#Google Gemini`, `#human annotation`, `#data privacy`, `#connected apps`, `#Google Workspace`

---

<a id="item-tech-news-2"></a>
### [OpenSSH-musl vulnerability exploited in Linux intrusions](https://arstechnica.com/security/2026/11/vulnerability-that-lets-hackers-ssh-into-linux-devices-is-under-active-exploitation/) ⭐️ 8.0/10

Researchers report that attackers are actively exploiting a critical vulnerability tracked as \*sshole to obtain privileged access to affected Linux systems. The flaw arises from an interaction between OpenSSH and the musl C library, allowing systems that meet additional, unspecified requirements to be compromised with unauthenticated access to high-privilege accounts within seconds. After \*sshole became public last Thursday, Greynoise observed the tracked GT10 group conducting mature intrusions against honeypots in Southeast Asia four days later. GT10 installed Python 3 where needed to run its TAC Agent backdoor, which supports shell commands, reconnaissance, and persistence; the backdoor contains Chinese-language comments and appears to have been generated with AI assistance. OpenSSH has released a fix, although the supplied account does not identify affected versions or detailed remediation requirements.

rss · Ars Technica · Nov 9, 19:41

**「Background」** The flaw affects OpenSSH’s sshd when running on musl-based Linux without PAM, a configuration used by default packages in distributions such as Alpine Linux. On vulnerable systems, an oversized password can bypass authentication and permit access to passwordless or password-disabled accounts, including privileged ones. OpenSSH 10.6p2 contains a fix, and operators are advised to install the patched OpenSSH or distribution package and restart sshd.

**「Operational impact」** Linux operators using OpenSSH and musl on systems that meet the vulnerability’s requirements should apply the released OpenSSH fix promptly and investigate for compromise, because active exploitation has produced unauthenticated privileged access and installation of the Python-dependent TAC Agent backdoor within seconds; post-exploitation telemetry identifies six attacker IPs, though not all SSHole activity is attributable to GT10.

<details><summary>References</summary>
<ul>
<li><a href="https://radar.cloudflare.com/security/zero-wire/sshole">sshole : OpenSSH password bypass on musl Linux | Cloudflare Radar</a></li>
<li><a href="https://thehackernews.com/2026/11/hackers-exploited-openssh-sshole-flaw.html">Hackers Target OpenSSH SSHole Flaw Within Hours of Disclosure...</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/openssh-flaw-lets-attackers-log-into-password-disabled-linux-accounts/">OpenSSH flaw lets attackers log into password-disabled Linux accounts</a></li>
<li><a href="https://sshole.events.greynoise.io/">SSHole (CVE-2026-123158) Activity 2026 | Tagged IP Analysis</a></li>

</ul>
</details>

**Tags**: `#Linux security`, `#OpenSSH`, `#musl`, `#active exploitation`, `#authentication bypass`

---

<a id="item-tech-news-3"></a>
### [Claude Code Settings Files Expose Secrets on GitHub](https://arstechnica.com/ai/2026/11/claude-code-settings-files-expose-thousands-of-secrets-on-github/) ⭐️ 8.0/10

Researchers at Apiiro report that Claude Code can write literal shell commands, including embedded credentials, into a user&\#x27;s \`.claude/settings.local.json\` file when the user selects “Yes, and don’t ask again” to approve a command. Although Claude Code&\#x27;s documentation places this file in a developer&\#x27;s global \`.gitignore\`, the protection is not reflected in repository-level ignore rules, allowing the file to be uploaded when a repository is cloned elsewhere, a folder is initialized as a repository, or Claude Code commits the file without explicit user input. Apiiro identified more than 100,000 public GitHub occurrences of the local settings file; roughly 1,100 files across 63 organizations reportedly contained API tokens, database passwords, private keys, or other sensitive credentials. Removing an exposed file from a repository does not necessarily remove the secrets from existing forks.

rss · Ars Technica · Nov 9, 17:24

**「How the leak works」** Claude Code stores approved commands as rules in \`.claude/settings.local.json\`; depending on the rule, it may preserve the command literally instead of reducing it to a generalized pattern. Global Git ignore rules protect the file only in the developer&\#x27;s existing environment, whereas a cloned repository or a newly initialized repository may not carry over that protection.

**「Consequences for developers」** Developers and organizations that uploaded these settings files face potential disclosure of API tokens, database passwords, private keys, and root credentials, and deleting the file from the current repository does not necessarily eliminate the secrets from existing forks.

**Tags**: `#AI security`, `#Claude Code`, `#secret leakage`, `#GitHub`, `#developer tools`

---

<a id="item-tech-news-4"></a>
### [Researchers chain app flaws for remote vehicle control](https://www.theregister.com/security/2026/11/09/researchers-pwn-automakers-android-apps-to-remotely-unlock-cars-honk-horns/5308483) ⭐️ 8.0/10

A pair of security researchers demonstrated that flaws in automakers’ Android apps could be chained to remotely control vehicles in Australia and the United States. Their attack combined web application firewall bypasses with default login credentials, reportedly enabling commands such as unlocking cars and honking horns. The findings highlight how failures in both perimeter protection and application authentication can expose sensitive connected-car functions. The supplied report does not identify the automakers, affected app versions, or whether the vulnerabilities have been patched.

rss · The Register · Nov 9, 17:31

**「Connected-Car App Security」** Connected-car Android apps can act as remote interfaces for functions such as locking, engine starting, and horn or light activation, with cloud services handling authentication and commands. A web application firewall \(WAF\) filters backend requests to block suspicious or unauthorized activity, while default credentials are logins that remain usable without being changed. Combining a WAF bypass with default-log access shows how weaknesses in both perimeter filtering and account authentication can expose physical vehicle controls.

**「Impact」** Exploiting the automakers’ Android apps allowed researchers to remotely start engines, flash headlights, and sound horns on connected vehicles from two major automakers. Both automakers fixed the vulnerabilities and rotated the affected credentials within about two hours of disclosure, although the researchers tested the complete chain only with U.S. accounts and vehicles.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theregister.com/security/2026/11/09/researchers-pwn-automakers-android-apps-to-remotely-unlock-cars-honk-horns/5308483">Researchers pwn automakers ’ Android apps to remotely unlock ...</a></li>
<li><a href="https://www.ericpetersautos.com/2026/11/09/bye-bye-boxer-and-maybe-subaru-too/">Bye Bye Boxer . . . And Maybe Subaru, Too - EPautos - Libertarian Car...</a></li>
<li><a href="https://www.theregister.com/security/2026/11/09/researchers-pwn-automakers-android-apps-to-remotely-unlock-cars-honk-horns/5308483">Researchers pwn automakers ’ Android apps to remotely unlock ...</a></li>
<li><a href="https://samcurry.net/forgerock">Hacking Two Automakers : ForgeRock Path Confusion, RCE, and...</a></li>

</ul>
</details>

**Tags**: `#connected-car security`, `#Android apps`, `#authentication bypass`, `#web application firewalls`, `#vehicle remote control`

---

<a id="item-tech-news-5"></a>
### [Claude Fable 5.2 and Mythos 5.2 Draw Scrutiny](https://www.anthropic.com/claude-fable-and-mythos-5-2) ⭐️ 7.0/10

The item frames Anthropic&\#x27;s Claude Fable 5.2 and Mythos 5.2 as new model releases, but the supplied material contains no primary announcement, so their exact capabilities, positioning, pricing, and compatibility cannot be verified. The most substantive firsthand reports concern Fable 5.2&\#x27;s coding: one tester said it consumed half of a five-hour token budget in 30 minutes while reporting seven potentially serious bugs in an Opus 5.5-generated browser machine-vision project, while another said early testing accelerated work on a 600,000-line Fortran materials-science codebase by 36 times in two days. These results are anecdotal and unverified, and the latter comment is truncated. Discussion also challenged benchmark design, including the effort-performance curve and choice of comparison models, while speculating without evidence that the 5.2 numbering reflected competitive timing against OpenAI&\#x27;s Astra and that Anthropic might reserve version 5.5.

hackernews · lairv · Nov 9, 18:01 · [Discussion](https://news.ycombinator.com/item?id=50429068)

**「Release context」** Anthropic has introduced Claude Fable 5.2 and Claude Mythos 5.2 as part of its Claude model lineup, with the announcement emphasizing benchmark results and coding performance. A highlighted example says Fable 5.2 ran Quantum ESPRESSO’s phonon code about 36 times faster on average than the stock version on the same GPU, reducing 13 benchmark cases from 3.3 hours to under four minutes.

**「Practical Impact」** Developers can now use the broadly available Claude Fable 5.2 for coding and reasoning tasks Anthropic says benchmarks above Opus 5.5 in nearly all evaluated capabilities, reducing the need to default to Opus for some workloads. Independent real-world validation is still pending, so the comments’ reported bug-finding and 36× Fortran optimization gains should be treated as early anecdotes rather than established results.

**「Community discussion」** Users described Fable 5.2 as competitive with Opus 5.5, particularly for code review, but said ordinary prompts may not reveal a clear difference and cautioned that the reported bugs and speedups need independent validation. The strongest criticism targeted Anthropic&\#x27;s benchmark presentation, with commenters questioning the Carbon effort curve, inconsistent competitor pairings, and the absence of a cyber-model comparison; another commenter speculated that Anthropic released 5.2 to mirror a new OpenAI Astra model, although no evidence was offered.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/claude-fable-and-mythos-5-2">Introducing Claude Fable 5 . 2 and Claude Mythos 5 . 2 \ Anthropic</a></li>
<li><a href="https://www.anthropic.com/claude-fable-and-mythos-5-2">Introducing Claude Fable 5.2 and Claude Mythos 5.2 \ Anthropic</a></li>
<li><a href="https://www.online-tech-tips.com/anthropic-claude-fable-5-2-mythos-5-2/">Anthropic releases Claude Fable 5.2 and Mythos 5.2 with ...</a></li>

</ul>
</details>

**Tags**: `#large-language-models`, `#AI model releases`, `#software engineering`, `#model evaluation`

---

<a id="item-tech-news-6"></a>
### [Watched Earth Maps a Week of Satellite Passes](https://www.watched.earth/) ⭐️ 7.0/10

Watched Earth is an open-source web application that finds satellites that passed over a user-specified location during the previous seven days and displays the corresponding imagery. It uses SGP4 tracking against the CelesTrak catalog for more than 17,000 objects, running in the browser in roughly half a second while rendering the objects on the GPU and solving Kepler’s equation each frame. The project integrates real imagery from Sentinel-2, Landsat, and NASA, including calculations to correct Sentinel-2 timestamps that can differ from the actual overpass time by five to ten minutes. The developer says the service does not store users’ locations and has published the code on GitHub.

hackernews · a585gupt · Nov 9, 17:51 · [Discussion](https://news.ycombinator.com/item?id=50428907)

**「Matching satellite passes with imagery」** Orbital catalogs provide satellite elements that SGP4 propagates into estimated positions and ground tracks, allowing services to calculate which passes crossed a chosen location during a given period. Earth-observation archives such as Sentinel-2, Landsat, and NASA store imagery separately, so matching a photograph to a pass may require accounting for timestamp differences and cloud cover.

**「Impact」** For researchers, trip planners, and geospatial users, Watched Earth provides a simpler location-first way to find real Sentinel-2, Landsat, and NASA images from satellites that passed over a selected place during the previous seven days, avoiding the manual collection and time-range selection required in tools such as the Copernicus Browser.

**「Community Discussion」** Commenters praised the project’s visual design, orbit and ground-track rendering, seamless integration of multiple geospatial data sources, and unusually broad satellite coverage. People working in geospatial planning and backpacking also described it as a practical, easier-to-use alternative to existing resources such as Copernicus because it links passes to the exact satellite images taken during them.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/dev-Armaan/satellites">GitHub - dev-Armaan/satellites</a></li>
<li><a href="https://browser.dataspace.copernicus.eu/?zoom">Copernicus Browser</a></li>
<li><a href="https://www.watched.earth/">Watched · Something watched you this week</a></li>

</ul>
</details>

**Tags**: `#satellite tracking`, `#earth observation`, `#orbital mechanics`, `#browser graphics`, `#open source`

---

<a id="item-tech-news-7"></a>
### [Washington Bettor Seeks Refund From Kalshi](https://arstechnica.com/tech-policy/2026/11/man-who-lost-308000-on-sports-bets-sues-kalshi-for-offering-illegal-gambling/) ⭐️ 7.0/10

Bellevue resident Scott Bright sued KalshiEX LLC in King County Superior Court on September 24, alleging that sports wagers he placed on the prediction-market platform violated Washington’s online-gambling ban. Bright says he lost more than $308,000 and is seeking over $580,000 under a state law that allows people who lose money in illegal gambling to recover it from the operator. Kalshi moved to dismiss and argued that the case belongs in federal court because its “event contracts” are not gambling and can be regulated only by the federal government. The dispute comes as state attorneys general are challenging Kalshi, while an earlier Washington order restricting the wagers Kalshi may offer took effect only after Bright’s losses.

rss · Ars Technica · Nov 9, 21:13

**「Background」** Prediction markets allow users to wager on the outcomes of future events and have become central to disputes over whether state gambling laws or federal regulation apply. Washington has prohibited internet gambling since 2006 and provides a statutory means for gambling losers to seek recovery; its Recovery of Money Lost at Gambling Act also allows the attorney general to recover money lost by Washington residents.

**「Impact」** If Bright succeeds, the case could establish whether an individual Washington customer can use the state’s gambling-recovery law to obtain restitution from Kalshi. The early-stage motion to dismiss leaves that question unresolved.

**Tags**: `#prediction markets`, `#online gambling`, `#regulation`, `#Kalshi`, `#technology policy`

---

<a id="item-tech-news-8"></a>
### [Jensen Huang’s Espionage Allegation Triggers Nvidia Probe](https://arstechnica.com/tech-policy/2026/11/ceo-jensen-huang-admits-affair-as-nvidia-probes-possible-chinese-espionage/) ⭐️ 7.0/10

Nvidia CEO Jensen Huang admitted in an internal employee message that he had an affair, after the Financial Times reported that US intelligence believed Alice Huang—an executive at Singapore-based Nvidia customer Megaspeed—had been recruited to spy for China’s Ministry of State Security. Nvidia said its board would open an independent investigation into reports that Huang had been the target of a foreign intelligence effort; Huang apologized, said he would cooperate, and pledged his continued commitment to the company. The allegation raises leadership, national-security and governance concerns for the prominent AI-chip company and may complicate Nvidia’s lobbying to loosen US chip-export restrictions while retaining access to China. Nvidia shares were reported to have fallen more than 4% after the investigation was announced, although the supplied reporting cites people familiar with an intelligence memo rather than publishing the underlying documentation or a government response.

rss · Ars Technica · Nov 9, 15:23

**「Background」** Jensen Huang co-founded Nvidia and has led it through the company’s rise as a major supplier of AI chips, making his leadership central to U.S. technology and national-security debates. The foreign-intelligence issue centers on reports that U.S. officials, citing an intelligence memo, believed Alice Huang—an executive at Nvidia customer Megaspeed—was recruited by China’s Ministry of State Security and had a romantic relationship with Huang; the supplied material does not include the underlying assessment. The episode has also intensified legislative scrutiny of Nvidia’s China business and U.S. chip-export rules, with lawmakers pressing the company for answers.

**「Corporate and Policy Consequences」** Nvidia shares fell more than 4% after the company opened an independent investigation, while the alleged intelligence links increase scrutiny of Huang’s leadership credibility and Nvidia’s ability to advocate for U.S. chip-export policy and continued access to China. The supplied reporting includes no direct intelligence documentation or government response, so the extent of any espionage or security breach remains unestablished.

<details><summary>References</summary>
<ul>
<li><a href="https://www.nytimes.com/2026/11/08/technology/nvidia-investigation-jensen-huang-china.html">Nvidia Opens Investigation Into Jensen Huang’s Relationship ...</a></li>
<li><a href="https://www.politico.com/news/2026/11/08/nvidia-investigation-chinese-spy-effort-jensen-huang-01155747">Nvidia launches investigation into reported Chinese spy ...</a></li>
<li><a href="https://www.dw.com/en/nvidia-ceo-huang-admits-affair-amid-rumors-of-china-spy-ties/a-79894747">Nvidia CEO Huang admits affair amid rumors of China spy ties</a></li>
<li><a href="https://www.cnbc.com/2026/11/08/nvidia-jensen-huang-investigation-china-spy.html">Nvidia investigates CEO Jensen Huang &#x27;s relationship with alleged...</a></li>

</ul>
</details>

**Tags**: `#Nvidia`, `#Jensen Huang`, `#national security`, `#Chinese espionage`, `#AI chips`

---

<a id="item-tech-news-9"></a>
### [Wyndham App Credential Exposed Customer Data](https://techcrunch.com/2026/11/09/hotel-giant-wyndham-exposed-customer-data-after-app-security-lapse/) ⭐️ 7.0/10

Wyndham reportedly left a hardcoded credential in its customer app that could allow anyone to access customer data. The hotel operator would not say whether it had the ability to determine whether any unauthorized access occurred before discovering the flaw. The supplied report does not establish whether customer data was actually accessed, how many records were exposed, or how long the credential remained embedded. The incident highlights the security risk of placing reusable secrets directly in client applications.

rss · TechCrunch · Nov 9, 23:03

**「Hardcoded App Credentials」** A hardcoded credential is a secret embedded directly in an application rather than protected through a proper authentication flow; when it grants access to backend systems, extracting it can bypass expected user authentication and expose records. Similar mobile-app flaws have been reported in a patient-care service, where hardcoded credentials could let holders obtain or modify sensitive patient data, and at Applebee&\#x27;s, where researchers found database credentials that exposed customer information. These cases show that embedding reusable credentials in apps is a recurring application-security failure mode, although the supplied report does not establish whether Wyndham&\#x27;s exposed credential was abused or how long it remained accessible.

**「User impact」** The hardcoded credential in Wyndham’s Android app could have allowed anyone to retrieve customer names, email addresses, Wyndham member numbers, sign-in JWTs, and internal files from a Salesforce-hosted database. Wyndham has not said whether it can determine whether the credential was abused historically, so the scale of any actual exposure remains unknown.

<details><summary>References</summary>
<ul>
<li><a href="https://www.zdnet.com/article/widely-used-clinical-service-found-to-include-hidden-backdoor-account/">Widely-used patient care app found to include hidden &#x27;backdoor&#x27; access</a></li>
<li><a href="https://www.techradar.com/pro/security/applebees-forced-to-fix-serious-security-issue-which-exposed-customer-data">Researcher found hardcoded credentials in Applebee&#x27;s mobile app</a></li>
<li><a href="https://techcrunch.com/2026/11/09/hotel-giant-wyndham-exposed-customer-data-after-app-security-lapse/">Hotel giant Wyndham exposed customer data after app security ...</a></li>
<li><a href="https://daily.dev/posts/hotel-giant-wyndham-exposed-customer-data-after-app-security-lapse-ag5qjtv06">Hotel giant Wyndham exposed customer data after app...</a></li>

</ul>
</details>

**Tags**: `#application security`, `#hardcoded credentials`, `#data exposure`, `#Wyndham`

---

<a id="item-tech-news-10"></a>
### [Waymo robotaxis continued illegally passing school buses after fix](https://techcrunch.com/2026/11/09/waymo-robotaxis-kept-illegally-passing-school-buses-after-software-fix-feds-say/) ⭐️ 7.0/10

Federal regulators say Waymo robotaxis continued illegally passing school buses nearly a year after the company deployed a software update intended to address the behavior. The allegation suggests the fix did not fully resolve the reported issue, raising concerns about software validation and regulatory oversight of Waymo’s autonomous-driving system. The supplied source excerpt does not specify the number of incidents, jurisdictions, regulatory findings, or technical details of the update.

rss · TechCrunch · Nov 9, 15:24

**「Software Fix and Subsequent Incidents」** Waymo said it deployed a software update to all affected robotaxis on November 17, 2025, to address incidents involving vehicles passing stopped school buses. However, the National Highway Traffic Safety Administration said that most of the reported incidents occurred after the update.

**「Regulatory and safety impact」** The repeated post-fix incidents in Austin indicate an unresolved software-validation gap in how Waymo robotaxis detect and yield to school buses, leaving the company exposed to continued federal scrutiny and possible corrective requirements; the available evidence does not show that a recall, suspension, or other specific remedy has been ordered.

<details><summary>References</summary>
<ul>
<li><a href="https://techcrunch.com/2026/11/09/waymo-robotaxis-kept-illegally-passing-school-buses-after-software-fix-feds-say/">Waymo robotaxis kept illegally passing school buses after software ...</a></li>
<li><a href="https://techcrunch.com/2026/11/09/waymo-robotaxis-kept-illegally-passing-school-buses-after-software-fix-feds-say/">Waymo robotaxis kept illegally passing school buses after software ...</a></li>

</ul>
</details>

**Tags**: `#Waymo`, `#robotaxis`, `#autonomous vehicles`, `#AI safety`, `#transportation regulation`

---

<a id="item-tech-news-11"></a>
### [Anthropic&\#x27;s super bug-finding Mythos model is going into Cisco and IBM products](https://www.theregister.com/ai-and-ml/2026/11/10/anthropics-super-bug-finding-mythos-model-is-going-into-cisco-and-ibm-products/5308616) ⭐️ 7.0/10

Cisco and IBM are planning to embed Anthropic&\#x27;s Mythos bug-finding capabilities into enterprise security products without exposing the underlying model.

rss · The Register · Nov 10, 00:00

**Tags**: `#AI security`, `#vulnerability detection`, `#Anthropic`, `#enterprise software`, `#Cisco and IBM`

---

<a id="item-tech-news-12"></a>
### [HOPE Improves Expert Pruning for Mixture-of-Experts Models](https://huggingface.co/blog/amazon/higher-order-pruning-experts) ⭐️ 7.0/10

HOPE \(Higher-Order Pruning of Experts\) is a second-order method for permanently pruning experts from Mixture-of-Experts language models without retraining, while remaining compatible with quantization and avoiding the latency of dynamic expert loading or offloading. Unlike first-order methods that score experts independently, HOPE models pairwise expert cooperation through an F-matrix whose diagonal approximates REAP importance rankings and whose off-diagonal entries capture co-activation interactions; it uses one calibration forward pass and solves a continuously relaxed quadratic program in roughly 1–2 seconds per layer before rounding it to a binary pruning decision. The article reports evaluations on Qwen3.5-122B, Qwen3.5-35B, and GLM-4.5-Air, using Evol-CodeAlpaca and SWE-Bench Verified trajectories for calibration and Tulu3 and SWE-Bench Pro for testing against REAP, MAN, EAN, and Frequency at 10%–50% pruning rates. Across those conditions, HOPE reportedly achieved the best average rank at 2.07 out of five methods, 39% top-1 finishes, 67% top-2 finishes, and gains of up to 6.1% on agentic coding tasks over the next-best method at 50% pruning. The memory motivation is substantial: Qwen3.5-122B is described as having 256 experts in each of 48 MoE layers, with expert MLPs accounting for about 95% of its roughly 250-GB parameter footprint despite only eight experts per layer being active for each token; however, the supplied excerpt does not provide exact post-pruning memory measurements or detailed quality trade-offs.

rss · Hugging Face Blog · Nov 9, 12:34

**「Background」** In a Mixture-of-Experts \(MoE\) model, a router sends each token to a small top-K subset of expert MLPs, enabling models with very large parameter counts while leaving all expert weights in inference memory. Expert pruning reduces that footprint by permanently removing selected experts, but common first-order methods score each expert independently and can overlook stable groups of co-activated, cooperating experts. HOPE is a second-order formulation that includes pairwise interaction terms; REAP can be viewed as its first-order special case when those terms are ignored.

**「Impact」** For MoE operators, HOPE enables permanent pruning of 10%–50% of experts without retraining, reducing expert-memory requirements while remaining compatible with quantization; at 50% pruning, it achieved the best average rank and improved agentic-coding results by up to 6.1% over the next-best method in the reported tests. The evidence covers three models and specific coding benchmarks, so it does not establish the same quality tradeoffs across other workloads.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2609.18916">[2609.18916] Higher-order pruning of experts in mixture-of ...</a></li>
<li><a href="https://arxiv.org/abs/2510.13999">[2510.13999] REAP the Experts: Why Pruning Prevails for One ... REAP the Experts: Why Pruning Prevails for One-Shot MoE ... REAP the Experts: Why Pruning Prevails for One-Shot MoE ... Router-weighted Expert Activation Pruning (REAP) - GitHub REAP E : WHY PRUNING PREVAILS FOR NE-S M E COMPRESSION Router-weighted Expert Pruning (REAP) - emergentmind.com REAP: - Cerebras</a></li>
<li><a href="https://extrapolator.ai/2026/11/09/amazon-hope-prunes-moe-experts-using-second-order-interactions/">Amazon HOPE Prunes MoE Experts Using Second-Order ...</a></li>
<li><a href="https://todayforai.com/en/items/art-dc5121c2-115">Amazon&#x27;s HOPE Higher-Order Expert Pruning Cuts MoE Memory ...</a></li>

</ul>
</details>

**Tags**: `#mixture-of-experts`, `#expert pruning`, `#LLM inference`, `#model compression`, `#higher-order pruning`

---

<a id="item-tech-news-13"></a>
### [Ownership Prompts Encourage Claude Fable Refactoring](https://simonwillison.net/2026/Nov/10/prompting-claude-fable-52/) ⭐️ 6.0/10

Anthropic reports that Claude Fable 5.2 responds strongly to how a prompt frames ownership of the codebase. In tests on small coding tasks, telling the model, “This codebase is yours” led it to merge repeated code in about half of attempts, compared with under a tenth when ownership was unstated or the codebase was presented as someone else’s. Without explicit ownership framing, the model tended to extend the existing structure even when doing so duplicated code. Developers can use this phrasing to encourage structural cleanup and consolidation, although the evidence comes from Anthropic’s limited small-task testing rather than broad model analysis.

rss · Simon Willison · Nov 10, 05:34

**「Code ownership in coding prompts」** Anthropic’s model-specific guidance for Claude Fable 5.2 treats code ownership as a prompting pattern that can influence whether a coding agent preserves an existing architecture or refactors it. “Ownership” here is prompt framing rather than a change in legal or operational responsibility.

**「Impact」** Developers using Claude Fable 5.2 for refactoring can make it more likely to consolidate repeated code by explicitly telling it, “This codebase is yours,” with Anthropic observing that behavior in about half of small-task trials versus under one-tenth without that framing. This remains a prompting heuristic rather than a general performance guarantee because Anthropic’s evidence covers small coding tasks.

<details><summary>References</summary>
<ul>
<li><a href="https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/prompting-claude-fable-5-2">Prompting Claude Fable 5.2 - Claude Platform Docs</a></li>
<li><a href="https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/prompting-claude-fable-5-2">Prompting Claude Fable 5.2 - Claude Platform Docs</a></li>

</ul>
</details>

**Tags**: `#Claude Fable 5.2`, `#prompt engineering`, `#coding agents`, `#code refactoring`

---

<a id="item-tech-news-14"></a>
### [Locating a Mysterious Beep with Claude Code](https://simonwillison.net/2026/Nov/9/mysterious-beeps/) ⭐️ 6.0/10

Simon Willison used Claude Code to build Beep Locator, a Python web application that coordinates phones, tablets, and laptops as microphones to triangulate an intermittent beep. He began the project in Claude Code Cloud from his iPhone with Opus 5.5 in Extra thinking mode, then continued development locally. Listeners connect over WebSockets, maintain 60-second audio buffers, use fast Fourier transform and high-pass filtering to detect candidate beeps, and upload clips surrounding a server-triggered chirp so sound arrivals can be aligned. The interface includes manual placement in “Rough mode,” calibration, clap testing, frequency confirmation, loudness guidance, and detection of physically impossible arrival times. In practice, the system narrowed the source to within about 40 cm, leading Willison to an old carbon monoxide detector that needed new batteries.

rss · Simon Willison · Nov 9, 23:57

**「Background」** Beep Locator was inspired by BeepBeep, a 2007 software-only acoustic ranging system for commodity devices that combines two-way sensing, self-recording, and sample counting. Its browser-based implementation uses WebAudio and WebSockets to collect and synchronize recordings from multiple devices, enabling differences in sound-arrival time to estimate the origin of a sound.

**「Practical impact」** Developers and hobbyists can reuse the open-source Beep Locator as a reference for browser-based, multi-device sound localization, illustrating how Claude Code accelerated the construction of a coordinated Python, WebSocket, and WebAudio system. It remains a personal-project prototype that required several devices and rough manual positioning, and its demonstrated result was roughly 40-centimeter localization accuracy rather than production-scale validation.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/simonw/beep-locator/compare">Compare · simonw/beep-locator · GitHub</a></li>
<li><a href="https://feeds.simonwillison.net/2026/Nov/9/mysterious-beeps/">Locating the source of a mysterious beep with Claude</a></li>

</ul>
</details>

**Tags**: `#Claude Code`, `#AI-assisted development`, `#sound localization`, `#multi-device audio`, `#web applications`

---

<a id="item-tech-news-15"></a>
### [NVIDIA and Elith Release Synthetic Japanese Financial Personas](https://huggingface.co/blog/nvidia/nemotron-personas-finance-japan) ⭐️ 6.0/10

Elith and NVIDIA have released Nemotron-Personas-Finance-Japan, a CC BY 4.0 synthetic dataset that expands 1 million records into 9 million Japanese-language personas for developing and evaluating financial AI without using real customer data. It contains 50 fields per record—9 persona fields, 11 persona attributes, and 30 contextual fields—along with approximately 1.5 billion tokens, 950,000 unique names, and more than 1,600 occupations, covering demographics, household finances, asset status, financial literacy, and behavior based on Japanese government statistics and public survey data. NVIDIA’s NeMo SDG-PGMs and NeMo Data Designer generated the data, with the source specifying gemma-4-31B-it for Japanese text, and the collection is designed to integrate with NeMo User Sim for customer simulation, dialogue generation, bias testing, and red-teaming. The article claims this is the first open million-record persona dataset combining official Japanese statistics with household-finance and financial-literacy data, but provides no independent validation, benchmark results, or comparative evidence establishing that claim. For Japanese banks, insurers, startups, and integrators, the release offers a commercially usable local simulation corpus, although its diversity, realism, and effects on downstream fairness still require application-specific evaluation.

rss · Hugging Face Blog · Nov 9, 15:05

**「Background」** Synthetic persona datasets create ... . Nemotron-Personas-Finance-Japan extends the earlier Nemotron-Personas-Japan collection by adding household-finance, asset, and financial-literacy attributes; NVIDIA and Elith generated it with NeMo Data Designer and NeMo SDG-PGMs, using official Japanese statistics and public survey distributions rather than records about real people.

**「Practical Impact」** Japanese banks, insurers, and fintech teams can use the 9 million synthetic personas to train, simulate, bias-test, and red-team financial AI without handling real customer data, while the CC BY 4.0 license lowers commercial-access barriers. Its effectiveness still requires validation against real-world behavior because the release provides limited evaluation evidence.

<details><summary>References</summary>
<ul>
<li><a href="https://www.aitoolsoasis.com/en/news/nvidia-launches-nemotron-personas-finance-japan-9m-1794243726212">NVIDIA Nemotron-Personas-Finance-Japan: 9M Synthetic Personas</a></li>
<li><a href="https://daily.dev/posts/nemotron-personas-finance-japan-a-synthetic-dataset-capturing-japan-s-demographics-and-financial-co-ebswz0n5l">Nemotron-Personas-Finance-Japan: A Synthetic Dataset...</a></li>
<li><a href="https://explainx.ai/blog/nvidia-nemotron-personas-finance-japan-synthetic-dataset-2026">Nemotron Finance Japan Dataset: 9M Personas (Nov 2026 ...</a></li>
<li><a href="https://www.aiwins.news/story/nvidia-shares-synthetic-japan-finance-dataset-for-more-localized-ai-dc555c">NVIDIA Shares Synthetic Japan Finance Dataset for More ...</a></li>
<li><a href="https://www.aitoolsoasis.com/en/news/nvidia-launches-nemotron-personas-finance-japan-9m-1794243726212">NVIDIA Nemotron-Personas-Finance-Japan: 9M Synthetic Personas</a></li>

</ul>
</details>

**Tags**: `#synthetic-data`, `#financial-AI`, `#persona-datasets`, `#privacy`, `#Japan`

---

<a id="item-tech-news-16"></a>
### [OpenAI Introduces Control Room for Research Workload Control](https://openai.com/index/control-room) ⭐️ 6.0/10

OpenAI announced Control Room, a centralized system for tracking model workloads across the company’s research infrastructure. The system is designed to stop workloads rapidly when safety or security concerns arise, providing a coordinated way to interrupt affected jobs. The announcement does not describe its architecture, deployment scope, shutdown mechanisms, or effectiveness, and provides no evidence of broad industry impact. Its immediate relevance is therefore to OpenAI’s internal AI safety, security, and infrastructure operations rather than a demonstrated change for the wider ecosystem.

rss · OpenAI News · Nov 9, 13:00

**「Background」** Model workloads are compute jobs used to train or evaluate AI models. Operating many such jobs across a research environment creates a need for centralized visibility and the ability to halt relevant work when safety or security concerns appear.

**Tags**: `#AI infrastructure`, `#AI safety`, `#workload management`, `#security`

---

<a id="item-tech-news-17"></a>
### [AI Model Claims Simulation Across Materials and Proteins](https://news.google.com/rss/articles/CBMiXEFVX3lxTFBTSjNqRzBJc3lxdE1QQmJwUFdjemp6UGFWQ0d4T1V0VkpLXzBJWVVUQXhQQjJMZzVIZVB2MGs1VWk0Wm1xQW5ZSmhWZnNLWFJ3V0Q3VGw4RHpDSHNl?oc=5) ⭐️ 6.0/10

EurekAlert\! announced a new AI model intended to simulate the behavior of substances across systems ranging from sand to proteins. The claim suggests a broad scientific machine-learning approach spanning granular materials and biological modeling. However, the supplied source is only a headline and does not identify the model, research team, publication, training methods, benchmarks, results, or validation. Its accuracy, scope, and practical limitations therefore cannot be assessed from the available evidence.

google\_news · EurekAlert\! · Nov 9, 18:58

**「Background」** Scientific machine learning uses neural networks to approximate physical dynamics, potentially reducing reliance on separate equations and material-specific solvers for each system. The reported model, WorldParticle, applies a unified architecture to phenomena spanning granular flows such as sliding sand and molecular processes such as protein folding.

**「Potential cross-domain modeling impact」** If validated, the model could provide materials-science and protein-modeling researchers with a unified way to simulate behavior across granular matter and biological systems. However, the headline provides no benchmarks, accuracy data, or comparison with existing methods, so its practical advantage remains unestablished.

<details><summary>References</summary>
<ul>
<li><a href="https://www.brightsurf.com/news/LRDYEKY8/new-ai-model-simulates-behavior-of-substances-from-sand-to-proteins.html">New AI model simulates behavior of substances, from sand to ...</a></li>

</ul>
</details>

**Tags**: `#AI for science`, `#scientific machine learning`, `#simulation`, `#materials modeling`, `#protein modeling`

---

<a id="item-tech-news-18"></a>
### [HUMAIN and Infra Agree $666.7M Saudi AI Infrastructure Financing](https://news.google.com/rss/articles/CBMi4gFBVV95cUxNcmdtc3hpSzRWa2JtTlJ6WTRZbFp4N1ctOFFoNzNIM3J1TEZ1Qk1aZFQ1Q2htLU1hSmd4dmxiakdGQjI1ejlJVjVxMUZtdG5UWFdLU1N2QjlMN1JMMDJ3R21DalU5bjQ1VVJCMGt6U2EzTHpHWnQxV1BVbm9FckY5cXFHUUZ6Q09tX3JuWlVfaFlPVXdzcUFVV1ppZUtxcVppRlNxUXdaTTIweHJvMDVMVnFaTkJ6cGxJWXBpUW9vZFVqWHl2S2tqalBNXzN1Vk01ajFhTWUzR2tuVDN6cmFxNlhB?oc=5) ⭐️ 6.0/10

Forbes Middle East reports that HUMAIN and Infra have agreed to $666.7 million in financing for AI infrastructure in Saudi Arabia. The agreement represents a material capital commitment to the country’s AI infrastructure sector. However, the supplied headline does not identify the financing structure, investors or lenders, project locations, hardware specifications, deployment schedule, or intended capacity. The deal’s precise technical scope and near-term impact therefore remain unclear pending further disclosures.

google\_news · Forbes Middle East · Nov 9, 15:39

**「Financing Context」** HUMAIN is a PIF-backed company developing AI infrastructure in Saudi Arabia, while the National Infrastructure Fund—referred to as “Infra” in the report—supports large digital-infrastructure projects. Related reporting describes an overall financing framework worth up to $1.2 billion, with non-binding terms tied to plans for as much as 250 megawatts of hyperscale AI data-center capacity.

**「Infrastructure Impact」** The financing is expected to fund GPU-equipped AI data centers for training and inference, enabling HUMAIN to serve customers in Saudi Arabia, across the region, and globally.

<details><summary>References</summary>
<ul>
<li><a href="https://www.linkedin.com/posts/aashishgidwani_humain-infra-announce-12bln-ai-projects-activity-7421417792987578368-sVoe">Saudi Arabia AI Infrastructure Fund Reaches... | LinkedIn</a></li>
<li><a href="https://www.bernama.com/en/news.php?id=2516766">Infra , HUMAIN Seal US$1.2 Bln Saudi AI Infrastructure Deal</a></li>
<li><a href="https://meatechwatch.com/2026/01/25/pif-backed-humain-secures-up-to-1-2bn-to-expand-ai-infrastructure/">PIF-backed Humain secures up to $1.2bn to expand AI infrastructure ...</a></li>
<li><a href="https://www.linkedin.com/posts/datapro-plus_saudi-infra-fund-humain-agree-up-to-12-activity-7420458498750148609-oqTq">Saudi Arabia&#x27;s Humain Secures $1.2B for AI Data Center ... | LinkedIn</a></li>
<li><a href="https://www.bernama.com/en/news.php?id=2516766">Infra , HUMAIN Seal US$1.2 Bln Saudi AI Infrastructure Deal</a></li>

</ul>
</details>

**Tags**: `#AI infrastructure`, `#startup financing`, `#Saudi Arabia`, `#compute infrastructure`

---