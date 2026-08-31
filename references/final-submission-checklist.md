# Final Submission Checklist

Use this reference for last-mile manuscript checks, especially when the user mentions final submission, camera-ready cleanup, LaTeX, formulas, notation, figures, tables, citations, anonymity, or the day before a deadline.

Source basis: distilled and paraphrased from MLNLP-World/Paper-Writing-Tips. Treat this as an operational checklist, not a substitute for the target venue's official rules.

## Priority Order

Check in this order:

1. Desk-reject and submission-system risks.
2. Anonymous-review and artifact privacy risks.
3. LaTeX compilation, references, figures, tables, and formulas.
4. Scientific-English and notation consistency.
5. Visual polish and page-economy improvements.

Do not spend the final hours polishing local phrasing before confirming page limit, formatting, anonymity, complete files, and successful compilation.

## Desk-Reject Risks

Verify against the official venue instructions:

- Page limit, appendix/supplement policy, font size, margins, line spacing, and template version.
- Required checklist, ethics statement, limitations statement, responsible AI statement, or reproducibility material.
- Anonymous submission compliance in PDF, supplement, code, data, demos, acknowledgments, metadata, file names, paths, and hidden files.
- Title, author-anonymous version, abstract, keywords, and track/topic selections match the submission portal.
- All figures, tables, formulas, captions, references, and appendices appear in the final compiled PDF.
- No unresolved LaTeX references, citation question marks, placeholders, comments, TODOs, overfull layout damage, or stale experiment numbers.
- Submission deadline, time zone, upload size, supplement format, and portal behavior are checked early enough to recover from slow uploads or site failures.

## LaTeX And Source Hygiene

- Compile from a clean source checkout and inspect the final PDF, not only the editor preview.
- Keep a dated final source/PDF backup before last-hour edits.
- Use `\label` and `\ref` or `\autoref` consistently for sections, figures, tables, and equations.
- Use nonbreaking spaces where a reference should stay attached to the noun, such as `Fig.~1`, `Table~2`, or `Sec.~3`.
- Avoid manual numbering for sections, figures, tables, equations, algorithms, and appendices.
- Check that footnotes attach cleanly to the intended punctuation and do not introduce anonymity leaks.
- Avoid layout hacks that make the final PDF fragile, especially aggressive figure shrinking, negative spacing, or tiny fonts.

## Notation And Formulas

- Use consistent symbol classes: lowercase italic for scalars, bold lowercase for vectors, bold uppercase for matrices, calligraphic letters for sets or structured collections when appropriate, and blackboard bold for number domains or expectations.
- Keep element symbols aligned with their set or collection symbols.
- Define non-obvious symbols, abbreviations, functions, and operators before or near first use.
- Use LaTeX commands for recurring functions, operators, model names, and special notation so formatting stays consistent.
- Treat formulas as part of the sentence: punctuation and following capitalization should match the grammar around the equation.
- Use aligned multi-line equations when the equality or transformation chain matters.
- Number only equations that are referenced or central to the argument.
- Check that parentheses and delimiters are sized professionally when expressions are large.

## Figures And Tables

- Prefer vector figures for diagrams and plots when possible; otherwise use sufficient resolution for print and zoomed PDF inspection.
- Ensure text inside figures is readable and visually close to the manuscript font size.
- Keep figure styles consistent: fonts, line weights, marker sizes, color semantics, arrows, module colors, and legend placement.
- Design for grayscale or color-impaired reading when the comparison matters; avoid relying only on color.
- Use a limited, meaningful color palette; use stronger color only when it encodes importance or category.
- Remove excessive whitespace around figures and keep key content visible at the printed size.
- Avoid repeating the full caption in the main text; use the main text to state the takeaway or interpretation.
- Captions should identify the question, setting, key comparison, and main conclusion, not only name the visual.
- Use booktabs-style tables; avoid vertical rules unless they are truly needed.
- Make tables scan naturally with clear baselines, grouped columns, consistent decimal precision, and explained abbreviations.

## Scientific English

- Use formal academic English; avoid contractions such as "don't", "can't", and "isn't".
- Define abbreviations, datasets, models, and metrics at first use; keep capitalization consistent afterward.
- Prefer present tense for stable facts, method descriptions, and paper-internal claims unless chronology matters.
- Avoid absolute or vague claims such as "solves", "always", "perfect", "semantic", "meaningful", or "better" unless the evidence precisely supports them.
- Reduce pronoun ambiguity; repeat the model, method, component, or dataset name when it improves clarity.
- Keep sentences focused: separate observation, hypothesis, method, and result when mixing them would blur the logic.
- Check articles, plural forms, hyphenation, and common sound-based article cases such as "an LSTM" and "a U-Net".
- Keep heading capitalization style consistent across the paper.

## Citations And Bibliography

- Prefer the published conference or journal version over an arXiv-only record when both exist.
- Do not cite multiple versions of the same paper unless there is a specific reason.
- Check author names, title capitalization, venue names, year, volume, pages, DOI, and URL fields instead of trusting exported BibTeX blindly.
- Keep venue naming style consistent, especially full names versus abbreviations.
- Make sure citation commands do not become ungrammatical sentence components.
- Leave a readable space between citation markers and surrounding text where the template expects one.
- Verify that every cited claim is supported by the cited work and that important recent direct competitors are not missing.

## Artifact And Supplement Privacy

- Search source, supplement, code, logs, notebooks, metadata, and data cards for author names, institutions, emails, acknowledgments, local usernames, absolute paths, cloud bucket names, API keys, and private URLs.
- Remove hidden directories or files from supplemental code archives unless explicitly required.
- Check hard-coded paths, cached outputs, notebook execution metadata, and comments for identity leaks.
- Ensure README files, demo pages, model cards, dataset cards, and code comments match anonymous-review policy.

## Final-Day Procedure

- Produce a candidate final PDF and supplement at least one day before the deadline.
- Run the official checklist before making cosmetic changes.
- Re-copy all critical numbers from the final experiment logs or tables into the manuscript, captions, abstract, and submission form.
- Upload an early valid version before the last-hour rush, then replace it only with carefully verified improvements.
- After submission, save the submitted PDF/source/supplement and monitor the registered email and venue website for deadline or submission-status updates.
