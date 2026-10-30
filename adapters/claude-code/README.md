# Adapter: Claude Code (stub)

P1 stub only. Full mapping lands in a later phase.

## Intended map (preview)

| Oakstack | Claude Code |
| --- | --- |
| Hub | Main session; `CLAUDE.md` pointers into Oakstack |
| Spawn | Subagents / separate sessions per `when-to-spawn` |
| Board | File in repo or project store |
| Plugin | Harness marketplace install of Oakstack (primary consume path) |

## Must not

- Duplicate git-ops policy outside kit docs.
- Fork Matt/pstack — `/setup-oakstack` detects and points only.

Git guardrails: prefer upstream `git-guardrails-claude-code` (pointer only; not vendored here).

See [`../README.md`](../README.md) and [`../generic/file-and-spawn.md`](../generic/file-and-spawn.md).
