# Source ingestion

Use before learning, comparing, counting, or attributing a writing pattern to a paper. The objective is to define what was actually read—not to reconstruct missing text.

## 1. Register each source

For every supplied PDF, LaTeX project, HTML page, plain-text extract, or copied passage, record: source label; available format; whether extraction is complete or damaged; paper and section identity when known; and the user's intended learning task. Treat availability as a property of the supplied material, not a claim that the whole paper was read.

## 2. Build a section-aware learning corpus

Include by default prose that can carry academic-writing decisions:

| Include | Conditions |
| --- | --- |
| Abstract, introduction, related work, method, experiments, results, discussion, limitations, conclusion | Preserve their section labels where available. |
| Prose around equations, figures, tables, and citations | Include the explanatory sentences, not equation syntax or reference metadata as ordinary prose. |
| Figure/table captions | Include only when the task concerns captions, result reporting, visual explanation, or their local rhetorical function. |
| Appendices and supplementary prose | Include only if the user requests it or it matches the target writing task. |

Exclude by default from language counts and transferable-pattern inference:

```text
reference lists and bibliography entries
author names, affiliations, acknowledgements, page headers/footers
copyright, license, publisher, submission, or template boilerplate
citation metadata and DOI strings
equation-only text, isolated table cells, axes, legends, and algorithm tokens
broken OCR, hyphenation artifacts, repeated PDF navigation text, and garbled characters
```

An excluded item may still be inspected for a narrow user-requested task, but must not silently enter a general corpus statistic.

## 3. Preserve location and extraction quality

Keep source anchors such as filename, section, page, paragraph, or supplied excerpt label. Mark text as `clean`, `partially extracted`, `OCR-uncertain`, or `fragmentary`. Do not normalize away uncertainty that affects an observed word, punctuation, equation, or citation.

## 4. Create analysis units

Segment usable material into paper → section → paragraph → sentence. Associate each unit with its section, source anchor, and text-quality label. Never treat a clipped line, a table cell, or a list of references as a sentence in a writing-style analysis.

## 5. Stop safely

If no reliable prose remains after exclusion, report `Insufficient evidence to learn writing patterns from this source.` If the source supports only one level of analysis, constrain conclusions to that level. Do not infer a paper's argument flow from headings, an abstract, or scattered snippets.
