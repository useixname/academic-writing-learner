# End-to-end cases

## Learn → profile → apply to an introduction

**Supplied corpus:** Three complete introductions in the same field. Each identifies a concrete limitation after describing relevant progress; all use simple result and transition verbs. One paper alone repeatedly uses an ornate phrase.

**Learning profile:**

```yaml
rhetorical_patterns:
  - pattern: acknowledge progress then state a remaining limitation
    local_role: state-limitation
    evidence: {paper_prevalence: "3/3 comparable introductions"}
    confidence: high
    transfer_level: conceptual
lexical_profile:
  preferred: [show, use, improve]
anti_patterns:
  - pattern: ornate recurring phrase in one paper
    classification: author-specific
    confidence: low
```

**User draft:** “LLM agents are widely used. However, they have memory problems. We propose MemAgent.”

**Context lock:** The draft does not specify the exact limitation or consequence. Do not invent either.

**Safe result:** Do not invent the limitation or consequence. Provide any safe local revision available from the supplied content, such as a low-budget cohesion edit, and identify the missing scientific step that prevents a fuller gap-to-solution rewrite. Ask for clarification only if the user specifically requests that fuller rewrite and it cannot meaningfully proceed without the missing information. Do not fabricate a long-horizon limitation, experimental result, or method contribution.

**Lesson:** A strong learned rhetorical pattern does not authorize filling missing scientific content.

## Reference disagreement and author voice

**References:** Two papers use `demonstrate` for controlled evaluations; two use `show` for descriptive results. The user's established Results style uses `show`.

**User sentence:** “Table~\ref{tab:main} shows that our method improves accuracy by 3.2\%.”

**Outcome:** Keep `shows`. The profile contains no universal winner, and the user's clear established wording matches a neutral result-reporting role. Do not replace it merely because another source uses a stronger verb.

## Paragraph logic rather than grammar

**Draft:** “We use Dataset A. Our method improves accuracy by 3.2\%. Dataset A contains 10 classes.”

**Diagnosis:** Each sentence is grammatical, but the dataset description interrupts result reporting.

**MEDIUM revision:** Reorder only if the surrounding context does not already define Dataset A: describe the dataset before the result, then preserve the metric and comparison locks. If Dataset A is defined immediately before this paragraph, retain the order and instead make the result transition explicit.

**Lesson:** Paragraph restructuring is conditional on local context and budget.
