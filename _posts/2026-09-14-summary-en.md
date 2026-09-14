---
layout: default
title: "Horizon Summary: 2026-09-14 (EN)"
date: 2026-09-14
lang: en
---

> From 73 items, 6 important content pieces were selected

---

**Technology News**
1. [Homebrew 7.0.0 Released with Official Native macOS GUI](#item-tech-news-1) ⭐️ 8.0/10
2. [Why is Google still serving dodgy ads?](#item-tech-news-2) ⭐️ 7.0/10
3. [Why 4-Hi HBM Wins on Inference Cost and DRAM Efficiency](#item-tech-news-3) ⭐️ 7.0/10
4. [Trump and Johnson push back as top AI CEOs back a slowdown](#item-tech-news-4) ⭐️ 7.0/10
5. [NVIDIA CUDA Moat Quantified: AMD Trails by Up to 42x on DeepSeek v4.1](#item-tech-news-5) ⭐️ 7.0/10

**Technology Blog**
1. [Slow developer experience will bottleneck fast models](#item-tech-blog-1) ⭐️ 6.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Homebrew 7.0.0 Released with Official Native macOS GUI](https://brew.sh/2026/09/13/homebrew-7.0.0/) ⭐️ 8.0/10

Homebrew 7.0.0 has been released, delivering an official native macOS GUI, faster install and upgrade performance, stricter sandboxing, and a built-in vulnerability/advisory database. The release drops support for macOS 10.15 and earlier, while Intel Macs are moved to Tier 3, meaning they will no longer receive new pre-compiled bottles. On Linux, the sandbox switches from Bubblewrap to Landlock. These changes significantly reshape platform support tiers and introduce first-party security tooling for the most widely used macOS package manager.

telegram · zaihuapd · Sep 13, 11:23

**「Background」** Homebrew is a free, open-source package manager originally created for macOS that has since expanded to Linux, and it is the de facto standard for installing command-line tools and developer software on Apple platforms. Major Homebrew releases \(such as the prior 5.0.0 and 5.1.0 lines\) have historically introduced architectural shifts — including the move to its own \`brew\` repository, bottle \(binary package\) infrastructure, and CI-driven builds — that redefine supported platforms, sandboxing models, and tier classifications for macOS versions and CPU architectures. Tier 3 in Homebrew&\#x27;s support model designates configurations that still receive fixes but no longer receive new prebuilt binaries, meaning affected users must build formulas from source.

**「Impact」** Users on macOS 10.15 or earlier must upgrade to macOS 11+ or migrate to an alternative such as MacPorts, while Intel Mac users immediately lose access to new pre-built bottles and will see Homebrew stop running on Intel Macs in or after September 2027.

<details><summary>References</summary>
<ul>
<li><a href="https://brew.sh/2026/09/13/homebrew-7.0.0/">Homebrew : 7 . 0 . 0</a></li>
<li><a href="https://github.com/Homebrew/brew/releases">Releases · Homebrew / brew</a></li>
<li><a href="https://brew.sh/2026/09/13/homebrew-7.0.0/">Homebrew: 7.0.0</a></li>
<li><a href="https://docs.brew.sh/Support-Tiers">Homebrew Documentation: Support Tiers</a></li>
<li><a href="https://daily.dev/posts/homebrew-7-0-0-cj7h7kzxv">Homebrew 7.0.0 | daily.dev</a></li>

</ul>
</details>

**Tags**: `#open-source`, `#developer-tools`, `#macOS`, `#package-management`, `#security`

---

<a id="item-tech-news-2"></a>
### [Why is Google still serving dodgy ads?](https://www.atomic14.com/2026/09/13/why-is-google-still-serving-dodgy-ads) ⭐️ 7.0/10

Examination of why Google continues to serve scam and AI-generated ads through AdSense and YouTube, highlighting publisher frustrations and the abuse of trusted cloud hosting domains.

hackernews · iamflimflam1 · Sep 13, 17:37 · [Discussion](https://news.ycombinator.com/item?id=49686445)

**Tags**: `#advertising`, `#google`, `#ad-fraud`, `#web-security`, `#platform-policy`

---

<a id="item-tech-news-3"></a>
### [Why 4-Hi HBM Wins on Inference Cost and DRAM Efficiency](https://newsletter.semianalysis.com/p/long-live-the-short-king-why-4-hi) ⭐️ 7.0/10

A SemiAnalysis technical analysis by Myron Xie argues that 4-hi HBM stacks can deliver the same memory bandwidth as taller HBM variants while using far fewer DRAM dies per package. Because inference workloads are typically more bandwidth-bound than capacity-bound, the piece contends that thinner stacks avoid over-provisioning memory capacity that AI accelerators cannot fully utilize when serving models rather than training them. Framing the configuration as a tool for cutting per-accelerator cost and stretching constrained DRAM supply during the current memory crunch, the analysis positions 4-hi HBM as economically attractive for buyers prioritizing inference economics over the maximum-capacity profiles that dominate training deployments. The argument rests on decoupling bandwidth from capacity in the inference regime, a distinction that has become more consequential as HBM demand has outpaced wafer supply.

rss · Semianalysis · Sep 13, 18:19

**「Background」** High Bandwidth Memory \(HBM\) vertically stacks multiple DRAM dies connected by through-silicon vias to deliver far higher bandwidth than conventional DDR memory, and it is the standard memory technology paired with modern AI accelerators from vendors such as AMD and NVIDIA as well as custom data-center ASICs. Stack height is conventionally described by the number of DRAM dies—8-hi and 12-hi configurations are common in current data-center GPUs—while 4-hi represents a thinner, lower-capacity option. Training workloads tend to be both capacity- and bandwidth-hungry, but large-scale inference is often dominated by bandwidth and latency requirements, which is the economic premise behind favoring shorter stacks.

**「Impact」** For cloud operators and AI accelerator buyers optimizing inference fleets, 4-hi HBM offers a route to equivalent bandwidth at lower per-package die cost and reduced DRAM consumption per system, which is meaningful while HBM supply remains tight. The trade-off only holds for models whose state fits within the smaller capacity envelope, so applicability depends on the size and serving patterns of the specific inference workload.

**Tags**: `#HBM`, `#AI-hardware`, `#semiconductor-memory`, `#DRAM`, `#inference-cost`

---

<a id="item-tech-news-4"></a>
### [Trump and Johnson push back as top AI CEOs back a slowdown](https://www.theverge.com/ai-artificial-intelligence/994441/trump-mike-johnson-ai-industry-overreacting) ⭐️ 7.0/10

Anthropic CEO Dario Amodei published a lengthy open letter calling to &quot;pace the frontier&quot; and slow down AI development, drawing public support from OpenAI&\#x27;s Sam Altman and Elon Musk on X, with Alphabet&\#x27;s Demis Hassabis offering tentative backing for the proposal. The unusual convergence of leading AI executives around a call for restraint marks a notable shift in industry rhetoric on frontier AI development. President Donald Trump and House Speaker Mike Johnson, however, characterized the industry response as an overreaction, dismissing the urgency of slowing AI progress. The split highlights a widening gap between the political leadership&\#x27;s posture toward AI regulation and the increasingly cautionary stance of the executives building frontier systems.

rss · The Verge · Sep 13, 19:41

**「Background」** Calls to slow or &\#x27;pause&\#x27; frontier AI development have been a recurring theme in AI policy debates since the Future of Life Institute&\#x27;s March 2023 open letter, which urged a six-month halt on training systems more powerful than GPT-4 and was signed by Musk and other prominent tech figures. Amodei&\#x27;s recent essay, &\#x27;We Must Pace the Frontier,&\#x27; revives this idea as a coordinated industry strategy, arguing that frontier labs need time to address safety and societal risks without sacrificing commercial or national competitiveness. The current alignment of Amodei \(Anthropic\), Altman \(OpenAI\), Musk \(xAI\), and Hassabis \(Google DeepMind\) is unusual because these leaders head direct competitors in the race to build more capable AI systems, making joint calls for restraint noteworthy.

**「Impact」** The political pushback from Trump and Johnson signals that US legislative action to slow frontier AI development is unlikely to advance on their watch, leaving corporate pacing decisions, voluntary commitments, and industry self-regulation as the near-term mechanisms shaping frontier AI rollout.

<details><summary>References</summary>
<ul>
<li><a href="https://darioamodei.com/post/we-must-pace-the-frontier">Dario Amodei — We Must Pace the Frontier</a></li>
<li><a href="https://www.bbc.com/news/articles/c14dpgm0rg4o">Anthropic boss Dario Amodei calls for AI development to slow down</a></li>
<li><a href="https://www.axios.com/2026/09/12/anthropic-ai-amodei-pacing">Anthropic, OpenAI CEOs call for slowdown in AI development</a></li>

</ul>
</details>

**Tags**: `#AI policy`, `#AI regulation`, `#AI industry`, `#AI safety`, `#US politics`

---

<a id="item-tech-news-5"></a>
### [NVIDIA CUDA Moat Quantified: AMD Trails by Up to 42x on DeepSeek v4.1](https://x.com/SemiAnalysis_/status/2098618867035557984) ⭐️ 7.0/10

SemiAnalysis has quantified NVIDIA&\#x27;s CUDA ecosystem advantage with new DeepSeek v4.1 Flash benchmarks, finding that AMD GPUs deliver up to 14.8x worse per-dollar performance than the NVIDIA H200 and up to 42x worse than B200/B300. The gap was underscored by CUDA&\#x27;s vLLM integration supporting the model just two days after release, while AMD&\#x27;s DeepSeek v4.1 Flash mirror image arrived later, though it worked out-of-the-box once available. SemiAnalysis attributes NVIDIA&\#x27;s lead to its ecosystem of roughly 6 million developers, which enables day-one kernel optimization for newly released models. The data substantiates the long-standing &quot;CUDA moat&quot; thesis with concrete, model-specific performance ratios relevant to AI infrastructure planning.

telegram · zaihuapd · Sep 13, 05:55

**「Background」** CUDA is NVIDIA&\#x27;s proprietary GPU computing platform, built over more than a decade into a mature ecosystem of compilers, libraries, and highly optimized kernels, while AMD&\#x27;s competing ROCm platform has historically lagged in software maturity and developer adoption. DeepSeek v4.1 Flash is a recent large language model release, and vLLM is a widely used open-source inference engine that serves LLMs efficiently on GPU hardware. Per-dollar performance comparisons normalize raw throughput differences against hardware acquisition cost, making them a key metric for hyperscale and enterprise AI deployment decisions.

**「Impact」** Organizations considering AMD accelerators for cost-efficient inference on newer models such as DeepSeek v4.1 Flash may face substantial per-dollar performance penalties until ROCm kernel optimization matures, reinforcing NVIDIA&\#x27;s pricing leverage in the AI accelerator market. The exact magnitude of the gap will depend on workload specifics and subsequent AMD software updates.

**Tags**: `#AI infrastructure`, `#GPU computing`, `#NVIDIA CUDA`, `#AMD ROCm`, `#DeepSeek`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [Slow developer experience will bottleneck fast models](https://seangoedecke.com/slow-devex-will-bottleneck-fast-models/) ⭐️ 6.0/10

Argues that as AI model inference becomes near-instantaneous, agent tool execution speed \(tests, file I/O, compilation\) will become the binding constraint on agentic coding workflows and revive interest in fast toolchains and DevEx investment.

rss · Sean Goedecke · Sep 14, 00:00

**Tags**: `#AI agents`, `#developer experience`, `#inference optimization`, `#agentic coding`, `#future of programming`

---