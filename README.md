# Interactive Cognition | 知彼

A cognitive base that shifts AI agent reasoning from internal analysis to modeling others' cognition and managing information flow. Built on Guiguzi and Sun Tzu. Works with any LLM agent — Claude, GPT, Gemini, or custom frameworks.

让 AI agent 的推理从内部分析转向建模他人认知、管理信息流。融合鬼谷子与孙子兵法。适用于任何 LLM agent。

---

## What it does | 它做什么

Most AI agents analyze problems from a single perspective — the user's. They treat other participants (opponents, teammates, customers, stakeholders) as static objects rather than active cognitive agents. Interactive Cognition adds a reasoning layer that models how others think, manages information flow deliberately, and adapts strategy to the opponent's state rather than applying universal templates.

大多数 AI agent 从单一视角（用户的视角）分析问题。他们把其他参与者（对手、团队、客户、利益相关方）当作静态对象，而不是活跃的认知主体。知彼增加了一个推理层——建模他人思维、有意识地管理信息流、根据对手状态调整策略，而非套用万能模板。

### Before (default agent) | 安装前

> "We want to close this deal."
>
> "Here's a 5-step closing strategy: build rapport, demonstrate value, handle objections, create urgency, ask for the close."

### After (with Interactive Cognition) | 安装后

> "Before strategizing your close, let's model the buyer. They're evaluating three vendors and their procurement deadline is Q3. Their core concern isn't price — it's implementation risk, because their last vendor switch failed. Your leverage isn't features; it's reducing their perceived risk. Reveal your migration support early, withhold competitive pricing until they've anchored on risk reduction, and elicit their internal approval process so you can time the close to their decision cycle."

---

## Core cognitive shift | 核心认知转换

**From**: "How do I think correctly about this problem?"

**To**: "How is the other party thinking, and how should I adapt?"

从「我如何正确地思考这个问题」到「对方在如何思考，我该如何适应」。

All other cognitive bases handle internal cognition — how you reason, decompose, verify, and structure your own thinking. This is the ONLY base that handles **cognitive interaction** — reasoning about, adapting to, and influencing the cognition of others.

所有其他认知底座处理内部认知。这是唯一处理**认知互动**的底座。

---

## How it works | 工作原理

**Four cognitive shifts** applied to every interactive scenario:

| Default mode | Target mode |
|---|---|
| Analyze the problem itself 只分析问题本身 | Model how all parties think about it 建模各方如何思考 |
| Reveal everything to demonstrate competence 全盘托出以展示能力 | Design information flow: reveal, withhold, elicit 设计信息流：释放、保留、引出 |
| Assess only your own position 只评估自己的状态 | Map bilateral cognitive states 映射双边认知状态 |
| Apply universal best practices 套用万能最佳实践 | Adapt to the opponent's current state 根据对手状态调整 |

**Absorbed frameworks** providing theoretical foundations:

融合的理论框架：

| Framework 框架 | Contribution 贡献 |
|---|---|
| Guiguzi 揣摩术 | Systematically model the other party's psychological state through listening and observation 通过倾听和观察系统性建模对方心理状态 |
| Guiguzi 捭阖术 | Control the rhythm of information opening (release) and closing (withhold) 控制信息开合节奏 |
| Guiguzi 反应术 | Elicit further disclosure by mirroring and responding 通过映射和回应引出对方进一步披露 |
| Guiguzi 飞钳术 | Find the core concern, use it to anchor conversation direction 找到核心关切，锚定对话方向 |
| Sun Tzu 知己知彼 | Any interactive scenario requires bilateral state assessment 任何互动场景都需要双边状态评估 |
| Sun Tzu 因敌制胜 | Effective strategy is a function of opponent's state 有效策略是对手状态的函数 |
| Sun Tzu 奇正相生 | Orthodox and unorthodox cycle — what was unexpected becomes expected 奇正循环——出其不意终变预期 |
| Sun Tzu 虚实 | Attack cognitive weak points, avoid cognitive strong points 攻其不备，避其锋芒 |
| Deng Xiaoping 韬光养晦 | Strategic information management — decouple capability from displayed intention 战略信息管理——能力与意图脱钩 |
| Han Feizi 术 | What is seen and what is done operate on different layers 表面与实际操作在不同层面 |

