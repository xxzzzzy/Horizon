---
layout: default
title: "Horizon Summary: 2026-09-10 (EN)"
date: 2026-09-10
lang: en
---

> From 136 items, 17 important content pieces were selected

---

**Technology News**
1. [vLLM v0.29.0 Released with Model Runner V2 Default and Kimi K3 Optimizations](#item-tech-news-1) ⭐️ 8.0/10
2. [4 groups caught using the same Chrome and Windows exploit kit](#item-tech-news-2) ⭐️ 8.0/10
3. [OpenAI claims Navier-Stokes breakthrough amid attribution dispute](#item-tech-news-3) ⭐️ 8.0/10
4. [WeChat zero-click worm spread via unanswered VoIP calls, patched by Tencent](#item-tech-news-4) ⭐️ 8.0/10
5. [Shopify acquires Tailwind CSS framework](#item-tech-news-5) ⭐️ 7.0/10
6. [GPT-6 Astra, Looped Transformers, and Hidden Reasoning](#item-tech-news-6) ⭐️ 7.0/10
7. [Six Chinese AI firms accused of aggressively copying US frontier models](#item-tech-news-7) ⭐️ 7.0/10
8. [Apple unveils $1,999 iPhone Duo as its first foldable iPhone](#item-tech-news-8) ⭐️ 7.0/10
9. [Google&\#x27;s AlphaGenome Atlas evaluates every possible single-base change in the human genome](#item-tech-news-9) ⭐️ 7.0/10
10. [Automattic CEO Matt Mullenweg placed on paid leave](#item-tech-news-10) ⭐️ 7.0/10
11. [Apple unveils Watch Series 12 and Watch Ultra 4 with an AI upgrade that can recap your day](#item-tech-news-11) ⭐️ 7.0/10
12. [SemiAnalysis Examines On-Device vs Datacenter Inference for Robotics](#item-tech-news-12) ⭐️ 6.0/10
13. [IBM releases Granite Time Series PatchTST-FM-r2 under permissive license](#item-tech-news-13) ⭐️ 6.0/10
14. [Analog Devices Bolsters Its &quot;Physical Intelligence&quot; Plans, Splashes $1.35B on Alif Semiconductor - hackster.io](#item-tech-news-14) ⭐️ 6.0/10

**Financial News**
1. [Ant International, Visa and Mastercard team up on standards for AI-agent payments](#item-finance-news-1) ⭐️ 7.0/10
2. [Adani Enterprises rises ~5% as airport unit raises $1 billion at $18 billion valuation](#item-finance-news-2) ⭐️ 7.0/10
3. [Chinese EV makers pivot to humanoid robots amid profit squeeze](#item-finance-news-3) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [vLLM v0.29.0 Released with Model Runner V2 Default and Kimi K3 Optimizations](https://github.com/vllm-project/vllm/releases/tag/v0.29.0) ⭐️ 8.0/10

vLLM v0.29.0 was released with 594 commits from 277 contributors, making Model Runner V2 \(MRV2\) the default architecture for all models and completing the multi-release rollout that began with pooling models. The release adds support for several new frontier models including Hy4-preview \(a 770B/49B-active MoE with Gated DeepSeek Sparse Attention and native MTP\), Qwen3.8-Flash-Next \(BF16/FP8/NVFP4 with MTP\), GraniteSWA and GraniteMoeSWA, NemotronH\_Omni\_Reasoning\_V3, and Kimi K3 NVFP4 checkpoints. Significant performance optimizations target Kimi K3 and DeepSeek V4, including fused MXFP4 top-k finalization \(~5% E2E latency reduction\), Mamba metadata preparation in a single Triton launch \(6.6-7.6x kernel speedup\), tuned Hopper low-latency GEMM now dispatched on SM100 with 12.9-25.2% speedup on eh\_proj, and MLA gate merged into the QKV-A projection. Additional improvements include speculative decoding per-request acceptance stats, a new sharded\_rdt P2P backend for RL weight sync, Mamba prefix caching delivering 9-25% TTFT improvement, FlashInfer all-reduce enabled by default, and breaking changes such as removal of ten deprecated model architectures and deprecation of \`python -m vllm.entrypoints.openai.api\_server\` in favor of \`vllm serve\`.

github · khluu · Sep 9, 08:54

**「Background」** vLLM is one of the most widely used open-source frameworks for high-throughput, low-latency LLM inference and serving. Model Runner V2 \(MRV2\) is a redesigned execution architecture that vLLM has been rolling out over multiple releases to improve memory efficiency, CUDA graph support, and feature coverage; until v0.29.0 it had been adopted incrementally, starting with pooling models before becoming the project-wide default.

**「Impact」** Operators deploying vLLM in production now run MRV2 by default, which changes per-step logits memory usage by a factor of 1/TP through batch-sharded sampling and enables automatic KV cache sizing via CUDA graph memory profiling, while MRV1 remains available only for a few ROCm models lacking MRV2 feature parity.

**Tags**: `#LLM Inference`, `#vLLM`, `#Open Source`, `#AI Infrastructure`, `#Model Serving`

---

<a id="item-tech-news-2"></a>
### [4 groups caught using the same Chrome and Windows exploit kit](https://arstechnica.com/information-technology/2026/09/4-groups-caught-using-the-same-chrome-and-windows-exploit-kit/) ⭐️ 8.0/10

Proofpoint researchers reveal BlueMoon, an exploit kit chaining two Chromium bugs and a Windows kernel flaw, used by at least four hacking groups including some with ties to China, with patches for all three vulnerabilities released within 24 hours.

rss · Ars Technica · Sep 9, 20:55

**Tags**: `#cybersecurity`, `#vulnerability-disclosure`, `#exploit-kit`, `#chrome`, `#windows`

---

<a id="item-tech-news-3"></a>
### [OpenAI claims Navier-Stokes breakthrough amid attribution dispute](https://www.theverge.com/ai-artificial-intelligence/992953/openai-math-millennium-prize-navier-stokes) ⭐️ 8.0/10

OpenAI announced that its AI agents have produced a proof addressing the Navier–Stokes existence and smoothness problem—one of the seven Millennium Prize Problems posed by the Clay Mathematics Institute in 2000—showing that the full Navier–Stokes equations can break down. The result was achieved using an internal model that the company says dramatically outperforms the Astra model released the previous week, requiring roughly 10,000 concurrent agents and millions of dollars in compute, though OpenAI says it will not claim the $1 million prize. The announcement was quickly complicated by NYU mathematician Tristan Buckmaster&\#x27;s claim that OpenAI employees offered him two options: post his and Levent Alpöge&\#x27;s related proof immediately so OpenAI could publish the following day, or collaborate on a joint paper that excluded Alpöge due to his affiliation with Anthropic. OpenAI, including chief research officer Mark Chen and technical staff member Sébastien Bubeck, has denied that its agents accessed or were trained on Buckmaster and Alpöge&\#x27;s work, though both proofs independently rely on an approach pioneered by mathematicians Diego Córdoba and Luis Martínez-Zoroa. The episode highlights mounting concern among mathematicians that frontier AI labs with proprietary models and vast compute may be displacing human researchers in the field.

rss · The Verge · Sep 9, 21:16

**「Background」** The Navier–Stokes equations describe how fluids such as water and air flow, but mathematicians had not determined whether they might, under some conditions, predict impossible states like a fluid having infinite velocity. The Millennium Prize Problems are seven open questions selected by the Clay Mathematics Institute in 2000, each carrying a $1 million reward; before this announcement, only one—Poincaré&\#x27;s conjecture—had been solved.

**「Impact」** The most concrete consequence is that mathematicians are publicly confronting a near-term future in which only a handful of frontier AI companies possess the proprietary models and multi-million-dollar compute needed to crack the field&\#x27;s hardest problems. Substantial uncertainty remains over whether OpenAI&\#x27;s agents worked independently or were influenced by Buckmaster and Alpöge&\#x27;s prior work, since OpenAI has denied access but has not disclosed evidence that rules out training on the transcripts.

**Tags**: `#AI`, `#machine-learning`, `#mathematics`, `#research`, `#OpenAI`

---

<a id="item-tech-news-4"></a>
### [WeChat zero-click worm spread via unanswered VoIP calls, patched by Tencent](https://www.theregister.com/security/2026/09/09/wechat-worm-could-pwn-a-friend-before-they-even-answered-the-call/5295234) ⭐️ 8.0/10

Security research team Calif released a demonstration of &quot;WeWorm,&quot; described as the first zero-click worm to spread through WeChat calls across both iOS and Android. The exploit fires before the recipient answers and still succeeds even if they pick up, with the victim reportedly hearing nothing on the call. Calif says AI assistance helped locate the underlying VoIP memory bug and produce the initial remote code execution exploit in roughly two days, with the worm component taking an additional week to build, a pace the researchers attribute to AI handling most of the technical work. Tencent, which operates WeChat, has since patched the vulnerability. The research was originally published at calif.io/research/weworm and reported by The Register.

rss · The Register · Sep 9, 12:45

**「Background」** WeChat is a cross-platform messaging and calling application operated by Tencent with over a billion active users, making vulnerabilities in it potentially affect a very large population across both iOS and Android. A zero-click remote code execution \(RCE\) exploit triggers without any action by the victim, while a worm variant additionally self-replicates from each compromised device to new targets—in this case spreading through incoming WeChat VoIP calls before the recipient answers. Calif Research also emphasized that AI-assisted vulnerability discovery and exploit development can compress timelines dramatically, taking their team from finding a memory-corruption bug in WeChat&\#x27;s VoIP stack to a working cross-platform RCE in about two days and to a self-spreading worm within roughly another week.

**「Impact」** Tencent has patched the WeChat vulnerability exploited by the AI-assisted WeWorm demo, mitigating a risk that could otherwise have compromised WeChat&\#x27;s more than one billion accounts through an unanswered VoIP call. The demonstration also illustrates that AI-assisted exploit development can compress worm construction from a multi-person, months-long effort to about one week, raising the baseline speed at which defenders must respond to similar memory-corruption bugs.

<details><summary>References</summary>
<ul>
<li><a href="https://calif.io/research/weworm">The first zero - click worm to spread through WeChat calls across iOS...</a></li>
<li><a href="https://www.1950.ai/post/wechat-zero-click-worm-how-ai-turned-a-voip-vulnerability-into-a-self-spreading-account-hijacking-t">WeChat Zero - Click Worm : How AI Turned a VoIP Vulnerability Into...</a></li>
<li><a href="https://cyberinsider.com/zero-click-worm-spreads-on-iphones-and-android-via-wechat-calls/">Zero - click worm spreads on iPhones and Android via WeChat calls</a></li>
<li><a href="https://arxiv.org/html/2606.03811v1">AI Agents Enable Adaptive Computer Worms</a></li>
<li><a href="https://www.esecurityplanet.com/artificial-intelligence/news-ai-wechat-worm-billion-accounts-apac-china/">AI-Assisted WeChat Worm Risks 1 Billion Accounts</a></li>

</ul>
</details>

**Tags**: `#security`, `#zero-click-rce`, `#wechat`, `#ai-assisted-exploitation`, `#vulnerability-research`

---

<a id="item-tech-news-5"></a>
### [Shopify acquires Tailwind CSS framework](https://tailwindcss.com/blog/tailwind-is-joining-shopify) ⭐️ 7.0/10

Shopify has acquired Tailwind CSS, the widely used open-source utility-first CSS framework, with the deal announced on the Tailwind blog. The acquisition follows significant business pressure on Tailwind Labs, including January layoffs that reportedly affected roughly 75% of its engineering team and were attributed by founder Adam Wathan to the impact of AI on the company&\#x27;s commercial offerings. Tailwind&\#x27;s documentation traffic had reportedly fallen about 40% from early 2023 even as the framework itself continued to grow in popularity, eroding the funnel that once fed users toward paid products such as Tailwind UI and template packs. Community framing characterizes the deal primarily as Shopify buying the team and the brand rather than a thriving SaaS business, given how much of the commercial layer has been hollowed out by AI-assisted design and code generation. Specific financial terms, the size of the team moving to Shopify, and any roadmap changes for Tailwind CSS were not detailed in the available announcement.

hackernews · EdwinHoksberg · Sep 9, 13:27 · [Discussion](https://news.ycombinator.com/item?id=49626190)

**「Background」** Tailwind CSS is a utility-first CSS framework, originally released around 2017 by Adam Wathan and the Tailwind Labs team, that lets developers compose styles directly in HTML using predefined utility classes instead of writing custom CSS rules. Tailwind Labs ran a dual model: the framework itself was distributed under a permissive open-source license, while monetization came from paid products such as Tailwind UI, Refactoring UI, and component/template libraries built on top of the framework. The combination of AI-assisted code generation, falling documentation traffic, and easier reproduction of polished UI templates has compressed the commercial side of many DevTools companies whose paid offerings sit a thin layer above a popular free library.

**「Impact」** Existing Tailwind CSS users can likely expect the open-source framework to remain free and continue under Shopify&\#x27;s ownership, with deeper integration into Shopify&\#x27;s merchant and storefront tooling the most probable direction. The acquisition is a concrete signal that the traditional open-source-plus-paid-templates DevTools business model is structurally harder to sustain as AI tools commoditize the adjacent paid products.

**「Community discussion」** Commenters broadly attribute the deal to AI disruption, citing the 75% layoffs and ~40% docs traffic decline as evidence that the template-based commercial layer could no longer be defended. Some respondents question whether utility-first CSS is still necessary given modern vanilla CSS features such as container queries, custom properties, and cascade layers, while others credit Tailwind with sharpening their design and HTML skills. A recurring thread argues that DevTools companies now need a &quot;scale&quot; moat like hosting or managed infrastructure to survive, since the commercial wrapper around a popular open-source library can increasingly be generated rather than purchased.

**Tags**: `#acquisition`, `#open-source`, `#web-development`, `#ai-impact`, `#css-framework`

---

<a id="item-tech-news-6"></a>
### [GPT-6 Astra, Looped Transformers, and Hidden Reasoning](https://magazine.sebastianraschka.com/p/gpt-6-astra-looped-transformers-and) ⭐️ 7.0/10

Sebastian Raschka published an analytical piece synthesizing reported developments about OpenAI&\#x27;s &quot;GPT-6 Astra&quot; with technical context on looped transformer architectures and hidden reasoning approaches in LLMs. The article contextualizes claims from The Information about &quot;recurrent depth&quot; or &quot;looped transformers,&quot; explaining how weight-reused looped layers relate to standard stacked transformer blocks and what they imply for chain-of-thought monitoring. Raschka also discusses hidden reasoning techniques and the computational requirements of chain-of-thought computation, grounding the discussion in current research literature. The piece is commentary and synthesis rather than an original announcement, as OpenAI has not confirmed the reported details.

hackernews · ModelForge · Sep 9, 14:37 · [Discussion](https://news.ycombinator.com/item?id=49627370)

**「Background」** Looped \(or recurrent-depth\) transformers apply the same set of transformer weights iteratively across multiple passes to refine a representation, effectively trading extra compute for memory savings compared to stacking new layers with distinct weights. Chain-of-thought reasoning extends a transformer&\#x27;s computational power by emitting intermediate tokens as a scratchpad, with the amount of added expressiveness depending on how many intermediate steps are produced during inference. When this iterative computation is kept internal rather than surfaced as text, it is described as &quot;hidden reasoning,&quot; because the multi-pass reasoning trace lives inside the model&\#x27;s forward passes but is not directly observable in its outputs.

**「Impact」** For AI practitioners and ML researchers, Raschka&\#x27;s analysis demystifies the &quot;looped transformer&quot; concept by showing it is functionally equivalent to stacking transformer layers while sharing weights to save GPU memory, which clarifies why chain-of-thought monitoring becomes harder in such designs.

**「Community Discussion」** Commenters broadly endorse Raschka&\#x27;s framing, with libraryofbabel reinforcing that looped transformers are essentially weight-shared stacked layers rather than a novel &quot;secret technique,&quot; while shawntan points to Will Merrill&\#x27;s papers on the computational requirements of chain-of-thought reasoning. Other commenters diverge, with siva7 expressing concern about a reported regression from &quot;Astra&quot; to &quot;Sol,&quot; and andai highlighting an MS Paint computer-use demo as a striking real-time demonstration.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/html/2604.07822">Loop , Think, &amp; Generalize: Implicit Reasoning in Recurrent - Depth ...</a></li>
<li><a href="https://www.emergentmind.com/papers/2604.11791">Mechanistic Dynamics of Looped Transformers</a></li>
<li><a href="https://arxiv.org/abs/2310.07923">The Expressive Power of Transformers with Chain of Thought</a></li>
<li><a href="https://huggingface.co/papers?q=computational+power">Daily Papers - Hugging Face</a></li>

</ul>
</details>

**Tags**: `#llm-architecture`, `#transformer-research`, `#model-releases`, `#ai-analysis`, `#reasoning-systems`

---

<a id="item-tech-news-7"></a>
### [Six Chinese AI firms accused of aggressively copying US frontier models](https://arstechnica.com/tech-policy/2026/09/six-chinese-ai-firms-accused-of-aggressively-copying-us-frontier-models/) ⭐️ 7.0/10

US intelligence and cyber agencies jointly accuse six Chinese AI companies—DeepSeek, Moonshot AI, Alibaba, MiniMax, StepFun, and Z.AI—of conducting industrial-scale distillation attacks on US frontier models since late 2024, likely with Chinese government awareness.

rss · Ars Technica · Sep 9, 20:06

**Tags**: `#AI policy`, `#model distillation`, `#geopolitics`, `#US-China tech competition`, `#AI security`

---

<a id="item-tech-news-8"></a>
### [Apple unveils $1,999 iPhone Duo as its first foldable iPhone](https://arstechnica.com/gadgets/2026/09/apples-long-rumored-foldable-becomes-reality-with-the-2000-iphone-duo/) ⭐️ 7.0/10

Apple has entered the foldable phone market with the iPhone Duo, priced starting at $1,999 and positioned in the same range as competing foldables from Google and Samsung. The device adopts a wider, shorter &quot;passport-like&quot; form factor rather than a square aspect ratio, a choice Apple framed during its reveal as a rejection of designs that stretch single apps and leave large black bars around video content. When open, the Duo uses a 7.6-inch Super Retina XDR foldable panel with a 1:1.4 aspect ratio, slightly wider than a classic 4:3 monitor, and pairs it with a 5.4-inch outer screen featuring asymmetric corners \(pointy on the hinge side, rounded on the opposite edge\) intended to nudge users toward opening the phone. The display stack includes multiple layers of flexible glass over a titanium base and a custom stiffer polymer top layer with a nano-texture finish for improved bright-light readability. Apple claims the multi-layer lamination process eliminates a visible crease down the middle of the screen and prevents one from developing over time, a durability claim that goes beyond what Samsung&\#x27;s Galaxy Z Fold 8 and other recent foldables have demonstrated.

rss · Ars Technica · Sep 9, 19:42

**「Background」** Foldable smartphones have been on the market since Samsung launched the original Galaxy Fold in 2019, with book-style devices typically opening from a phone-sized exterior into a roughly square tablet-sized interior display. Competing book-style foldables from Samsung \(most recently the Galaxy Z Fold 8\), Google, and others have largely used that square inner aspect ratio, which critics note works well for split-screen multitasking but stretches standard apps and leaves large black bars when watching video. Apple had been rumored to be developing a foldable iPhone for several years—sometimes referred to in leaks as the &quot;iPhone Ultra&quot;—making its official entry a notable late arrival into an established category.

**「Impact」** iOS developers now face adapting their apps to the iPhone Duo&\#x27;s new 1:1.4 aspect ratio and dual 5.4-inch outer / 7.6-inch inner displays, adding another foldable form factor Apple does not support. Samsung&\#x27;s dismissive &quot;Sim sequel&quot; and &quot;So far, so same&quot; reaction suggests Apple&\#x27;s long-awaited debut validates rather than disrupts existing foldable design conventions, with the $1,999 starting price matching the Galaxy Z Fold 8&\#x27;s competitive range.

<details><summary>References</summary>
<ul>
<li><a href="https://www.macrumors.com/2026/09/09/iphone-duo-start-at-2000/">Foldable iPhone Duo Will Start at $2,000, Won&#x27;t Launch... - MacRumors</a></li>
<li><a href="https://9to5google.com/2026/09/09/samsung-apple-iphone-duo-reaction/">Samsung reacts to Apple &#x27;s foldable iPhone Duo</a></li>
<li><a href="https://www.engadget.com/2254316/iphone-duo-vs-samsung-galaxy-z-fold-8-comparison/">iPhone Duo Vs Samsung Galaxy Z Fold 8: Here&#x27;s How They Stack Up</a></li>
<li><a href="https://www.wired.com/story/apple-debuts-the-iphone-duo-its-first-folding-iphone/">Apple Debuts the iPhone Duo , Its First Folding iPhone | WIRED</a></li>

</ul>
</details>

**Tags**: `#hardware`, `#mobile`, `#apple`, `#foldable-phones`, `#consumer-electronics`

---

<a id="item-tech-news-9"></a>
### [Google&\#x27;s AlphaGenome Atlas evaluates every possible single-base change in the human genome](https://arstechnica.com/science/2026/09/googles-ai-genome-system-evaluates-every-possible-one-base-change/) ⭐️ 7.0/10

Google announced AlphaGenome Atlas, a resource that uses its AlphaGenome deep learning software to predict the functional consequences of every possible single-base change across the human genome, totaling roughly 9 billion variants \(3 billion reference bases × 3 alternative bases\). AlphaGenome is specifically designed to interpret non-coding DNA—the more than 97% of the genome that does not encode proteins—including regulatory sequences that control where and when genes are expressed, centromeres, chromosome-protecting caps, and splicing signals. Applying a single unified model across all variants gives researchers a uniform way to flag potentially functional non-coding mutations. The article cautions, however, that until biologists adopt the resource heavily, it remains unclear how much value AlphaGenome provides beyond what is already implicit in its training data. AlphaGenome itself is not new, but this release marks its first genome-wide, systematic application at single-base resolution.

rss · Ars Technica · Sep 9, 16:34

**「Background」** Although humans have roughly 3 billion DNA bases, less than 3% of the genome encodes proteins; the remaining majority is non-coding DNA that includes regulatory elements controlling where, when, and how genes are expressed, as well as structural features like centromeres and repetitive sequences derived from ancient viruses. AlphaGenome, a unified deep learning DNA sequence model developed by Google DeepMind, is designed to predict the functional effects of genetic variants—particularly single-base changes—on this non-coding portion of the genome, including regulatory activity, splicing, and gene expression. Applying the model genome-wide, as AlphaGenome Atlas does, therefore means scoring approximately 9 billion possible single-base substitutions against diverse functional readouts.

**「Impact」** Researchers and clinical genomics users gain a precomputed, genome-wide resource of AlphaGenome model scores for all 9 billion possible single-nucleotide variants, letting them look up predicted regulatory effects on non-coding DNA without running the model themselves. An accompanying preprint reports the atlas reliably distinguished disease-causing from benign changes in a clinical genomics database, though the source item notes that its practical advantage over reanalyzing AlphaGenome&\#x27;s own training data still depends on how heavily biologists adopt it.

<details><summary>References</summary>
<ul>
<li><a href="https://deepmind.google/blog/alphagenome-ai-for-better-understanding-the-genome/">AlphaGenome : AI for better understanding the... — Google DeepMind</a></li>
<li><a href="https://storage.googleapis.com/deepmind-media/papers/alphagenome.pdf">AlphaGenome : advancing regulatory variant</a></li>
<li><a href="https://rewire.it/blog/alphagenome-gene-regulation-2d-embeddings-splicing-noncoding-dna/">AlphaGenome : Gene Regulation &amp; Non - Coding DNA | rewire.it</a></li>
<li><a href="https://www.nature.com/articles/d41586-026-02835-4">DeepMind’s new genome ‘atlas’ charts effects of all nine billion human gene mutations | Nature</a></li>
<li><a href="https://deepmind.google/blog/alphagenome-atlas-a-predictive-map-of-every-possible-dna-letter-change-in-the-human-genome/">AlphaGenome Atlas: Molecular predictions for 9 Billion human DNA variants — Google DeepMind</a></li>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/google-deepmind/alphagenome-atlas/">AlphaGenome Atlas: a high-resolution map of human DNA</a></li>

</ul>
</details>

**Tags**: `#genomics`, `#AI/ML`, `#bioinformatics`, `#deep learning`, `#Google`

---

<a id="item-tech-news-10"></a>
### [Automattic CEO Matt Mullenweg placed on paid leave](https://www.theverge.com/tech/993022/wordpress-automattic-ceo-matt-mullenweg-leave-of-absence) ⭐️ 7.0/10

Matt Mullenweg, CEO of Automattic, the company behind WordPress.com, has been placed on a paid leave of absence, according to reporting by 404 Media and The Verge. In an internal Slack message, Mullenweg claimed the decision was made against his will and accused Automattic chief financial officer Mark Davies of &\#x27;conspiring&\#x27; with board members to put him on leave. The reported leadership turmoil follows ongoing controversies surrounding Automattic, including its high-profile dispute with WP Engine. The development raises uncertainty about the leadership of a company that stewards a significant portion of the open web through WordPress.

rss · The Verge · Sep 9, 22:15

**「Background」** Automattic is the commercial parent company of WordPress.com and a major contributor to the open source WordPress project, which Matt Mullenweg co-founded. Mullenweg has served as Automattic&\#x27;s CEO and is also a key steward of the broader WordPress ecosystem, which powers a substantial share of the web. The leadership change follows a prolonged and public dispute between Mullenweg and the hosting company WP Engine, in which Automattic&\#x27;s actions and rhetoric drew criticism from parts of the open source community.

**「Impact」** Automattic and the broader WordPress ecosystem face immediate leadership uncertainty, as a contested paid leave places co-founder and CEO Matt Mullenweg—a central figure in steering the open-source WordPress project—on the sidelines at a company already strained by the WP Engine dispute, prior layoffs, and a class-action lawsuit alleging abuse of control over the WordPress ecosystem.

<details><summary>References</summary>
<ul>
<li><a href="https://byteiota.com/matt-mullenweg-ousted-automattic-wordpress/">Matt Mullenweg Ousted From Automattic: What Devs Must Know</a></li>
<li><a href="https://wpvswpe.report/">WordPress vs WP Engine Conflict Timeline: Complete History</a></li>
<li><a href="https://en.wikipedia.org/wiki/Matt_Mullenweg">Matt Mullenweg - Wikipedia</a></li>
<li><a href="https://techcrunch.com/2026/09/09/automattics-board-forces-ceo-matt-mullenweg-into-leave-of-absence/">Automattic&#x27;s board forces CEO Matt Mullenweg into leave of absence | TechCrunch</a></li>
<li><a href="https://techcrunch.com/2025/01/12/wordpress-vs-wp-engine-drama-explained/">The WordPress vs. WP Engine drama, explained | TechCrunch</a></li>

</ul>
</details>

**Tags**: `#WordPress`, `#Automattic`, `#open source`, `#leadership`, `#tech industry`

---

<a id="item-tech-news-11"></a>
### [Apple unveils Watch Series 12 and Watch Ultra 4 with an AI upgrade that can recap your day](https://techcrunch.com/2026/09/09/apple-unveils-watch-series-12-and-watch-ultra-4-with-an-ai-upgrade-that-can-recap-your-day/) ⭐️ 7.0/10

Apple launches Watch Series 12 and Watch Ultra 4 with new &\#x27;Audio Intelligence&\#x27; AI features that recap conversations and rewind audio from daily interactions.

rss · TechCrunch · Sep 9, 18:08

**Tags**: `#Apple`, `#AI`, `#Wearables`, `#Smartwatch`, `#Consumer Electronics`

---

<a id="item-tech-news-12"></a>
### [SemiAnalysis Examines On-Device vs Datacenter Inference for Robotics](https://newsletter.semianalysis.com/p/where-does-a-robot-think-on-device) ⭐️ 6.0/10

SemiAnalysis has published a piece titled &\#x27;Where Does a Robot Think – On-Device vs Datacenter Inference&\#x27; examining the tradeoffs between running AI inference locally on a robot versus in a datacenter. According to the analysis summary accompanying this item, the article addresses how physical AI and robotics are reshaping the compute landscape, weighing edge hardware constraints against datacenter-scale capabilities. The opening line of the piece, &\#x27;For most of its short history, AI lived behind a screen,&\#x27; frames the central premise: robotics forces a reconsideration of where inference must occur to meet latency, power, and reliability demands. Beyond this opening sentence, the full technical arguments, quantitative comparisons, and named hardware or model references in the article are not available in the supplied excerpt, so specific claims cannot be verified here. Readers seeking concrete data on latency, model size, power budgets, or specific platforms will need to consult the original SemiAnalysis post.

rss · Semianalysis · Sep 9, 20:53

**「Background」** On-device AI inference means running a trained model directly on a robot&\#x27;s own hardware \(such as an onboard accelerator chip\), while datacenter inference means transmitting the robot&\#x27;s sensor data to remote servers that execute the model and return results. For physical AI, the tradeoff hinges on latency, bandwidth, and cost: real-time motion control often demands millisecond-scale responses that a network round-trip cannot reliably provide, yet datacenter GPUs can host larger or more frequently updated models than a single robot could carry, and amortizing a shared GPU across many robots can eventually beat the cost of putting a full inference chip in every machine. The article frames these tradeoffs against the broader compute landscape for robotics, where different companies are making diverging bets on whether intelligence should live on the robot or in the cloud.

<details><summary>References</summary>
<ul>
<li><a href="https://newsletter.semianalysis.com/p/where-does-a-robot-think-on-device">Where Does a Robot Think – On-Device vs Datacenter Inference – On-Device vs Datacenter Inference</a></li>
<li><a href="https://sechub.in/view/3288308">Where Does a Robot Think – On - Device vs Datacenter Inference</a></li>

</ul>
</details>

**Tags**: `#AI inference`, `#edge computing`, `#robotics`, `#AI hardware`, `#semiconductors`

---

<a id="item-tech-news-13"></a>
### [IBM releases Granite Time Series PatchTST-FM-r2 under permissive license](https://huggingface.co/blog/ibm-research/ibm-releases-sota-granite-time-series) ⭐️ 6.0/10

IBM has released Granite Time Series PatchTST-FM-r2, a ~385M-parameter zero-shot time series foundation model that adds probabilistic forecasting and missing-value imputation to the PatchTST family. The architecture replaces standard transformer blocks with conformer layers that combine multi-head self-attention and temporal convolution using alternating kernel sizes \{5, 5, 3, 3\}, applies 50% overlapping patches with Hamming-window weighting and overlap-and-add forecasting, and expands from 20 to 30 blocks to support contexts up to 8,192 steps and a 99-quantile prediction head. As of September 8, 2026, the model ranks \#1 on the GIFT-Eval benchmark among zero-shot replicable models with permissive commercial-friendly licensing, with a geometric-mean CRPS of 0.467 and MASE of 0.6846, and remains competitive when pretrained models are included \(3rd in CRPS, 4th in MASE\), outperforming larger models such as Chronos-2, Timer-S1, and Toto variants. The model is dual-licensed under Apache 2.0 and OpenMDW 1.0, with model weights, architecture, inference pipeline, and benchmark reproduction code openly released on Hugging Face and GitHub. Its documented pretraining corpus combines selected GiftEvalPretrain datasets, KernelSynth-based synthetic data, a TSMixup corpus restricted to non-evaluation datasets, and approximately 500,000 synthetic CauKer sequences of length 4,096.

rss · Hugging Face Blog · Sep 9, 15:36

**「Background」** Time series foundation models \(TSFMs\) are pretrained models designed to generate forecasts zero-shot across diverse time series datasets, removing the need to train a separate model for each forecasting problem. GIFT-Eval \(General Time Series Forecasting Model Evaluation\), introduced by Salesforce Research in October 2024, is a widely used benchmark that evaluates TSFMs across heterogeneous datasets and forecasting scenarios, distinguishing between strict zero-shot models and &quot;pretrained&quot; models allowed to use GIFT-Eval training portions. PatchTST-FM-r2 builds on IBM&\#x27;s PatchTST-FM-r1, released in March 2026 as part of a broader Granite TSFM family drop, and adopts conformer blocks—originally from speech processing—that pair multi-head self-attention with temporal convolution to capture both long-range and local temporal structure.

**「Impact」** Practitioners and enterprise teams gain a top-performing, permissively licensed open-source option for zero-shot time-series forecasting and imputation, removing licensing barriers that previously pushed them toward non-replicable or closed-weight alternatives on the GIFT-Eval leaderboard.

<details><summary>References</summary>
<ul>
<li><a href="https://www.salesforce.com/blog/gift-eval-time-series-benchmark/">Time Series Forecasting Benchmark : Introducing GIFT - Eval</a></li>
<li><a href="https://tsfm.ai/blog/gift-eval-deep-dive">GIFT - Eval : Salesforce &#x27;s Comprehensive TSFM Benchmark — TSFM.ai</a></li>
<li><a href="https://tsfm.ai/blog/ibm-march-2026-time-series-refresh">IBM&#x27;s March 2026 Time-Series Refresh: Four Models, Three Forecasters, and a Surprise — TSFM.ai</a></li>

</ul>
</details>

**Tags**: `#time-series`, `#foundation-models`, `#open-source`, `#IBM`, `#forecasting`

---

<a id="item-tech-news-14"></a>
### [Analog Devices Bolsters Its &quot;Physical Intelligence&quot; Plans, Splashes $1.35B on Alif Semiconductor - hackster.io](https://news.google.com/rss/articles/CBMizwFBVV95cUxOQlNhYkpGVXJpSUMwUlQ1QzBfeUZ4MDBnQmVjUGZHcWhVNVQ1eGRYdGtfcTlfTENhNHlsUFkxeGJxYnlPMV95cjRSVlRVY2xDVk9OaG9aVHFCSHNjUFlaWHhUaHNhXzBwSlFRaTk3aGlzLVg5LUdkbjBZYjZ1ZFUwT1E2Zm9IRXVJbDZzTFBVYTZvaFVvUFJza043dkZ3VkFiUU40VlprYmNsQzh4aVd6dUZySWM0WmxrYzlJN1oxSno5UDZJTDNOcmJkMl9yc2s?oc=5) ⭐️ 6.0/10

Analog Devices announces a $1.35 billion acquisition of Alif Semiconductor to strengthen its edge AI and &\#x27;physical intelligence&\#x27; strategy.

google\_news · hackster.io · Sep 9, 14:59

**Tags**: `#semiconductors`, `#edge-ai`, `#m&amp;a`, `#embedded-systems`, `#hardware`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Ant International, Visa and Mastercard team up on standards for AI-agent payments](https://www.cnbc.com/2026/09/10/ant-international-visa-mastercard-ai-agent-payment-standard.html) ⭐️ 7.0/10

Ant International, Visa, and Mastercard announced a partnership to develop common &quot;Know Your Agent&quot; standards — a framework for verifying the identity and trustworthiness of AI software that makes purchases on a user&\#x27;s behalf. The companies cited a McKinsey projection that AI agents will handle $3 trillion to $5 trillion of global consumer commerce by 2030.

rss · CNBC Finance · Sep 10, 01:53

**「background」** Each of the three companies had launched its own AI-agent payment protocol over the prior 12 months, and the new effort aims to make those systems interoperable so an agent registered with one network works across the others. Ant International, which separated from Ant Group roughly three years ago, operates the Alipay+ network linking more than 50 digital wallets worldwide, while Visa and Mastercard dominate card payments in developed economies.

**「impact」** Merchants and payment processors would gain a shared way to identify and monitor AI-driven transactions, which the partners say is necessary for agent-based commerce to scale across both card networks and digital wallets.

**Tags**: `#AI payments`, `#payments industry`, `#fintech partnerships`, `#digital wallets`, `#e-commerce`

---

<a id="item-finance-news-2"></a>
### [Adani Enterprises rises ~5% as airport unit raises $1 billion at $18 billion valuation](https://www.cnbc.com/2026/09/09/adani-enterprises-airport-fundraise-shares.html) ⭐️ 7.0/10

Shares of Adani Enterprises rose nearly 5% on Wednesday after its airport subsidiary, Adani Airport Holdings, agreed to raise about $1 billion \(₹98.25 billion\) from Alpha Wave Global, Premji Invest, Temasek, and funds managed by BlackRock, at an ~$18 billion pre-money valuation.

rss · CNBC Finance · Sep 9, 06:26

**「Background」** Adani Airport Holdings operates eight airports across India and handles more than 23% of the country&\#x27;s passenger traffic, according to the company; the deal follows Adani Enterprises&\#x27; ₹150 billion qualified institutional placement \(a share sale to institutional investors\) in July.

**「Impact」** The new investors will collectively own about 5.54% of Adani Airport Holdings after the final tranche, expected by July 2027, and the funds will be used to expand annual passenger capacity to about 200 million and develop airport-city real estate plus non-aviation businesses like ground handling and retail.

**Tags**: `#fundraising`, `#infrastructure`, `#aviation`, `#India`, `#private-equity`

---

<a id="item-finance-news-3"></a>
### [Chinese EV makers pivot to humanoid robots amid profit squeeze](https://www.cnbc.com/2026/09/09/chinas-ev-makers-shift-gears-to-focus-on-humanoids-as-car-market-slows.html) ⭐️ 7.0/10

Several major Chinese electric-vehicle makers, including Xpeng, BYD, Nio, Xiaomi, Li Auto and Geely, are expanding into humanoid robotics as China&\#x27;s EV market heads for its weakest sales year since 2021 and industry-wide profit margins fell to 1.5% in the first half of 2026, according to the China Association of Automobile Manufacturers.

rss · CNBC Finance · Sep 9, 04:12

**「Background」** These companies fueled China&\#x27;s EV boom over the past decade, but slowing demand and razor-thin profits have pushed them to seek new growth drivers and reframe themselves as technology companies, analysts at Counterpoint Research and Fitch Ratings said.

**「Impact」** Investors remain skeptical: Xpeng shares are down more than 45% year-to-date despite the company&\#x27;s $900 million robotics raise last month at a $6.3 billion unit valuation, and Jefferies analysts say they have yet to see firm external orders or clear revenue guidance from the automakers entering the sector.

**Tags**: `#Chinese EV market`, `#Humanoid Robotics`, `#Corporate Strategy`, `#Market Trends`, `#Electric Vehicles`

---