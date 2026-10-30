# Workflow: Troubleshooting summaries

**When:** End of every substantial worker (and hub) run that hit a snag — and as a required kickoff pointer so workers cannot “forget.”

**Result:** A `### Troubleshooting resolutions` section the hub can triage; 2nd hits promote into the consumer mistake ledger.

## Rule

Every substantial completion, blocker, or hygiene-done reply ends with:

```markdown
### Troubleshooting resolutions
- <snag in one line> → <fix in one line>
```

If nothing snagged: `- none`.

## Hub duties

1. **Paste this workflow** (or a one-line pointer) into every substantial kickoff ([`../contracts/kickoff.md`](../contracts/kickoff.md)).
2. **Triage** bullets: discard noise; keep process traps.
3. **2nd-hit promote** — when the same snag→fix appears twice (or matches a known trap), add/update a row in the **consumer** mistake ledger and regenerate kickoff traps when generators exist (P2). Do not dump traps only into the project store.

## Worker duties

1. Log snags as you fix them (tool auth, wrong SoT path, stale base branch, missing submodule, etc.).
2. Prefer actionable fixes over venting.
3. Never put secrets, tokens, or private hostnames in the bullet text — redact.

## Friction log (optional living file)

Consumers may keep `internal/implement-friction-log.md` as a working pad. Mechanism is portable; entries are consumer sediment. Promote out; do not let the log replace the ledger.

## Cite

- [`../contracts/messages.md`](../contracts/messages.md)
- [`../principles/consumer-owns-ledger-rows.md`](../principles/consumer-owns-ledger-rows.md)