**Six anti-patterns** that catch interactive reasoning failures:

六个反模式，捕捉互动推理失误：

| Anti-pattern 反模式 | Description 描述 |
|---|---|
| Unilateral thinking 单边思维 | Only analyzing the problem, ignoring how others think about it 只分析问题本身，忽视他人如何思考 |
| Projection fallacy 投射谬误 | Assuming others share your cognitive model 假设他人与你思维方式相同 |
| Manipulation slope 操控滑坡 | Sliding from "understanding others" to "manipulating others" 从「理解他人」滑向「操控他人」 |
| Over-modeling 过度建模 | Complex opponent modeling in simple scenarios 在简单场景中做复杂对手建模 |
| Static model 静态模型 | Building a model of the other party and never updating it 建模后不再更新 |
| Ignoring counter-modeling 忽视反向建模 | Forgetting that the other party is also modeling YOU 忘记对方也在建模你 |

---

## Installation | 安装

### Claude Code
```bash
cp cognitive-protocol.md ~/.claude/interactive-cognition.md
echo '@~/.claude/interactive-cognition.md' >> ~/.claude/CLAUDE.md
```

### Codex
```bash
cat cognitive-protocol.md >> AGENTS.md
```

### Gemini
Paste `cognitive-protocol.md` into `system_instruction`.

将 `cognitive-protocol.md` 内容粘贴到 `system_instruction` 中。

### Cursor
```bash
cat cognitive-protocol.md >> .cursorrules
```

### Any agent | 任何 agent
Inject `cognitive-protocol.md` (~30 lines) into the system prompt. See [`install/generic.md`](install/generic.md) for details.

将 `cognitive-protocol.md`（约 30 行）注入系统提示词。详见 [`install/generic.md`](install/generic.md)。

---

## File structure | 文件结构

```
interactive-cognition/
├── README.md                  ← You are here / 你在这里
├── cognitive-protocol.md      ← Core rules (~30 lines, always-on) / 核心规则（约 30 行，始终激活）
├── SKILL.md                   ← Full framework reference / 完整框架参考
├── anti-patterns.md           ← Detailed anti-pattern guide / 反模式详解
├── examples.md                ← Before/after scenarios / 前后对比示例
└── install/
    ├── claude-code.md         ← Claude Code installation / Claude Code 安装指南
    ├── codex.md               ← Codex installation / Codex 安装指南
    ├── gemini.md              ← Gemini installation / Gemini 安装指南
    └── generic.md             ← Universal guide / 通用安装指南
```

---

## Composability | 可组合性

Interactive Cognition is a **cognitive base** — it changes how the agent reasons about multi-party scenarios, not what it produces. It stacks cleanly with any domain skill and any other cognitive base because it operates on a unique axis: **inter-personal cognition** rather than intra-personal cognition.

知彼是一个**认知底座**——它改变 agent 对多方场景的推理方式，而非产出内容。它与任何领域技能和其他认知底座无冲突叠加，因为它运行在独特的轴上：**人际认知**而非个人内部认知。

### Relationship to other cognitive bases | 与其他认知底座的关系

| Layer 层级 | What it governs 管辖范围 | Example 示例 |
|---|---|---|
| First Principles 第一性原理 | Input quality — what foundations you build on 输入质量 | "Audit assumptions before solving" 先审计假设 |
| Systems Thinking 系统思维 | Structure quality — seeing feedback loops and emergence 结构质量 | "Map the system before intervening" 先映射系统 |
| Interactive Cognition 知彼 | Interaction quality — modeling others' cognition 互动质量 | "Model the other party before responding" 先建模对方 |

