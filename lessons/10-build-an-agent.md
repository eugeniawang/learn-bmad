# Module 10 — Build Your Own Teammate (BMad Builder + Memory)

> **Where this fits:** A bonus "level up" module — once you've met the BMAD team, this is
> how you *make your own* teammate. Stands alone; it helps (not required) to have done
> Module 3 first. **The point:** by the end you'll understand the BMAD way to build a
> custom agent — including agents that **remember and improve over time** — and you'll
> have sketched one for your build.

*Source: SOURCE.md §6.5 (BMad Builder + persistent memory). Instructor: this is a NEW,
evolving feature — teach the concept + process; for exact mechanics, point to the BMB
docs. Do before tell. Keep it fun.*

---

## Do This First

Before any explanation, a daydream. Ask (personalize to their build in `MY_BUILD.md`):

> "Forget BMAD's built-in crew for a second. If you could invent **one** AI teammate
> custom-built for [their build] — give it a name, a job, and one thing it should always
> remember about you or your project — what would it be?"

Let them invent it. That little daydream *is* the thing BMAD Builder lets you actually make.

## What Just Happened

You just designed an agent: a **role**, a **personality**, and **something it remembers**.
Those three things are exactly what **BMad Builder (BMB)** helps you create — for real.

> Define on first use: **BMad Builder (BMB)** = the "meta-module" of BMAD — the part you
> use to *extend BMAD itself*, building your own agents, skills, and modules with guided
> assistance (then share them via the BMad Marketplace).

## The Idea

BMB gives you a **guided pipeline** to build a teammate — you don't hand-write the
plumbing, you get walked through it (very on-brand for BMAD: a workflow, not winging it).
The same five beliefs apply — you decide the few things that matter (who is this agent?
what's its job? what should it know?), and the tooling builds consistently against that.

What you can build with BMB: **agents** (your own specialists — domain experts *or*
personal companions), **skills** (Module 11), **workflows**, and whole **modules** you can
share.

### The headline: agents that *remember* (the "self-learning" bit)

BMB's standout feature for agents is **persistent memory**: per the docs, agents can
**"remember across sessions and keep improving."** That's the self-learning idea — a
teammate whose memory **evolves with you over time** instead of starting cold every chat.
Think "personal AI companion that actually gets to know your project."

Keep two layers straight (this trips people up):

- **Persistent facts** — static things you *hand* the agent up front (your org rules, your
  preferences, a file of context). You edit these; they don't change on their own.
- **Persistent memory** — what the agent *learns and refines* across sessions on its own.
  This is the evolving, "syncs with you over time" layer.

> **Honesty flag (say this to the learner):** persistent memory / self-learning agents are
> **new and still evolving** in BMB. You now get the *idea* and the *BMAD process*; for the
> exact mechanics — how memory is stored, synced, reset — the BMB docs are the source of
> truth: `bmad-builder-docs.bmad-method.org`. Don't let me (or anyone) wing the specifics.

## Pattern / Anti-pattern

- ✅ **Pattern:** build an agent when you have a *recurring* job with a clear role — and
  give it memory when it should get smarter about *you/your project* over time.
- ❌ **Anti-pattern:** building a custom agent for a one-off task (just ask, or use
  quick-dev), or cramming ten unrelated jobs into one mega-agent (that's the
  everything-blur again — make specialists).
- **Build vs. customize:** making a *new* teammate → BMad Builder. *Tweaking an existing*
  one (new persona, extra facts, menu change) → the `bmad-customize` helper, no new agent
  needed.

## Explain It Back

Ask: *"In your own words — what's the difference between persistent **facts** and
persistent **memory**? And would your dream agent from earlier want memory, or just facts?"*
Listen for: facts = static/you-set; memory = evolves/the-agent-learns. Repair if they blur them.

## Scenario Check (light — predict, then reveal)

> "Three teammate ideas — for each, does it want **persistent memory**, just **persistent
> facts**, or neither?
> (a) An agent that enforces your company's fixed style guide.
> (b) A writing companion that should learn your voice over months.
> (c) A one-time 'rename these files' helper."

*(Reveal: (a) facts — the rules are fixed, hand them over. (b) memory — it should evolve
with you; this is the self-learning sweet spot. (c) neither — that's a quick task, not a
teammate. Reward the reasoning.)*

## Apply to Your Build

Update the **M10 line** in `MY_BUILD.md`:

> *A custom agent I'd build for my project: name ____, job ____, and it should
> [remember / be told] ____ — because ____.*

Draft a first version from their "Do This First" daydream, then let them refine it.

## Review Hooks / Go Further

- **Pairs well next:** **Module 11 — Build Your Own Skill** (the capabilities your agent's
  menu is made of), and **Module 3 — Meet the BMAD Team** (the agents BMB-built ones sit
  alongside).
- **Go further (for real):** BMB Quick Start + "Build Your First Module" →
  `bmad-builder-docs.bmad-method.org`. Share what you build via the BMad Marketplace
  (SOURCE §9).
- **If they ask exact memory mechanics** → don't guess; that's the BMB docs' job. Point them there.
