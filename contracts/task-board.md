# Contract: Task board

Portable shape for the hub’s live board. A consumer’s `notes.md` (or equivalent) is one instance — filename is not sacred.

## Rules

1. **Live status only** — no essay history; archive cold narrative elsewhere.
2. **Capped length** — if the board grows past a readable screen, close or spawn hygiene; do not append forever.
3. **Each open workstream** includes:
   - **id** — stable short id (e.g. `OAK-4`)
   - **owner role** — `hub` or named worker / spawn class
   - **links** to kickoff paths (files preferred over chat paste alone)
   - **done criteria** — checkable
4. **Closed workstreams** trigger **store hygiene** spawn (see [`../workflows/store-hygiene.md`](../workflows/store-hygiene.md)) unless the close was a tiny no-judgment pass the hub already cleaned.

## Suggested sections

```markdown
## Tasks

### In Progress
- [ ] **ID** Title — owner: hub|worker — kickoff: path — done when: …

### Queued
- [ ] **ID** …

### Done
- [x] **ID** … — link to receipt if any
```

## Hub ownership

Only the hub (or a hygiene worker under hub kickoff) rewrites board ownership and closes workstreams. Workers may propose “mark done” in their completion message; the hub applies it.
