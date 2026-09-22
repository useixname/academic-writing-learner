# User Language Profile

Use this profile to preserve the user's manuscript voice and established terminology. It is evidence from the current draft or explicitly supplied prior writing, not a license to preserve actual errors.

## Build only from sufficient material

When multiple relevant user passages exist, identify stable choices rather than tallying every token. If only one sentence is supplied, treat its language as local context; do not infer a whole-author style. Record observations rather than normative judgments.

```yaml
user_language_profile:
  source_scope: current draft sections or supplied writing samples
  established_terminology:
    method_names: []
    dataset_names: []
    metric_names: []
    technical_terms: []
    abbreviations: []
    variable_names: []
    defined_concepts: []
  preferred_verbs: []
  preferred_result_language: []
  preferred_transition_style: []
  sentence_complexity: short|mixed|dense|unknown
  recurring_natural_expressions: []
  uncommon_in_user_writing: []
  uncertainty: []
```

## Apply the profile

When equally accurate choices exist, use this order:

```text
scientific correctness
→ established user terminology
→ user's existing clear natural vocabulary
→ relevant reference-paper convention
→ domain-general academic English
→ model preference
```

Do not introduce a new lexical choice when the user's established vocabulary expresses the same scientific meaning clearly and naturally. Do not use a synonym merely to avoid repetition of a technical term. Repetition of a defined method, metric, or concept is usually preferable to ambiguity.

## Vocabulary-drift check

Before accepting a proposed revision, compare it with the local manuscript and profile:

1. Is a new word necessary for a real semantic distinction?
2. Is it a defined technical term or evidenced field convention?
3. Would it make the passage noticeably more ornate, abstract, or formal than surrounding user prose?
4. Does it displace a protected term or a stable natural user choice?

If the answer to 1 and 2 is no, and 3 or 4 is yes, reject the new lexical choice. Label any remaining uncertainty as `Model-inferred`, not as user preference.

## Reader-familiarity check

Before introducing an uncommon nontechnical word, ask:

1. Is it necessary for scientific precision?
2. Is it established terminology in the manuscript?
3. Is it conventional in the relevant reference corpus?
4. Does it express a distinction that a simpler familiar word cannot?

If all four answers are no, prefer the simpler familiar wording. Do not introduce lexical novelty merely to make prose appear more academic. This is a check for reader-facing clarity, not an attempt to guess an individual advisor's or reviewer's preferences.
