# Contract: Kickoff shape

Every **substantial** spawn includes the fields below. Adapters may paste this as a file, a chat message, or both — content matters, not the transport.

## Required fields

1. **Goal + done criteria** — checkable; what “done” looks like.
2. **In-scope paths** — repo and/or project store paths the worker may write.
3. **Out-of-scope** — one-liners the worker must not touch.
4. **Troubleshooting pointer** — link to [`../workflows/troubleshooting-summaries.md`](../workflows/troubleshooting-summaries.md) (required section in the final reply).
5. **Generated process traps** — from the **consumer** mistake ledger / kit example rows — never hand-authored only in the store.
6. **Report path** — where to write receipts (`internal/` vs user-facing `docs/`).
7. **Spawn class** — one of:
   - `interactive-product` — grill / wayfinder / discovery; human answers in this child
   - `implement` — one ticket / PR
   - `hygiene` — store close or weekly backstop
   - `research` — bounded investigation, no product plan approval
   - `ops` — operational runbook (consumer-defined); no kit secrets

## Suggested skeleton

```markdown
# Kickoff: <short title>

- **Spawn class:** implement | interactive-product | hygiene | research | ops
- **Goal:** …
- **Done when:** …
- **In scope:** `path/…`, `store/…`
- **Out of scope:** …
- **Report path:** `internal/<name>.md` (or docs/…)
- **Troubleshooting:** follow workflows/troubleshooting-summaries.md; end with ### Troubleshooting resolutions
- **Process traps:** <generated from consumer ledger>
- **Principles to cite:** e.g. orchestrator-stays-hub, tracker-sot-not-chat
```

## Hub checklist before spawn

- [ ] Done criteria are checkable without guessing.
- [ ] Out-of-scope includes “do not edit hub preferences” unless hygiene needs a documented exception.
- [ ] Interactive product work uses spawn class `interactive-product` and a **child** the human can drive.
- [ ] Report path matches [`store-layout.md`](store-layout.md) (cold receipts → `internal/` or archive).
