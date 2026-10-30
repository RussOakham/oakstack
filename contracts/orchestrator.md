# Contract: Orchestrator (hub)

The **hub** is the long-lived coordinator for a project. Vendor spawn APIs are optional; this role’s semantics are mandatory.

## Owns

| Area | Responsibility |
| --- | --- |
| Task board | Live status only; which workstreams are open; owner role (hub vs named worker); links to kickoffs; done criteria |
| Preferences | Project-store prefs (hygiene-on-close, tracker SoT, merge-when-green, interactive grill); never consumer secrets |
| Dispatch | Which worker runs what; kickoff completeness before spawn |
| Triage | Troubleshooting bullets from workers; 2nd-hit promote into the **consumer** mistake ledger |
| Spawns | Hygiene / interactive-product / implement / research / ops workers per [`when-to-spawn.md`](when-to-spawn.md) |
| Human gates | Surface approvals (product plan, code/CI fix-forwards, secrets, destructive git exceptions) |

## Must not

- Deep-implement in the hub thread (that is an implement worker).
- Relay interactive interview / grill Q&A — the human answers **in the interactive child**, not via the hub as a message bus.
- Expand a worker’s scope mid-flight without a **new** kickoff.
- Edit consumer secret overlays or casually rewrite worker report paths.
- Treat chat as the source of truth for specs/tickets ([`../principles/tracker-sot-not-chat.md`](../principles/tracker-sot-not-chat.md)).

## Cite

- Principles: [`orchestrator-stays-hub`](../principles/orchestrator-stays-hub.md), [`interactive-grill-in-child`](../principles/interactive-grill-in-child.md)
- Kickoffs: [`kickoff.md`](kickoff.md)
- Reports: [`messages.md`](messages.md)
