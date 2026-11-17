# PM Brain OS

A portable, AI-native operating system for AI product leaders. Built on Claude Code. Travels with you across every role.

---

## What this is?

PM Brain OS is a structured thinking environment — not a template library, not a wiki, not a prompt collection. It is an operating system for how a PM leader thinks, communicates, and makes decisions, with Claude Code as the agentic orchestrator and execution layer.

**PORTABILITY PRINCIPLE** - The system is organized into three layers that separate what is permanently yours from what is specific to your current company. Switch roles: update the Company Layer, swap the Context Library, leave the Core Layer untouched. Your voice, your frameworks, your templates — they go with you.

---

## Architecture

### Layer diagram

```
┌─────────────────────────────────────────────────────────────────────┐
│                        YOU (The PM)                                 │
│         L7/L8 · AI-Native · Amazon · Expedia · AI Startups         │
└─────────────────────────────┬───────────────────────────────────────┘
                              │  Your brief, inputs, feedback
                              ▼
┌─────────────────────────────────────────────────────────────────────┐
│                    CLAUDE.md — ENTRY POINT                          │
│  Master orchestrator. Loads context in order, routes to the right   │
│  agent, enforces output standards across every workflow.            │
│                                                                     │
│  On every session start, Claude Code loads this file first.         │
│  Everything below runs through it.                                  │
└──────┬──────────────────────┬───────────────────────┬──────────────┘
       │ [1–3] Core Layer     │ [4] Template          │ [5] Company Layer
       ▼                      ▼                       ▼
┌─────────────────┐  ┌─────────────────┐  ┌──────────────────────────┐
│   core/         │  │  core/          │  │  company/                │
│                 │  │  templates/     │  │                          │
│  voice.md       │  │                 │  │  company_context.md      │
│  [Loaded 1st]   │  │  prd_template   │  │  goals.md                │
│  Tone, structure│  │  stakeholder_   │  │  stakeholders.md         │
│  calibration    │  │  update_        │  │  org_structure.md        │
│                 │  │  template       │  │                          │
│  career_        │  │  roadmap_       │  │  Swappable per role.     │
│  context.md     │  │  review_        │  │  Replace this folder     │
│  [Loaded 2nd]   │  │  template       │  │  when you switch jobs.   │
│  L7-L8 profile  │  │  research_      │  │  Core Layer untouched.   │
│                 │  │  synthesis_     │  └──────────────────────────┘
│  frameworks.md  │  │  template       │
│  [Loaded 3rd]   │  │                 │
│  RICE · JTBD    │  │  One loaded per │
│  Pyramid · DACI │  │  workflow type  │
└─────────────────┘  └─────────────────┘
                              │
                              │ [6] Context Library (selective)
                              ▼
              ┌───────────────────────────────┐
              │   context-library/            │
              │                               │
              │   research/   decisions/      │
              │                               │
              │   Loaded selectively —        │
              │   only what the task needs.   │
              │   Files > 12 months old are   │
              │   flagged before loading.     │
              └───────────────┬───────────────┘
                              │
                              │ CLAUDE.md classifies intent → routes
                              ▼
┌─────────────────────────────────────────────────────────────────────┐
│                         agents/                                     │
│                                                                     │
│  prd_agent.md              roadmap_review_agent.md                  │
│  research_synthesis_agent.md   metrics_callout_agent.md             │
│  stakeholder_update_agent.md   conflict_resolution_agent.md         │
│                            meeting_actions_agent.md                 │
│                                                                     │
│  CLAUDE.md routes here automatically based on your intent.         │
│  Ambiguous input → you choose. No match → inline or new agent.     │
└──────────────────────────────┬──────────────────────────────────────┘
                               │  Output
                               ▼
              ┌────────────────────────────────┐
              │  Output standards (enforced    │
              │  by CLAUDE.md on every run):   │
              │                                │
              │  ✓ Conclusions first           │
              │  ✓ Tradeoffs section required  │
              │  ✓ L7-L8 bar — no filler       │
              │  ✓ ~80K token budget enforced  │
              └────────────────┬───────────────┘
                               │  Calibration feedback
                               ▼
              ┌────────────────────────────────┐
              │  core/voice.md updated         │
              │  One sentence. Immediately.    │
              │  Confirmed inline.             │
              └────────────────────────────────┘
```
"Core Layer" is Portable

