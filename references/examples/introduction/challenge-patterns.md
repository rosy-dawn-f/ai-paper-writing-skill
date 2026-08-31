# Introduction Challenge Patterns

Use these patterns to motivate the exact technical challenge the paper solves.

## Existing Task With Method Chain

Use when prior work has a clear progression.

Skeleton:

`This problem is challenging because [general challenge]. Traditional methods [approach], but they [limitation]. Recent [method family] methods improve [aspect] by [mechanism]; however, they still [remaining limitation] because [technical reason]. This unresolved issue motivates [paper direction].`

Checks:

- The final limitation must be exactly what the method solves.
- Avoid listing prior work without explaining failure modes.

## Existing Task With Historical Insight

Use when the paper's idea resembles an older principle but solves a modern limitation.

Skeleton:

`A classical line of work suggests that [insight/principle] can help [goal]. However, these methods rely on [assumption] and therefore struggle with [modern setting]. Recent learning-based methods avoid [old limitation], but they often miss [principle] and consequently [failure]. This motivates a method that combines [insight] with [modern mechanism].`

Checks:

- Respect the older work.
- Explain why older methods are insufficient without dismissing them.

## Novel Task Or Setting

Use when there are no direct prior methods.

Skeleton:

`In this work, we study [new task/setting], where the goal is to [goal]. This problem is challenging for three reasons. First, [challenge 1 and reason]. Second, [challenge 2 and reason]. Finally, [challenge 3 and reason]. These challenges require [method direction].`

Checks:

- Each challenge should be independent.
- Do not invent a fake prior-method gap when direct prior work does not exist.
