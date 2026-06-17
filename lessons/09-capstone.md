# Module 9 — Your Build, the BMAD Way

> **Where this fits:** This is the capstone — you're turning everything into a one-page
> BMAD plan for your actual build. It works best after a few modules (more lines in
> `MY_BUILD.md` = richer plan), but it's fully doable as a standalone if you jumped
> straight here. **The point:** you leave with a real artifact — not notes about BMAD,
> but a plan for *your thing*, ready to hand to an AI crew tomorrow.

*Source: SOURCE.md §2 (four phases), §4 (right-sizing). Instructor: no new theory here —
just the build. Doing is the lesson.*

---

## Do This First

Before any recap, dive straight into the build. Open `MY_BUILD.md` and look at "The
build" section at the top.

Now write — right now, don't overthink it — **one paragraph** answering:

> *What am I building, for whom, and why does it matter that it exists?*

Don't polish. Don't qualify. One paragraph, present tense, written like you're pitching
it to a collaborator who's never heard of it. That paragraph is going into the capstone
in a moment.

## What Just Happened

You just wrote the seed of a PRD — the thing Phase 2 of the full BMAD method calls
"the contract the rest of the project is measured against." If it felt hard to write,
that's useful data: vagueness there compounds into every downstream decision. If it
felt easy, you've been thinking clearly. Either way, you have something real.

## The Idea

Four-line crash course for anyone joining cold:

1. **Plan first.** A little structure up front prevents a lot of expensive wrong turns.
2. **Right-size the process.** Small change → `bmad-quick-dev`. Real product → walk the
   four phases: Analysis → Planning → Solutioning → Implementation.
3. **Make decisions explicit.** Written-down calls mean every agent (every fresh chat)
   builds the *same* thing. Implicit decisions made independently = integration
   nightmares.
4. **Build in slices.** One story at a time, each in a fresh chat, one concrete thing
   shipped before the next starts.

That's the whole method. The capstone is just applying it to your build on purpose.

## Pattern / Anti-pattern

- ✅ **Pattern:** fill this one-pager *before* you open a dev chat — so the first
  message an AI sees is "here's the plan, here's the first story" instead of "here's a
  vague idea, good luck."
- ❌ **Anti-pattern:** keep the plan in your head, figure it out as you go, react to
  whatever the AI produces. (You know what that's called.)
- **How to tell which you're in:** if the AI could implement your build without asking
  you a single clarifying question, the plan is real. If it would have to guess on the
  first move, it isn't yet.

## Explain It Back

Ask yourself: *"If someone handed me this one-pager and said 'run it' — what's the
first thing I'd do, and why?"*

If the answer is immediate and specific ("start Phase 2, run `bmad-create-story` on
slice #1"), the plan is tight. If the answer is "...figure out the architecture first?"
— that's a signal that Phase 3 / solutioning needs a line in your plan.

## Scenario Check (light — predict, then reveal)

Quick sanity check on your own plan. Predict first, then read the reveal.

> **If you handed this one-pager to an AI crew tomorrow morning, what's the one thing
> that's still too vague for them to make a real decision — the thing they'd have to
> guess?**

Write down your answer before reading on.

*(Reveal: it's almost always the architecture/approach call — the "how" that locks in
everything else. If you haven't named it explicitly, two agents implementing different
parts will make that call independently and get different answers. That's exactly what
Phase 3 solutioning exists to prevent. Check your "First explicit decision" box. Is it
there? Is it specific enough that the AI can't interpret it two ways? If not, tighten
it.)*

## Apply to Your Build

This IS the capstone. Open `MY_BUILD.md` and work through the checklist in
**"Capstone — my one-page BMAD plan"**, one box at a time.

**[ ] What & why** — paste (and tighten) the paragraph you wrote in "Do This First."
One paragraph, specific enough to be a contract.

**[ ] Phases I'll use** — look at the four phases (Analysis → Planning → Solutioning →
Implementation) and decide out loud which ones your build actually needs and which
you're skipping, with a one-line reason each. "Skip Analysis — I've been thinking about
this for months, assumptions are clear" is a perfectly good answer. So is "Do all
four." The point is that *you decided*, not that the phases decided for you.

**[ ] Right-sized** — pull your M7 line from `MY_BUILD.md`. Is this a quick-dev job
(small, clear, low blast radius) or a full-method job (real product, multiple moving
parts)? Write it as a decision, not a hedge: "quick-dev, because X" or "full method,
because Y."

**[ ] First explicit decision** — pull your M5 line. One architecture or approach call
you're locking in before the first dev chat. Not "I'll figure it out." Not "probably X."
Locked. Written. Done.

**[ ] First slice** — pull your M6 line. The first story or two you'd actually build.
Small enough to ship in one session; real enough that it proves the thing exists.

**[ ] My next real step** — one sentence, concrete, time-bound. "Open a fresh chat,
invoke `bmad-help`, describe the build, ask where to start" is a perfectly valid next
step. So is "run `bmad-quick-dev` on slice #1 tonight." It must be a step you can
actually take this week, not a direction.

When all six boxes are checked, fill in: **"Where this plan lives / how I'll use it."**
Dropbox, Notion, pinned in your repo — wherever you'll actually open it before the
next dev session.

## Review Hooks / Go Further

That's it. You built the plan.

A few things to do with it:

- **Any line in `MY_BUILD.md` still blank?** That's the module to revisit — not
  because the course requires it, but because a blank line is an unresolved question
  your AI crew will have to guess the answer to.
- **Ready to do it for real?** Invoke `bmad-help` (SOURCE §5) — it inspects your
  project, shows what's already done, and tells you exactly what to do next. It also
  runs automatically at the end of every workflow, so you never have to remember which
  phase comes after which. Start there.
- **Want to go deeper?** The Docs Map (SOURCE §9) has a link for every question this
  course didn't answer — the Getting Started tutorial, the Quick Dev philosophy, the
  Solutioning deep-dive, the full roadmap.

Go build something real.
