# Skill Schema Guidelines

Use this folder for cross-skill output-shape conventions.

## Current Convention

- Every skill may expose `schemas/output.schema.json`.
- Example payloads in `examples/output.json` should match that schema.
- Schemas should stay intentionally narrow and validate only the public output contract, not every internal implementation detail.

## Recommended Base Fields

Use these when they are meaningful:

- `requires_human_approval`
- `suggested_actions`
- `risk_note`
- `confidence`

Do not force them into every skill if the concept does not fit.

## Design Rules

- Prefer simple JSON Schema objects over clever composition.
- Keep required fields minimal.
- Validate shape and important enums, not business truth.
- Preserve room for future extension by allowing additional properties unless the contract is intentionally strict.
