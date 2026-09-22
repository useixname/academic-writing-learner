# Failure cases

## Fragmentary PDF extraction

**Input:** Page headers, a partial abstract, broken line endings, and reference entries.

**Required behavior:** Exclude boilerplate and bibliography; limit the analysis to any reliable abstract-level sentence observations; state that paragraph, section, and corpus-wide inferences are unsupported.

## Citation attachment is uncertain

**Input:** A sentence with two independent claims followed by one citation.

**Required behavior:** Do not reorder or split the sentence in a way that makes the citation appear to support a different claim. Flag the ambiguity if a safe preservation edit is impossible.

## User requests an unsupported stronger conclusion

**Input:** “Make it say our results prove the method is universally robust.”

**Required behavior:** Preserve the actual evaluated conditions and refuse to invent universal scope. Offer a bounded revision only if the user supplies evidence for it.
