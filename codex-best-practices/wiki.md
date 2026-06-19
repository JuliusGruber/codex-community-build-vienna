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

## Interrogatory LLM

If you have a rough idea of what you want but aren’t sure how to describe it well, ask Codex to question you first. Tell it to challenge your assumptions and turn the fuzzy idea into something concrete before writing code.

- [`grill-me`](https://github.com/mattpocock/skills/tree/main/skills/productivity/grill-me)
- [`grill-with-docs`](https://github.com/mattpocock/skills/tree/main/skills/engineering/grill-with-docs)

## Prompt essentials

A good default is to include four things in your prompt:

- **Goal:** What are you trying to change or build?
- **Context:** Which files, folders, docs, examples, or errors matter for this task? You can `@`-mention specific files as context.
- **Constraints:** What standards, architecture, safety requirements, or conventions should Codex follow?
- **Done when:** What should be true before the task is complete, such as tests passing, behavior changing, or a bug no longer reproducing?
