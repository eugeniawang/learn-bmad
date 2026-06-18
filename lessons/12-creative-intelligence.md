# Module 12 — Think Differently: the Creative Intelligence Suite

> **Where this fits:** A bonus module — a separate BMAD add-on for the *fuzzy front-end*
> of building, before you know enough to start Analysis. Stands completely alone. **The
> point:** by the end you'll know what CIS is, when to reach for it instead of (or before)
> the standard BMAD flow, and which of its five specialists to call for which kind of stuck.

*Source: [cis-docs.bmad-method.org](https://cis-docs.bmad-method.org). Instructor: keep it
concrete — the "when would you actually be stuck like this?" angle makes these agents click.
Do before tell. Never invent CIS behavior; point to the CIS docs for anything not covered here.*

---

## Do This First

Before anything about CIS, a quick diagnosis. Ask (personalize to their build in
`MY_BUILD.md`):

> "Right now with [their build] — are you more *problem-clear* (you know exactly what
> you're solving, just need to figure out the *how*)? Or *problem-fuzzy* (you've got an
> idea but the shape is still murky, the user is unclear, or you're honestly not sure
> if it's the right thing to build)?"

Let them answer. If they say **problem-clear**: "Standard BMAD Analysis — Module 4 — is
exactly where to start. CIS is for the *other* situation." If they say **problem-fuzzy**:
"That's exactly what we're about to solve."

## What Just Happened

You just found the gap. **BMAD's four-phase map starts at Analysis — which assumes you're
clear enough on the problem to analyze it.** When you're not there yet, you need something
upstream. That's CIS. It's not a replacement for the four phases; it's the *pre-flight*.

## The Idea — CIS and the Fuzzy Front-End

The Creative Intelligence Suite is a separate BMAD module built for the phase before
Analysis: when ideas are vague, problems need reframing, or you're genuinely not sure
what you're building or for whom.

**Core idea:** structured creativity beats unstructured staring. CIS gives you five
specialist agents who each run a *proven process* on your fuzzy situation. You don't
just brainstorm — you brainstorm using 36 tested techniques, anti-bias baked in.

> **"CIS is a separate module"** — define this on first use. Like all BMAD modules, it's
> an installable extension. The commands below only work once it's installed
> (see the [CIS docs](https://cis-docs.bmad-method.org) for install steps). This module
> teaches the *concept* — setup lives in the docs.

## Meet the Five (plus one on the way)

Each agent has a name, a command, and a specific job. Learn the role, not just the name.

| Agent | Command | Their job | Reach for them when… |
|---|---|---|---|
| **Carson** — Brainstorming Coach | `/cis-brainstorm` | Structured ideation: 36 techniques across 7 categories; SCAMPER; anti-bias protocol (shifts creative domain every 10 ideas so you don't cluster) | You need fresh ideas and the blank page isn't helping |
| **Maya** — Design Thinking Coach | `/cis-design-thinking` | 5-phase human-centered design: empathy → define → ideate → prototype → test | You're designing for users and you're not sure you actually understand them |
| **Victor** — Innovation Strategist | `/cis-innovation-strategy` | Disruption mapping; business model alternatives; market gap analysis; outputs a strategy doc | You're looking for the *opportunity*, not just the feature |
| **Dr. Quinn** — Problem Solver | `/cis-problem-solving` | Systematic root-cause diagnosis — gets to the *actual* problem before jumping to solutions | You've been solving the same problem repeatedly and it keeps coming back |
| **Sophia** — Storyteller | `/cis-storytelling` | 25 story frameworks; turns your product/feature/idea into a compelling narrative | You can build it but can't explain why it matters |
| **Caravaggio** — Presentation Master | *(coming soon)* | Persuasive presentation structure | — |

> **Where CIS fits the four-phase map:** CIS runs *upstream* of Phase 1 (Analysis) — or
> *alongside* it when you realize mid-Analysis that the problem needs reframing. Once CIS
> produces an output (a reframed problem, an innovation brief, a user insight), that feeds
> normally into BMAD's Analysis phase. The two aren't competing; they're sequential.

## Spotlight — Carson and SCAMPER

SCAMPER is the most teachable CIS technique and worth a minute. It's seven creative lenses
applied to whatever you're stuck on:

**S**ubstitute · **C**ombine · **A**dapt · **M**odify · **P**ut to other uses ·
**E**liminate · **R**everse

Carson doesn't just name them — he walks you through each angle and generates ideas at
every step. The anti-bias rule (switching creative domain every 10 ideas) is what keeps
it from producing 40 variations of the same thought.

Quick demo prompt: *"What if [their build]'s biggest frustration was the raw material? Run
SCAMPER on it — pick two lenses and show us what comes out."*

## Pattern / Anti-pattern

- ✅ **Pattern:** fuzzy problem → CIS first → clarity → BMAD Analysis. The front-end work
  makes everything downstream faster and more targeted.
- ❌ **Anti-pattern:** using CIS to *avoid* deciding. It generates options — the point is
  to *converge* to a clear problem, not to keep exploring indefinitely. CIS is a pre-flight
  check, not a holding pattern.
- **How to tell:** if you've run two CIS sessions and still can't say what you're building
  in a sentence, you're avoiding the decision, not making it.

## Explain It Back

Ask: *"So — when would you reach for CIS instead of going straight to BMAD Analysis?
And which agent would you call first for [their build]?"*

Listen for the fuzzy-front-end distinction. If they can name a CIS agent AND explain why
that one fits their build, that's the win.

## Scenario Check (predict, then reveal)

Three scenarios. For each: which CIS agent, if any?

> 1. *"You're three months into building. The features are clear. You're stuck on a
>    technical architecture call."* → **Not CIS** — that's Winston the Architect (Module 3)
>    and Solutioning (Module 5). CIS is pre-Analysis, not mid-build.
> 2. *"You have a rough product idea but every time you explain it, people look confused.
>    You think the problem might be in how you're framing it, not the product itself."*
>    → **Sophia** (Storyteller) to find the narrative — or **Dr. Quinn** (Problem Solver)
>    if the framing confusion hints at a deeper misdiagnosis of the problem.
> 3. *"You have a vague sense there's a business opportunity in [their domain], but you
>    haven't validated it or found the angle yet."* → **Victor** (Innovation Strategist)
>    — this is exactly the disruption-mapping / market-gap job.

Reward the reasoning. "Wrong" agent with good logic is still a win.

## Apply to Your Build

Update the **M12 line** in `MY_BUILD.md`:

> *The CIS agent I'd most want on my build right now is ____, because my situation
> is currently [problem-clear / problem-fuzzy] in this specific way: ____.*

If they're fully problem-clear: the honest answer might be "none right now, and here's
why" — that's a great answer. Knowing when *not* to use a tool is part of the skill.

## Review Hooks / Go Further

- **Install CIS:** [cis-docs.bmad-method.org](https://cis-docs.bmad-method.org) → Getting
  Started tutorial — install + run your first Carson session.
- **GitHub module:** [bmad-code-org/bmad-module-creative-intelligence-suite](https://github.com/bmad-code-org/bmad-module-creative-intelligence-suite)
- **Pairs well with:** Module 3 (Meet Your AI Crew) — CIS adds five more specialists to the
  roster; Module 4 (Think First) — where the CIS output feeds in.
- **Track 6 siblings:** Modules 10–11 (BMad Builder) are the other "level up" add-ons —
  once you've seen what CIS agents can do, you might want to build your own (Module 10).
