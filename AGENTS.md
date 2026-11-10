# AGENTS.md

Embodied AI / Physical AI data platform template (real2sim2real, synthetic data, asset pipelines, simulation).

Read this file first in every session. Keep changes atomic and reviewable.

## Commands

```bash
# Setup
uv sync

# Checks (run before finishing work)
uv run ruff check .
uv run pytest -x
# Add: typecheck, data validation, sim checks as needed
```

## Development Process (mandatory)

1. **Spec first**: Non-trivial work starts with a short spec in `specs/` or linked issue. Confirm understanding before coding.
2. **Plan**: Write a short plan (steps + verification points) before large changes.
3. **Small changes**: Prefer atomic, reviewable slices. One intent per commit/PR.
4. **Verify**: Run relevant checks and show evidence. Do not claim success without output.
5. **Review**: Independent review before merge. No self-merge of agent-written code.
6. **Document**: Update docs or add ADR when conventions or architecture change.

## Boundaries

**Ask first**
- New dependencies, data schema / format changes, or external service integrations.
- Changes to simulation physics, asset standards, quality gates, or CI.
- Anything under `infra/`, secrets, or production configs.

**Never**
- Commit secrets or credentials.
- Edit generated files by hand.
- Force-push or merge without explicit human approval.
- Invent file paths, API behavior, or test results.

## Skills

Prefer skills under `.agents/skills/` when the task matches.

- `asset-pipeline`: CAD / USD / SimReady conversion and validation workflows.
- NVIDIA official skills (Isaac Sim, Omniverse CAD-to-SimReady, etc.) are encouraged when relevant.

## Code & Style

- Prefer existing patterns over new abstractions.
- Small, focused changes. No speculative features.
- Comments explain *why*, not *what*.
- Keep this file short; move details to `docs/` and link them.
