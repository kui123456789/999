---
name: dependency-bump
description: Workflow command scaffold for dependency-bump in 999.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /dependency-bump

Use this workflow when working on **dependency-bump** in `999`.

## Goal

Update project dependencies and type definitions to latest versions.

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

- Update package.json and pnpm-lock.yaml with new dependency versions.
- Update one or more @types/function/*.d.ts or @types/iframe/*.d.ts files as needed.
- Optionally update tavern_sync.mjs if related to type or dependency changes.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.