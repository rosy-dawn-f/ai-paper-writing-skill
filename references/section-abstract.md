# Abstract Section Guide

Use this reference when drafting or revising an abstract, auditing its sentence roles and detail levels, or learning writing techniques from supplied reference abstracts. Follow the operation and scope in SKILL.md; analysis alone does not authorize a rewrite.

## Goal

Give the reader a self-contained research argument: what the task is, what remains difficult, what changes in this work, and what the evidence supports. Keep the method recognizable without reproducing its implementation sequence. More explanation of an implementation detail does not, by itself, make that detail worth including.

## Establish The Story Before Polishing

Identify the main contribution and which designs support it. Ask:

- What exact technical problem or setting does the paper address?
- What specific limitation or unmet requirement is supported by the supplied material?
- What is the core contribution: insight, performance, capability, task, dataset, metric, or analysis?
- Why can the method work in essence?
- What technical advantage or new insight should a reviewer remember?
- Which experiment result is strong enough to support the central claim?

If contribution priority or a design rationale is unclear, inspect the supplied introduction's gap/contribution paragraphs and relevant problem analysis. Request only the missing passages needed to resolve it; do not require a full manuscript for local editing. When drafts disagree, identify the current implementation and evidence before transferring prose. Do not revive obsolete capabilities or results from a more fluent older draft.

For a structural revision, assign sentence functions and detail levels before choosing wording. Fix crowded or missing roles before adding transitions. Process order explains how a system runs; the abstract also needs the relationship between a research requirement, the design that answers it, and the observed benefit. Do not invent a causal bridge that the source does not establish.

## Sentence Functions And Detail Levels

These are functions to cover as relevant, not a fixed sentence count or mandatory order. Adjacent functions may share a sentence if it remains easy to read.

| Function | Reader's question | Useful precision and stopping point |
|---|---|---|
| Orientation | What is the object/task, and what does it do in this setting? | Give its category, function, or application. Avoid starting with several delays, constraints, modules, and failure modes at once. |
| Challenge or need | What specific difficulty motivates this work? | Name the condition, limitation, and consequence needed to understand the contribution. A miniature literature taxonomy is useful only if it prepares the method choice. |
| Contribution | What is proposed, and what changes? | State the method type and distinctive idea or capability before accumulating component names. Make the main contribution distinguishable from supporting designs. |
| Method essence | How does the idea address the need? | Retain the smallest mechanism that identifies the approach and its purpose. Usually stop before dimensions, discretization levels, layer counts, mapping rules, and routine constraints. |
| Evidence | Where, relative to what, and how well did it work? | Keep the decisive setting, comparator, metric, direction, magnitude, and interpretation-changing conditions. These can span neighboring sentences. |
| Interpretation, if useful | What does the evidence support? | Return to the opening question within the tested scope. Omit a generic importance sentence when the result already completes the argument. |

**Opening choice.** A short functional orientation often helps an unfamiliar or crowded opening: name what the intervention does before explaining why it falls short. It need not be a textbook definition. A clear challenge-led, finding-led, or capability-led opening may work better for other papers. Two reference abstracts beginning with definitions do not establish a journal-wide rule. Prefer informative function verbs over unsupported importance language, without banning phrases merely because they are common.

**Detail selection.** For each method detail, ask whether removing it would obscure the contribution, its essential mechanism, or an important boundary. If it mainly enables reproduction, place it in Method. A design's purpose can justify mentioning the design, but does not justify all its implementation parameters. Avoid deleting so much that only a generic claim such as "combines prediction with learning" remains.

- A long module name is not a mechanism explanation. Introduce only names and acronyms needed to identify the contribution or follow the evidence, define them as required by the reading unit, and explain their role. Avoid carrying over every internal name simply to match the methods section.
- Method and evidence need different precision. A state dimension and an improvement percentage are both numbers, but serve different purposes. Simplifying a mechanism does not justify replacing a measured result with "performs better."
- Exact technical detail belongs when it defines the contribution or evidence boundary: a four-bit representation in a compression paper, a hard memory limit in a capability claim, or an operating condition on which a reported gain depends. Do not replace a material condition with vague "matched settings."

