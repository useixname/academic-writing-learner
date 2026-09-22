# Evidence, conflict, and transfer policy

## Knowledge-source labels

Every material recommendation must identify one or more sources:

| Label | Meaning |
| --- | --- |
| **Reference-evidenced** | Directly observed in user-supplied reference material; name the relevant source and context. |
| **User-evidenced** | Required by the user's draft, stated intent, terminology, target, or explicit constraints. |
| **Domain-general** | Broad academic-writing practice, not established by this corpus. |
| **Model-inferred** | A contextual interpretation or suggested fit; it is not evidence of convention. |
| **Insufficient evidence** | The available material cannot justify the requested conclusion. |

Use `Reference-evidenced` only for what the supplied material actually shows. A pattern may be reference-evidenced and still have low confidence or be unsuitable for transfer.

## Resolve competing signals

For a writing choice, evaluate evidence in this order:

1. Scientific correctness and explicit user meaning, including protected terminology and revision budget.
2. The user's established, clear natural vocabulary and manuscript-wide language profile.
3. Accuracy, logical validity, and reader clarity.
4. Same-task and same-section evidence from multiple relevant references.
5. Same-task evidence from a relevant venue or genre, if the corpus establishes it.
6. Multi-paper evidence in the supplied corpus.
7. A recurring pattern within one credible, relevant paper.
8. General academic-writing guidance.
9. Model preference.

Frequency is only a tie-breaker among equally clear, accurate, and contextually fitting alternatives. Never let it override factual precision, user terminology, or a more appropriate rhetorical role.

When evidence remains genuinely mixed, retain the user's acceptable wording or offer alternatives with their conditions. Do not manufacture a consensus. Do not introduce a new lexical choice when the user's established vocabulary expresses the same scientific meaning clearly and naturally.

## Transfer fidelity

| Level | May transfer | Must not do |
| --- | --- | --- |
| **Conceptual** | Argument sequence, information order, and rhetorical move. | Imply that the user's study has the source paper's evidence or contribution. |
| **Structural** | General sentence or paragraph frame after adapting it to the user's actual facts. | Preserve a distinctive syntactic fingerprint or source-specific sequence. |
| **Lexical** | Ordinary technical terms and conventional non-distinctive collocations. | Substitute names into a recognizable source sentence. |

Never perform “sentence imitation”: near-paraphrasing a source sentence, transferring distinctive metaphors or unusual multiword strings, or presenting a source-derived sentence as original user prose.

### Pattern-overuse guardrail

Learned patterns are options, not mandatory templates. A rhetorical decision may recur, but do not repeatedly realize the same function with the same lexical or syntactic scaffold merely because it appeared in a reference or profile. In particular, do not serially reuse stock frames such as “Despite recent advances …”, “To address this limitation …”, or “Experimental results demonstrate …” when a simpler locally fitting realization is available. Vary form only when it improves the local writing; do not vary established technical terminology for style.

## Applying the policy to a draft

1. Identify the user's intended role and propositions before editing.
2. Set or infer the revision budget under the entrypoint rules.
3. Check whether an edit is necessary. If it is not, keep the wording.
4. If changing, use the lowest-fidelity transfer that solves the real problem: conceptual before structural before lexical.
5. Verify that claims, citations, quantifiers, comparisons, uncertainty, and scope remain unchanged unless the user explicitly directs otherwise.
6. Explain each substantive edit in terms of outcome and evidence—not vague assertions that it is “more academic.”
7. Before delivery, inspect the revised text for unusual nontechnical multiword overlap with source material. Do not use a fixed word-count or n-gram threshold as the sole criterion; judge distinctiveness, source-specificity, and whether the wording was unnecessarily preserved. Keep necessary technical terms, conventional academic phrases, and formulaic expressions; independently rewrite distinctive source-specific phrasing.

### Claim-strength guardrail

Do not turn `suggest`, `is associated with`, `may`, `can`, or `is consistent with` into `demonstrate`, `prove`, `causes`, `will`, or `establish` without user-provided evidence and authorization. Conversely, do not weaken an accurately stated claim merely to sound cautious. Flag unsupported claim language instead of silently inventing a replacement premise.

### Minimal-edit guardrail

Do not replace a clear ordinary word with a longer or rarer synonym solely to sound formal (`use` to `utilize`, `show` to `demonstrate`, `help` to `facilitate`). Make such a change only when it adds a real distinction that you state.

## Failure behavior

| Condition | Required response |
| --- | --- |
| One paper or one isolated example | Describe it as an observation in that source; do not call it a field norm. |
| Abstract, excerpt, or damaged extraction only | Limit analysis to units supported by the available text. |
| Sources conflict | State the competing observations and use the resolution order; retain an acceptable user choice when unresolved. |
| Reference expression is unclear, inflated, or awkward | Classify as `Neutral`, `Author-specific`, `Overused`, or `Avoid`; do not learn it merely because it recurs. |
| User asks about a field-wide practice absent from the corpus | Return `Insufficient evidence`; offer clearly labelled domain-general guidance if useful. |
| Required factual context is missing | Do not invent it. Complete any safe useful revision, identify the unresolved point, and ask a focused question only if the requested revision cannot meaningfully proceed. |
