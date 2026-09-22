# Academic Writing Learner

An evidence-bound Codex skill for learning transferable academic-writing decisions from reference papers and applying them to a user's manuscript without replacing the user's voice, terminology, scientific meaning, or LaTeX structure.

Academic Writing Learner does not treat academic writing as synonym replacement. It learns the decision behind a reference-paper expression—its rhetorical role, evidence basis, appropriate conditions, and transfer limit—then uses that decision only when it fits the user's real scientific content.

## What it does

- Learns from user-provided papers, excerpts, PDFs, LaTeX sources, or other readable research material.
- Separates usable prose from references, boilerplate, broken OCR, isolated table cells, and other misleading corpus material.
- Builds a transient, current-context learning profile with traceable evidence, confidence, section/function scope, and negative patterns.
- Revises prose with a `KEEP`-first and minimum-sufficient-intervention policy.
- Preserves scientific propositions, numbers, units, citations, technical terminology, math, cross-references, and LaTeX commands.
- Prioritizes the user's established natural language over stylistic novelty and model preference.
- Detects lexical and syntactic AI-like inflation without relying on an AI-detector score.
- Compares supplied papers using paper prevalence and comparable context rather than raw occurrence counts alone.

## Core principle

```text
communicative intention
        ↓
writing decision
        ↓
context-appropriate language realization
```

The skill transfers conceptual organization, rhetorical moves, general structures, and ordinary field-appropriate collocations. It does not copy distinctive source sentences, fabricate evidence, or turn a user's manuscript into the voice of a reference author.

## Workflow

```text
Reference material
  → source ingestion and evidence boundary
  → rhetorical and writing analysis
  → transient learning profile
  → user-language and manuscript-integrity constraints
  → KEEP or minimum sufficient revision
  → semantic, terminology, readability, and source-independence checks
  → final text
```

The transient learning profile is constructed when later reasoning or revision needs it. It is shown or saved only when useful or requested, and it does not imply cross-session or long-term memory.

## Modes

| Mode | Purpose |
| --- | --- |
| `LEARN` | Learn reusable, evidence-bound writing decisions from supplied material. |
| `APPLY` | Revise a user draft with profile-aware, meaning-preserving minimum intervention. |
| `EXPLAIN` | Explain a revision in terms of rhetorical purpose, evidence, and trade-offs. |
| `COMPARE` | Compare patterns across a supplied comparable corpus without false consensus. |
| `AUDIT` | Conduct an explainable audit of integrity, terminology, readability, drift, and over-editing. |

## Safety and integrity

Before a substantive revision, the skill locks relevant propositions, entities, method names, comparisons, conditions, qualifiers, uncertainty, causal relations, quantities, citations, terminology, and markup. A revision involving any of the following is treated as high risk and receives extra adversarial checks:

```text
numbers or statistics · citations · LaTeX or math · claim/causal wording
multiple scientific propositions · paragraph reordering · technical terminology
```

The source-independence check evaluates whether an overlap is distinctive and source-specific; it does not use a fixed n-gram threshold that would misclassify normal academic phrasing or necessary terminology.

## Repository layout

```text
.
├── SKILL.md                         # Entry point, routing, shared rules
├── references/                      # Mode-specific protocols and schemas
├── examples/                        # Core, learning, application, failure, and end-to-end cases
├── evals/                           # Regression, adversarial, and end-to-end evaluation scenarios
├── CHANGELOG.md
└── LICENSE
```

Start with [SKILL.md](SKILL.md). It routes each mode to only the references it needs. The detailed reference files should not all be loaded for every task.

## Install

Clone the repository into the Codex skills directory, then start a new Codex session so the skill can be discovered:

```bash
git clone https://github.com/useixname/academic-writing-learner.git \
  ~/.codex/skills/academic-writing-learner
```

If `CODEX_HOME` is configured, use its `skills/academic-writing-learner` subdirectory instead. You can then invoke it explicitly as `$academic-writing-learner` or let Codex select it for matching academic-writing tasks.

## Evaluation and refinement

The included evaluation assets test invariants such as meaning preservation, correct `KEEP` behavior, terminology and citation preservation, no unsupported field-wide generalization, no unnecessary vocabulary upgrade, and no distinctive source-language leakage.

This is a v1.0 candidate intended for behavior-driven refinement. Add a rule, example, or evaluation only in response to a demonstrated failure mode from real paper-and-draft tasks.

## Contributing

Contributions should preserve these boundaries:

1. Do not replace user language with source language merely because it is more frequent.
2. Do not turn local source observations into field-wide claims.
3. Do not weaken manuscript-integrity or source-independence checks.
4. Prefer a narrow correction backed by a real failure case over broader instruction accumulation.

## License

This project is released under the [MIT License](LICENSE).
