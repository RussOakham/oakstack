# P1 generic dry-run receipt

Proof artifact accompanying [`../docs/generic-adapter-dry-run.md`](../docs/generic-adapter-dry-run.md). Produced as the worker-shaped output of the documented file-and-spawn exercise (hub writes kickoff; worker would write this receipt in a second chat).

| Contract | Purpose |
| --- | --- |
| `orchestrator.md` | Hub ownership and never-do |
| `worker.md` | Bounded worker + report-back |
| `kickoff.md` | Required spawn fields |
| `messages.md` | Completion / blocker / hygiene / plan-approved |
| `task-board.md` | Live board conventions |
| `when-to-spawn.md` | Stay vs spawn table |
| `store-layout.md` | Hot vs cold store paths |

Done criteria met: yes.

### Troubleshooting resolutions

- Source Homestead workflow bodies were not mounted in this agent environment → authored portable workflows from plan §3.2 / inventory General notes instead of a line-by-line strip
