# Readability And Review Readiness

Use this reference when polishing manuscript text, captions, figures/tables, submission checks, common reviewer criticisms, rebuttal prep, or post-rejection revision.

## Readability Axes

Diagnose prose through four axes:

- Logical strength: the reasoning itself is coherent; connectives only reflect real logic.
- Defensibility: claims are supported by references, facts, experiments, or appropriately cautious wording.
- Confusion time: readers spend little time wondering what a concept, pronoun, symbol, component, or result means.
- Information density: text and visuals deliver useful information without familiar filler or buried conclusions.

## Logical Strength

Do not use connectives to fake logic. Check whether phrases like "therefore", "to this end", "accordingly", "first", "moreover", and "last but not least" actually match the relationship between clauses or items.

Prefer direct structure:

- State the problem.
- State the design choice.
- State the evidence.
- State the conclusion.

If modules are unordered, introduce them as components rather than pretending they form a ranked sequence.

## Defensibility

Review every strong statement as if a skeptical reviewer is asking "How do you know?"

Common repairs:

- Add citations for claims about field pain points, known limitations, or practical consequences.
- Add direct experiment references for causal explanations.
- Use cautious language for indirect evidence.
- Replace broad claims such as "solves", "proves", "significantly", or "universal" when evidence is narrower.
- Avoid demeaning prior work; contrast scope, assumptions, data, objective, or empirical behavior.

## Confusion Time

Reduce "what is this?" moments:

- Define a concept near first mention.
- Explain a named component by its function or implementation immediately.
- Break long sentences when relative pronouns or nested clauses create ambiguity.
- Use topic sentences near the start of paragraphs.
- Keep notation, symbols, abbreviations, and capitalization consistent.

## Information Density

Get to the point quickly, especially at section starts. Avoid retelling common field history unless it directly motivates the gap.

For figures and tables:

- Make captions state the question and key conclusion, not just describe the plot.
- Explain abbreviations and unusual settings in or near the visual.
- Put the sentence analyzing an important result close to the figure/table reference.
- Design tables around the comparison the reader should make, even if that repeats a baseline.
- Move long hyperparameter detail to appendix unless it is essential to a claim.

## Detail Checklist

Use this after major story issues are fixed:

- Ensure figures and tables together tell the complete story.
- Check symbol, abbreviation, capitalization, citation, and reference consistency.
- Verify all figures/tables are mentioned in order.
- Increase figure text and legend size if readability is marginal.
- Improve table scanning with grouping, bolding, removal of redundancy, and clear baselines.
- Place important information in prominent positions.
- Add appendix/code details that improve reproducibility.

## Last-Hours Submission Checklist

Prioritize desk-reject risks first:

- Correct page count and formatting.
- Anonymous submission compliance, including acknowledgments, code, demos, metadata, and supplementary materials.
- No missing figures, formulas, tables, captions, or references.
- No LaTeX placeholders, question marks, broken references, or compilation artifacts.
- All numbers copied correctly from final experiments.
- Figures are vectorized or high enough resolution.
- Captions are grammatical and punctuated consistently.
- Section title capitalization is consistent.

## Common Negative Reviews And Repairs

- Unprofessional presentation: missing key references, messy structure, omitted required supplements, or setup mismatch. Repair with recent reference coverage, aligned configuration, and complete submission materials.
- Validity questioned: implausible numbers, overclaiming, flawed setup, or weak argumentation. Repair with more experiments, clearer scope, and rigorous wording.
- Prior work not respected: missing latest work, weak baselines, unfair comparison, or dismissive framing. Repair with updated comparisons and evidence-based contrast.
- Lack of novelty: unclear story, incremental design, or known knowledge. Repair by sharpening the core contribution and emphasizing the strongest supported insight.
- Poor presentation: grammar, missing details, hard-to-follow writing. Repair through focused rewriting, topic sentences, definitions, and better visuals.
- Disagreement with approach: reviewer doubts the route or experimental design. Repair with additional evidence, precedent from relevant literature, and precise limitation statements.

## Rejection Recovery

Treat rejection as diagnostic data, not a verdict on the project. Cluster reviews by underlying concern, then decide whether to:

- repair writing/story only,
- add decisive experiments,
- reposition the claim,
- target a more suitable venue,
- release or improve code/data/supplement,
- abandon only if the core claim cannot be defended.

Do not simply resubmit with cosmetic changes when reviewers identified validity, fairness, or novelty problems.
