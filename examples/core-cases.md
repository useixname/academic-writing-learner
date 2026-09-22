# Core cases

These examples illustrate decisions, not required wording. Adapt to the user's meaning and revision budget.

## 1. Keep an already adequate sentence

**User text:** “The model uses previous examples to improve performance.”

**Outcome:** Keep.

**Reason:** The sentence is clear and appropriately scoped. There is no demonstrated correctness, clarity, naturalness, or reference-fit problem requiring a rewrite. `Evidence source: User-evidenced; confidence: High.`

## 2. Avoid an empty vocabulary upgrade

**User text:** “Our method uses an adaptive sampler.”

**Outcome:** Keep `uses`; do not automatically substitute `utilizes`.

**Reason:** The longer verb adds no technical distinction. `Evidence source: Domain-general; confidence: High.`

## 3. Calibrate an unsupported strong claim

**User text:** “Our experiments prove that the approach is robust.”

**Outcome:** Flag “prove” unless the user has established a formal proof. A possible factual-preserving alternative is “Our experiments show that the approach performs robustly under [specified conditions],” but only if those conditions are supplied.

**Reason:** Empirical results normally support an empirical observation, not proof. `Evidence source: Domain-general + User-evidenced; confidence: Medium.`

## 4. Transfer a rhetorical move, not a sentence

**References:** Three supplied introductions first acknowledge recent progress, then state a remaining limitation.

**User need:** Introduce a genuine unresolved limitation after summarizing related work.

**Outcome:** Recommend the conceptual move “acknowledge relevant progress, then specify the remaining limitation and its consequence.” Draft new language from the user's facts; do not adapt a reference sentence by swapping nouns.

**Evidence:** “3 of 3 comparable supplied introductions.” `Evidence source: Reference-evidenced; confidence: High.`

## 5. Do not generalize a single source

**Reference observation:** One paper repeatedly writes “It is worth noting that”.

**Outcome:** “This phrase recurs in this paper, but the supplied corpus is insufficient to treat it as a field convention. It may be an author habit; I would not recommend transferring it without a communicative need.”

`Evidence source: Reference-evidenced; confidence: Low for a general convention.`

## 6. Respect the requested budget

**User request:** “Polish this, but keep my voice and sentence order.”

**Outcome:** Set LOW budget. Correct clear grammar and local awkwardness only; offer a reorganized version separately, labelled as exceeding the requested budget, if paragraph order truly blocks comprehension.

## 7. Refuse unsupported paragraph inference

**Input:** A paper abstract only.

**Outcome:** Analyze word, phrase, sentence, and abstract-level rhetorical choices. State that paragraph- and section-level strategy cannot be inferred from an abstract alone.
