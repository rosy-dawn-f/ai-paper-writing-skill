# Evidence-First Literature Positioning

Use this reference before drafting a literature gap, a contribution claim, or a sentence that characterizes prior work. It prevents terminology drift, over-broad claims, and strawman comparisons.

## Trigger

Read this file when the task includes any of the following:

- "existing methods", "most studies", "no prior work", "first", or "unexplored";
- a contribution framed as a new problem, framework, coordination, or capability;
- a local PDF folder, supplied references, or a request to compare with prior work;
- uncertainty about field-preferred terminology.

## Evidence Ledger

For each closest source, record only four facts:

`Source | What it controls or predicts | Capability it demonstrates | Precise distinction from this work`

Use the ledger to decide the wording:

- A local, non-exhaustive corpus supports: "Among the reviewed studies..." or "The reviewed studies do not directly...".
- A comprehensive search can support broader wording only when its coverage is documented.
- "First", "none", and "unexplored" require a systematic, current search. Otherwise remove them.

## Comparison Protocol

1. Name the prior-work family using the terminology found in its own papers.
2. State the demonstrated benefit fairly.
3. Identify one specific remaining design question: mechanism, prediction target, decision timing, action space, spatial deployment, assumption, or evaluation setting.
4. State how the present construction addresses that question.

Do not equate a different implementation with an absent capability. For example, a paper that has a fixed action area does not prove that every paper has a fixed action area.

## Terminology Discipline

Adopt the noun that appears in the closest target literature.

- Use `strategy`, `approach`, `scheme`, `method`, or `controller` for a practical control method.
- Use `formulation` only for an explicitly defined optimization problem, MDP, state-action model, or mathematical program.
- Use `framework` only when the work defines an operational organization of components and their interfaces, not merely a new label for a known task.

If the corpus provides no stable terminology, use the least theory-laden accurate noun and flag the choice as tentative.

## Manuscript Voice

For a journal article or short paper, use `this paper` when introducing the manuscript's method, contributions, organization, or scope. Reserve `this study` for a particular empirical investigation, dataset analysis, or experimental result when that distinction is useful. Keep the choice consistent within a section; do not use `this study` as a casual substitute for `this paper`.

## Anti-Strawman Patterns

Avoid:

`Prior forecasts are merely appended to the controller input and are therefore not useful.`

Prefer:

`Prior predictive or model-based controllers demonstrate the value of future-state information. This work addresses the distinct question of how [specific forecast] should determine [specific control decision].`

Avoid:

`Existing methods use a fixed spatial control area.`

Prefer:

`Many reviewed methods use a pre-specified control area, while spatially differentiated or boundary-oriented designs have also been explored. The present work differs by [specific mechanism and action].`

## Contribution Strength Test

For every contribution, write:

`Construction | New capability | Closest comparator | Evidence`

Treat a contribution as weak if it only re-describes a problem. A framework contribution is defensible when it:

1. formalizes an operational link between previously separate elements;
2. enables a concrete action, prediction target, or decision capability;
3. has a direct baseline or ablation that can test that capability.

## VSL Case Record: Local-Corpus Experience

Use only as a case example, not as a universal survey result.

- Preferred paper-level nouns included `VSL control strategy`, `VSL control approach`, and `VSL control scheme`; reserve `VSL formulation` for a defined control problem.
- Reactive, feedback, predictive/MPC, RL, imagination-augmented, lane-level, individualized, boundary-oriented, and vehicle-targeted VSL designs can all exist. Do not write that prediction, spatial refinement, or coordination is absent without checking direct competitors.
- A defensible gap may be a particular combination of disturbance mechanism, forecast horizon, action semantics, and implementation boundary rather than any one element alone.

## Final Check

Before finalizing the paragraph or contribution list, verify:

- Each broad prior-work statement has a source and a review boundary.
- Each contrast acknowledges what the comparator actually achieves.
- Terminology matches the source literature.
- The contribution states construction and capability, not rhetoric alone.
- Any priority claim has evidence appropriate to its strength.
