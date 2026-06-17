# GLOSSARY.md — Learn BMAD

> Plain-English definitions, defined the first time the course leans on them. If a term
> isn't here and isn't in `SOURCE.md`, the instructor points you to the official docs
> rather than guessing.

| Term | In plain English | First used | Source |
| --- | --- | --- | --- |
| **BMAD Method** | An AI-driven way to build software that uses specialist AI agents, guided workflows, and planning that scales to the job — from a bug fix to a platform. ("Build More, Architect Dreams.") | M1 | SOURCE §0 |
| **Vibe coding** | Handing a big, vague request to one AI in one long chat and hoping. The thing BMAD is the antidote to. | M1 | SOURCE §1 |
| **Phase** | One of BMAD's four stages of a build: Analysis, Planning, Solutioning, Implementation. | M2 | SOURCE §2 |
| **PRD** | Product Requirements Document — the "what we're building and why" document, produced in the Planning phase. | M2/M4 | SOURCE §2 |
| **Analysis** | Phase 1 — thinking clearly about the problem before committing (brainstorming, research). Optional but sharpens everything. | M4 | SOURCE §2.1 |
| **Solutioning** | Phase 3 — deciding *how* to build it and breaking it into units of work. | M5 | SOURCE §2.3 |
| **Architecture** | The set of technical decisions for a build (e.g. "use GraphQL for all APIs"), written down so every agent follows the same plan. | M5 | SOURCE §2.3 |
| **ADR** | Architecture Decision Record — a short note capturing one technical decision and why it was made. | M5 | SOURCE §2.3 |
| **Epic** | A big chunk of work that breaks down into smaller stories. | M5 | SOURCE §2.3 |
| **Story** | One small, implementable unit of work — the thing a developer builds in one go. | M5/M6 | SOURCE §2.3 |
| **Readiness gate** | A pre-build check (`check-implementation-readiness`) that returns PASS / CONCERNS / FAIL before you start coding. | M5 | SOURCE §2.3 |
| **Implementation** | Phase 4 — actually building it, one story at a time, each in a fresh chat. | M6 | SOURCE §2.4 |
| **The build cycle** | The repeating Implementation loop: create-story → dev-story → code-review, then a retrospective per epic. | M6 | SOURCE §2.4 |
| **Fresh chat per workflow** | The discipline of running each workflow in its own chat so stale context doesn't leak between steps. | M6 | SOURCE §7 |
| **Dev Loop Automation** | Running the build cycle with less hand-holding — a V6 roadmap item, partly "coming soon." | M6 | SOURCE §2.4 |
| **Agent** | A specialized AI persona with a role — e.g. Analyst (Mary), PM (John), Architect (Winston), Developer (Amelia). | M3 | SOURCE §3 |
| **Party Mode** | Your whole AI team in one chat, debating in character — great for big decisions and retros. | M3 | SOURCE §3 |
| **Quick Dev** | The single-workflow fast path for small changes: clarify → plan → implement → review. | M7 | SOURCE §4 |
| **Scale-adaptive** | BMAD's idea that you apply as much or as little process as the size of the change deserves. | M7 | SOURCE §4 |
| **Human-in-the-loop** | The points where a human steps in to decide. BMAD spends these on high-value moments and automates the rest. | M7 | SOURCE §4 |
| **BMad-Help** | The "front door" skill that inspects your project and tells you what to do next. It also runs automatically at the end of every workflow. | M8 | SOURCE §5 |
| **Module (BMAD)** | An optional add-on to the core method: BMM, CIS, GDS, TEA, BMB. (Not the same as a *course* module.) | M8 | SOURCE §6 |
| **Adversarial review** | A review where the reviewer *must* find issues — breaks "looks good to me" rubber-stamping. | Background concept | SOURCE §7 |
| **BMad Builder (BMB)** | The "meta-module" you use to *extend BMAD itself* — build your own agents, skills, and modules with guided assistance, then share them. | M10/M11 | SOURCE §6.5 |
| **Skill** | A self-contained capability the AI can run; in BMAD, agent skills (load a persona) or workflow skills (run a process). Built on the open Agent Skills standard, so they work across 40+ tools. | M11 | SOURCE §6, §6.5 |
| **Persistent memory** | What a BMB agent remembers and refines *across sessions* so it keeps improving — the "self-learning"/companion layer. Distinct from static persistent_facts. | M10 | SOURCE §6.5 |
| **Persistent facts** | Static facts you hand an agent up front (org rules, preferences, file refs). You edit them; they don't evolve on their own. | M10 | SOURCE §6.5 |
| **bmad-customize** | The helper for *tailoring an existing* agent/workflow via TOML overrides (no new agent). Build new = BMB; tweak existing = this. | M10 | SOURCE §6.5 |

## Explain-back prompts

- "BMAD in my own words": an AI build method that plans first and uses specialists, so I
  stop winging it.
- "Why phases?": so vague thinking can't quietly wreck everything downstream.
- "Quick-dev vs full method?": small job, light process; big job, more structure.
