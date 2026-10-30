# Principle: Thin adapters only

**When it applies:** `adapters/<platform>/` and harness plugins.

**Rule:** Platform folders map roles ↔ primitives (hub, spawn, board). They do **not** duplicate SDLC prose that belongs in `contracts/`, `workflows/`, or `docs/`.

**Stop when:** An adapter grows a second copy of hygiene, kickoff, or git-ops policy — link the kit file instead.

**Cite in kickoffs as:** `thin-adapters-only`
