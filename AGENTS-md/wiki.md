# Layered AGENTS.md files

Codex supports layered `AGENTS.md` guidance:

- A global file in `~/.codex/`
- A repository-root `AGENTS.md`
- Additional `AGENTS.md` or `AGENTS.override.md` files in nested directories

Codex loads these files from the root toward the current working directory. Files closer to the working directory are appended later and therefore override broader guidance. Each directory contributes at most one file, with `AGENTS.override.md` taking precedence over `AGENTS.md`. The combined instructions default to a 32 KiB limit.

Source: [Official AGENTS.md guide](https://developers.openai.com/codex/guides/agents-md)
