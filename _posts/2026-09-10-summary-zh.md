---
layout: default
title: "Horizon Summary: 2026-09-10 (ZH)"
date: 2026-09-10
lang: zh
---

> 从 136 条内容中筛选出 17 条重要资讯。

---

**科技新闻**
1. [vLLM v0.29.0 发布：Model Runner V2 成为默认架构](#item-tech-news-1) ⭐️ 8.0/10
2. [4 groups caught using the same Chrome and Windows exploit kit](#item-tech-news-2) ⭐️ 8.0/10
3. [OpenAI 声称攻克千禧年数学难题引发学术界震动](#item-tech-news-3) ⭐️ 8.0/10
4. [微信零点击蠕虫漏洞已被腾讯修复](#item-tech-news-4) ⭐️ 8.0/10
5. [Shopify 收购 Tailwind CSS，开源 CSS 框架迎来新东家](#item-tech-news-5) ⭐️ 7.0/10
6. [Sebastian Raschka 解读 GPT-6 &quot;Astra&quot; 与循环 Transformer 架构](#item-tech-news-6) ⭐️ 7.0/10
7. [Six Chinese AI firms accused of aggressively copying US frontier models](#item-tech-news-7) ⭐️ 7.0/10
8. [苹果发布首款折叠屏 iPhone Duo，售价 1999 美元起](#item-tech-news-8) ⭐️ 7.0/10
9. [谷歌推出 AlphaGenome Atlas，预测全基因组单碱基变异功能](#item-tech-news-9) ⭐️ 7.0/10
10. [WordPress 母公司 Automattic CEO 穆伦维格被迫休假](#item-tech-news-10) ⭐️ 7.0/10
11. [Apple unveils Watch Series 12 and Watch Ultra 4 with an AI upgrade that can recap your day](#item-tech-news-11) ⭐️ 7.0/10
12. [机器人思考在哪里进行——设备端推理与数据中心推理的权衡](#item-tech-news-12) ⭐️ 6.0/10
13. [IBM 发布 Granite 时间序列 PatchTST-FM-r2 基础模型](#item-tech-news-13) ⭐️ 6.0/10
14. [Analog Devices Bolsters Its &quot;Physical Intelligence&quot; Plans, Splashes $1.35B on Alif Semiconductor - hackster.io](#item-tech-news-14) ⭐️ 6.0/10

**财经新闻**
1. [蚂蚁国际携手 Visa、Mastercard 共建 AI 代理支付标准](#item-finance-news-1) ⭐️ 7.0/10
2. [Adani 机场业务子公司达成 10 亿美元融资协议，Adani Enterprises 股价上涨约 5%](#item-finance-news-2) ⭐️ 7.0/10
3. [中国电动车企转向人形机器人应对市场放缓](#item-finance-news-3) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [vLLM v0.29.0 发布：Model Runner V2 成为默认架构](https://github.com/vllm-project/vllm/releases/tag/v0.29.0) ⭐️ 8.0/10

vLLM v0.29.0 正式发布，共包含 277 位贡献者提交的 594 次提交（其中 91 位为新贡献者），其中最核心的变更是在所有模型上将 Model Runner V2（MRV2）设为默认架构，完成了此前从 pooling 模型开始的多版本分阶段推广。MRV2 在本版本获得 CUDA graph 内存分析用于 KV cache 自动调整（\#53306）、批分片采样使每步 logits 内存减少 1/TP（\#50465）、prompt embeds（\#42963）、\`extract\_hidden\_states\` 推测支持（\#49811）、spec decode 下统一的 FULL cudagraph 派发（\#53407）以及 EAGLE/MTP draft prefill 之前的 DP-sync 跳过（\#53694）等能力，仅有少数 ROCm 模型仍使用 MRV1。模型支持方面新增了采用 Gated DeepSeek Sparse Attention 与原生 MTP 的 Tencent Hy4-preview（770B/49B-active MoE，\#54160）、支持 BF16/FP8/NVFP4 与 MTP 的 Qwen3.8-Flash-Next（\#53896）、GraniteSWA 与 GraniteMoeSWA（\#52706）、带 MTP 的 NemotronH\_Omni\_Reasoning\_V3（\#52929、\#53121）以及 Kimi K3 NVFP4 检查点（\#53132）。Kimi K3 与 DeepSeek V4 的性能优化尤为显著：K3 潜在尾部的融合 MXFP4 top-k 终化使端到端延迟降低约 5%（\#53152），Mamba 元数据准备通过一次 Triton 启动实现 6.6–7.6 倍内核加速（\#52388），调优过的 Hopper 低延迟 GEMM 现也在 SM100 上派发（\#53534）并用于 \`eh\_proj\`（12.9–25.2% 加速，\#53942），MLA 门控被合并进 QKV-A 投影（\#54015）；DeepSeek V4 方面将共享专家融合进 MegaMoE（\#53040），并启用 opt-in 的 FlashInfer \`moe\_ep\` 专家后端（\#49636）。此外还有推测解码（per-request spec decode metrics、logprobs 自适应验证、SM100 稀疏 MLA）、新的 \`sharded\_rdt\` P2P RL 权重同步后端、Mamba 前缀缓存带来 9%–25% TTFT 改善（\#52789）、FlashInfer all-reduce 默认开启（\#52998）等改进，同时包含多项破坏性变更：移除 10 个已弃用模型架构（\#53608）、FlexOlmo、Olmo3 与 Hunyuan V1/VL 迁移至 Transformers 后端（\#53615）、PyAV 视频解码后端移除（\#54231）、\`python -m vllm.entrypoints.openai.api\_server\` 弃用改为 \`vllm serve\`（\#52131），并删除了 \`VLLM\_TEST\_FORCE\_FP8\_MARLIN\` 与 \`VLLM\_ROCM\_USE\_AITER\_FP4\_ASM\_GEMM\` 环境变量。

github · khluu · 9月9日 08:54

**「背景」** vLLM 是目前应用最广泛的开源大语言模型推理与服务框架之一，由 vllm-project 社区维护，支持多种 GPU 与加速器后端以及 Tensor Parallelism、Pipeline Parallelism、Speculative Decoding 等推理优化。Model Runner V2 是 vLLM 对其内部模型执行路径的重构版本，旨在统一不同模型族的执行流程并降低新增模型的接入成本。vLLM 采用较快的迭代节奏，每隔数周发布一个次要版本，并在版本号节点引入较大幅度的架构演进与破坏性变更。

**「影响」** 升级到 v0.29.0 的 vLLM 用户将自动获得 MRV2 的内存与吞吐改进以及 Kimi K3 / DeepSeek V4 上的端到端性能提升，但需要核查生产环境中是否仍有依赖 MRV1 的 ROCm 模型，并相应调整部署脚本与配置以兼容 \`vllm serve\` 新入口以及被移除的 PyAV 视频解码后端与若干已弃用模型架构。

**标签**: `#LLM Inference`, `#vLLM`, `#Open Source`, `#AI Infrastructure`, `#Model Serving`

---

<a id="item-tech-news-2"></a>
### [4 groups caught using the same Chrome and Windows exploit kit](https://arstechnica.com/information-technology/2026/09/4-groups-caught-using-the-same-chrome-and-windows-exploit-kit/) ⭐️ 8.0/10

Proofpoint researchers reveal BlueMoon, an exploit kit chaining two Chromium bugs and a Windows kernel flaw, used by at least four hacking groups including some with ties to China, with patches for all three vulnerabilities released within 24 hours.

rss · Ars Technica · 9月9日 20:55

**标签**: `#cybersecurity`, `#vulnerability-disclosure`, `#exploit-kit`, `#chrome`, `#windows`

---

<a id="item-tech-news-3"></a>
### [OpenAI 声称攻克千禧年数学难题引发学术界震动](https://www.theverge.com/ai-artificial-intelligence/992953/openai-math-millennium-prize-navier-stokes) ⭐️ 8.0/10

周二，OpenAI 宣布其 AI 智能体已解决了纳维-斯托克斯千禧年数学难题，这是七大千禧年难题之一。然而这一突破在正式公布前便陷入争议：纽约大学数学家 Tristan Buckmaster 与 Anthropic 员工 Levent Alpöge 此前利用 OpenAI 和 Anthropic 的公开模型合作近一年，刚刚证明了一个简化版的纳维-斯托克斯方程可以发生崩溃。OpenAI 技术员工 Sébastien Bubeck 在新闻发布会上承认，团队是听闻 Buckmaster 和 Alpöge 工作的传闻后才决定攻克这一难题，但 OpenAI 否认其模型访问或训练了这两位研究者的成果。其内部模型在数天内便得出完整证明，运行了约一万个并行智能体，成本高达数百万美元，不过 OpenAI 表示不会申领百万美元奖金。

rss · The Verge · 9月9日 21:16

**「背景信息」** 千禧年难题由克雷数学研究所于 2000 年选定，每个难题的解答可获一百万美元奖金，迄今只有另一道难题被解决。纳维-斯托克斯方程描述流体（如水和空气）随时间流动的方式，被广泛应用于流体力学领域，但数学家此前并不完全理解这些方程，特别是它们是否会在某些条件下崩溃并预测出不可能的状态，例如流体具有无限速度。

**「影响」** 如果 OpenAI 和 Anthropic 继续争夺更多数学荣誉，人类数学家可能在这些公司之外几乎无开放性问题可攻克，数学研究将日益集中在拥有海量内部资源的少数前沿 AI 公司手中。

**标签**: `#AI`, `#machine-learning`, `#mathematics`, `#research`, `#OpenAI`

---

<a id="item-tech-news-4"></a>
### [微信零点击蠕虫漏洞已被腾讯修复](https://www.theregister.com/security/2026/09/09/wechat-worm-could-pwn-a-friend-before-they-even-answered-the-call/5295234) ⭐️ 8.0/10

Calif Research 公布名为 WeWorm 的零点击蠕虫概念验证，可通过微信来电在 iOS 与 Android 平台间传播，受害者无需接听电话或与手机交互，漏洞即被触发并实现远程代码执行（RCE）。研究人员借助 AI 协助，从一个 VoIP 内存缺陷到完成首个 RCE 利用仅用约两天，再花一周构建出蠕虫形态；腾讯随后修复了该漏洞。事件凸显 AI 辅助漏洞挖掘已显著降低跨平台蠕虫的开发门槛，对月活超过十亿的微信用户构成潜在安全风险。

rss · The Register · 9月9日 12:45

**「背景」** 零点击蠕虫（zero-click worm）指的是无需受害者任何操作即可远程入侵并自我传播的恶意代码，因无需用户交互而具有极高的隐蔽性和危害性。微信（WeChat）是腾讯旗下的超级应用，全球月活跃用户超过十亿，集即时通讯、VoIP 语音/视频通话、移动支付等功能于一身，其庞大的用户基数使得针对它的漏洞影响面极大。内存破坏类漏洞（如缓冲区溢出、释放后使用等）是处理不可信网络输入（如 VoIP 信令与媒体流）时的经典缺陷，常被攻击者武器化用于远程代码执行，而近年来 AI 辅助的漏洞挖掘与利用开发正在显著缩短这类攻击从发现到武器化的时间。

**「潜在影响」** 在腾讯处置该漏洞前，WeChat 用户即使不接听来电，也可能因 WeWorm 通过 iOS 和 Android 的 VoIP 零点击远程代码执行而被入侵。腾讯已关闭该漏洞，用户仍应以官方安全更新和公告确认防护状态。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://calif.io/research/weworm">The first zero - click worm to spread through WeChat calls across iOS...</a></li>
<li><a href="https://www.1950.ai/post/wechat-zero-click-worm-how-ai-turned-a-voip-vulnerability-into-a-self-spreading-account-hijacking-t">WeChat Zero - Click Worm : How AI Turned a VoIP Vulnerability Into...</a></li>
<li><a href="https://cyberinsider.com/zero-click-worm-spreads-on-iphones-and-android-via-wechat-calls/">Zero - click worm spreads on iPhones and Android via WeChat calls</a></li>
<li><a href="https://www.esecurityplanet.com/artificial-intelligence/news-ai-wechat-worm-billion-accounts-apac-china/">AI-Assisted WeChat Worm Risks 1 Billion Accounts</a></li>

</ul>
</details>

**标签**: `#security`, `#zero-click-rce`, `#wechat`, `#ai-assisted-exploitation`, `#vulnerability-research`

---

<a id="item-tech-news-5"></a>
### [Shopify 收购 Tailwind CSS，开源 CSS 框架迎来新东家](https://tailwindcss.com/blog/tailwind-is-joining-shopify) ⭐️ 7.0/10

Shopify 宣布收购开源 CSS 框架 Tailwind 背后的公司 Tailwind Labs，这一被广泛使用的实用工具类（utility-first）CSS 框架正式并入电商平台生态。此次收购发生在 Tailwind Labs 商业模式遭受严重冲击的背景下：据公司 2025 年 1 月披露的信息，团队裁员比例高达 75%，文档流量自 2023 年初以来下降约 40%，核心原因是 AI 辅助编程降低了开发者对文档和商业模板的依赖。Tailwind 以通过预定义类名（如 p-4、flex 等）在 HTML 中直接组合样式而著称，重塑了现代前端 CSS 的编写方式；收购后 Tailwind 将作为 Shopify 旗下独立产品继续运营，并以 MIT 许可证保持开源。

hackernews · EdwinHoksberg · 9月9日 13:27 · [社区讨论](https://news.ycombinator.com/item?id=49626190)

**「背景」** Tailwind CSS 由 Adam Wathan 等人于 2017 年推出，倡导通过预定义工具类直接在 HTML 中编写样式，区别于 BEM 等传统 CSS 命名规范。其商业公司 Tailwind Labs 围绕框架构建了 UI 模板、组件库订阅和商业许可等收入来源。2025 年 1 月，Tailwind Labs 宣布大规模裁员并首次公开承认 AI 对公司业务造成剧烈冲击，为本次收购埋下伏笔。

**「影响」** 短期来看，现有 Tailwind 用户和开发者的使用流程不会受到影响，框架本身将继续以 MIT 许可证开源维护，Shopify 也承诺 Tailwind 保持独立运营；长期而言，Tailwind Labs 原有的商业产品（UI 模板、组件订阅等）未来或将逐步与 Shopify 电商生态整合。

**「社区讨论」** 社区讨论呈现出明显的两极化：不少开发者表达了对 Tailwind 团队及其工具的感谢与认可，也有用户质疑在 LLM 编码能力日益增强的当下，是否仍有必要依赖 Tailwind 这类工具类框架，而非直接使用现代原生 CSS 功能。讨论中的一个核心共识是：随着 AI 降低了开源工具被复现和替代的成本，单纯依靠&quot;开源核心+周边商业产品&quot;的 DevTools 商业模式正变得愈发难以维系，相关公司需要依托规模化托管、运维等 AI 难以替代的服务才能生存。

**标签**: `#acquisition`, `#open-source`, `#web-development`, `#ai-impact`, `#css-framework`

---

<a id="item-tech-news-6"></a>
### [Sebastian Raschka 解读 GPT-6 &quot;Astra&quot; 与循环 Transformer 架构](https://magazine.sebastianraschka.com/p/gpt-6-astra-looped-transformers-and) ⭐️ 7.0/10

机器学习研究者 Sebastian Raschka 在其博客《ModelForge》中对近期报道的 OpenAI GPT-6 &quot;Astra&quot; 泄露消息进行了技术分析，重点拆解了&quot;循环 Transformer&quot;（looped transformers / recurrent depth）与隐藏推理（hidden reasoning）这两个被外界渲染为突破性的概念。文章以 The Information 的报道为引子，指出该报道将 Astra 描述为掌握了某种使思维链监控更难实施的&quot;秘密技术&quot;，但 Raschka 通过对比相关研究指出，所谓循环 Transformer 在本质上等价于堆叠更多 Transformer 层并复用其权重以节省显存，并非架构层面的全新发明。与此同时，他讨论了将推理痕迹隐藏在模型内部而非外显输出的机制，及其与可解释性、可监控性之间的权衡。整体而言，该文章属于对泄露信息的学术综合与技术评论，并附带对循环 Transformer 通用性、训练稳定性等问题的开放讨论，而非 OpenAI 的官方公告或经核实的发布。

hackernews · ModelForge · 9月9日 14:37 · [社区讨论](https://news.ycombinator.com/item?id=49627370)

**「背景」** 循环 Transformer（也称循环深度架构）会在推理时重复使用同一组层或参数，以增加计算深度；这不同于不断堆叠具有独立权重的新层，但具体能力取决于重复结构、迭代次数和训练方式。所谓“隐藏推理”是模型在不生成完整思维链的情况下，通过内部迭代或潜在表示进行计算；它与输出中间推理文本的显式思维链并不相同。研究表明，思维链的中间生成确实能扩大 Transformer 可执行的计算范围，而且可表达的计算能力通常会随生成长度增加，但这并不能证明所有隐藏或循环计算都等同于有效推理。

**「影响」** 对关注大模型架构前沿的研究者与工程师而言，Raschka 的分析有助于澄清将&quot;循环 Transformer&quot;误读为全新范式的流行叙事，还原其作为权重共享层堆叠优化的本质；但关于 GPT-6 &quot;Astra&quot; 的真实能力与发布状态仍属推测，缺乏官方确认。

**「社区讨论」** 评论区中，shawntan 补充了 Will Merrill 关于&quot;何种计算问题最少需要多少思维链步数&quot;的论文作为背景，并指出循环 Transformer 与早期通用 Transformer 研究之间的渊源；libraryofbabel 明确表示循环 Transformer 就是权重复用的层堆叠，并非外界渲染的&quot;秘密技术&quot;，与 Raschka 的结论一致；wolttam 从机制层面解释了若将整个 Transformer 自身循环则必然形成隐藏推理痕迹；siva7 则表达了对泄露模型在周一表现惊艳但周二能力下降的担忧，反映出社区对未发布模型稳定性与可靠性的疑虑。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2604.07822">Loop , Think, &amp; Generalize: Implicit Reasoning in Recurrent - Depth ...</a></li>
<li><a href="https://arxiv.org/abs/2310.07923">The Expressive Power of Transformers with Chain of Thought</a></li>

</ul>
</details>

**标签**: `#llm-architecture`, `#transformer-research`, `#model-releases`, `#ai-analysis`, `#reasoning-systems`

---

<a id="item-tech-news-7"></a>
### [Six Chinese AI firms accused of aggressively copying US frontier models](https://arstechnica.com/tech-policy/2026/09/six-chinese-ai-firms-accused-of-aggressively-copying-us-frontier-models/) ⭐️ 7.0/10

US intelligence and cyber agencies jointly accuse six Chinese AI companies—DeepSeek, Moonshot AI, Alibaba, MiniMax, StepFun, and Z.AI—of conducting industrial-scale distillation attacks on US frontier models since late 2024, likely with Chinese government awareness.

rss · Ars Technica · 9月9日 20:06

**标签**: `#AI policy`, `#model distillation`, `#geopolitics`, `#US-China tech competition`, `#AI security`

---

<a id="item-tech-news-8"></a>
### [苹果发布首款折叠屏 iPhone Duo，售价 1999 美元起](https://arstechnica.com/gadgets/2026/09/apples-long-rumored-foldable-becomes-reality-with-the-2000-iphone-duo/) ⭐️ 7.0/10

苹果在硬件发布会上推出首款折叠屏 iPhone Duo，经过多年传闻后正式进入折叠手机市场。该机起售价为 1999 美元，采用更宽、更矮的护照式设计，展开和折叠时均为 1:1.4，配备 5.4 英寸外屏和 7.6 英寸 Super Retina XDR 折叠屏。苹果称其柔性玻璃、钛金属基底及定制聚合物表层可提升强光可读性，并减少或消除折痕，但实际耐用性仍需市场检验。

rss · Ars Technica · 9月9日 19:42

**标签**: `#hardware`, `#mobile`, `#apple`, `#foldable-phones`, `#consumer-electronics`

---

<a id="item-tech-news-9"></a>
### [谷歌推出 AlphaGenome Atlas，预测全基因组单碱基变异功能](https://arstechnica.com/science/2026/09/googles-ai-genome-system-evaluates-every-possible-one-base-change/) ⭐️ 7.0/10

谷歌于本周二发布了 AlphaGenome Atlas，这是一套利用 AlphaGenome 模型预测人类基因组中每一个可能单碱基变异（约 90 亿个）功能后果的资源。该模型专注于非编码调控 DNA——这部分 DNA 占人类基因组的绝大部分，负责控制基因的开关、剪接与表达等过程，但仍有许多序列功能不明。AlphaGenome Atlas 的优势在于用单一软件包完成全基因组规模的变异解读，为识别功能性非编码区域提供了统一工具。然而，由于源文章内容被截断，且该资源刚刚发布，目前尚不清楚在实际生物学研究中，AlphaGenome Atlas 相比其训练数据能带来多少额外价值，这一问题有待研究人员广泛使用后得到验证。

rss · Ars Technica · 9月9日 16:34

**「背景」** AlphaGenome 是 Google DeepMind 此前推出的一款用于理解基因组调控功能的统一 DNA 序列深度学习模型，能够同时预测剪接、基因表达等多项调控性功能注释。人类基因组中绝大多数 DNA 并不编码蛋白质，而是承担调控基因活动等关键功能，但如何系统评估非编码区域中单个碱基变化的功能后果一直是基因组学领域的难题。该模型此前已通过 API 形式向研究人员开放，AlphaGenome Atlas 则是其首次在全基因组规模上的系统性应用。

**「影响」** 基因组学研究人员与临床遗传学家可直接查询覆盖 9 亿个单碱基变体的非编码调控效应预测，将原本零散的变体解读工作集中到 AlphaGenome Atlas 这一个统一资源上。DeepMind 与学术合作者在临床基因组学数据库中的初步验证表明，该预测能够区分致病变异与无害变异，但其相对现有方法的实际增益仍取决于生物学界后续的广泛采用与独立评估。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepmind.google/blog/alphagenome-ai-for-better-understanding-the-genome/">AlphaGenome : AI for better understanding the... — Google DeepMind</a></li>
<li><a href="https://storage.googleapis.com/deepmind-media/papers/alphagenome.pdf">AlphaGenome : advancing regulatory variant</a></li>
<li><a href="https://www.nature.com/articles/d41586-026-02835-4">DeepMind’s new genome ‘atlas’ charts effects of all nine billion human gene mutations | Nature</a></li>
<li><a href="https://deepmind.google/blog/alphagenome-atlas-a-predictive-map-of-every-possible-dna-letter-change-in-the-human-genome/">AlphaGenome Atlas: Molecular predictions for 9 Billion human DNA variants — Google DeepMind</a></li>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/google-deepmind/alphagenome-atlas/">AlphaGenome Atlas: a high-resolution map of human DNA</a></li>

</ul>
</details>

**标签**: `#genomics`, `#AI/ML`, `#bioinformatics`, `#deep learning`, `#Google`

---

<a id="item-tech-news-10"></a>
### [WordPress 母公司 Automattic CEO 穆伦维格被迫休假](https://www.theverge.com/tech/993022/wordpress-automattic-ceo-matt-mullenweg-leave-of-absence) ⭐️ 7.0/10

WordPress.com 母公司 Automattic 的首席执行官马特·穆伦维格\(Matt Mullenweg\)已被安排带薪休假。据报道，公司首席财务官马克·戴维斯\(Mark Davies\)被指与董事会成员合谋推动了这一决定。穆伦维格在公司 Slack 消息中表示，休假安排违背了他的意愿。此事发生在 Automattic 与 WP Engine 纠纷持续发酵的背景下，为这家掌管 WordPress 生态系统的关键企业的领导层增添了不确定性。

rss · The Verge · 9月9日 22:15

**标签**: `#WordPress`, `#Automattic`, `#open source`, `#leadership`, `#tech industry`

---

<a id="item-tech-news-11"></a>
### [Apple unveils Watch Series 12 and Watch Ultra 4 with an AI upgrade that can recap your day](https://techcrunch.com/2026/09/09/apple-unveils-watch-series-12-and-watch-ultra-4-with-an-ai-upgrade-that-can-recap-your-day/) ⭐️ 7.0/10

Apple launches Watch Series 12 and Watch Ultra 4 with new &\#x27;Audio Intelligence&\#x27; AI features that recap conversations and rewind audio from daily interactions.

rss · TechCrunch · 9月9日 18:08

**标签**: `#Apple`, `#AI`, `#Wearables`, `#Smartwatch`, `#Consumer Electronics`

---

<a id="item-tech-news-12"></a>
### [机器人思考在哪里进行——设备端推理与数据中心推理的权衡](https://newsletter.semianalysis.com/p/where-does-a-robot-think-on-device) ⭐️ 6.0/10

SemiAnalysis 发布了一篇由 Ivan Chiam 撰写的分析文章，探讨机器人与物理 AI 场景下设备端推理与数据中心推理之间的取舍。文章指出，在其短暂的发展历程中，AI 大多运行于屏幕之后，而如今随着机器人的兴起，AI 算力的部署位置正面临新的抉择。该文聚焦于边缘计算、AI 硬件及半导体路线图等关键议题，对 AI 系统设计具有重要参考价值。

rss · Semianalysis · 9月9日 20:53

**标签**: `#AI inference`, `#edge computing`, `#robotics`, `#AI hardware`, `#semiconductors`

---

<a id="item-tech-news-13"></a>
### [IBM 发布 Granite 时间序列 PatchTST-FM-r2 基础模型](https://huggingface.co/blog/ibm-research/ibm-releases-sota-granite-time-series) ⭐️ 6.0/10

IBM 发布了 Granite Time Series PatchTST-FM-r2，作为 Granite 时间序列基础模型家族的新版本，拥有约 3.85 亿参数，支持零样本预测、概率预测与缺失值填补，并采用 Apache 2.0 与 OpenMDW 1.0 双重宽松商业许可证开源，权重、架构、推理流程与复现代码均已公开。架构上，该模型从 r1 的标准 Transformer 层改为基于 Conformer 的模块，在多头自注意力中融合时间卷积以同时捕获长短期时序依赖，并将网络深度从 20 层扩展至 30 层，交替使用卷积核尺寸为 3 和 5 以平衡局部与全局建模。模型支持最长 8192 步的上下文长度，并通过 99 分位预测头输出点预测与概率分布，同时引入 50%重叠 patch 与汉明窗加权以及重叠相加预测以平滑 patch 边界。截至 2026 年 9 月 8 日，在 GIFT-Eval 基准的可复现零样本模型中，PatchTST-FM-r2 在 CRPS（几何均值 0.467）与 MASE（几何均值 0.6846）两项指标上均排名第二，并在采用宽松商业许可证的模型中位列第一；当纳入允许使用基准训练数据的预训练模型后，它仍位列 CRPS 第三、MASE 第四。训练数据由 GIFT-Eval 预训练数据子集、基于 KernelSynth 的自定义合成数据、TSMixup 语料以及约 50 万条长度为 4096 的 CauKer 合成序列组成。

rss · Hugging Face Blog · 9月9日 15:36

**「背景知识」** 时间序列基础模型（TSFM）是通过大规模数据预训练后，能够在未见过的时序数据上直接进行零样本预测的通用模型，用户无需为每个新数据集重新训练。PatchTST 是该领域一种代表性的架构，它将时间序列切分成若干“块”（patch）后再输入 Transformer，从而高效地捕捉长期时序依赖关系。GIFT-Eval 由 Salesforce Research 于 2024 年提出，是一套覆盖多种数据集和预测场景的综合时序基准测试，用于评估模型在零样本以及允许使用预训练数据情况下的泛化能力，并同时采用 CRPS 与 MASE 等指标进行排名。

**「影响」** 对于需要在生产环境中部署零样本时间序列预测的企业和开发者而言，PatchTST-FM-r2 在 GIFT-Eval 基准上达到同类可比模型前列的同时，配合 Apache 2.0 与 OpenMDW 1.0 双重宽松许可证并公开训练语料组成，显著降低了商业集成与合规审查的门槛。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.salesforce.com/blog/gift-eval-time-series-benchmark/">Time Series Forecasting Benchmark : Introducing GIFT - Eval</a></li>
<li><a href="https://tsfm.ai/blog/gift-eval-deep-dive">GIFT - Eval : Salesforce &#x27;s Comprehensive TSFM Benchmark — TSFM.ai</a></li>
<li><a href="https://github.com/SalesforceAIResearch/gift-eval">GitHub - SalesforceAIResearch/ gift - eval · GitHub</a></li>

</ul>
</details>

**标签**: `#time-series`, `#foundation-models`, `#open-source`, `#IBM`, `#forecasting`

---

<a id="item-tech-news-14"></a>
### [Analog Devices Bolsters Its &quot;Physical Intelligence&quot; Plans, Splashes $1.35B on Alif Semiconductor - hackster.io](https://news.google.com/rss/articles/CBMizwFBVV95cUxOQlNhYkpGVXJpSUMwUlQ1QzBfeUZ4MDBnQmVjUGZHcWhVNVQ1eGRYdGtfcTlfTENhNHlsUFkxeGJxYnlPMV95cjRSVlRVY2xDVk9OaG9aVHFCSHNjUFlaWHhUaHNhXzBwSlFRaTk3aGlzLVg5LUdkbjBZYjZ1ZFUwT1E2Zm9IRXVJbDZzTFBVYTZvaFVvUFJza043dkZ3VkFiUU40VlprYmNsQzh4aVd6dUZySWM0WmxrYzlJN1oxSno5UDZJTDNOcmJkMl9yc2s?oc=5) ⭐️ 6.0/10

Analog Devices announces a $1.35 billion acquisition of Alif Semiconductor to strengthen its edge AI and &\#x27;physical intelligence&\#x27; strategy.

google\_news · hackster.io · 9月9日 14:59

**标签**: `#semiconductors`, `#edge-ai`, `#m&amp;a`, `#embedded-systems`, `#hardware`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [蚂蚁国际携手 Visa、Mastercard 共建 AI 代理支付标准](https://www.cnbc.com/2026/09/10/ant-international-visa-mastercard-ai-agent-payment-standard.html) ⭐️ 7.0/10

蚂蚁国际宣布与 Visa 和 Mastercard 达成合作，共同制定用于 AI 代理支付的&quot;了解你的代理&quot;\(Know Your Agent\)通用标准，旨在提升不同支付系统之间的互操作性。麦肯锡预计，到 2030 年 AI 代理将处理 3 至 5 万亿美元的全球消费商业交易，三方希望借此建立信任机制以应对 AI&quot;幻觉&quot;等风险。蚂蚁国际首席创新官杨江明强调&quot;信任是 AI 转型的基石&quot;，Mastercard 首席数字官 Pablo Fourez 也指出，跨框架互操作性对于智能体商业规模化至关重要。

rss · CNBC Finance · 9月10日 01:53

**标签**: `#AI payments`, `#payments industry`, `#fintech partnerships`, `#digital wallets`, `#e-commerce`

---

<a id="item-finance-news-2"></a>
### [Adani 机场业务子公司达成 10 亿美元融资协议，Adani Enterprises 股价上涨约 5%](https://www.cnbc.com/2026/09/09/adani-enterprises-airport-fundraise-shares.html) ⭐️ 7.0/10

Adani Enterprises 旗下机场业务子公司 Adani Airport Holdings 与淡马锡、贝莱德、Premji Invest 和 Alpha Wave Global 签署约 98.25 亿卢比（约 10 亿美元）的有约束力融资协议，按约 180 亿美元投前估值定价；消息发布后 Adani Enterprises 股价当日上涨近 5%。

rss · CNBC Finance · 9月9日 06:26

**「背景」** Adani Airport Holdings 是印度机场运营商，管理该国 8 座机场，客运量占比超过 23%，此前 Adani Enterprises 刚于今年 7 月完成 1500 亿卢比合格机构配售。

**「影响」** 所筹资金将用于扩建和现代化机场基础设施、推进 Adani 机场城项目以及非航空业务，公司表示目标是未来将年旅客吞吐能力提升至约 2 亿人次。

**标签**: `#fundraising`, `#infrastructure`, `#aviation`, `#India`, `#private-equity`

---

<a id="item-finance-news-3"></a>
### [中国电动车企转向人形机器人应对市场放缓](https://www.cnbc.com/2026/09/09/chinas-ev-makers-shift-gears-to-focus-on-humanoids-as-car-market-slows.html) ⭐️ 7.0/10

中国主要电动车企——包括小鹏、比亚迪、蔚来、小米、理想和吉利——正在转向人形机器人领域，以寻求新的增长动力；据花旗估算，小鹏上月为机器人业务融资 9 亿美元后，其机器人部门估值达 63 亿美元，与该公司电动车业务 65 亿美元的估值相当。

rss · CNBC Finance · 9月9日 04:12

**「背景」** 由于竞争加剧，中国电动汽车销量正走向 2021 年以来最差年份，2026 年上半年汽车制造业平均利润率降至 1.5%（中国汽车工业协会数据，经 Counterpoint Research 引述）；据 Counterpoint，截至 8 月，中国车企已占全球涉足人形机器人的近 20 家车企的过半。

**「影响」** 小鹏股价今年下跌逾 45%，是主要电动车企中表现最差的，融资消息公布后股价仍下跌；Jefferies 分析师指出，目前车企尚未获得明确的外部订单，人形机器人的外部需求仍是悬而未决的问题。

**标签**: `#Chinese EV market`, `#Humanoid Robotics`, `#Corporate Strategy`, `#Market Trends`, `#Electric Vehicles`

---