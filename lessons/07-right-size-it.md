> **Where this fits:** You know the four phases. Now learn when to skip most of them.
> **The point:** Knowing when NOT to run heavy process is a first-class skill — not a shortcut.

*Source: SOURCE.md §4 (Scale-Adaptive + Quick Dev)*

---

## Do This First

Three changes. Sort each into **quick-dev** or **full method** — before reading on.

1. You spot a typo in your app's welcome message. Fix it.
2. You want to add a user profile photo upload feature.
3. You decide to rebuild your app as a multi-tenant SaaS platform.

Write down your answers. Then keep reading.

---

## What Just Happened

You probably sorted them fast. That's the point.

Typo → quick-dev, obviously. New platform → full method, obviously. The photo upload is the interesting one — medium scope, but still a *defined feature*, not a new product. Probably quick-dev, depending on complexity.

BMAD has a name for this judgment: **scale-adaptive**. The method isn't one-size-fits-all. It adapts to the size of the job. And the ability to make that call quickly? That's a skill you're building right now.

---

## The Idea

BMAD's scale-adaptive rule is a table with two rows:

| Scope | Approach |
|---|---|
| Small updates or additions | `bmad-quick-dev` — a single workflow: clarify intent → plan → implement → review |
| Major changes or additions | Full four-phase method, as much or as little rigor as the work deserves |

**Quick-dev** (define it: the `bmad-quick-dev` workflow) is not "BMAD lite." It's BMAD compressed into one workflow for work that doesn't need four phases.

The philosophy behind it comes from a tension: **human-in-the-loop turns are necessary but expensive.** (Human-in-the-loop = the moments where you, the human, weigh in and redirect.) Too much intervention throttles velocity. Zero intervention lets the AI's predictable failures run unchecked.

Quick-dev solves this with three moves:

1. **Compress intent first.** You and the model squeeze the request into one coherent, small, contradiction-free goal before any code is written. Intent can start from a few phrases, a bug-tracker link, or even a story number.
2. **Route to the smallest safe path.** A true zero-blast-radius change can go straight to implementation. Bigger ones take the fuller path through the workflow.
3. **Relocate human control to high-value moments only:** intent clarification, spec approval, final review. The AI runs the rest.

It's the same belief as the whole method — spend human judgment where it changes the outcome — just applied in miniature.

---

## Pattern / Anti-pattern

**Pattern:** Small, clear change → quick-dev. Compress intent, let it run, review the result.

**Anti-pattern:** Running the full four-phase method on a one-line fix. PRDs, epics, architecture docs, readiness gates — for a typo. That's not rigor; it's overhead that slows you down and trains you to resent the process.

Over-processing small work is itself a mistake. BMAD is explicit about this.

---

## Explain It Back

Finish these sentences without scrolling up:

- "Quick-dev is a single workflow with these four steps: ___"
- "Human-in-the-loop turns are ___ but ___"
- "Quick-dev relocates human control to three moments: ___"
- "Scale-adaptive means ___"

---

## Scenario Check (light — predict, then reveal)

**Scenario:** Your app has a broken button — it submits a form but shows no confirmation message to the user. You've identified the bug. It's about a 30-minute fix.

Quick-dev or full method? Why?

Write your prediction, then reveal:

<details>
<summary>Reveal</summary>

**Quick-dev.** This is a contained bug fix with a clear root cause and defined success criteria (button shows confirmation after submit). Intent is already compressed — you know exactly what broken looks like and what fixed looks like. No PRD needed, no architecture document, no epic.

Running the full four-phase method here would be overkill — and recognizing *that* is the skill. The wrong answer isn't just "full method." The wrong answer is not having a framework for deciding.

</details>

---

## Apply to Your Build

Open `MY_BUILD.md`. Find the Module 7 line. Fill it in:

> **M7 — Right-Size It:** Is this a quick-dev job or a full-method job? Why?

Think about the next change you're planning for your build. Which approach fits? Write one sentence on why.

---

## Review Hooks / Go Further

- **Pairs with Module 1:** Belief #3 — "scale rigor to the change" — is the theory. This module is the practice.
- **Pairs with Module 9 (Capstone):** You'll use this judgment when putting the whole method together on your real build.
- **If you want the exact quick-dev commands and setup:** point to SOURCE §9 (Docs Map) — the Getting Started tutorial covers installation and invocation.
- **The meta-point to carry forward:** BMAD gives you more process than you'll always need. Knowing which parts to skip, and when, is what separates someone using the method from someone being used by it.
