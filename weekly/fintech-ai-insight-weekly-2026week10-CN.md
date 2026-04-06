![FinTech AI Insight Weekly Banner](../images/fintech-ai-insight-weekly-2026week10-EN/banner-fintech-ai-insight-weekly.png)

# FinTech AI Insight Weekly · Week 10 · 2026

## 1) 摘要

- 本周模型更新集中在轻量化执行模型、实时多模态交互、长链任务和工具调用，包括 GPT-5.4 Mini / Nano、Gemini 3.1 Flash Live、GLM-5.1 和 Claude Mythos。
- 产品 / 项目部分包括面向 Agent 的支付与财务 CLI 工具、Silicon Friendly、TradingAgents 和 claw-code，内容覆盖终端接口、网站可操作性评估、多智能体交易框架和 agent harness 开源实现。
- 金融动态部分包括 JPMorgan 关于合成数据与 guardrails 的技术文章、Bank of America 的 AI-powered meeting journey、Capital One 的多智能体工作流案例，以及 PNC 的营运资金方案。
- 研究与观点部分包括长期运行应用程序的 harness 设计、人工智能学习科学品味，以及关于认知投降、agent orchestration、工程实践和产品管理的讨论。

## 2) 模型观察

### [OpenAI 发布 GPT-5.4 Mini 和 Nano 模型](https://openai.com/zh-Hans-CN/index/introducing-gpt-5-4-mini-and-nano/)

OpenAI 发布了 GPT-5.4 Mini 和 Nano 两个模型，把 GPT-5.4 的能力下放到更快、更便宜的小模型，用来作为“执行层”和子 Agent 的主力。

- GPT-5.4 Mini：定位即时响应的代码助手，以及由大模型规划、Mini 并行执行的子智能体；同时覆盖解析复杂 UI 截图的 computer use，以及代码、推理、多模态、工具使用方面的提升。
- GPT-5.4 Nano：定位速度和成本敏感的简单任务，包括分类、数据抽取、排序和简单辅助的子 Agent。
- 性能关系是：`GPT-5.4 > GPT-5.4 mini ≈ GPT-5.4 nano > GPT-5 mini`。
- 价格是：`GPT-5.4 mini` 为 `0.75 / 4.50 美元每百万 Token`，`GPT-5.4 nano` 为 `0.20 / 1.25 美元每百万 Token`。

![OpenAI GPT-5.4 Mini and Nano](../images/fintech-ai-insight-weekly-2026week10-EN/model-openai-gpt-5-4-mini-nano.webp)

### [谷歌上线 Gemini 3.1 Flash Live 预览版](https://blog.google/innovation-and-ai/technology/developers-tools/build-with-gemini-3-1-flash-live/)

谷歌上线了 Gemini 3.1 Flash Live 预览版，通过 Gemini Live API 支持超低延迟的实时语音 / 视觉对话 Agent。

- 支持实时语音和视觉输入。
- 可以在嘈杂环境下进行更稳、更自然的多语言对话。
- 可以直接接工具执行操作。

![Gemini 3.1 Flash Live](../images/fintech-ai-insight-weekly-2026week10-EN/model-gemini-3-1-flash-live.png)

### [智谱发布 GLM-5.1](https://x.com/Zai_org/status/2037490078126084514?s=20)

智谱发布了 GLM-5.1。公开测试结果显示，GLM-5.1 的 Coding 得分比 GLM-5 提升明显；同时，GLM-5 Turbo 在一些长链任务中的表现较好，例如助理类任务和频繁调用工具的场景。

![GLM-5.1](../images/fintech-ai-insight-weekly-2026week10-EN/model-glm-5-1.png)

### [Anthropic 正在测试 Claude Mythos](https://fortune.com/2026/03/26/anthropic-says-testing-mythos-powerful-new-ai-model-after-data-leak-reveals-its-existence/?preview_id=4450088%5C)

Fortune 报道称，Anthropic 正在测试一款名为 `Claude Mythos` 的新模型。相关材料将其描述为能力显著更强、价格更高，当前仅向少量早期客户开放，并对其潜在网络安全影响保持谨慎。

![Claude Mythos](../images/fintech-ai-insight-weekly-2026week10-EN/model-claude-mythos.png)

## 3) 热门产品 / 项目

### 面向 Agent 的支付与财务 CLI 工具


