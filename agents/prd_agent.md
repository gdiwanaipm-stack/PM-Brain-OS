# Agent: PRD Generator

## Purpose

Produce a first-draft PRD calibrated to L7-L8 standards, using the PM's preferred template and voice, grounded in the current company context and goals.

## Context files to load

```
core/voice.md
core/career_context.md
core/frameworks.md
core/templates/prd_template.md
company/company_context.md
company/goals.md
```

## Trigger prompt

```
Load core/voice.md, core/career_context.md, core/frameworks.md, core/templates/prd_template.md, company/company_context.md, and company/goals.md.

Then write a PRD for: [feature or initiative name].

Problem context: [1-2 sentences on the user problem or opportunity].
Key constraints: [any known constraints — timeline, platform, team size].
Success looks like: [what metric or outcome defines success].

Use the PRD template. Include a Tradeoffs section. Write at L7 bar — strategic, opinionated, no filler.
```

## Output

A complete draft PRD saved to `context-library/[initiative-slug]/prd_v1.md`.

## Calibration note

If the PM provides feedback on the output, update `core/voice.md` with what changed and why.
