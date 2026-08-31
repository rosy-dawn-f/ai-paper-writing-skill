# Not Recommended Introduction Patterns

Use this when diagnosing weak novelty presentation.

## Abstract Novelty Without Mechanism

Problem:

The introduction uses broad phrases such as "semantic-aware", "structure-preserving", "adaptive", or "unified" but does not explain what the method actually does.

Reviewer reaction:

- The method may look shallow.
- The novelty may look rhetorical.
- Readers may not know which experiment validates the claim.

Repair:

- State the concrete mechanism in one sentence.
- Explain why the mechanism addresses the challenge.
- Move decorative naming after functional explanation.

## Naive Baseline Patch Story

Problem:

The introduction first presents an overly simple baseline, then frames the method as a patch over it.

Reviewer reaction:

- The contribution looks incremental.
- The challenge feels easy because the writing made it easy.

Repair:

- Motivate the challenge through strong prior work and real failure modes.
- Explain the root technical reason.
- Position the method as solving the root issue, not patching a toy baseline.

## Contribution List As Module List

Problem:

The contributions are just module names.

Repair:

- Pair every module with a claim and evidence.
- Rewrite each bullet as contribution plus technical advantage.
