# Abstract Section Guide

Use this reference when drafting, rewriting, or checking an AI/ML/CV/NLP paper abstract.

## Goal

Make the abstract a complete miniature paper: task, gap or challenge, core idea, method essence, strongest evidence, and value. Keep it readable for a reviewer who has not yet accepted the paper's premise.

## Pre-Writing Questions

Answer before drafting:

- What exact technical problem or setting does the paper address?
- Why is there no well-established solution?
- What is the core contribution: insight, performance, capability, task, dataset, metric, or analysis?
- Why can the method work in essence?
- What technical advantage or new insight should a reviewer remember?
- Which experiment result is strong enough to support the central claim?

## Template Selection

Choose one dominant abstract logic. Do not mix all templates.

### Template A: Challenge To Contribution

Use when the technical challenge is easy to state and the method directly solves it.

Structure:

1. Task and importance.
2. Specific challenge in prior methods.
3. One or two sentences introducing the contribution.
4. Benefits of the contribution.
5. Experiment summary.

Sentence roles:

- `Task`: define the input, output, or setting.
- `Challenge`: state the limitation and its technical reason.
- `Contribution`: name the method idea without full module details.
- `Benefit`: explain what the design enables.
- `Evidence`: report the strongest result and scope.

### Template B: Challenge To Insight To Contribution

Use when the novelty is an observation or principle, and the method implements that insight.

Structure:

1. Task and importance.
2. Challenge or failure mode.
3. One-sentence insight.
4. Method contribution that operationalizes the insight.
5. Benefit and experiment summary.

Quality bar:

- The insight sentence must be understandable without reading the Method section.
- The implementation sentence should name the mechanism, not list every step.
- The benefit must follow from the insight, not from generic engineering.

### Template C: Multiple Contributions

Use when the paper has two or three real contributions that cannot be collapsed into one idea.

Structure:

1. Task or setting.
2. Optional contrast with prior methods.
3. Contribution 1 plus advantage.
4. Contribution 2 plus advantage.
5. Contribution 3 plus advantage, if needed.
6. Experiment summary.

Rule: write each contribution with its technical advantage in the same sentence or adjacent sentence. Avoid a bare list of modules.

### Template D: Capability First

Use when the work enables a new task, benchmark, application setting, or deployment capability.

Structure:

1. New capability or setting.
2. Why previous methods cannot support it.
3. Proposed framework.
4. What the capability enables.
5. Evidence and boundaries.

## Sentence-Level Checks

- Does every sentence have one role?
- Does the abstract include task, challenge, contribution, benefit, and evidence?
- Can the method name be understood from surrounding words?
- Are all strong adjectives backed by numbers or experiments?
- Is there any method detail that belongs in Method instead?
- Are dataset names, metrics, and improvements included only when they strengthen the central claim?

## Example Bank

Load examples only when drafting or rewriting a concrete abstract:

- `references/examples/abstract/index.md`
- `references/examples/abstract/template-a-challenge-contribution.md`
- `references/examples/abstract/template-b-challenge-insight-contribution.md`
- `references/examples/abstract/template-c-multiple-contributions.md`

## Output Pattern

Return:

1. Abstract logic outline.
2. Chosen template and why it fits.
3. Revised abstract.
4. Claim-evidence map.
5. Warnings about overclaiming, missing evidence, or unclear novelty.
