---
layout: default
title: "Horizon Summary: 2026-11-11 (EN)"
date: 2026-11-11
lang: en
---

> From 122 items, 18 important content pieces were selected

---

**Technology News**
1. [AlphaProof Code Verifies Signal Protocol Implementation](#item-tech-news-1) ⭐️ 8.0/10
2. [AMD Zen 6’s Core, Memory, and I/O Trade-Offs](#item-tech-news-2) ⭐️ 8.0/10
3. [Grok Build Links Expose Thousands of Users’ Data](#item-tech-news-3) ⭐️ 8.0/10
4. [Nvidia has a Jensen Huang problem—and no obvious successor](#item-tech-news-4) ⭐️ 8.0/10
5. [N-able Takes Remote Access Service Offline After Zero-Day Disclosures](#item-tech-news-5) ⭐️ 8.0/10
6. [Git Releases Fixes for Six Security Vulnerabilities](#item-tech-news-6) ⭐️ 8.0/10
7. [Gemini 4 Carbon Expands Access for Complex AI Work](#item-tech-news-7) ⭐️ 8.0/10
8. [DeepMind Unveils Gemini Robotics 2.5 and ASIMOV-jailbreak](#item-tech-news-8) ⭐️ 7.5/10
9. [Synaptics Patent Claims Halt DisplayLink Driver Work](#item-tech-news-9) ⭐️ 7.0/10
10. [Modern Web Guidance Teaches Coding Agents Native Browser APIs](#item-tech-news-10) ⭐️ 7.0/10
11. [Meta launches Muse Ember for efficient agent tasks](#item-tech-news-11) ⭐️ 7.0/10
12. [Pentagon backs launch rivals as Falcon retirement approaches](#item-tech-news-12) ⭐️ 7.0/10
13. [Oura to Acquire Counsel Health for $625 Million](#item-tech-news-13) ⭐️ 7.0/10
14. [New York AI Safety Law Brings OpenAI and Anthropic Under Oversight](#item-tech-news-14) ⭐️ 7.0/10
15. [llm-gemini 0.36 Adds Gemini 4 Carbon](#item-tech-news-15) ⭐️ 6.0/10
16. [Ownership Framing Boosts Claude Refactoring](#item-tech-news-16) ⭐️ 6.0/10

**Financial News**
1. [Polymarket says annualized revenue has topped $1.8 billion](#item-finance-news-1) ⭐️ 8.0/10
2. [Waller leans toward December rate hike](#item-finance-news-2) ⭐️ 8.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [AlphaProof Code Verifies Signal Protocol Implementation](https://deepmind.google/blog/introducing-alphaproof-code/) ⭐️ 8.0/10

Google DeepMind says AlphaProof Code, a multi-agent framework powered by Gemini Carbon, formally verified security properties of Signal’s compiled cryptographic protocol implementation down to the code running on devices. Researchers and models translated Signal’s security goals into Lean specifications that humans reviewed, after which agents generated more than six million lines of Lean proofs and flagged about 1% of the codebase for closer human examination. The four-week effort proved selected properties, including protection of messages before and after a device is temporarily compromised, and the system also generated machine-checked proofs that two isolated versions with reintroduced historical bugs were insecure. This advances implementation-level verification beyond design-level protocol analysis, but the guarantees remain limited to the security properties and specifications chosen by the researchers rather than establishing that the code is bug-free.

rss · DeepMind Blog · Nov 10, 12:02 · [Discussion](https://news.ycombinator.com/item?id=50439193)

**「Background」** ... 

**「Impact」** For Signal users and maintainers, AlphaProof Code provides machine-checked assurance that the compiled libsignal implementation satisfies specified security properties, including protecting messages before and after temporary device compromise. For cryptographic software teams, the open-sourced proof artifacts and four-week AI-assisted workflow offer a reusable path toward implementation-level verification, though they do not establish that Signal as a whole is bug-free or guarantee properties outside the reviewed specification.

**「Community Reaction」** Commenters welcomed the practical use of AI for formal verification but questioned whether the theorems were correctly scoped, whether the human-defined specifications captured the intended behavior, and whether AI-generated Lean might conceal errors or loopholes. Some saw verification of the implementation rather than the protocol specification as the central advance, while others expressed optimism that rigorously verified software could become standard practice.

<details><summary>References</summary>
<ul>
<li><a href="https://deepmind.google/blog/introducing-alphaproof-code/">Formal Verification of Signal’s Protocol with Gemini</a></li>
<li><a href="https://adtmag.com/articles/2026/11/10/google-uses-ai-agents-to-verify-signal-code.aspx">Google Uses AI Agents to Verify Signal Code, Keeping ...</a></li>
<li><a href="https://deepmind.google/blog/introducing-alphaproof-code/">Formal Verification of Signal’s Protocol with... — Google DeepMind</a></li>
<li><a href="https://google-deepmind.github.io/code-verification/">AlphaProof Code : Verifying Signal’s Security at the Machine- Code ...</a></li>
<li><a href="https://shiftdelete.net/en/alphaproof-code">AlphaProof Code Verifies Signal Encryption at Machine Level</a></li>

</ul>
</details>

**Tags**: `#AI-assisted formal verification`, `#software security`, `#cryptography`, `#theorem proving`, `#Signal protocol`

---

<a id="item-tech-news-2"></a>
### [AMD Zen 6’s Core, Memory, and I/O Trade-Offs](https://chipsandcheese.com/p/amds-zen-6-family-feeding-the-beast) ⭐️ 8.0/10

The article examines AMD’s Zen 6 CPU family, focusing on trade-offs in the core, memory controller, and I/O chiplet, including branch prediction, vector execution, and memory and I/O behavior. Reported headline configurations reach up to 256 cores and 5.3 GHz, with claimed IPC gains of 20% to 31%, although those maxima are not available on the same SKU. The analysis presents Zen 6 as a balancing exercise rather than a simple expansion of resources, with discussion pointing to two-ahead branch prediction, four vector loads per cycle at 256 bits or less, and reductions in integer multiply and PDEP/PEXT throughput. For AM5 users, an anticipated smaller-node I/O chiplet and improved memory controller are especially significant because existing Zen 4 and Zen 5 systems reportedly struggle to exceed 3600 MT/s when both memory channels are active.

hackernews · pixelpoet · Nov 10, 17:02 · [Discussion](https://news.ycombinator.com/item?id=50443090)

**「Zen 6 architectural context」** Zen 6 continues AMD’s chiplet-based CPU design, grouping compute cores and cache into Core Chiplet Dies while providing memory and I/O functions on separate chiplets; it follows the broad architectural direction established in Zen 4 and Zen 5. AMD distinguishes standard Zen 6 from the denser Zen 6c variant, and early server implementations are associated with the EPYC “Venice” generation, larger per-core L3 caches, a wider execution window, and PCIe 6.0 support. This lineage and variant split provide the baseline for evaluating the changes to Zen 6’s execution cores, memory controller, and I/O chiplet.

**「Practical impact」** AMD says Zen 6-based EPYC Venice offers 20%–31% higher IPC and configurations with up to 256 cores and 5.3 GHz clocks, potentially increasing compute density for data-center workloads. Because those peak figures are not combined on the same SKU, server buyers must compare the workload-relevant core count, clock speed, and IPC of individual processors.

**「Community Reaction」** Commenters generally view Zen 6 as a set of balanced core improvements and consider its 32-core C-core chiplet and larger L3 cache particularly noteworthy. The main practical concern is AM5 memory performance, while unresolved questions involve gather throughput, the reasons for reducing integer multipliers, the relationship between multiply and PDEP/PEXT circuitry, and whether users must manage 32-core chiplets as the lowest practical NUMA grouping.

<details><summary>References</summary>
<ul>
<li><a href="https://chipsandcheese.com/p/amds-zen-6-family-feeding-the-beast">AMD’s Zen 6 Family: Feeding the Beast - by George Cozma</a></li>
<li><a href="https://www.techpowerup.com/review/amd-zen-6-technical-deep-dive/">AMD Zen 6 Technical Deep Dive - TechPowerUp</a></li>
<li><a href="https://www.pcmag.com/news/amd-zen-6-architecture-details-epyc-venice-cpus-future-ryzens">AMD&#x27;s &#x27;Zen 6&#x27; Architecture Detailed: EPYC Data Center Chips ...</a></li>
<li><a href="https://www.theregister.com/systems/2026/11/10/amd-winds-up-zen-6-cores-for-faster-clock-speeds/5308603">AMD winds up Zen 6 cores for faster clock speeds - The Register</a></li>
<li><a href="https://wccftech.com/amd-zen-6-architecture-ipc-cores-memory-performance-epyc-venice/">AMD Zen 6 Architecture Brings A Phenomenal 27% IPC Increase ...</a></li>
<li><a href="https://tech.yahoo.com/computing/articles/amd-just-unveiled-256-core-170000235.html">AMD Just Unveiled A 256-Core Monster With Its New EPYC Venice ...</a></li>

</ul>
</details>

**Tags**: `#AMD Zen 6`, `#CPU architecture`, `#Memory subsystem`, `#Microarchitecture`, `#Hardware analysis`

---

<a id="item-tech-news-3"></a>
### [Grok Build Links Expose Thousands of Users’ Data](https://arstechnica.com/security/2026/11/grok-build-coding-agent-leaks-oodles-of-confidential-info-some-belonging-to-spacexsi/) ⭐️ 8.0/10

Security researchers at Claroc found that Grok Build’s randomized app-sharing URLs could be enumerated, exposing data from thousands of live projects to anyone who discovered a link. Most exposed pages revealed their associated information, including internal business plans, advertising proposals, medical exam results, cruise galley checklists, and employee names and ID numbers. The flaw also affected 24 apps built by SpaceXSI, containing a confidential sales onboarding plan, a map of 594 accounts, internal sales-tool addresses, and advertising proposals. Claroc’s analysis identified unsafe isolation between applications hosted on a shared origin, where one app’s JavaScript could access another app’s authenticated data rather than relying on a secret URL alone. Claroc notified SpaceXSI on Sunday and escalated publicly; SpaceXSI removed links to all 24 internal apps within hours of Ars Technica’s inquiry, but almost all other exposed data remained available at publication.

rss · Ars Technica · Nov 10, 21:12

**「Background」** ...

**「Impact」** Share-link enumeration allowed anyone who discovered a Grok Build URL to read associated app data, exposing sensitive business, medical, and employee information from thousands of user projects and 24 SpaceXSI apps. SpaceXSI removed the links for its own 24 apps within hours of Ars’ inquiry, but the report does not state when links to affected users’ projects were disabled.

<details><summary>References</summary>
<ul>
<li><a href="https://www.unite.ai/ru/claroc-research-finds-35-578-grok-apps-accessible-without-sign-in/">Исследование Claroc : 35 578 приложений Grok доступны без...</a></li>
<li><a href="https://arstechnica.com/security/2026/11/grok-build-coding-agent-leaks-oodles-of-confidential-info-some-belonging-to-spacexsi/">Grok Build coding agent leaks oodles of confidential info ...</a></li>

</ul>
</details>

**Tags**: `#AI coding agents`, `#application security`, `#data privacy`, `#vulnerability disclosure`, `#Grok Build`

---

<a id="item-tech-news-4"></a>
### [Nvidia has a Jensen Huang problem—and no obvious successor](https://arstechnica.com/gadgets/2026/11/nvidia-has-a-jensen-huang-problem-and-no-obvious-successor/) ⭐️ 8.0/10

Nvidia faces a potential succession crisis as an investigation threatens CEO Jensen Huang and there is no obvious successor for the AI-chip leader.

rss · Ars Technica · Nov 10, 14:53

**Tags**: `#Nvidia`, `#AI semiconductors`, `#executive succession`, `#corporate governance`

---

<a id="item-tech-news-5"></a>
### [N-able Takes Remote Access Service Offline After Zero-Day Disclosures](https://techcrunch.com/2026/11/10/n-able-takes-its-remote-access-service-offline-after-researcher-publishes-dozens-of-zero-day-bugs/) ⭐️ 8.0/10

N-able reportedly took its remote access service offline after a researcher published dozens of zero-day vulnerabilities. The company also urged self-hosted customers to shut down their servers amid what it described as a critical security incident. The action reflects concern that the newly disclosed flaws could be exploited in cyberattacks, although the supplied account does not identify the affected products, vulnerabilities, exploitation status, or restoration timeline.

rss · TechCrunch · Nov 10, 15:45

**「Background」** N-able’s N-central remote access service is available in hosted and customer-operated, on-premises configurations. A zero-day is a vulnerability publicly disclosed before a vendor fix is available; the issues reported here were more than 30 alleged “Able2Shell” flaws said to expose credentials and enable execution with root privileges.

**「Operational and security impact」** N-able hosted N-central users face service disruption, while self-hosted administrators are being urged to keep affected servers offline because newly disclosed critical vulnerabilities could enable credential theft, creation of privileged accounts, or full server compromise. N-able says it has not observed active exploitation, making the shutdown a precautionary containment measure rather than confirmation that every deployment has been breached.

<details><summary>References</summary>
<ul>
<li><a href="https://thehackernews.com/2026/11/n-able-takes-hosted-n-central-offline.html">N-able Takes N-central Cloud Offline After Researcher ...</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/n-able-takes-cloud-platform-offline-after-30-plus-zero-days-published/">N-able takes cloud platform offline after 30+ &quot;zero-days ...</a></li>
<li><a href="https://techcrunch.com/2026/11/10/n-able-takes-its-remote-access-service-offline-after-researcher-publishes-dozens-of-zero-day-bugs/">N-able takes its remote access service offline after ...</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/n-able-takes-cloud-platform-offline-after-30-plus-zero-days-published/">N-able takes cloud platform offline after 30+ &quot;zero-days ...</a></li>
<li><a href="https://cybernews.com/security/n-central-offline-after-33-zero-day-vulnerabilities-disclosed/">N-central vulnerabilities: 33 critical flaws disclosed ...</a></li>

</ul>
</details>

**Tags**: `#cybersecurity`, `#zero-day vulnerabilities`, `#remote access`, `#N-able`, `#incident response`

---

<a id="item-tech-news-6"></a>
### [Git Releases Fixes for Six Security Vulnerabilities](https://github.blog/open-source/git/git-security-vulnerabilities-announced-7/) ⭐️ 8.0/10

Git released patched versions for six security vulnerabilities: CVE-2026-111760 \(arbitrary code execution during recursive clones\), CVE-2026-113408 \(path traversal through a server’s advertised HEAD\), CVE-2026-114467 \(stack corruption when removing signatures\), CVE-2026-114469 \(out-of-bounds reads when applying binary patches\), CVE-2026-105437 \(heap corruption during large merges\), and CVE-2026-114466 \(filesystem access through fast-import streams\). The fixes are included in Git 2.56.1, with backports to Git 2.55.1, 2.54.1, 2.53.1, 2.52.1, 2.51.3, and 2.50.2, and Git recommends updating Git as well as applications that bundle it. The affected behaviors include recursive cloning of malicious repositories, cloning from malicious servers, merging crafted tags or large results, applying crafted binary patches, and processing untrusted fast-import streams; Git now rejects the affected fast-import features unless the caller explicitly enables --allow-unsafe-features. GitHub says fixes are deployed across github.com, GitHub Enterprise Cloud, and GitHub Enterprise Cloud with data residency, with GitHub Enterprise Server updates available in versions 3.19.15, 3.20.11, 3.21.9, and 3.22.4, and coordinated updates planned for GitHub Desktop, the GitHub Copilot app, Codespaces, and Actions.

rss · GitHub Blog · Nov 10, 18:00

**「Background」** Git processes untrusted repository content in several distinct subsystems, including clone and submodule handling, reference negotiation, patch application, merge generation, signature stripping, and fast-import command parsing. The fixes use input validation, size and overflow checks, safer buffer handling, and an explicit opt-in for unsafe fast-import features; when immediate updates are not possible, the project advises restricting clones, merges, patches, and fast-import input to trusted sources, while noting that precautions do not replace patching.

**「Impact」** Developers, CI systems, hosting services, and applications that bundle Git should install the patched release for their branch or maintenance series, because untrusted repository content can otherwise trigger code execution, file disclosure, unintended writes, crashes, or memory corruption. GitHub Enterprise Server administrators should upgrade to 3.19.15, 3.20.11, 3.21.9, or 3.22.4, and users of GitHub Desktop, GitHub Copilot, Codespaces, and Actions should use the patched versions as they become available.

**Tags**: `#Git`, `#security vulnerabilities`, `#open source`, `#code execution`, `#CVE`

---

<a id="item-tech-news-7"></a>
### [Gemini 4 Carbon Expands Access for Complex AI Work](https://deepmind.google/blog/gemini-4-carbon-is-now-available/) ⭐️ 8.0/10

Google DeepMind has made Gemini 4 Carbon generally available to paying developers and enterprises through the API in Google AI Studio and Gemini for business, with introductory pricing of $2 per million input tokens and $10 per million output tokens, and is rolling it out to all Google AI Ultra subscribers in Google Antigravity, the Gemini app, and AI Mode in Search. While Gemini 4 Argon remains the recommended choice for most software engineering and knowledge work, Carbon uses more tokens for long-horizon tasks such as complex multi-step coding and debugging, open-ended scientific research, dense-document analysis, and cybersecurity. Google reports that Carbon ranked first on CursorBench 4.0, Perplexity’s WANDR, and Zapier’s AutomationBench at more than 2× lower cost per task than the next-best external model, and ranked second on the Multimodal Knowledge Agent benchmark at more than 6× lower average cost than the leader. The company is also previewing /swarm in Google Antigravity, which lets developers assign Carbon to architectural, coordination, and audit roles while lighter models work in parallel isolated workspaces and adversarial verifiers check changes. Google also reports leading cyber results on SEC-bench Pro, ExploitGym, and CWE-bench v1, 100% scanning recall and 95% triage precision on its internal Project Fortify benchmark, and Carbon-assisted generation of millions of lines of Lean for AlphaProof Code proofs of key security properties in Signal’s cryptographic protocol; however, the excerpt provides few underlying scores and no independent validation for these claims.

rss · DeepMind Blog · Nov 10, 16:03

**「Model Positioning」** Gemini 4 Argon was recently launched as Google DeepMind’s recommended model for most software engineering and knowledge work. Carbon was first released two weeks earlier to a limited group of cybersecurity defenders through the Fairwind Program before its broader launch, and it emphasizes extended reasoning, thorough exploration, and repeated verification loops while potentially consuming more tokens than Argon.

**「Practical Effect」** Developers and enterprises can now use Carbon through supported APIs for long-running coding, scientific, enterprise-analysis, and security workflows, while Ultra subscribers gain access across Google Antigravity, the Gemini app, and Search. Organizations evaluating it should validate performance on their own workloads because the published excerpt omits most underlying benchmark scores and test methods.

**Tags**: `#Gemini 4 Carbon`, `#AI models`, `#agentic workflows`, `#software engineering`, `#cybersecurity`

---

<a id="item-tech-news-8"></a>
### [DeepMind Unveils Gemini Robotics 2.5 and ASIMOV-jailbreak](https://arstechnica.com/google/2026/11/deepmind-reveals-gemini-robotics-2-5-and-open-safety-benchmark-asimov-jailbreak/) ⭐️ 7.5/10

Google DeepMind announced Gemini Robotics 2.5, a vision-language-action \(VLA\) system whose Gemini Embodied Reasoning component interprets instructions and live video to plan tasks before generating robot actions. Google evaluated the system on more than 200 activities, including serving food with tongs and using a pipette, and demonstrated Apptronik’s Apollo 2 humanoid tying a bow; DeepMind reports a 30–100% higher success rate and 20–30% faster performance than the previous version, based on laboratory testing. In trials with Apptronik and Mercedes-Benz, Gemini-powered Apollo 2 robots kitted automotive parts in several European factories at a reported 96% success rate, although DeepMind says closing the remaining four-percent gap to human reliability will be a “steep road.” The release also introduced the open ASIMOV-jailbreak safety benchmark for evaluating jailbreak risks in embodied AI.

rss · Ars Technica · Nov 10, 15:00

**「How the System Works」** Embodied AI connects language and visual perception to physical actions. In DeepMind’s architecture, Gemini Embodied Reasoning uses instructions and live video to plan how a robot should complete a task, while the Gemini Robotics VLA generates the actuator commands that carry out that plan; deformable objects such as ribbons are particularly challenging to manipulate.

**「Practical Impact」** Robotics developers and manufacturers gain a more dexterous VLA model, a reported Mercedes-Benz factory deployment result, and the open ASIMOV-jailbreak benchmark for safety evaluation, but the performance figures remain company-reported and do not yet establish human-level reliability.

**Tags**: `#robotics`, `#embodied AI`, `#AI safety`, `#vision-language-action`

---

<a id="item-tech-news-9"></a>
### [Synaptics Patent Claims Halt DisplayLink Driver Work](https://lwn.net/SubscriberLink/1102549/acbc92e00cee3a3f/) ⭐️ 7.0/10

Patent claims from Synaptics prompted DisplayLink to stop work on its display drivers, according to the supplied account. The assertions raise concerns about the legality of reverse engineering, the sustainability of open-source driver maintenance, and continued interoperability for users of DisplayLink hardware. The available material does not identify the specific patents or explain the conduct Synaptics challenged, leaving the dispute&\#x27;s legal and industry scope uncertain. The immediate consequence is that driver development has stopped, leaving users dependent on the existing software unless the dispute is resolved or an alternative implementation becomes available.

hackernews · speckx · Nov 10, 18:02 · [Discussion](https://news.ycombinator.com/item?id=50443824)

**「Background」** DisplayLink is a proprietary display-over-USB technology whose Linux support has relied on drivers that implement its protocol. The project halted by the dispute was Vino, an open-source Rust DisplayLink driver written by developer Mike Lothian with Claude; after he sought technical help from a Synaptics engineer, Synaptics alleged that implementing the protocol implicated its patents and demanded the project&\#x27;s removal. Reports say Synaptics asserted 125 patent claims, although no ruling established that those claims were valid or infringed; reverse engineering alone is not necessarily infringement, which depends on whether an implementation covers every limitation of an enforceable patent claim.

**「Open-source DisplayLink support stalls」** For developers and Linux users dependent on open-source DisplayLink support, Synaptics&\#x27; cease-and-desist has reportedly halted work on the Vino driver and exposed contributors to patent-litigation risk. The practical result is that affected USB graphics hardware may remain without active open-source driver maintenance, although the evidence does not establish an industry-wide effect.

**「Community Reaction」** Several commenters called Synaptics&\#x27;s threatened $25,000 payment for documentation costs an unreasonable scare tactic, while one disputed the legal theory by distinguishing patent disclosure from trade-secret protection and noting clean-room reverse engineering. Others argued that DisplayLink was already losing ground because of high DDR prices and native DisplayPort Alt Mode support in Thunderbolt and USB4 docks, with one user also describing recurring audio problems; these claims are community commentary rather than verified evidence of broader industry impact.

<details><summary>References</summary>
<ul>
<li><a href="https://tech.yahoo.com/computing/articles/synaptics-hits-open-source-linux-151911998.html">Synaptics Hits Open-Source Linux Driver Vino With Cease-and ...</a></li>
<li><a href="https://emergent.sh/news/synaptics-patent-threat-kills-claude-written">Synaptics Patent Threat Kills Claude-Written DisplayLink</a></li>
<li><a href="https://videocardz.com/newz/synaptics-threatens-developer-who-used-claude-ai-to-create-open-source-displaylink-driver">Synaptics threatens developer who used Claude AI to create ...</a></li>
<li><a href="https://www.tomshardware.com/peripherals/docking-stations-hubs/synaptics-sends-cease-and-desist-order-to-creator-of-open-source-displaylink-driver-dares-him-to-publicize-its-threats-dev-reverse-engineers-displaylink-using-claude-ai-and-rust-synaptics-threatens-to-bill-creator-for-legal-documentation">Synaptics sends cease-and-desist order to creator of open - source ...</a></li>
<li><a href="https://www.phoronix.com/news/Synaptics-Blocks-Vino-Driver">Synaptics Appears To Use Legal Threats To Block Open - Source ...</a></li>

</ul>
</details>

**Tags**: `#open-source drivers`, `#patent enforcement`, `#DisplayLink`, `#reverse engineering`

---

<a id="item-tech-news-10"></a>
### [Modern Web Guidance Teaches Coding Agents Native Browser APIs](https://github.com/GoogleChrome/modern-web-guidance) ⭐️ 7.0/10

The Chrome team, in collaboration with Firefox, MDN, and Edge, released Modern Web Guidance 1.0, an open-source knowledge base of more than 200 expert-written guides, roughly 1.7 MB in size, intended to steer coding agents from legacy div-and-JavaScript patterns toward native features such as CSS.highlights, &lt;dialog&gt; with showModal\(\), and field-sizing. Its agent skill and retrieval-based CLI reportedly reduce a 500 MB native stack to about 7 MB of pure JavaScript and search in roughly 10 ms on the user&\#x27;s CPU. A deterministic legacy-scan command, trained on 30,000 GitHub repositories, was reported to have 92% average precision on held-out repositories. In the project&\#x27;s own evaluation of Codex, Claude, and agy across 200 tasks with about 1,700 Playwright/AST-based assertions, agents&\#x27; pass rate increased from 55% without the skill to 92% with it, though this is not an independent benchmark. The package can be installed, searched, or scanned through npx modern-web-guidance@latest with the install, search, and legacy-scan subcommands.

hackernews · paulirish · Nov 10, 18:01 · [Discussion](https://news.ycombinator.com/item?id=50443812)

**「Background」** Coding agents may recognize modern browser APIs but still default to older DOM-and-JavaScript patterns, such as custom elements and scripting for dialogs, text highlighting, or auto-growing textareas. Modern Web Guidance addresses this gap with an open-source, searchable knowledge base and CLI that delivers targeted implementation guidance to agents, helping them modernize existing code and prefer native web-platform features.

**「Effect on Web Developers」** For developers using the skill or CLI, the project reports that guided coding agents improved task pass rates from 55% to 92% across 200 tasks, while the legacy-pattern scanner achieved 92% average precision on held-out repositories, making native-browser-API modernization more practical than relying on prompts alone. Teams should still verify browser support for each recommended feature, because compatibility tables show that some modern CSS capabilities are not uniformly available across Chrome, Firefox, and Safari.

**「Community Discussion」** A commenter highlighted a compatibility concern, listing features stable in Chrome but unsupported in Firefox and Safari, including CSS @function, calc-size\(\), interpolate-size, corner-shape, border-shape, flex-wrap: balance, text-fit, and newer scroll features. Other participants proposed a grep-friendly Markdown index on GitHub Pages to avoid installation, questioned whether Chrome-led guidance could reinforce browser dominance, preferred SSR-first compiled templates such as HtmlFlow or kotlinx.html with Tailwind and Alpine.js over an SPA, and asked where errors should be reported.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/GoogleChrome/modern-web-guidance">GitHub - GoogleChrome / modern - web - guidance : Keep your coding...</a></li>
<li><a href="https://news.ycombinator.com/item?id=50443812">Show HN: Get your coding agent off ~2019 JavaScript, onto modern ...</a></li>
<li><a href="https://caniuse.com/">Can I use... Support tables for HTML5, CSS3, etc</a></li>
<li><a href="https://modern-css.com/browser-support/">CSS Browser Support &amp; Compatibility Checker | modern.css</a></li>
<li><a href="https://github.com/GoogleChrome/modern-web-guidance">GitHub - GoogleChrome/modern-web-guidance: Keep your coding ...</a></li>

</ul>
</details>

**Tags**: `#coding-agents`, `#web-platform`, `#browser-apis`, `#developer-tools`, `#open-source`

---

<a id="item-tech-news-11"></a>
### [Meta launches Muse Ember for efficient agent tasks](https://simonwillison.net/2026/Nov/10/muse-ember/) ⭐️ 7.0/10

Meta AI launched Muse Ember 1.0, its smallest and most efficiency-focused model, for tool calls, coding subtasks, routing, extraction, and long-document parsing, with support for up to 1 million input tokens. At up to 200,000 tokens, it costs $0.10 per million input tokens, $0.004 per million cached-input tokens, and $0.50 per million output tokens; above 200,000, those rates rise to $0.30, $0.012, and $1.50, placing its long-prompt rates between GPT-6 Luna and Claude Haiku 5.5. Artificial Analysis results cited in the article place Ember’s xhigh and max settings at roughly $0.12 and $0.14 per task, with Intelligence Index scores of about 34 and 36, respectively, on the cost-performance Pareto frontier. The model offers six reasoning levels—minimal, low, medium, high, xhigh, and max—but an informal SVG exercise found that “high” did not return a complete image and that reasoning level did not cleanly predict visual quality. Willison judged the “max” pelican output comparable to Muse Wonder despite Ember costing 40 times less, although that illustration was not a broad benchmark of quality.

rss · Simon Willison · Nov 10, 07:28

**「Muse model family」** Muse is Meta’s family of generative models, and Muse Ember is its compact, efficiency-focused tier, following the mid-weight Spark, Spark’s open-source twin Glimmer, and the larger Muse Wonder. It targets high-volume agent workflows such as tool use, coding subtasks, routing, extraction, and long-document parsing, with support for contexts of up to 1 million tokens. Because selectable reasoning levels can change token consumption, these models are also compared by their Artificial Analysis Intelligence Index and cost per completed task rather than by token prices alone.

**「Impact」** Developers running high-volume agent workflows can use Muse Ember as a cost-efficient option for repeated tool calls, coding subtasks, routing, extraction, and long-document parsing, with a 1M-token input limit and base pricing of $0.10 per million input tokens and $0.50 per million output tokens. Its higher-priced long-prompt tiers and the lack of independent validation mean actual savings will depend on prompt length and reasoning-token use.

<details><summary>References</summary>
<ul>
<li><a href="https://interestingengineering.com/ai-robotics/meta-muse-ember-smallest-model-ai-agents">Meta unveils Muse Ember , its smallest model yet for cheaper AI agents</a></li>
<li><a href="https://techcrunch.com/2026/11/09/meta-releases-muse-ember-a-new-lightweight-model-for-agent-execution/">Meta releases Muse Ember , a new lightweight model for... | TechCrunch</a></li>
<li><a href="https://artificialanalysis.ai/articles/meta-s-muse-ember-is-the-cheapest-model-scoring-36-on-the-intelligence-index">Meta &#x27;s Muse Ember is the cheapest model ... | Artificial Analysis</a></li>
<li><a href="https://dev.meta.ai/models/muse-ember">Muse Ember | Meta</a></li>
<li><a href="https://research.meta.ai/blog/muse-ember">Introducing Our Smallest, Most Efficient Model: Muse Ember</a></li>

</ul>
</details>

**Tags**: `#language models`, `#AI agents`, `#model efficiency`, `#tool use`, `#pricing`

---

<a id="item-tech-news-12"></a>
### [Pentagon backs launch rivals as Falcon retirement approaches](https://arstechnica.com/space/2026/11/the-us-military-seems-to-be-getting-nervous-about-the-launch-supply-crunch/) ⭐️ 7.0/10

The Pentagon’s Office of Strategic Capital conditionally committed $150 million to Stoke Space on October 26 and another $150 million to Rocket Lab on Tuesday, marking the first significant support it has provided to commercial launch companies. The intervention indicates that defense officials view SpaceX’s planned wind-down of Falcon as a potential national-security and launch-capacity risk. SpaceX has stopped accepting commercial Falcon 9 orders for launches after 2028, while government missions for customers including NASA and the US Space Force are expected to continue; the Space Force contract permits orders through 2029 and launches through 2033. Falcon’s eventual retirement remains dependent on Starship proving capable of carrying national-security payloads, while SpaceX’s near-term priority is using that capacity for Starlink satellites and Starmind orbital data centers.

rss · Ars Technica · Nov 10, 23:02

**「Military launch transition」** Falcon 9 and Falcon Heavy remain important military launch vehicles, with the Space Force contract allowing orders through 2029 and launches through 2033 even as SpaceX stops accepting commercial Falcon 9 orders after 2028. The Pentagon’s Office of Strategic Capital, created in 2022 to finance companies developing strategically important technologies, is backing alternative providers with $150 million conditional loan commitments each to Stoke Space and Rocket Lab. The support is intended to advance new medium-class rockets before Starship is ready for national-security payloads, with each loan still subject to financial, legal, technical, and other closing requirements.

**「Launch capacity impact」** The Pentagon’s conditional $150 million commitments to Stoke Space and Rocket Lab are intended to expand alternative US launch capacity for defense and other government payloads as Falcon winds down, but they do not provide an immediate replacement because SpaceX can accept Falcon 9 and Falcon Heavy government orders through 2029, with launches extending through 2033.

<details><summary>References</summary>
<ul>
<li><a href="https://www.war.gov/News/Releases/Release/Article/4633729/department-of-wars-office-of-strategic-capital-signs-150-million-conditional-lo/">Department of War&#x27;s Office of Strategic Capital Signs $150 ...</a></li>
<li><a href="https://www.war.gov/News/Releases/Release/Article/4644766/the-department-of-wars-office-of-strategic-capital-signs-150-million-conditiona/">The Department of War&#x27;s Office of Strategic Capital Signs ...</a></li>
<li><a href="https://arstechnica.com/space/2026/11/the-us-military-seems-to-be-getting-nervous-about-the-launch-supply-crunch/">The US military seems to be getting nervous about the launch ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/National_Security_Space_Launch">National Security Space Launch - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#commercial space launch`, `#SpaceX Falcon`, `#defense financing`, `#Rocket Lab`, `#Stoke Space`

---

<a id="item-tech-news-13"></a>
### [Oura to Acquire Counsel Health for $625 Million](https://www.theverge.com/gadgets/1031284/oura-counsel-health-acquisition) ⭐️ 7.0/10

Oura agreed to acquire Counsel Health, an AI-native primary-care startup, for $625 million after adding its AI chatbot to the Oura app earlier this year. Counsel Health&\#x27;s app provides AI-generated responses and insights based on health data reported by users. The announcement did not provide details about the underlying models, privacy safeguards, regulatory strategy, or planned post-acquisition changes. The deal follows Oura&\#x27;s decision to postpone an IPO valued at up to $2.2 billion indefinitely because of uncertainty in the IPO market.

rss · The Verge · Nov 10, 21:40

**「Counsel Health and Oura」** Counsel Health describes itself as an “AI-native primary care company,” using an app to provide AI-generated guidance and insights from users’ reported health data, with access to licensed medical professionals. Oura had already integrated Counsel Health’s chatbot into its smart-ring app in June before announcing the planned acquisition, extending an existing product relationship.

**「Impact」** Once the $625 million acquisition closes, Oura members’ existing chatbot access will sit within a broader connected-care offering that links continuous biometric data to personalized medical guidance and on-demand licensed doctors. The available material does not specify how clinical safety, escalation, or coverage will change after closing.

<details><summary>References</summary>
<ul>
<li><a href="https://cd.aevumnews.com/en/oura-to-acquire-ai-native-primary-care-startup-counsel-health-for-625m">Oura to Acquire AI - Native Primary Care Startup Counsel Health for...</a></li>
<li><a href="https://thenextweb.com/news/oura-counsel-health-625m-acquisition-ai-doctors">Oura buys Counsel Health for $ 625 m to put AI and doctors in its app</a></li>
<li><a href="https://www.businesswire.com/news/home/20261110737835/en/Oura-to-Acquire-Counsel-Health-Advancing-Vision-for-More-Connected-Personalized-Healthcare">Oura to Acquire Counsel Health , Advancing Vision for More...</a></li>
<li><a href="https://cd.aevumnews.com/en/oura-to-acquire-ai-native-primary-care-startup-counsel-health-for-625m">Oura to Acquire AI -Native Primary Care Startup Counsel Health for...</a></li>

</ul>
</details>

**Tags**: `#health AI`, `#AI chatbots`, `#startup acquisitions`, `#wearables`

---

<a id="item-tech-news-14"></a>
### [New York AI Safety Law Brings OpenAI and Anthropic Under Oversight](https://techcrunch.com/2026/11/10/openai-anthropic-face-new-oversight-as-new-yorks-ai-safety-law-takes-effect/) ⭐️ 7.0/10

New York is preparing to enforce its sweeping AI safety law, placing major AI developers such as OpenAI and Anthropic under new oversight. Covered developers must register with the state, disclose their safety practices, and report critical incidents or face fines. The change represents a significant expansion of regulatory scrutiny, although the report provides limited detail about enforcement scope, exact compliance requirements, or penalty amounts.

rss · TechCrunch · Nov 10, 20:52

**「New York’s RAISE Act」** New York’s Responsible AI Safety and Enforcement \(RAISE\) Act is described as the first comprehensive state-level AI safety law in the United States, establishing oversight for large frontier-AI developers such as OpenAI and Anthropic. Its framework requires developer registration, disclosure of safety practices, and reporting of critical incidents within 72 hours, with financial penalties for noncompliance; registration opened on November 10, 2026, ahead of a January 1, 2027 deadline.

**「Industry impact」** For major developers subject to New York’s law—including OpenAI and Anthropic—the immediate consequence is a new compliance burden: they must register, disclose their safety practices, and report critical incidents or risk fines. The available report does not specify the precise coverage, disclosure thresholds, or penalty amounts, and the relevant policy material describes New York’s regime as state-level rather than federal.

<details><summary>References</summary>
<ul>
<li><a href="https://www.techbuzz.ai/articles/new-york-s-ai-safety-law-hits-openai-anthropic-today">New York&#x27;s AI Safety Law Hits OpenAI, Anthropic Today</a></li>
<li><a href="https://codingislove.com/new-york-raise-act-ai-safety-law/">New York opens RAISE Act registration for OpenAI, Anthropic ...</a></li>
<li><a href="https://www-cdn.anthropic.com/a9ceec76a54d28d27affffcdab6faf7c142cd587.pdf">Anthropic 2026</a></li>

</ul>
</details>

**Tags**: `#AI regulation`, `#AI safety`, `#OpenAI`, `#Anthropic`, `#New York`

---

<a id="item-tech-news-15"></a>
### [llm-gemini 0.36 Adds Gemini 4 Carbon](https://simonwillison.net/2026/Nov/10/llm-gemini/) ⭐️ 6.0/10

llm-gemini 0.36 adds support for Gemini 4 Carbon, which Google made broadly available on November 10, 2026 after initially announcing it two weeks earlier for a subset of cyber defenders. Google launched Carbon at $2 per million input tokens and $10 per million output tokens, then scheduled those prices to double on December 1, 2026, to $4 and $20 respectively. Carbon supports low, medium, and high reasoning efforts, with medium as the default, and Simon Willison illustrated the modes with generated pelican prompts. He also used Carbon through Google Antigravity IDE to create a standalone Three.js and OpenStreetMap mech animation and highlighted a YouTube demo of Antigravity’s /swarm feature; these demonstrations are examples rather than independent benchmarks.

rss · Simon Willison · Nov 10, 20:09

**「Background」** llm-gemini 0.36 is the plugin release that added support for Google’s Gemini 4 Carbon model. Carbon had been announced two weeks earlier for a limited group of cyber defenders before becoming broadly available on November 10, 2026; its API supports configurable low, medium, and high reasoning effort, with medium as the default, and launch pricing of $2 per million input tokens and $10 per million output tokens before a scheduled December 1 increase to $4 and $20.

**「Developer Impact」** Developers using llm-gemini can select Gemini 4 Carbon and configure its reasoning effort, but those seeking the lower launch pricing would need to use it before the announced December 1 increase.

**Tags**: `#Gemini`, `#LLM APIs`, `#model pricing`, `#llm-gemini`

---

<a id="item-tech-news-16"></a>
### [Ownership Framing Boosts Claude Refactoring](https://simonwillison.net/2026/Nov/10/prompting-claude-fable-52/) ⭐️ 6.0/10

Anthropic&\#x27;s “Prompting Claude Fable 5.2” documentation says the model follows prompts closely when they specify who owns the codebase. In Anthropic&\#x27;s tests on small coding tasks, prompts that left ownership unstated or presented the code as someone else&\#x27;s tended to make Claude extend the existing structure, even when that duplicated code. When told, “This codebase is yours: what it&\#x27;s for and how it&\#x27;s built are your call, and you&\#x27;ll keep building on it,” Claude merged repeated code in about half of attempts, compared with under one tenth without such framing. The finding offers a concrete refactoring tactic, but the evidence is limited to vendor-reported small-task tests and lacks broader validation in the supplied material.

rss · Simon Willison · Nov 10, 05:34

**「Background」** Prompt engineering for coding models can influence whether a model extends an existing structure or actively refactors it. Anthropic’s guidance for Claude Fable 5.2 describes explicitly establishing the model’s ownership of a codebase as a prompting technique that encourages code consolidation and structural improvements.

**「Practical impact」** Developers using Claude Fable 5.2 can explicitly frame the codebase as the model’s own to make it more likely to consolidate repeated code and improve repository structure rather than extend existing duplication. The evidence is limited to Anthropic’s tests on small coding tasks, so the effect is not yet established for larger codebases.

**Tags**: `#prompt engineering`, `#Claude`, `#code refactoring`, `#AI-assisted coding`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Polymarket says annualized revenue has topped $1.8 billion](https://www.cnbc.com/2026/11/10/polymarket-annualized-revenue-us-growth.html) ⭐️ 8.0/10

Polymarket says its annualized revenue run rate has exceeded $1.8 billion as U.S. exchange volume and financing have surged, while regulatory and political scrutiny intensifies.

rss · CNBC Finance · Nov 10, 13:00

**Tags**: `#Polymarket`, `#prediction markets`, `#revenue growth`, `#CFTC investigation`, `#regulation`

---

<a id="item-finance-news-2"></a>
### [Waller leans toward December rate hike](https://www.cnbc.com/2026/11/10/fed-governor-waller-sees-december-hike-likely.html) ⭐️ 8.0/10

Federal Reserve Governor Christopher Waller said he is leaning toward a December rate increase and would consider a 50-basis-point hike if October inflation exceeds forecasts. Headline CPI rose 0.4% and core CPI rose 0.3%, each 0.1 percentage point above the Dow Jones consensus; traders fully priced a 25-basis-point December move and assigned 12.5% odds to a 50-basis-point move.

rss · CNBC Finance · Nov 10, 17:13

**「Background」** After raising rates by 25 basis points in September, the Fed held steady in October pending more information; Dallas Fed President Lorie Logan expects two more quarter-point hikes before pausing to assess their effects.

**「Impact」** A December increase would tend to raise borrowing costs for businesses and households, with a 50-basis-point move tightening financial conditions more sharply than a quarter-point increase.

**Tags**: `#Federal Reserve`, `#interest rates`, `#inflation`, `#monetary policy`, `#December meeting`

---