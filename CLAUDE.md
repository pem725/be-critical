# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a Claude Code skill definition that enables **critical analysis mode**. When invoked, it transforms Claude from a validation-oriented assistant into an adversarial critic that challenges user thinking through structured multi-layer analysis.

## Skill Structure

- `Skill.md` - The skill definition with YAML frontmatter (name, description) and the full system prompt
- `PromptTipDebias.txt` - Reference material containing adversarial prompting techniques with examples
- `README.md` - User-facing documentation

## How the Skill Works

### 1. Mode Selection (One Question)
On invocation, asks user to select analysis mode:
- 🔍 Stress test reasoning → Fallacy + Bias detection
- 💀 Find holes in plan → Blind spots + Premortem + Red Team
- ⚔️ Argue both sides → Debate mode with verdict
- 🔬 Full analysis → Everything

### 2. Sequential Analysis Protocol
1. **Classify** the query type (Early Stage Idea, Confident Decision, etc.)
2. **Select** technique sequence (3-5 layers based on stakes)
3. **Apply** each technique sequentially, building on previous insights
4. **Synthesize** findings into brutal 3-4 sentence summary
5. **Create** shareable artifact with risk levels and actions

## Detection Capabilities

### Logical Fallacies (40+)
Organized into 6 categories with detection signals:
- Relevance (Ad Hominem, Appeal to Authority, Red Herring, etc.)
- Presumption (False Dilemma, Slippery Slope, No True Scotsman, etc.)
- Causal (Post Hoc, Correlation ≠ Causation, Reverse Causation, etc.)
- Generalization (Hasty Generalization, Survivorship Bias, Cherry Picking, etc.)
- Structural (Straw Man, False Equivalence, Equivocation, etc.)
- Psychological (Sunk Cost, Bandwagon, Appeal to Ignorance, etc.)

### Cognitive Biases (20+)
Organized into 3 categories:
- Decision-Making (Anchoring, Planning Fallacy, Overconfidence, etc.)
- Social/Self-Perception (Fundamental Attribution Error, Halo Effect, etc.)
- Information Processing (Confirmation Bias, Hindsight Bias, Base Rate Neglect, etc.)

## Core Techniques

| Technique | Purpose |
|-----------|---------|
| Blind Spot Finder | Surface unstated assumptions |
| Steelman Opposition | Build strongest counterargument |
| Socratic Interrogation | Expose weak reasoning via questions |
| Reality Check | Call out rationalizations directly |
| Premortem | Work backwards from failure |
| Red Team Exercise | Systematic attack across 5 dimensions |
| Confirmation Bias Detector | Identify what user wants to believe |
| Multi-Perspective Critic | Evaluate from Expert/Loser/Future Self views |
| Competitive Threat | Role-play competitor trying to destroy approach |
| Opportunity Cost Analyzer | Focus on what's being sacrificed |
| Logical Fallacy Detector | Scan for 40+ named reasoning errors |
| Cognitive Bias Detector | Identify systematic thinking errors |
| Debate Mode | Argue both sides, find crux, deliver verdict |
| Argument Mapper | Visualize premise→conclusion structure |

## Key Behavioral Constraints

When editing this skill, maintain these principles:
- No validation by default - disagreement is the primary output
- No diplomatic softening - avoid "you might consider" language
- Discomfort is success - if response doesn't challenge, it wasn't critical enough
- Each analysis layer must build on insights from previous layers
- Name specific fallacies/biases, don't just say "flawed logic"
- Final synthesis must be actionable (proceed/pivot/stop)
