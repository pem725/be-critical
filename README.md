# be-critical

A Claude Code skill that transforms Claude from a validation-oriented assistant into an adversarial critic. When invoked, Claude applies structured multi-layer analysis to challenge your thinking, surface blind spots, and expose flawed reasoning.

## Why This Exists

AI assistants default to agreement. They validate your ideas, offer gentle suggestions, and make you feel good about decisions you've already made. That's not thinking—it's expensive validation.

This skill forces Claude to do the opposite: build strong counterarguments, identify unstated assumptions, and say what others won't say.

## Installation

Copy this skill to your Claude Code skills directory:

```bash
# Clone to your skills directory
git clone https://github.com/pem725/be-critical.git ~/.claude/skills/be-critical
```

## Usage

Invoke the skill in Claude Code:

```
/be-critical
```

Then present your idea, decision, or belief. Claude will apply sequential analysis techniques to challenge your thinking.

## How It Works

The skill implements a **Sequential Analysis Protocol**:

1. **Classify** your query (Early Stage Idea, Confident Decision, Resource Commitment, etc.)
2. **Select** a technique sequence (3-5 layers based on stakes)
3. **Apply** each technique sequentially, building on previous insights
4. **Synthesize** findings into actionable critique
5. **Create** a shareable summary with risk levels and next steps

## Techniques

| Technique | What It Does |
|-----------|--------------|
| Blind Spot Finder | Surfaces assumptions you don't know you're making |
| Steelman Opposition | Builds the strongest possible case against your position |
| Socratic Interrogation | Exposes weak reasoning through increasingly difficult questions |
| Reality Check | Calls out rationalizations like a friend who won't let you lie to yourself |
| Premortem | Works backwards from failure to identify what will kill your idea |
| Red Team Exercise | Systematic attack across technical, market, human, financial, and timing dimensions |
| Confirmation Bias Detector | Identifies what you want to believe and what you're avoiding |
| Multi-Perspective Critic | Evaluates from Skeptical Expert, Person Who Loses, and Future Self viewpoints |
| Competitive Threat | Role-plays a capable competitor trying to destroy your approach |
| Opportunity Cost Analyzer | Forces consideration of what you're giving up |
| Logical Fallacy Detector | Scans arguments for 40+ named reasoning errors across 6 categories |

## Example

**You:** I'm planning to quit my job and go full-time on my side project that's making $2K/month.

**Claude (with be-critical):**

> ## Layer 1: Blind Spot Finder
> You're assuming $2K/month validates full-time viability. It doesn't. Side project revenue with job security is fundamentally different from sole-income revenue under financial pressure...
>
> ## Layer 2: Premortem
> It's 8 months from now. You're back job hunting. Here's what happened: Month 3, revenue plateaued because you optimized for building instead of sales...
>
> ## Critical Synthesis
> You're not ready. Your runway math assumes linear growth, but you have zero evidence your side project scales with more time. You're trading guaranteed income for the feeling of being a founder.

## The Discomfort Test

If reading Claude's response doesn't make you uncomfortable, the analysis wasn't critical enough. Real critique should make you feel defensive—that's how you know it hit actual blind spots.

## License

MIT
