# AGENT.md Wiki

## Layered AGENTS.md files

Codex supports layered `AGENTS.md` guidance:

- A global file in `~/.codex/`
- A repository-root `AGENTS.md`
- Additional `AGENTS.md` or `AGENTS.override.md` files in nested directories

Codex loads these files from the root toward the current working directory. Files closer to the working directory are appended later and therefore override broader guidance. Each directory contributes at most one file, with `AGENTS.override.md` taking precedence over `AGENTS.md`. The combined instructions default to a 32 KiB limit.

Source: [Official AGENTS.md guide](https://developers.openai.com/codex/guides/agents-md)

Keep it practical. A short, accurate `AGENTS.md` is more useful than a long file full of vague rules. Start with the basics, then add new rules only after you notice repeated mistakes.

A good `AGENTS.md` covers:

- Repository layout and important directories
- How to run the project
- Build, test, and lint commands
- Engineering conventions and PR expectations
- Constraints and do-not rules
- What done means and how to verify work

When Codex makes the same mistake twice, ask it for a retrospective and update `AGENTS.md`.

## Initialize project guidance (CLI)

Use `/init` to generate a starter `AGENTS.md` in the current project directory. `AGENTS.md` gives Codex durable project guidance, including:

- How to run, build, test, and lint the project
- Repository layout and engineering conventions
- Review expectations and constraints
- What done means and how to verify work

Treat the generated file as a scaffold. Edit it to reflect the real project workflow and review the resulting diff, especially when the repository already has an `AGENTS.md`.

## Large monorepo? Use nested AGENTS.md files for subprojects

Place another AGENTS.md inside each package. Agents automatically read the nearest file in the directory tree, so the closest one takes precedence and every subproject can ship tailored instructions. For example, at time of writing the main OpenAI repo has 88 AGENTS.md files.

## Governance and status

AGENTS.md is an open format stewarded by the Agentic AI Foundation under the Linux Foundation. It is a Linux Foundation-backed community convention, not a formal standards-body specification such as an ISO or IETF standard.

Source: [AGENTS.md](https://agents.md/)
