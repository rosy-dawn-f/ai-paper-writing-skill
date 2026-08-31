# Module Design Template

Use when a module paragraph is vague.

## Design Order

1. Define representation or variables.
2. Define input.
3. Describe operations in execution order.
4. Define output.
5. State downstream use.

## Fill-In Skeleton

`We represent [object] as [symbol/structure], where [definition]. Given [input], we first [operation 1]. Next, [operation 2]. We then [operation 3]. The module outputs [output], which [downstream use].`

## Equation Integration

When using equations:

- Introduce every symbol before or near first use.
- Explain what the equation computes.
- State how the computed value is used.
- Treat the equation as part of a sentence with proper punctuation.

## Checks

- Could a reader implement this paragraph?
- Are all tensors, dimensions, or sets defined when needed?
- Does the paragraph avoid unexplained module names?