"Company Layer" is Swappable

"Project Layer" is by initiative

---

## The three layers explained

### Core Layer — permanent, yours forever

The Core Layer encodes the PM as a professional. It does not change between companies. It changes only when the PM grows — when their voice evolves, their frameworks sharpen, or feedback from outputs reveals a calibration gap.

**`voice.md`** is the most important file in the system. It defines how every output is written: tone, structure, what goes in every document regardless of type (spoiler: tradeoffs), and how the system learns from feedback. When a PM gives feedback on an output — "this was too cautious", "I needed more options surfaced" — that signal is written back into `voice.md`. The system calibrates over time rather than resetting.

**`career_context.md`** tells Claude what level of PM it is working with. At L7-L8, this means: don't explain basic concepts, don't over-hedge, write as if addressing a peer who will push back on anything that isn't sharp. This file also captures domain expertise (AI-native products, FAANG-scale execution, early-stage startups) so outputs are calibrated to the domains the PM actually operates in.

**`frameworks.md`** stores the PM's preferred analytical lenses: RICE for prioritization, Jobs-to-be-Done for user research, Pyramid Principle for communication, evaluation-first development and AI product flywheel for AI features. These are applied consistently across all outputs unless a specific project overrides them.

**`templates/`** holds the canonical document formats the PM returns to every time — PRD, stakeholder update, roadmap review, research synthesis. Each template is opinionated, not blank. They embed the structural choices the PM has already made (conclusions first, explicit tradeoffs section, open questions with owners) so the PM is not re-making those decisions for every document.

---

### Company Layer — swappable per role

The Company Layer is the context the PM needs to operate in a specific organization. It answers: who are we, what are we trying to do, who are the players, and how do decisions get made here?

When a PM joins a new company or switches teams, they replace this folder. The Core Layer is untouched. The AI immediately has the right company context without any reconfiguration of frameworks, voice, or templates.

**`company_context.md`** — mission, business model, competitive landscape, strategic priorities, cultural norms. The things that shape every product decision.

**`goals.md`** — current OKRs and quarterly focus. The lens through which all prioritization is evaluated.

**`stakeholders.md`** — the influence map. Who cares about what, how they prefer to receive information, where the tensions are.

**`org_structure.md`** — reporting lines, cross-functional team composition, and decision rights. Prevents outputs that misread who has authority to approve what.

---

### Context Library — per initiative, accumulates in a role

The Context Library is the knowledge layer for current work. It holds curated research syntheses and a decision log — not raw data, not notes, but processed insight that can be pulled directly into a prompt.

**`research/`** stores user research synthesis files in a consistent format. Each file is a finished synthesis — Jobs-to-be-Done lens applied, key findings extracted, open questions named. Research older than 12 months is reviewed for continued relevance before being loaded into a session.

**`decisions/`** stores one file per significant product decision: what was decided, what was not chosen, what would change the decision, and when it should be revisited. This prevents re-litigating settled questions and gives new team members (or a new AI session starting cold) instant context on why the product is the way it is.

---

## Workflow Agents

Each agent in `agents/` is a triggered workflow — a pre-configured prompt template that loads the right context files and runs a specific PM task. Agents are not chatbots. They are structured operations. `CLAUDE.md` routes to them automatically based on intent classification; you do not need to invoke them by name.

| Agent | Task | Key context loaded |
|-------|------|--------------------|
| `prd_agent.md` | Write a first-draft PRD | Core + Company + goals |
| `research_synthesis_agent.md` | Synthesize user research | Core + Company + research template |
| `stakeholder_update_agent.md` | Draft a stakeholder update | Core + Company + stakeholders |
| `roadmap_review_agent.md` | Prepare roadmap review narrative | Core + Company + roadmap template |
| `metrics_callout_agent.md` | Interpret and call out metrics | Core + Company goals |
| `conflict_resolution_agent.md` | Navigate stakeholder conflicts | Core + Company + stakeholders + org |
| `meeting_actions_agent.md` | Process meeting notes into actions | Core + Company |

