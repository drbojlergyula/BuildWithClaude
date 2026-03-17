# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a business-focused project template for building with Claude Code. It includes documentation templates, a brainstorm file, and pre-built Claude tools (agent, command, skills) — all using a Dream Home Design interior design website as the example to replace.

## Documentation

- [Project Spec](docs/project_spec.md) — Product requirements, features, tech stack, API design
- [Architecture](docs/architecture.md) — System design, data flow, component breakdown
- [Brainstorm](docs/brainstorm.md) — Scratchpad for ideas before they go into the spec
- [Project Status](docs/project_status.md) — Current progress and milestones
- [Changelog](docs/changelog.md) — Version history

Update files in the `docs/` folder after major milestones and additions to the project.

## Claude Tools

The agent, command, and skills below are **examples built around the Dream Home Design interior design website**. They will not directly apply to every project — a tool that adds a portfolio entry makes no sense for an Excel-to-website converter or a data processing tool.

Use them as a guide for the format and level of detail, then replace, rename, or delete them to match your own project. To create a new tool, add a plain-English text file in the relevant folder (`.claude/agents/`, `.claude/commands/`, or `.claude/skills/`) describing what you want Claude to do, step by step.

### Agent
- [seo-reviewer](.claude/agents/seo-reviewer.md) — Audits every page for SEO issues (titles, meta descriptions, image alt text, heading structure)

### Command
- `/add-project` — Guided workflow for adding a new project to the portfolio ([source](.claude/commands/add-project.md))

### Skills
- [content-check](.claude/skills/content-check/SKILL.md) — Scans all pages for placeholder text, broken links, and missing alt text
- [pre-launch-checklist](.claude/skills/pre-launch-checklist/SKILL.md) — Full feature verification before the site goes live
