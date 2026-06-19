# Top 10 most-used MCP servers — OpenAI Codex

**Scope:** OpenAI Codex (Codex CLI + OpenAI/ChatGPT MCP connectors) only.

> Ranking produced by a multi-agent research workflow (6 parallel Codex-focused
> searches → synthesis → adversarial verification). Ordering verified against
> OpenAI's official Codex MCP docs; repo links corrected by the verification
> pass. npm snapshot ~30 days ending 2026-06-18.

| #  | Server | Repo | What it does | Codex signal |
|----|--------|------|--------------|--------------|
| 1  | **Context7** | https://github.com/upstash/context7 | Up-to-date, version-pinned library docs into context | Canonical `config.toml` example in official Codex docs; #1 across ~9/11 Codex listicles; real user configs |
| 2  | **Playwright MCP** | https://github.com/microsoft/playwright-mcp | Browser automation via accessibility-tree snapshots | Named in official Codex docs; most common browser server in real `config.toml` dumps; ~21.7M npm/mo |
| 3  | **GitHub MCP** | https://github.com/github/github-mcp-server | PRs, issues, code search, CI logs (beyond git) | In official Codex docs; tied most-cited (~9/11 listicles). Maintained Go repo — *not* the archived npm pkg |
| 4  | **Chrome DevTools MCP** | https://github.com/ChromeDevTools/chrome-devtools-mcp | Drives live Chrome via CDP — perf traces, DOM, network | Named in official Codex docs; in real configs + Codex 5.1 bug reports; ~2.3M npm/wk |
| 5  | **Sentry MCP** | https://github.com/getsentry/sentry-mcp | Pulls Sentry errors/traces for prod debugging | Official Codex docs w/ `codex mcp login sentry`; Sentry ships a dedicated Codex setup anchor |
| 6  | **Figma MCP (Dev Mode)** | *hosted-only:* `https://mcp.figma.com/mcp` · guide: https://github.com/figma/mcp-server-guide | Figma design specs/tokens → code | Official Codex docs HTTP+bearer example; in Codex integration articles |
| 7  | **Supabase MCP** | https://github.com/supabase/mcp | Postgres/SQL, migrations, auth/storage, edge fns | Dedicated openai/codex Discussion #3372; DB example in Codex guides |
| 8  | **Filesystem MCP** | https://github.com/modelcontextprotocol/servers/tree/main/src/filesystem | Scoped local file read/write/search | Canonical STDIO example across major Codex setup guides; ~263K npm/wk |
| 9  | **Serena** | https://github.com/oraios/serena | LSP-backed semantic code nav + symbol editing | README lists Codex as supported; configured in openai/codex issues #13025 / #3100 |
| 10 | **OpenAI Docs MCP** | *hosted-only:* `https://developers.openai.com/mcp` · docs: https://developers.openai.com/learn/docs-mcp | Search/read OpenAI platform docs from the agent | OpenAI's *own* first-party server, featured in Codex docs |

## Confidence & caveats

- **Ranks 1–6 are high-confidence** — all explicitly named in OpenAI's official
  Codex MCP docs *and* corroborated by setup guides, listicles, and real
  `openai/codex` issue config dumps.
- **#10 OpenAI Docs MCP is ranked on official endorsement, not adoption** — by
  pure usage, **Notion** or **Sequential Thinking** would take that slot.
- **No real per-client telemetry exists** — nobody publishes "how many Codex
  users enabled server X." This is triangulation from official docs +
  tutorial/listicle frequency + community configs + npm download proxies. The
  npm proxy undercounts hosted/HTTP servers (Sentry, Figma, GitHub's Go binary)
  since they aren't npm-distributed.

## Repo-link corrections (from the verification pass)

- **Figma (#6)** — there is no public source repo; the Dev Mode server is
  hosted-only at `https://mcp.figma.com/mcp`.
- **OpenAI Docs MCP (#10)** — also hosted-only at `https://developers.openai.com/mcp`.
- **Supabase (#7)** — `supabase-community/supabase-mcp` is a stale redirect;
  canonical is now first-party `supabase/mcp`.
- `modelcontextprotocol/servers` (Filesystem) is **actively maintained**, not
  archived — the archived set is the separate `servers-archived` repo (home of
  the deprecated GitHub/Postgres npm packages).

## Honorable mentions

Notion, Sequential Thinking, Linear, Vercel, Snyk, and `tuannvm/codex-mcp-server`
(the reverse — exposes Codex *as* a server to other agents; deliberately excluded
from the main list).
