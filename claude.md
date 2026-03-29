# CLAUDE.md

This file is read by Claude Code at the start of every session. It provides context about the project structure, available tools, and working conventions.

## Overview

This is a business-focused project template for building with Claude Code. It includes documentation templates and pre-built Claude tools — all using a Dream Home Design interior design website as the example to replace. Run `/start` to replace all example content with the user's real project.

## Documentation

| File | Purpose |
|---|---|
| [docs/project_spec.md](docs/project_spec.md) | What is being built, who it is for, features, tech stack, API design |
| [docs/architecture.md](docs/architecture.md) | System design, data flow, component breakdown, file structure |
| [docs/brainstorm.md](docs/brainstorm.md) | Scratchpad for ideas before they are ready for the spec |
| [docs/project_status.md](docs/project_status.md) | Current progress, active phase, upcoming milestones |
| [docs/changelog.md](docs/changelog.md) | Version history and notable changes |

**Update docs after every major milestone or addition.** The spec and architecture are the primary source of truth — keep them accurate so context does not need to be re-explained each session.

## Claude Tools

Tools live in `.claude/` as plain-English text files. To create a new tool, add a file to the relevant folder describing what Claude should do, step by step — in plain English.

**Agents** are specialist personas given a specific job. Invoke by asking Claude to "run the [name] agent."
**Commands** are shortcut tasks triggered by typing `/command-name`.
**Skills** are repeatable checklists invoked by asking Claude to "run the [name] skill."

### Commands (`.claude/commands/`)

| Command | Description |
|---|---|
| `/start` | Interviews the user, populates all project docs, sets up the project from scratch |
| `/new-feature` | Guided workflow for adding a new feature to the spec with user stories and version assignment |
| `/update-docs-and-commit` | Updates changelog and project status to reflect recent work, then commits to git |

### Agents (`.claude/agents/`)

| Agent | Description |
|---|---|
| `spec-reviewer` | Reviews the project spec for completeness, clarity, and gaps before building starts |

### Skills (`.claude/skills/`)

| Skill | Description |
|---|---|
| `doc-sync-check` | Checks all project docs are consistent with each other and free of placeholder text |

## Working conventions

- **One task at a time.** Give Claude a single, specific instruction rather than a list. Results are better and easier to review.
- **Be specific.** "Add a hero image with the studio name centred on top" is better than "make the homepage look nice."
- **Ask for explanations.** If Claude does something you don't understand, ask: "Explain what you just did in plain English."
- **Keep docs current.** The more accurate the spec and architecture are, the less context needs to be repeated across sessions.
- **After major changes:** update `docs/changelog.md` and `docs/project_status.md`.
- **After deciding something new:** move it from `docs/brainstorm.md` into `docs/project_spec.md`.
