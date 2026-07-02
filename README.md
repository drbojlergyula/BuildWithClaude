<!-- repo-description: Deprecated — this template grew up and moved to BuildWithAI, which includes everything here plus multi-assistant support and plugin installation. -->

# BuildWithClaude → moved to BuildWithAI

> **⚠️ This template has merged into [BuildWithAI](https://github.com/drbojlergyula/BuildWithAI).**
>
> Everything here — the AI team (project-advisor, spec-reviewer, build-verifier, research-analyst), the guided workflows (`/start` through `/go-live`), the docs-as-memory structure — lives on there, actively maintained, with two upgrades:
>
> 1. **It still works exactly the same in Claude Code** (nothing was removed — Claude is the best-supported tool there), and *also* works with Codex, GitHub Copilot, Cursor and anything else that reads the open AGENTS.md / Agent Skills standards.
> 2. **You can install the AI team into an existing project as a plugin** — no template cloning needed:
>    ```
>    /plugin marketplace add drbojlergyula/BuildWithAI
>    /plugin install buildwithai-team@buildwithai
>    ```

## What should I do?

- **Starting a new project?** Use [BuildWithAI](https://github.com/drbojlergyula/BuildWithAI) as your template. If you only use Claude Code, follow its [gentle start-here guide](https://github.com/drbojlergyula/BuildWithAI/blob/main/docs/start_here_with_claude.md) — same 15-minute experience this repo offered.
- **Already built a project from this template?** Nothing breaks — your copy is yours and keeps working. To get the newest AI team in your existing project, install the plugin with the two commands above.

## Why the merge?

Maintaining two near-identical templates meant every improvement had to be made twice — the exact documentation-drift problem this product exists to solve. One repo, one source of truth, faster improvements.

The full toolkit this repo pioneered (last updated July 2026, in the Agent Skills / subagents formats) remains in this repository's files for reference, frozen as of the merge.

---
*Built to solve the bus-factor problem. One prompt: `/put-me-in-context` — now at [BuildWithAI](https://github.com/drbojlergyula/BuildWithAI).*
