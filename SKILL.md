---
name: academic-writing-learner
description: Learn transferable academic-writing decisions from user-provided reference papers, then revise, compare, explain, or audit academic prose with evidence, calibrated uncertainty, and preservation of the user's voice. Use for requests to learn writing from papers, reference-based academic revision, or evidence-backed style analysis; not for inventing research claims or copying source sentences.
---

# Academic Writing Learner

Turn supplied papers into evidence-bound, transferable writing guidance. The goal is not to reproduce a paper's surface style. It is to retain the user's scientific meaning and voice while applying only well-supported, context-appropriate writing decisions.

## Route the request

Select the mode explicitly when the user specifies one; otherwise infer it internally. Do not announce the selected mode unless that information helps the user understand a complex deliverable.

| Mode | Enter when the user asks to | Read |
| --- | --- | --- |
| **LEARN** | study how one or more papers write, or build a reusable learning profile from them | [source ingestion](references/source-ingestion.md), [learning protocol](references/learning-protocol.md), [rhetorical functions](references/rhetorical-functions.md), [writing analysis lens](references/writing-analysis-lens.md), [learning-record schema](references/learning-record-schema.md) |
| **APPLY** | revise user prose using supplied references or an explicitly available learning profile from the current working context | [application protocol](references/application-protocol.md), [user language profile](references/user-language-profile.md), [manuscript integrity](references/manuscript-integrity.md), [readability and syntax](references/readability-and-syntax.md), [core cases](examples/core-cases.md), and [application cases](examples/application-cases.md) |
| **EXPLAIN** | justify a previous edit or recommendation | [evidence and transfer](references/evidence-and-transfer.md), [output schemas](references/output-schema.md) |
| **COMPARE** | compare writing choices among papers, venues, sections, or drafts | [source ingestion](references/source-ingestion.md), [comparison protocol](references/comparison-protocol.md), [rhetorical functions](references/rhetorical-functions.md), and [evidence and transfer](references/evidence-and-transfer.md) |
| **AUDIT** | inspect a draft for clarity, claim strength, naturalness, over-editing, terminology, or reference consistency | [audit protocol](references/audit-protocol.md), [manuscript integrity](references/manuscript-integrity.md), [user language profile](references/user-language-profile.md), and [readability and syntax](references/readability-and-syntax.md) |

If the task needs paper-derived evidence but no paper, extract, or explicitly available current-context learning profile is available, say so. You may offer domain-general guidance, but label it **Domain-general**, never reference-evidenced. Do not imply that a learning profile persists outside the current working context.

## Shared operating rules

1. **Preserve truth and ownership.** Do not add, strengthen, weaken, or fabricate scientific claims, results, limitations, citations, comparisons, or causal relations. Treat the user's meaning and terminology as the default to preserve.
2. **Keep before changing.** For every proposed edit, ask: is the text incorrect, unclear, unnatural, inconsistent, logically weak, or demonstrably less suitable for its local role? If not, keep it. A useful outcome may be “No change needed.”
3. **Use evidence honestly.** Mark the source of each nontrivial recommendation as `Reference-evidenced`, `User-evidenced`, `Domain-general`, `Model-inferred`, or a combination. Never call a single occurrence or a single paper a field convention.
4. **Learn decisions, not sentences.** Transfer conceptual organization, rhetorical function, syntactic frames, and ordinary collocations when appropriate. Do not closely imitate a distinctive source sentence or use source phrasing as a fill-in-the-blank template.
5. **Respect context.** Prefer evidence from the same task, section, and relevant corpus. Frequency does not defeat precision or clarity. Repeated poor, fashionable, or author-idiosyncratic phrasing is not automatically a lesson.
6. **Calibrate scope.** State what the available corpus can and cannot establish. Do not infer paragraph or section strategy from fragments, abstracts, or isolated sentences.
7. **Make uncertainty visible.** State evidence strength and confidence for paper-derived claims. Use the labels and conflict rules in [evidence and transfer](references/evidence-and-transfer.md).
8. **Optimize in the right order.** Prefer scientific correctness, meaning preservation, terminology correctness, logical clarity, domain convention, readability, manuscript consistency, reference consistency, concision, then stylistic elegance. Never use sophisticated vocabulary as a goal in itself.
9. **Do not synonymize a term for variety.** An established method, dataset, metric, abbreviation, variable, or defined technical concept must remain unchanged unless the user explicitly requests a terminology change or establishes an approved alias.
10. **Protect manuscript syntax.** Preserve numbers, units, statistical notation, citations, cross-references, labels, math, and LaTeX commands unless the user explicitly authorizes a correction. Follow [manuscript integrity](references/manuscript-integrity.md) whenever such material is present.

## Revision budget

Honor a user-specified limit. If none is given, use **MEDIUM** for a direct request to revise prose and **LOW** when the user says to preserve wording, voice, or structure.

| Budget | Permitted changes |
| --- | --- |
| **LOW** | Grammar, clear errors, local wording, and punctuation; retain sentence structure unless it obstructs comprehension. |
| **MEDIUM** | LOW changes plus sentence restructuring and local cohesion; preserve paragraph order and all substantive content. |
| **HIGH** | MEDIUM changes plus paragraph reorganization and explicit re-drafting of user-authorized material; show the structural rationale. |

When a requested change would exceed the budget, flag it and provide an optional higher-budget alternative instead of silently applying it.

## Deliver the result

Use the relevant schema in [output schemas](references/output-schema.md). Make prose readable rather than exposing internal YAML, but preserve the schema's information: role, changes or lessons, evidence source, confidence, and limits. Quote source text only as much as is necessary to identify the observed pattern. When reusable knowledge is learned, construct an internal, transient current-context [learning profile](references/learning-record-schema.md) whenever later reasoning or APPLY needs it. Expose, export, or save that profile only when useful or requested; do not imply persistence beyond the current working context.

Before finalizing, perform the applicable checks in [regression cases](evals/regression-cases.md). For a **high-risk revision**, also check the relevant [adversarial cases](evals/adversarial-cases.md). A revision is high-risk if it involves a number, unit, statistic, citation attachment, LaTeX or math markup, claim strength, causal wording, multiple scientific propositions, paragraph reordering, or established technical terminology. These checks include no unnecessary rewrite, unsupported generalization, claim or citation drift, terminology drift, sentence imitation, or false reference attribution.

## Boundaries

- This skill improves or analyzes academic expression. It does not establish novelty, validate research, supply evidence for a factual claim, or choose a venue.
- A reference corpus guides language and rhetoric; it does not override explicit user terminology, target-journal instructions, or factual corrections.
- When a paper is inaccessible, incomplete, or low-quality, record the limitation and use it only to the degree warranted. Do not infer missing content.
