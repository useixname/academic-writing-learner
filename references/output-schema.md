# Output schemas

Use these as an internal completeness checklist. Render them as concise prose, a table, or tracked revisions according to the user's requested format; do not expose empty fields.

## LEARN

```yaml
paper_learning:
  corpus_boundary: sources, material_available, relevant_context, limitations
  ingestion: included_units, excluded_material, extraction_quality
  source_assessment: corpus_role, rationale
  learning_profile:
    status: constructed|not-needed
    scope: current-context-only
    persistence: transient-only
    exposed_to_user: true|false
  transferable_patterns:
    - pattern: functional description
      level: word|phrase|sentence|paragraph|section|paper-argument
      local_role: rhetorical function
      appropriate_when: condition
      avoid_when: condition
      transfer_level: conceptual|structural|lexical
      evidence: source and context/count
      evidence_source: Reference-evidenced
      confidence: high|medium|low
  avoid_learning: patterns and rationale
  transfer_guidance: prioritized lessons
```

## APPLY

```yaml
revision:
  original_intent: propositions and rhetorical role
  revision_budget: low|medium|high
  integrity_locks: summarize only protected items relevant to the user-facing result
  learning_profile_used: explicit current-context profile or none
  verdict: keep|revise|safe-partial-revision|clarify-before-revising
  revised_text: user-facing text when revision is warranted
  preserved_elements: meaning, terminology, claim strength, voice
  substantive_changes:
    - change: what changed and why
      evidence_source: Reference-evidenced|User-evidenced|Domain-general|Model-inferred
      evidence: source/context or explanation
      confidence: high|medium|low
  limits: unavailable evidence or unresolved choice
```

For `keep`, state briefly why no change is warranted. Do not pad the result with speculative alternatives.

## EXPLAIN / COMPARE / AUDIT

```yaml
analysis:
  question_or_scope: user request
  observations: direct, contextualized observations
  interpretation: conclusion with evidence source
  alternatives_or_conflicts: only when relevant
  recommendation: context-specific action or no change
  confidence: high|medium|low
  limits: what the evidence cannot establish
```

For COMPARE, report both raw occurrence frequency and paper prevalence whenever a count is used. For AUDIT, add location, severity, and a distinction between a material finding and a stylistic preference.

## Citation discipline

Identify source text by user-provided filename, paper label, section, paragraph, or excerpt location whenever available. Do not pretend to have counts, page numbers, venue facts, or broad-corpus evidence that were not observed.
