---
layout: default
title: "Horizon Summary: 2026-11-09 (EN)"
date: 2026-11-09
lang: en
---

> From 70 items, 11 important content pieces were selected

---

**Technology News**
1. [Goldman Sachs reportedly pulls Claude Code from bankers and traders](#item-tech-news-1) ⭐️ 7.0/10
2. [Nvidia is investigating Jensen Huang’s relationship with a Chinese spy](#item-tech-news-2) ⭐️ 7.0/10
3. [worse\_query iOS Sandbox Escape PoC Includes 27.3 Beta](#item-tech-news-3) ⭐️ 7.0/10
4. [AI-Designed Avian Flu Vaccine Shows Broad Protection in Animals](#item-tech-news-4) ⭐️ 7.0/10
5. [SQLite parse\_number Extension: C Outperforms Rust](#item-tech-news-5) ⭐️ 6.0/10
6. [Using Electrical Noise to Probe Cuprate Superconductivity](#item-tech-news-6) ⭐️ 6.0/10
7. [Epic Games Launcher Confirms SteamOS Support](#item-tech-news-7) ⭐️ 6.0/10
8. [Apple Urges Faster Development of an Agentic Siri](#item-tech-news-8) ⭐️ 6.0/10
9. [Elvis and Eminem Rights Holders Sue Suno](#item-tech-news-9) ⭐️ 6.0/10
10. [Huawei Claims Fully Chinese PC](#item-tech-news-10) ⭐️ 6.0/10
11. [ITU Meeting Puts 278 Internet Governance Proposals on the Table](#item-tech-news-11) ⭐️ 6.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Goldman Sachs reportedly pulls Claude Code from bankers and traders](https://www.thestateofai.com/news/goldman-sachs-claude-code-traders-bankers) ⭐️ 7.0/10

Goldman Sachs is reportedly withdrawing Anthropic’s Claude Code from its bankers and traders, restricting an AI coding agent within a regulated financial institution. The available account does not clarify whether this is a complete prohibition, a temporary rollback, or a change in entitlements, nor does it provide Goldman Sachs’ stated reasons. Security, compliance, data-access controls, auditability, and usage costs are plausible considerations raised in the accompanying analysis and discussion, but they are not confirmed explanations from the bank. The restriction nevertheless shows how institutional governance can constrain the deployment of agentic AI even when its capabilities are commercially attractive.

hackernews · TheWiggles · Nov 8, 18:16 · [Discussion](https://news.ycombinator.com/item?id=50415628)

**「Background」** Claude Code is Anthropic’s agentic coding assistant, and its risk profile depends heavily on the permissions and connected systems available to the user running it. In financial institutions, workstations may provide access to client or trading data, proprietary information, email, and internal networks, making identity, entitlement, audit, and data-boundary controls essential.

**「Impact」** Affected Goldman Sachs bankers and traders will have reduced or revoked access to Claude Code. The longer-term effect on AI-assisted development will depend on whether the bank substitutes controlled alternatives or continues limiting agent access.

**「Community discussion」** Commenters emphasized the danger of semi-unattended agents operating from finance professionals’ workstations, while others cited unpredictable consumption billing, compliance requirements, application entitlements, and auditability as practical constraints. One commenter speculated that an operational loss caused the change, and another questioned its timing in relation to Goldman Sachs’ purported role in Anthropic’s IPO, but neither explanation was confirmed.

**Tags**: `#enterprise AI`, `#coding agents`, `#AI security`, `#financial services`, `#Claude Code`

---

<a id="item-tech-news-2"></a>
### [Nvidia is investigating Jensen Huang’s relationship with a Chinese spy](https://www.theverge.com/ai-artificial-intelligence/1029562/nvidia-investigating-jensen-huang-relationship-chinese-spy) ⭐️ 7.0/10

Nvidia’s board has opened an independent investigation into CEO Jensen Huang’s relationship with Megaspeed executive Alice Huang, reportedly recruited by China’s Ministry of State Security to spy on the company.

rss · The Verge · Nov 8, 20:22

**Tags**: `#Nvidia`, `#Jensen Huang`, `#corporate governance`, `#China`, `#espionage`

---

<a id="item-tech-news-3"></a>
### [worse\_query iOS Sandbox Escape PoC Includes 27.3 Beta](https://x.com/forcequitOS/status/2119475139528020218?) ⭐️ 7.0/10

According to the supplied report, forcequitOS published the “worse\_query” zero-day sandbox-escape proof of concept on November 8, targeting iOS 26.0–26.7.2 and iOS 27.2, including the 27.3 beta. The author describes it as the successor to bad\_query and says that, with an App Group configured, it can access system paths and modify application data; it is intended for development and research, not jailbreaking. The author also says the report was submitted to Apple for review but the vulnerability had not yet been patched, while tools such as GestaltX reportedly emerged quickly based on the PoC. The supplied material does not include exploit details, independent validation, or confirmation of the current patch status.

telegram · zaihuapd · Nov 9, 02:36

**「Background」** An iOS sandbox escape breaks the isolation that normally limits an app to its designated containers and permissions. The worse\_query proof of concept is described as the direct successor to bad\_query; it requires developers to configure an App Group container and is intended for development and research rather than functioning as a standalone jailbreak.

**「Operational impact」** Developers of App Group–enabled apps on iOS 26.0–26.7.2, iOS 27.2, or the reported 27.3 beta should assume a vulnerable app could cross its intended sandbox boundary and access system paths or modify app data through the public worse\_query PoC. With no patch confirmed for the affected builds, developers should assess their apps’ privileges and data exposure while treating the exploit’s real-world reach as unverified until it is independently tested and Apple confirms a fix.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/forcequitOS/worse_query">forcequitOS / worse _ query : A sandbox escape for iOS 26 and 27...</a></li>
<li><a href="https://github.com/forcequitOS/worse_query">GitHub - forcequitOS/ worse _ query : A sandbox escape for iOS 26...</a></li>

</ul>
</details>

**Tags**: `#iOS`, `#沙盒逃逸`, `#零日漏洞`, `#漏洞研究`, `#安全工具`

---

<a id="item-tech-news-4"></a>
### [AI-Designed Avian Flu Vaccine Shows Broad Protection in Animals](https://www.cam.ac.uk/stories/ai-developed-vaccines-against-viruses) ⭐️ 7.0/10

A University of Cambridge team and other institutions reported in November 2026 that an AI-assisted avian influenza candidate vaccine produced broad immune responses and protection in mice and ferrets. Protection was stronger than that from the study’s control formulation, which was based on a WHO candidate vaccine virus. The artificially designed broad-spectrum antigens do not exist naturally, and the team says AI-assisted design can accelerate vaccine antigen development. Human clinical trials are planned, but protection has not yet been demonstrated in people, while the supplied account does not specify the AI model, training data, or design method.

telegram · zaihuapd · Nov 9, 03:00

**「Background」** Broadly protective influenza vaccines are designed to generate immune responses against multiple virus strains rather than relying on a single strain-specific antigen. In this study, AI-assisted methods were used to create artificial broad-spectrum vaccine antigens that do not occur naturally, and their protective effects were evaluated in mice and ferrets. These animal-model results represent preclinical evidence, so human efficacy and safety will need to be assessed in clinical trials.

**「Public-health impact」** For vaccine developers and public-health agencies, the study supports advancing the AI-designed broad-spectrum avian influenza candidate into human trials, with the potential to accelerate emergency vaccine development and broaden strain coverage. The immediate impact remains investigational: protection has been demonstrated only in mice and ferrets, and the candidate’s effectiveness in people is still unproven.

**Tags**: `#AI辅助药物设计`, `#禽流感疫苗`, `#动物实验`, `#计算生物学`

---

<a id="item-tech-news-5"></a>
### [SQLite parse\_number Extension: C Outperforms Rust](https://simonwillison.net/2026/Nov/8/sqlite-parse-number-c-vs-rust/) ⭐️ 6.0/10

Simon Willison used Claude Opus 5.5 to compare SQLite extensions that implement parse\_number\(\), stripping commas, dollar and pound signs, and percent signs, handling a leading minus, and returning NULL for unparseable input. The initial C extension produced a 14 KB shared library, versus 321 KB for Rust using Rusqlite and 298 KB with sqlite-loadable-rs. After Claude replaced the C implementation’s strtod-based parsing with custom code, the revised C version beat both Rust variants across benchmarks processing 2 million rows: it recorded 19 ns per row for mixed data, 16 ns for integers, and 18 ns for decimals, compared with Rust results of 32–55 ns depending on the library and dataset. The resulting experiment and report were published in Simon Willison’s simonw/research GitHub repository, demonstrating that a substantially smaller C extension could also outperform the AI-generated Rust implementations in this specific test.

rss · Simon Willison · Nov 8, 22:26

**「Background」** SQLite loadable extensions can add custom SQL functions at runtime, allowing parse\_number\(\) to normalize strings such as “-$1,234.56” before SQLite performs arithmetic or ordering. The comparison considers implementing the parser in C, where standard-library numeric conversion functions such as strtod are available, or in Rust, with code complexity, binary size, and per-row performance as the main criteria.

**「Practical impact」** For developers shipping loadable SQLite extensions, this experiment suggests a purpose-built C implementation can outperform both tested Rust options while remaining compact: the C binary was 14 KB versus 298–321 KB for Rust, and the optimized C parser processed rows in 16–19 ns versus 32–55 ns. These narrow prototype results do not establish general C-over-Rust superiority for other extension workloads.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/asg017/sqlite-loadable-rs">GitHub - asg017/ sqlite - loadable - rs : A framework for writing fast and...</a></li>

</ul>
</details>

**Tags**: `#SQLite`, `#Rust`, `#C`, `#performance comparison`, `#AI-assisted development`

---

<a id="item-tech-news-6"></a>
### [Using Electrical Noise to Probe Cuprate Superconductivity](https://arstechnica.com/science/2026/11/physicists-listened-to-electrical-noise-to-crack-a-superconductor-mystery/) ⭐️ 6.0/10

Researchers led by Milan Allan of Ludwig Maximilian University of Munich and Ingmar Swart of Utrecht University used faint electrical noise from current flowing through cuprate superconductors to investigate the pseudogap, the apparent loss of electrons above the superconducting transition temperature. The Science study addressed two long-standing explanations: electrons becoming trapped in ordered structures such as charge-density waves, or Cooper pairs forming before superconductivity and serving as its precursor. By treating the electrical crackle as a way to detect pairs directly, the team reported finding some answers, although the supplied excerpt does not specify the measured signatures, numerical results, or final conclusion. The work is a condensed-matter research result rather than a demonstrated application.

rss · Ars Technica · Nov 8, 12:15

**「The Cuprate Pseudogap Puzzle」** Superconductors carry current without resistance, but most operate only a few degrees above absolute zero. Copper-based cuprates, discovered in the late 1980s, superconduct at higher temperatures reachable with affordable liquid nitrogen, yet their microscopic mechanism remains debated. Above the superconducting transition, the pseudogap appears as a reduction in the number of electrons detected at energies where they would normally be expected.

**「A New Experimental Probe」** For condensed-matter researchers, analyzing electrical noise provides an additional way to probe electron pairing in cuprates and potentially distinguish competing explanations of the pseudogap; the supplied excerpt reports no practical device, material, or engineering application.

**Tags**: `#superconductivity`, `#cuprates`, `#condensed-matter physics`, `#electrical-noise analysis`

---

<a id="item-tech-news-7"></a>
### [Epic Games Launcher Confirms SteamOS Support](https://www.theverge.com/games/1029557/epic-games-launcher-is-coming-to-steamos) ⭐️ 6.0/10

Epic Games has confirmed that its Epic Games Launcher will support Valve’s Linux-based SteamOS alongside a handful of other Linux distributions. Communications Director Jake Jones provided the confirmation to GamingOnLinux. In October, Epic said it was investigating Fortnite compatibility with SteamOS, while the launcher was in preview and SteamOS was not specifically listed as supported. The announcement confirms launcher compatibility but does not establish that Fortnite itself will run on SteamOS.

rss · The Verge · Nov 8, 20:52

**「Linux compatibility context」** SteamOS is Valve’s Linux-based gaming operating system, best known for the Steam Deck, while Linux distributions can differ in how they package applications. Epic’s new Games Launcher was already in preview as the company separately investigated Fortnite compatibility, so the confirmed SteamOS support applies to distributing the launcher rather than establishing that Fortnite itself is compatible.

**「What This Means for Linux Users」** SteamOS users can now regard the Epic Games Launcher as an officially supported client, but they should not assume Fortnite or other games are compatible with the platform.

<details><summary>References</summary>
<ul>
<li><a href="https://www.gamingonlinux.com/2026/11/epic-games-comments-on-planned-linux-distribution-support/">Epic Games comments on planned Linux distribution support</a></li>

</ul>
</details>

**Tags**: `#Linux gaming`, `#SteamOS`, `#Epic Games Launcher`, `#game distribution`

---

<a id="item-tech-news-8"></a>
### [Apple Urges Faster Development of an Agentic Siri](https://www.theverge.com/ai-artificial-intelligence/1029552/apple-siri-ai-agentic) ⭐️ 6.0/10

Apple is accelerating its effort to build a more agentic Siri, according to Bloomberg reporter Mark Gurman’s account relayed by The Verge. CEO John Ternus is pressuring AI czar Craig Federighi to advance the Siri roadmap and deliver an AI agent capable of competing with OpenAI’s Dots or Meta’s Muse. Federighi has reportedly produced a functional version of Siri AI on an exceptionally short timeline. However, the brief secondhand account provides no concrete features, release date, benchmarks, or availability details, leaving the scope and readiness of the broader effort unclear.

rss · The Verge · Nov 8, 19:18

**「Background」** An agentic AI assistant can go beyond answering questions by planning and carrying out multi-step tasks on a user’s behalf. The reported competition among Apple, OpenAI, and Meta concerns how quickly their assistants can provide this broader combination of reasoning and action.

**Tags**: `#Apple Siri`, `#AI agents`, `#consumer AI`, `#product strategy`

---

<a id="item-tech-news-9"></a>
### [Elvis and Eminem Rights Holders Sue Suno](https://www.theverge.com/ai-artificial-intelligence/1029533/elvis-eminem-suno-ai-music-clone-lawsuit) ⭐️ 6.0/10

Elvis Presley’s music rights holders and the publisher of some of Eminem’s biggest records have sued generative-music company Suno, alleging that it unlawfully generates music and lyrics that mimic those artists. The Presley plaintiffs claim the conduct violates Tennessee law, although the supplied report does not identify the specific statute or provide the full legal theory. The Eminem case similarly alleges unauthorized artist imitation, but the available details do not specify its causes of action, claimed damages, or requested remedies. The lawsuits add to the legal pressure surrounding Suno’s artist-mimicking capabilities, yet filing suit does not establish that the company has infringed anyone’s rights.

rss · The Verge · Nov 8, 17:23

**「Background」** Elvis Presley was a foundational American singer and actor whose recordings and recognizable persona remained commercially significant long after his death. The Presley suit invokes Tennessee law, while the Eminem suit is brought by a music publisher; both allege that Suno generates music and lyrics mimicking the artists without authorization.

**「Legal pressure on artist imitation」** The lawsuits increase Suno’s legal exposure over generating music and lyrics that imitate protected artists, potentially leading to restrictions on its service if the claims succeed.

<details><summary>References</summary>
<ul>
<li><a href="https://en.m.wikipedia.org/wiki/Elvis_Presley">Elvis Presley - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#generative-audio`, `#Suno`, `#copyright`, `#music-ai`, `#legal`

---

<a id="item-tech-news-10"></a>
### [Huawei Claims Fully Chinese PC](https://www.theregister.com/systems/2026/11/09/huawei-says-its-made-a-100-percent-chinese-pc/5308335) ⭐️ 6.0/10

Huawei says it has produced a PC built entirely with Chinese components, according to The Register. The claim could mark progress in China’s domestic hardware ecosystem and efforts to reduce reliance on foreign supply chains. However, the available excerpt provides no component list, specifications, manufacturing details, performance data, or independent verification. It also does not clarify whether “100 percent Chinese” refers to component design, sourcing, assembly, or all three, leaving the achievement’s scope and limitations uncertain.

rss · The Register · Nov 9, 02:14

**「Historical context」** Huawei has built its PC strategy around Kunpeng processors and HarmonyOS, partly in response to restrictions on access to advanced foreign chips and software. In this context, “100 percent Chinese” is a vendor claim about the origin of the computer’s key hardware and software, not a standard certification that can substitute for a documented bill of materials and independent verification.

**「Potential supply-chain impact」** If independently substantiated, Huawei’s PC could give Chinese buyers and component suppliers a platform less dependent on foreign parts, supporting China’s broader semiconductor self-sufficiency effort. However, without specifications or independent verification, its immediate commercial availability and ability to replace foreign-supplied systems remain unproven.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bloomberg.com/graphics/2023-china-huawei-semiconductor/">How Huawei Is Helping China Build Up Its Semiconductor ...</a></li>

</ul>
</details>

**Tags**: `#Huawei`, `#personal computing`, `#Chinese hardware`, `#supply chains`

---

<a id="item-tech-news-11"></a>
### [ITU Meeting Puts 278 Internet Governance Proposals on the Table](https://www.theregister.com/networks/2026/11/08/internet-governance-about-to-get-its-quadrennial-stress-test-at-itu-meeting/5308031) ⭐️ 6.0/10

An upcoming International Telecommunication Union meeting is set to debate 278 proposals concerning Internet governance. Some participants fear the proposals could shift the balance of power toward governments and away from standards bodies and other stakeholders. The meeting therefore represents a significant test of how technical standards and public policy interact within the global Internet. The available account does not detail the individual proposals, their technical implications, or any confirmed outcomes, leaving their concrete impact uncertain.

rss · The Register · Nov 8, 09:33

**「Internet governance context」** The International Telecommunication Union \(ITU\) is the United Nations specialized agency for digital technologies, and its Plenipotentiary Conference—held every four years—sets organization-wide policy and strategy. Internet governance intersects with ITU work because governments participate as member states, while many core Internet protocols are developed through the IETF’s multi-stakeholder process, making proposals at ITU meetings significant for the balance of state influence and broader technical participation.

**「Potential governance shift」** If the ITU’s PP-26 meeting adopts measures among the 278 proposals that increase governmental authority, the balance of influence in internet governance could shift toward governments; because no specific proposals or outcomes are identified, the effect on standards, operators, and users remains uncertain.

<details><summary>References</summary>
<ul>
<li><a href="https://www.itu.int/">ITU : Connecting the world and beyond</a></li>

</ul>
</details>

**Tags**: `#Internet governance`, `#ITU`, `#Technology policy`, `#Internet standards`

---