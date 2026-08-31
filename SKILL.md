---
name: ai-paper-writing
description: Coach AI conference paper writing, section drafting, revision, reviewer-readiness, and final submission cleanup using guidance distilled from hzwer/WritingAIPaper, Master-cai/Research-Paper-Writing-Skills, and MLNLP-World/Paper-Writing-Tips. Use when Codex is asked to draft, diagnose, polish, restructure, review, or prepare AI/ML/CV/NLP conference manuscripts, abstracts, introductions, related work, methods, experiments, conclusions, contribution statements, paragraph flow, claim-evidence alignment, rebuttal preparation, LaTeX/figure/table/formula/citation checks, submission checklists, or research-integrity checks for deceptive or unfair experimental practices.
---

# AI Paper Writing

## Overview

Use this skill to help authors make AI conference papers clearer, more defensible, and easier for reviewers to trust. Treat writing as reviewer-facing engineering: identify the core contribution, build a self-contained story at multiple levels, draft each section with a clear role, reduce confusion time, and check claims against evidence. Prioritize writing quality and reviewer effectiveness over minimizing context; load detailed section guides and examples whenever they would improve the manuscript.

Source basis: distilled and paraphrased from [hzwer/WritingAIPaper](https://github.com/hzwer/WritingAIPaper), [Master-cai/Research-Paper-Writing-Skills](https://github.com/Master-cai/Research-Paper-Writing-Skills), and final-submission checklist guidance from [MLNLP-World/Paper-Writing-Tips](https://github.com/MLNLP-World/Paper-Writing-Tips). Do not reproduce long passages from the sources; use the bundled references as working guidance.

## Quick Workflow

1. Identify the user's artifact and stage: idea framing, outline, abstract, introduction, related work, method, experiments, full draft, rebuttal, or pre-submission check.
2. Ask for missing manuscript context only if needed: target venue, page limit, contribution claims, main baselines, key results, and reviewer concerns.
3. Clarify the paper story before sentence-level edits. If drafting or rewriting a section, build a compact mini-outline first.
4. When an older or alternative draft is available, compare reverse outlines before choosing prose. Preserve a stronger causal structure when warranted, but revalidate every name, mechanism, claim, and result instead of copying stale content.
5. Determine whether the work is one contribution chain, several necessary threads that converge on one paper-level capability, or several sibling papers that share an umbrella topic. Do not equate narrative compression with deleting substantive work. When multiple work packages must be preserved or related manuscripts must be differentiated, read `references/multi-thread-narrative.md` before choosing the story.
6. Build a gap-driven narrative funnel: move from the broad task to the target capability, progressively narrow to the specific unmet requirement and root cause, then introduce the contribution and evidence. Use the fewest gap branches justified by the work; keep one chain by default and branch only when distinct contributions genuinely answer distinct gaps.
7. Before writing any claim about what prior work typically does, cannot do, or has not studied, inspect the closest available sources and build a compact evidence ledger. Read `references/literature-positioning.md` when a local literature corpus, PDFs, or prior-work novelty claim is in scope.
8. Diagnose the paper around four axes:
   - Core contribution: insight, performance, or new capability.
   - Story structure: abstract, introduction, and body each tell a complete version of the contribution.
   - Readability: logical strength, defensibility, confusion time, and information density.
   - Trustworthiness: fair comparisons, transparent training, complete reporting, and no cherry-picking.
9. For section writing, keep each paragraph to one message, state the paragraph role, and verify sentence-to-sentence flow.
10. Check every major claim in the abstract, introduction, and conclusion against experimental evidence.
11. When drafting or substantially rewriting a section, load the matching example bank entry after the section guide and choose a concrete writing pattern.
12. Produce actionable edits, not generic advice. Prefer rewritten paragraphs, replacement outlines, reviewer-risk tables, checklists, claim-evidence maps, or exact experiment gaps.
13. Separate must-fix risks from polish. Lead with issues that could cause rejection, desk rejection, or loss of reviewer trust.

## Task Routing

- For ideation, outline, contribution statements, high-level story, or experiment-story alignment, read `references/paper-architecture.md`.
- For several substantive work packages, multi-stage systems, tightly interleaved contribution lines, prediction-to-decision or other upstream-to-downstream pipelines, sibling manuscripts with overlapping umbrella topics, or title differentiation between related papers, read `references/multi-thread-narrative.md`.
- For novelty positioning, literature-gap claims, contribution wording, terminology choices, or a user-provided literature corpus, read `references/literature-positioning.md` before drafting the relevant prose.
- For abstract drafting or rewriting, read `references/section-abstract.md`; when writing actual prose, also read `references/examples/abstract/index.md` and the matching template.
- For introduction drafting or rewriting, read `references/section-introduction.md`; also read `references/paper-architecture.md` when the core contribution or gap-driven narrowing is unclear, and add `references/multi-thread-narrative.md` when necessary work lines must branch and reconverge, an older draft demonstrates a stronger interleaving pattern, or a related manuscript must remain visibly distinct. For actual prose, read `references/examples/introduction/index.md` and the matching opening/challenge/pipeline pattern.
- For related work, read `references/section-related-work.md`.
- For method section writing, pipeline explanation, module motivation, or technical advantage, read `references/section-method.md`; add `references/multi-thread-narrative.md` when module outputs cross stage, scale, representation, or decision boundaries. When writing actual prose, also read `references/examples/method/index.md` and the matching template.
- For experiment planning, results writing, ablations, figure/table communication, or evaluation completeness, read `references/section-experiments.md`; add `references/multi-thread-narrative.md` when the evidence must establish an upstream artifact, its downstream usefulness, and the final system capability without reverting to module-by-module silos. Add `references/integrity-risks.md` when fairness or reproducibility is in question.
- For conclusion, limitations, impact, or future work, read `references/section-conclusion.md`.
- For paragraph flow, reverse outlining, topic sentences, or "does this paragraph make sense?", read `references/paragraph-flow.md` and optionally `references/readability-review.md`.
- For whole-paper reviewer simulation, claim-evidence alignment, or self-review before submission, read `references/paper-review.md`.
- For polishing, figure/table captions, reviewer-facing readability, common negative reviews, or rejection recovery, read `references/readability-review.md`.
- For claims about fair comparison, baseline setup, hyperparameters, compute, evaluation, seeds, data leakage, or suspicious result reporting, read `references/integrity-risks.md`.
- For final submission, camera-ready cleanup, LaTeX, notation, formulas, figures, tables, citations, bibliography, anonymity, supplement/code privacy, deadline-day checks, or "the day before submission", read `references/final-submission-checklist.md`.

Do not load all section references at once. Load the section guide needed for the current edit target, then add the relevant example template if drafting or rewriting prose, and add risk/checklist references only if the task calls for them.

## Review Heuristics

Frame the paper as a promise to reviewers:

- What should readers remember after one minute?
- Which prior methods define the competition?
- Which result directly supports each contribution claim?
- Where could a skeptical reviewer say "unsupported", "unfair", "incremental", "unclear", or "irreproducible"?
- Which details must be moved into the main paper, appendix, caption, or code release for trust?

When reviewing text, annotate issues with severity:

- `Blocking`: likely desk rejection, reviewer distrust, invalid comparison, unsupported central claim, anonymity/page-limit problem, or missing decisive evidence.
- `Major`: hurts novelty, story, defensibility, or reproducibility but can be fixed in revision.
- `Minor`: grammar, flow, style, local clarity, caption polish, or consistency.

## Output Patterns

Choose the format that best fits the user's artifact:

- Manuscript diagnosis: `Top risks`, `Story repair`, `Experiment gaps`, `Line-level edits`.
- Section draft or rewrite: compact section outline, revised paragraphs with paragraph roles, short self-review checklist, and claim-evidence map for major claims.
- Template-driven section writing: name the selected template, explain why it fits, then produce the revised prose.
- Paragraph flow check: one-sentence diagnosis, reverse outline, flow breaks, and a revised paragraph.
- Introduction help: territory, niche, occupancy, a gap-driven funnel with only the necessary branches, contribution bullets, and a page-one-figure suggestion if useful.
- Multi-thread or sibling-paper help: a paper-level capability statement, thread-role map, interface-alignment audit, convergence test, sibling-paper identity matrix when applicable, and an evidence-backed title/story boundary.
- Literature-positioning audit: source-backed terminology, an evidence ledger for direct competitors, calibrated gap language, and any claims that require a broader search.
- Related work help: topic clusters, relationship to this paper, missing citations to check, and non-dismissive contrast language.
- Pre-submission: desk-reject checks first, then anonymity and artifact privacy, then LaTeX/figure/table/formula/citation consistency, then reproducibility.
- Rebuttal prep: reviewer concern, factual answer, extra evidence, wording boundary, and what to promise only if already done.

When producing a claim-evidence map, use:

`Claim: ... | Evidence: ... | Status: supported / needs evidence / overclaimed`

## Guardrails

- Preserve scientific honesty. Never suggest hiding compute, seeds, baselines, failed datasets, hyperparameters, data leakage, test-set tuning, or model size.
- Prefer defensible claims over stronger-sounding claims. Use "may", "suggests", or "is consistent with" when evidence is indirect.
- If a claim cannot be supported by results, weaken, relocate, or remove it instead of improving the rhetoric around it.
- Do not invent citations, scores, venues, deadlines, acceptance rates, or reviewer comments. Browse or ask when current or paper-specific facts matter.
- Do not generalize from one or a few papers into claims about an entire field. State the review boundary (for example, "among the reviewed studies") unless the search is demonstrably comprehensive.
- Do not create a strawman gap. Acknowledge a prior method's demonstrated capability before contrasting the distinct capability, mechanism, assumption, action space, or evaluation setting addressed by the present work.
- Use terminology evidenced in the target literature. Reserve terms such as "formulation" for a defined mathematical or decision problem; otherwise prefer the nouns used by the field, such as method, approach, strategy, scheme, or controller.
- In a journal article or short paper, refer to the manuscript and its contributions as "this paper" by default. Use "this study" only when referring specifically to an empirical investigation or when the target venue's established style requires it; do not alternate the two without a reason.
- A contribution that only relabels a problem is weak. Present a framework contribution only when it introduces an operational construction, a distinct capability, and a planned evidence path.
- Do not preserve workload by promoting routine implementation steps into artificial contribution lines. A durable thread needs a causal necessity, a distinct output or role, an evidence path, and a truthful relationship to the paper-level capability.
- Do not differentiate sibling papers only through model names, datasets, or fashionable umbrella wording. Their research questions, operational semantics, action or output roles, and decisive evidence must establish a defensible boundary; otherwise flag overlap instead of manufacturing novelty.
- Respect the target venue's official rules. Page limits, anonymity, checklist requirements, and deadlines must be verified from official sources when relevant.
- For Chinese drafts, preserve the author's intended technical meaning while producing publication-quality English when asked.
