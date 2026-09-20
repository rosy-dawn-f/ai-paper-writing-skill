# Experiments Section Guide

Use this reference when planning experiments, rewriting results, checking ablations, or improving figure/table communication.

## Goal

Convince reviewers that the contribution is effective, causal, fair, and useful in realistic settings.

## Core Questions

The experiments section should answer:

- Effectiveness: Is the method better than strong and recent baselines?
- Causality: Which modules or design choices cause the gain?
- Generalization: Does the method work beyond the easiest or most favorable setting?
- Practical value: What are the costs, tradeoffs, and deployment constraints?
- Scope: Where does the method fail or become less reliable?
- Integration: When several threads are claimed to work together, is the interface useful and does the integrated system exhibit the intended behavior?

## Planning From Claims

Map each contribution to evidence:

`Contribution -> claim -> required experiment -> table/figure -> result sentence`

For a multi-thread manuscript, also map:

`Thread output or role -> downstream requirement -> available evidence -> supported conclusion`

Typical evidence types:

- Main benchmark comparison.
- Ablation by removing, replacing, or disabling a component.
- Sensitivity analysis for key hyperparameters.
- Robustness or out-of-distribution evaluation.
- Efficiency, latency, memory, FLOPs, or training cost analysis.
- Qualitative visualization with clear selection criteria.
- Failure cases and limitations.

## Recommended Experiment Package

For a standard AI conference paper, check whether the paper needs:

1. Main comparison table against strong recent baselines.
2. Ablation table for every central module or design choice.
3. Module interaction ablation when components depend on each other.
4. Sensitivity analysis for important hyperparameters or thresholds.
5. Robustness or OOD tests for the claimed deployment setting.
6. Efficiency table if the method changes model size, compute, memory, latency, or training cost.
7. Qualitative figures that explain failure/success modes, not only best-looking cases.
8. Failure cases and limitation analysis.

Not every paper needs every item, but every contribution needs evidence.

## Cross-Thread Research-Question Ladder

When a paper combines an upstream representation, predictor, calibrated environment, data construction, or other enabling thread with a downstream decision or generation method, organize the argument around questions rather than mirroring the method directory:

1. Is the upstream artifact or validity foundation credible for its claimed role?
2. Is the cross-thread interface aligned and informative for the downstream task?
3. Does integration change the intended downstream behavior or mechanism?
4. Does the resulting system improve the paper-level outcome within the tested scope?

Use only the questions implied by the claims and evidence. A single result may answer more than one question; several module ablations may answer one question together. If the experiment inventory is fixed, reuse existing results where they genuinely answer these questions, weaken unsupported synergy claims, and record evaluation limits. Do not invent experiments or imply that an upstream gain caused a downstream gain without integrated evidence.

## Experimental Setup

Make comparisons reproducible:

- State datasets, splits, metrics, preprocessing, training budget, hardware when relevant, and evaluation protocol.
- Name baselines and implementation sources.
- Explain deviations from prior protocols.
- Report comparable tuning budgets when possible.
- Report mean/std or multiple seeds when randomness affects conclusions.
- Use `integrity-risks.md` if compute, seeds, data leakage, private tests, or baseline fairness may be questioned.

## Experiment Section Decomposition

Typical order:

1. Experimental setup: datasets, metrics, implementation, baselines.
2. Main results: answer whether the method works.
3. Ablations: answer why it works.
4. Analysis: robustness, sensitivity, efficiency, qualitative findings.
5. Limitations or failure cases.

For tightly interleaved work, a question-led order may be clearer:

1. Setup and evidence scope.
2. Credibility of enabling artifacts or foundations.
3. Interface usefulness and cross-thread interaction.
4. Downstream behavior and system-level outcomes.
5. Boundary conditions and limitations.

Do not use this order mechanically; choose the smallest structure that tests the paper's actual claims.

## Writing Results

For each result paragraph:

1. State the question being tested.
2. Identify the setting, comparator, and metric.
3. Report the direction and magnitude of the main result.
4. Interpret what it supports.
5. State boundaries if the result is narrow.

Use neighboring setup text and referenced tables where they already supply this information; do not repeat all fields in every sentence. Check percentage denominators, units, and whether a change is relative or in percentage points. Verify calculations against supplied data; when values or comparison bases are missing, identify the gap without fabricating them. A number alone does not justify generalization or causality; ablation or analysis must support the claimed inference.

Result paragraph skeleton:

`Table X evaluates [question] on [dataset/setting]. Compared with [strong baseline], our method [result]. This supports [claim] because [technical interpretation]. However, [boundary/failure/tradeoff] indicates that [scope].`

## Figure/Table Writing Rules

Tables and figures are part of the argument, not decoration.

A reference locates a visual; prose explains its relevant contents and role. For results, identify the key comparison or trend and the supported inference. For method diagrams, explain components and their relationships. Match labels with the text. Analyze what matters without repeating the caption or transcribing every value. If a visual is unavailable, distinguish a wording audit from verification of its contents.

Hard table rules:

- Put table captions above tables when the venue style allows or requires it.
- Prefer booktabs-style tables with minimal horizontal rules.
- Avoid vertical rules and dense line stacks.
- Mark metric direction in headers, such as `Accuracy ↑` or `LPIPS ↓`.
- Keep decimal precision consistent within each metric.
- Group multi-dataset or multi-setting results with clear headers.
- Use restrained highlighting for best and second-best values.

Caption rules:

- State the question, setting, key comparison, and main takeaway.
- Explain abbreviations and special settings.
- Do not use the caption as a long discussion section.
- Make the visual understandable when skimmed independently.

## Experimental Rigor Checklist

- Are baselines recent, relevant, and fairly configured?
- Are metrics standard and sufficient for the task?
- Is every abstract/introduction claim supported by a result?
- Are all important modules ablated?
- Are datasets and scenarios challenging enough?
- Are limitations of evaluation scope explicit?
- Are unfavorable results disclosed when they affect the claim?
- Does every claimed thread convergence have joint or interface-level evidence, rather than only separate module metrics?
- Are compute, training budget, and implementation choices transparent?

## Output Pattern

Return:

1. Claim-evidence experiment map.
2. Missing experiment or ablation list.
3. Revised experiment-section outline, organized by research question when that better exposes cross-thread evidence.
4. Result paragraph rewrites.
5. Figure/table communication fixes.
6. Fairness or reproducibility risks.
7. Unsupported interface or synergy claims that must be weakened when no additional experiments are available.
