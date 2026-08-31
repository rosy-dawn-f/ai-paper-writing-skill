# Paper Architecture

Use this reference when helping with ideas, outlines, abstracts, introductions, related work, contribution statements, or experiment-story alignment.

## Core Contribution

Classify the contribution into one primary promise:

- Insight: explain a phenomenon or mechanism that was poorly understood.
- Performance: do something measurably better under fair comparison.
- Capability: enable something that previous systems could not do.

Make the primary promise visible early. Secondary novelties can support the promise, but avoid making the paper feel like a bag of tricks.

Good contribution statements answer:

- What exactly is the increment over prior work?
- Why should the community care now?
- Which evidence proves the claim?
- What should a reviewer remember after closing the PDF?

Do not equate a small score increase with knowledge. Treat experimental gains as evidence for a discovery, not as the discovery itself.

## Three-Level Story

Tell a complete version of the story at three scales:

- Abstract: problem, gap, method essence, strongest evidence, value.
- Introduction: territory, niche, proposed solution, contributions, main findings.
- Body: related work, method, experiments, analysis, limitations, conclusion.

Each level should be self-contained and should unfold the same contribution with increasing detail. If the abstract claims one novelty and the experiments support another, repair the story before polishing language.

## Gap-Driven Narrative Funnel

Use the gap as a narrowing mechanism, not as a fixed number of parallel claims. Start with the shared trunk:

`territory -> target capability -> progressively narrower unmet requirement -> root technical issue`

Then choose the smallest structure justified by the work:

- Single contribution: `gap -> contribution -> evidence`.
- Several mechanisms answering one gap: introduce one contribution and distinguish the primary mechanism from supporting design constraints.
- Distinct contributions answering distinct gaps: branch only where the causal logic actually separates, map each branch as `gap -> root cause -> contribution -> evidence`, and reconverge only if the combined system supports a joint capability.

Do not force symmetry, two branches, or one contribution per paragraph. The test is whether readers can see how each narrowing step makes the eventual contribution necessary. A shorter introduction is worse if it removes these causal bridges and leaves only a list of limitations followed by a list of modules.

When comparing an older draft with a newer compressed version, compare reverse outlines rather than sentence polish. Recover stronger narrowing steps or causal bridges if the older draft has them, but revalidate all terminology, mechanisms, action spaces, experimental settings, and numerical claims before reuse. Transfer the narrative skeleton, not stale facts or an article-specific branch count.

## Reader-First Framing

Write for target readers, not for the chronological research process. Hide dead ends unless they explain a necessary design decision, limitation, or ablation. Before writing the full paper, it can help to build a one-slide story and test whether peers outside the project understand:

- the problem,
- the gap,
- the method idea,
- the main evidence,
- why the result matters.

## Introduction Pattern

Use a three-move structure:

1. Establish the territory: show the area is important, active, and still problematic.
2. Find the niche: identify a specific gap, limitation, unresolved question, or missing capability.
3. Occupy the niche: state the paper's approach, findings, value, and contribution.

Practical checks:

- Put the novel and interesting point early.
- Spend the most space on original ideas and decisive evidence.
- Respect prior work before criticizing it.
- Avoid broad field history that most readers already know.
- Consider a page-one figure when the idea is visual, architectural, or comparison-heavy.

## Related Work

Organize related work by relationships to this paper, not by a flat historical list. Usually choose three or four relevant topics:

- background methods the reader needs,
- direct competitors,
- adjacent lines of work,
- methods whose limitations motivate the paper.

For each topic, explain how prior work relates to the present contribution. Avoid dismissive phrasing. If claiming that prior work lacks something, give evidence and cite appropriately. When uncertain about taxonomy or priority, inspect related-work sections in highly relevant recent papers.

## Experiment Story

Every central claim should map to a table, figure, ablation, analysis, or qualitative result. Build the results section around contribution statements:

- main comparison for effectiveness,
- ablation for which component matters,
- analysis for why it works,
- robustness or generalization for where it holds,
- efficiency or compute for practical tradeoffs,
- limitations for where it fails.

Be honest about scope. If evidence is indirect, weaken the wording rather than stretching the claim.
