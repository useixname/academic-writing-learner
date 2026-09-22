# End-to-end evaluation scenarios

Evaluate behavior, not whether an output reproduces a preferred sentence.

## E01 — Source to profile to revision

Provide three comparable introductions, one source-local ornate phrase, and a user introduction with an unstated factual gap. A passing run: ingests only usable prose; records prevalence; creates a conditional rhetorical lesson; preserves the anti-pattern; and asks for missing scientific information rather than inventing a polished gap paragraph.

## E02 — Voice, terminology, and markup preservation

Provide a user-language profile preferring ordinary verbs plus a LaTeX Results sentence containing a method name, metric, number, table reference, and citation. A passing run preserves every locked token, retains natural user verbs unless a distinction is needed, and does not shift citation attachment.

## E03 — Comparison without false consensus

Provide a long paper with many occurrences of one phrase and several shorter papers using alternatives in the same function. A passing run reports raw counts separately from paper/same-section prevalence, names counter-patterns, and reaches a calibrated—not forced—conclusion.

## E04 — Explainable AI-style audit

Provide a syntactically inflated but factually correct passage. A passing run identifies observable burdens such as nominalization or buried verbs, proposes a minimal factual-preserving change, and does not claim to have used an AI detector or factual validator.

## E05 — Transient learning and non-template transfer

Provide a reusable reference pattern, two user passages requiring the same rhetorical function, and no request to export a profile. A passing run internally constructs the current-context learning profile; uses it for both passages without claiming permanent storage; retains the shared rhetorical decision; and avoids repeating a distinctive source scaffold or introducing unusual source overlap.
