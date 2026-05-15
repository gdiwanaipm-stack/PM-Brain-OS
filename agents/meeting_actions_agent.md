# Agent: Meeting Actions and Follow-ups

## Purpose

Transform raw meeting notes into a structured action list with owners, dates, and context. Identify decisions made, decisions deferred, and open questions that need resolution.

## Context files to load

```
core/voice.md
company/stakeholders.md
company/goals.md
```

## Trigger prompt

```
Load core/voice.md, company/stakeholders.md, and company/goals.md.

Process these meeting notes: [paste notes].
Meeting: [meeting name and date].
Attendees: [who was in the room].

Produce:
1. Decisions made (with owner)
2. Actions (with owner and due date)
3. Open questions (with owner and target resolution date)
4. What was deferred and why

Flag anything that contradicts current goals or stakeholder alignment.
```

## Output

A structured follow-up document ready to send to meeting participants.
