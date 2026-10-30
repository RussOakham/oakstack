# Contract: Message shapes

Workers and interactive children report with these minimum shapes. Extra prose is fine; missing fields are not.

## Completion

**When:** Worker finished the assignment (success or partial with clear remaining work owned by hub/human).

| Field | Required |
| --- | --- |
| Outcome | One short verdict |
| Links to artifacts | Paths or URLs written |
| `### Troubleshooting resolutions` | Bullet list; `- none` allowed |

## Blocker

**When:** Needs hub or human before continuing.

| Field | Required |
| --- | --- |
| What blocked | Concrete stop |
| Evidence | Path, log snippet, or tracker link |
| Proposed next owner | Hub / human / named worker |

Still include `### Troubleshooting resolutions` if any snags were resolved on the way.

## Hygiene-done

**When:** Hygiene worker finished close or weekly pass ([`../workflows/store-hygiene.md`](../workflows/store-hygiene.md)).

| Field | Required |
| --- | --- |
| Cold paths archived/deleted | List |
| `archived.md` line | Index updated |
| Friction promote result | Promoted / none / deferred with reason |

## Plan-approved

**When:** Interactive-product child reached explicit human approval of a plan/spec.

| Field | Required |
| --- | --- |
| Plan/spec links | Tracker or doc paths (tracker preferred SoT) |
| Explicit human approval noted | Who/when; not hub-inferred |

## Troubleshooting footer (all substantial replies)

```markdown
### Troubleshooting resolutions
- <snag> → <fix>   # or: - none
```

See [`../workflows/troubleshooting-summaries.md`](../workflows/troubleshooting-summaries.md).
