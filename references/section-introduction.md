# Introduction Section Guide

Use this reference when drafting, rewriting, or diagnosing an introduction.

## Contents

- Goal and logic maps
- Reason backward and recover logic from older drafts
- Multi-thread interleaving
- Forward story
- Opening patterns
- Technical-challenge patterns
- Pipeline patterns
- Contribution bullets
- Common failure modes
- Example bank and output pattern

## Goal

Lead readers from task importance to a precise technical gap, then to the paper's contribution and evidence. The introduction should make the paper's novelty feel inevitable, not decorative.

## Logic Map

Build the introduction around this gap-driven funnel:

`task -> target capability/metric -> prior methods fail -> root technical issue -> proposed idea/pipeline -> why it works -> evidence and contributions`

If any link is missing, repair the story before polishing sentences. Each paragraph should reduce the space of possible problems until the paper's exact contribution becomes a credible response rather than an arbitrary choice.

Choose the fewest branches supported by the contribution structure. A paper with one central gap should remain a single chain. When solving one requirement exposes another necessary gap, or distinct contributions answer genuinely distinct limitations, branch from the shared funnel and map only those branches:

`shared task and capability -> gap A -> contribution A -> evidence A`

`requirement exposed by A -> optional gap B -> contribution B -> evidence B`

`optional convergence -> combined capability -> joint evidence`

Do not assume that two branches are better than one, and do not force every component to have its own gap. Conversely, do not overload one gap with orthogonal requirements such as timing, actuation, spatial coordination, robustness, and stability while explaining only one root cause. Either derive each necessary requirement with a visible causal bridge or identify one as the primary gap and present the others as supporting design constraints.

## Reason Backward First

Before writing, answer:

- What technical problem does the paper solve?
- Why is there no well-established solution?
- Which previous methods define the strongest contrast?
- What contribution solves the challenge?
- Why does the contribution work?
- Which result proves the contribution matters?
- What should a reviewer remember as the paper's new knowledge?

## Recovering Logic From An Older Draft

When the user prefers an older draft, compare the drafts at two separate levels:

1. Reverse-outline both versions by paragraph role and causal transition.
2. Decide which version better preserves progressive narrowing through `problem -> requirement -> gap -> response`, including any branches genuinely required by the contribution structure.
3. Build a current fact ledger for names, mechanisms, assumptions, action spaces, datasets, baselines, and results.
4. Reuse the stronger outline and transition rhythm, but rewrite it with the current fact ledger and calibrated literature claims.

Do not reject an older draft merely because its grammar is weaker, and do not restore obsolete content merely because its narrative structure is stronger. Treat logic, style, and factual validity as separate layers.

## Multi-Thread Interleaving

When several substantive work lines must remain visible, read `multi-thread-narrative.md` before drafting. First decide whether they are serial, parallel, or foundational; then derive each line from a necessary requirement of one paper-level capability. Module count alone does not justify multiple gap branches.

For application- or decision-oriented work, introduce the required downstream behavior before the upstream estimator, predictor, representation, simulator, or data construction. This lets the reader see why the upstream output must have a particular scale, horizon, semantic meaning, or validity property.

The introduction should expose three kinds of connection:

1. a causal bridge from the shared task to each necessary thread;
2. an interface or scholarly handoff between threads; and
3. a reconvergence statement supported by the method overview and evidence plan.

If a thread is foundational rather than a runtime input, say which validity claim or evaluation environment it establishes. Do not describe it as a direct computational input merely for narrative symmetry.

## Forward Story

Write in this order unless the paper demands another structure:

1. Task, application, or scientific setting.
2. Desired behavior, metric, capability, or practical requirement.
3. Why current methods fall short.
4. Root technical reason for the failure.
5. Proposed idea or pipeline.
6. Why the idea works and what insight it provides.
7. Evidence summary and contributions.

## Part A: Opening The Task

Choose the opening style based on reader familiarity.

### A1. Task First, Then Applications

Use when the task is niche or ambiguous.

Structure:

1. Define the task by input and output.
2. Clarify the objective or scope.
3. Name two or three applications.

Skeleton:

`[Task] aims to estimate/reconstruct/generate/predict [output] from [input]. This capability supports [application 1], [application 2], and [application 3].`

### A2. Applications First

Use when the task is familiar to target reviewers.

Structure:

1. Open with why the application matters.
2. State the target requirement, such as accuracy, efficiency, robustness, safety, or controllability.
3. Move quickly to the challenge.

### A3. General Task To Specific Setting

Use when the paper studies a new setting under a familiar task.

Structure:

1. Start from the broader task.
2. Narrow to the specific setting.
3. Define the input/output boundary of that setting.

### A4. Open With Challenge

Use when the task is very familiar and the failure case is the real hook.

Structure:

1. State the task or application in one sentence.
2. Mention representative prior methods.
3. Expose the unresolved failure case and its technical reason.

## Part B: Introducing The Technical Challenge

The challenge paragraph is the heart of the introduction. It should name both limitation and technical reason.

### B1. Existing Task With Method Chain

Use when there is a clear lineage of prior methods.

Structure:

1. General challenge in the task.
2. Traditional or early methods and their limitation.
3. Recent methods and their limitation.
4. Final unresolved challenge that this paper solves.

Avoid making the paper look like a small patch over a naive baseline. Lead through real prior methods and real failure modes.

### B2. Existing Task With Historical Insight

