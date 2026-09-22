# Learning protocol

Use this protocol in **LEARN** and any **APPLY** request that needs new reference extraction. First apply [source ingestion](source-ingestion.md) to establish usable text, then use [rhetorical functions](rhetorical-functions.md) for stable labels. Scale the depth to the material: do not force paper-level analysis from a short extract.

## 0. Establish the evidence boundary

Record for each source: identifier supplied by the user; available material and missing sections; paper type; venue/status if actually supplied or verifiable; relevant field and writing task; and any evident extraction defects. Assign a provisional corpus role:

| Role | Appropriate use |
| --- | --- |
| **High-confidence reference** | Relevant, sufficiently complete, and consistently clear material; eligible for positive transferable patterns. |
| **Medium-confidence reference** | Useful but narrower, incomplete, mixed-quality, or less task-aligned; use with qualification. |
| **Context-only reference** | Gives terminology or background, but not a basis for general style claims. |

Do not infer quality from prestige alone. Do not invent venue or publication facts. A corpus role is an assessment of usefulness for the current writing task, not an evaluation of the research.

## 1. Segment only what exists

Identify paper, section, paragraph, and sentence boundaries where possible. Mark the local section role (for example, introduction, related work, method, result, limitation, discussion, conclusion) and whether the text is complete enough for paragraph-, section-, or paper-level inference.

## 2. Recover scientific and rhetorical intent

For each useful unit, record the factual content separately from its rhetorical function. Typical functions include establishing importance, defining a problem, acknowledging progress, locating a gap, stating a limitation, introducing a method, reporting evidence, qualifying a claim, interpreting a result, and delimiting scope. Do not mistake a frequent word for a rhetorical strategy.

## 3. Select decisions worth learning

Examine only choices that pass all relevant checks:

1. It is a real writing or information-organization decision, not merely domain content.
2. Its local function is identifiable.
3. It improves clarity, precision, economy, reader guidance, or calibrated claim strength.
4. It is transferable beyond the named study without copying a distinctive expression.
5. Its source and context can be cited in the learning record.

Ignore uninformative wording and isolated style trivia. Classify selected candidates as `Positive`, `Neutral`, `Author-specific`, `Overused`, or `Avoid`. “Frequent” alone never means “Positive.”

## 4. Abstract a reusable pattern

For each candidate, produce a compact record:

```text
Pattern: [functional or structural description, not a copied sentence]
Level: word | phrase | sentence | paragraph | section | paper-argument
Local role: [rhetorical function]
Observed evidence: [paper/section/count or examples]
Appropriate when: [necessary factual and rhetorical conditions]
Avoid when: [conditions that make it misleading or formulaic]
Transfer level: conceptual | structural | lexical
Classification: Positive | Neutral | Author-specific | Overused | Avoid
Evidence source: Reference-evidenced | ...
Confidence: High | Medium | Low
```

At the section and paper-argument levels, record the sequence of functions rather than forcing the source's exact headings or sentence order. For example, an introduction may move from importance to progress to an unresolved limitation to the work's response, but must not be presumed to do so if the actual text does not.

## 5. Consolidate across sources

Group genuinely comparable patterns by same writing task and section. Report counts with their denominator and the scope, such as “3 of 4 supplied introductions use an explicit limitation after prior progress.” Treat patterns as competing only if they serve the same local function.

Use the following confidence labels:

| Confidence | Minimum basis |
| --- | --- |
| **High** | Consistent observation across multiple relevant papers or multiple comparable sections, with no material counter-pattern. |
| **Medium** | Repeated in one strong relevant paper or in a small/mixed corpus; useful but not a stable convention claim. |
| **Low** | One observation, fragmentary material, ambiguous function, or mainly interpretive inference. |

## 6. Produce a reusable learning record, guidance, and limits

Create the internal record using [learning-record schema](learning-record-schema.md). State the most transferable lessons, what not to learn, each lesson's appropriate conditions, evidence basis, confidence, and corpus limitations. Preserve negative learning as a first-class result: a single idiosyncratic construction, repeated filler, or low-quality expression can be explicitly recorded as not recommended for transfer.
