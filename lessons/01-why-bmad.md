# Module 1 — Why BMAD Exists

> **Where this fits:** This is the "why bother" module. You need nothing before it — it's
> a great first taste, but it also stands alone if you wandered in from the menu.
> **The point:** by the end you'll be able to say, in your own words, why throwing a big
> vague request at one AI tends to go wrong — and the five beliefs BMAD uses to fix it.

*Source: SOURCE.md §0–§1. Instructor: keep it to a few lines per turn. Do before tell.*

---

## Do This First

Before any theory — a tiny thought experiment. Ask the learner (personalize to their
build from `MY_BUILD.md`):

> Imagine you open one fresh AI chat and type: **"Build me [their build idea]."** Just
> that. One sentence, one chat, go.
> **What are the top two ways you think that goes wrong?**

Let them answer first. Don't lead the witness.

## What Just Happened

Whatever they said, it almost certainly lands in one of four buckets. These are the
*predictable* ways LLMs fail on big vague asks (straight from the BMAD docs):

- **Misreads what you meant** (builds the wrong thing, confidently).
- **Fills gaps with guesses** (invents details you never decided).
- **Drifts** (wanders into stuff you didn't ask for).
- **Gets noisy** (so much output you can't tell what's right).

The kicker: on a *big* build, these tiny errors **compound**. A wrong guess in step one
becomes three wrong things by step five. This is the chaos BMAD exists to kill.

## The Idea

BMAD's whole personality is **five beliefs**. Introduce them as the antidote to what just
went wrong — one line each:

1. **Plan before you build.** A little thinking up front beats a lot of rework later.
2. **Make decisions explicit.** Written-down decisions = everyone (every agent, every
   future chat) builds the *same* thing.
3. **Scale rigor to the change.** A typo doesn't need a 12-step process; a platform does.
4. **Use specialists, not one generalist.** A dedicated analyst, architect, and developer
   each beat one AI wearing all the hats.
5. **Keep the human in the loop — where it matters.** Spend your attention on the big
   calls; let the AI run the rest.

> Define on first use: **"vibe coding"** = the one-chat, wing-it approach above. Not evil,
> just fragile once the build gets real.

The mindset flip to name out loud: **you stop being the person typing every instruction,
and become the person directing a team and approving the important calls.**

## Pattern / Anti-pattern

- ✅ **Pattern:** name the build, decide the few things that matter, then let AI execute
  against those decisions.
- ❌ **Anti-pattern:** "Build me the whole thing" in one breath, then play whack-a-mole
  with everything it got wrong.
- **How to tell which you're in:** if you can't point to a single written-down decision
  the AI is building *against*, you're vibe coding.

## Explain It Back

Ask: *"In one or two sentences — why does BMAD plan first instead of just letting the AI
go?"* Listen for the **compounding** idea (small early errors snowball). If they miss it,
give one concrete example from their own build and ask again.

## Scenario Check (light — predict, then reveal)

Give them a realistic mess and ask which belief would've saved it:

> "Someone one-chatted a food-delivery app. Halfway through, the AI had built two
> different login systems that don't talk to each other. **Which of the five beliefs
> would've prevented this — and why?**"

Let them pick and explain. *(Reveal: belief #2, make decisions explicit — one written
'this is how login works' decision means every part builds against it. Belief #4 helps
too: an architect would've owned that call.)* Reward the reasoning, not the exact number.

## Apply to Your Build

Update the **M1 line** in `MY_BUILD.md`:

> *On my build, the place where "just wing it in one chat" would bite me hardest is: ____*

Draft a first version *for* them from their build details, then let them edit it.

## Review Hooks / Go Further

- **Revisit later:** the five beliefs reappear everywhere — flag belief #3 (scale rigor)
  as the star of Module 7, and #4 (specialists) as the star of Module 3.
- **Pairs well next:** **Module 2 — The Four-Phase Map** (now that you know *why*, see the
  *shape*). Or jump to whatever itches.
- **If they ask "so how do I actually start using BMAD?"** → that's setup; point to the
  Getting Started tutorial (SOURCE §9) and offer Module 8 (Never Get Lost).
