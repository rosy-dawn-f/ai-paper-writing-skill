# Abstract Template B: Challenge To Insight To Contribution

Use when the paper's value comes from a new observation or principle.

## Sentence Roles

1. Task: define the setting.
2. Challenge: expose the failure mode.
3. Insight: state the key observation in one sentence.
4. Contribution: explain how the method operationalizes the insight.
5. Evidence: summarize results and scope.

## Fill-In Skeleton

`[Task] requires [desired behavior], yet current methods often [failure mode] under [condition]. We observe that [insight], suggesting that [principle]. Based on this observation, we propose [method], which [mechanism that implements the insight]. This design [advantage] while [tradeoff or constraint if relevant]. Experiments on [datasets/settings] show [main result], supporting [supported conclusion].`

## Good Insight Sentence

A good insight sentence is concrete enough to guide method design:

- Weak: `We observe that features are important.`
- Stronger: `We observe that [specific feature relation] remains stable under [condition], while [competing signal] changes substantially.`

## Revision Checks

- The insight must be understandable before the Method section.
- The contribution must clearly implement the insight.
- Evidence should validate the insight or its consequence, not only report a leaderboard number.
