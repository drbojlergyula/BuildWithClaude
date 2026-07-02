<!-- repo-description: A starter template that gives your project an AI team — advisor, spec reviewer, QA, and researcher — plus guided workflows, from the first prompt. -->

# BuildWithClaude

**Your project, with an AI team included.**

A starter template for building software with Claude Code — designed for business owners, founders, and non-technical builders. Clone it, open it, and Claude greets you, interviews you about your idea, writes your project documents, and introduces the team of AI specialists that now works for you.

> Looking for the multi-assistant version (Claude Code + Codex + GitHub Copilot)? Use **BuildWithAI** — same team, works across tools. This repo is the simple, Claude-only on-ramp.

---

## What makes it different

Most templates give you empty folders. This one gives you **staff**:

| Your team member | What they do |
|---|---|
| 🧭 **project-advisor** | Senior advisor. Reviews everything, surfaces blind spots, tells you what to focus on next — and *remembers its advice between sessions*. |
| 🔍 **spec-reviewer** | Requirements analyst. Catches gaps in your plan on paper, where they are cheap to fix. |
| ✅ **build-verifier** | QA engineer. After Claude builds something, this agent independently runs it and proves it works. |
| 🌐 **research-analyst** | Market researcher. Investigates competitors, pricing, and technology choices on the live web and files a cited brief. |

Plus guided workflows for the whole life of the project:

`/start` → `/new-feature` → `/fix-bug` → `/update-docs-and-commit` → `/put-me-in-context` → `/doc-sync-check` → `/go-live`

And one signature move: type **`/put-me-in-context`** and anyone — you after a holiday, a new teammate, a contractor — gets a full project briefing in seconds. Every decision lives in AI-readable docs, so the knowledge never walks out the door.

---

## Quick start

**1. Get the tools**

- [Git](https://git-scm.com) — saves and versions your project
- [VS Code](https://code.visualstudio.com) — free code editor
- [Claude Code](https://claude.com/claude-code) — install the CLI or the VS Code extension
- A free account at [github.com](https://github.com)

**2. Copy this template**

On the GitHub page, click **"Use this template" → "Create a new repository"**, name it, and click Create.

**3. Download it**

Open VS Code, open the Terminal (**View → Terminal**), and run:

```
git clone https://github.com/YOUR-USERNAME/YOUR-PROJECT-NAME.git
```

Then open the folder in VS Code (**File → Open Folder**).

**4. Open Claude Code — and just say hello**

The template knows it is brand new. Claude will welcome you and offer to set everything up. Or jump straight in:

```
/start
```

Claude interviews you about your idea (5–10 minutes), fills in every project document, proposes a technology stack and an MVP plan, then introduces your AI team.

**5. Build**

> "Build the order form described in the project spec."

---

## Day to day

| When | Do this |
|---|---|
| Need a full project summary | `/put-me-in-context` |
| Adding something new | `/new-feature` (you can even type `/new-feature customers can pay by card`) |
| Something is broken | `/fix-bug` — reproduce, fix, verify, record |
| Finished a piece of work | `/update-docs-and-commit` |
| Feeling stuck or unsure | "Run the project-advisor agent" |
| About to build from the spec | "Run the spec-reviewer agent" |
| Just built a feature | "Run the build-verifier agent" — independent QA |
| Need outside facts | "Run the research-analyst agent" — e.g. "what do competitors charge?" |
| Docs feel stale | `/doc-sync-check` |
| Ready to launch | `/go-live` — Go / No-Go readiness report |

---

## What's in the box

```
BuildWithClaude/
├── CLAUDE.md                    ← Claude reads this every session
├── docs/                        ← Your project's long-term memory
│   ├── project_spec.md          ← What you are building and why
│   ├── architecture.md          ← How it is structured
│   ├── brainstorm.md            ← Ideas before they are decisions
│   ├── project_status.md        ← Progress and milestones
│   └── changelog.md             ← History of changes
└── .claude/
    ├── agents/                  ← Your AI team (4 specialists)
    ├── skills/                  ← Guided workflows (7 slash commands)
    ├── rules/                   ← Modular conventions Claude always follows
    ├── hooks/                   ← The welcome-on-open magic
    └── settings.json            ← Safe permission defaults + hook wiring
```

Everything is plain Markdown with YAML frontmatter — current Claude Code formats (Agent Skills open standard, real subagents, SessionStart hooks). Open any file to see how it works; edit it in plain English to make it yours.

All files are pre-filled with a working example. `/start` replaces the example with your actual project.

---

## Questions or issues?

Describe what you expected and what happened instead — Claude can diagnose and fix most problems directly. If the docs ever drift from reality, `/doc-sync-check` finds it.

---
*Built to solve the bus-factor problem. One prompt: `/put-me-in-context`.*
