---
layout: default
title: be-critical
description: A Claude Code skill that transforms AI from yes-man to adversarial critic
---

<nav style="background: #f6f8fa; padding: 1em; margin-bottom: 2em; border-radius: 6px;">
  <strong>Navigation:</strong>
  <a href="#about">About</a> ·
  <a href="#installation">Installation</a> ·
  <a href="#how-it-works">How It Works</a> ·
  <a href="#what-it-detects">Detection</a> ·
  <a href="#examples">Examples</a> ·
  <a href="#credits">Credits</a>
</nav>

# be-critical

**Stop getting validated. Start getting challenged.**

A Claude Code skill that transforms Claude from a validation-oriented assistant into an adversarial critic. When invoked, it applies structured multi-layer analysis to challenge your thinking, surface blind spots, and expose flawed reasoning.

[View on GitHub](https://github.com/pem725/be-critical) | [Download v0.2](https://github.com/pem725/be-critical/releases/tag/v0.2)

---

<h2 id="about">The Problem</h2>

AI assistants default to agreement. They validate your ideas, offer gentle suggestions, and make you feel good about decisions you've already made.

That's not thinking—it's **expensive validation**.

The conversations where AI pushes back are the ones that actually change how you think. The validation conversations? You forget them immediately.

### The Solution

This skill forces Claude to do the opposite:
- Build strong counterarguments
- Identify unstated assumptions
- Detect logical fallacies and cognitive biases
- Say what others won't say

**If reading the response doesn't make you uncomfortable, it wasn't critical enough.**

---

<h2 id="installation">Installation Guide</h2>

### Method 1: Claude.ai Settings (Easiest)

The simplest way to install this skill is through the Claude.ai web interface:

1. Download [be-critical-v0.2.zip](https://github.com/pem725/be-critical/releases/download/v0.2/be-critical-v0.2.zip)
2. Go to [claude.ai/settings/capabilities](https://claude.ai/settings/capabilities)
3. Scroll to the **Skills** section
4. Either:
   - Click **Add Skill** and select the zip file, or
   - **Drag and drop** the zip file directly onto the page
5. The skill is now available in your Claude conversations

**Using it:** Just type `/be-critical` in any Claude conversation and the skill will activate.

---

### Method 2: Claude Code CLI

If you use Claude Code (Anthropic's command-line interface), you can install the skill locally:

#### Prerequisites

You need Claude Code installed. If you don't have it:

```bash
npm install -g @anthropic-ai/claude-code
```

> **Don't have npm?** Download Node.js from [nodejs.org](https://nodejs.org/) first.

#### Install the Skill

**On Mac/Linux:**
```bash
mkdir -p ~/.claude/skills
cd ~/.claude/skills
git clone https://github.com/pem725/be-critical.git
```

**On Windows (PowerShell):**
```powershell
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.claude\skills"
cd "$env:USERPROFILE\.claude\skills"
git clone https://github.com/pem725/be-critical.git
```

> **Don't have git?** Download from [git-scm.com](https://git-scm.com/downloads)

#### Using the Skill

1. Start Claude Code by running `claude` in your terminal
2. Type `/be-critical` and press Enter
3. Claude will ask what kind of critique you need
4. Present your idea, decision, or question
5. Get challenged!

---

### Method 3: Manual Download

If you prefer not to use git:

1. Go to the [Releases page](https://github.com/pem725/be-critical/releases)
2. Download `be-critical-v0.2.zip`
3. Extract the zip file
4. Either:
   - **For Claude.ai:** Upload `Skill.md` at [claude.ai/settings/capabilities](https://claude.ai/settings/capabilities)
   - **For Claude Code:** Move the folder to `~/.claude/skills/be-critical`

---

### Troubleshooting

| Problem | Solution |
|---------|----------|
| Skill doesn't appear in Claude.ai | Refresh the page after uploading |
| "command not found: claude" | Claude Code isn't installed. Run `npm install -g @anthropic-ai/claude-code` |
| "command not found: git" | Git isn't installed. Download from [git-scm.com](https://git-scm.com/downloads) |
| "command not found: npm" | Node.js isn't installed. Download from [nodejs.org](https://nodejs.org/) |
| "/be-critical" not recognized in Claude Code | Restart Claude Code after installing the skill |

---

<h2 id="how-it-works">How It Works</h2>

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

<h2 id="what-it-detects">What It Detects</h2>

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

### Analysis Techniques

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

<h2 id="examples">Examples</h2>

### Example 1: Solar Panel Decision

> **Question**: Should I get solar panels installed on my house in Virginia? My house is shaded a bit.

> **Bottom Line**: **Don't proceed yet.** Get a professional shade analysis first. The phrase "shaded a bit" is too vague to commit $15,000+. If shade reduces production by more than 20%, the financial case collapses. Get data before deciding. *(Medium confidence)*

[Read full analysis →](https://github.com/pem725/be-critical/blob/main/examples/solar-panels.md)

---

### Example 2: Electric Vehicles vs ICE

> **Question**: Are electric vehicles really environmentally friendly compared to internal combustion or hybrid vehicles?

> **Bottom Line**: **Yes, but it's overstated.** EVs produce 50-70% fewer lifetime emissions than average ICE vehicles—the data is robust. However, the advantage shrinks significantly when compared to efficient hybrids, depends heavily on your regional grid mix, and ignores mining externalities. *(Medium-high confidence)*

[Read full analysis →](https://github.com/pem725/be-critical/blob/main/examples/ev-vs-ice.md)

---

### Example 3: Apple AI Investment

> **Question**: Will Apple successfully innovate and integrate AI into their products for another market run? Are they a good stock market bet?

> **Bottom Line**: **Probably yes on AI, but you're asking the wrong question.** Apple will integrate AI competently—they always do—but "successful market run" conflates product execution with stock returns. You're not betting on Apple's AI capability; you're betting the market is underestimating them. That's a harder case to make at a $3T+ valuation. *(Medium confidence)*

[Read full analysis →](https://github.com/pem725/be-critical/blob/main/examples/apple-ai-investment.md)

---

## Why I Built This

I kept having "conversations" with AI where every response was basically *"That's brilliant! Here's how to make your already-perfect idea even better!"*

And I get it. It feels good when AI validates your thinking. But if your AI assistant never pushes back on your ideas, you're not using it to think sharply. You're using it to feel better about decisions you've already made.

The goal isn't to be mean. The goal is to **surface truth**. You can get validation anywhere. The value is in seeing what you can't see and saying what others won't say.

Be the critic you actually need, not the cheerleader you can easily find.

---

<h2 id="credits">Credits</h2>

The adversarial prompting techniques in this skill were inspired by [AI Prompt Hackers](https://www.aiprompthackers.com/p/10-prompts-that-force-ai-to-challenge) and their excellent article "10 Prompts That Force AI to Challenge Your Thinking."

---

## License

MIT

---

<nav style="background: #f6f8fa; padding: 1em; margin-top: 2em; border-radius: 6px; text-align: center;">
  <a href="#about">About</a> ·
  <a href="#installation">Installation</a> ·
  <a href="#how-it-works">How It Works</a> ·
  <a href="#what-it-detects">Detection</a> ·
  <a href="#examples">Examples</a> ·
  <a href="#credits">Credits</a>
  <br><br>
  <a href="https://github.com/pem725/be-critical">GitHub</a> ·
  <a href="https://github.com/pem725/be-critical/releases">Releases</a> ·
  <a href="https://github.com/pem725/be-critical/issues">Issues</a>
</nav>
