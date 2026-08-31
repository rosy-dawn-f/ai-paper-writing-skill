# Integrity Risks

Use this reference when checking whether an AI paper's experimental design, reporting, or claims could look deceptive, unfair, cherry-picked, or irreproducible. The source inspiration is `NotGoodIdeas.md` from hzwer/WritingAIPaper; treat its examples as warning signs to avoid, never as tactics to imitate.

## Compute And Capacity

Risk patterns:

- Train the proposed method longer or on more data while hiding the difference behind iterations, epochs, or sample reuse.
- Increase compute-heavy operations while reporting only parameter count.
- Add ensembles, EMA, self-distillation, reparameterization, or expensive modules without transparent reporting.
- Compare large proposed models to smaller baselines.

Repairs:

- Report epochs, iterations, data exposure, hardware, wall-clock where relevant, parameters, FLOPs/latency/memory when relevant.
- Match training budgets or explain why they differ.
- Include fair larger/smaller baseline variants when size is central.
- Separate training-time and inference-time costs.

## Hyperparameters And Seeds

Risk patterns:

- Tune the proposed method more carefully than baselines.
- Use different learning-rate schedules, batch sizes, augmentations, or magic constants without disclosure.
- Cherry-pick random seeds or report only the best run.

Repairs:

- State tuning protocol and search ranges.
- Use comparable tuning budgets for baselines.
- Report mean/std or confidence intervals when randomness matters.
- Disclose seeds and important implementation constants.

## Minor Tweaks Hidden As Novelty

Risk patterns:

- Quietly swap activations, normalization, attention, pooling, resizing, skip connections, pretraining, or augmentations while attributing gains to the named method.
- Add capacity or training tricks that are not part of the claimed contribution.

Repairs:

- List implementation changes clearly.
- Ablate each meaningful tweak.
- Attribute gains to the actual source.
- Keep the named contribution and experimental evidence aligned.

## Incremental Complexity

Risk patterns:

- Add losses, formulas, curriculum learning, distillation, NAS, RL framing, or learnable gates mainly to inflate novelty.
- Use beta-gated components that can silently disable failed ideas.
- Depend on opaque hyperparameter sensitivity while claiming generality.

Repairs:

- Prefer simple explanations and simple baselines.
- Prove each component is needed.
- Report failure modes and sensitivity.
- Remove complexity that does not change evidence or capability.

## Evaluation And Reporting

Risk patterns:

- Measure many metrics/datasets but report only favorable ones.
- Modify evaluation metrics or channels in ways that make comparisons incompatible.
- Test baselines under mismatched preprocessing, hardware, prompting, or training conditions.
- Use subjective private tests, selected examples, or human preference claims without protocol.
- Leak test data, random seeds, benchmark examples, or upstream pretraining overlap.

Repairs:

- Predefine or justify metrics and datasets.
- Report unfavorable or neutral results when they affect scope.
- Align evaluation settings with prior work and disclose deviations.
- Use public test sets or transparent private-test protocols.
- Check and disclose possible data contamination.
- Present qualitative examples with selection criteria, not just the best cases.

## Red-Flag Audit Questions

Ask these before finalizing claims:

- Would the main result still hold under matched compute and model size?
- Are all baselines strong, recent, and tuned fairly?
- Can a reader reproduce the reported setting from the paper and appendix?
- Are any negative datasets, seeds, metrics, or ablations hidden?
- Does every performance gain have an honest attribution?
- Could the test set, prompts, benchmark examples, or human evaluation be contaminated?
- Are subjective claims backed by a protocol and enough examples?
- Is any renamed method actually someone else's contribution?

When a risk is present, recommend transparent reporting and claim narrowing rather than rhetorical cover.
