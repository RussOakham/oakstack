# Oakstack

Vendor-neutral portable **agent / SDLC kit**: contracts, workflows, project-store templates, starter principles, and thin harness adapters.

Working prose may say “the kit”; the product name is **Oakstack**.

## What it is

- **Files + conventions** — no required proprietary runtime.
- **Orchestrator-as-hub + sub-agent workers** as first-class contracts (roles, kickoff/report shapes, task board, hygiene, when-to-spawn).
- **Consumer overlay pattern** — Oakstack ships portable defaults; each consumer keeps secrets, hosts, and product traps locally.
- **Thin adapters** — map the same semantics to Cursor, Claude Code, Codex, or a human with a second chat.

## Non-goals

- Not a Homestead (or any household) app repo — no money/domain taxonomies, VPS/vault hosts, or fleet inventory.
- Not upstream for [Matt skills](https://github.com/mattpocock/skills) or [pstack](https://github.com/cursor/plugins) — Oakstack **detects, prompts, and points**; it does not vendor or replace them.
- Not a headless/CI pin story yet — submodule / `OAKSTACK_ROOT` bake is deferred.
- Not npm-published process docs (GitHub is the home; npm name collisions are irrelevant).

## How to consume

**Primary (locked):** install Oakstack as a **harness plugin** (Cursor / Claude / Codex marketplaces as thin adapters). The kit installs into the **interface/harness**, not into consumer repositories.

**Per-project alignment:** run **`/setup-oakstack`** (shape in this repo; marketplace publish later). Setup detects Matt/pstack prerequisites, prompts where missing, and points at Oakstack prefs/stubs. **`doctor`** is the non-interactive check setup (and later CI) can call.

**Generic fallback (no plugin):** clone or open this repo and follow [`adapters/generic/file-and-spawn.md`](adapters/generic/file-and-spawn.md) — hub + workers from files and a second chat only.

## Layout (P1)

| Path | Role |
| --- | --- |
| [`contracts/`](contracts/) | Hub, worker, kickoff, messages, task board, spawn rules, store layout |
| [`workflows/`](workflows/) | Store hygiene, troubleshooting summaries, interactive product loop |
| [`templates/project-store/`](templates/project-store/) | Preferences skeleton, archived index, friction-log stub |
| [`principles/`](principles/) | Six starter decision rules (cite in kickoffs) |
| [`adapters/`](adapters/) | Adapter contract + generic file-and-spawn; Cursor/Claude stubs |
| [`skills/setup-oakstack/`](skills/setup-oakstack/) | `/setup-oakstack` skill shape (detect / prompt / point) |

Later phases add SDLC docs, mistake-ledger schemas/scripts, fuller adapters, and Mixed cleanup.

## License

[MIT](LICENSE) — public under [RussOakham/oakstack](https://github.com/RussOakham/oakstack).

## Proof

See [`docs/generic-adapter-dry-run.md`](docs/generic-adapter-dry-run.md) for a hub + one worker dry-run using only files and a second chat.
