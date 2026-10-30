# Contract: When to spawn

Decision table for the hub. Prefer staying on the hub for status; spawn for bounded judgment-heavy or interactive work.

| Situation | Stay on hub | Spawn worker |
| --- | --- | --- |
| Status, prioritization, “what next” | ✓ | |
| Interactive grill / wayfinder / discovery interview | | ✓ `interactive-product` (human answers **there**) |
| Implement one ticket / PR | | ✓ `implement` |
| Store close-hygiene or weekly backstop | | ✓ `hygiene` (unless tiny no-judgment pass) |
| writing-for-agents pass on hot context (non-trivial) | | ✓ |
| Trivial pointer fix (few files, no judgment) | ✓ same-store pass OK | |
| Research spike with clear report path | | ✓ `research` |
| Consumer ops runbook (no kit secrets) | | ✓ `ops` |

## Anti-patterns

- Hub silently one-shot “grilling” the human in the parent thread.
- Spawning implement workers without kickoff done criteria.
- Using the human as a relay for child Q&A.
- Spawning hygiene for every typo fix (stay on hub).

## Cite

- [`orchestrator.md`](orchestrator.md), [`kickoff.md`](kickoff.md)
- Principles: [`../principles/orchestrator-stays-hub.md`](../principles/orchestrator-stays-hub.md), [`../principles/interactive-grill-in-child.md`](../principles/interactive-grill-in-child.md)
