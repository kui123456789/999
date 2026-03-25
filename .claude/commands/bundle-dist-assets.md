---
name: bundle-dist-assets
description: Workflow command scaffold for bundle-dist-assets in 999.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /bundle-dist-assets

Use this workflow when working on **bundle-dist-assets** in `999`.

## Goal

Bundles and outputs built assets to the dist directory, typically after code or asset changes.

## Common Files

- `dist/角色卡示例/界面/状态栏/index.html`
- `dist/角色卡示例/界面/状态栏/index.js.map`
- `dist/角色卡示例/脚本/自动更新角色卡/index.js`
- `dist/角色卡示例/脚本/自动更新角色卡/index.js.map`
- `示例/角色卡示例/角色卡示例.png`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Build or bundle source code/assets
- Output results to dist/ directory (e.g., .js, .js.map, .html)
- Optionally update related example images or files

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.