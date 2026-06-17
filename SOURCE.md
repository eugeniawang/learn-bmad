# SOURCE.md — The BMAD Method (canonical source of truth)

> This is the source of truth for the whole course. If a lesson and this file
> disagree, **this file wins.** Everything here is distilled faithfully from the
> official BMAD documentation (see the Docs Map at the bottom). Where the docs are
> uncertain or evolving, this file says so rather than guessing.
>
> Course note: this course teaches the BMAD **philosophy and method** — the *why*
> and the *shape of the workflow*. It deliberately does **not** teach installation
> or configuration in depth. When a learner wants setup detail, point them at the
> Docs Map.

---

## 0. The one-paragraph version

**BMAD = Build More, Architect Dreams.** It is an AI-driven development framework
that helps you build software across the *whole* journey — from a fuzzy idea, through
planning, all the way to AI agents writing the code. Instead of one AI improvising
everything in a single chat ("vibe coding"), BMAD gives you **specialized AI agents**,
**guided workflows**, and **planning that scales to the size of the job** — anything
from a one-line bug fix to an enterprise platform. If you're comfortable working with
an AI coding assistant (Claude, Cursor, Copilot), you're ready to use it.

---

## 1. Why BMAD exists (the philosophy)

The problem it solves: when you hand a big, vague request to a single AI in one long
chat, predictable things go wrong. LLMs **misread intent**, **fill gaps with
confident guesses**, **drift into unrelated work**, and **produce noisy output**. The
bigger the build, the more these small errors compound.

BMAD's answer is a set of beliefs baked into the workflow:

- **Plan before you build.** A little structured thinking up front prevents a lot of
  expensive rework. Vagueness compounds: a vague idea → a vague PRD → wrong
  architecture bets → stories that miss edge cases. The cost grows at every step.
- **Make decisions explicit.** When technical decisions are written down, every agent
  (and every future chat) implements *consistently*. Implicit decisions made
  independently by different agents = an integration nightmare.
- **Scale the rigor to the change.** A typo fix should not require a Product
  Requirements Document. A new platform should. BMAD lets you apply *as much or as
  little* process as the work deserves.
- **Use specialists, not one generalist.** A dedicated analyst, PM, architect, and
  developer each do their job better than one AI trying to wear every hat at once.
- **Keep the human in the loop — at the moments that matter.** Human attention is the
  bottleneck. BMAD spends it on high-value decisions (clarify the intent, approve the
  spec, review the result) and lets the AI run between them.

**The mental shift:** you stop being the person typing every instruction, and become
the person *directing a team* and *approving the important calls*.

---

## 2. The Four Phases (the method)

BMAD organizes a build into four phases. You don't always use all four — small work
skips most of them (see §4, Scale-Adaptive). But the full arc looks like this:

| Phase | Name | The question it answers | What it produces |
|---|---|---|---|
| 1 | **Analysis** | "Do I understand the problem?" | Sharper thinking (brief, research) — *optional but valuable* |
| 2 | **Planning** | "**What** should we build, and **why**?" | A PRD (Product Requirements Document) |
| 3 | **Solutioning** | "**How**? Then **what units of work**?" | `architecture.md` (with ADRs), epics & stories, a readiness gate |
| 4 | **Implementation** | "Build it." | Working software, one story at a time |

**Each workflow should run in a fresh chat.** This keeps context clean and stops the
AI from dragging stale assumptions between steps.

### Phase 1 — Analysis (optional, but it sharpens everything)

Helps you think clearly *before* committing to build. Every tool here is optional, but
skipping analysis entirely means your PRD is built on assumptions instead of insight.

- **Brainstorming.** A facilitated creative session. The AI acts as a *coach pulling
  ideas out of you* through structured techniques — it does **not** generate the ideas
  for you. Best when you have a problem but no clear solution yet.
- **Market / competitor / customer research and feasibility.** Attack the problem from
  different angles so that by the time you sit down to plan, you know *what* you're
  building and *for whom*.

Why it's first: "A PRD answers 'what should we build and why?' If you feed it vague
thinking, you get a vague PRD — and every downstream document inherits that vagueness."