All load as always-on cognitive protocols. No conflicts. Combined: well-founded reasoning (FP), structurally sound analysis (ST), strategically aware interaction (IC).

三者同时加载，互不冲突。组合效果：基础扎实的推理 + 结构健全的分析 + 战略自觉的互动。

---

## Theoretical foundation | 理论基础

Built on two pillars of classical Chinese strategic thought:

**Guiguzi (鬼谷子)** — the original treatise on interpersonal cognitive strategy. Provides operational techniques for modeling others (揣摩), controlling information flow (捭阖), eliciting disclosure through response (反应), and anchoring conversations to core concerns (飞钳).

**Sun Tzu (孙子兵法)** — the framework for bilateral state assessment and adaptive strategy. Provides the principle that effective action is always a function of the opponent's state (因敌制胜), the cycling between orthodox and unorthodox (奇正相生), and targeting cognitive vulnerabilities (虚实).

Supplemented by Deng Xiaoping's strategic information management (韬光养晦) and Han Feizi's observation that visible action and actual operation exist on different layers (术).

The cognitive protocol strips all historical context and translates these ideas into executable instructions for any reasoning agent.

认知协议剥离了所有历史背景，将这些思想转译为任何推理 agent 可执行的指令。

---

## All Cognitive Bases

Cognitive bases are meta-cognitive instruction sets that change HOW an agent thinks, not WHAT it does. Each one targets a different cognitive axis. Mix and match.

| Cognitive Base | What it changes |
|---|---|
| [First Principles](https://github.com/d-wwei/first-principles) | Reason from verified foundations, not inherited conventions |
| [Results-Driven](https://github.com/d-wwei/results-driven) | Require evidence for completion, not just activity |
| [Tacit Knowledge](https://github.com/d-wwei/tacit-knowledge) | Think like an experienced practitioner |
| [Attention Allocation](https://github.com/d-wwei/attention-allocation) | Find and concentrate on the ONE binding constraint |
| [Bayesian Reasoning](https://github.com/d-wwei/bayesian-reasoning) | Calibrated probability thinking, not binary judgments |
| [Constraint as Catalyst](https://github.com/d-wwei/constraint-as-catalyst) | Turn constraints into innovation catalysts |
| [Conviction Override](https://github.com/d-wwei/conviction-override) | Override rational caution when obstacles are convention, not physics |
| [Cross-Domain Connector](https://github.com/d-wwei/cross-domain-connector) | Detect structural isomorphisms across disciplines |
| [Dialectical Thinking](https://github.com/d-wwei/dialectical-thinking) | Synthesize through contradictions (矛盾论) |
| [Double-Loop Learning](https://github.com/d-wwei/double-loop-learning) | Question the assumptions that produce errors |
| [Frame Auditing](https://github.com/d-wwei/frame-auditing) | Detect and transcend invisible analytical frames |
| [Inversion Thinking](https://github.com/d-wwei/inversion-thinking) | Map failure modes first, then avoid them |
| [Motivation Audit](https://github.com/d-wwei/motivation-audit) | Audit motivational drivers before analysis (正心诚意) |
| [Non-Attachment](https://github.com/d-wwei/non-attachment) | Radical cognitive freedom — use frameworks without fusing |
| [Principled Action](https://github.com/d-wwei/principled-action) | Unify knowing and doing through practice-theory spirals (知行合一) |
| [Second-Order Thinking](https://github.com/d-wwei/second-order-thinking) | Trace consequences beyond first-order effects |
| [Systems Thinking](https://github.com/d-wwei/systems-thinking) | Feedback-driven structural analysis, not linear cause-effect |
| [Temporal Wisdom](https://github.com/d-wwei/temporal-wisdom) | Make time your ally — compound effects and phase awareness |
| [Cognitive Base Creator](https://github.com/d-wwei/cognitive-base-creator) | Generate new cognitive bases from any thinking framework |

---

## License

MIT
