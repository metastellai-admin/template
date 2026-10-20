# Embodied AI Agent Template

Sample repository structure for an embodied AI / Physical AI engineering team.

It provides:

- A short, practical `AGENTS.md` as the entry point for coding agents (Codex, Claude, Cursor, etc.).
- A defined development process that balances AI usage with stability.
- A place for team Skills under `.agents/skills/`.
- Supporting docs and ADR structure.

## Quick Start

1. Copy this structure into your repository (or use it as a starting point).
2. Fill in real commands, stack details, and domain-specific rules in `AGENTS.md`.
3. Add team Skills under `.agents/skills/`.
4. Keep `AGENTS.md` short; put longer guidance in `docs/`.

## Structure

```
AGENTS.md                  # Agent entry point (read first)
docs/
  development-process.md   # Detailed workflow
  adr/                     # Architecture Decision Records
.agents/skills/            # Team skills (auto-discovered by agents)
specs/                     # Feature / data specs
.github/workflows/         # CI
```

## Philosophy

- Maximize useful AI assistance.
- Keep agent context small and accurate.
- Enforce review, verification, and small changes for stability.
- Skills capture repeated domain workflows (asset pipelines, data quality, simulation).

See `AGENTS.md` and `docs/development-process.md` for the rules.