Each agent file contains: the purpose of the workflow, the exact list of context files to load, a copy-paste trigger prompt with labeled inputs, and the expected output format.

AI models for Agentic workflows are chosen to balance token efficiency and output accuracy

---

## AI model

PM Brain OS is built on **Claude claude-opus-4-6** (Anthropic), accessed via Claude Code.

Claude claude-opus-4-6 is chosen for:
- **Extended thinking** — adaptive reasoning for complex PM problems (competitive strategy, conflict resolution, tradeoff analysis) that benefit from a longer reasoning pass before output
- **Large context window** — enough headroom to load multiple context files simultaneously alongside raw research or meeting notes
- **Instruction fidelity** — follows structured, multi-part prompts reliably without losing constraints mid-output

The system is designed to work with Claude Code's file-reading capabilities directly. `CLAUDE.md` acts as the master orchestrator — loaded automatically by Claude Code on every session start, it controls context load order, agent routing, and output standards without any manual configuration. No external orchestration layer is needed.

---

## Context design: how much is enough

A key architectural constraint is **what fits in a single prompt without degrading output quality**.

PM Brain OS is designed around a working context budget of approximately **60,000–80,000 tokens** per session. This accommodates:

- Full Core Layer: ~3,000–5,000 tokens (voice, career context, frameworks, one template)
- Company Layer: ~2,000–4,000 tokens (context, goals, stakeholders — depending on org complexity)
- One Context Library file: ~2,000–6,000 tokens (a research synthesis or decision log)
- Task input (meeting notes, raw data, brief): ~5,000–15,000 tokens
- Working room for output generation: ~20,000–40,000 tokens

**The design rule**: load what is relevant to the specific task, not everything in the library. The agent trigger prompts specify exactly which files to load — never "load everything". This keeps reasoning focused and prevents context dilution, where a model has too much information and begins making generic rather than grounded outputs.

For most PM tasks, loading the full Core Layer plus two Company Layer files plus one task-specific input is the right operating budget. Research synthesis sessions that involve large raw input sets may require dropping one Core Layer file (typically `frameworks.md`) to stay within the quality window.

**What does not scale**: dumping an entire Notion workspace, a full quarter of meeting notes, or a complete product spec history into a single session. The system is designed around curated, processed inputs — not firehose ingestion. The Context Library's job is to pre-process raw material into structured knowledge before it enters a prompt.

---

## Portability: using this across jobs and companies

The Core Layer is the PM's professional identity in file form. It is the thing that took years to develop and does not change when a company changes.

When you join a new company:

1. Archive the current `company/` folder and `context-library/` folder — they have value as a record of your prior role
2. Create a new `company/` folder using the templates as starting structure
3. Fill in `company_context.md`, `goals.md`, `stakeholders.md`, and `org_structure.md` from onboarding materials, your first 30 days of observation, and early stakeholder conversations
4. Begin building the `context-library/` as you run research and make decisions

The Core Layer is untouched. The AI immediately operates with your calibrated voice, your frameworks, and your templates in the new context.

This is the portability contract: **the system knows you; you just tell it where you are**.

---

## Feedback loop and calibration

PM Brain OS is not static. Every time the PM gives feedback on an output, it is a calibration signal.
╔═════════════════════════════════════════════════════════════════════╗
║                      FEEDBACK LOOP                                  ║
╠═════════════════════════════════════════════════════════════════════╣
║  "Too hedged"        →  voice.md Feedback Log updated              ║
║  "Missed constraint" →  frameworks.md updated                      ║
║  "Wrong exec tone"   →  stakeholder_map.md updated                 ║
║                                                                     ║
║  System gets sharper every session. This is the learning loop.     ║

**The loop:**

