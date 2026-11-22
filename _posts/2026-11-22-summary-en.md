---
layout: default
title: "Horizon Summary: 2026-11-22 (EN)"
date: 2026-11-22
lang: en
---

> From 60 items, 8 important content pieces were selected

---

**Technology News**
1. [Reported Lean Verification of the Riemann Hypothesis](#item-tech-news-1) ⭐️ 9.0/10
2. [Zhejiang University Runs QRAM on a Superconducting Chip](#item-tech-news-2) ⭐️ 9.0/10
3. [USB Monitor Passthrough Throttled Downloads by 75%](#item-tech-news-3) ⭐️ 7.0/10
4. [Muru brings AI-assisted Rust tooling to Python servers](#item-tech-news-4) ⭐️ 7.0/10
5. [Anthropic’s IPO Tests Its Safety-First Positioning](#item-tech-news-5) ⭐️ 6.0/10
6. [Signal Restricts Mobile Screenshots Over AI Surveillance Concerns](#item-tech-news-6) ⭐️ 6.0/10
7. [FBI Investigates Reported NCIC Database Hack](#item-tech-news-7) ⭐️ 6.0/10

**Technology Blog**
1. [Avoiding Blunders in Software Design](#item-tech-blog-1) ⭐️ 6.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Reported Lean Verification of the Riemann Hypothesis](https://leanprover-community.github.io/blog/posts/riemann-hypothesis/) ⭐️ 9.0/10

Levent Alpöge reportedly published a Lean formalization of the Riemann Hypothesis on November 20, 2026, comprising roughly 17 million lines of code developed with assistance from Claude. On November 21, Lean FRO and the Mathlib Initiative reportedly stated that the formalized proposition matches Mathlib’s RiemannHypothesis, the codebase compiles without errors, and multiple independent proof checkers validated the proof. If confirmed, the result would be a major milestone for AI-assisted theorem proving and formal mathematics; however, the supplied material contains only community reports and a relayed announcement, not an independent audit of the repository and proof. Multiple checker implementations and consistency proofs were cited as safeguards against a single prover or kernel bug yielding a spurious verification.

hackernews · g-b-r · Nov 21, 14:36 · [Discussion](https://news.ycombinator.com/item?id=50589618)

**「Background」** The Riemann Hypothesis states that every nontrivial zero of the Riemann zeta function has real part 1/2. Lean is an interactive theorem prover whose trusted kernel can mechanically check proof terms, allowing large mathematical developments to be encoded as reusable libraries rather than informal arguments. The reported project by Levent Alpöge was released as a Lean library on November 20, 2026, comprising about 17 million lines of code.

**「Impact」** If the reported certification holds, Alpöge’s 17-million-line Lean artifact makes the Riemann Hypothesis independently machine-checkable and provides a substantial benchmark for scalable, AI-assisted formal proof, while giving mathematicians and proof-system developers a reusable codebase to audit and extend.

**「Community reaction」** Commenters viewed verification across several independently implemented kernels with consistency proofs as strong protection against a checker-specific bug, while noting that fake proofs have previously passed individual checkers and that checker independence may be overstated. They credited Alpöge’s human oversight and ability to direct Claude, but said the supplied evidence did not independently resolve every validity concern.

<details><summary>References</summary>
<ul>
<li><a href="https://leanprover-community.github.io/blog/posts/riemann-hypothesis/">Lean verification of the Riemann Hypothesis | Lean community blog</a></li>
<li><a href="https://casrai.org/news/anthropic-levent-alpoge-claude-lean-riemann-hypothesis-claim-2026">175,000-File Lean Riemann Hypothesis Proof Claim — CASRAI</a></li>
<li><a href="https://thedefiant.io/frontier/ai/lean-groups-certify-claude-assisted-riemann-proof">Lean Groups Certify Claude-Assisted Riemann Proof | Frontier</a></li>
<li><a href="https://www.datastudios.org/post/claude-riemann-hypothesis-proof-lean-community-certifies-levent-alpoge">Claude-assisted Riemann hypothesis proof certified by Lean ...</a></li>

</ul>
</details>

**Tags**: `#formal verification`, `#Lean`, `#Riemann Hypothesis`, `#AI-assisted theorem proving`, `#mathematical foundations`

---

<a id="item-tech-news-2"></a>
### [Zhejiang University Runs QRAM on a Superconducting Chip](https://finance.sina.com.cn/stock/2026-11-21/doc-iniznhsk3530826.shtml) ⭐️ 9.0/10

According to a Sina Finance report, a Zhejiang University team has implemented what it describes as the world’s first QRAM prototype running on real hardware: the team’s self-developed “Tianmu-2” superconducting quantum chip. The researchers successfully operated 4-bit and 8-bit prototypes with reported accuracies of 80.9% and 60.4%, respectively. They also reported reducing circuit depth by more than 30% compared with an unoptimized design and experimentally verified that the architecture has local noise resilience. Published in Nature Physics, the work is an early-stage result with limited bit width, and the team plans to continue scaling up the QRAM implementation.

telegram · zaihuapd · Nov 21, 08:31

**「QRAM and quantum memory」** Quantum random-access memory \(QRAM\) is the quantum counterpart of conventional random-access memory, storing quantum states so that algorithms can retrieve selected data while aiming to preserve quantum coherence. The bucket-brigade architecture used in the reported prototype transfers information through successive storage cells, making transfer errors, circuit depth, and protection against local noise central scaling challenges; its 4-bit and 8-bit configurations contain 16 and 256 storage cells, respectively.

**「Practical impact」** Quantum-computing researchers now have a real superconducting-chip testbed for evaluating QRAM designs under limited bit widths and local noise, with the reported prototypes reducing circuit depth by more than 30% compared with unoptimized designs. Near-term utility remains constrained by the 4-bit and 8-bit demonstrations’ 80.9% and 60.4% accuracies, making the result a research milestone rather than a production-scale quantum memory.

<details><summary>References</summary>
<ul>
<li><a href="https://news.mydrivers.com/1/1167/1167501.htm">news.mydrivers.com/1/1167/1167501.htm</a></li>

</ul>
</details>

**Tags**: `#量子计算`, `#QRAM`, `#超导量子芯片`, `#量子存储`

---

<a id="item-tech-news-3"></a>
### [USB Monitor Passthrough Throttled Downloads by 75%](https://blog.tymscar.com/posts/studiodisplayethernet/) ⭐️ 7.0/10

The post documents a case where Ethernet traffic routed through a USB monitor’s passthrough reduced download throughput by 75%. The added latency delayed packet acknowledgements enough for an adapter buffer to fill, causing packet loss and severe throttling. Replacing the Ethernet adapter with one that required less frequent acknowledgements resolved the slowdown. The case illustrates how an unexpected component in a USB networking path can masquerade as an ISP or bandwidth problem.

hackernews · soheilpro · Nov 21, 10:36 · [Discussion](https://news.ycombinator.com/item?id=50587875)

**「USB Ethernet Acknowledgement Latency」** A USB Ethernet connection routed through a monitor can add latency between the network interface and the host while receiving packets. If acknowledgements are delayed, the interface’s DMA buffers can fill and drop packets, reducing throughput even when the underlying internet connection is fast.

**「Practical consequence」** Users relying on Ethernet pass-through in a USB monitor experienced a 75% download-speed reduction because added latency delayed packet acknowledgements, filled the Ethernet adapter’s buffers, and caused packet drops; switching Ethernet adapters resolved the slowdown. Because the problem depends on the adapter and connection path, testing a direct or different Ethernet adapter is a practical troubleshooting step before blaming the broadband service.

**「Community Discussion」** Some readers initially focused on the monitor itself, while others clarified that the relevant failure was delayed acknowledgements and packet loss within the USB Ethernet path. A commenter reported a superficially similar issue with a multigig copper SFP+ module that negotiated a lower line rate and dropped packets, while another compared the opaque throttling to Ghostty’s io\_uring-related I/O pressure on Linux.

<details><summary>References</summary>
<ul>
<li><a href="https://news.ycombinator.com/item?id=50587875">My monitor was cutting my download speed by 75 % | Hacker News</a></li>
<li><a href="https://blog.tymscar.com/posts/studiodisplayethernet/">My Monitor Was Cutting My Download Speed by 75% :: The ...</a></li>
<li><a href="https://www.weylan-d.com/blog/detail/7221/">usb to ethernet chip causes packet loss | Weyland</a></li>

</ul>
</details>

**Tags**: `#USB networking`, `#packet loss`, `#performance debugging`, `#Ethernet`

---

<a id="item-tech-news-4"></a>
### [Muru brings AI-assisted Rust tooling to Python servers](https://simonwillison.net/2026/Nov/21/muru/) ⭐️ 7.0/10

Muru is a new AI-assisted Rust server created by Graham Dumpleton to run both ASGI and WSGI Python applications in development and production. Dumpleton, who started mod\_wsgi 20 years ago, has published 18 detailed design posts since November 4, 2026, covering workers, process forking, HTTPS, combined WSGI and ASGI support, releases, canaries, containers, Kubernetes, autoscaling, overlays, monitoring, and a toolbar with tracing. He says AI handles much of the surface-level work while he judges whether the results are good enough and continues polishing the project. The supplied account provides no benchmarks, maturity assessment, or adoption evidence, so Muru&\#x27;s practical performance and production readiness remain unverified.

rss · Simon Willison · Nov 21, 23:56

**「Python web-server context」** WSGI is the traditional interface for hosting synchronous Python web applications and was created in 2003, while ASGI provides an asynchronous counterpart capable of supporting protocols such as WebSockets. Graham Dumpleton, creator of mod\_wsgi, is applying two decades of Python deployment experience to Muru, a Rust-based routing edge, control plane, and runtime for serving both WSGI and ASGI applications.

**「Potential deployment impact」** For teams deploying Python ASGI or WSGI applications, Muru could consolidate routing, zero-downtime releases, traffic management, and Python-aware process management within a Rust-based runtime. However, the source provides no benchmarks, maturity assessment, or adoption evidence, so its performance and production readiness remain unverified.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.muruhq.dev/">Muru</a></li>
<li><a href="https://grahamdumpleton.me/">Home - Graham Dumpleton</a></li>
<li><a href="https://www.youtube.com/watch?v=CPz0s1CQsTE">Graham Dumpleton - Secrets of a WSGI master. - YouTube</a></li>
<li><a href="https://docs.muruhq.dev/">Muru ¶</a></li>
<li><a href="https://github.com/GrahamDumpleton/muru">GitHub - GrahamDumpleton/muru: Routing edge, control plane ...</a></li>

</ul>
</details>

**Tags**: `#Python`, `#Rust`, `#ASGI`, `#WSGI`, `#AI-assisted development`

---

<a id="item-tech-news-5"></a>
### [Anthropic’s IPO Tests Its Safety-First Positioning](https://www.theverge.com/podcast/1038701/anthropic-ipo-ai-safety-openai-nvidia-structure) ⭐️ 6.0/10

In the third and final episode of The Verge’s “AI in real life” series, senior AI reporter Hayden Field examines how Anthropic’s public-company structure may affect its safety-first positioning. The AI lab behind Claude went public on the Nasdaq, and the episode focuses less on the scale of the IPO’s financial figures than on the pressure of operating as a public company. The discussion highlights the tension between maintaining a safety-focused mission and meeting the expectations of investors. The supplied excerpt does not include enough detail to determine which specific commitments, governance mechanisms, or policy changes are under consideration.

rss · The Verge · Nov 21, 15:00

**「Anthropic’s governance structure」** Anthropic created a Long-Term Benefit Trust in 2023 to oversee its business practices and established a public benefit fund containing about 847 million Class N shares. Its public-benefit-corporation status and unusual Nasdaq governance arrangement place majority control of the board in the hands of external trustees, while potentially limiting management’s ability to maximize shareholder returns. This structure provides the context for examining whether pressure to meet public-market expectations could conflict with Anthropic’s safety-first commitments.

**「IPO pressures Anthropic’s safety pledge」** For Anthropic, going public introduces greater pressure to deliver profits while managing enormous compute commitments, placing its safety-first and public-benefit commitments under increased shareholder scrutiny rather than guaranteeing a policy change.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/10/28/anthropic-pbc-what-its-structure-means-for-investors-.html">Anthropic PBC: What its structure means for investors - CNBC</a></li>
<li><a href="https://www.morningstar.com/stocks/anthropic-after-ipo-who-controls-company">Anthropic: After the IPO, Who Controls the Company? - Morningstar</a></li>
<li><a href="https://www.ft.com/content/9536c7b9-c600-48ec-8fe2-453b0ca187e9?syn-25a6b1a6=1">Anthropic’s IPO set to test external trust with power over board</a></li>
<li><a href="https://techcrunch.com/2026/11/19/anthropics-ipo-puts-ais-circular-financing-boom-to-the-test/">Anthropic’s IPO puts AI’s circular financing boom to the test</a></li>
<li><a href="https://apnews.com/article/anthropic-ipo-public-benefit-corp-a2a04c9bcf681c1b46b13607171c83b4">Anthropic&#x27;s Wall Street debut will test its pledge to ...</a></li>

</ul>
</details>

**Tags**: `#Anthropic`, `#AI safety`, `#AI industry`, `#IPO`

---

<a id="item-tech-news-6"></a>
### [Signal Restricts Mobile Screenshots Over AI Surveillance Concerns](https://techcrunch.com/2026/11/21/signal-restricts-mobile-screenshots-as-it-confronts-existential-threat-of-ai-surveillance/) ⭐️ 6.0/10

Signal is limiting users’ ability to take screenshots in both its Android and iOS apps. The company frames the restriction as a response to the threat posed by AI-enabled surveillance. It represents a cross-platform privacy and mobile-security change, but the supplied material does not explain how the restriction works, which app versions or devices are affected, or whether exceptions remain. The source also provides no implementation details or evidence that other messaging platforms are following suit.

rss · TechCrunch · Nov 21, 21:37

**「Background」** AI agents can potentially extract private chat content from screenshots captured on a phone screen. Signal had already blocked screenshots in its Windows app by default, and its new Android and iOS restrictions extend that earlier protection, although users can disable the setting and Signal describes the approach as incomplete because other, subtler access methods remain.

**「Practical privacy impact」** With screenshot blocking enabled, supported iOS and Android devices will prevent mobile assistants from capturing visible Signal chats, reducing one AI-assisted surveillance pathway. The protection is incomplete and device-dependent, and disabling it weakens Signal’s stated privacy guarantees.

<details><summary>References</summary>
<ul>
<li><a href="https://techcrunch.com/2026/11/21/signal-restricts-mobile-screenshots-as-it-confronts-existential-threat-of-ai-surveillance/">Signal restricts mobile screenshots as it confronts ...</a></li>
<li><a href="https://tech.yahoo.com/cybersecurity/articles/signal-restricts-mobile-screenshots-confronts-213710971.html">Signal restricts mobile screenshots as it confronts ...</a></li>
<li><a href="https://www.reuters.com/legal/litigation/signal-restricts-screenshots-block-ai-agents-reading-messages-2026-11-20/">EXCLUSIVE: Signal restricts screenshots to block AI agents ...</a></li>
<li><a href="https://cybersecuritynews.com/signal-restricts-screenshots/">Signal Restricts Screenshots to protect User Privacy from AI ...</a></li>
<li><a href="https://tech.yahoo.com/cybersecurity/articles/signal-restricts-mobile-screenshots-confronts-213710971.html">Signal restricts mobile screenshots as it confronts ...</a></li>
<li><a href="https://www.unite.ai/signal-adds-screenshot-restrictions-to-limit-mobile-ai-data-capture/">Signal Adds Screenshot Restrictions to Limit Mobile AI Data ...</a></li>

</ul>
</details>

**Tags**: `#privacy`, `#mobile security`, `#AI surveillance`, `#Signal`

---

<a id="item-tech-news-7"></a>
### [FBI Investigates Reported NCIC Database Hack](https://techcrunch.com/2026/11/21/trump-says-reported-fbi-database-hack-is-not-good/) ⭐️ 6.0/10

President Donald Trump said a reported hack of the FBI’s National Crime Information Center was “not good.” The FBI is reportedly investigating the incident, but the available report provides no technical details, confirmed impact, affected records, or timeline. The unspecified scope leaves the potential consequences for criminal investigations and public safety unresolved.

rss · TechCrunch · Nov 21, 18:44

**「NCIC overview」** The National Crime Information Center \(NCIC\) is a computerized law-enforcement database available to local, state, and federal agencies. It contains records on fugitives, missing persons, criminal histories, stolen property, and other topics, making it important for investigations and interagency coordination.

**「Operational Impact」** The suspected NCIC intrusion could disrupt or raise integrity concerns for federal, state, and local law-enforcement agencies that rely on the nationwide criminal-information system. The FBI is still investigating, and no confirmed data loss, service outage, or exploitation has been established.

<details><summary>References</summary>
<ul>
<li><a href="https://www.usatoday.com/story/news/crime/2026/11/21/donald-trump-ncic-breach-fbi/92897372007/">Donald Trump calls second FBI system breach &#x27;not good&#x27;</a></li>
<li><a href="https://apnews.com/article/fbi-database-ncic-hack-d066cff87a64a564db0a00172c124972">FBI probing hack of its national criminal justice database ...</a></li>
<li><a href="https://www.thegatewaypundit.com/2026/11/breaking-fbis-national-crime-database-hacked/">BREAKING: FBI ’s National Crime Database Has Been Hacked * The...</a></li>
<li><a href="https://www.theguardian.com/us-news/2026/nov/21/usda-fbi-outages-cyber-attack">USDA, FBI breached by hackers amid spate of tech... | The Guardian</a></li>

</ul>
</details>

**Tags**: `#cybersecurity`, `#FBI`, `#NCIC`, `#government systems`, `#data breach`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [Avoiding Blunders in Software Design](https://seangoedecke.com/to-code-well-avoid-blunders/) ⭐️ 6.0/10

rss · Sean Goedecke · Nov 22, 00:00

**「Background」** Sean Goedecke argues that excellent programming depends less on discovering brilliant abstractions than on avoiding catastrophic design mistakes, particularly in large commercial codebases maintained by big teams. In software, unlike a game where a blunder may merely narrow the lead, one mistake can turn an otherwise elegant codebase into a janky one.

**「Solution」** He identifies two cardinal dangers: inconsistency and unnecessary requirements. Examples of blunders include adding a parallel system for an existing job, creating a second source of truth, making a safe synchronous operation delicate and asynchronous, adding subtle failure modes, and complicating an important interface. Requirements are especially dangerous because they are sticky—once embedded, engineers must assume they are necessary—and because features that interact with them create combinatorial complexity in large codebases. His prescription is to fit each task as naturally as possible into the existing code, reduce it to the smallest necessary requirements, and spend effort on details rather than clever patterns or extra features; he says this guidance applies to both hand-written code and AI agents, while mainly addressing “impure engineering” in large commercial teams. He also notes that current coding agents are about as good as humans at consistency but worse at avoiding unnecessary requirements.

**「Takeaway」** The article’s central thesis is that durable software comes from preserving consistency and minimizing requirements, not from showcasing cleverness; the safest route to good work is to notice and avoid blunders.

**Tags**: `#software design`, `#maintainability`, `#technical debt`, `#requirements management`, `#large codebases`

---