# Workflow: Interactive product loop

**When:** Product discovery, grill, wayfinder, or questionnaire work that needs a human in the loop.

**Result:** Plan/spec links with **explicit human approval** in the child; hub does not relay Q&A.

Skill names (Matt grill / wayfinder / to-spec / triage, etc.) are fine to cite. Oakstack is **not** their upstream — install via those ecosystems; `/setup-oakstack` only detects and points ([`../skills/setup-oakstack/SKILL.md`](../skills/setup-oakstack/SKILL.md)).

## Placement

| Role | Where |
| --- | --- |
| Hub | Spawns `interactive-product` with a full kickoff; does **not** interview |
| Interactive child | Runs grill/wayfinder; human answers **here** |
| Human | Drives the child; approves plan/spec |
| Implement worker | Only after plan-approved + tracker tickets exist |

## Intake-first

1. Confirm goal, constraints, and tracker SoT before deep grilling.
2. Prefer issue-tracker tickets/specs as SoT; store holds drafts/receipts ([`../principles/tracker-sot-not-chat.md`](../principles/tracker-sot-not-chat.md)).
3. Stop at **Plan-approved** message shape ([`../contracts/messages.md`](../contracts/messages.md)) — do not silently implement.

## Anti-patterns

- Hub one-shot “grill dump” in the parent thread.
- Using the hub as a message bus (“tell the child that Russell said…”).
- Finishing the grill unsupervised when approval is required.
- Linking consumer-private raw URLs as if they were kit SoT — point at Oakstack docs or the consumer’s own overlay.

## Cite

- [`../principles/interactive-grill-in-child.md`](../principles/interactive-grill-in-child.md)
- [`../contracts/when-to-spawn.md`](../contracts/when-to-spawn.md)
