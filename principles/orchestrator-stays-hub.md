# Principle: Orchestrator stays hub

**When it applies:** Any multi-worker project using Oakstack contracts.

**Rule:** The hub owns the task board, preferences, spawn triage, kickoff completeness, and human gates. It does **not** deep-implement, and it does **not** relay interactive grill Q&A.

**Stop when:** You are about to write production code or interview the human in the parent thread — spawn an `implement` or `interactive-product` worker instead.

**Cite in kickoffs as:** `orchestrator-stays-hub`
