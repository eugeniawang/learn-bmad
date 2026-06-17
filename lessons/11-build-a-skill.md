# Module 11 — Build Your Own Skill (BMad Builder)

> **Where this fits:** A bonus "level up" module — the companion to Module 10. Where an
> agent is *who*, a skill is *what they can do*. Stands alone, but Module 10 (agents) is a
> natural partner. **The point:** by the end you'll know what a "skill" is in BMAD, the
> BMAD way to build one, and you'll have spec'd one for your build.

*Source: SOURCE.md §6 (skill categories) and §6.5 (BMad Builder + the open Agent Skills
standard). Instructor: do before tell; keep it light. Never show code — describe in plain
English.*

---

## Do This First

Before any explanation, ask (personalize to their build in `MY_BUILD.md`):

> "Think about building [their build]. Is there a **repeatable chore** you'd love to press
> a button for — 'turn meeting notes into tasks,' 'draft a release note,' 'check my copy
> against our style'? Name one you do (or will do) over and over."

Let them name it. That repeatable chore is a perfect candidate for a **skill**.

## What Just Happened

You just found a *reusable capability* — something worth packaging once and reaching for
again and again. That's exactly what a **skill** is.

> Define on first use: a **skill** = a self-contained capability the AI can run. In BMAD
> there are two flavors: **agent skills** (load a persona, like Mary the Analyst) and
> **workflow skills** (run a structured, multi-step process without loading a persona).
> The chore you named is the workflow kind.

## The Idea

An **agent** is *who* (a persona); a **skill** is *what they can do*. In fact, a BMAD agent
is basically a persona **plus a menu of skills/workflows** it can run. So skills are the
building blocks — and **BMad Builder (BMB)** gives you a guided pipeline to make your own.

Two things worth knowing:

- **The open Agent Skills standard.** BMB skills are built on an *open* standard, so they
  **work across 40+ AI tools** — not just BMAD. A skill you build isn't locked in.
- **Shareable.** You can distribute what you build through the **BMad Marketplace** (or any
  compliant one) — so a skill you make can help other people too.

The BMAD *way* to build one is — predictably — a **guided workflow**, not freehand: you
describe the capability, BMB helps you scaffold it, and there's a **validate** step before
it's done (the same "make it explicit, then check it" discipline from the rest of BMAD).
The BMB Quick Start literally walks you through building your first skill.

## Pattern / Anti-pattern

- ✅ **Pattern:** turn a *repeated* task into a skill — package it once, reuse it forever,
  and let it work across your tools.
- ❌ **Anti-pattern:** building a skill for something you'll do exactly once (just ask the
  AI), or making one giant do-everything skill instead of a few focused ones.
- **Agent or skill?** If you want a *persona* with judgment and a menu → agent (Module 10).
  If you want *one capability* you can invoke → skill. Often you build skills, then give an
  agent a menu of them.

## Explain It Back

Ask: *"In your own words — what's the difference between an agent and a skill? And is the
chore you named earlier better as a skill, or does it need a whole agent?"* Listen for:
agent = persona/who; skill = capability/what. Repair if they merge the two.

## Scenario Check (light — predict, then reveal)

> "For each, is it better as a **skill**, a whole **agent**, or **neither**?
> (a) 'Convert any meeting transcript into a tidy action list.'
> (b) 'A standing product-coach I chat with weekly that knows my roadmap.'
> (c) 'Rename one folder, once.'"

*(Reveal: (a) a skill — one clear, repeatable capability. (b) an agent — it's a persona
with memory and judgment (hello, Module 10). (c) neither — that's a one-off; just ask.
Reward the reasoning, not the exact label.)*

## Apply to Your Build

Update the **M11 line** in `MY_BUILD.md`:

> *A skill I'd build for my project: it takes ____ and produces ____, and I'd reuse it
> whenever ____.*

Draft a first version from their "Do This First" chore, then let them refine it.

## Review Hooks / Go Further

- **Pairs well next:** **Module 10 — Build Your Own Teammate** (give your agent a menu of
  skills like this one), and **Module 8 — Never Get Lost** (where the module ecosystem lives).
- **Go further (for real):** BMB Quick Start ("build your first skill") →
  `bmad-builder-docs.bmad-method.org`; share via the BMad Marketplace (SOURCE §9).
- **If they ask about the exact skill file format / Agent Skills spec** → that's the BMB
  docs and the open standard; point them there rather than guessing.