Illustrative compression, only when faithful to the study: "a 256-dimensional state selects one of five action levels" may become "forecasts and recent observations guide coordinated decisions" when encoding is incidental. Keep the distinguishing forecasting mechanism elsewhere; if the encoding itself is the innovation, explain it instead. Likewise, retain a supplied "9% lower delay than baseline B under condition C" rather than compressing it into an unbounded superiority claim. These are teaching examples, not reported results or reusable facts.

## Learn From Reference Abstracts

When the user asks for close comparison, inspect each sentence on three axes: **function, detail level, and wording/claim strength**. Explain how it connects to the previous sentence and what it prepares next. A compact table can use `source sentence | role and connection | granularity | wording and limits`; do not impose it for a simple polish.

- Separate an observed choice from its effect and from the inferred lesson. Identify both successful moves and weaknesses, even in published examples; prestige is not evidence that every sentence is optimal.
- Compare how space is allocated to problem framing, design rationale, implementation, and evidence. Check whether a named design answers an established need, rather than praising the number of technical terms or transitions.
- Transfer narrative relationships, not a reference paper's facts, novelty claims, shortcomings, fixed sentence count, or exact opening. An example without numerical results is not a reason to delete available quantitative evidence.
- Supplied examples can be enough for a bounded writing analysis. Do not expand into literature research merely to imitate a venue; verifying field-wide gaps or venue conventions is a separate evidence task.

## Wording And Evidence Alignment

- Choose verbs for sentence function: introduce a proposal, describe what its mechanism does, report what was measured, then state what the evidence supports. "Important," "effective," or "appropriate" cannot substitute for the relevant function or result.
- Calibrate scope as well as modality. A condition-specific "may" or "can" is not interchangeable with an established result; changing a hedge alone does not repair an unsupported universal claim. Preserve valid modality and tense.
- Inspect dense noun strings, referents, and compressed contrasts for meaning. Specify the intended dimension when necessary (onset versus duration, simultaneous benefits versus synchronized processes). These are contextual checks, not a word blacklist.
- Order evidence around the main promise. Component accuracy, system performance, and process observations have different roles; separate gains do not establish that one caused the other. Make a change of comparator explicit.
- Match the opening problem to the ending evidence. Efficiency gains alone do not establish sample efficiency, delay compensation, or prevention of breakdown. Distinguish research motivation, implemented mechanism, observed outcome, and causal explanation; narrow the claim when the available evidence does not connect them.

## Template Selection

Use these optional patterns to choose a dominant argument. They describe functions, not sentence quotas; merge moves or end on decisive evidence when appropriate. Example skeletons do not authorize unsupported claims, fixed contribution counts, or mandatory concluding sentences.

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

## Final Pass

- Can readers identify the object, unmet need, main contribution, and decisive evidence without reading Method?
- Does each sentence add a clear function at the right detail level, and does its connection reflect the source rather than an invented rationale?
- Have implementation details been reduced without losing the mechanism's identity or material evidence conditions?
- Do the opening promise, method capability, results, and final inference agree in scope and comparator?

## Example Bank

Load examples only when drafting or rewriting a concrete abstract:

- `references/examples/abstract/index.md`
- `references/examples/abstract/template-a-challenge-contribution.md`
- `references/examples/abstract/template-b-challenge-insight-contribution.md`
- `references/examples/abstract/template-c-multiple-contributions.md`

## Output By Request

- **Draft/revise:** deliver the abstract; add a sentence-function explanation, key changes, or unresolved evidence boundary only as needed or requested.
- **Audit:** ground findings in source spans, covering structure, detail selection, and language as requested. Do not automatically rewrite.
- **Learn/compare:** distinguish source wording from inferred lessons, explain sentence functions and level of precision, and preserve exceptions. Provide a revision only when requested.

Outlines, tables, template explanations, and claim-evidence maps are aids, not a mandatory package. Do not make an ordinary abstract revision depend on extra examples, a full-paper audit, or new experiments.
