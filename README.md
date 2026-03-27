# BuildWithClaude

A starter template for building software with Claude Code — Anthropic's AI coding assistant. Designed for business owners and non-technical users.

---

## Quick start

**1. Get the tools**

- [Git](https://git-scm.com) — saves and versions your project
- [VS Code](https://code.visualstudio.com) — free code editor
- Claude Code — install from the VS Code Extensions panel (search "Claude Code")
- A free account at [github.com](https://github.com)

**2. Copy this template**

On the GitHub page, click **"Use this template" → "Create a new repository"**, give it a name, and click Create.

**3. Download to your computer**

Open VS Code, open the Terminal (**View → Terminal**), and run:

```
git clone https://github.com/YOUR-USERNAME/YOUR-PROJECT-NAME.git
```

Then open the downloaded folder in VS Code (**File → Open Folder**).

**4. Run /start**

Open Claude Code in VS Code and type:

```
/start
```

Claude will interview you about what you want to build and fill in all the project documents automatically. The whole thing takes about 5–10 minutes.

**5. Start building**

Once `/start` is done, give Claude plain-English instructions:

> "Build the homepage described in the project spec."
> "Run the pre-launch checklist."
> "Add a user notifications feature to the spec."

---

## What's in this template?

```
BuildWithClaude/
├── CLAUDE.md                        ← Instructions Claude reads every session
├── docs/
│   ├── project_spec.md              ← What you are building and why
│   ├── architecture.md              ← How the project is structured
│   ├── brainstorm.md                ← Scratchpad for ideas
│   ├── project_status.md            ← Progress and milestones
│   └── changelog.md                 ← History of changes
└── .claude/
    ├── agents/                      ← Specialist Claude personas
    ├── commands/                    ← Shortcut tasks (e.g. /start, /add-project)
    └── skills/                      ← Repeatable checklists
```

All files are pre-filled with a working example (a fictional interior design studio). `/start` replaces all of it with your actual project.

---

## Questions or issues?

Describe what you expected to happen and what happened instead — Claude can diagnose and fix most problems directly.
