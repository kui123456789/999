---
name: bump-dependencies
description: Workflow command scaffold for bump-dependencies in 999.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /bump-dependencies

Use this workflow when working on **bump-dependencies** in `999`.

## Goal

Updates project dependencies and related type definitions.

## Common Files

- `package.json`
- `pnpm-lock.yaml`
- `@types/function/*.d.ts`
- `@types/iframe/*.d.ts`
- `tavern_sync.mjs`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Update package.json and pnpm-lock.yaml to new dependency versions
- Update relevant @types/*.d.ts files if type packages are bumped
- Optionally update tavern_sync.mjs if related to dependency changes

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.