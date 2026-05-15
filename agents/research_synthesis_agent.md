# Agent: User Research Synthesis

## Purpose

Transform raw research input (interview notes, survey data, usability findings) into a structured synthesis using the PM's preferred framework and template. Surface the Jobs-to-be-Done, key tensions, and open questions.

## Context files to load

```
core/voice.md
core/career_context.md
core/frameworks.md
core/templates/research_synthesis_template.md
company/company_context.md
```

## Trigger prompt

```
Load core/voice.md, core/career_context.md, core/frameworks.md, core/templates/research_synthesis_template.md, and company/company_context.md.

Then synthesize the following research: [paste raw notes or attach file].

Research question: [what were we trying to learn?]
Participant profile: [who did we talk to?]

Use the research synthesis template. Apply Jobs-to-be-Done as the primary lens. Surface what surprised us, what we still don't know, and the tradeoffs in how we interpret the data. Write at L7 bar.
```

## Output

A synthesis document saved to `context-library/research/YYYY-MM_[study-name].md`.
