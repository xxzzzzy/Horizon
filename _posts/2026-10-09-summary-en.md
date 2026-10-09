---
layout: default
title: "Horizon Summary: 2026-10-09 (EN)"
date: 2026-10-09
lang: en
---

> From 137 items, 14 important content pieces were selected

---

**Technology News**
1. [OpenAI withdraws three mathematical results](#item-tech-news-1) ⭐️ 7.0/10
2. [Let&\#x27;s Encrypt cuts certificate lifetimes to 64 days starting February 2027](#item-tech-news-2) ⭐️ 7.0/10
3. [Amazon Replaces Fire Tablets with Google-Certified Alexa Tablets](#item-tech-news-3) ⭐️ 7.0/10
4. [Amazon builds 1,000th satellite, readies space internet launch](#item-tech-news-4) ⭐️ 7.0/10
5. [Nvidia&\#x27;s big bet on physical AI aims for safer robotaxis, humanoid robots](#item-tech-news-5) ⭐️ 7.0/10
6. [Anthropic launches free OSS Scanner for open-source security](#item-tech-news-6) ⭐️ 7.0/10
7. [Fired OpenAI safety researchers dispute misconduct claims, warn of chilling effect](#item-tech-news-7) ⭐️ 7.0/10
8. [Google adds agentic AI capabilities to Gemini for businesses](#item-tech-news-8) ⭐️ 7.0/10
9. [Anthropic announces effort to defend infrastructure and open-source projects from AI attacks](#item-tech-news-9) ⭐️ 7.0/10
10. [Nvidia dreamDojo paper accepted as ICML spotlight despite reported bugs](#item-tech-news-10) ⭐️ 7.0/10
11. [ThinkingBox: Solving an agent task once vs. solving it 20/20: 507 stateful workflows graded on terminal database state \[R\]](#item-tech-news-11) ⭐️ 7.0/10
12. [China&\#x27;s Speed-First AI Safety Regime: Why Beijing Won&\#x27;t Slow Frontier Development](#item-tech-news-12) ⭐️ 6.0/10

**Financial News**
1. [S&amp;P sees China&\#x27;s property slump nearing an end by 2028](#item-finance-news-1) ⭐️ 7.0/10
2. [Huawei refocuses on smartphones as EV deliveries drop 29%](#item-finance-news-2) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [OpenAI withdraws three mathematical results](https://twitter.com/danintheory/status/2108065033070789090) ⭐️ 7.0/10

OpenAI withdrew three mathematical results from its AI-generated proofs repository, prompting expert discussion about the reliability and verification of LLM-produced mathematical claims.

hackernews · sashank\_1509 · Oct 8, 07:05 · [Discussion](https://news.ycombinator.com/item?id=50002650)

**Tags**: `#AI`, `#formal-verification`, `#LLM-limitations`, `#mathematics`, `#scientific-integrity`

---

<a id="item-tech-news-2"></a>
### [Let&\#x27;s Encrypt cuts certificate lifetimes to 64 days starting February 2027](https://arstechnica.com/gadgets/2026/10/lets-encrypt-cuts-certificate-lifetimes-to-64-days-starting-february-2027/) ⭐️ 7.0/10

Let&\#x27;s Encrypt will reduce free SSL/TLS certificate lifetimes from 90 days to 64 days beginning February 10, 2027, continuing its long-running push toward shorter certificate validity periods. Administrators using modern ACME clients that support ACME Renewal Information \(ARI\) should see seamless renewals, while those relying on hardcoded schedules \(such as scripts that trigger at fixed offsets like &quot;60 days before expiration&quot;\) must update before the deadline or risk unexpected expirations. Let&\#x27;s Encrypt will begin opt-in testing of the 64-day certificates on October 14 so operators can validate their setups ahead of the production change. The reduction further limits the damage window from compromised or mis-issued private keys, and Let&\#x27;s Encrypt plans to shorten defaults to 45 days in 2028 as browser-side maximum validity rules continue to tighten.

rss · Ars Technica · Oct 8, 19:57

**「Background」** Before Let&\#x27;s Encrypt launched in early 2016, SSL/TLS certificates from commercial authorities were typically issued with lifetimes of one to three years, and many servers relied on manual or scripted renewal processes rather than automation. Let&\#x27;s Encrypt introduced the Automated Certificate Management Environment \(ACME\) protocol and started issuing certificates with a 90-day lifetime specifically to force administrators to adopt automated renewal, since shorter validity limits the window of exposure if a private key is stolen or a certificate is misissued. ACME Renewal Information \(ARI\) is an extension that lets the certificate authority tell the client when it should renew, removing the need for hardcoded offsets such as &quot;60 days before expiration&quot; and enabling even shorter certificate lifetimes going forward.

**「Impact」** Administrators relying on hardcoded renewal intervals \(e.g., &quot;60 days before expiration&quot; cron jobs\) or manual certificate processes must migrate to ACME clients supporting ACME Renewal Information \(ARI\) before February 10, 2027, or risk unexpected certificate expirations on Let&\#x27;s Encrypt-issued certificates. This change aligns with the broader CA/Browser Forum schedule that ultimately caps TLS certificate lifetimes at 47 days by 2029, meaning certificate lifetime reductions will continue to pressure any remaining non-automated renewal workflows.

<details><summary>References</summary>
<ul>
<li><a href="https://arstechnica.com/gadgets/2026/10/lets-encrypt-cuts-certificate-lifetimes-to-64-days-starting-february-2027/">Let &#x27; s Encrypt cuts certificate lifetimes to 64 days ... - Ars Technica</a></li>
<li><a href="https://letsencrypt.org/2026/10/07/64-day-certs">64 - Day Certificate Lifetimes Coming Feb 2027 - Let &#x27; s Encrypt</a></li>
<li><a href="https://www.geekslop.com/technology-articles/computers-programming/hacking-and-security-technology-articles/2026/lets-encrypt-64-day-ssl-certs">Let &#x27; s Encrypt Cuts SSL Cert Lifetimes To 64 Days ... - Geek Slop</a></li>
<li><a href="https://www.digicert.com/blog/tls-certificate-lifetimes-will-officially-reduce-to-47-days">TLS Certificate Lifetimes Will Officially Reduce to 47 Days | DigiCert</a></li>

</ul>
</details>

**Tags**: `#TLS/SSL`, `#certificates`, `#security`, `#infrastructure`, `#DevOps`

---

<a id="item-tech-news-3"></a>
### [Amazon Replaces Fire Tablets with Google-Certified Alexa Tablets](https://arstechnica.com/gadgets/2026/10/amazons-new-alexa-tablets-drop-the-fire-branding-but-are-more-android-than-ever/) ⭐️ 7.0/10

Amazon has retired its 15-year-old Fire Tablet lineup and rebranded its tablets as Alexa Tablets, marking a strategic reversal in which the devices are now Google-certified Android tablets with full Play Store access rather than running the company&\#x27;s long-standing forked Fire OS. The shift follows Amazon&\#x27;s shutdown of its Appstore last year, which had been the sole app source for Fire tablets, and it stands in sharp contrast to the Fire TV Stick&\#x27;s move in the opposite direction onto Amazon&\#x27;s custom Linux-based Vega OS. The new lineup comprises three redesigned unibody aluminum devices: the $230 Alexa Tablet 8 and $330 Tablet 11, both with 16:10 displays on a MediaTek 8189 processor, and the $500 Tablet 12 Pro, which uses a MediaTek Dimensity 8400 with 8GB of RAM, 128GB of storage, a 3:2 2800×1840 120Hz display at 500 nits peak brightness, plus optional $50 matte display, $150 keyboard, and $90 stylus accessories.

rss · Ars Technica · Oct 8, 16:32

**「Background」** Fire OS is Amazon&\#x27;s custom Android fork that powered Kindle Fire and Fire Tablet devices since 2011, running Android apps exclusively through Amazon&\#x27;s own Appstore while stripping out Google services. The decision to abandon that approach for tablets comes after Amazon shut down its Appstore last year, eliminating the curated app ecosystem that defined Fire devices for over a decade. Meanwhile, Amazon has been pushing its Fire TV Sticks in the opposite direction, moving them off Android onto the internally developed Linux-based Vega OS.

**「Impact」** Existing Fire tablet buyers and prospective customers gain access to the full Google Play Store and standard Android app catalog, ending the long-standing Appstore-only limitation that defined Amazon&\#x27;s tablets. The simultaneous divergence of Fire Sticks onto Vega OS means Amazon&\#x27;s hardware now spans two opposite operating-system philosophies depending on device category.

**Tags**: `#hardware`, `#android`, `#amazon`, `#consumer-electronics`, `#ecosystem-strategy`

---

<a id="item-tech-news-4"></a>
### [Amazon builds 1,000th satellite, readies space internet launch](https://arstechnica.com/space/2026/10/amazon-builds-1000th-satellite-is-weeks-away-from-space-internet-rollout/) ⭐️ 7.0/10

Amazon has manufactured its 1,000th satellite at its Kirkland, Washington factory for the Amazon Leo broadband constellation and is weeks away from offering its first commercial service, according to senior company officials speaking with Ars Technica. The debut marks Amazon&\#x27;s entry into a low-Earth orbit broadband market that SpaceX&\#x27;s Starlink has dominated for roughly five years, with OneWeb having offered only limited services, leaving Amazon as the only real global competitor. Amazon, now the world&\#x27;s second-largest satellite manufacturer behind SpaceX, is producing a handful of satellites per day, and the upcoming Vulcan rocket return-to-flight mission will carry the first Amazon Leo satellites, with a second Vulcan already being prepared for additional launches this year. The project is led by Rajeev Badyal, who previously led Starlink during its early years before being fired by Elon Musk roughly eight years ago, alongside production director Paul Palcisco and business VP Chris Weber. Interest in the service extends beyond consumers to airlines, shipping companies, and government customers seeking broadband for applications ranging from commerce to warfighting.

rss · Ars Technica · Oct 8, 15:28

**「Background」** Low-Earth orbit satellite constellations deliver broadband internet from space, a market pioneered commercially by SpaceX&\#x27;s Starlink beginning around 2019–2020 and since expanded globally. Amazon has been developing its Kuiper constellation, now branded Amazon Leo, for nearly a decade, positioning it as the first credible global challenger to Starlink. Amazon&\#x27;s hiring of former Starlink leader Rajeev Badyal to head the program has been a notable signal of its competitive ambitions in this space.

**「Impact」** For consumers, airlines, shipping companies, and governments seeking low-Earth orbit broadband, Amazon Leo&\#x27;s imminent commercial debut provides the first large-scale alternative supplier to SpaceX&\#x27;s Starlink, while OneWeb remains a smaller option with limited service. The near-term rollout will rely on United Launch Alliance Vulcan rockets, making Vulcan&\#x27;s return-to-flight schedule a pacing factor for Amazon&\#x27;s constellation deployment.

**Tags**: `#satellite-internet`, `#space-tech`, `#broadband-infrastructure`, `#amazon`, `#leo-constellation`

---

<a id="item-tech-news-5"></a>
### [Nvidia&\#x27;s big bet on physical AI aims for safer robotaxis, humanoid robots](https://arstechnica.com/ai/2026/10/nvidias-big-bet-on-physical-ai-aims-for-safer-robotaxis-humanoid-robots/) ⭐️ 7.0/10

Nvidia has expanded its Halos full-stack safety system from autonomous vehicles into broader robotics with &quot;Halos for Robotics,&quot; announced in June 2026, targeting warehouse autonomous mobile robots, humanoid robots, and surgical robots. Amit Goel, Nvidia&\#x27;s head of robotics ecosystem and edge computing, framed safety as &quot;the next bottleneck&quot; now that AI models and robot hardware are maturing, and the system is anchored on hardware like the Nvidia IGX Thor computing module, which dedicates an independent processor to safety workloads running on the same silicon as the functional system. The push follows CEO Jensen Huang&\#x27;s March 2026 All-In Podcast claim that physical AI is already driving nearly $10 billion in annual revenue, having been promoted to Nvidia&\#x27;s second-most important growth category in 2025. Nvidia has also invested directly in humanoid robotics startups including Agility Robotics and Figure AI and partnered with Unitree on an open humanoid robot reference design for researchers.

rss · Ars Technica · Oct 8, 11:15

**「Background」** Nvidia&\#x27;s physical AI business refers to AI systems that operate in the real world through robots, autonomous vehicles, and other machines, as distinguished from purely digital AI applications. The company&\#x27;s Halos safety system debuted in 2025 as a full-stack solution, combining hardware and software, to help autonomous vehicle developers implement guardrails against harmful behavior. Halos for Robotics, announced in June 2026, extends that same architecture to industrial robots, autonomous mobile robots, and humanoid platforms, reflecting Nvidia&\#x27;s bet that safety certification will become the gating constraint as AI models and robot hardware reach commercial maturity.

**「Impact」** Robotics companies and developers building humanoid, warehouse, or surgical robots gain an integrated hardware-plus-software safety framework they can build upon, potentially accelerating commercial deployment of physical AI systems while addressing regulatory and public safety concerns.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/inside-nvidia-halos-for-robotics-a-full-stack-functional-safety-system-for-physical-ai/">Inside NVIDIA Halos for Robotics : A Full-Stack Functional Safety ...</a></li>
<li><a href="https://arstechnica.com/ai/2026/10/nvidias-big-bet-on-physical-ai-aims-for-safer-robotaxis-humanoid-robots/">Nvidia &#x27;s big bet on physical AI aims for safer robotaxis, humanoid ...</a></li>

</ul>
</details>

**Tags**: `#AI safety`, `#robotics`, `#Nvidia`, `#autonomous vehicles`, `#industry strategy`

---

<a id="item-tech-news-6"></a>
### [Anthropic launches free OSS Scanner for open-source security](https://www.theverge.com/ai-artificial-intelligence/1008521/anthropic-open-source-oss-scanner) ⭐️ 7.0/10

Anthropic has launched OSS Scanner, a free service that uses its Claude models to periodically scan opt-in open-source projects for security vulnerabilities. Reports are generated by Claude rather than manually reviewed, and include vulnerability reproduction steps, descriptions, and patch suggestions when possible, though Anthropic notes they may contain errors. According to Anthropic, its scanning work over the past six months has surfaced more than 29,000 candidate vulnerabilities, of which roughly 6,000 were manually reviewed, and 85 out of 97 high- or critical-severity findings from early testing met its disclosure process requirements. Core maintainers of eligible projects can apply to participate by submitting a GitHub pull request to opt in.

rss · The Verge · Oct 8, 21:53

**「Background」** Open-source software underpins much of the modern software supply chain, but individual projects often lack dedicated security staff or budgets for continuous vulnerability scanning. AI-assisted code and vulnerability analysis has been an emerging application of large language models, with vendors increasingly packaging models as automated review or auditing services. OSS Scanner applies it to repositories themselves rather than to code written by a single developer.

**「Impact」** Eligible open-source maintainers can gain free, model-driven periodic vulnerability reports on their projects, potentially catching issues earlier, but the findings are unverified by human reviewers and may include false positives that require careful triage.

**Tags**: `#AI`, `#open-source`, `#security`, `#developer-tools`, `#Anthropic`

---

<a id="item-tech-news-7"></a>
### [Fired OpenAI safety researchers dispute misconduct claims, warn of chilling effect](https://techcrunch.com/2026/10/08/fired-openai-safety-researchers-dispute-misconduct-claims-warn-of-chilling-effect/) ⭐️ 7.0/10

Three former OpenAI safety researchers publicly disputed allegations of mishandling sensitive information in an open letter, challenging the misconduct claims that the company cited as grounds for their dismissals. The researchers warned that their firings are creating a chilling effect on OpenAI&\#x27;s AI safety culture, potentially discouraging internal safety work and how safety concerns are raised within the company. The coordinated public pushback from a group of former safety staff represents an unusual public dispute between members of a frontier AI lab&\#x27;s safety team and its management. The story was reported by TechCrunch&\#x27;s Rebecca Bellan on October 8, 2026, and raises broader questions for the AI governance community about how safety-related personnel disputes are handled at major labs.

rss · TechCrunch · Oct 8, 20:04

**「Background」** OpenAI has faced repeated departures of safety-focused researchers since 2023, when figures such as co-founder Ilya Sutskever and alignment team co-leader Jan Leike publicly raised concerns that safety work was being deprioritized against commercial pressures. The three dismissed researchers identified in the open letter — Jasmine Wang, Tomek Korbak, and Mikita Balesni — specifically deny leaking information to The Information and ask OpenAI to honor prior public commitments to embed third-party safety auditors and preserve model monitorability. OpenAI has not formally responded to the letter, though an internal memo attributed to a research leader praises the three researchers&\#x27; contributions to AI safety and denies that the terminations were retaliatory.

**「Impact」** Public allegations of a chilling effect on safety culture from dismissed researchers could intensify external scrutiny of OpenAI&\#x27;s internal governance and its handling of safety-related whistleblower concerns from AI safety staff and policy observers.

<details><summary>References</summary>
<ul>
<li><a href="https://techcrunch.com/2026/10/08/fired-openai-safety-researchers-dispute-misconduct-claims-warn-of-chilling-effect/">Fired OpenAI safety researchers dispute misconduct claims , warn...</a></li>
<li><a href="https://chang.aevumnews.com/en/openai-ex-safety-researchers-challenge-misconduct-claims-allege-chilling-effect">OpenAI Ex- Safety Researchers Challenge Misconduct Claims ...</a></li>
<li><a href="https://fourweekmba.com/ai-fired-openai-safety-researchers-deny-leak-in-open-letter/">Fired OpenAI Safety Researchers Deny Leak in Open Letter</a></li>

</ul>
</details>

**Tags**: `#AI safety`, `#OpenAI`, `#AI governance`, `#industry news`, `#workplace culture`

---

<a id="item-tech-news-8"></a>
### [Google adds agentic AI capabilities to Gemini for businesses](https://techcrunch.com/2026/10/08/google-brings-agentic-ai-to-gemini-starting-with-businesses/) ⭐️ 7.0/10

Google is equipping Gemini with agentic AI capabilities, starting with business users, enabling the assistant to plan and execute tasks across business apps and systems. The agent can delegate work to subagents and orchestrate multiple AI models rather than relying on a single model. It also operates with a dedicated workplace identity, including an email address, allowing it to act on behalf of a user within enterprise environments. The rollout begins with businesses, positioning Gemini as an agentic platform for enterprise workflows.

rss · TechCrunch · Oct 8, 18:18

**「Background」** Agentic AI refers to AI systems that can autonomously plan multi-step tasks, invoke tools, and take actions across software systems rather than just generating text in response to a prompt. A common pattern in this space is multi-agent orchestration, where a primary agent delegates subtasks to specialized subagents and may route work across multiple underlying AI models, allowing different reasoning capabilities or model strengths to be combined for a single workflow. Giving these agents a distinct workplace identity, such as an email address, lets them act on behalf of an organization in tools like calendars, email, and business apps while keeping their actions attributable and auditable.

**「Why it matters」** Gemini is shifting from a conversational assistant into an autonomous enterprise agent capable of planning multi-step work, orchestrating subagents, and accessing business systems under its own workplace identity, which positions Google to compete directly with other agentic enterprise platforms. The shift introduces operational and governance risks for businesses, since delegating tasks to an agent that acts across apps and carries an identity could expand automation scope faster than enterprise access controls and audit practices are ready for.

<details><summary>References</summary>
<ul>
<li><a href="https://techcrunch.com/2026/10/08/google-brings-agentic-ai-to-gemini-starting-with-businesses/">Google brings agentic AI to Gemini , starting with... | TechCrunch</a></li>
<li><a href="https://cloud.google.com/blog/products/ai-machine-learning/welcome-to-gemini-at-work-2026">Gemini at Work 2026: Introducing Gemini agent | Google Cloud Blog</a></li>
<li><a href="https://antigravity.google/">Google Antigravity</a></li>

</ul>
</details>

**Tags**: `#agentic AI`, `#Google Gemini`, `#enterprise AI`, `#AI agents`, `#multi-agent systems`

---

<a id="item-tech-news-9"></a>
### [Anthropic announces effort to defend infrastructure and open-source projects from AI attacks](https://www.theregister.com/ai-and-ml/2026/10/09/ai-company-moves-to-defend-critical-infrastructure-and-open-source-projects-from-ai/5302128) ⭐️ 7.0/10

Anthropic has announced efforts to defend critical infrastructure and open-source projects from AI-powered attacks, according to The Register. The company projects that attackers will hold the advantage for at least the next two years, framing the period as one in which defensive postures must be built up against offensive AI use. The initiative targets two distinct areas: safeguarding critical infrastructure systems and protecting open-source software ecosystems from AI-enabled threats. Anthropic, as a major AI lab, is taking a proactive stance on how its own technology category may be weaponized against foundational systems. The available reporting does not detail the specific technical mechanisms, partner organizations, or funding commitments behind the effort.

rss · The Register · Oct 8, 23:57

**「Background」** Anthropic is a San Francisco-based AI safety company known for its Claude family of large language models. Critical infrastructure encompasses essential systems such as power grids, water supplies, and other utilities that are increasingly targeted by sophisticated cyberattacks, while open-source software projects are publicly available codebases that can contain unpatched vulnerabilities exploitable by adversaries. The emerging use of AI to automate the discovery and exploitation of software flaws has raised concerns that defenders are falling behind attackers, a gap Anthropic is now attempting to address.

**「Impact」** Operators of critical infrastructure such as power grids, water utilities, and transportation systems gain access to Anthropic&\#x27;s frontier AI models and engineering support through its new Critical Infrastructure Defense Program, which also extends protective efforts to open-source projects. The full defensive benefit remains uncertain because Anthropic itself projects that AI-enabled attackers will hold the advantage over defenders for that period.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Anthropic">Anthropic - Wikipedia</a></li>
<li><a href="https://www.anthropic.com/news/anthropic-cyber-mission">Introducing the Anthropic Cyber Mission \ Anthropic</a></li>
<li><a href="https://www.axios.com/2026/10/08/anthropic-critical-infrastructure-cybersecurity">Anthropic launches AI push to protect critical infrastructure</a></li>
<li><a href="https://www.axios.com/2026/10/08/anthropic-critical-infrastructure-cybersecurity">Anthropic launches AI push to protect critical infrastructure</a></li>
<li><a href="https://www.anthropic.com/news/anthropic-cyber-mission">Introducing the Anthropic Cyber Mission \ Anthropic</a></li>

</ul>
</details>

**Tags**: `#AI Security`, `#Critical Infrastructure`, `#Open Source`, `#Cybersecurity`, `#Anthropic`

---

<a id="item-tech-news-10"></a>
### [Nvidia dreamDojo paper accepted as ICML spotlight despite reported bugs](https://www.reddit.com/r/MachineLearning/comments/1x0i6b5/nvidias_erroneous_paper_accepted_as_icmls/) ⭐️ 7.0/10

A Reddit post alleges that Nvidia&\#x27;s dreamDojo robotics world model paper, accepted as an ICML spotlight, contains serious bugs in its released code that affect pre-training, post-training, and evaluation. The paper reports only a marginal ~0.5 dB PSNR improvement over the prior Cosmos 2.5 baseline despite training on roughly 44,000 hours of human data plus additional robot data using 256 H100 GPUs, which the poster considers a disproportionately small gain for the resources invested. During an attempted reproduction using Nvidia&\#x27;s released GR1 data, the poster and a colleague reportedly identified a bug in the post-training code with the help of Claude, and two further pre-training bugs were already filed on the project&\#x27;s GitHub issues. The source code is publicly available but the underlying datasets are not open-sourced, and the poster questions how such well-known authors and the ICML reviewers did not notice the errors before acceptance. The episode is being framed by the poster as evidence of weak peer-review rigor for large-scale, foundation-model papers that report only incremental improvements.

reddit · r/MachineLearning · /u/Amazing-Fox-7295 · Oct 8, 04:58

**「Background」** ICML \(International Conference on Machine Learning\) is one of the premier peer-reviewed venues in machine learning, and a &quot;spotlight&quot; designation is reserved for a limited fraction of accepted papers that reviewers flag as particularly noteworthy, typically representing roughly the top 5% of submissions. World models in robotics are generative systems trained to simulate how environments evolve in response to actions, enabling policy learning, planning, and synthetic data generation without real-world interaction. DreamDojo is Nvidia&\#x27;s extension of its Cosmos foundation model family, applying a two-stage recipe \(pre-training on large-scale human video followed by post-training on robot embodiment data\) to produce a generalist robotics world model, with PSNR \(peak signal-to-noise ratio\) used as a standard image-fidelity metric to quantify how closely generated frames match ground-truth frames.

**「Impact」** If the alleged code bugs are confirmed, the reported state-of-the-art claims for dreamDojo would not be reproducible, undermining trust in the ICML spotlight result and likely prompting closer scrutiny of future large-compute, proprietary-data foundation model submissions with only marginal reported gains.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/NVIDIA/DreamDojo">GitHub - NVIDIA / DreamDojo : Official Codebase for &quot; DreamDojo ...&quot;</a></li>
<li><a href="https://huggingface.co/nvidia/DreamDojo">nvidia / DreamDojo · Hugging Face</a></li>
<li><a href="https://dreamdojo-world.github.io/">DreamDojo : A Generalist Robot World Model from Large-Scale Human...</a></li>

</ul>
</details>

**Tags**: `#reproducibility`, `#peer-review`, `#world-models`, `#robotics`, `#nvidia`

---

<a id="item-tech-news-11"></a>
### [ThinkingBox: Solving an agent task once vs. solving it 20/20: 507 stateful workflows graded on terminal database state \[R\]](https://www.reddit.com/r/MachineLearning/comments/1x17shf/thinkingbox_solving_an_agent_task_once_vs_solving/) ⭐️ 7.0/10

Microsoft researchers introduce ThinkingBox-Bench, a 507-task, 5-domain benchmark showing that AI agents&\#x27; single-run success rates poorly predict actual terminal-state correctness across 10,140 trials per model.

reddit · r/MachineLearning · /u/tuhin\_k · Oct 9, 00:50

**Tags**: `#AI-agents`, `#agent-evaluation`, `#benchmark`, `#LLM-reliability`, `#Microsoft-Research`

---

<a id="item-tech-news-12"></a>
### [China&\#x27;s Speed-First AI Safety Regime: Why Beijing Won&\#x27;t Slow Frontier Development](https://newsletter.semianalysis.com/p/beijing-will-not-pace-the-frontier) ⭐️ 6.0/10

SemiAnalysis has published an analysis arguing that Beijing will not slow frontier AI development in the name of safety, framing China&\#x27;s approach as a &\#x27;speed-first&\#x27; AI safety regime rather than one modeled on precautionary Western pacing proposals. The piece, authored by Mark Chen, situates China&\#x27;s regulatory posture as prioritizing rapid frontier advancement, a stance that has implications for how global AI safety norms, export controls, and competitive dynamics between leading labs may evolve. The analysis is relevant to AI policy and geopolitics because divergent US and Chinese philosophies on safety-versus-speed could shape international standards and the strategic environment for frontier model development. Because the supplied source content is limited to a brief teaser \(&\#x27;AI safety is on fire&\#x27;\), the specific regulatory mechanisms, technical claims, named policies, dates, and quantitative evidence cited in the full article cannot be verified from this excerpt alone. Readers should consult the full SemiAnalysis piece for the substantive arguments, named actors, and data underlying the &\#x27;speed-first&\#x27; characterization.

rss · Semianalysis · Oct 8, 17:46

**「Background」** On 12 September 2026, Anthropic CEO Dario Amodei published an essay calling on frontier AI labs to deliberately slow the pace at which they improve model capabilities, framing safety as a matter of pacing frontier development. This call coincided with heightened US-China AI competition, including a September 2026 Trump-Xi meeting where US Treasury Secretary Scott Bessent proposed a bilateral AI safety mechanism with Chinese vice-premier He Lifeng, though the proposal stopped short of a major formal safety agreement.

**「Impact」** If the analysis&\#x27;s core thesis holds, Western policymakers and frontier AI labs should not assume Chinese domestic safety regulation will moderate the pace of competitor model development, increasing pressure on US governance, investment, and compute-strategy decisions.

<details><summary>References</summary>
<ul>
<li><a href="https://newsletter.semianalysis.com/p/beijing-will-not-pace-the-frontier">Beijing Will Not Pace the Frontier : China ’s Speed - First AI Safety ...</a></li>
<li><a href="https://www.theguardian.com/us-news/2026/sep/23/trump-xi-ai-trade-geopolitics">AI looms large over Trump-Xi meeting amid deep... | The Guardian</a></li>

</ul>
</details>

**Tags**: `#AI policy`, `#AI safety`, `#China`, `#geopolitics`, `#regulation`

---

## Financial News

<a id="item-finance-news-1"></a>
### [S&amp;P sees China&\#x27;s property slump nearing an end by 2028](https://www.cnbc.com/2026/10/08/chinas-real-estate-market-may-be-set-for-a-turnaround-sp-says.html) ⭐️ 7.0/10

S&amp;P Global Ratings forecasts that China&\#x27;s yearslong residential property slump may bottom in the third quarter of 2028, with prices in major cities like Beijing and Shanghai potentially recovering as soon as 2027.

rss · CNBC Finance · Oct 8, 09:27

**「Background」** Chinese home prices have already fallen 22% from their 2021 peak following a debt-driven developer cycle and chronic oversupply, and S&amp;P says new policies — restrictions on developers selling unfinished homes and mortgage subsidies for first-time buyers of units under 1.5 million yuan \(about $220,000\) — have improved its outlook since February, when it judged a recovery was &quot;out of reach.&quot;

**「Impact」** Developers are expected to scale back land purchases and new projects to reduce oversupply, while Morgan Stanley analyst Stephen Cheung argues the mortgage subsidy will mostly pull forward planned purchases rather than create new demand.

**Tags**: `#China economy`, `#real estate`, `#S&amp;P forecast`, `#property policy`, `#global markets`

---

<a id="item-finance-news-2"></a>
### [Huawei refocuses on smartphones as EV deliveries drop 29%](https://www.cnbc.com/2026/10/08/huawei-china-smartphone-ev-slow.html) ⭐️ 7.0/10

Huawei launched its Mate 90 series on Oct. 1, 2026 using a homegrown &quot;LogicFolding&quot; chip, as the company refocuses on smartphones while deliveries of Huawei-powered vehicles through its HIMA auto tech system fell 29% year-on-year in September—the third straight monthly decline—against a Chinese auto market down more than 20% year-to-date per the China Passenger Car Association.

rss · CNBC Finance · Oct 8, 08:04

**「Background」** U.S. restrictions from 2019 cut Huawei off from Google&\#x27;s Android and TSMC-made chips, halving its consumer business to about $34 billion in 2021 before it recovered to roughly $51 billion \(39% of revenue\) in 2025; the company now sells only several million smartphones outside China each year, down from over 240 million units at its peak.

**「Why it matters」** The EV slowdown has hit partners directly: Seres, which manufactures the Aito line with Huawei, has seen Shanghai-listed shares drop more than 60% year-to-date, prompting Huawei to extend its Seres cooperation by another five years announced Oct. 1.

**Tags**: `#Huawei`, `#smartphones`, `#China EV market`, `#semiconductors`, `#corporate strategy`

---