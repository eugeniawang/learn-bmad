# Module 2 — The Four-Phase Map

> **Where this fits:** This is the "whole journey on one page" module. Nothing before it
> is required — it's self-contained. Module 1 (why BMAD exists) pairs well before it,
> but you don't need it.
> **The point:** by the end you'll be able to name the four phases, say the question each
> one answers, and know which phases your build actually needs (spoiler: probably not all four).

*Source: SOURCE.md §2. Instructor: one beat at a time — let them predict before you explain.*

---

## Do This First

Before any explanation — a quick prediction game. Pull their build from `MY_BUILD.md`.

> Here are the four phase names, **scrambled**: Implementation, Analysis, Solutioning,
> Planning.
>
> **Without looking anything up — put them in order, and guess in one line what each one
> is for.** Use [their build] as your mental anchor: what would you actually need to do
> before you could write a single line of code?

Let them answer. Don't correct yet — you're about to show them the map.

## What Just Happened

However they ordered it, something real just happened: they had to think about *what
comes before what*. That instinct — sequencing work deliberately — is exactly what BMAD
makes explicit.

Here's the actual map:

| Phase | Name | The question it answers | What it produces |
|---|---|---|---|
| 1 | **Analysis** | "Do I understand the problem?" | Sharper thinking — *optional, but it makes everything downstream better* |
| 2 | **Planning** | "What should we build, and why?" | A **PRD** (Product Requirements Document — the contract the project is measured against) |
| 3 | **Solutioning** | "How? Then what are the units of work?" | `architecture.md` (with ADRs), epics & stories, a go/no-go gate |
| 4 | **Implementation** | "Build it." | Working software, one story at a time |

One discipline runs through all of it: **each phase runs in a fresh chat.** New phase, new
conversation — no stale context dragging in.

## The Idea

Walk through each phase in one or two lines, naming what it actually *does*:

**Phase 1 — Analysis** is optional, but skipping it means your PRD is built on assumptions
instead of insight. BMAD offers brainstorming, research, and feasibility tools here — all
designed to sharpen the problem *before* you commit to building a solution.

**Phase 2 — Planning** turns a sharp idea into a PRD. That document answers "what and why"
and becomes the reference every later decision gets checked against. Vague in → vague PRD
→ wrong architecture bets → stories that miss edge cases. The mess compounds.

**Phase 3 — Solutioning** is two moves: first, *how* (technical decisions recorded in
`architecture.md` with ADRs — Architecture Decision Records, i.e. written-down "we chose
X because Y"); then *what units of work* (epics and stories, plus a readiness gate that
gives a PASS / CONCERNS / FAIL before a single line is written).

> The classic Solutioning nightmare: no shared architecture, so one agent builds a REST
> API and another builds GraphQL — and then you get to explain to them why they can't talk
> to each other.

**Phase 4 — Implementation** is the build. Sprint planning once, then a repeating cycle:
create a story → implement it → review it. One story at a time, fresh chat each round.

One more thing worth naming now, because it will come up: **you don't always use all four
phases.** Small work often skips most of this. That tradeoff gets its own module (Module 7
— Right-Size It), but keep it in the back of your mind.

## Pattern / Anti-pattern

- ✅ **Pattern:** run each phase in its own fresh chat, producing a real artifact the next
  phase builds on. Clean handoffs, no stale assumptions.
- ❌ **Anti-pattern:** one long chat that improvises analysis, planning, architecture, AND
  code in a rolling stream of consciousness. Feels fast; costs double later.
- **How to tell which you're in:** if there's no PRD and no architecture doc, you're in the
  anti-pattern — whether you meant to be or not.

## Explain It Back

Ask: *"In one sentence each — what does Planning produce, and how is Solutioning different
from it?"* Listen for the key distinction: Planning answers *what and why* (PRD); Solutioning
answers *how and in what pieces* (architecture + stories). If they conflate them, give the
one-line version: "Planning is the brief; Solutioning is the blueprint."

## Scenario Check (light — predict, then reveal)

Give them this artifact and ask which phase produced it, and which phase is **missing**:

> You're handed a folder with two files:
> - `architecture.md` — lists the tech stack, the API pattern, and three ADRs explaining
>   key decisions.
> - `epic-01.md` — a breakdown of the first feature into five stories.
>
> **Which phase produced these? And if this is all you have — what phase's artifact is
> conspicuously absent, and why does that matter?**

Let them predict and explain. *(Reveal: both files come from Solutioning (Phase 3). What's
absent is the PRD from Planning (Phase 2) — and that matters because without it, you can't
tell if the architecture is solving the right problem. The stories might be perfectly written
for the wrong product.)* Reward the reasoning, not the exact answer.

## Apply to Your Build

Update the **M2 line** in `MY_BUILD.md`:

```
M2 — Which phases my build actually needs:
Analysis: [yes / probably / skip — reason]
Planning: [yes / probably / skip — reason]
Solutioning: [yes / probably / skip — reason]
Implementation: [yes — this one's always yes]
```

Draft a first version *for* them based on what they've shared about their build, then let
them edit it. A small side project might honestly skip Analysis and go light on Solutioning;
a real product with multiple moving parts probably wants all four.

## Review Hooks / Go Further

- **Pairs well next:** **Module 4 — Think First** goes deep on Analysis and Planning (why
  vagueness is so expensive, and how a PRD actually gets made). **Module 7 — Right-Size It**
  is the direct follow-on to the "you don't always use all four" note above — that's where
  the tradeoffs live.
- **Pairs well before:** this module is a great warmup for any of Modules 3–6, since it
  gives you the map before you explore individual rooms.
- **If they ask about install/config or how to actually run a workflow** → that's setup
  territory; point to the Getting Started tutorial (SOURCE §9):
  https://docs.bmad-method.org/tutorials/getting-started
- **Dev Loop Automation** (running the Phase 4 cycle with less hand-holding) is on the V6
  roadmap — "coming soon" per the docs, with early pieces landing. Flag it as roadmap if
  it comes up; don't imply it's fully shipped.
