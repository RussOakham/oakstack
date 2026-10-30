# Workflow: Store hygiene

**When:** (1) a workstream closes, or (2) weekly backstop.

**Result:** Cold paths archived or deleted; `archived.md` updated; friction 2nd-hits promoted; hot context still readable.

De-Homesteaded portable playbook. No product hosts, money prefs, or subscription IDs.

## Close hygiene (must)

On workstream close:

1. **Identify cold files** created only for that workstream under `internal/` and closed-only `docs/` receipts.
2. **Archive or delete** — prefer archive into `archived/` with an `archived.md` index line; delete if disposable noise.
3. **Keep hot:** `preferences.md`, living `workflows/`, `principles/`, friction-log mechanism, open board (`notes.md` or equivalent).
4. **Friction promote** — scan recent troubleshooting bullets / friction-log entries for a **2nd hit**; promote into the **consumer** mistake ledger (or living playbook), never only as a store paste. Kit owns ledger schema/tools later; rows stay consumer-owned.
5. **Board** — hub marks the workstream done; drop stale kickoff links.
6. **Report** with **Hygiene-done** shape ([`../contracts/messages.md`](../contracts/messages.md)).

Tiny no-judgment pointer fixes may stay on the hub without a hygiene spawn ([`../contracts/when-to-spawn.md`](../contracts/when-to-spawn.md)).

## Weekly backstop

1. Prune inbox-like noise (orphan drafts, superseded snapshots).
2. Re-run friction 2nd-hit promote.
3. Optional: writing-for-agents pass on **hot** context only (non-trivial → spawn; trivial → hub).
4. Confirm `archived.md` matches what is on disk.
5. Report Hygiene-done.

## Do not

- Delete living preferences or open kickoffs.
- Promote Homestead/consumer secrets into Oakstack kit files.
- Treat hygiene receipts as permanent SoT — they are cold after the next pass.

## Cite

- [`../contracts/store-layout.md`](../contracts/store-layout.md)
- [`../principles/consumer-owns-ledger-rows.md`](../principles/consumer-owns-ledger-rows.md)