### Phase 2 — Planning (What & Why)

Turn the sharpened idea into a **PRD** — the document that states what to build and
why. This is the contract the rest of the project is measured against. (For small
work you can jump straight here, or skip to quick-dev — see §4.)

### Phase 3 — Solutioning (How, then what units of work)

| Workflow | Purpose | Produces |
|---|---|---|
| `bmad-create-architecture` | Make technical decisions explicit | `architecture.md` with ADRs (Architecture Decision Records) |
| `bmad-create-epics-and-stories` | Break requirements into implementable work | Epic files, each with stories |
| `bmad-check-implementation-readiness` | A gate check before building | A PASS / CONCERNS / FAIL decision |

**Why solutioning matters (the killer example):** if several agents implement
different parts of a system with no shared architectural guidance, they each make
independent technical decisions that conflict — e.g. one uses REST, another GraphQL.
Result: integration nightmare. With solutioning, the architecture decides ("Use
GraphQL for all APIs"), every agent follows it, and integration is straightforward.

Planning asks *What & Why*; Solutioning asks *How, then what units of work*.

### Phase 4 — Implementation (build it, one story at a time)

Once planning is done, you build. **Each step runs in a fresh chat.**

- **Once per project:** run `bmad-sprint-planning` → creates `sprint-status.yaml`,
  which tracks all epics and stories.
- **The build cycle, repeated per story:**

| Step | Workflow | Purpose |
|---|---|---|
| 1 | `bmad-create-story` | Create a story file from the epic |
| 2 | `bmad-dev-story` | Implement the story |
| 3 | `bmad-code-review` | Quality validation *(recommended)* |

- **After all stories in an epic:** run `bmad-retrospective`.
- **Dev Loop Automation** (running the build cycle with less hand-holding) is a
  headline item on the V6 roadmap — "coming soon," with early pieces landing.

---

## 3. The agents (your specialized AI crew)

BMAD ships specialized agent personas. Each has a name, a role, and a focus. Confirmed
named agents:

| Agent | Name | Role focus |
|---|---|---|
| Analyst | **Mary** | Requirements, research, thinking clearly about the problem |
| Product Manager | **John** | PRD creation, requirements discovery |
| Architect | **Winston** | System/technical design, architecture decisions |
| UX Designer | **Sally** | UX patterns and UI specs |
| Developer | **Amelia** | Story execution, writing the code |
| Tech Writer | **Paige** | Documentation, knowledge curation |

There are also **Scrum Master** and **QA / Test** roles in the cycle. (This course
doesn't lean on their persona names; the role is what matters.)

### Party Mode (`bmad-party-mode`)

Your whole AI team in one room — PM, Architect, Dev, UX, whoever you need. Party Mode
orchestrates the discussion, picking the relevant *installed* agents per message.
Agents respond **in character** — they agree, disagree, and build on each other's
ideas. It's a real back-and-forth that continues as long as you want.

**Good for:** big decisions with tradeoffs · brainstorming · post-mortems when things
go wrong · sprint retrospectives and planning.

---

## 4. Scale-Adaptive: match the process to the job

You do **not** always run the full four phases. BMAD adapts:

| Scope of change | Recommended approach |
|---|---|
| **Small updates or additions** | Run `bmad-quick-dev` — clarify intent, plan, implement, and review in a *single* workflow. The full four-phase method is likely overkill. |
| **Major changes or additions** | Start with the full BMad Method, applying as much or as little rigor as needed. |

### Quick Dev (`bmad-quick-dev`) — the philosophy of fewer, better checkpoints

The premise: **human-in-the-loop turns are necessary but expensive.** Constant
intervention throttles velocity; zero intervention lets the AI's predictable failures
run wild. Quick-dev rebalances this — it lets the model run unsupervised for longer,
but only *after* the workflow builds a strong enough boundary to make that safe.

Its design:

1. **Compress intent first.** Human and model squeeze the request into *one* coherent
   goal — small enough, clear enough, and contradiction-free enough to execute. Intent
   can start as a couple of phrases, a bug-tracker link, plan-mode output, or even a
   story number.
2. **Route to the smallest safe path.** A true one-shot, zero-blast-radius change can
   go straight to implementation; bigger ones take the fuller path.
3. **Relocate human control to high-value moments only:** intent clarification, spec
   approval, and review of the final product.

This is the same belief as the whole method, in miniature: spend human judgment where
it changes the outcome, automate the rest.

---

## 5. BMad-Help: the front door (so you never get lost)

**The fastest way to get started, and the cure for "where do I even begin?"** Run the
`bmad-help` skill (optionally with a question) and it will:

- **Inspect your project** to see what's already been done.
- **Show your options** based on which modules you have installed.
- **Recommend what's next** — including the first required task.
- **Answer questions** like "I have a SaaS idea, where do I start?" or "I have an
  existing Rails app, where should I start?"

Crucially, **BMad-Help also runs automatically at the end of every workflow**, telling
you exactly what to do next. No memorizing phases, no hunting through docs.

> Tip from the docs: right after installing BMAD, invoke `bmad-help` immediately. It
> detects your installed modules and points you to the right starting point.

---

## 6. The module ecosystem (BMAD is bigger than dev)

BMAD is a core method plus optional modules. You install what you need.

| Code | Module | What it adds |
|---|---|---|
| **BMM** | BMad Method | The core dev framework: the four phases, the agents, the build cycle |
| **CIS** | Creative Intelligence Suite | Innovation Strategist, Design Thinking Coach, Brainstorming Coach, Problem Solver, Storyteller, Presentation Master; frameworks like SCAMPER and Reverse Brainstorming |
| **GDS** | Game Dev Studio | Game-specific workflows (Unity, Unreal, Godot, custom); Game Design Document workflow; Quick Flow; 21+ game types |
| **TEA** | Test Architect | An expert agent (**Murat**) + 9 workflows for enterprise testing: strategy, risk-based planning, quality gates, requirements traceability |
| **BMB** | BMad Builder | Build and customize your own agents and skills |

There's also a lightweight **built-in QA** for quick test coverage on small/medium
projects — handy when full TEA is more than you need.

**Install channels:** `stable` (default — latest released version), `next` (the main
branch, for early adopters), `pinned` (a specific version, for reproducibility).

---

## 6.5 Building your own — BMad Builder (BMB), up close

BMB is the **meta-module**: the part of BMAD you use to *extend BMAD itself*. With
guided assistance, it gives you "the complete pipeline to create your own AI modules and
skills" — then share them via the BMad Marketplace (or any compliant marketplace).

What you can build with it:

- **Agents** — your own specialist personas (role, persona, communication style, and a
  menu of things they can do). The docs frame these as everything from **domain experts**
  (legal, medical, creative, technical) to **personal AI companions**.
- **Skills** — self-contained capabilities built on the **open Agent Skills standard**, so
  they work across 40+ AI tools, not just BMAD. (In BMAD, an agent is essentially a
  persona plus a *menu of skills/workflows* it can run.)
- **Workflows** and **full modules** — bundle agents + workflows into shareable packages.

### Persistent memory — "agents that learn" (newer; evolving)

BMB's headline feature for agents is **persistent memory**: per the BMB docs, agents can
**"remember across sessions and keep improving."** That's the "self-learning agent" idea —
a personal AI companion whose memory **evolves with you over time**, rather than starting
cold every chat.

A related-but-distinct knob exists on regular BMAD agents: **`persistent_facts`** — static
facts an agent always keeps in mind (org rules, domain constants, your preferences), set
in a TOML override. The docs explicitly note these static facts are **distinct from the
runtime memory sidecar** (the evolving memory). So there are two layers worth separating:

| Layer | What it is | Changes over time? |
|---|---|---|
| **`persistent_facts`** | Static facts you hand the agent up front (literal lines or `file:` refs) | No — you edit them |
| **Persistent memory / runtime memory** | What the agent remembers and refines across sessions | Yes — it evolves |

> **Fidelity flag:** persistent memory / self-learning agents are a **new and evolving**
> part of BMB. This course teaches the *concept and the BMAD process* at a high level;
> for exact mechanics (how memory is stored, synced, and reset) send learners to the BMB
> docs (`bmad-builder-docs.bmad-method.org`) — do **not** invent specifics.

### Build vs. customize (don't confuse them)

- **Build a NEW agent/skill/module** → that's **BMad Builder (BMB)**.
- **Tailor an EXISTING agent/workflow** (change a persona, add facts, tweak the menu)
  without editing installed files → that's the **`bmad-customize`** helper, which writes
  TOML override files under `_bmad/custom/`. Customizations survive updates.

## 7. Supporting ideas worth knowing

- **Adversarial review.** A review technique where the reviewer *must* find issues —
  no "looks good" allowed. It adopts a cynical stance to break confirmation bias.
  Zero findings triggers a halt: re-analyze or justify. It forces thoroughness and
  catches what's *missing*, not just what's wrong.
- **`project-context.md`.** A file (default location `_bmad-output/project-context.md`)
  holding project context and AI rules. Workflows look for it so agents share the same
  understanding of your project.
- **Fresh chat per workflow.** A recurring discipline: each workflow runs in its own
  chat so context stays clean and stale assumptions don't leak across steps.
- **Quick Flow vs Full Method.** "Quick flow" = the fast, single-workflow path for
  small work. "Full method" = the four-phase path for substantial work.

---

## 8. How to actually start (high level — details live in the docs)

1. You need an AI IDE / assistant you're comfortable with (Claude Code, Cursor, etc.).
2. Install BMAD (`npx bmad-method install`) and select the modules you want.
3. Invoke **`bmad-help`** immediately — it tells you where to start for *your* project.
4. For small work, reach for **quick-dev**. For a real product, walk the four phases:
   Analysis → Planning → Solutioning → Implementation, each in a fresh chat.

> This course intentionally keeps setup light. When a learner wants the exact install
> and configuration steps, send them to the Getting Started tutorial in the Docs Map.

---

## 9. Docs Map (answer questions from here, or point learners here)

When a learner asks something this course doesn't cover, **answer from this SOURCE if
it's here; otherwise point them to the exact place below** rather than guessing.

| You want… | Go to |
|---|---|
| The docs home | https://docs.bmad-method.org/ |
| Install + first run | https://docs.bmad-method.org/tutorials/getting-started |
| Why analysis matters | https://docs.bmad-method.org/ (Explanation → Analysis Phase) |
| The Quick Dev philosophy | https://docs.bmad-method.org/ (Explanation → Quick Dev) |
| Solutioning deep-dive | https://docs.bmad-method.org/ (Explanation → Solutioning) |
| Adversarial review | https://docs.bmad-method.org/ (Explanation → Adversarial Review) |
| The roadmap (V6, Dev Loop Automation) | https://docs.bmad-method.org/roadmap/ |
| BMad Builder (build agents/skills/modules) | https://bmad-builder-docs.bmad-method.org |
| BMad Builder — build your first module | https://bmad-builder-docs.bmad-method.org/tutorials/build-your-first-module/ |
| Customize an existing agent (TOML overrides) | https://docs.bmad-method.org/how-to/customize-bmad |
| The BMad Marketplace (share what you build) | https://github.com/bmad-code-org/bmad-plugins-marketplace |
| Everything, in one file (for AI) | https://docs.bmad-method.org/llms-full.txt |
| The source code | https://github.com/bmad-code-org/BMAD-METHOD |

---

## 10. Source & fidelity notes

- Distilled from the official BMAD Method documentation (`docs.bmad-method.org`,
  including `llms-full.txt`, generated 2026-06-07) and the public repo. BMAD is V6 at
  time of writing; some Phase-4 automation ("Dev Loop Automation") is on the roadmap
  and labeled "coming soon" in the docs — this course flags that rather than implying
  it's fully shipped.
- Confirmed agent names (Mary, John, Winston, Sally, Amelia, Paige) come from the
  installed BMAD agent skill set. Scrum Master / QA persona names are intentionally
  left unnamed here to avoid asserting anything the source didn't confirm.
- This course is an independent learning aid, not an official BMAD product.
