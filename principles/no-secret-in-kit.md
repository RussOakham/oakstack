# Principle: No secret in kit

**When it applies:** Any contribution to Oakstack itself, templates, examples, or public adapters.

**Rule:** Oakstack never ships hostnames, tokens, vault paths, or household IDs. Consumers overlay secrets locally.

**Stop when:** A PR or paste would add private infra, money taxonomy UUIDs, or credential-shaped strings — redact and keep them in the consumer overlay.

**Cite in kickoffs as:** `no-secret-in-kit`
