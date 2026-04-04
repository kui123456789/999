---
name: bump-dependencies
description: Workflow command scaffold for bump-dependencies in 999.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /bump-dependencies

Use this workflow when working on **bump-dependencies** in `999`.

## Goal

Updates project dependencies and type definitions, ensuring the project uses the latest versions.

## Common Files

- `package.json`
- `pnpm-lock.yaml`
- `tavern_sync.mjs`
- `@types/function/*.d.ts`
- `@types/iframe/*.d.ts`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Update one or more @types/* .d.ts files and/or tavern_sync.mjs
- Update package.json and pnpm-lock.yaml
- Commit with message containing 'Bump deps' or similar

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.