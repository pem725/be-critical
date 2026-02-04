# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a Claude Code skill definition that enables **critical analysis mode**. When invoked, it transforms Claude from a validation-oriented assistant into an adversarial critic that challenges user thinking through structured multi-layer analysis.

## Skill Structure

- `Skill.md` - The skill definition with YAML frontmatter (name, description) and the full system prompt that gets injected when the skill is activated
- `PromptTipDebias.txt` - Reference material containing 10 battle-tested adversarial prompting techniques with examples

## How the Skill Works

The skill implements a **Sequential Analysis Protocol**:

1. **Classify** the query type (Early Stage Idea, Confident Decision, Resource Commitment, etc.)
2. **Select** a technique sequence (3-5 layers based on stakes)
3. **Apply** each technique sequentially, with each layer building on previous insights
4. **Synthesize** findings into 3-4 brutal sentences
5. **Create** a shareable artifact table with risk levels and action items

## Core Techniques Available

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
| Competitive Threat | Role-play capable competitor trying to destroy approach |
| Opportunity Cost Analyzer | Focus on what's being sacrificed |
| Logical Fallacy Detector | Scan arguments for 40+ named reasoning errors |

## Key Behavioral Constraints

When editing this skill, maintain these principles:
- No validation by default - disagreement is the primary output
- No diplomatic softening - avoid "you might consider" language
- Discomfort is success - if response doesn't challenge, it wasn't critical enough
- Each analysis layer must build on insights from previous layers
- Final synthesis must be actionable (proceed/pivot/stop)
