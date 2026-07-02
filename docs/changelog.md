# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

<!-- Add a new dated section each time you make significant changes.
     Use ### Added, ### Changed, ### Fixed, ### Removed as needed.
     Example entry below — delete it when you add your first real entry. -->

---

## 2026-07-02 — Deprecated: merged into BuildWithAI *(later the same day)*

### Changed
- **This template merged into [BuildWithAI](https://github.com/drbojlergyula/BuildWithAI)** — same AI team and workflows, still fully Claude Code-native, plus multi-assistant support and plugin installation. This repo is frozen; see the README for migration notes.

---

## 2026-07-02 *(template history — replaced by your own entries after /start)*

### Added
- **AI team** — Two new agents: `build-verifier` (independent QA that runs what was built) and `research-analyst` (cited web research briefs)
- **New skills** — `/put-me-in-context` (instant project briefing), `/fix-bug` (reproduce → fix → verify → record), `/go-live` (launch readiness with Go/No-Go report)
- **Welcome-on-open** — SessionStart hook detects an untouched template and offers `/start` automatically
- **Modular rules** — Documentation conventions moved to `.claude/rules/documentation.md`
- **Safe defaults** — `.claude/settings.json` pre-approves read-only git commands and denies reading `.env` files

### Changed
- **Commands became skills** — All workflows migrated from the legacy `.claude/commands/` format to the Agent Skills open standard (`.claude/skills/<name>/SKILL.md` with YAML frontmatter)
- **Agents are real subagents now** — `project-advisor` and `spec-reviewer` gained the YAML frontmatter Claude Code requires (tools, model, memory), so they run in their own context with scoped permissions; the advisor remembers past advice via persistent memory
- **README and CLAUDE.md** rewritten around the "AI team in a box" experience

---

## YYYY-MM-DD *(example entry — delete when you add your first real entry)*

### Added
- **Order form** — Public form collecting name, email, and order details
- **Owner dashboard** — Password-protected view listing all submitted orders
- **Mark as handled** — Button on each order to update its status

### Changed
- Layout updated to work correctly on mobile screens below 400px

### Fixed
- Form submission not showing confirmation message in Safari — resolved by replacing `fetch` response handling