- [`Stripe Projects`](https://projects.dev/)：把原本零散、繁琐的基础设施配置统一到命令行中完成，让开发者或 AI Agent 通过几条 CLI 命令开通和管理托管、数据库、鉴权、AI、分析等服务。
- [`Ramp CLI`](https://agents.ramp.com/)：用于管理公司财务的 CLI 产品，覆盖卡片、账单、费用、差旅和审批等 50 多种工具。
- [`Visa CLI`](https://visacli.sh/)：让开发者或 AI 代理在终端环境中安全执行支付；获得测试资格后，可以在编程时直接调用 CLI，为图像生成、音乐生成等付费 API，以及各类专有数据源和付费数据服务按需付款。

![Agent Finance CLI](../images/fintech-ai-insight-weekly-2026week10-EN/product-agent-finance-cli.png)

### [Silicon Friendly：评估网站对 Agent 的友好程度](https://siliconfriendly.com/)

Silicon Friendly 提供了一套评估网站对 AI Agent 友好程度的体系，使用 30 个检查项和 5 个等级来衡量网站能力。

- `L1`：基础可读性，关注 Agent 是否能读懂内容。
- `L2`：可发现性，关注 Agent 是否能找到信息。
- `L3`：结构化交互，关注 Agent 是否能和网站“对话”。
- `L4`：Agent 集成，关注 Agent 是否能在网站上执行操作。
- `L5`：完全自治运行，关注 Agent 是否能在网站上“生存”并自动协作。

![Silicon Friendly](../images/fintech-ai-insight-weekly-2026week10-EN/product-silicon-friendly.webp)

### [TauricResearch/TradingAgents：多智能体金融交易框架](https://github.com/TauricResearch/TradingAgents)

`TradingAgents` 是一个模拟真实交易公司分工的多智能体交易框架，通过由大语言模型驱动的基本面、情绪、新闻、技术分析师，以及交易员和风控角色协同工作，对市场进行分析、讨论并形成交易决策。该项目在 GitHub Trending 月榜中排第 `13`，本月新增星标 `16,280`。

![TradingAgents Schema](../images/fintech-ai-insight-weekly-2026week10-EN/project-tradingagents-schema.png)

### [ultraworkers/claw-code：Rust 实现的 CLI Agent Harness](https://github.com/ultraworkers/claw-code)

`claw-code` 是一个围绕 Claude Code 能力形态进行净室重写的开源项目，当前同时包含 Python porting workspace 和 `rust/` 目录下的生产实现。项目覆盖 API client、runtime、tools、commands、plugins 和 CLI 等模块，并配套 `USAGE`、`PARITY`、`ROADMAP`、`PHILOSOPHY` 等文档，用于说明构建、认证、会话、测试和当前功能对齐进度。

![Claw Code Star History](../images/fintech-ai-insight-weekly-2026week10-EN/project-claw-code-star-history.png)

## 4) 金融动态

### [JPMorgan：用合成数据强化 LLM guardrails](https://www.jpmorganchase.com/about/technology/blog/fence-framework)

JPMorgan 发布技术文章，介绍如何通过合成数据生成方法提升大型语言模型 guardrails 的覆盖范围与测试能力，重点讨论其在模型治理与安全防护中的应用。

### [Bank of America：把 AI 嵌入高净值客户服务流程](https://newsroom.bankofamerica.com/content/newsroom/press-releases/2026/03/merrill-and-bank-of-america-private-bank-launch-ai-powered-meeti.html)

Bank of America 宣布为 Merrill 和 Private Bank 推出 AI-powered meeting journey，用于支持客户会议相关流程，覆盖会前准备、会议协作与会后跟进等环节。

### [Capital One：构建面向消费银行运营场景的多智能体工作流](https://www.nvidia.com/gtc/session-catalog/sessions/gtc26-ex82362/)

Capital One 在 NVIDIA GTC 会议上展示了一个面向消费银行运营场景的 proprietary multi-agentic AI workflows 案例，介绍多智能体在具体银行运营用例中的编排方式。

### [PNC：推出营运资金优化的 Agentic AI](https://www.pnc.com/en/corporate-and-institutional/campaigns/optimize-working-capital-agentic-ai.html)

PNC 发布了 Optimize Working Capital Agentic AI 方案，面向营运资金管理场景，聚焦企业客户在资金调度、营运效率和相关流程中的应用。

## 5) 热门研究

### [Anthropic：长期运行应用程序开发的 Harness Design](https://www.anthropic.com/engineering/harness-design-long-running-apps)

Anthropic 工程师展示了如何通过 harness 设计和多智能体结构，提升 Claude 在前端设计与长时间全栈编码任务中的表现。在前端设计任务中，团队引入“生成器 + 评估器”闭环，把设计质量拆成可评分维度，并由评估 agent 借助 Playwright 实际操作页面后给出反馈。在长时全栈编码任务中，团队进一步采用“规划者 - 生成者 - 评估者”架构，让规划、实现和验收形成多轮迭代。文章也展示了随着模型从 Opus 4.5 升级到 4.6，团队如何继续删减不再必要的脚手架，并保留仍然有效的 harness 结构。

![Harness Design](../images/fintech-ai-insight-weekly-2026week10-EN/research-anthropic-harness-design.png)

### [人工智能可以学会科学审美](https://arxiv.org/abs/2603.14473)

这项工作提出来自社区反馈的强化学习（RLCF）范式，把“科学品味”学习表述为偏好建模与对齐问题。研究者先在 70 万对按领域和时间匹配的高引用与低引用论文上训练 Scientific Judge，用于判断研究想法的潜在影响力；再以其作为奖励模型，训练 Scientific Thinker 生成更高潜在影响力的研究想法。论文报告称，Scientific Judge 在相关评判任务上优于多种先进模型，并能泛化到未来年份、未见领域和同行评审偏好。

![Scientific Taste](../images/fintech-ai-insight-weekly-2026week10-EN/research-scientific-taste.png)

### [人工智能必须通过超人适应性智能拥抱专业化](https://arxiv.org/abs/2602.23643)

这篇文章质疑以 AGI 作为人工智能未来核心目标的表达方式，认为“能够做人类能做的一切”并不是一个足够清晰、稳定的定义。作者主张，与其追求抽象的通用性，不如接受专业化，并在专业化过程中追求超越人类的表现。为此，文中提出“超人类可适应智能”（SAI）的概念，用来描述既能在重要任务上超越人类、又能填补人类能力空白的智能系统。

![SAI Specialization](../images/fintech-ai-insight-weekly-2026week10-EN/research-sai-specialization.png)

## 6) 重要观点

### [Andrej Karpathy：编程的终结与 Agent 的循环时代](https://www.youtube.com/watch?v=kwSVtQ7dziU)

Karpathy 在这期访谈中讨论了 agent orchestration、AutoResearch、开放协作和模型专业化。他将高效编码描述为如何同时编排一群长期在线、有记忆的代码 Agent 和自治系统，并把工程师的瓶颈表述为“能指挥多少 tokens 以多高吞吐率工作”。


### [Simon Willison：让编程智能体真正可用的工程实践](https://www.youtube.com/watch?v=owmJyKVu5f8)

这场演讲总结了 Simon Willison 对编码代理工程实践的看法，重点包括通过测试、沙箱、提示注入防护和质量验证来提升代理可用性，以及把人类角色更多转向测试设计、架构选择、重构和质量判断。


### [深度解析：Harness Engineering](https://mp.weixin.qq.com/s/-mgf8K7XZrTKoD0pMOIn3w)

这篇文章的核心判断是，模型不再是主要瓶颈，系统才是。作者把 AI 工程的演进概括为从 Prompt Engineering 到 Context Engineering，再到 Harness Engineering，并将后者定义为让模型能够作为 Agent 持续行动的外循环系统。文中重点拆解了 durable state、计划分解、guides 与 sensors、legibility、工具中介和人机边界等构件，认为未来 agent 的可靠性更取决于状态管理、反馈回路、验证机制和系统编排，而不只是模型单步能力。

![Harness Engineering](../images/fintech-ai-insight-weekly-2026week10-EN/viewpoint-harness-engineering.png)

### [林俊旸：从“推理型”思维到“Agent型”思维](https://eu.36kr.com/zh/p/3740825962135558)

这篇文章回顾了从 o1、R1 带动的“推理型思维”浪潮，到“智能体式思维”逐渐成为主线的转变。作者认为，推理不应只是生成更长的思考轨迹，而应与编码、工具调用、长任务执行和代理工作流结合，转向“为了行动而思考”。在这一变化下，强化学习基础设施也从相对封闭的推理 RL，转向环境更复杂、训练与推理解耦更明显的 agentic RL。文章进一步指出，未来竞争力将更多取决于环境设计、训练部署一体化、harness 与编排工程，以及能把模型决策与真实结果闭环起来的系统能力。



### [Anthropic：81,000 人对 AI 的期待](https://www.anthropic.com/features/81k-interviews)

这份 Anthropic 访谈在一周内面向 159 个国家、70 种语言、80,508 名用户开展。受访者对 AI 的期待集中在节省时间、减轻心智负担、职业提升和财务机会等方面，同时也表达了对幻觉、依赖、就业、治理和隐私等问题的担忧。


## 7) 本周观察

- 本周主线很明确：模型、产品和研究都在朝“让 Agent 真正进入工作流”收敛，重点已经从演示能力转向执行能力。
- FinTech 相关进展也更偏具体落地。JPMorgan 关注治理与护栏，Bank of America、Capital One 和 PNC 则分别把 AI 放进客户流程、银行运营和企业资金管理场景。
- 研究和观点部分反复指向同一个结论：决定 agent 上限的，不只是模型本身，更是 harness、权限、反馈、验证和环境设计这些外循环系统。
- 对 FinTech 团队来说，更现实的机会仍然是把权限、流程、资金操作和内部协作整理成可被 Agent 安全调用的接口，而不是只追逐最新模型。
