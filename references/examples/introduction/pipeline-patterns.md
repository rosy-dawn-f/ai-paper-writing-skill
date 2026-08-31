# Introduction Pipeline Patterns

Use these patterns when introducing the proposed method in the introduction.

## One Contribution With Multiple Advantages

Skeleton:

`We propose [framework/representation], a [method type] for [task]. The key idea is [core innovation]. Specifically, [high-level implementation]. Compared with [prior family], this design [advantage 1]. It also [advantage 2], which is important for [setting].`

Use when one central idea drives the paper.

## Two Contributions

Skeleton:

`We propose [framework] to address [challenge]. The first contribution is [contribution 1], which [advantage]. However, [remaining challenge] remains. We therefore introduce [contribution 2], which [mechanism] and [advantage].`

Use when the pipeline has two distinct and necessary ideas.

## New Module On Existing Pipeline

Skeleton:

`Building on [prior pipeline], we introduce [module] to address [specific limitation]. We observe that [observation]. Based on this observation, [module] [mechanism]. Unlike [generic alternative], it [advantage].`

Use when the novelty is a module, not a full framework.

## Observation Driven

Skeleton:

`Our key observation is that [observation]. This suggests that [principle]. We implement this principle through [method mechanism], which [advantage].`

Use when the paper's novelty depends on one clear insight.

## Gap-Driven Funnel With Optional Branches

Core skeleton:

`[Task] requires [target capability]. Existing [method family] demonstrates [established benefit], but [specific limitation] remains because [root cause]. This narrows the unresolved problem to [precise gap]. We therefore introduce [contribution], which [mechanism and capability]. [Evidence] tests this response directly.`

Optional branch:

`Addressing [gap A] requires [new requirement], which exposes [gap B] because [root cause B]. We therefore introduce [contribution B]. [Contribution A] and [contribution B] jointly enable [combined capability], supported by [joint evidence].`

Use the core skeleton for a single gap and add a branch only when the second contribution has a distinct causal necessity. Do not infer the number of gaps from the number of modules, and do not present the method as a list of module names.

Legacy-draft variant:

`Reverse-outline the older and newer drafts. Retain the version with the clearer causal bridges, then replace every obsolete name, mechanism, assumption, or result with the current verified content. Preserve logic and transition rhythm, not stale claims.`

## Several Necessary Threads With Explicit Convergence

Generic skeleton:

`[Application] requires [paper-level capability]. Achieving this capability first requires [validity or fidelity requirement], yet [root issue A] prevents reliable evaluation or deployment. We therefore develop [foundational thread A], which establishes [scholarly role]. Effective decisions further require [information requirement], but [root issue B] limits the usable state. We introduce [enabling thread B], whose output [interface semantics] supports [downstream role]. Finally, [decision requirement] remains because [root issue C], motivating [decision thread C]. Rather than three independent modules, these threads establish [foundation], expose [decision-relevant information], and act on it through [mechanism], jointly enabling [capability]. Available evidence addresses [cross-thread questions].`

Use only the justified branches. If thread A does not produce a runtime artifact, describe it as a validity foundation rather than claiming that it directly feeds thread B.

Interface sentence:

`At each [availability/update point], [upstream thread] outputs [object with spatial/entity, temporal, and variable semantics]. [Downstream thread] consumes this object as [state/context/constraint/evaluation basis] to [decision role].`

Fixed-evidence variant:

`Map the existing figures and tables to the thread-role and research-question ladders. Retain a convergence claim only when joint evidence supports it; otherwise describe the demonstrated component capabilities and state the integration boundary.`

Sibling-paper differentiation variant:

`Keep the broad task recognizable, but derive each paper's title and opening from its discriminating scientific identity: [failure mechanism], [information or prediction semantics], [structural scale], [decision role], [action/output space], and [decisive evidence]. Do not distinguish the papers only by swapping model names or using the same fashionable umbrella phrase.`

## Checks

- The method preview should be concrete enough to be credible.
- Do not hide a simple method behind abstract terms.
- Do not introduce many module names without explaining their roles.
- Verify that the funnel becomes progressively more specific and reaches the exact problem solved by the paper.
- When branches exist, verify that each justified gap points to a contribution and evidence item, and that any convergence claim has joint evidence.
- If one contribution contains several mechanisms, identify which mechanism answers the primary gap and which mechanisms satisfy secondary design constraints.
- Prefer causal density over raw brevity; compression must not erase why a component is necessary.
- For several retained threads, verify removal, interface, and convergence rather than equating workload with contribution count.
- For sibling manuscripts, verify that their titles, opening problem statements, method previews, and decisive evidence preserve distinct identities.
