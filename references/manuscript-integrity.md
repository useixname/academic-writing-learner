# Manuscript integrity

Use whenever the input contains scientific, bibliographic, mathematical, or markup-bearing content. This protocol is a preservation guardrail, not permission to alter protected content.

## Protect by default

Lock these items before revision:

```text
numbers, percentages, ranges, dates, units, statistical values, significance markers
method, model, dataset, benchmark, metric, variable, and abbreviation names
comparators, experimental conditions, scopes, quantifiers, and uncertainty markers
citations and their attachment to the claims they support
LaTeX commands, environments, math delimiters, labels, refs, cites, and formatting macros
figure/table/equation identifiers and cross-references
URLs, accession identifiers, code identifiers, file paths, and user-defined symbols
```

Examples of protected tokens include `3.2\%`, `$F_1$`, `\textsc{Baseline}`, `Table~\ref{tab:main}`, `\cite{smith2025}`, `\label{sec:method}`, and `\begin{equation}`. Preserve exact commands and balanced delimiters even when revising nearby prose.

## Establish locks before editing

Use this internal record for any substantive revision:

```yaml
proposition_lock:
  main_claims: []
  entities: []
  method_names: []
  comparisons: []
  conditions: []
  qualifiers_and_uncertainty: []
  causal_relations: []
  quantities_and_units: []
  citations: []
terminology_lock:
  method_names: []
  dataset_names: []
  metric_names: []
  technical_terms: []
  abbreviations: []
  variable_names: []
  defined_concepts: []
markup_lock:
  latex_commands_and_environments: []
  math_expressions: []
  cross_references: []
```

## Verify after editing

Compare revised text against each lock. Confirm that values, units, scope, polarity, comparators, conditions, citations, reference targets, and markup remain attached to the same factual content. Do not move a citation across a sentence boundary if doing so changes which claim it appears to support.

Do not synonymize locked terminology for stylistic variety. If a protected item appears erroneous, flag it separately and request or apply only the user-authorized correction. Never “repair” an unknown citation key, label, number, or equation by guessing.

## Report integrity limits

For a prose-only revision, briefly state only material preservation constraints that affected the result. For a high-risk or LaTeX-heavy revision, state that protected tokens were preserved and identify any unresolved potential error without claiming compilation or factual verification.
