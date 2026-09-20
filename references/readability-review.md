# Readability And Language Audit

Use for local polishing, language audits, caption wording, or learning writing techniques from annotations. Follow the operation and scope selected in SKILL.md; these checks do not authorize rewriting.

## Four Axes

Assess logical strength, defensibility, confusion time, and information density. Combine applicable checks in one reading; they are not six mandatory passes. Inspect enough surrounding text to resolve references and avoid false missing-information reports. Distinguish linguistic findings from unverified scientific facts.

## Six Checks

### 1. Sentence Function And Semantic Commitment

Identify the intended role of a key sentence: established fact, research need, research action, observation, interpretation, or significance. Check whether its subject, main verb, modality, and qualifiers convey that role and the correct research object.

For example, reporting that results "highlight importance" may miss a passage's intended effectiveness claim. A capability statement may also obscure an unmet research need. Diagnose the contextual mismatch rather than judging a phrase in isolation.

Do not equate `can` with completed research, `should` with an unsolved problem, or `calculate` with lack of novelty. Never manufacture a gap through substitution. Distinguish a simulation finding from a deployment claim and an observation from a causal explanation. Phrase-level revisions must preserve scientific meaning.

### 2. Reasoning And Gap Completion

Trace the relationship relevant to the paragraph: important requirement, specific boundary of existing work, consequence of that boundary, and corresponding research action. A statement that a factor matters does not by itself establish an unmet requirement.

Connectives must reflect actual cause, contrast, refinement, or sequence. Distinguish execution order from conceptual dependence; unordered components need no invented chronology.

Do not invent prior-work limitations to complete the chain. A literature claim may remain unverified in a bounded language audit. Constructing or verifying one requires source evidence through `literature-positioning.md`.

### 3. Definitions, Mechanisms, And Referents

Check that a key object has a usable meaning and function before its design or results depend on it. Expanding an acronym may not explain its role. A phrase such as "responds indirectly" may require the intermediate mechanism.

Resolve `this`, `the method`, numbered summaries, and cross-section references to identifiable targets. Check nearby sentences, definitions, and figures before reporting a gap. Do not require every definition to occur in the immediately preceding sentence.

For deeper flow or implementation issues, use `paragraph-flow.md` or `section-method.md` only when that work is within scope.

### 4. Evidence Expression And Visual Interpretation

Check whether an effectiveness statement identifies the relevant conditions, comparator, metric, direction and magnitude, and supported inference. These can be supplied by adjacent text or a clearly referenced table; every sentence need not repeat them.

A figure/table pointer locates evidence. The surrounding prose explains what matters. A results visual supports an observation or claim; a method visual explains structure or process. Captions and labels should identify essential terms and settings without duplicating a long discussion.

Do not transcribe every cell or invent missing numbers. Use `section-experiments.md` for quantitative reporting and result-interpretation details. Without the visual or data, report the inspection limit rather than asserting that its contents were checked.

### 5. Tense, Voice, Terminology, And Convention

Judge tense by its discourse role: stable properties, completed procedures, reported findings, or future work. Valid changes need no forced unification. Imperatives can fit algorithms or instructions; an unexplained shift into commands may disrupt descriptive prose.

Keep names, abbreviations, symbols, and manuscript voice stable for the same referent. Preserve meaningful distinctions. Abstract and body may independently introduce abbreviations; follow the applicable reading unit and venue convention.

A collocation queried by a reviewer is not automatically wrong. Verify field usage when making a convention claim; otherwise retain its uncertain status. Treat numbering, capitalization, and citation placement as style-dependent, not universal language rules.

### 6. Information Progression And Structural Promises

Identify the paragraph's main message and what it adds: definition, mechanism, evidence, interpretation, or synthesis. A coherent paragraph may contain several supporting moves. The opening should orient readers without a rigid topic-sentence formula.

Check that headings, stated stage counts, and module lists match the material. Repetition across abstract, introduction, and conclusion can serve different reading levels; flag it when it displaces needed information or changes the story, not merely because concepts recur.

## Findings And Learning Output

Ground each consequential finding in a short source span:

`Location/span | Likely reader interpretation | Mismatch and effect | Certainty`

Use `supported finding`, `context-dependent`, or `unverified` for certainty. Severity depends on scientific impact, not grammatical size. Consolidate overlapping findings, and allow "no supported issue found." Use prose for a small task rather than forcing a table or score.

When explaining annotations, distinguish reviewer statements from inferred lessons, preserve authorship, and identify whether a quotation is before or after revision. A lone question mark does not establish a specific diagnosis. Offer an observable learning check with its limits; obey requests excluding rewrites or correction advice.

## Conditional Follow-Up

Submission-format checks belong to `final-submission-checklist.md`; reviewer criticism and rejection recovery belong to `paper-review.md`. Read them only for that requested work. Complete the current language task even when separate factual or experimental questions remain unresolved.
