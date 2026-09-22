# Regression cases and scoring rubric

Run the applicable cases mentally before delivering an analysis or revision. These are behavioral invariants, not string-matching tests.

| ID | Input condition | Passing behavior |
| --- | --- | --- |
| R01 | A clear, grammatical sentence with suitable scope | Return `Keep` rather than manufacture an edit. |
| R02 | Ordinary clear verb such as `use` or `show` | Do not upgrade vocabulary without a stated semantic reason. |
| R03 | One paper contains a phrase | Describe a source-local observation; do not call it a field convention. |
| R04 | Empirical evidence is described with `prove` | Do not silently strengthen or validate the claim; flag or calibrate it without inventing facts. |
| R05 | A distinctive source sentence is relevant | Transfer function or structure only; produce independent user-specific wording. |
| R06 | A paragraph problem is present | Diagnose organization or rhetorical role, not merely grammar. |
| R07 | An abstract or fragment is supplied | Do not infer absent paragraphs, sections, or paper-level argument flow. |
| R08 | References disagree | State the conflict and context; do not fabricate consensus or use raw frequency over clarity. |
| R09 | The user demands minimal change | Use LOW budget; separate any high-budget alternative. |
| R10 | A recommendation relies on general knowledge | Label it `Domain-general`, not `Reference-evidenced`. |
| R11 | A source has frequent but awkward filler | Record it as non-transferable when warranted; frequency is not quality. |
| R12 | The user asks a field-wide question with insufficient corpus | Return `Insufficient evidence` and identify what would be needed. |

## Score each completed task

Score `0` (fails), `1` (partly meets), or `2` (meets) on applicable dimensions:

| Dimension | A score of 2 means |
| --- | --- |
| Meaning preservation | No scientific proposition, scope, qualifier, comparison, or terminology was altered without authorization. |
| Reader clarity | The result makes the intended local role and relationships easier to follow. |
| Reference integrity | Each reference-derived claim is traceable to supplied material and is not overgeneralized. |
| Voice preservation | The revision retains acceptable user wording and conforms to the revision budget. |
| Transfer integrity | No distinctive sentence imitation; any transfer is contextual and level-appropriate. |
| Uncertainty calibration | Confidence and limitations match the actual corpus and interpretation. |
| Edit necessity | Every substantive edit has a concrete reason; `Keep` is used when appropriate. |

Do not report a numerical total to the user unless they ask for an audit score. Any `0` in meaning preservation, reference integrity, or transfer integrity requires correction before delivery.
