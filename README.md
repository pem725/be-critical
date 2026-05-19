# be-critical

**[View Documentation Site](https://pem725.github.io/be-critical/)**

A Claude Code skill that transforms Claude from a validation-oriented assistant into an adversarial critic. When invoked, Claude applies structured multi-layer analysis to challenge your thinking, surface blind spots, and expose flawed reasoning.

## Why This Exists

AI assistants default to agreement. They validate your ideas, offer gentle suggestions, and make you feel good about decisions you've already made. That's not thinking—it's expensive validation.

This skill forces Claude to do the opposite: build strong counterarguments, identify unstated assumptions, and say what others won't say.

## Installation

### Easiest: Claude.ai Settings

1. Download [be-critical-v0.3.zip](https://github.com/pem725/be-critical/releases/download/v0.3/be-critical-v0.3.zip)
2. Go to [claude.ai/settings/capabilities](https://claude.ai/settings/capabilities)
3. Drag and drop the zip file onto the page, or click **Add Skill** and select it
4. Done! Type `/be-critical` in any conversation.

### Alternative: Claude Code CLI

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/pem725/be-critical.git ~/.claude/skills/be-critical
```

See the [full installation guide](https://pem725.github.io/be-critical/#installation) for detailed instructions.

## Usage

Invoke the skill in any Claude conversation:

```
/be-critical
```

Claude will ask one question to focus the analysis:

| Mode | What It Does |
|------|-------------|
| 🔍 **Stress test my reasoning** | Scans for logical fallacies and cognitive biases |
| 💀 **Find holes in my plan** | Identifies blind spots, failure modes, and what will kill your idea |
| ⚔️ **Argue both sides** | Builds strongest case FOR and AGAINST, then identifies which holds up |
| 🔬 **Full analysis** | All of the above |

Then present your idea. Analysis runs automatically.

## What It Detects

### Logical Fallacies (40+)

| Category | Examples |
|----------|----------|
| Relevance | Ad Hominem, Appeal to Authority, Red Herring, Tu Quoque |
| Presumption | False Dilemma, Begging the Question, Slippery Slope, No True Scotsman |
| Causal | Post Hoc, Correlation ≠ Causation, Reverse Causation |
| Generalization | Hasty Generalization, Cherry Picking, Survivorship Bias |
| Structural | Straw Man, False Equivalence, Equivocation |
| Psychological | Sunk Cost, Bandwagon, Appeal to Ignorance |

### Cognitive Biases (20+)

| Category | Examples |
|----------|----------|
| Decision-Making | Anchoring, Loss Aversion, Planning Fallacy, Overconfidence |
| Social/Self-Perception | Fundamental Attribution Error, Halo Effect, Authority Bias |
| Information Processing | Confirmation Bias, Hindsight Bias, Base Rate Neglect |

## Analysis Techniques

| Technique | What It Does |
|-----------|--------------|
| Blind Spot Finder | Surfaces assumptions you don't know you're making |
| Steelman Opposition | Builds the strongest possible case against your position |
| Socratic Interrogation | Exposes weak reasoning through increasingly difficult questions |
| Reality Check | Calls out rationalizations like a friend who won't let you lie to yourself |
| Premortem | Works backwards from failure to identify what will kill your idea |
| Red Team Exercise | Systematic attack across technical, market, human, financial, and timing dimensions |
| Logical Fallacy Detector | Names specific reasoning errors and shows why they invalidate the argument |
| Cognitive Bias Detector | Identifies systematic thinking errors distorting perception |
| Debate Mode | Argues both sides, finds the crux, delivers a verdict |
| Argument Mapper | Visualizes premise→conclusion structure and attacks weakest links |

## Two-Stage Manuscript Review Protocol

For peer review of academic manuscripts, `be-critical` runs a specialized two-stage workflow defined in [`manuscript_review_protocol.md`](manuscript_review_protocol.md).

**Pre-flight** — Assess the target journal (tier, indexing, audience, typical methodological standard). Critique severity is calibrated to the journal's published bar, not to top general-science venues.

**Stage 1 — Summary, Logic Model, Questions.** Read the paper, then produce a single markdown artifact containing:
- Plain-language summary of the contribution
- Verbatim research questions / hypotheses
- A Mermaid logic model showing theory → predictions → design → measures → analysis → findings → claims, with explicit "inferential leap" branches where the chain skips a step
- Evidence map (claim → evidence cited → strength)
- 5–10 categorized provocations (logical / evidential / framing / structural)
- 3–6 targeted questions for the human reviewer (verdict instinct, severity dials, field-specific calls)

The protocol then **stops** and waits for the reviewer's answers. The Stage 1 artifact is neutral-to-mildly-skeptical inventory, not a verdict.

**Stage 2 — Review in the reviewer's voice.** Using the reviewer's answers to calibrate severity and priority, produce a review in two-letter format:
- *To Editor:* short, compresses the paper's contribution into two sentences, conveys recommendation through tone, flags reviewer calibration if needed
- *To Authors:* opens with what's genuinely strong, then 3–5 named-header sections with numbered points (location pointer + why it matters + recommended literature where useful), closes constructively

See [`examples/manuscript-review-stage2.md`](examples/manuscript-review-stage2.md) for a worked example.

## Example: Debate Mode

**You:** Should I pivot from B2B to B2C?

**Claude:**

> ## The Case FOR Pivoting to B2C
> - Larger addressable market (100x potential customers)
> - Faster feedback loops for product iteration
> - Brand building creates long-term moat
>
> ## The Case AGAINST Pivoting to B2C
> - Customer acquisition costs 5-10x higher
> - Your team has zero consumer marketing experience
> - B2B revenue is predictable; B2C is volatile
>
> ## The Crux
> The debate hinges on: Can you acquire B2C customers profitably before runway ends?
>
> ## Verdict
> **Winner**: AGAINST with high confidence
>
> Your current B2B traction is real. Pivoting throws away validated demand to chase a market where you have no competitive advantage and no relevant experience.
>
> **However**, if you've found a B2C distribution channel with <$5 CAC, then FOR would be correct.

## The Discomfort Test

If reading Claude's response doesn't make you uncomfortable, the analysis wasn't critical enough. Real critique should make you feel defensive—that's how you know it hit actual blind spots.

## Examples

See the [examples/](examples/) folder for detailed walkthroughs:

- [Solar Panel Decision](examples/solar-panels.md) - Evaluating whether to install solar panels on a shaded house in Virginia
- [Electric Vehicles vs ICE](examples/ev-vs-ice.md) - Analyzing environmental claims about electric vehicles
- [Apple AI Investment](examples/apple-ai-investment.md) - Full analysis of Apple's AI future and stock potential
- [Retirement Investment](examples/retirement-investment.md) - How be-critical protects you from bad financial advice (includes a privacy-preserving template)

## Credits

The adversarial prompting techniques in this skill were inspired by [AI Prompt Hackers](https://www.aiprompthackers.com/p/10-prompts-that-force-ai-to-challenge) and their excellent article "10 Prompts That Force AI to Challenge Your Thinking."

## License

MIT
