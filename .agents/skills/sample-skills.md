---
name: asset-pipeline
description: Guide CAD/USD/SimReady conversion, validation, and packaging workflows for embodied AI assets. Use when converting models, checking SimReady conformance, or preparing assets for simulation.
---

# Asset Pipeline Skill

## When to use

Use this skill for requests involving:

- CAD (STEP, etc.) → OpenUSD conversion
- SimReady conformance and validation
- Physics / material assignment for simulation
- Packaging assets for Isaac Sim or similar

## Steps

1. Identify source assets and target format / profile.
2. Prefer official NVIDIA skills (e.g. omniverse-cad-to-simready) when available.
3. Run conversion and validation tools; capture output.
4. Document any failures or manual fixes.
5. Place final assets in the agreed directory and update any manifest.

## Notes

- Ask before changing asset standards or quality gates.
- Show validation evidence before claiming success.
