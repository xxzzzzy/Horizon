---
layout: default
title: "Horizon Summary: 2026-11-28 (EN)"
date: 2026-11-28
lang: en
---

> From 69 items, 10 important content pieces were selected

---

**Technology News**
1. [Trump Administration Secures 10% Intel Stake](#item-tech-news-1) ⭐️ 8.0/10
2. [OpenSec Discloses Pre-Auth Linux nfsd Root Flaw](#item-tech-news-2) ⭐️ 8.0/10
3. [Google&\#x27;s DeepCrossAttention Targets Faster Transformer Inference](#item-tech-news-3) ⭐️ 7.0/10
4. [WebRTC E-Skimming Scripts Found on Shopping Sites](#item-tech-news-4) ⭐️ 7.0/10
5. [AWS Challenger: Trainium3 Inference and Microarchitecture Deep Dive](#item-tech-news-5) ⭐️ 7.0/10
6. [Birmingham Oracle Failure Reaches £128 Million](#item-tech-news-6) ⭐️ 6.0/10
7. [Europe’s AI Push Has Cloud Ambition but Limited Sovereignty](#item-tech-news-7) ⭐️ 6.0/10
8. [AI Boom Lengthens Optical Equipment Lead Times](#item-tech-news-8) ⭐️ 6.0/10
9. [British social security system techies yank services offline following &\#x27;cyber incident&\#x27;](#item-tech-news-9) ⭐️ 6.0/10
10. [How cutting-edge prosthetics can help probe the human mind](#item-tech-news-10) ⭐️ 6.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Trump Administration Secures 10% Intel Stake](https://arstechnica.com/tech-policy/2026/11/intel-faced-a-choice-give-trump-10-or-face-the-consequences/) ⭐️ 8.0/10

Internal notes from a federal lawsuit allege that Commerce Department lawyer David Shapiro told Intel’s CFO in August 2025 that transferring 10% of the chipmaker to the U.S. government was non-negotiable, while warning that rejection would carry consequences he could not predict. Although Shapiro said Intel’s board could reject the offer, it accepted days later; Trump then said the United States had paid nothing for the shares and now “fully owns and controls 10% of INTEL,” which he valued at roughly $11 billion. A former Trump administration official described this as part of a broader Commerce Department shift away from goals such as job creation and market share toward securing cash or ownership from private companies. For Intel and the semiconductor sector, the reported deal represents direct government intervention in a major chipmaker’s ownership and corporate governance, with potentially significant implications for semiconductor manufacturing, chip supply chains, and industrial policy.

rss · Ars Technica · Nov 27, 12:05

**「Background」** Intel is a Santa Clara-based technology company that designs and manufactures CPUs and related semiconductor products. The episode described in the lawsuit connects Intel’s ownership and corporate governance to a broader shift in U.S. industrial policy, in which officials increasingly sought direct financial returns from private companies alongside national competitiveness and job-creation goals.

**「Impact」** Intel shareholders and semiconductor supply-chain partners now face a U.S. government with a 10% ownership interest in Intel, giving Washington a direct channel to influence the chipmaker’s governance and investment priorities. The financial terms remain disputed: the source says the government received shares valued at about $11 billion for nothing, while Intel’s August 22, 2025 announcement describes an $8.9 billion government investment.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Intel">Intel - Wikipedia</a></li>
<li>Intel and Trump Administration Reach Historic Agreement to Accelerate...</li>

</ul>
</details>

**Tags**: `#Intel`, `#semiconductors`, `#US industrial policy`, `#government intervention`, `#chip supply chains`

---

<a id="item-tech-news-2"></a>
### [OpenSec Discloses Pre-Auth Linux nfsd Root Flaw](https://opensec.in/blog/nfs2root-cve-2026-99362) ⭐️ 8.0/10

OpenSec disclosed CVE-2026-99362, a pre-authentication heap overflow in the Linux kernel NFS server nfsd, with a CVSS score of 9.8. According to the disclosure, a single connection to TCP port 2049 can trigger an out-of-bounds kernel heap write and obtain a root shell; the flaw has reportedly existed since Linux 3.16 in 2014 and affects systems using NFSv4.1 or NFSv4.2, including file servers, NAS devices, and cluster storage nodes. Fixes were released in Linux 6.12.117, 6.18.61, 7.3.2, and 7.4-rc1, requiring a kernel upgrade and reboot, while restricting access to TCP/2049 is presented as a temporary mitigation when immediate patching is impossible. The CVE is listed as publicly disclosed on November 20, 2026, but the supplied material provides no vulnerability analysis, exploit validation, or evidence of active exploitation, leaving those details dependent on OpenSec&\#x27;s account.

telegram · zaihuapd · Nov 27, 12:57

**「Background」** Linux nfsd is the in-kernel server that exports filesystems over NFS, commonly on TCP port 2049; NFSv4.1 and 4.2 are the relevant protocol versions for the reported flaw. A pre-authentication heap overflow occurs before access credentials are checked and can corrupt adjacent kernel memory, creating a potential path to privileged code execution. The vulnerability is traced back to Linux kernel 3.16, released in March 2014.

**「Operational impact」** Linux file servers, NAS appliances, and cluster storage nodes exposing nfsd over TCP/2049 with NFSv4.1 or 4.2 are at risk of unauthenticated kernel compromise and a root shell, requiring immediate upgrades to Linux 6.12.117, 6.18.61, 7.3.2, or 7.4-rc1 with a reboot, or temporary firewall restrictions on TCP/2049 where patching is not yet possible.

<details><summary>References</summary>
<ul>
<li><a href="https://opensec.in/blog/nfs2root-cve-2026-99362">NFS2 ROOT ( CVE - 2026 - 99362 ): pre -auth root in Linux nfsd | OpenSec</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/new-nfs2root-linux-flaw-can-let-attackers-gain-root-privileges/">New NFS2 ROOT Linux flaw can let attackers gain root privileges</a></li>

</ul>
</details>

**Tags**: `#Linux 内核`, `#NFS`, `#CVE-2026-99362`, `#远程代码执行`, `#漏洞修复`

---

<a id="item-tech-news-3"></a>
### [Google&\#x27;s DeepCrossAttention Targets Faster Transformer Inference](https://research.google/blog/supercharging-transformer-residual-connections/) ⭐️ 7.0/10

Google Research introduced DeepCrossAttention \(DCA\), an architecture that applies attention across transformer layers so tokens can use information from earlier layers rather than relying solely on conventional token-wise attention. The approach aims to reduce inference cost while maintaining comparable model quality, with the supplied account reporting performance up to three times faster. This could help developers run transformer models more efficiently, but the available evidence does not establish broad benchmark superiority or production readiness.

hackernews · ComputedCamp995 · Nov 27, 23:06 · [Discussion](https://news.ycombinator.com/item?id=50672565)

**「Background」** In standard transformers, attention mixes information across tokens within a sequence, while residual connections carry and combine representations through successive layers. DeepCrossAttention changes this depth-wise pathway by using learnable weights and cross-attention to dynamically combine outputs from earlier layers, which Google says helps counter information dilution in conventional residual connections.

**「Potential inference gains」** For developers serving transformer workloads, DeepCrossAttention’s reported ability to maintain comparable model quality while running up to 3× faster could reduce inference latency and compute costs. A public PyTorch implementation enables experimentation, but the supplied evidence does not establish broad benchmark coverage or production readiness.

**「Community Discussion」** One commenter suggested that cross-layer attention could help with multi-step reasoning problems such as the &quot;strawberry problem,&quot; although that remains speculative rather than a demonstrated result. Other participants compared the architecture conceptually with DenseNet and criticized the choice of line graphs, while an unrelated subscription-model discussion did not assess DCA.

<details><summary>References</summary>
<ul>
<li><a href="https://research.google/blog/supercharging-transformer-residual-connections/">Supercharging transformer residual connections</a></li>
<li><a href="https://github.com/Yuan-ManX/DeepCrossAttention-PyTorch/blob/main/README.md">DeepCrossAttention -PyTorch/README.md at main · Yuan-ManX ... -...</a></li>

</ul>
</details>

**Tags**: `#transformers`, `#attention mechanisms`, `#model inference efficiency`, `#deep learning research`

---

<a id="item-tech-news-4"></a>
### [WebRTC E-Skimming Scripts Found on Shopping Sites](https://www.infohawk.com/news/2026-11-27-black-friday-webrtc-skimmer) ⭐️ 7.0/10

A report says e-skimming scripts appeared on popular shopping sites and may use WebRTC as a channel to evade detection. The core risk is the ability of untrusted third-party JavaScript to run in shoppers’ browsers, not a flaw in WebRTC itself, because equivalent exfiltration could be attempted over ordinary HTTP requests. The available item provides no affected-site list or deeper technical analysis, leaving the campaign’s scope, evidence, and impact unclear.

hackernews · scanr · Nov 27, 15:40 · [Discussion](https://news.ycombinator.com/item?id=50668145)

**「Web skimming and WebRTC」** E-skimming, or web skimming, involves malicious code loaded by an online shop capturing payment-card details as customers enter them, often through compromised or untrusted third-party JavaScript. WebRTC is a browser API for peer-to-peer communication; the concern here is its use as a potentially less-monitored channel for exfiltrating stolen data, not a vulnerability in WebRTC itself, since malicious page-loaded scripts could perform similar requests through ordinary HTTP.

**「Practical consequences」** Shoppers on affected shopping sites could have payment-card details captured by malicious third-party scripts, with WebRTC providing a less-monitored exfiltration path. Merchants therefore need to control and audit embedded scripts and monitor WebRTC traffic, although disabling WebRTC alone would not prevent equivalent HTTP exfiltration.

**「Community Reactions」** Commenters broadly favored blocking, sandboxing, or more closely monitoring third-party scripts, with one commenter citing the incident as a reason to block ads. Some argued that the deeper problem is allowing remote code to run freely in the browser, while others questioned why advertising providers do not isolate ad code more effectively.

<details><summary>References</summary>
<ul>
<li><a href="https://sifirincidakika.com/haber/populer-alisveris-sitelerinde-webrtc-tabanli-kredi-karti-skimming-betikleri-bulundu">Popüler alışveriş sitelerinde WebRTC tabanlı kredi kartı skimming ...</a></li>

</ul>
</details>

**Tags**: `#WebRTC`, `#e-skimming`, `#third-party JavaScript`, `#browser security`, `#e-commerce`

---

<a id="item-tech-news-5"></a>
### [AWS Challenger: Trainium3 Inference and Microarchitecture Deep Dive](https://newsletter.semianalysis.com/p/trainium3-inferencex) ⭐️ 7.0/10

SemiAnalysis examines the microarchitecture of AWS&\#x27;s Trainium3 inference accelerator, analyzing its performance-per-cost and utilization characteristics versus NVIDIA&\#x27;s GB300 platform.

rss · Semianalysis · Nov 27, 15:54

**Tags**: `#AI hardware`, `#AWS Trainium`, `#inference accelerators`, `#microarchitecture`, `#semiconductors`

---

<a id="item-tech-news-6"></a>
### [Birmingham Oracle Failure Reaches £128 Million](https://www.theregister.com/public-sector/2026/11/27/bill-for-birminghams-oracle-debacle-reaches-128m/5312563) ⭐️ 6.0/10

The reported cost of Birmingham&\#x27;s failed Oracle-led enterprise resource planning replacement has reached £128 million. Further losses may arise from the delayed SAP replacement. The SAP delay is described as a factor that helped bankrupt the city, meaning the £128 million figure may not represent the final cost. The supplied account provides no cost breakdown, revised timetable, or evidence supporting a higher projected total.

rss · The Register · Nov 27, 14:03

**「ERP Replacement Context」** An enterprise resource planning system integrates core functions such as finance, procurement, and workforce management, making a failed replacement costly and operationally disruptive. Birmingham&\#x27;s program included an Oracle-led replacement followed by a delayed SAP replacement, so both the original failure and the subsequent delay contribute to the overall financial exposure.

**Tags**: `#enterprise software`, `#Oracle`, `#SAP`, `#public-sector IT`, `#project failure`

---

<a id="item-tech-news-7"></a>
### [Europe’s AI Push Has Cloud Ambition but Limited Sovereignty](https://www.theregister.com/ai-and-ml/2026/11/27/europes-ai-sovereignty-push-lots-of-cloud-not-much-silver-lining/5312120) ⭐️ 6.0/10

Europe’s data-center investment and cloud capacity are booming, but the analysis argues that this does not automatically translate into AI sovereignty. The models, AI chips, and industry influence remain concentrated in the United States and Asia, leaving Europe reliant on foreign technology providers and ecosystems. The result is a gap between Europe’s expanding infrastructure and its limited control over the hardware, models, and commercial power underpinning AI.

rss · The Register · Nov 27, 11:32

**「What AI Sovereignty Means」** AI sovereignty refers to a region’s ability to control the compute infrastructure, AI models, supply chains, and policy needed to pursue artificial intelligence independently rather than relying on foreign providers. Europe’s expanding cloud and data-center footprint can increase local access to computing capacity, but hosting infrastructure alone does not guarantee control over advanced chips, model development, or commercial influence.

**「Limited practical autonomy」** For European organizations, expanding cloud and data-center capacity may improve AI availability, but it will deliver little strategic autonomy while key models, chips, and industry influence remain concentrated in the US and Asia, potentially deepening reliance on foreign suppliers.

**Tags**: `#AI sovereignty`, `#data centers`, `#cloud computing`, `#AI chips`, `#AI policy`

---

<a id="item-tech-news-8"></a>
### [AI Boom Lengthens Optical Equipment Lead Times](https://www.theregister.com/networks/2026/11/27/ai-boom-leaves-network-operators-waiting-up-to-18-months-for-kit/5312366) ⭐️ 6.0/10

AI-driven data-center demand is tightening the supply of optical equipment and components, leaving some network operators waiting as long as 18 months for hardware. RETN reports that optical-equipment prices have risen by around 50% this year as telecommunications operators compete with data centers for components. The bottleneck increases both deployment delays and infrastructure costs for network operators.

rss · The Register · Nov 27, 10:45

**「Optical equipment demand」** AI data centers require high-capacity network connections, so their expansion places optical-networking components in demand from both data-center operators and telecommunications carriers. RETN, the international data-network platform connecting Europe and Asia that supplied the pricing observation, represents the operator side of this market, while separate reporting found fiber-optic prices in 2026 roughly six to ten times their 2025 levels amid AI-related demand.

**「Higher costs and deployment delays」** Network operators now face longer fiber and optical-equipment lead times and roughly 50% higher component prices as AI data centers compete for supply, increasing the risk of delayed network expansion and broadband or BEAD deployment schedules.

<details><summary>References</summary>
<ul>
<li><a href="https://retn.net/">RETN : Leading Data Network Platform Connecting Europe and Asia</a></li>
<li><a href="https://arstechnica.com/gadgets/2026/11/ukraines-fiber-optic-drones-get-squeezed-by-ai-data-center-demand/">Ukraine’s fiber- optic drones get squeezed by AI data center demand</a></li>
<li>AI buildout is straining broadband supply chains - CoBank</li>

</ul>
</details>

**Tags**: `#AI infrastructure`, `#networking hardware`, `#supply chains`, `#data centers`

---

<a id="item-tech-news-9"></a>
### [British social security system techies yank services offline following &\#x27;cyber incident&\#x27;](https://www.theregister.com/security/2026/11/27/british-social-security-system-techies-yank-services-offline-following-cyber-incident/5312522) ⭐️ 6.0/10

British social security technology staff took services offline following a cyber incident, while pensioners were assured that funds would arrive as normal.

rss · The Register · Nov 27, 10:01

**Tags**: `#cybersecurity`, `#government IT`, `#social security`, `#service outage`, `#UK`

---

<a id="item-tech-news-10"></a>
### [How cutting-edge prosthetics can help probe the human mind](https://www.technologyreview.com/2026/11/27/1149946/cutting-edge-prosthetics-allow-researchers-to-probe-the-human-mind/) ⭐️ 6.0/10

An early clinical trial is testing a prosthetic hand that connects to arm nerves and enables its user to move and feel with it independently at home.

rss · MIT Technology Review · Nov 27, 10:00

**Tags**: `#neurotechnology`, `#prosthetics`, `#sensory feedback`, `#peripheral nerve interfaces`, `#clinical trials`

---