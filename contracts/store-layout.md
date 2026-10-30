# Contract: Project store layout

Hot vs cold paths for a consumer project store (Cursor Project store or equivalent). Oakstack’s template lives under [`../templates/project-store/`](../templates/project-store/).

## Hot (keep)

| Path | Role |
| --- | --- |
| `preferences.md` | Durable coordinator prefs (no secrets) |
| `notes.md` (or task board) | Live board per [`task-board.md`](task-board.md) |
| `workflows/` | Living playbooks (or pointers into Oakstack workflows) |
| `principles/` | Decision rules cited in kickoffs |
| `docs/` (living) | Project context, handoffs still governing day-to-day |
| `internal/implement-friction-log.md` | Living friction mechanism (entries may promote out) |

## Cold (archive or delete)

| Kind | Action |
| --- | --- |
| Closed-only receipts under `docs/` or `internal/` | Move to `archived/` (or delete if disposable) and index in `archived.md` |
| Snapshot metrics / one-shot triage | Archive when superseded |
| Duplicate twins of kit/repo SoT | Delete after consumer points at Oakstack |

## Conventions

- **User-facing deliverables** → usually `docs/` (or media/).
- **Evidence, audits, working notes** → `internal/` (not user `docs/`).
- **`archived.md`** → pointer index for cold files; hygiene updates it.
- **No secrets in the store’s portable prefs** — vault paths, tokens, household IDs stay in consumer-private overlays ([`../principles/no-secret-in-kit.md`](../principles/no-secret-in-kit.md)).

## Hygiene triggers

Close of a workstream → [`../workflows/store-hygiene.md`](../workflows/store-hygiene.md). Weekly backstop → same workflow.
