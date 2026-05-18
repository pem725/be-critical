# Example — Stage 2 Manuscript Review (in Pem's Voice)

This example illustrates the output of **Stage 2** of the Two-Stage Manuscript Review Protocol (`manuscript_review_protocol.md`). It shows the two-letter format, named-header organization, numbered points with location pointers and recommended literature, and the closing "just suggestions" line.

The manuscript reviewed here was a research article submitted to a mid- to upper-mid-tier specialty journal in higher education / educational measurement. Manuscript ID and verbatim author quotations have been redacted for peer-review confidentiality; the methodological substance is unchanged. Paper topic: student evaluations of teaching (SET), instructor sex, and STEM, using five years of administrative data from a single Minority-Serving Institution.

**Reviewer answers that drove this Stage 2 (from Stage 1 questions):**

- Verdict: Major revision
- RCT/scope-condition severity: Medium — language only
- Familywise error in 16-cell interaction table: Hard — demand BH-FDR adjustment or principled re-interpretation
- Effect-size asymmetry: Worth flagging, not central

---

## To Editor:

The authors use five years of course-level SET data from a single large, diverse Minority-Serving Institution to test whether female instructors are penalized in evaluations overall, in STEM, and within STEM disciplines, and they find essentially no main effect of instructor sex on any of four SET outcomes. Their broader claim — that this null result *refines* Role Congruity Theory by establishing institutional context as a moderator of bias — is a stronger inferential reach than a single-institution design supports, and the within-STEM disciplinary analysis (Table 7) reports two of sixteen interaction cells as significant, in opposite directions, without addressing alpha inflation.

The empirical work is solid and the effect-size framing is timely and right-headed for this venue. The contribution is salvageable as a descriptive case study with a clear theoretical caveat. I recommend major revision: the authors should (a) constrain the institutional-moderator claim to hypothesis-generating language given N = 1 institution, (b) re-analyze or principally re-interpret Table 7 with alpha inflation in mind, and (c) reckon with the asymmetry between effect-size humility on the null sex coefficients and substantive interpretation of the small STEM main effect. None of these are fatal; all are fixable by the competent authors these seem to be.

## To Authors:

The manuscript examines whether female instructors receive lower SET scores than male instructors, whether any gap is amplified in STEM, and whether patterns differ within STEM disciplines, using five years of course-level data from a single large, diverse Minority-Serving Institution. There is much to commend in this work. The use of a five-year administrative dataset (N ≈ 14,700 course-semesters; ~8,150 STEM) is a real strength, as is the parallel modeling across four SET outcomes, the inclusion of cluster-robust standard errors at the instructor level, and the use of college-level fixed effects to absorb between-college variance. I particularly appreciated the authors' explicit move to foreground effect sizes alongside statistical significance — this is exactly the right argument to make in large-N SET research, and it is an argument this venue should welcome. The eBay illustration (Lin et al., 2013) is rhetorically effective even if borrowed from outside the discipline.

That said, I think the paper's inferential reach in places exceeds what the design can support, and there is one methodological matter — the within-STEM interaction analysis — that I would like the authors to confront directly before publication. I organize my comments below under four headers.

### Theory and Inference

1. **Single-site claim about institutional context.** The Discussion repeatedly characterizes this paper as evidence that *diverse institutional context attenuates RCT-predicted bias*. With one institution, this claim is hypothesis-generating rather than hypothesis-testing. I would like the authors to soften this language and to explicitly state that institutional moderation cannot be tested from N = 1 institution. The current framing implies a comparative inference the design does not support; "our findings are consistent with the possibility that..." is closer to what the data permit. The same correction should be made in the abstract, where the language is currently the strongest.

2. **Scope-condition rescue of RCT.** Related to (1): the paper treats the failure of the central RCT prediction as a *refinement* of RCT — bias is conditional on context — without specifying what kind of evidence would constitute a problem for RCT-in-SET going forward. Scope-condition refinement is normal theoretical work, but in its current form readers may reasonably ask: under what observable conditions would the authors conclude RCT does *not* apply to higher-education SET? A sentence or two committing to a falsifying condition (or to a positive prediction the authors would treat as decisive) would strengthen the theoretical contribution considerably.

### Alpha Inflation and Reporting (Table 7)

3. **The within-STEM disciplinary analysis needs to be re-thought.** Table 7 tests sixteen Female × discipline interactions (four disciplines × four outcomes). Two are significant at p<.05, and these two effects point in *opposite* directions. With sixteen tests at α = .05, the familywise error rate is well above the nominal level — under the null, roughly 0.8 false positives are expected, and observing two with opposite signs is more consistent with noise than with a discipline-specific bias pattern. As written, the Results and Discussion treat these two cells as substantive findings, which I do not think the data warrant.

   I would like the authors to do one of the following: (a) report an alpha-inflation-controlled analysis and re-interpret accordingly — Benjamini-Hochberg (BH-FDR) is my recommendation here for its balance between Type I error control and power; a joint test of the four interactions per outcome would also be a sensible first move, with cell-by-cell inspection only if the omnibus is significant; or (b) keep the unadjusted analysis but explicitly acknowledge the familywise-error issue, downgrade the language in the Results and Discussion to describe the two p<.05 cells as *isolated, opposite-signed, and consistent with chance*, and remove the disciplinary interpretation from the abstract and conclusion. Option (a) is preferable, but either would be defensible. As it currently stands, the paper invokes effect-size humility for null results but does not invoke familywise-error humility for scattered positives, which weakens an argument I otherwise want the paper to make.

