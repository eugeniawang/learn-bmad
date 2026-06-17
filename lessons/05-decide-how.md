# Module 5 — Decide How

> **Where this fits:** Phase 3, Solutioning. You've already said *what* to build and *why*
> (that was Planning). Now you pin down *how* — and chop the work into pieces.
> **The point:** by the end you'll know why writing your technical decisions down before
> building saves you from the integration nightmare that kills momentum mid-project.

*Source: SOURCE.md §2 (Phase 3 — Solutioning). Instructor: do before tell. No code shown.*

---

## Do This First

Before any theory — make one real decision about your build, in plain English. Pull up
their `MY_BUILD.md` details and ask:

> "Pick ONE technical fork you'll hit early in your build — something where two paths
> exist and you'd have to choose. Examples: *'Users sign in with email/password, not
> social login.'* Or: *'The app stores data in the cloud, not on-device.'*
> **Write it down in one sentence.**"

Let them write it. Don't pre-fill it for them — but if they're stuck, give two concrete
options from their own build to pick between.

## What Just Happened

They just made an **Architecture Decision Record** — an ADR. It's not a fancy thing; it's
any explicit technical choice, written down so every future agent (and future chat) builds
against the same assumption.

The key word is *explicit*. The decision was already going to get made. Writing it down
is the whole move.

## The Idea

**Solutioning** (Phase 3) is the bridge between *what to build* and *actually building it*.
It answers two questions in order:

1. **How?** — What technical choices govern this project?
2. **What units of work?** — How do we break that into buildable pieces?

It produces three things:

- **`architecture.md` with ADRs** — the living record of technical decisions. An **ADR**
  (Architecture Decision Record) is one written-down choice: what was decided, and why.
  Think of it as the ref call that every future agent has to honor.
- **Epics & stories** — an **epic** is a big chunk of functionality (e.g., "user
  authentication"); a **story** is one implementable slice of it (e.g., "user can log in
  with email"). Stories are small enough for one agent to finish in one chat.
- **Readiness gate** — before a single line of code gets written, `bmad-check-implementation-readiness`
  reviews everything and returns **PASS**, **CONCERNS**, or **FAIL**. A FAIL now costs
  nothing. A FAIL discovered in implementation costs everything.

> **Solutioning vs. Planning:** Planning asks *What & Why*. Solutioning asks *How, then
> what units of work*. Two separate phases, two separate chats, two separate jobs.

## Pattern / Anti-pattern

- ✅ **Pattern:** write one ADR per meaningful technical fork before building. Every agent
  reads the same doc and builds toward the same architecture.
- ❌ **Anti-pattern:** skip the architecture doc and let each agent "figure it out." Each
  agent does — and they figure out different things.
- **How to tell which you're in:** if two agents could each build a separate piece of your
  app *right now* and produce code that doesn't connect, you skipped Solutioning.

## Explain It Back

Ask: *"In one sentence — what's the difference between Planning and Solutioning?"*

Listen for *what/why vs. how/units of work*. If they conflate them, give the analogy:
Planning is the brief ("we need a house, 3 bedrooms, budget X"). Solutioning is the
blueprint ("here's what material, here's how the plumbing connects"). You can't give a
blueprint to five contractors without one — they'll each wire the bathroom differently.

## Scenario Check (light — predict, then reveal)

> Two agents are building your app in parallel. Agent A builds the data-fetching layer.
> Agent B builds the front-end that consumes it. They work from the same PRD — same
> feature list, same requirements.
>
> When they try to connect their pieces, nothing works. Agent A used REST. Agent B
> expected GraphQL.
>
> **What was missing? Predict before scrolling.**

*(Reveal: a shared, explicit architecture decision. One line in `architecture.md` — "Use
GraphQL for all APIs" — and both agents build toward the same interface. The PRD said
what to build; the ADR says how the pieces connect. Without it, two agents reading the
same requirements will still make different technical calls.)*

## Apply to Your Build

Update the **M5 line** in `MY_BUILD.md`:

> *One technical decision I should make explicit up front: ____*

Draft a first version from their build details — something concrete, like the data storage
approach, the auth method, or the API style. Let them refine it.

## Review Hooks / Go Further

- **The agent who runs Solutioning is Winston** — the Architect (meet him in Module 3 if
  you haven't). He owns `architecture.md` and ADRs by role.
- **Next up: Module 6 — Ship It** (Implementation). That's where epics and stories become
  working software, one story at a time.
- **The readiness gate** (`bmad-check-implementation-readiness`) is a great example of
  Module 7's core idea — scaling rigor to the stakes. A FAIL before building is cheap.
  A FAIL after is not.
- **If they ask about the exact commands** to run Solutioning → point to SOURCE §9
  (Getting Started / setup tutorial). The commands are `bmad-create-architecture`,
  `bmad-create-epics-and-stories`, and `bmad-check-implementation-readiness` — in that
  order, each in a fresh chat.
