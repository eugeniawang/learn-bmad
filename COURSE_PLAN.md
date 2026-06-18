# COURSE_PLAN.md — Learn BMAD (for Beginners)

Planning + validation artifact. The course this describes lives at the repo root and
is delivered through **Claude Code** (`CLAUDE.md` is the instructor).

## Identity & promise

- **Course:** Learn BMAD — the Method, for People Who Are Learning to Build.
- **One-line promise:** Understand *why* the BMAD Method exists and *how* its workflow
  works — well enough to point your own build through it — without drowning in setup.
- **Vibe:** fun, lighthearted, wry. A buffet, not a lecture hall.

## Goal lens

- **Goal type:** general learning / understanding (topic + source led), grounded in one
  real thing the learner wants to build.
- **Learner goals (what success looks like):**
  1. Explain, in plain words, what the BMAD Method is and *why* it beats one-chat "vibe
     coding."
  2. Name the four phases (Analysis → Planning → Solutioning → Implementation) and say
     what each is *for*.
  3. Decide *how much* BMAD a given job needs (quick-dev vs full method) — including
     when **not** to use heavy process.
  4. Map their own build idea onto the BMAD workflow.
- **Out of scope:** install/config mechanics; senior-dev depth; exam prep; writing code;
  exhaustive per-workflow command references (we point to the docs for those).
- **Capstone / proof:** a one-page "BMAD plan" for the learner's own build, in
  `MY_BUILD.md` — phases identified, rigor right-sized, agents and next step named.

## Audience

Beginners who are learning to build — not senior engineers. People who feel the chaos
of "just ask the AI and hope," and want a solid, repeatable scaffolding. Comfortable
chatting with an AI assistant; not expected to know agile, PRDs, or architecture.

## Delivery & practice environment

- **Delivery:** Claude Code (`CLAUDE.md` adapter). Single runtime.
- **Practice environment:** the Claude Code conversation itself. "Doing" = making real
  judgment calls on the learner's own build, predicting-then-revealing, role-playing the
  agents, and reading real BMAD docs/repo pages — not writing code.

## Navigation — NON-SEQUENTIAL by design (key decision)

Per the course owner: modules are a **pick-your-own buffet**, not a 1→9 march. The
default navigation mode is **flexible**. A learner can jump straight to, say, "the dev
loop" or "right-sizing" and learn it standalone. Each module is written to stand alone
(its own quick context primer), with light "if you liked this, try…" cross-links.
A recommended order exists for anyone who wants a guided path, but it is opt-in.

## Module map (12 short, standalone modules)

> Note: no per-module time estimates anywhere in the course — by owner decision, time
> predictions on modules aren't useful. The active-time *tracker* (which measures real
> time spent) stays; up-front duration guesses do not.

Grouped into loose tracks (used as "phases" on the landing page). Order is a
*suggestion*, not a requirement.

**Track 1 · Foundations** (the why)
1. **Why BMAD Exists** — vibe-coding pain → the five beliefs of the method.
2. **The Four-Phase Map** — the whole journey at a glance; what each phase is for.

**Track 2 · Your AI Crew**
3. **Meet Your AI Crew** — specialized agents vs one generalist; Party Mode.

**Track 3 · The Method, Up Close**
4. **Think First** — Analysis & Planning; why vagueness compounds; the PRD.
5. **Decide How** — Solutioning; explicit decisions; epics, stories, the readiness gate.
6. **Ship It** — Implementation; the story cycle; fresh chats; review; retro; the dev loop.

**Track 4 · Working Smart**
7. **Right-Size It** — quick-dev vs full method; the economics of human-in-the-loop.
8. **Never Get Lost** — BMad-Help, the module ecosystem (CIS/GDS/TEA/BMB), the docs map.

**Track 5 · Capstone**
9. **Your Build, the BMAD Way** — pull it together into a one-page plan for the real thing.

**Track 6 · Level Up — Build Your Own (BMad Builder)** *(bonus/advanced; added per owner request)*
10. **Build Your Own Teammate** — BMB pipeline to create a custom agent; persistent memory / self-learning agents (taught at concept level, with a fidelity flag — it's new/evolving; point to BMB docs).
11. **Build Your Own Skill** — BMB pipeline to build a reusable skill on the open Agent Skills standard.

## Learner capabilities (configured)

- Beginner-first mode: ON (define jargon on first use; assume zero agile/PM background).
- Glossary-first: ON (`GLOSSARY.md`).
- Scenario gates: ON but **light** — judgment scenarios and "predict-then-reveal," not
  recall quizzes. Per owner: less testy, more interactive.
- Spaced review: light (review hooks per module; no heavy gating because non-sequential).
- Competency map: ON (`COMPETENCY_MAP.md`) — maps modules to the four goals + source.
- Helper commands: ON.
- Visual aids / NotebookLM: OFF (not requested).

## Source / traceability policy

`SOURCE.md` is canonical and faithful to the official docs. Every module's claims trace
to a SOURCE section. **Questions the course doesn't cover → answer from SOURCE if
present, else point to the exact Docs Map entry; never invent BMAD behavior.**

## Model guidance

- Run the teaching on a **mid tier** (e.g. Sonnet) — it's judgment-and-conversation
  work, not heavy reasoning. Opus is overkill; Haiku may be too shallow for the
  scenario coaching.
- The static `reference/` aids (cheat-sheet, quiz) need **no model** — open in a browser.

## External dependencies

None required to learn. Optional: a real BMAD install if the learner wants to try the
workflows for real (pointed to, not required).

## Build roadmap

SOURCE → adapter (`CLAUDE.md`) → templates → `LESSONS.md` index + 9 `lessons/` files →
`reference/` aids → `index.html` → `VALIDATION.md` → private GitHub repo.

## Validation checklist (completed in VALIDATION.md)

- Structural: all files present, JSON parses, module counts match across README /
  LESSONS / PROGRESS / progress.json.
- Self-contained: learner can start from the folder alone.
- Harness smoke proof: Claude Code commands defined; first-run + resume dry-run.
- Adversarial coherence: skeptical pass for contradictions, undefined jargon, dead
  commands, broken non-sequential promises.
