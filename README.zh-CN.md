# Academic Writing Learner

**语言：** [English](README.md) | [简体中文](README.zh-CN.md)

一个以证据为边界的 Codex Skill：它从参考论文中学习可迁移的学术写作决策，并将其应用于用户论文，同时不替换用户的写作声音、术语、科学含义或 LaTeX 结构。

Academic Writing Learner 不把学术写作视为同义词替换。它学习参考论文表达背后的决策——修辞功能、证据基础、适用条件和迁移上限——并且只在这些决策与用户真实的科学内容相匹配时使用它们。

## 它能做什么

- 从用户提供的论文、正文摘录、PDF、LaTeX 源文件或其他可读研究材料中学习。
- 将可学习的正文与参考文献、模板 boilerplate、损坏的 OCR、孤立表格单元格等会干扰分析的内容分开。
- 构建当前上下文内暂存的 Learning Profile，其中包含可追溯证据、置信度、章节/功能范围和负面模式。
- 采用 `KEEP` 优先、最小充分干预的策略修订文字。
- 保护科学命题、数字、单位、引用、技术术语、数学表达式、交叉引用和 LaTeX 命令。
- 让用户已建立的自然语言优先于风格新奇性和模型偏好。
- 不依赖 AI detector 分数，直接识别词汇和句法层面的 AI 式膨胀。
- 以论文覆盖率和可比较语境，而不是单纯出现次数，比较多篇参考论文中的模式。

## 核心原则

```text
交际意图
    ↓
写作决策
    ↓
适合具体语境的语言实现
```

该 Skill 可以迁移概念组织、修辞动作、一般结构和普通且符合领域习惯的搭配；但不会复制来源论文中具有辨识度的句子、编造证据，或把用户论文改写成某位参考作者的声音。

## 工作流

```text
参考材料
  → source ingestion 与 evidence boundary
  → 修辞与写作分析
  → 当前上下文内暂存的 Learning Profile
  → 用户语言与 manuscript integrity 约束
  → KEEP 或最小充分修订
  → 语义、术语、可读性和 source independence 检查
  → 最终文本
```

只有在后续推理或修订确实需要时，才会在内部构建暂存 Learning Profile。它仅在有用或用户要求时展示/保存，并不表示跨会话或长期记忆。

## 工作模式

| 模式 | 用途 |
| --- | --- |
| `LEARN` | 从提供的材料中学习可复用、有证据支撑的写作决策。 |
| `APPLY` | 以 Learning Profile 为依据，在保留含义的前提下最小干预地修订用户文本。 |
| `EXPLAIN` | 从修辞目的、证据和取舍角度解释一次修改。 |
| `COMPARE` | 在提供的可比较语料中比较写作模式，不制造虚假的共识。 |
| `AUDIT` | 对完整性、术语、可读性、风格漂移和过度修改进行可解释审计。 |

## 安全性与完整性

在实质性修改前，Skill 会锁定相关命题、实体、方法名称、比较对象、条件、限定语、不确定性、因果关系、数值、引用、术语和标记语法。只要修订涉及下列任一内容，就会被视为高风险并触发额外的 adversarial checks：

```text
数字或统计值 · 引用 · LaTeX 或数学表达式 · claim/causal wording
多个科学命题 · 段落重排 · 已建立的技术术语
```

source-independence 检查会判断重叠表达是否具有独特性和来源特异性；它不会使用固定 n-gram 阈值，从而避免把正常学术搭配或必要术语误判为来源泄漏。

## 仓库结构

```text
.
├── SKILL.md                         # 入口、模式路由和共享规则
├── references/                      # 各模式按需读取的协议与 schema
├── examples/                        # 核心、学习、应用、失败和端到端案例
├── evals/                           # 回归、对抗和端到端评估场景
├── CHANGELOG.md
└── LICENSE
```

请从 [SKILL.md](SKILL.md) 开始。它会为每个模式路由到实际需要的参考文件，而不是在每个任务中加载全部细则。

## 安装

将仓库克隆到 Codex 的 skills 目录，然后重新开启 Codex 会话，使其发现该 Skill：

```bash
git clone https://github.com/useixname/academic-writing-learner.git \
  ~/.codex/skills/academic-writing-learner
```

如果设置了 `CODEX_HOME`，请改用其 `skills/academic-writing-learner` 子目录。之后可以显式调用 `$academic-writing-learner`，或让 Codex 在匹配的学术写作任务中自动选择它。

## 评估与迭代

仓库内的评估资产检验以下不变量：科学含义保留、正确的 `KEEP` 行为、术语与引用保留、无依据的领域泛化、无必要词汇升级，以及无具有辨识度的来源语言泄漏。

这是一个面向 behavior-driven refinement 的 v1.0 候选版本。只有在真实的“参考论文 + 用户草稿”任务中观察到新的失败模式时，才应增加规则、案例或评估。

## 贡献

贡献应持续遵守以下边界：

1. 不能因为来源表达更高频，就用来源语言替换用户语言。
2. 不能把局部来源观察升级为领域范围的结论。
3. 不能削弱 manuscript integrity 或 source-independence 检查。
4. 与其不断累积宽泛规则，不如针对真实失败案例做窄而明确的修正。

## 许可证

本项目采用 [MIT License](LICENSE)。
