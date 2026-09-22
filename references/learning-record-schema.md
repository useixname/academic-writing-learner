# Academic Writing Learning Profile

This profile is the bridge between a completed LEARN task and a later APPLY task. It is a transient current-context record, not implied long-term memory. Whenever reusable learning is needed for subsequent reasoning or APPLY, construct it internally even when the user did not request a visible report or saved file. Create it only from inspected material; omit unknown fields rather than filling them from general knowledge.

## Required provenance fields

```yaml
learning_profile:
  profile_scope:
    target_field: user-supplied or observed scope
    intended_use: learn|apply|compare|audit
    created_from: source labels
    persistence: current working context only
  corpus:
    papers:
      - source: identifier
        usable_sections: []
        material_quality: clean|partially_extracted|ocr_uncertain|fragmentary
        corpus_role: high-confidence|medium-confidence|context-only
    limitations: []
```

## Knowledge fields

Store each item as a compact decision record, never as a source sentence to reuse.

```yaml
  lexical_profile:
    preferred: []              # ordinary, evidence-supported choices
    domain_standard: []        # terms/collocations tied to the field
    context_dependent: []
    uncommon_or_avoid_unless_needed: []
  collocations: []
  rhetorical_patterns: []
  sentence_patterns: []
  paragraph_patterns: []
  section_patterns: []
  claim_patterns: []
  cohesion_patterns: []
  anti_patterns: []
  transferable_lessons: []
  unresolved_observations: []
```

Each nonempty item must include:

```yaml
  pattern: functional description
  level: word|phrase|sentence|paragraph|section|paper-argument
  local_role: canonical rhetorical-function label where relevant
  appropriate_when: []
  avoid_when: []
  transfer_level: conceptual|structural|lexical
  classification: positive|neutral|author-specific|overused|avoid
  evidence:
    paper_prevalence: "n/N comparable papers"
    occurrence_count: optional raw count
    scope: comparable section and function
    anchors: []
  evidence_source: Reference-evidenced
  confidence: high|medium|low
```

## Use in APPLY

Retrieve only records that match the user's current section, rhetorical role, and revision need. A profile is guidance, not authority to change scientific content. If the profile lacks an applicable item, retain clear user language or use explicitly labelled domain-general advice.

## Update and invalidation

Add observations only after the learning protocol and source-ingestion rules are met. Keep contradictory observations rather than overwriting them. Update paper prevalence when the comparable corpus changes. Mark a record `stale_for_current_task` when its field, genre, target section, or available corpus no longer matches the requested revision. Do not export or persist the transient record unless useful or requested.
