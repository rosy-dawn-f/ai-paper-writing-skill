# Whole-Paper Review

Use this reference for adversarial, reviewer-style self-review before submission or before major revision.

## Goal

Detect rejection risks and assess whether central claims are clear, defensible, and supported. Follow the requested audit or revision scope; unresolved research questions need not prevent delivery of a completed review.

## Critical Rule

Every major claim, especially in the Abstract, Introduction, and Conclusion, must be technically correct and explicitly supported by evidence. If not, add evidence, weaken the claim, move the claim to future work, or remove it.

## What Usually Gets A Paper Accepted

Check whether the paper has at least one strong acceptance path:

- Sufficient contribution: new task, new pipeline, new module, new design principle, new experimental finding, new dataset/metric, or new insight.
- Better empirical performance than prior methods under fair comparisons.
- Sufficient comparison experiments and ablation studies.
- Clear writing that lets reviewers understand the contribution quickly.
- Method design that is technically reasonable and reproducible.

## Common Rejection Dimensions

| Dimension | Typical failure signals |
| --- | --- |
| Insufficient contribution | Failure case is too common or trivial; technique is well explored; gains are predictable; novelty is hard to state. |
| Unclear writing | Missing technical details; method cannot be reproduced; module motivation is vague; paper story changes across sections. |
| Weak empirical effect | Improvement is marginal; absolute performance is not competitive; gains are inconsistent across settings. |
| Incomplete evaluation | Missing ablations, baselines, metrics, datasets, robustness tests, or failure cases needed for the claims. |
| Problematic method design | Setting is unrealistic; method has technical flaws; requires per-scenario tuning; added complexity creates more limitation than benefit. |
| Trust and fairness risk | Compute, seeds, data exposure, baseline tuning, or evaluation protocol is unfair or underreported. |

## Five-Dimension Self-Review

### 1. Contribution

- What new knowledge does the paper give to readers?
- Is the target failure case meaningful rather than trivial?
- Is the technical idea non-obvious beyond standard practice?
- Is the gain surprising, insightful, or practically meaningful?
- Is the novelty type explicit: task, pipeline, module, metric, dataset, finding, or insight?

### 2. Writing Clarity

- Can a knowledgeable reader reproduce the method from the paper?
- Does each key module have enough technical detail?
- Is every module motivated by a concrete challenge?
- Are terms, symbols, and notation consistent across sections?
- Does each paragraph carry one clear message?

When language coverage is requested or wording appears to change scientific meaning, read `readability-review.md`. Audit semantic commitment as well as grammar. Consolidate one finding when the same passage raises overlapping language, evidence, and clarity concerns.

### 3. Experimental Strength

- Are improvements over strong baselines meaningful?
- Is absolute performance competitive for the target venue?
- Are gains consistent across datasets, settings, and metrics?
- Are strengths and failure cases reported honestly?
- Are ablations strong enough to support causal claims?

### 4. Evaluation Completeness

- Are all strong and recent baselines included?
- Are evaluation metrics standard and sufficient?
- Are datasets/scenarios challenging enough?
- Is each contribution validated by at least one experiment?
- Are protocols documented well enough to reproduce?

### 5. Method Design Soundness

- Is the experimental setting realistic?
- Does the method rely on unreasonable assumptions?
- Is the method robust without heavy per-case hyperparameter retuning?
- Do benefits outweigh added complexity?
- Could reviewers argue that the net contribution is negative?

## Adversarial Writing Workflow

1. Read as a skeptical reviewer within the requested scope.
2. Answer applicable questions with explicit evidence; distinguish unavailable evidence from a demonstrated defect.
3. Classify findings as supported, context-dependent, or unverified. Mark relevant work as `pass`, `needs revision`, or `needs new experiment`; skip inapplicable items.
4. Make only requested revisions. For an audit, report findings without automatically producing replacement prose or changing files.
5. Recheck changes and affected claims. Finish once scoped work is complete; list unresolved needs for sources, experiments, or author decisions. Repeat only when new changes or findings justify another pass.

Briefly identify reviewed sections/layers and unverified matters. Use a coverage table only when scale warrants it. Do not imply that a language review validated experiments or that a wording edit supplied missing evidence.

## Rejection Recovery

Use only for rejection or major-revision work. Cluster concerns into contribution, validity, evidence, presentation, and venue fit. Distinguish writing repairs from new experiments, claim repositioning, or artifact improvements; address the underlying concern before cosmetic resubmission. Consider a different venue or project direction only when the evidence warrants it. Rejection alone does not invalidate the project.

## Output Pattern

Return:

1. `Blocking risks`: issues likely to cause rejection or desk rejection.
2. `Major risks`: issues likely to lower scores.
3. `Claim-evidence map`: major claims with support status.
4. `Five-dimension self-review`: pass/needs revision/needs experiment.
5. `Revision plan`: ordered fixes, separating writing fixes from experiment fixes.
6. `Reviewer questions`: likely questions and how to answer them.
