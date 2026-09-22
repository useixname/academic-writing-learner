# Application cases

## Preserve terminology and LaTeX

**Input:** `As shown in Table~\ref{tab:main}, \textsc{MemAgent} improves $F_1$ by 3.2\% over \textsc{Baseline}~\cite{smith2025}.`

**Revision need:** The prose is already direct and grammatical.

**Outcome:** Keep. Do not replace the cross-reference with “the table,” rename either method, turn `$F_1$` into prose, change `3.2\%`, or move the citation.

**Reason:** The wording needs no edit; all markup, terminology, quantity, comparison, and citation attachment are protected.

## Preserve user language over a fashionable alternative

**User profile:** The manuscript naturally and consistently uses `use`, `show`, and `improve`.

**Draft:** “Our method uses a memory buffer to improve accuracy.”

**Reference profile:** A few sources use `leverage`.

**Outcome:** Keep the user's verbs unless a genuine distinction is required. The source observation does not justify a vocabulary shift.

## Repair syntactic inflation without content drift

**Draft:** “The utilization of episodic memory enables the improvement of reasoning performance under few-shot settings.”

**LOW/MEDIUM revision:** “Using episodic memory improves reasoning performance in few-shot settings.”

**Checks:** `episodic memory`, `reasoning performance`, and `few-shot settings` remain unchanged. The edit restores a direct verb; it does not claim statistical significance or alter the condition.
