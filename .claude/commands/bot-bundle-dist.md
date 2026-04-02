---
name: bot-bundle-dist
description: Workflow command scaffold for bot-bundle-dist in 999.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /bot-bundle-dist

Use this workflow when working on **bot-bundle-dist** in `999`.

## Goal

Regenerate and commit built distribution files for the frontend or scripts.

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

- Build the project to generate updated dist files (HTML, JS, maps, etc).
- Commit the new or changed files in dist/ directory.
- Optionally include updated example assets (e.g., images, YAMLs) if relevant.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.