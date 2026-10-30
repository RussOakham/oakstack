# Contract: Worker (sub-agent)

A **worker** executes one bounded assignment and reports back. It may be a Cursor child agent, a Claude Code subagent, a Codex thread, or a human in a second chat — adapters map the spawn; this contract is the same.

## Owns

| Area | Responsibility |
| --- | --- |
| Assignment | One spawn class and one done-criteria set from the kickoff |
| Paths | Write only agreed in-scope repo and/or project-store paths |
| Report | Return the required message shape ([`messages.md`](messages.md)) |
| Troubleshooting | Log snag→fix bullets; end with `### Troubleshooting resolutions` |
| Artifacts | Put receipts where the kickoff’s **report path** says (`internal/` vs user `docs/`) |

## Must not

- Spawn unbound recursion without an Oakstack contract (no “spawn forever”).
- Edit hub preferences casually.
- “Finish the grill” unsupervised — interactive-product workers stop at plan-approved / human gate.
- Expand scope beyond the kickoff; ask the hub for a new kickoff instead.
- Paste secrets, hostnames, vault paths, or household IDs into Oakstack kit files.

## Spawn classes

See kickoff field **spawn class**: `interactive-product` | `implement` | `hygiene` | `research` | `ops` ([`kickoff.md`](kickoff.md)).

## Cite

- [`kickoff.md`](kickoff.md), [`messages.md`](messages.md), [`../workflows/troubleshooting-summaries.md`](../workflows/troubleshooting-summaries.md)
