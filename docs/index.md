---
layout: default
title: be-critical
description: A Claude Code skill that transforms AI from yes-man to adversarial critic
---

# be-critical

**Stop getting validated. Start getting challenged.**

A Claude Code skill that transforms Claude from a validation-oriented assistant into an adversarial critic. When invoked, it applies structured multi-layer analysis to challenge your thinking, surface blind spots, and expose flawed reasoning.

[View on GitHub](https://github.com/pem725/be-critical) | [Download v0.2](https://github.com/pem725/be-critical/releases/tag/v0.2)

---

## The Problem

AI assistants default to agreement. They validate your ideas, offer gentle suggestions, and make you feel good about decisions you've already made.

That's not thinking—it's **expensive validation**.

The conversations where AI pushes back are the ones that actually change how you think. The validation conversations? You forget them immediately.

## The Solution

This skill forces Claude to do the opposite:
- Build strong counterarguments
- Identify unstated assumptions
- Detect logical fallacies and cognitive biases
- Say what others won't say

**If reading the response doesn't make you uncomfortable, it wasn't critical enough.**

---

## How It Works

### 1. One Question to Focus

When you invoke `/be-critical`, Claude asks one question:

| Mode | What It Does |
|------|-------------|
| 🔍 **Stress test my reasoning** | Scans for logical fallacies and cognitive biases |
| 💀 **Find holes in my plan** | Identifies blind spots, failure modes, and what will kill your idea |
| ⚔️ **Argue both sides** | Builds strongest case FOR and AGAINST, then delivers verdict |
| 🔬 **Full analysis** | All of the above |

### 2. BLUF First

Every analysis leads with **Bottom Line Up Front**:

```
## BLUF (Bottom Line Up Front)

**Question**: Should I quit my job to pursue my startup?

**Bottom Line**: **Not yet.** Your $2K/month side revenue doesn't validate
full-time viability. You're trading guaranteed income for the feeling of
being a founder. Get to $5K/month with a clear growth trajectory first.
(Medium confidence)
```

No buried ledes. The verdict comes first; supporting analysis follows.

### 3. Multi-Layer Analysis

The skill applies 3-5 techniques in sequence, where each layer reveals what previous ones missed:

- **Layer 1** reveals you're assuming a problem exists
- **Layer 2** shows you're optimizing for feeling productive over validating demand
- **Layer 3** identifies this is the third time you've done this pattern
- **Layer 4** exposes you're afraid of sales conversations so you hide in building

By Layer 4, you've gone from "some risks" to "here's the psychological pattern that keeps sabotaging you."

---

## What It Detects

### 40+ Logical Fallacies

| Category | Examples |
|----------|----------|
| Relevance | Ad Hominem, Appeal to Authority, Red Herring, Tu Quoque |
| Presumption | False Dilemma, Begging the Question, Slippery Slope, No True Scotsman |
| Causal | Post Hoc, Correlation ≠ Causation, Reverse Causation |
| Generalization | Hasty Generalization, Cherry Picking, Survivorship Bias |
| Structural | Straw Man, False Equivalence, Equivocation |
| Psychological | Sunk Cost, Bandwagon, Appeal to Ignorance |

### 20+ Cognitive Biases

| Category | Examples |
|----------|----------|
| Decision-Making | Anchoring, Planning Fallacy, Overconfidence, Loss Aversion |
| Social/Self-Perception | Fundamental Attribution Error, Halo Effect, Authority Bias |
| Information Processing | Confirmation Bias, Hindsight Bias, Base Rate Neglect |

---

## Analysis Techniques

| Technique | What It Does |
|-----------|--------------|
| **Blind Spot Finder** | Surfaces assumptions you don't know you're making |
| **Steelman Opposition** | Builds the strongest possible case against your position |
| **Socratic Interrogation** | Exposes weak reasoning through increasingly difficult questions |
| **Reality Check** | Calls out rationalizations like a friend who won't let you lie to yourself |
| **Premortem** | Works backwards from failure to identify what will kill your idea |
| **Red Team Exercise** | Systematic attack across technical, market, human, financial, and timing dimensions |
| **Logical Fallacy Detector** | Names specific reasoning errors and shows why they invalidate the argument |
| **Cognitive Bias Detector** | Identifies systematic thinking errors distorting perception |
| **Debate Mode** | Argues both sides, finds the crux, delivers a verdict |
| **Argument Mapper** | Visualizes premise→conclusion structure and attacks weakest links |

---

## Examples

### Example 1: Solar Panel Decision

> **Question**: Should I get solar panels installed on my house in Virginia? My house is shaded a bit.

> **Bottom Line**: **Don't proceed yet.** Get a professional shade analysis first. The phrase "shaded a bit" is too vague to commit $15,000+. If shade reduces production by more than 20%, the financial case collapses. Get data before deciding. *(Medium confidence)*

[Read full analysis →](https://github.com/pem725/be-critical/blob/main/examples/solar-panels.md)

### Example 2: Electric Vehicles vs ICE

> **Question**: Are electric vehicles really environmentally friendly compared to internal combustion or hybrid vehicles?

> **Bottom Line**: **Yes, but it's overstated.** EVs produce 50-70% fewer lifetime emissions than average ICE vehicles—the data is robust. However, the advantage shrinks significantly when compared to efficient hybrids, depends heavily on your regional grid mix, and ignores mining externalities. *(Medium-high confidence)*

[Read full analysis →](https://github.com/pem725/be-critical/blob/main/examples/ev-vs-ice.md)

---

## Installation

```bash
git clone https://github.com/pem725/be-critical.git ~/.claude/skills/be-critical
```

Then invoke in Claude Code:

```
/be-critical
```

---

## Why I Built This

I kept having "conversations" with AI where every response was basically *"That's brilliant! Here's how to make your already-perfect idea even better!"*

And I get it. It feels good when AI validates your thinking. But if your AI assistant never pushes back on your ideas, you're not using it to think sharply. You're using it to feel better about decisions you've already made.

The goal isn't to be mean. The goal is to **surface truth**. You can get validation anywhere. The value is in seeing what you can't see and saying what others won't say.

Be the critic you actually need, not the cheerleader you can easily find.

---

## Credits

The adversarial prompting techniques in this skill were inspired by [AI Prompt Hackers](https://www.aiprompthackers.com/p/10-prompts-that-force-ai-to-challenge) and their excellent article "10 Prompts That Force AI to Challenge Your Thinking."

---

## License

MIT

---

<p style="text-align: center; color: #666; margin-top: 3em;">
  <a href="https://github.com/pem725/be-critical">GitHub</a> ·
  <a href="https://github.com/pem725/be-critical/releases">Releases</a> ·
  <a href="https://github.com/pem725/be-critical/issues">Issues</a>
</p>
