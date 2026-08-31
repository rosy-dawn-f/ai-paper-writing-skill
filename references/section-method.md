# Method Section Guide

Use this reference when drafting or revising the Method section, pipeline explanation, module descriptions, or technical advantages.

## Goal

Make the method concrete, motivated, and easy to implement. A reviewer should understand what the method does, why each module exists, and why the design should help.

## Pre-Writing Questions

Before writing, list:

- What are the inputs, outputs, assumptions, and scope?
- What modules exist in the pipeline?
- What is the forward process of the full method?
- For each module, how does it run?
- Why is each module needed?
- Why should each module work better than a simpler alternative?
- Which experiment or ablation supports each module?
- Which implementation details are essential for reproduction?
- For every cross-stage connection, what exactly is handed off, at what scale and time, and which downstream component or paper-level claim consumes it?

## Recommended Workflow

1. Sketch the pipeline figure first.
2. Map subsections from the figure.
3. For each subsection, plan motivation, design, and technical advantage.
4. Write the concrete design first to build a technical backbone.
5. Add motivation and advantages after the design is understandable.
6. Add notation definitions close to first use.
7. Add implementation details near the end or in a dedicated subsection.
8. For multi-thread systems, end each major thread with an explicit interface handoff and verify cross-stage alignment using `multi-thread-narrative.md`.

## Method Section Skeleton

Typical structure:

1. Overview: setting, inputs/outputs, core idea, figure pointer, subsection map.
2. Module 1: motivation, design, advantage.
3. Module 2: motivation, design, advantage.
4. Module 3 or objective/training/inference.
5. Implementation details when needed.

Overview paragraph skeleton:

`Given [input], our goal is to [output/task]. As shown in Fig. X, the proposed method consists of [module A], [module B], and [module C]. [Module A] ..., [Module B] ..., and [Module C] .... The following subsections describe these components in order.`

## Module Triad

For every important module, cover three elements.

### Design

Describe representation, network, data structure, objective, or algorithm. Use a clear input to output flow:

`given input -> operation 1 -> operation 2 -> output`

Design paragraph skeleton:

`We represent [object] as [representation]. Given [input], the module first [step 1], then [step 2], and finally [step 3]. This produces [output], which is used for [downstream role].`

### Motivation

Explain why the module is necessary. Tie it to a specific failure mode, constraint, or insight introduced earlier.

Motivation paragraph skeleton:

`A remaining challenge is [problem]. Directly applying [standard approach] leads to [failure mode] because [technical reason]. To address this, we design [module], which [high-level function].`

### Technical Advantage

Explain why the design is expected to help. Link the advantage to measurable behavior when possible, such as accuracy, robustness, efficiency, stability, generalization, or interpretability.

Advantage paragraph skeleton:

`This design has two advantages. First, [advantage] because [mechanism]. Second, [advantage], which improves [metric/behavior] under [setting].`

## Writing Module Subsections

Use this order unless the design is unusually complex:

1. Motivation: why this subsection exists.
2. Design: exact computation or data flow.
3. Advantage: why it helps and what evidence should validate it.

If the design is hard to understand, write design first, then add a short motivation paragraph before it.

## Interface Handoff Contract

When one method thread supports another, end the subsection with:

`Output: ... | Semantics/shape: ... | Availability or timing: ... | Consumer: ... | Downstream role: ...`

Check that the receiving subsection uses the same entities, indices, units, horizon, update interval, and variable semantics. If a transformation is required, describe it as part of the method rather than letting the reader infer it.

For a foundational thread, state the evaluation environment, assumption, or validity claim it establishes instead of inventing a runtime data dependency. For a parallel thread, state the joint requirement it satisfies and where the branches reconverge.

## Implementation Details

Include details that affect reproducibility or fairness:

- architecture depth, width, feature dimensions, heads, layers,
- loss weights and schedules,
- coordinate transforms, normalization, preprocessing,
- training/inference differences,
- sampling or data construction,
- hyperparameters that are not obvious defaults.

Move routine details to appendix only if the main method remains reproducible.

## Method Clarity Checks

### Logic Level

- Can the method be summarized in one pipeline?
- Do subsections follow the pipeline order?
- Does each module answer a previously stated challenge?
- Are serial, parallel, and foundational relationships represented truthfully?
- Can every cross-thread interface be traced from output semantics to downstream use?

### Paragraph Level

- Does each paragraph have one message?
- Does the first sentence reveal the paragraph role?
- Are motivation, design, and advantage separated when needed?

### Sentence Level

- Is each sentence's purpose clear?
- Are terms and symbols stable?
- Are equations integrated into the surrounding grammar?
- Are pronouns unambiguous?

## Common Failure Modes

- A module is named before its function is clear.
- The figure carries details that the text never explains.
- Motivation is vague, such as "to improve performance".
- Advantage is asserted but not connected to an ablation.
- The method reads like incremental patching of a weak baseline.
- Reproducibility depends on hidden implementation details.
- Adjacent modules are individually clear but their spatial/entity units, time scales, variables, or action roles do not align.
- A subsection ends at its own metric and never explains what the next stage receives or why it is useful.
- A foundational validation step is drawn as a runtime module even though it does not produce a runtime input.

## Example Bank

Load examples only when drafting or rewriting concrete method text:

- `references/examples/method/index.md`
- `references/examples/method/overview-template.md`
- `references/examples/method/module-triad-template.md`
- `references/examples/method/module-design-template.md`
- `references/examples/method/motivation-patterns.md`
- `references/examples/method/common-issues.md`

## Output Pattern

Return:

1. Pipeline or subsection outline.
2. Module table: `Module | Design | Motivation | Advantage | Output/interface | Downstream or paper-level role | Evidence`.
3. Revised method text with paragraph roles.
4. Missing implementation details needed for reproducibility.
5. Suggested ablations for claims made in Method.
6. Interface-alignment risks for cross-stage or multi-thread systems.