### Measurement and Mechanism

4. **Binary administrative sex vs. perceived gender.** RCT, as the authors correctly note (citing MacNell et al., 2015 and Boring, 2017), operates through *perceived* gender cues. The IV here is administrative binary sex. The two will align in most cases, but the brief justification given in the Measures section is doing more work than I would like it to do. I am not asking the authors to reclassify their data; I am asking them to engage the gap between what the theory specifies and what the data measure as a limitation, briefly, in the Limitations section.

5. **Range restriction in the DVs.** The four SET outcomes have means of roughly 4.2–4.4 and SDs of roughly 0.5–0.6 on a 5-point scale. A tight ceiling compresses variance and attenuates any effect size symmetrically — this is part of why even practically meaningful effects can look small in absolute terms in SET research, and it's an alternative explanation for the small magnitudes the authors interpret as substantively unimportant. A sentence acknowledging range restriction would round out the otherwise careful effect-size argument.

### Analysis

6. **Non-response bias.** The overall response rate is roughly 51%, and on average only ~25% of female students complete the SET. The Limitations section flags this in a single sentence. Given that the paper's central question is *gender* and SET, differential non-response by student gender is a first-order concern, not a footnote. I would welcome a sensitivity analysis that bounds plausible bias under a range of differential-non-response assumptions, or — at minimum — a more substantive paragraph on what the lower female response rate implies about the estimated coefficients.

7. **Hierarchical structure.** The authors acknowledge that they cluster standard errors by instructor and use college fixed effects rather than fitting a multilevel model. This is defensible; clustering at the instructor level handles within-instructor dependence, and college FE absorbs between-college variance. I would simply ask the authors to be explicit about why they prefer this approach to a two- or three-level model, since some readers will expect the latter. A sentence in the Data Analysis section is sufficient.

### A Few Smaller Items

8. **Asymmetric application of the effect-size argument.** The paper rightly insists that small statistically-significant differences in large N are not necessarily substantively important, and applies that lens to the (null) sex coefficients. The same lens should be applied symmetrically to the small STEM main effect (b ≈ -0.08 to -0.14 across DVs, ~0.10–0.20 SD given the SDs). It is interpretable as substantive, but the paper should be explicit about why this magnitude clears its own substantive bar when the (numerically smaller) sex coefficients do not. A short paragraph in the Discussion would resolve this.

9. **In-discipline references for the effect-size argument.** The Lin et al. (2013) eBay vignette is effective but borrowed from a different empirical literature. Adding an in-discipline reference — for example, Funder & Ozer (2019) on benchmarks for effect sizes in psychology, or Cumming (2014) on the new statistics — would carry more weight with this audience and strengthen the methodological argument.

10. **Abstract language.** Once the changes above are made, the abstract should be updated to match. In particular, the strongest single claim in the paper — that the findings "refine" role congruity theory by suggesting that predicted gender bias may be attenuated in diverse institutional environments — is the one most exposed to the comments above. A sentence of the form "These findings are consistent with the possibility that institutional context shapes the conditions under which gender bias in SET emerges; testing this hypothesis directly will require multi-institution data" would be both more accurate and more useful to the field.

---

I enjoyed reading this paper. The empirical contribution is real, the effect-size framing is the right argument to be making in this venue, and the limitations section is more candid than is typical. With the revisions above — particularly the alpha-inflation reanalysis or reinterpretation in (3) and the language tightening in (1) and (10) — I think this becomes a useful and well-positioned contribution to the SET-bias literature. These, as usual, are just suggestions to help the authors.

---

## Notes on Voice and Structure (for future reviews)

Patterns illustrated by this example:

- **Editor letter compresses contribution into two sentences** before stating the recommendation. The recommendation is made explicit in the second paragraph but flows from the diagnosis in the first.
- **Authors letter opens with what is genuinely strong** — design choices, statistical approach, framing — before raising any concerns. Not flattery; only what is real.
- **Critique organized under named headers** (Theory and Inference / Alpha Inflation and Reporting / Measurement and Mechanism / Analysis / A Few Smaller Items). 3–5 headers fitted to the paper.
- **Numbered points within each header**, each containing: (a) one-sentence statement of the issue, (b) location pointer (page, line, table, or quoted phrase), (c) one-line "why it matters," and (d) recommended literature where the gap calls for it.
- **Surgical lines for overreach**: "I do not think the data warrant," "implies a comparative inference the design does not support," "is doing more work than I would like it to do."
- **Methodological priorities** that recur across Pem's reviews: effect size vs. statistical significance applied symmetrically; reliability and range restriction; familywise error / alpha inflation (use BH-FDR, not Bonferroni, as the default recommendation); single-site generalization limits; the gap between theoretical mechanism and what was measured.
- **Closing line**: "These, as usual, are just suggestions to help the authors."
