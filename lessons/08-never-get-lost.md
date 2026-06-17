# Module 8 — Never Get Lost

> **Where this fits:** You've been through the method, the crew, the phases, the
> solutioning, the build cycle. Now: what do you do when you forget where you are?
> **The point:** BMad-Help is your compass — run it first, not the docs. The docs are
> for when you need to go deeper. You never have to guess.

*Source: SOURCE.md §5 (BMad-Help), §6 (module ecosystem), §9 (Docs Map). Do before tell.*

---

## Do This First

Before any theory — write the question. Look at your build in `MY_BUILD.md` and fill in
this blank for real:

> *"I have [your build], where do I start?"*

Write it out. The full sentence. You'll need it in a moment.

## What Just Happened

You just drafted the exact thing you'd say to BMad-Help. That matters because
BMad-Help is not documentation — it's an interactive starting point. You hand it a
question (or nothing at all), and it:

- **Inspects your project** to see what's already been done.
- **Shows your options** based on which modules you have installed.
- **Recommends what's next** — including the first required task.
- **Answers questions** like the one you just wrote.

You never have to memorize which phase comes after which. You never have to guess
whether your project needs a PRD or can skip straight to stories. You ask.

And here's the part people miss: **BMad-Help also runs automatically at the end of
every workflow**, telling you exactly what to do next. The compass doesn't just work
when you're lost — it hands you the next step every time you finish something.

## The Idea

**BMad-Help is the front door.** The docs say: right after installing BMAD, invoke
`bmad-help` immediately. It detects your installed modules and points you to the right
starting point. Not a generic "here are all the phases" — the right starting point *for
your project, with your modules*.

Speaking of modules: BMAD is a core method plus optional add-ons. You install what you
need.

| Code | Module | What it adds |
|---|---|---|
| **BMM** | BMad Method | The core: four phases, agents, build cycle |
| **CIS** | Creative Intelligence Suite | Innovation + design thinking; frameworks like SCAMPER |
| **GDS** | Game Dev Studio | Game-specific workflows; Unity, Unreal, Godot; 21+ game types |
| **TEA** | Test Architect | Agent Murat + 9 enterprise testing workflows |
| **BMB** | BMad Builder | Build and customize your own agents and skills |

There's also a lightweight **built-in QA** for quick test coverage — handy when full
TEA is more than you need.

**Install channels** (the version you get): `stable` is the default (latest released),
`next` is the main branch for early adopters, `pinned` locks a specific version for
reproducibility.

BMad-Help knows which of these you have installed. That's why it can make a real
recommendation instead of a generic one.

**When you're mid-project and lost, BMad-Help is still move one.** The Docs Map
(below) is move two — when you know what you need and want to go deeper.

## Pattern / Anti-pattern

- ✅ **Pattern:** get lost → run `bmad-help` → get a recommendation → move.
- ❌ **Anti-pattern:** get lost → google around → skim three doc pages → still not sure →
  improvise a guess.
- ✅ **Pattern:** want deeper detail on a specific topic → go to the Docs Map, find the
  exact URL, read that section.
- ❌ **Anti-pattern:** guess what the docs probably say and act on the guess.

The theme: **pull from the right place, don't improvise**. BMad-Help for "where do I
go?"; the Docs Map for "how does this work?"; the source for "what exactly does it
say?"

## Explain It Back

Ask: *"In your own words — what does BMad-Help do that the docs don't?"* Listen for the
idea that it's interactive, project-aware, and module-aware — not just a table of
contents. If they say "it inspects your project," that's the key bit.

## Scenario Check (light — predict, then reveal)

> You're three weeks into a project. You just finished `bmad-create-architecture` and
> you can't remember what runs next or whether you need to do it. **What's your first
> move, and where would you look it up if BMad-Help wasn't available?**

Predict before reading on.

*(Reveal: first move is `bmad-help` — it inspects the project, sees you've got
architecture done, and tells you exactly what's next. If you needed to look it up
without it: the Docs Map → Explanation → Solutioning
(`https://docs.bmad-method.org/` → Solutioning deep-dive). Not a guess — the exact
section.)*

## Apply to Your Build

Update the **M8 line** in `MY_BUILD.md`:

> *"The first thing I'd ask BMad-Help: [the sentence you wrote at the top of this
> module]"*

That sentence is yours. It's a real question about a real build — not a classroom
exercise.

## Review Hooks / Go Further

- **This module pairs with every other module.** It's the get-unstuck tool, not a
  phase — invoke it any time.
- **When BMad-Help gives you a recommendation**, that recommendation will point at one
  of the phases or workflows from the earlier modules. That's the design. The compass
  assumes you know the terrain.
- **Next:** Module 9 (Capstone) — you'll take everything in `MY_BUILD.md` and turn it
  into a one-page BMAD plan you'd actually use.
- **Docs Map — the real URLs:**
  - Docs home → `https://docs.bmad-method.org/`
  - Install + first run → `https://docs.bmad-method.org/tutorials/getting-started`
  - Everything in one file (for AI context) → `https://docs.bmad-method.org/llms-full.txt`
  - Roadmap (V6, Dev Loop Automation) → `https://docs.bmad-method.org/roadmap/`
