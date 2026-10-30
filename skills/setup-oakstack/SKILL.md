---
name: setup-oakstack
description: >-
  Per-project alignment for Oakstack consumers. Detects Matt skills and pstack
  prerequisites, prompts when missing, points at install paths, and aligns
  Oakstack-owned prefs/stubs. Doctor is the non-interactive check. Shape only —
  marketplace publish later. Use when the user runs /setup-oakstack or asks to
  wire Oakstack into a repo.
---

# /setup-oakstack

**Shape only (P1).** Marketplace publish and full automation come later. Oakstack is **not** upstream for Matt skills or pstack.

## Intent

1. **Harness plugin** already installed the kit into the interface (or the human is using the generic file adapter).
2. This slash **aligns the consumer repo**: Matt + pstack prerequisites + Oakstack prefs/stubs.
3. **`doctor`** = non-interactive check (verify prerequisites / alignment). Setup is interactive; doctor is what setup (and later CI) calls.

## Detect

Check (read-only) for signals such as:

| Check | Healthy signal (examples) |
| --- | --- |
| Matt skills | `setup-matt-pocock-skills` / grill / wayfinder skills present or documented install path |
| pstack / poteto | pstack plugin or poteto-mode skill present; models override file optional |
| Oakstack prefs | Consumer `preferences.md` (or template copy) includes hygiene / grill-in-child / tracker SoT bullets |
| Oakstack pointers | `AGENTS.md` or equivalent links `contracts/` / workflows (via plugin path or documented root) |

Do **not** vendor Matt or pstack into the consumer. Do **not** invent headless pin design (deferred).

## Prompt

For each missing prerequisite:

1. Say what is missing in one line.
2. Point at the **upstream** install (Matt setup slash / pstack setup / Oakstack plugin docs).
3. Ask the human before writing files.

## Point + align (when human agrees)

- Copy or merge from [`../../templates/project-store/`](../../templates/project-store/) as needed (prefs skeleton, `archived.md`, friction-log stub, empty `principles/`).
- Ensure kickoffs can cite Oakstack principles and troubleshooting workflow.
- Record that doctor should re-run clean.

## Doctor (non-interactive)

Exit conceptually green when:

- [ ] Matt product-loop skills reachable **or** explicitly deferred by human note
- [ ] pstack/poteto HOW reachable **or** explicitly deferred
- [ ] Consumer prefs include portable Oakstack bullets (no secrets)
- [ ] Hub/worker contracts findable from the harness or documented path

Print a short pass/fail list; do not mutate on doctor alone.

## Inspiration (do not fork)

- `mattpocock/skills` → `/setup-matt-pocock-skills`
- `cursor/plugins` pstack → `/setup-pstack`