Use when your insight has roots in traditional methods or theory.

Structure:

1. State the limitation of mainstream methods.
2. Introduce the older insight or principle.
3. Explain why older methods cannot directly solve the modern setting.
4. Show why recent methods still miss the point.
5. Bridge to your method.

### B3. Novel Task Or Setting

Use when direct prior methods do not exist.

Structure:

1. State the new goal.
2. Explain why it is challenging for two or three reasons.
3. For each reason, state observable difficulty and technical cause.
4. Transition to the proposed pipeline.

## Part C: Introducing The Pipeline

Choose based on contribution shape.

### C1. One Contribution With Multiple Advantages

Use when one representation/framework is the main novelty.

Structure:

1. Introduce the framework or representation.
2. Point to a teaser or pipeline figure if available.
3. State the key innovation.
4. Explain concrete implementation at high level.
5. State advantages over previous methods.

### C2. Two Contributions

Use when one contribution solves the main challenge and another handles a remaining issue.

Structure:

1. Introduce the framework.
2. State contribution 1 and its advantage.
3. Identify the remaining challenge.
4. State contribution 2 as the response.
5. Connect both to evidence.

### C3. New Module On Existing Pipeline

Use when the novelty is a module added to an established pipeline.

Structure:

1. Start from the prior pipeline.
2. State the module as the innovation.
3. Give the observation that motivates it.
4. Explain how it plugs into the pipeline.
5. Contrast with generic alternatives.

### C4. Observation Driven

Use when the contribution follows from one important empirical or theoretical observation.

Structure:

1. State the observation.
2. Explain why prior methods fail to exploit it.
3. Introduce the method that operationalizes it.
4. State the resulting advantage and evidence.

### C5. Gap-Driven Funnel With Optional Branches

Use when the introduction needs to narrow through one or more layers of limitation before the contribution becomes inevitable.

Structure:

1. Establish the task and target capability.
2. Progressively narrow from a broad limitation to the root issue the paper actually solves.
3. Introduce the contribution at the narrowest justified point.
4. If the work contains a distinct dependent contribution, show the requirement that creates a second branch before introducing it.
5. Reconverge branches only when the combined pipeline enables a joint capability.
6. Mirror the final gap--contribution structure in the contribution bullets and evidence summary.

### C6. Several Necessary Threads With Explicit Convergence

Use when the paper contains multiple non-routine work packages that jointly enable one capability.

Structure:

1. State the paper-level task and downstream capability.
2. Derive the minimum requirements for that capability.
3. Introduce each thread only after its own requirement and root issue are clear.
4. Mark the role of each thread: serial, parallel, or foundational.
5. Explain the interface or scholarly handoff rather than listing modules.
6. Reconverge on the joint method claim and preview the cross-thread evidence.

Apply the removal and convergence tests in `multi-thread-narrative.md`. If routine support work fails the removal test, keep it in the method or setup rather than elevating it into a contribution bullet.

## Contribution Bullets

Contribution bullets should be specific and verifiable:

- Use "We identify..." for observations or analysis.
- Use "We propose..." for methods, modules, frameworks, tasks, datasets, or metrics.
- Use "We demonstrate..." for empirical findings.
- Avoid bullets that restate ordinary engineering steps.
- Avoid claiming novelty for a component if the real novelty is how it is used, analyzed, or evaluated.
- Map every bullet to at least one experiment, figure, theorem, or analysis.

## Common Failure Modes

- The introduction starts with broad field history and reaches the paper too late.
- The gap is generic rather than the exact challenge the method solves.
- The technical reason behind the gap is missing.
- Prior work is dismissed without evidence.
- The method appears as an arbitrary pipeline rather than a response to the gap.
- The introduction lists gaps without progressively narrowing from the task to the exact root issue.
- The writing forces multiple gap branches because the method has multiple components, even though one central gap would explain the design more clearly.
- Necessary gap branches are compressed into one paragraph and followed by a component list, obscuring which contribution answers which gap.
- Several substantive threads are reduced to a model list without causal roles, interfaces, or a joint capability.
- A foundational validation thread is falsely described as a runtime input to force a serial pipeline.
- The introduction claims cross-thread synergy, but the method overview or available evidence never demonstrates where the threads meet.
- A newer draft is shorter but has lower causal density than an older draft.
- The writing introduces a naive solution only to make the proposed method look better.
- Contributions do not match experiments.
- The abstract and introduction make stronger claims than the results section.

## Example Bank

Load examples only when drafting or rewriting a concrete introduction:

- `references/examples/introduction/index.md`
- `references/examples/introduction/opening-patterns.md`
- `references/examples/introduction/challenge-patterns.md`
- `references/examples/introduction/pipeline-patterns.md`
- `references/examples/introduction/not-recommended-patterns.md`

## Output Pattern

Return:

1. Introduction logic map as a gap-driven funnel; include branches and convergence only when the work requires them. For a multi-thread paper, name each thread's serial, parallel, or foundational role.
2. Chosen opening/challenge/pipeline patterns and why they fit.
3. Paragraph-by-paragraph outline with roles; when an older draft is supplied, state which causal bridges are retained and which facts are discarded. When several threads are retained, show their interface handoffs and reconvergence paragraph.
4. Revised introduction or targeted paragraph rewrite.
5. Claim-evidence map for the strongest claims.
6. Missing evidence or citation checks.
