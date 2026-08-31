# Module Motivation Patterns

Use when a method module lacks a clear reason to exist.

## Failure-Mode Motivation

`Previous methods [do X], which works when [condition]. However, under [hard condition], they [failure mode] because [technical reason].`

## Constraint Motivation

`The method must [requirement], but directly [naive approach] would [cost/failure]. Therefore, we design [module] to [function] while [constraint].`

## Insight Motivation

`We observe that [property] remains [stable/useful] under [condition]. This suggests that [design principle], motivating [module].`

## Efficiency Motivation

`A direct implementation of [operation] requires [cost]. To reduce this cost, [module] approximates/reuses/factorizes [object] by [mechanism].`

## Checks

- The motivation should not be "to improve performance".
- The motivation should explain why the design is necessary.
- The motivation should connect to an experiment or ablation.
