# VALIDATION.md — Learn BMAD

Maintainer verification record for the generated course. Run against the **actual
generated folder**, 2026-06-17.

## 1. Structural validation

| Check | Result |
|---|---|
| Required files for Claude Code runtime present | ✅ `CLAUDE.md`, `README.md`, `LESSONS.md`, `SOURCE.md`, `lessons/01–09`, `templates/*`, `reference/*`, `index.html` |
| JSON parses | ✅ `templates/progress.json`, `templates/user.json` both parse |
| Module count consistent | ✅ 11 across `progress.json` (11 sessions), `lessons/` (11 files), `LESSONS.md` (11 links), `README.md` (11), `PROGRESS.md` (11 rows), `index.html` (11 ids) |
| No unfilled `{{placeholders}}` | ✅ none (only legit React `{{ __html }}` in index.html) |
| No TODO/stub/lorem | ✅ none |
| Every lesson has the full 10-beat shape | ✅ all 9 have the 8 core `##` headings + "Where this fits" primer |
| README quick start matches adapter commands | ✅ "Let's get started", "Module N", "Menu", "Continue", "Define X" all defined in `CLAUDE.md` |
| Lessons include guided practice, explain-back, scenario check, apply, review hooks | ✅ confirmed per file |
| Per-session split + lean index | ✅ `LESSONS.md` is an index; adapter loads only the current `lessons/NN` file |
| `reference/` aids self-contained, no CDN, no model | ✅ `reference-card.html` + `quiz.html` are inline CSS/JS only |
| Model-guidance note present | ✅ in `CLAUDE.md` header, `COURSE_PLAN.md`, homepage tagline implies Claude Code |
| Homepage JSX transpiles | ✅ Babel transpile check passed |

## 2. Self-contained folder audit

- ✅ A learner can start from this folder alone — open in Claude Code, say "Let's get
  started." No dependency on the `create-course` builder repo.
- ✅ First-run setup copies every template (`user.json`, `progress.json`, `PROGRESS.md`,
  `MY_BUILD.md`, `GLOSSARY.md`, `COMPETENCY_MAP.md`) into working files.
- ✅ No private paths, no external file requirements. BMAD install is *optional* and
  only pointed to (this course teaches the method, not the setup), which is by design.
- ✅ `reference/` aids work offline in a browser with no model.

## 3. Harness-specific smoke proof (Claude Code)

- ✅ Correct adapter exists: `CLAUDE.md`.
- ✅ Commands defined: Start / Let's get started, Module N, Jump to Module N, Menu,
  What's next?, Continue/Resume, sequential|flexible mode, Help, Define X, Open the
  reference card, Quiz me, Show my progress, Show my time, Pause/Resume timer, I'm
  stuck on X, Parking lot.
- ✅ First-run path dry-run: adapter asks name → role → **build** (running example) →
  goal → success → comfort → confirms flexible/beginner-first → writes working files →
  plays back → shows module menu. Coherent against the templates.
- ✅ Resume path dry-run: loads `user.json`, finds module via `LESSONS.md` index, loads
  only that `lessons/NN` file, checks `progress.json`. Coherent.
- ✅ Uses `AskUserQuestion` for setup/checks where available; free-form fallback allowed.
- ⚠️ **Runtime-proof limit:** verified by reading the adapter against the generated
  files (structural proof). A live end-to-end teaching run was not executed in this
  build session. No blocker — the wiring is internally consistent.

## 4. Adversarial coherence review (skeptical learner + maintainer pass)

Findings and dispositions:

- **Non-sequential promise vs. a framework built around "sessions."** *Fixed/accepted:*
  every lesson opens with a standalone "Where this fits" primer so a cold jump works;
  `navigation.mode` defaults to `flexible`; README/PROGRESS/menu all frame a buffet.
  `progress.json` keeps the field name `sessions` (framework requirement) but everything
  learner-facing says "Module." Accepted as a known, documented naming bridge.
- **Homepage component says "Session N of TOTAL" in the detail view.** *Accepted with
  rationale:* the generic component uses "Session"; the curriculum blurb and all course
  prose say "Module." Low-impact cosmetic; not worth forking the vendored component.
- **Could a learner over-index on setup?** *Mitigated:* adapter + SOURCE explicitly keep
  install light and redirect to the Docs Map; "no setup rabbit-holes" is a guardrail.
- **Risk of the instructor inventing BMAD behavior.** *Mitigated:* "Answering BMAD
  questions" rule in `CLAUDE.md` mandates SOURCE-or-Docs-Map, never guess; SOURCE §10
  flags fidelity limits (e.g. Scrum Master/QA names left unnamed; Dev Loop Automation
  marked roadmap).
- **Brainstorming misframing risk** (AI generating ideas vs. coaching). *Verified fixed:*
  Module 4 states the AI is a coach pulling ideas *out of you*, not generating them.
- **Capstone must ship the running example.** *Verified:* Module 9 walks the learner
  through completing the "one-page BMAD plan" checklist in `MY_BUILD.md`.
