---
title: "Details | Codex Community Build - Vienna"
source: "https://codex-events.com/account/events/codex-build-vienna-2026-06-20?tab=details"
author:
published:
created: 2026-06-19
description: "See the schedule, location, and judging details for Codex Community Build - Vienna."
tags:
  - "clippings"
---
### Beginner Developer

Selected

## Audience

Developers who can code but are new to Codex or agentic coding.

## Short Description

Choose this track if you can code but are new to Codex or agentic coding. You will learn the basic developer loop: understand a repo, write or improve `AGENTS.md`, plan a small change, let Codex implement it, run checks, review the diff, and prepare a clean PR.

## Build goal

Ship a small, reviewable PR in a starter repo.

## Example projects

- Fix a bug with a failing test.
- Add a small UI component.
- Add a CLI flag.
- Improve error handling.
- Add a simple API route.
- Write tests for uncovered behavior.

## Codex concepts

- CLI, IDE extension, and desktop app basics.
- Chat vs Project: use chat for questions and planning; select a project folder when Codex needs repo or file context.
- `AGENTS.md` as durable repo guidance.
- `/plan` for task shaping.
- Existing skills and plugins from the marketplace.
- File mentions and IDE context.
- Test, lint, type-check, and format commands.
- `/review` and diff inspection.
- Practical permission modes: Chat/Read-only for planning, Auto/Agent for normal repo work, Full Access only for trusted tasks.
- `/permissions` as the way to tighten or loosen what Codex can do during a session.
- Commit and PR hygiene.

Resources

Codex app: Desktop app setup and local project workflow.

Codex CLI: Terminal-first Codex workflow and local repo usage.

Codex IDE extension: Using Codex inside VS Code-compatible editors and JetBrains.

Codex Sites: How Codex creates and publishes hosted websites, web apps, and games.

In-app browser: Previewing pages, leaving visual comments, and using browser-assisted iteration.

Codex best practices: Core habits for context, planning, verification, review, and reusable guidance.

Custom instructions with AGENTS.md: How Codex discovers and applies repo instructions.

AGENTS.md standard: General convention for writing agent-facing project instructions.

Agent approvals and security: Practical safety model for approvals, sandboxing, and network access.

Staff instructions

## Suggested flow

1. Ask Codex to summarize the repo and identify test commands.
2. Generate or refine `AGENTS.md`.
3. Define the change with done-when criteria.
4. Use `/plan` before implementation.
5. Implement with Codex.
6. Run verification commands.
7. Run `/review`.
8. Inspect the diff and prepare a commit or PR.
9. Try one existing skill or plugin that improves the workflow.

## Success criteria

- Participant has a passing, reviewable code change.
- Participant understands the difference between prompting and verification.
- Participant knows how to keep Codex scoped to a small change.

## Track instructions

- Keep tasks small enough to finish and review during the session.
- Help participants find the right setup, test, lint, and type-check commands before implementation starts.
- Nudge them to use `/plan` before edits and `/review` before accepting changes.
- Watch for permission confusion: default to Chat/Read-only for planning and Auto/Agent for normal repo work.
- If local setup fails, move them to a prepared starter repo or cloud task rather than losing the session to environment debugging.