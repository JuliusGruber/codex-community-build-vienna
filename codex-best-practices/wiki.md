# Codex Best Practices

Treat Codex like a teammate you configure and improve over time.

- Start each task with the right context.
- To provide context faster, use speech dictation in the Codex app to dictate your request instead of typing it.
- Use `AGENTS.md` for durable project guidance.
- Configure Codex to fit your workflow.
- Connect external systems using MCP.
- Turn repeatable work into reusable skills.
- Automate workflows once they are stable.

## Prompt essentials

A good default is to include four things in your prompt:

- **Goal:** What are you trying to change or build?
- **Context:** Which files, folders, docs, examples, or errors matter for this task? You can `@`-mention specific files as context.
- **Constraints:** What standards, architecture, safety requirements, or conventions should Codex follow?
- **Done when:** What should be true before the task is complete, such as tests passing, behavior changing, or a bug no longer reproducing?
