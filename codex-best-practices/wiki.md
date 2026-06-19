# Codex Best Practices

Treat Codex like a teammate you configure and improve over time.

- Start each task with the right context.
- Use `AGENTS.md` for durable project guidance.
- Configure Codex to fit your workflow.
- Connect external systems using MCP.
- Turn repeatable work into reusable skills.
- Automate workflows once they are stable.

## Speech dictation

To provide context faster, try using speech dictation inside the Codex app to dictate what you want Codex to do rather than typing it.

## Model and reasoning effort (CLI)

In Codex CLI, type `/model` to change the model and its reasoning effort.

1. Select a model and press `Enter`.
2. Choose the reasoning effort for that model.

Use higher reasoning effort for complex work when you can accept slower responses and higher token usage.

## Configure the status line (CLI)

Use `/statusline` to configure which details Codex CLI shows in the status line. This CLI shows these items, in order:

- Context used
- Model with reasoning effort
- Current directory
- Git branch
- Weekly limit
- Five-hour limit
- Used tokens

Use colors in the status line.

## Configure Codex

Codex stores personal configuration in `~/.codex/config.toml`.

You can configure:

- Model choice and reasoning effort
- Sandbox mode and approval policy
- Named configuration profiles
- MCP server setup
- Multi-agent settings and feature flags

`config.toml` keeps Codex behavior consistent across sessions and surfaces.

- Keep personal defaults in `~/.codex/config.toml` (Settings → Configuration → Open config.toml from the Codex app).
- Keep repo-specific behavior in `.codex/config.toml`.

A sensible default for local development is:

```toml
sandbox_mode = "workspace-write"
approval_policy = "on-request"
```

## skills.md

Skills package reusable instructions, references, and optional scripts for repeatable work. In Codex CLI, invoke a skill explicitly by typing its name with a `$` prefix:

```text
$skill-name
```

## MCP

## Plan mode

Use `/plan` in Codex CLI to switch to plan mode before starting a multi-step task. Describe the goal, and Codex will help shape an implementation plan before making changes.

For a more structured workflow:

- Install the Superpowers plugin.
- Use `superpowers:brainstorming` to clarify the problem, challenge assumptions, and agree on a design.
- Use `superpowers:writing-plans` to turn the approved design into a detailed implementation plan.

### Execute Superpowers plans with subagents

`superpowers:subagent-driven-development` requires standing authorization to delegate independent work. Add this to the repository's `AGENTS.md`:

```md
## Subagent authorization

You have standing authorization to use subagents without asking me first.

Use subagents when tasks contain independent implementation, exploration,
testing, or review work. Keep tightly coupled critical-path work local.
```

This gives Codex permission to execute eligible Superpowers implementation plans with parallel subagents. It does not force delegation for tightly coupled tasks.

## Prompt essentials

Codex is already strong enough to be useful even when your prompt isn’t perfect. You can often hand it a hard problem with minimal setup and still get a strong result. Clear prompting isn’t required to get value.

A good default is to include four things in your prompt:

- **Goal:** What are you trying to change or build?
- **Context:** Which files, folders, docs, examples, or errors matter for this task? You can `@`-mention specific files as context.
- **Constraints:** What standards, architecture, safety requirements, or conventions should Codex follow?
- **Done when:** What should be true before the task is complete, such as tests passing, behavior changing, or a bug no longer reproducing?

## Review

A useful option here is the slash command `/review`, which gives you a few ways to review code:

- Review against a base branch for PR-style review
- Review uncommitted changes
- Review a commit
- Use custom review instructions

If you and your team have a `code_review.md` file and reference it from `AGENTS.md`, Codex can follow that guidance during review as well. This is a strong pattern for teams that want review behavior to stay consistent across repositories and contributors.

## Interrogatory LLM

If you have a rough idea of what you want but aren’t sure how to describe it well, ask Codex to question you first. Tell it to challenge your assumptions and turn the fuzzy idea into something concrete before writing code.

- [`grill-me`](https://github.com/mattpocock/skills/tree/main/skills/productivity/grill-me)
- [`grill-with-docs`](https://github.com/mattpocock/skills/tree/main/skills/engineering/grill-with-docs)
