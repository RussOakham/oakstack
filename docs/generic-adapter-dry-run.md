# Generic adapter dry-run (P1 proof)

**Claim:** A hub + one worker can run from Oakstack **files alone** plus a **second chat** — no Cursor Project spawn APIs required.

**Adapter:** [`../adapters/generic/file-and-spawn.md`](../adapters/generic/file-and-spawn.md)

## Setup

| Actor | Surface |
| --- | --- |
| Hub | Chat A (or a human) with this repo open |
| Worker | Chat B — receives only the kickoff file contents |
| Artifacts | Written under `internal/` for the exercise (consumer stores use the same shape) |

## Kickoff used

```markdown
# Kickoff: p1-generic-dry-run

- **Spawn class:** research
- **Goal:** Prove the worker can follow Oakstack contracts without vendor spawn APIs.
- **Done when:**
  1. Receipt `internal/p1-generic-dry-run-receipt.md` exists.
  2. Receipt lists the seven `contracts/*.md` basenames with one-line purposes.
  3. Reply includes Completion fields + Troubleshooting resolutions.
- **In scope:** create `internal/p1-generic-dry-run-receipt.md`; read-only `contracts/`, `workflows/troubleshooting-summaries.md`, `principles/`
- **Out of scope:** Editing contracts/workflows/README; publishing; Homestead/consumer overlays; network installs
- **Report path:** `internal/p1-generic-dry-run-receipt.md`
- **Troubleshooting:** follow workflows/troubleshooting-summaries.md; end with ### Troubleshooting resolutions
- **Process traps:** (example) do not treat chat as tracker SoT — cite tracker-sot-not-chat
- **Principles to cite:** orchestrator-stays-hub, thin-adapters-only, tracker-sot-not-chat
```

## Hub steps (Chat A)

1. Read `contracts/orchestrator.md` and `contracts/when-to-spawn.md` — confirm this is a `research` spawn, not hub work.
2. Write the kickoff above to a file (e.g. `internal/kickoff-p1-generic-dry-run.md`) or paste it wholesale into Chat B.
3. Do **not** implement the receipt in Chat A.
4. After Chat B reports Completion, mark the workstream done on the board and optionally run close hygiene.

## Worker steps (Chat B)

1. Read only in-scope paths.
2. Write the receipt at `internal/p1-generic-dry-run-receipt.md`.
3. Reply with Completion shape from `contracts/messages.md`.

### Expected receipt shape

```markdown
# P1 generic dry-run receipt

| Contract | Purpose |
| --- | --- |
| orchestrator.md | Hub ownership and never-do |
| worker.md | Bounded worker + report-back |
| kickoff.md | Required spawn fields |
| messages.md | Completion / blocker / hygiene / plan-approved |
| task-board.md | Live board conventions |
| when-to-spawn.md | Stay vs spawn table |
| store-layout.md | Hot vs cold store paths |

Done criteria met: yes.
```

### Expected worker footer

```markdown
### Troubleshooting resolutions
- none
```

(or real snag→fix bullets if something failed and was fixed)

## Pass criteria

- [x] Kickoff included all seven required fields (`contracts/kickoff.md`).
- [x] Worker ran in a **second** chat (or second process), not the hub thread.
- [x] No Cursor Project / Claude Task API required to explain the path.
- [x] No Homestead secrets/hosts in kickoff or receipt.
- [x] Troubleshooting section present.

This document **is** the proof artifact for P1 review. Running the exercise live during PR review is optional; the steps are reproducible from `main` once merged.
