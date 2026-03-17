# BuildWithClaude

A starter template for business owners and non-technical users who want to build software with the help of Claude Code — Anthropic's AI coding assistant.

Everything in this template is pre-structured with descriptions and examples so you know exactly what to fill in. The example used throughout is a company website for **Dream Home Design**, a fictional interior design studio. Replace every example with your own project.

---

## Quick start — the 5 things to replace

Once you have the template set up (see the step-by-step guide below), you only need to update 5 things to make it yours:

1. **`docs/project_spec.md`** — describe your project instead of Dream Home Design
2. **`docs/architecture.md`** — describe how your project is structured
3. **`docs/project_status.md`** — set your own phases and start date
4. **`.claude/agents/`**, **`.claude/commands/`**, **`.claude/skills/`** — replace the website-specific tools with ones relevant to your project (or just delete them and add your own as you go)
5. **`claude.md`** — update the overview line to describe your project

Everything else (brainstorm, changelog) fills itself in naturally as you work.

---

## What is Claude Code?

Claude Code is an AI assistant made by Anthropic that you talk to inside your code editor (VS Code). Instead of writing code yourself, you describe what you want in plain English and Claude writes, edits, and checks the code for you.

Think of it like having a developer sitting next to you who you can give instructions to at any time.

---

## What is this template?

When you start a new project with Claude Code, it helps a lot to give Claude some context about your project upfront — what you are building, who it is for, how it should work. Without that context, Claude has to guess, which leads to mistakes and back-and-forth.

This template gives you a ready-made folder structure with pre-written files that explain to Claude:

- What your project is and what it should do
- How the pieces of the project connect together
- What tools Claude should use to help you
- How to keep track of progress and changes

All files are pre-filled with a working example (the Dream Home Design website) so you can see exactly what good looks like — then replace it with your own project.

---

## What is in this template?

```
BuildWithClaude/
├── claude.md                        ← Instructions for Claude about your project
├── .gitignore                       ← Tells Git which files to ignore
├── docs/
│   ├── project_spec.md              ← What you are building and why
│   ├── architecture.md              ← How the project is technically structured
│   ├── brainstorm.md                ← Scratchpad for ideas before they go into the spec
│   ├── project_status.md            ← Current progress and what is next
│   └── changelog.md                 ← History of changes to the project
└── .claude/
    ├── settings.json                ← Claude Code settings for this project
    ├── agents/
    │   └── seo-reviewer.md          ← Example agent: checks pages for SEO issues
    ├── commands/
    │   └── add-project.md           ← Example command: adds a new portfolio project
    └── skills/
        ├── content-check/           ← Example skill: scans for placeholder text and broken links
        └── pre-launch-checklist/    ← Example skill: verifies the site works before going live
```

### What does each file do?

**`CLAUDE.md`**
This is the most important file. Every time you open Claude Code in this project, Claude reads this file first. It tells Claude what your project is, where the key documents are, and what tools are available. Keep it up to date as your project grows.

**`docs/project_spec.md`**
Your product brief. Describes what you are building, who it is for, what features it needs, and the technical decisions (like which tools or services to use). This is the first document you should fill in.

**`docs/architecture.md`**
Describes how the project is put together technically — the folder structure, how data moves through the system, and what each file does. Claude uses this to navigate your project without you having to explain it every time.

**`docs/brainstorm.md`**
A scratchpad for thinking through ideas before they are ready to go into the spec. Use it to explore options, list pros and cons, and record decisions.

**`docs/project_status.md`**
A living document that tracks where you are in the project — what phases are complete, what is in progress, and what is coming next.

**`docs/changelog.md`**
A log of notable changes to the project over time. Update it after major additions or milestones.

### What are agents, commands, and skills?

These are reusable tools you set up once and ask Claude to run whenever you need them.

