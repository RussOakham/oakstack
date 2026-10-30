# AGENTS

Always-read entry for Oakstack. Prefer these pointers over inventing process.

## Contracts (hub + workers)

- Hub role → [`contracts/orchestrator.md`](contracts/orchestrator.md)
- Worker role → [`contracts/worker.md`](contracts/worker.md)
- Kickoff fields → [`contracts/kickoff.md`](contracts/kickoff.md)
- Report shapes → [`contracts/messages.md`](contracts/messages.md)
- Task board → [`contracts/task-board.md`](contracts/task-board.md)
- Stay vs spawn → [`contracts/when-to-spawn.md`](contracts/when-to-spawn.md)
- Store hot/cold → [`contracts/store-layout.md`](contracts/store-layout.md)

## Workflows

- Close + weekly hygiene → [`workflows/store-hygiene.md`](workflows/store-hygiene.md)
- End-of-run snags → [`workflows/troubleshooting-summaries.md`](workflows/troubleshooting-summaries.md)
- Grill / wayfinder in child → [`workflows/interactive-product-loop.md`](workflows/interactive-product-loop.md)

## Principles (cite in kickoffs)

See [`principles/`](principles/) — especially `orchestrator-stays-hub`, `interactive-grill-in-child`, `tracker-sot-not-chat`, `no-secret-in-kit`, `consumer-owns-ledger-rows`, `thin-adapters-only`.

## Adapters

- Adapter contract → [`adapters/README.md`](adapters/README.md)
- Files + second chat → [`adapters/generic/file-and-spawn.md`](adapters/generic/file-and-spawn.md)

## Setup

- Per-project alignment → [`skills/setup-oakstack/SKILL.md`](skills/setup-oakstack/SKILL.md)
- Product overview → [`README.md`](README.md)

## Hard rules (short)

1. No Homestead secrets, hosts, vault paths, or household IDs in this kit.
2. Prefer structured git/issue tools; no force push; no destructive git without human exception.
3. Substantial worker replies end with `### Troubleshooting resolutions` (`- none` allowed).
4. Issue tracker is SoT for specs/tickets; stores hold drafts and receipts.
