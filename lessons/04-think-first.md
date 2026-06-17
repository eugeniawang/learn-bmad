# Module 4 — Think First

> **Where this fits:** Phases 1 and 2 of the four-phase map — Analysis then Planning.
> You've seen the map (Module 2); now you slow down before you build.
> **The point:** by the end you'll know why a sharp idea going in saves enormous pain
> coming out — and exactly how BMAD helps you get there.

*Source: SOURCE.md §2.1–§2.2. Instructor: doing before telling. No code shown.*

---

## Do This First

Before any theory — a quick stress-test. Take your build idea and finish this sentence:

> "This is for **[specific person]** who has **[specific problem]**."

Now ask yourself honestly: *How confident am I in both blanks? Could I name one real
person who fits — and explain why they'd pay or show up for this?*

Sit with any shakiness there. That's the assumption worth pressure-testing first.

## What Just Happened

You just hit the thing that kills more builds than bad code: **a blurry picture of who
you're building for and why they care.** Most builders skip this because it feels like
procrastinating. It is not. It's the only move that makes everything else cheaper.

Here's the ugly math from the BMAD docs:

> **Vagueness compounds.** A vague idea → a vague PRD → wrong architecture bets →
> stories that miss edge cases. The cost grows at every step.

Catching a fuzzy assumption now costs a conversation. Catching it after the
architecture is set costs weeks.

## The Idea

Phase 1 is **Analysis** (optional, but it sharpens everything). Phase 2 is
**Planning** — the step that produces the **PRD** (Product Requirements Document: the
written contract that says what you're building and why).

Here's what each phase actually does:

**Analysis — Phase 1**

- **Brainstorming:** a facilitated creative session. The AI acts as a *coach pulling
  ideas out of you* through structured techniques. It does **not** generate ideas for
  you — it asks questions, pokes at edges, challenges assumptions, and helps you
  surface what you already half-know. Best when you have a real problem but no clear
  solution yet.
- **Market / competitor / customer research and feasibility.** Attack the problem from
  different angles. By the time you sit down to plan, you want to know *what* you're
  building and *for whom* — not guess.

Analysis is optional. Skipping it is fine for small work. But skipping it means your
PRD is built on assumptions instead of insight — and every downstream document
inherits whatever's wrong.

**Planning — Phase 2**

Turn the sharpened idea into a **PRD**: the document that states what to build and why.
This is the contract the rest of the project is measured against. If Analysis clarified
your thinking, the PRD just captures it. If you skipped Analysis, the PRD is where that
clarity has to come from — which is harder, but still the right starting point for
everything that follows.

## Pattern / Anti-pattern

- ✅ **Pattern:** spend a little time clarifying who you're building for and why before
  you write a single requirement. Brainstorm by talking *to* an AI that asks good
  questions — not one that hands you a solution.
- ❌ **Anti-pattern:** skip straight to "write me a PRD" with a half-baked idea. The
  PRD sounds complete, but every vague spot in your thinking becomes a hole in it.
- **How to tell which you're in:** if you can't explain your PRD's "why" in one sentence
  without hedging, the vagueness is still in there.

## Explain It Back

Ask: *"Brainstorming in BMAD — is the AI coming up with ideas, or are you?"* Listen for
the correct answer: **you** are. The AI is a coach asking the questions that help you
find what you already know. If they say "the AI generates ideas," gently correct it —
this distinction matters for getting any real value out of the session.

## Scenario Check (light — predict, then reveal)

Two lines from two different PRDs. Predict which one will cause downstream pain:

> **A:** "Users can set their preferences."
>
> **B:** "A logged-in user can toggle email notifications on or off from their account
> settings page; the change takes effect immediately."

Pick A or B, then explain *where* the pain shows up — in the architecture? In the
stories? In QA?

*(Reveal: A. "Preferences" is undefined — the architect has to guess what it means, the
developer builds something, QA tests something slightly different, and the whole team
finds out they diverged at review. B is concrete enough that every downstream step
builds the same thing. Vagueness didn't kill anything on its own — it just deferred the
argument to the worst possible moment.)*

## Apply to Your Build

Update the **M4 line** in `MY_BUILD.md`:

> *The one assumption in my idea worth pressure-testing first: ____*

Draft a first version *for* them from their build details — e.g., "who exactly is my
user and what makes them different from someone who wouldn't care about this?" — then
let them sharpen it.

## Review Hooks / Go Further

- **Pairs well next:** **Module 5 — Decide How** (once you have a sharp PRD, the
  Architect turns it into an architecture — that's where "what" becomes "how").
- **Pairs well back:** **Module 2 — The Four-Phase Map** if the two-phase sequence
  here felt fast; the full map shows where Analysis and Planning sit in the arc.
- **If they ask about the exact PRD workflow, commands, or setup:** point to SOURCE §9
  (Docs Map) — that's where the actual tool docs live.
- **Brainstorming depth:** the CIS module (Creative Intelligence Suite) extends
  Analysis with dedicated agents — an Innovation Strategist, Design Thinking Coach,
  and more. Not required; useful when the problem space is genuinely fuzzy.