**Agents** are specialists. An agent is a focused version of Claude that is given a specific job and knows exactly how to do it. For example, the `seo-reviewer` agent knows how to check every page of your website for SEO problems.

**Commands** are shortcuts. A command is a task you run often, written down as a series of steps. Instead of explaining the same task to Claude every time, you type `/add-project` and Claude follows the steps automatically.

**Skills** are repeatable checklists. A skill is a step-by-step process Claude follows to check or verify something. For example, the `pre-launch-checklist` skill works through everything that should be tested before a website goes live.

All three are just text files — you write them in plain English, and Claude follows them.

---

## How to get started — step by step

### Step 1 — Get the tools

You need three things installed on your computer:

1. **Git** — a tool for saving and managing versions of your project. Download it from [git-scm.com](https://git-scm.com).
2. **VS Code** — a free code editor. Download it from [code.visualstudio.com](https://code.visualstudio.com).
3. **Claude Code** — the AI assistant that lives inside VS Code. Install it by opening VS Code, going to the Extensions panel (the four-square icon on the left), searching for "Claude Code", and clicking Install.

You will also need a free account at [github.com](https://github.com). GitHub is a website where you store your project online so it is backed up and safe.

---

### Step 2 — Copy this template to your own GitHub account

"Cloning" means making your own copy of this project that you can edit freely.

1. Go to the GitHub page for this template repository
2. Click the green **"Use this template"** button near the top right
3. Click **"Create a new repository"**
4. Give your project a name (e.g. `my-company-website`)
5. Choose **Private** if you don't want others to see it, or **Public** if you don't mind
6. Click **"Create repository"**

You now have your own copy of the template in your GitHub account.

---

### Step 3 — Download your copy to your computer

Now you need to get that copy onto your computer so you can work on it.

1. Open VS Code
2. Open the Terminal inside VS Code: go to **View → Terminal** in the menu bar
3. In the terminal, type the following (replace `YOUR-USERNAME` and `YOUR-PROJECT-NAME` with your own):

```
git clone https://github.com/YOUR-USERNAME/YOUR-PROJECT-NAME.git
```

4. Press Enter. Git will download your project into a new folder on your computer.
5. In VS Code, go to **File → Open Folder** and open that new folder.

---

### Step 4 — Fill in the documents

Start with `docs/project_spec.md`. Open it and replace the Dream Home Design example with your own project. Answer the questions in the file:

- What is your product?
- Who is it for?
- What should it do?

Then fill in `docs/architecture.md` with how you want the project to be structured. If you are not sure yet, leave the example in place and ask Claude to help you adapt it.

---

### Step 5 — Start talking to Claude

Open Claude Code in VS Code (look for the Claude icon in the sidebar or press the keyboard shortcut shown after installation).

Claude will read `CLAUDE.md` automatically and understand the context of your project. You can now give it instructions in plain English, for example:

> "Build the homepage described in the project spec."

> "Run the pre-launch checklist skill."

> "/add-project"

---

### Step 6 — Keep your documents up to date

As Claude builds things and your project grows, keep the documents updated:

- Add completed work to `docs/changelog.md`
- Update `docs/project_status.md` with the current phase
- Move any decisions from `docs/brainstorm.md` into `docs/project_spec.md`

This ensures Claude always has accurate context about your project, no matter when you open a new session.

---

## Tips for working with Claude

- **Be specific.** Instead of "make the website look nice", say "add a hero image to the homepage with a full-width photo and the studio name centred on top."
- **One thing at a time.** Give Claude one task at a time rather than a long list. It works better this way.
- **Ask Claude to explain.** If Claude does something you don't understand, ask: "Can you explain what you just did in plain English?"
- **Use the documents.** The more you fill in `project_spec.md` and `architecture.md`, the less you need to repeat yourself to Claude across sessions.

---

## Questions or issues?

If something is not working as expected, ask Claude directly — describe what you expected to happen and what happened instead. Claude can diagnose most problems and fix them for you.
