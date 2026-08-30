---
name: bot-bundle-artifacts
description: Workflow command scaffold for bot-bundle-artifacts in 999.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /bot-bundle-artifacts

Use this workflow when working on **bot-bundle-artifacts** in `999`.

## Goal

Bundles and commits built/dist artifacts, typically after code or config changes.

## Common Files

- `dist/角色卡示例/界面/状态栏/index.html`
- `dist/角色卡示例/界面/状态栏/index.js.map`
- `dist/角色卡示例/界面/状态栏/main.css.map`
- `dist/角色卡示例/脚本/自动更新角色卡/index.js`
- `dist/角色卡示例/脚本/自动更新角色卡/index.js.map`
- `dist/角色卡示例/脚本/变量结构/index.js.map`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Build project to generate dist/ files
- Commit updated dist/ files (e.g., .js, .js.map, .html, .png)
- Use commit message '[bot] bundle'

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.