# Module 6 — Ship It

> **Where this fits:** You've planned, architected, and sliced the work into stories and
> epics. Now you actually build. This module is about the build cycle: how BMAD turns a
> pile of stories into working software, one chunk at a time.
> **The point:** by the end you'll know the three-step cycle that runs for every story —
> and why each story gets its own fresh chat instead of piling up in one.

*Source: SOURCE.md §2.4 (Implementation) and §7 (fresh chat per workflow). Instructor: do before tell. Keep turns short.*

---

## Do This First

Before any explanation — a quick slice-and-dice. Pull up their build from `MY_BUILD.md` and ask:

> Think about [their build idea]. If you had to break the first wave of work into **2–3
> small chunks** — each one something you could hand to a developer on Monday and expect
> done by Friday — what would they be? Just plain English. No jargon yet.

Let them answer. Write down what they say — you'll use it in "Apply to Your Build."
Don't correct vocabulary yet; the point is to get them thinking in *slices*, not in
monoliths.

## What Just Happened

They just did the hardest part of Phase 4 intuitively: sliced work into chunks small
enough to build without blowing up the context. Those chunks have a name in BMAD:

- **Story** — one small, independently buildable unit of work. "User can log in with
  email and password." Concrete. Completable. Reviewable.
- **Epic** — a group of related stories that together deliver a bigger feature. "User
  auth" might be an epic; "log in," "sign up," and "reset password" are its stories.
- **Sprint** — the planning layer above epics: which epics/stories are we working on and
  in what order.

## The Idea

Implementation in BMAD has two modes: a **once-per-project setup**, then a **cycle you
repeat for every story**.

**Once, at the start:** run `bmad-sprint-planning`. It creates a file called
`sprint-status.yaml` — your tracker. Every epic and story lives there so you always
know what's done, what's in progress, and what's next.

**Then, per story — the build cycle:**

| Step | Workflow | What it does |
|---|---|---|
| 1 | `bmad-create-story` | Turns the epic entry into a full story file — context, acceptance criteria, everything the developer needs |
| 2 | `bmad-dev-story` | Implements the story — this is where the code gets written |
| 3 | `bmad-code-review` | Validates the result — catches issues before you move on *(recommended)* |

After every story in an epic is done: run `bmad-retrospective`. It's a structured
look-back — what worked, what didn't, what to carry forward. Think of it as the team
debriefing after a sprint.

**One more thing on the horizon:** BMAD V6 has a roadmap item called **Dev Loop
Automation** — running this cycle with less hand-holding between steps. It's flagged
"coming soon" in the docs, with early pieces landing. It's not fully shipped yet, so
don't count on it; the three-step manual cycle above is what you've got today.

## Pattern / Anti-pattern

- ✅ **Pattern:** one story, one build cycle, one fresh chat. Small, reviewable, shippable
  chunks. The tracker tells you where you are.
- ❌ **Anti-pattern:** "implement the whole auth epic in one go" — context blows up, the AI
  loses track, review is impossible, and when something breaks you have no idea where.
- **How to tell which you're in:** if you can't say "this chat is building exactly one
  story," you've probably merged too much.

## Explain It Back

Ask: *"Walk me through what happens between 'I approved the architecture' and 'I have
working software.' What are the steps?"*

Listen for: sprint-planning → create-story → dev-story → code-review → retrospective
(after the epic). If they miss the sprint-planning setup step or the retrospective,
prompt gently — those bookends matter.

## Scenario Check (light — predict, then reveal)

> "BMAD runs each story in a **fresh chat** instead of continuing the same conversation.
> Why? What goes wrong if you keep building story after story in one long chat?"

Let them predict. Then reveal:

*Each workflow running in its own chat keeps context clean. A long single chat accumulates
stale assumptions — early decisions that were revised, context from story 1 that
subtly biases story 5 in ways you can't see. A fresh chat means the agent is working
only with what's actually true right now, not what was true three stories ago.*

## Apply to Your Build

Take what they said in "Do This First" and formalize it. Update the **M6 line** in
`MY_BUILD.md`:

> *My build sliced into the first 2–3 stories: [story 1] / [story 2] / [story 3]*

Draft a version for them from what they described — plain English, not workflow jargon —
then let them edit it. If their slices are too big ("implement the whole backend"), help
them cut one down to something that fits inside one developer-week.

## Review Hooks / Go Further

- **Pairs well with Module 5 (Decide How):** the architecture doc created in solutioning
  is what `bmad-dev-story` builds *against* — so those decisions show up here at build
  time. If you haven't done Module 5, the stories risk drifting.
- **Pairs well with Module 9 (Capstone):** the "First slice" field in the capstone plan
  is exactly what you filled in here. You're ahead.
- **If they ask about Dev Loop Automation:** honest answer — roadmap, not fully shipped.
  Point to SOURCE §9 → the roadmap URL (`docs.bmad-method.org/roadmap/`) for the latest.
- **If they ask about exact workflow commands or setup:** point to SOURCE §9 → Getting
  Started tutorial. This module is the *why and shape*, not the install guide.
