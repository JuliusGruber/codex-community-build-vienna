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

## Initialize project guidance (CLI)

Use `/init` to generate a starter `AGENTS.md` in the current project directory. `AGENTS.md` gives Codex durable project guidance, including:

- How to run, build, test, and lint the project
- Repository layout and engineering conventions
- Review expectations and constraints
- What done means and how to verify work

Treat the generated file as a scaffold. Edit it to reflect the real project workflow and review the resulting diff, especially when the repository already has an `AGENTS.md`.

## Prompt essentials

Codex is already strong enough to be useful even when your prompt isn’t perfect. You can often hand it a hard problem with minimal setup and still get a strong result. Clear prompting isn’t required to get value.

A good default is to include four things in your prompt:

- **Goal:** What are you trying to change or build?
- **Context:** Which files, folders, docs, examples, or errors matter for this task? You can `@`-mention specific files as context.
- **Constraints:** What standards, architecture, safety requirements, or conventions should Codex follow?
- **Done when:** What should be true before the task is complete, such as tests passing, behavior changing, or a bug no longer reproducing?

## Interrogatory LLM

If you have a rough idea of what you want but aren’t sure how to describe it well, ask Codex to question you first. Tell it to challenge your assumptions and turn the fuzzy idea into something concrete before writing code.

- [`grill-me`](https://github.com/mattpocock/skills/tree/main/skills/productivity/grill-me)
- [`grill-with-docs`](https://github.com/mattpocock/skills/tree/main/skills/engineering/grill-with-docs)
