# CLAUDE.md

This file is read by Claude Code at the start of every session.

## Overview

This is a business-focused project template for building with Claude Code. It ships with documentation templates and a pre-built AI team (agents, skills, hooks). All files are pre-filled with a generic working example. Run `/start` to replace the example content with the user's real project.

If the SessionStart hook reports the template as untouched, offer `/start` before anything else.

## Documentation

| File | Purpose |
|---|---|
| [docs/project_spec.md](docs/project_spec.md) | What is being built, who it is for, features, tech stack, API design |
| [docs/architecture.md](docs/architecture.md) | System design, data flow, component breakdown, file structure |
| [docs/brainstorm.md](docs/brainstorm.md) | Scratchpad for ideas before they are ready for the spec |
| [docs/project_status.md](docs/project_status.md) | Current progress, active phase, upcoming milestones |
| [docs/changelog.md](docs/changelog.md) | Version history and notable changes |

The spec and architecture are the primary source of truth. Documentation conventions live in `.claude/rules/documentation.md`.

## Your AI team

**Skills** (`.claude/skills/`) — guided workflows, invoked as slash commands or picked up automatically when relevant:

| Skill | When |
|---|---|
| `/start` | Once, at the very beginning — interview that populates all project docs |
| `/new-feature` | Adding anything new — user stories, version placement, spec update |
| `/update-docs-and-commit` | After finishing any piece of work — docs refreshed, work committed |
| `/put-me-in-context` | Anyone needs instant full project context |
| `/doc-sync-check` | Docs feel out of date — finds drift, contradictions, placeholders |
| `/fix-bug` | Something is broken — reproduce, fix, verify, record |
| `/go-live` | Before launch — readiness check with a Go / No-Go report |

**Agents** (`.claude/agents/`) — specialists that run in their own context:

| Agent | When |
|---|---|
| `project-advisor` | After setup, after each phase, or when stuck — blind-spot review with persistent memory |
| `spec-reviewer` | Before building — checks the spec for gaps, vagueness, scope creep |
| `build-verifier` | After building — independently runs and tests the feature against the spec |
| `research-analyst` | A decision needs outside facts — cited web research briefs |

To create a new tool, add a markdown file with YAML frontmatter to the relevant folder — plain English instructions work.

## Working conventions

- **One task at a time.** A single, specific instruction beats a list.
- **Be specific.** "Add a contact form with name, email, and message fields" beats "add a way for people to get in touch."
- **Explain in plain English** when asked — the user may be non-technical.
- **Verify before declaring done.** Prefer running the thing (or the build-verifier agent) over assuming.
