# Adapters

Adapters map Oakstack **roles** to platform **primitives**. They must stay thin ([`../principles/thin-adapters-only.md`](../principles/thin-adapters-only.md)).

## Adapter contract

| Oakstack role | Adapter must map to | Must not |
| --- | --- | --- |
| Orchestrator (hub) | Long-lived parent session / Project agent + task board file | Own a second copy of SDLC prose |
| Worker spawn | Child agent, subagent, second chat, or second process with the **same kickoff file** | Require MCP (MCP is an accelerator) |
| Kickoff | File and/or message containing [`../contracts/kickoff.md`](../contracts/kickoff.md) fields | Invent a vendor-only field set that drops required fields |
| Reports | Completion / Blocker / Hygiene-done / Plan-approved shapes | Drop `### Troubleshooting resolutions` |

## Included adapters (P1)

| Path | Status |
| --- | --- |
| [`generic/file-and-spawn.md`](generic/file-and-spawn.md) | Full minimum path — files + second chat |
| [`cursor/`](cursor/) | Stub README only (P5 expands) |
| [`claude-code/`](claude-code/) | Stub README only (P5 expands) |

## Git-ops behavior (all adapters)

No destructive git; prefer structured non-destructive git/issue tools when available; push without force. Platform-specific tool names belong in the adapter, not in core contracts.
