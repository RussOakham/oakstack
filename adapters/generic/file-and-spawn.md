# Adapter: Generic (files + spawn)

**Minimum viable Oakstack.** Any human or agent that can (1) read files and (2) open a second chat/process can run hub + workers — no Cursor Project APIs, no Claude Task tool, no MCP required.

## Map

| Role | How |
| --- | --- |
| Hub | One chat (or person) that edits the task board file and writes kickoff files |
| Spawn | Paste or `@`-attach the kickoff file into a **second** chat; that chat is the worker |
| Board | `notes.md` or any file matching [`../../contracts/task-board.md`](../../contracts/task-board.md) |
| Reports | Worker replies in the second chat using [`../../contracts/messages.md`](../../contracts/messages.md); hub copies artifact links onto the board |

## Dry-run steps

1. Open this repo (or a consumer that vendors/points at it).
2. Hub reads [`../../contracts/orchestrator.md`](../../contracts/orchestrator.md) and [`../../contracts/when-to-spawn.md`](../../contracts/when-to-spawn.md).
3. Hub writes a kickoff file (example below) with all required fields.
4. Hub opens a **second** chat; pastes the kickoff (or points at the file).
5. Worker executes only in-scope paths; returns Completion (or Blocker) with troubleshooting footer.
6. Hub updates the board; if the workstream closes, follow [`../../workflows/store-hygiene.md`](../../workflows/store-hygiene.md).

Worked example: [`../../docs/generic-adapter-dry-run.md`](../../docs/generic-adapter-dry-run.md).

## Example kickoff file

```markdown
# Kickoff: example-worker

- **Spawn class:** research
- **Goal:** List the seven contract files and confirm each has a one-line purpose.
- **Done when:** A short markdown receipt exists at `internal/example-contract-list.md` with seven bullets.
- **In scope:** `internal/example-contract-list.md` (create), read-only `contracts/`
- **Out of scope:** Editing contracts, README, or preferences; no network publishes
- **Report path:** `internal/example-contract-list.md`
- **Troubleshooting:** follow workflows/troubleshooting-summaries.md; end with ### Troubleshooting resolutions
- **Process traps:** (none yet — consumer ledger empty)
- **Principles to cite:** orchestrator-stays-hub, thin-adapters-only
```