- **Undefined jargon.** *Mitigated:* `GLOSSARY.md` covers PRD, ADR, epic, story,
  readiness gate, agent, Party Mode, quick-dev, etc.; adapter defines on first use.

## 5. Coverage vs. the owner's brief

| Owner ask | Covered in |
|---|---|
| Teach the philosophy + the method (not just philosophy) | M1 (beliefs) + M2–M6 (the method) |
| Not exam-y; fewer quizzes; more scenarios | Light "predict-then-reveal" checks only; no recall drills; quiz.html is a no-stakes gut-check |
| Interactive, scenario-driven, "how to build different things" | Every module = do-first + apply-to-your-build + scenario |
| Go through the phases, grounded in purpose | M2 map + M4/M5/M6 deep-but-light |
| How guided workflows go / dev loop automation | M6 (build cycle, dev loop) + M7 (quick-dev) |
| How BMAD is different | M1 (vs vibe coding) threaded throughout |
| Don't focus on setup | Guardrail; redirect to Docs Map |
| Answer questions from docs or point to the right place | "Answering BMAD questions" rule + SOURCE §9 Docs Map |
| Beginners learning to build (not senior devs) | Beginner-first mode, no code shown, jargon defined |
| Non-sequential, pick-a-module | Flexible default; standalone modules; buffet framing |
| Fun, lighthearted | Wry tone baked into adapter + every lesson |
| Distilled, not ginormous | 12 short modules (9 core + 3 bonus: BMad-Builder ×2 + CIS); no per-module time predictions (owner decision) |
| Meet-the-team is fun/game-like (owner request) | M3 rewritten: in-character intros, "lineup changes" caveat, "Draft Your Crew" scenario game |
| Practical BMad-Builder sessions (owner request) | M10 (build an agent + memory) + M11 (build a skill); SOURCE §6.5 added |

## 6. Outstanding / next actions

- None blocking. Optional future polish: a live end-to-end teaching run to upgrade §3
  from structural proof to runtime proof; optional GitHub Pages deploy (skipped — repo
  is private).

## 7. Adversarial review pass (BMAD reviewer, read-only) + dispositions

A read-only BMAD-style adversarial review (channeling John/PM + "you must find issues")
ran against the curriculum and the official docs. Findings were triaged against the actual
files before acting — several "Critical" findings were verified to be reviewer misreads
(citation-checked per the orchestrator's review discipline).

**Verified-and-fixed (valid findings):**
- Glossary "Adversarial review" mis-cited a teaching module (it's a background concept, not
  taught in a module) → relabeled "Background concept (SOURCE §7)."
- Glossary "BMad-Help" definition missing the auto-runs-at-end-of-every-workflow fact → added.
- `LESSONS.md` Module 4 descriptor didn't flag it covers two phases → added "(Phases 1 & 2)".
- Party Mode "only uses installed agents" caveat → added in M3.
- M3 primer assumed prior modules (broke the standalone/non-sequential promise) → rewritten
  to be fully standalone (also satisfies the owner's "make it fun/game-like" request).

**Rejected (reviewer misreads — verified against files):**
- "M6 omits the 3-step cycle / doesn't flag Dev Loop Automation as roadmap" → FALSE: M6
  states the cycle (create-story → dev-story → code-review, retro per epic) and flags the
  roadmap caveat (lines 58–61, 111–112).
- "LESSONS.md lists Party Mode under Module 8" → FALSE: it's under Module 3, correctly.
- "M4 doesn't flag Analysis as optional" → FALSE: M4 says so explicitly (twice).
- "M1 mis-cross-references adversarial review to Module 7" → FALSE: M1 correctly maps
  scale-rigor→M7 and specialists→M3.
- "quick-dev is missing a 'present results' step" → REJECTED as unsourced: SOURCE §4 lists
  clarify→plan→implement→review; "present results" is not in SOURCE, so not asserted.

**Accepted with rationale:**
- M9 capstone cold-start needing a populated `MY_BUILD.md`: first-run setup captures the
  build *before* any module is chosen, so the file is populated regardless of entry point.

## 8. Post-review additions (owner requests, 2026-06-17)

- **Module 3 → "Meet the BMAD Team"**: rewritten as the fun, character-driven, game-like
  module (in-character intros, when-to-use each, the lineup-changes caveat, "Draft Your
  Crew" scenario game). Faithful to SOURCE §3.
- **Module 10 — Build Your Own Teammate** and **Module 11 — Build Your Own Skill**: new
  bonus "Level Up" track on BMad Builder. Grounded in SOURCE §6.5 (added), itself sourced
  from the BMB README + customize-bmad docs. Persistent memory / self-learning agents are
  taught at concept level with an explicit fidelity flag (new/evolving → point to BMB docs);
  no mechanics invented.
- **Time predictions removed** from all modules (owner decision); active-time *tracking*
  retained (it measures real time, not a prediction).
