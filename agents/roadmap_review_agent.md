# Agent: Roadmap Review

## Purpose

Prepare a roadmap review deck narrative, grounded in company goals and the PM's strategic framing. Outputs a structured narrative that can be translated into slides.

## Context files to load

```
core/voice.md
core/career_context.md
core/frameworks.md
core/templates/roadmap_review_template.md
company/company_context.md
company/goals.md
company/stakeholders.md
```

## Trigger prompt

```
Load core/voice.md, core/career_context.md, core/frameworks.md, core/templates/roadmap_review_template.md, company/company_context.md, company/goals.md, and company/stakeholders.md.

Prepare a roadmap review for Q[X] [YYYY].
Current commitments: [list what the team is shipping this quarter].
Next quarter candidates: [list what is under consideration].
Audience: [who will be in the room].
Key tension to surface: [what is the hardest tradeoff in this roadmap].

Use Now / Next / Later structure. Explicitly call out what is not on the roadmap and why. Include a Tradeoffs section. Write at L7 bar.
```

## Output

A narrative document structured for executive presentation, saved to `context-library/roadmap/Q[X]-[YYYY]-review.md`.
