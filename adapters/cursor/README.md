# Adapter: Cursor (stub)

P1 stub only. Full mapping lands in a later phase.

## Intended map (preview)

| Oakstack | Cursor |
| --- | --- |
| Hub | Parent Project agent + project store (`notes.md`) |
| Spawn | Child agents / `CreateAgent`; typed Task subagents for non-interactive work |
| Board | Project store task board |
| Plugin | Harness marketplace install of Oakstack (primary consume path) |

## Must not

- Put SDLC prose only under `.cursor/` — link `contracts/` and `workflows/`.
- Duplicate git-ops policy; cite kit docs when they exist (P3+).

See [`../README.md`](../README.md) and [`../generic/file-and-spawn.md`](../generic/file-and-spawn.md) for the semantics this adapter will implement.
