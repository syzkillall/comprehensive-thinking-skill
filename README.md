# Comprehensive Thinking

[English](#comprehensive-thinking) | [中文完整说明](README.zh-CN.md)

A reasoning skill for AI agents to improve complex judgment, premise auditing, counterargument pressure, and verifiable conclusions.

Comprehensive Thinking is designed for moments when a short answer is not enough: strategy decisions, architecture judgments, debugging direction, research evaluation, medical or legal information review, and other high-cost problems where rough reasoning can create real damage.

It does not ask the AI to simply "think more". It asks the AI to make its reasoning easier to inspect, challenge, correct, and verify.

<details>
<summary>中文</summary>

全面思考是一套为 AI Agent 设计的推理型 Skill，用来提升 AI 在复杂判断、前提审计、反方压力和可验证结论方面的质量。

它适用于那些不能只靠一句话回答的问题：战略判断、架构选择、复杂 bug 方向、研究价值判断、医学或法律信息审视，以及其他一旦粗糙推理就可能造成真实代价的场景。

全面思考不是让 AI 简单地“多想一点”，而是让 AI 的思考过程更容易被审视、被质疑、被修正，也更容易被验证。

</details>

## Readability

Comprehensive Thinking is written to be serious, precise, calm, and developer-facing.

The goal is not to sound grand. The goal is to make AI reasoning trustworthy enough for problems where conclusions need to survive scrutiny. A good answer should redefine the real problem, expose hidden assumptions, identify the key contradiction, introduce strong opposing views, and close with a path that can be checked.

<details>
<summary>中文</summary>

全面思考的英文气质应该是：严肃、精准、克制、面向开发者。

它不追求宏大的修辞，而是让 AI 的推理在严肃问题中经得起审视。一次好的回答应该重新定义真实问题，暴露隐藏前提，识别关键矛盾，引入有力量的反方意见，并把结论收束到可以检查的路径上。

</details>

## Quick Start

Install as a personal Codex skill:

```bash
git clone https://github.com/syzkillall/comprehensive-thinking-skill.git ~/.codex/skills/comprehensive-thinking
```

Then restart Codex so the skill can be loaded.

For Claude Code, Claude.ai, update, and uninstall instructions, see [INSTALL.md](INSTALL.md).

<details>
<summary>中文</summary>

作为 Codex 个人 Skill 安装：

```bash
git clone https://github.com/syzkillall/comprehensive-thinking-skill.git ~/.codex/skills/comprehensive-thinking
```

然后重启 Codex，让新的 Skill 被加载。

Claude Code、Claude.ai、更新和卸载方式，请看 [INSTALL.md](INSTALL.md)。

</details>

## Usage

Trigger the skill by asking for `comprehensive-thinking`, `全面思考`, or a similar high-responsibility reasoning request.

Example prompts:

```text
Please use comprehensive-thinking to judge whether this product should move from a tool to a platform.

请用全面思考分析：这个多模块系统是否应该重构为事件驱动架构？

请用全面思考帮我想清楚：我是否应该投入一年时间做这个方向？
```

More prompt examples are available in [examples/prompts.md](examples/prompts.md).

<details>
<summary>中文</summary>

你可以通过 `comprehensive-thinking`、`全面思考`，或者同等高责任复杂判断请求来触发这个 Skill。

示例：

```text
请用全面思考帮我判断：我现在是否应该把这个产品从工具型产品转向平台型产品？

请用全面思考分析：这个多模块系统是否应该重构为事件驱动架构？

请用全面思考帮我想清楚：我是否应该投入一年时间做这个方向？
```

更多示例见 [examples/prompts.md](examples/prompts.md)。

</details>

## When To Use It

Use this skill when the problem has at least one of these traits:

- High complexity: multiple systems, actors, stages, incentives, or tradeoffs.
- High uncertainty: important facts are missing or easy to misread.
- High cost of being wrong: the answer affects money, safety, trust, architecture, reputation, or long-term direction.
- Structural causes: the visible problem may be only a symptom.
- Value tradeoffs: there is no simple right answer.

It is especially useful for product strategy, engineering architecture, root-cause analysis, research direction, serious personal or organizational decisions, and AI agent evaluation.

<details>
<summary>中文</summary>

当问题具备以下特征之一时，适合使用全面思考：

- 高复杂度：涉及多个系统、角色、阶段、激励或取舍。
- 高不确定性：关键事实不足，或事实容易被误读。
- 错误代价高：答案会影响资金、安全、信任、架构、声誉或长期方向。
- 存在结构性原因：表面问题可能只是症状。
- 存在价值取舍：没有简单的正确答案。

它特别适合产品策略、工程架构、根因分析、研究方向、严肃的个人或组织决策，以及 AI Agent 质量评估。

</details>

## How It Works

The skill uses a five-review reasoning structure:

1. Define the key problem and domain.
2. Use master-level theory systems to establish the judgment axis.
3. Collect key facts and build a problem-specific synthesis.
4. Apply counterargument pressure and premise analysis.
5. Close with a full-picture understanding and a verifiable path.

The core principle is:

```text
High-quality conclusion = master logic x key real information
```

The skill is not meant to fill a template. Each review must change the problem definition, evidence selection, judgment boundary, opposing view, or verification path.

<details>
<summary>中文</summary>

全面思考使用五重审视结构：

1. 定义关键问题与领域。
2. 用领域大师理论体系建立判断主轴。
3. 收集关键事实，并形成当前问题自己的综合理解。
4. 加入最强反方意见，并进行前提辩证分析。
5. 收束到全貌理解与可验证路径。

核心原则是：

```text
高质量结论 = 大师逻辑 x 关键真实信息
```

全面思考不是为了填模板。每一重审视都必须真正改变问题定义、证据选择、判断边界、反方压力或验证方式。

</details>

## Repository Map

```text
SKILL.md                         Runtime skill instructions
INSTALL.md                       Installation guide
agents/openai.yaml               UI metadata and default prompt
examples/prompts.md              Example prompts
evals/quality-checklist.md       Quality checklist and scoring guide
references/master-theory-research.md
                                 Reference notes for theory selection
README.zh-CN.md                  Full Chinese README
```

<details>
<summary>中文</summary>

```text
SKILL.md                         Skill 运行说明
INSTALL.md                       安装说明
agents/openai.yaml               UI 元数据与默认提示
examples/prompts.md              示例提示词
evals/quality-checklist.md       质量检查清单与评分方式
references/master-theory-research.md
                                 理论体系选择参考
README.zh-CN.md                  中文完整说明
```

</details>

## Quality Checklist

A good Comprehensive Thinking answer should:

- Redefine the real problem instead of answering only the surface question.
- Clarify the object, boundary, success standard, and cost of being wrong.
- Use theory as reasoning logic, not decoration.
- Identify the key contradiction and judgment axis.
- Use real facts that could change the conclusion.
- Build a synthesis specific to the current problem.
- Include a strong opposing view.
- Audit hidden premises.
- Explain scope, unknowns, risks, and falsifying conditions.
- End with evidence, experiment, implementation, testing, acceptance, or documentation.

See [evals/quality-checklist.md](evals/quality-checklist.md) for the full checklist.

<details>
<summary>中文</summary>

一次有效的全面思考应该：

- 重新定义真实问题，而不是只回答表层问题。
- 明确讨论对象、边界、成功标准和错误代价。
- 让理论体系真实参与推理，而不是作为装饰。
- 识别关键矛盾和判断主轴。
- 使用能改变结论的真实事实。
- 形成当前问题自己的综合理解。
- 给出有力量的反方意见。
- 审计隐藏前提。
- 说明适用范围、未知、风险和可推翻条件。
- 最终落到证据、实验、实现、测试、验收或文档沉淀之一。

完整清单见 [evals/quality-checklist.md](evals/quality-checklist.md)。

</details>

## Why This Exists

AI can help us solve problems, but do we trust its answers?

For many complex questions, AI answers can feel too summary-first: a quick scan of information, a confident structure, and then a conclusion that appears polished but not fully examined. The missing part is not only information. It is the quality of reasoning.

In some domains, rough reasoning is expensive. People ask medical questions, researchers evaluate serious directions, engineers design fragile systems, and teams make decisions that shape long-term outcomes. In those contexts, the answer should not merely sound reasonable. It should be inspectable.

Comprehensive Thinking was created to explore how AI agents can be guided toward higher-quality reasoning processes: better problem definition, better premise auditing, better counterargument pressure, and better verification.

<details>
<summary>中文</summary>

AI 可以帮助我们解决问题，但我们信任它的答案吗？

当我们遇到一些复杂问题时，AI 的表现有时并不让人放心。它可以在互联网上搜集信息，再把这些信息总结后提供给我们，但这些答案常常缺少信任感。这种信任感的缺失不只是信息不足，更是推理质量不足。

在一些场景中，老百姓的寻医问药，学者们对专业领域的研究，工程师们设计精密的系统，团队做长期方向判断，这些场景都需要严肃的推理。粗糙不是风格问题，粗糙会带来真实代价。

全面思考就是在这个背景下诞生的。它试图探索如何引导 AI Agent 形成更高质量的思维过程：更好的问题定义，更好的前提审计，更强的反方压力，以及更可验证的结论收束。

</details>

## About The Author

Created by 元臻, a product manager and independent developer exploring AI agents, reasoning systems, and skill design.

WeChat: `Syz_Anakin`

Open to exchange and collaboration.

<details>
<summary>中文</summary>

作者：元臻

产品经理、独立开发者，折腾 AI 中。

微信：`Syz_Anakin`

欢迎交流、合作。

</details>

## License

Apache-2.0. See [LICENSE](LICENSE).
