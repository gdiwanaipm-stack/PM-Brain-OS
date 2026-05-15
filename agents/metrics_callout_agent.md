# Agent: Metrics Callout

## Purpose

Interpret a set of metrics and produce a crisp callout that explains what the numbers mean, what they imply for product decisions, and what the PM should watch next.

## Context files to load

```
core/voice.md
core/career_context.md
core/frameworks.md
company/goals.md
```

## Trigger prompt

```
Load core/voice.md, core/career_context.md, core/frameworks.md, and company/goals.md.

Interpret the following metrics: [paste data or describe the numbers].
Context: [what initiative or feature do these metrics belong to? What was expected?]

Surface: what the numbers tell us, what they don't tell us, what action they suggest, and what the key tradeoff is in how we interpret them.

Write at L7 bar. Conclusions first.
```

## Output

A concise callout (under 400 words) ready to paste into a stakeholder update or leadership review.
