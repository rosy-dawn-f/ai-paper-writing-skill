# Multi-Thread Narrative And Sibling-Paper Differentiation

Use this reference when a manuscript contains several substantive work packages that must support one paper-level claim, when an upstream model serves a downstream decision or generation task, when an older draft demonstrates useful narrative interleaving, or when two related manuscripts need distinct research identities.

## Goal

Preserve real work without turning the paper into a catalogue of modules. Each retained thread should have a causal reason to exist, a defined output or scholarly role, a downstream or paper-level consumer, and an evidence path. Threads should converge on one capability only when the method and evidence actually support that convergence.

This workflow does not require new experiments. When the evidence inventory is fixed, reorganize the available evidence around the strongest supportable questions, calibrate unsupported claims, and disclose remaining limits instead of inventing studies or results.

## Decide The Narrative Topology

Choose among three structures before drafting.

### One Contribution Chain

Use one chain when one idea carries the novelty and the other components are standard implementation, training, preprocessing, or evaluation support. Do not create a separate gap for every module.

### Several Necessary Threads With Convergence

Use multiple threads when each one:

- answers a distinct requirement or root technical issue;
- contributes a non-routine construction, analysis, representation, decision mechanism, or validity foundation;
- has a defined output or role in the whole paper;
- can be tied to available evidence; and
- is necessary for the shared paper-level capability.

The threads may be serial, parallel, or foundational:

- `serial`: one thread produces an artifact consumed by the next;
- `parallel`: different threads satisfy different requirements of the joint capability;
- `foundational`: a thread establishes validity, fidelity, identifiability, or a trustworthy evaluation environment without pretending to emit a runtime tensor to the next module.

Do not draw a fake feed-forward arrow from a foundational study merely to make the pipeline look tighter.

### Sibling Papers Or Separate Claims

Use a sibling-paper analysis when two manuscripts share an umbrella topic but claim distinct scientific questions. If they differ only by model names, minor architecture substitutions, datasets, or wording while retaining the same question, operational setting, outputs, action role, and decisive evidence, the separation is not yet defensible. Flag the overlap rather than using rhetoric to disguise it.

## Thread-Role Map

Start with a one-sentence paper-level capability, then complete this map:

| Thread | Causal necessity | Gap or root issue | Construction or insight | Output or scholarly role | Downstream/paper-level consumer | Available evidence | Role in final capability |
|---|---|---|---|---|---|---|---|

Good role labels include `validity foundation`, `state or representation enabler`, `decision mechanism`, `cross-stage interface`, and `system-level validation`. These are prompts, not a fixed three-part taxonomy.

Apply two tests:

1. **Removal test:** if a thread is removed, which part of the paper-level capability becomes unsupported?
2. **Convergence test:** where do the threads meet in the claim, method, and evidence? A verbal meeting in the introduction alone is insufficient.

If a work package cannot pass the removal test, treat it as support rather than a standalone contribution. If the threads cannot pass the convergence test, use honest parallel contributions or reconsider whether they belong in one paper.

## Four Interleaving Techniques

### 1. Derive Upstream Work From The Downstream Need

For decision-oriented or application-oriented papers, begin with the behavior the final system must achieve. Derive the information, representation, fidelity, or prediction required to make that behavior possible, then introduce the upstream method as the response.

Prefer:

`decision need -> missing information or validity requirement -> upstream construction -> downstream use`

over:

`upstream model -> reported accuracy -> unrelated controller`

This is a reasoning order, not necessarily the implementation order.

### 2. Audit Multi-Dimensional Alignment

For every upstream-to-downstream connection, inspect the dimensions that determine whether the interface is operational rather than decorative:

| Dimension | Upstream artifact | Downstream requirement | Alignment status or transformation |
|---|---|---|---|
| Entity/spatial unit |  |  |  |
| Temporal horizon and update interval |  |  |  |
| Variable/representation semantics |  |  |  |
| Action or decision relevance |  |  |  |
| Assumptions and evaluation setting |  |  |  |

Use domain-appropriate dimensions when these do not fit. A mismatch may motivate an explicit transformation, calibrated wording, or a limitation; do not hide it behind the phrase "prediction driven" or another broad umbrella term.

### 3. End Each Method Thread With An Interface Handoff

At the end of each major method subsection, state:

`Output: ... | Semantics/shape: ... | Availability or timing: ... | Consumer: ... | Downstream role: ...`