1. PM runs an agent and gets an output
2. PM provides feedback — "this was too hedged", "I needed the options more clearly separated", "the ask was buried"
3. The relevant file in the Core Layer is updated — usually `voice.md`, sometimes `frameworks.md`
4. The update records what changed and why, so the calibration is legible to a future session starting cold

This is the memory mechanism. The system does not rely on conversation history between sessions — it relies on explicit, structured knowledge in files. Each session starts with the same context, but that context gets sharper over time as calibrations accumulate.

---

## Critique: what it does well and where it can improve

### What works well!!

**Portability without configuration overhead.** Swapping the Company Layer takes minutes, not hours. The PM does not have to re-teach the system their style or preferences. The Core Layer carries it.

**Opinionated structure produces better outputs.** Blank templates produce generic outputs. The templates here embed the PM's existing decisions about structure — so the AI is filling in content within a proven frame rather than inventing structure from scratch.

**Tradeoffs as a first-class output.** Most AI-assisted PM tools produce confident, smooth outputs that paper over hard decisions. This system mandates a Tradeoffs section in every document. The PM gets the tension surfaced, not resolved for them.

**Calibration survives session resets.** Because calibration lives in files rather than conversation memory, the system does not degrade between sessions. A PM who has been using this for six months has a materially better-calibrated Core Layer than they did on day one.

**Agent specificity beats chat generality.** Each workflow agent loads only what is relevant and runs a specific operation. This produces sharper outputs than asking a general-purpose chat session to "help me write a PRD".

### What can improve??

**Context budget management is manual.** The PM decides what to load in each session. There is no automated relevance scoring or dynamic context selection. For PMs managing large context libraries, this becomes a judgment call every session. A future improvement would be an index layer that recommends which research or decision files are most relevant to the current task.
I ask the agent to summarize if the conversations goes beyond 15, open a new session paste the summarized version and then continue. This has helped me prevent context rot.

**The feedback loop requires PM discipline.** Calibration only happens if the PM takes the step of writing feedback back into `voice.md` or `frameworks.md`. This is not automatic. A PM under time pressure will skip it. The system would benefit from a lightweight post-session prompt: "Any feedback on this output? One sentence to update voice.md?"

**No automatic freshness management.** Research and company context files can go stale without a signal. A 14-month-old competitive landscape file loaded without review will produce confident but outdated analysis. The system needs a convention (currently: check dates manually) that could be improved with a lightweight staleness flag or review prompt.

**The Context Library grows without pruning.** Over a multi-year role, the decisions and research folders accumulate. There is no built-in archival or pruning workflow. Old decisions remain in the library and create noise unless the PM actively curates them.

**Template coverage is not yet complete.** The system has templates for PRDs, stakeholder updates, roadmap reviews, and research synthesis. Missing: launch readiness reviews, go-to-market briefs, executive briefings, and retrospective formats. These are planned, not shipped.

**Single-model dependency.** The system is currently designed around Claude claude-opus-4-6. A model version change or provider shift requires reviewing agent trigger prompts and potentially recalibrating `voice.md` for any behavioral differences in output style.


 ### The gap worth knowing and the reasons for this gap

  Right now there's no memory.md inside the PM Brain OS repo itself — no single file that says "here's what this system has learned and when." The calibration is distributed (voice.md, decisions/, research/)
  which is intentional for portability, but it means there's no single audit trail of how the system has evolved.

  If you wanted one, a core/calibration_log.md would be the right place — a running record of what changed in voice.md and why, dated. That would make the system's learning legible to a cold session or a new
  collaborator without having to read the diff history.

---

## Getting started

1. Fork or clone this repository
2. Fill in `core/voice.md` with your communication style and calibration preferences
3. Fill in `core/career_context.md` with your level, domain, and working style
4. Fill in `core/frameworks.md` with your preferred PM frameworks
5. Fill in `company/` files with your current company context
6. Open Claude Code and run your first agent by copying the trigger prompt from any file in `agents/`
7. After your first output, update `core/voice.md` with one calibration observation

The system compounds. The more sessions you run and calibrate, the sharper every subsequent output becomes.

---

## License

MIT. Use it, adapt it, carry it with you.
