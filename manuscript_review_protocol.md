# Two-Stage Manuscript Review Protocol

This protocol extends `be-critical` for academic peer review. It produces a calibrated, journal-aware review through a two-stage workflow with a deliberate handoff to the human reviewer.

Use this protocol whenever the query type is **Academic Manuscript** — i.e., the user hands over a PDF (or DOCX/HTML) of a paper for peer review, especially from `~/GoogleDrive/Service/Reviews/current/`.

---

## Pre-flight: Journal Quality Assessment

Before reviewing, characterize the target venue. Critique severity must match the journal's typical standard, not the field's ceiling. (A solid mid-tier specialty journal does not need to clear a Nature bar.)

Produce a short journal profile:

| Field | What to fill in |
|------|-----------------|
| Journal | Full name, publisher |
| Tier (heuristic) | Top-tier general, top-tier specialty, mid-tier specialty, low-tier specialty, unknown |
| Indexing & metrics | SSCI/SCI/Scopus; recent IF if known; CiteScore; H-index if known |
| Audience | Practitioners, researchers, policy, mixed |
| Typical methodological standard | What kind of evidence routinely clears review here? Single-site empirical work? Multi-site? Replications? Case studies? |
| Calibration verdict | One sentence: "Hold the paper to the standard of *typical articles in this venue*, which means [X]." |

If the journal is unknown, flag this and ask the user, or proceed with a conservative mid-tier assumption.

---

## Stage 1 — Summary, Logic Model, and Targeted Questions

**Goal:** Build a neutral-to-mildly-skeptical inventory the user can react to. Do not pre-decide the verdict.

Produce one artifact (markdown, with embedded Mermaid for diagrams; HTML on request):

1. **Header** — title, author block (blinded), journal, manuscript ID, submission type, date.
2. **Journal profile** — the table from Pre-flight.
3. **Plain-language summary** — 1–2 paragraphs. What the paper claims, what they did, what they conclude. Neutral.
4. **Research questions / hypotheses** — verbatim or close paraphrase, in a numbered list.
5. **Logic model (Mermaid `graph TD`)** — visualize the argument chain:
   `THEORY → PREDICTIONS → DESIGN → MEASURES → ANALYSIS → FINDINGS → CLAIMED CONTRIBUTIONS`. Use clear node labels. Add an "INFERENTIAL LEAPS" branch for places where the chain skips a step.
6. **Evidence map** — table:

   | Claim | Evidence cited (study, table, statistic) | Strength (strong / mixed / thin) | Notes |
   |------|------|------|------|

7. **Provocations** — 5–10 candidate critique points organized under the four buckets from `be-critical`:
   - **Logical** (falsifiability, tautology, internal contradiction)
   - **Evidential** (single studies, self-citation scaffolding, design-claim mismatch)
   - **Framing** (metaphor-as-theory, selective citation, denominator problems)
   - **Structural** (sections that don't connect, scope vs. depth)

   For each provocation: one-sentence statement of the issue, a pointer to the page/line/table, and a one-line "why it matters."

8. **Targeted questions for the human reviewer** — 3–6 questions whose answers genuinely shape the review. Required questions:
   - **Verdict instinct.** Reject / Major revision / Minor revision / Accept (with conditions)?
   - **Severity dial.** Which provocations are fatal flaws vs. would-improve-the-paper?
   - **Field-specific calls** that depend on knowledge Claude doesn't have (e.g., is this measure standard? is this finding novel? has this critique been litigated already?).
   - Optional: anything to specifically praise or specifically not raise.

9. **Stop.** Do not write the review. Wait for the user's answers.

Save the Stage 1 artifact alongside the manuscript: `<MANUSCRIPT_ID>_stage1.md` in the same directory as the PDF.

---

## Stage 2 — Review in the User's Voice

**Goal:** Produce a publication-ready peer review using Pem's two-letter format and voice. Triggered only after the user has answered Stage 1 questions.

Read voice memory and prior reviews (see `reference_review_locations.md` in project memory) before drafting. Then write:

### Letter 1 — To Editor

- 1 short paragraph.
- Compress the paper's contribution into **two sentences** the editor can scan.
- Convey the recommendation through tone (often without stating the verdict label outright — the editor reads it).
- If reviewer calibration matters (e.g., "I think prior reviews were too lenient" or "I am holding this to typical-for-the-journal, not Nature"), say so.

### Letter 2 — To Authors

- Open with what is **genuinely strong** (sampling, design choices, transparency, etc.). Do not flatter; only note what is real.
- Then a 1–2 sentence framing of the overall concern.
- Organize critique under named headers (e.g., **Theory and Inference**, **Measurement**, **Analysis**, **Generalization**, **A few smaller items**). Use whatever 3–5 headers fit the paper.
- Numbered points within each header. Each point: state the issue, point to the location (page/line/table), explain why it matters, and where useful, recommend literature.
- Close with a constructive line in Pem's voice (e.g., "These, as usual, are just suggestions to help the authors.").

Save the Stage 2 artifact: `<MANUSCRIPT_ID>_review.md` in the same directory as the PDF.

---

## Voice Guide (drawn from Pem's prior reviews)

- **Civil but firm.** "I struggled with the language" / "I enjoyed reading the paper even though…" / "fixable by the competent authors these seem to be."
- **Name undefined or misused key terms.** When the paper uses a term as load-bearing but never grounds it (e.g., "inertia," "upregulation," "reciprocity"), call it out by name.
- **Cite specific page/line numbers and table references.** Reviewers who can be checked against the manuscript carry more weight.
- **Recommend specific literature** when there's a real gap. Don't pad with citations; recommend only what would change the analysis.
- **Surgical lines for overreach.** "I don't think that conclusion is justifiable given your model." "These coefficients are not directly comparable unless…"
- **Methodological priorities Pem reliably surfaces:**
  - Effect size vs. statistical significance — applied symmetrically (don't let authors invoke effect-size humility on null results while interpreting tiny non-null effects as "findings").
  - Reliability/validity must be inspected before structural results are interpreted.
  - Convergent vs. discriminant validity asymmetries.
  - Item wording / valence as a confound.
  - Cross-lagged interpretation requires matched measurement quality.
  - Missing data assumptions (MAR/MCAR) named explicitly.
  - Posterior/credible-interval interpretation should not be smuggled back into NHST framing.
  - ICC / variance partition cannot be cleanly read when reliability is unaccounted for.
  - Generalization beyond the sampled context (single site, single discipline, single cohort).
  - Alpha inflation / familywise error — when many comparisons are run, scattered "significant" findings deserve familywise-error-adjusted skepticism. Use the terms "alpha inflation" or "familywise error," not "multiplicity." Recommend Benjamini-Hochberg (BH-FDR) as the default correction for its balance between Type I error control and power; mention Bonferroni only as a more conservative alternative when context calls for it.
- **Close with constructive intent.** "These, as usual, are just suggestions to help the authors."

---

## Worked Example

For a worked Stage 2 review illustrating the two-letter format, named-header organization, numbered points with location pointers, and the voice patterns above, see [`examples/manuscript-review-stage2.md`](examples/manuscript-review-stage2.md). The example is a redacted version of an actual review (peer-review confidentiality preserved); the voice and structure are unchanged.

## Calibration Reminder

This protocol holds papers to a high but **journal-appropriate** standard. The bar is the venue's typical published article, not the ceiling of top general-science journals. Do not import standards from a more elite venue to manufacture rejection.

Fatal flaws block publication anywhere; "would-improve" notes are constructive at this venue. Spend critique budget on inference, evidence, measurement, and generalization.