For a foundational thread, replace `Consumer` with the paper-level claim or evaluation component it validates. The handoff should use the same terms, units, indices, and timing assumptions as the receiving subsection.

### 4. Organize Results Around Cross-Thread Questions

When evidence is sufficient, use a question ladder rather than repeating the method directory:

1. Is the upstream artifact or validity foundation credible for its claimed role?
2. Is the cross-thread interface aligned and informative for the downstream task?
3. Does the integrated method change the intended downstream behavior or mechanism?
4. Does the resulting system improve the paper-level outcome within the tested scope?

Not every paper needs four headings. Merge questions when one result answers several, and omit questions that the paper does not claim. When existing evidence cannot answer a question, weaken the corresponding claim instead of proposing fictitious evidence.

## Branch And Reconvergence Protocol

Use this drafting sequence:

1. State the shared task and paper-level capability.
2. Derive the minimum requirements for that capability.
3. Introduce a branch only when a requirement has its own root issue and response.
4. Mark whether each branch is serial, parallel, or foundational.
5. State the interface or scholarly handoff between branches.
6. Reconverge in three places:
   - the contribution-level claim;
   - the method overview or system diagram; and
   - the evidence story.

A compact generic pattern is:

`shared task -> required capability -> {validity requirement -> foundation; information requirement -> representation/prediction; decision requirement -> policy/control} -> explicit handoffs -> joint capability -> cross-thread evidence`

Use only the branches justified by the actual work. The braces do not imply that every paper needs three threads.

## Learning From A Stronger Alternative Draft

When another draft demonstrates stronger interleaving:

1. Reverse-outline it by paragraph role and causal transition.
2. Extract transferable techniques such as branch timing, interface explanation, reconvergence position, and evidence ordering.
3. Keep a fact ledger for each manuscript so model names, mechanisms, assumptions, settings, and results do not leak across drafts.
4. Transfer the narrative operation, not the other manuscript's scientific identity or claims.

## Sibling-Paper Identity Matrix

Compare sibling manuscripts below the shared umbrella:

| Identity dimension | Paper A | Paper B | Shared or discriminating? |
|---|---|---|---|
| Scientific question and target capability |  |  |  |
| Disturbance, failure, or causal mechanism |  |  |  |
| Operational setting and assumptions |  |  |  |
| Information/prediction target semantics |  |  |  |
| Spatial/entity unit or structural representation |  |  |  |
| Temporal horizon and decision timing |  |  |  |
| Downstream role |  |  |  |
| Output/action space and execution semantics |  |  |  |
| Decisive evidence and primary claim |  |  |  |

Then make three ledgers:

- `shared foundation`: terminology and background that may legitimately overlap;
- `paper-specific identity`: mechanisms, claims, interfaces, actions, and evidence unique to each manuscript;
- `leakage risks`: sentences, figures, contribution labels, or title phrases that would make one paper sound like the other.

### Title Separation

Build each title from:

`recognizable broad task + discriminating scientific object, mechanism, representation, or capability`

The title does not need to list every module. It should expose the dimension that organizes the paper's evidence. Avoid giving both papers the same fashionable modifier plus the same broad task when their actual distinction lies in different prediction semantics, structural scales, decision roles, or action spaces.

Run three tests:

1. **Swap test:** could the titles be exchanged without becoming inaccurate? If yes, they are not separated enough.
2. **Evidence test:** does each title foreground something directly supported by that paper's decisive evidence?
3. **Abstract test:** do the first problem sentence, method preview, and contribution bullets preserve the same identity as the title?

## Output Pattern

Return only the items needed for the task:

1. Paper-level capability statement.
2. Narrative-topology decision and rationale.
3. Thread-role map and removal/convergence tests.
4. Multi-dimensional interface audit.
5. Paragraph- or section-level interleaving outline.
6. Cross-thread research-question and evidence map.
7. Sibling-paper identity matrix, overlap warning, and title separation when applicable.
8. Claims that must be calibrated because existing evidence does not support the desired story.

## Guardrails

- Preserve substantive work, not the appearance of workload.
- Do not manufacture gaps, interfaces, causality, or convergence.
- Do not imply an upstream model improves the downstream system unless the evaluation supports that relationship.
- Do not use narrative differentiation to conceal duplicate publication or salami slicing.
- Keep project-specific values, private paths, and transient implementation details out of reusable narrative rules.
