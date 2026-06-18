# Learn BMAD — the Method, for People Who Are Learning to Build

A self-paced, **hands-on** course that teaches you what the **BMAD Method** is, *why*
it exists, and *how* its workflow actually works — without drowning you in setup. You
don't just read about it: you reason through real scenarios and point your **own build**
through the method. Your instructor is Claude Code. This folder is self-contained — open
it in Claude Code and start from here.

> BMAD = **B**uild **M**ore, **A**rchitect **D**reams: an AI-driven development framework
> that takes you from a fuzzy idea all the way to AI agents writing the code — using
> specialized agents, guided workflows, and planning that scales to the job.

## How to get it

1. **Download** — click the green **Code** button on this page → **Download ZIP**
2. **Unzip** the file (double-click on Mac, or right-click → Extract on Windows)
3. **Open the folder** in Claude Code:
   - **Claude Code desktop app** — File → Open Folder → select `learn-bmad`
   - **VS Code with Claude Code extension** — open the folder in VS Code, then open the Claude Code panel
   - **Terminal** — `cd learn-bmad && claude`
4. **Start** — type:

```
Let's get started
```

> **Model:** Claude Sonnet works great for this course — no need for Opus.

On first run the instructor asks a few quick questions — most importantly, **the one real thing you want to build**. From then on every module applies BMAD to *your* project.

## Quick reference — commands

Any time:
- **"Menu"** / **"What's next?"** — see the module buffet and a suggested pick
- **"Module N"** / **"Jump to Module N"** — start any module, in any order
- **"Continue my course"** — resume where you left off
- **"Define X"** — plain-language definition
- **"Show my progress"** / **"Show my time"** — your checkmarks and active learning time
- **"I'm stuck on X"** — get unstuck
- **"Quiz me"** — light scenario practice (no recall drills, promise)

## This course is a buffet, not a staircase

The modules are **non-sequential**. Pick whatever you're curious about — want to know
about the dev loop? Go straight to Module 6. Each module stands on its own. There's a
recommended order if you want one (just ask), but you're free to wander.

## Course focus

- **Goal:** understand the BMAD philosophy and method well enough to run your own build
  through it — and to know how *much* method a given job needs.
- **Success looks like:** you can explain why BMAD beats one-chat "vibe coding," name
  the four phases and what each is for, and decide quick-dev vs full method.
- **Out of scope:** install/config mechanics, senior-dev depth, exam prep, writing code,
  exhaustive command references. (We point you to the official docs for those.)
- **Capstone / proof:** a one-page BMAD plan for your real project, in `MY_BUILD.md`.

## What you'll learn

The *why* behind BMAD (the five beliefs), the four-phase journey (Analysis → Planning →
Solutioning → Implementation), your specialist AI crew and Party Mode, how to right-size
the process to the work, and where to go when you're lost — all grounded in the one
thing you actually want to build.

## The 12 modules

Pick any. Order is a suggestion, not a rule.

**Track 1 · Foundations**
1. **Why BMAD Exists** — the pain of winging it, and the five beliefs that fix it.
2. **The Four-Phase Map** — the whole journey on one page.

**Track 2 · Your AI Crew**
3. **Meet Your AI Crew** — specialist agents vs one generalist; Party Mode.

**Track 3 · The Method, Up Close**
4. **Think First** — Analysis & Planning, and why vagueness gets so expensive.
5. **Decide How** — Solutioning: explicit decisions, epics, stories, the go/no-go gate.
6. **Ship It** — Implementation: the story cycle, fresh chats, review, the dev loop.

**Track 4 · Working Smart**
7. **Right-Size It** — quick-dev vs the full method; how much process is enough.
8. **Never Get Lost** — BMad-Help, the module ecosystem, and the docs map.

**Track 5 · Capstone**
9. **Your Build, the BMAD Way** — pull it all together for your real project.

**Track 6 · Level Up — Add-Ons & Build Your Own (BMad Builder)** *(bonus / advanced)*
10. **Build Your Own Teammate** — create a custom agent, including agents that remember and improve over time.
11. **Build Your Own Skill** — turn a repeatable chore into a reusable skill.
12. **Think Differently** — the Creative Intelligence Suite: five specialist agents for the fuzzy front-end, before you're clear enough to start Analysis.

## Prerequisites

- You're comfortable chatting with an AI assistant (you're here, so: yes).
- A build idea — anything you want to make. Don't have one? The instructor helps you
  pick a small one at setup.
- No coding, agile, or product-management background required. Truly beginner-first.
- Modules are short and standalone — take as many as you like, in any order.

## What's in this folder

| File | What it is |
|------|-----------|
| [README.md](./README.md) | you are here |
| [index.html](./index.html) | course landing page (open in a browser) |
| [CLAUDE.md](./CLAUDE.md) | the Claude Code instructor (this is what teaches you) |
| [LESSONS.md](./LESSONS.md) | the module index (the buffet menu) |
| [lessons/](./lessons/) | one file per module (loaded one at a time) |
| [SOURCE.md](./SOURCE.md) | canonical BMAD source of truth + docs map |
| [reference/](./reference/) | printable cheat-sheet + a light self-check quiz (no AI needed) |
| [COURSE_PLAN.md](./COURSE_PLAN.md) | how this course was designed |
| [VALIDATION.md](./VALIDATION.md) | the build's quality-check record |
| [templates/](./templates/) | user.json, progress.json, PROGRESS.md, MY_BUILD.md, GLOSSARY.md, COMPETENCY_MAP.md |

To begin, open this folder in Claude Code and say **"Let's get started."**

## A note on accuracy

This course is distilled faithfully from the official BMAD documentation
([docs.bmad-method.org](https://docs.bmad-method.org)) and [repo](https://github.com/bmad-code-org/BMAD-METHOD), but it's an independent learning aid, not an official
BMAD product. When the instructor isn't sure, it points you to the real docs rather than
guessing. [SOURCE.md](./SOURCE.md) is the source of truth.

## Privacy note

`user.json`, `progress.json`, `PROGRESS.md`, and `MY_BUILD.md` are generated locally and hold *your* details and your build idea. They are gitignored and never leave your machine.
