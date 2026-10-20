# Development Process

This document defines the expected workflow for human + AI agent collaboration on the embodied AI platform.

## Flow

1. **Issue / Spec** — Non-trivial work begins with a short written spec (`specs/`) or clear issue.
2. **Plan** — Agent or human writes a short plan with steps and verification points.
3. **Implement** — Small, reviewable slices. Prefer one intent per commit.
4. **Verify** — Run lint, tests, and domain checks (data quality, sim validation). Show evidence.
5. **PR + Review** — Independent review (human or second agent). No self-merge of agent-written code.
6. **Merge** — Only after checks pass and review is approved.

## AI Agent Rules

- Always start from `AGENTS.md`.
- Use Skills in `.agents/skills/` for repeated workflows (asset conversion, data validation, documentation).
- Produce evidence (command output, validation results, screenshots) before claiming done.
- Keep PRs small enough for human review in under 15 minutes.

## Quality Gates

- All PRs must pass CI (lint + tests).
- Simulation or data pipeline changes require corresponding validation output.
- Architecture or convention changes require an ADR in `docs/adr/`.

## Skills Location

Team skills live in `.agents/skills/`. They travel with the repository so every clone has them available to Codex and compatible agents.
