---
name: 999-conventions
description: Development conventions and patterns for 999. TypeScript React project with freeform commits.
---

# 999 Conventions

> Generated from [kui123456789/999](https://github.com/kui123456789/999) on 2026-03-25

## Overview

This skill teaches Claude the development patterns and conventions used in 999.

## Tech Stack

- **Primary Language**: TypeScript
- **Framework**: React
- **Architecture**: hybrid module organization
- **Test Location**: separate

## When to Use This Skill

Activate this skill when:
- Making changes to this repository
- Adding new features following established patterns
- Writing tests that match project conventions
- Creating commits with proper message format

## Commit Conventions

Follow these commit message conventions based on 200 analyzed commits.

### Commit Style: Free-form Messages

### Prefixes Used

- `[bot]`
- `feat`
- `fix`

### Message Guidelines

- Average message length: ~19 characters
- Keep first line concise and descriptive
- Use imperative mood ("Add feature" not "Added feature")


*Commit message example*

```text
feat: 提醒怎么添加按钮
```

*Commit message example*

```text
fix: parseString 在一些情况下应该优先解析 json
```

*Commit message example*

```text
chore: bump deps
```

*Commit message example*

```text
ci: 更新 node 版本为 24
```

*Commit message example*

```text
style: casing
```

*Commit message example*

```text
[bot] bump template repository update
```

*Commit message example*

```text
[bot] Bump deps
```

*Commit message example*

```text
[bot] bundle
```

## Architecture

### Project Structure: Single Package

This project uses **hybrid** module organization.

### Source Layout

```
src/
├── 世界书/
├── 正则/
├── 角色卡/
├── 酒馆助手/
├── 预设/
```

### Configuration Files

- `.prettierrc`
- `package.json`
- `tsconfig.json`

### Guidelines

- This project uses a hybrid organization
- Follow existing patterns when adding new code

## Code Style

### Language: TypeScript

### Naming Conventions

| Element | Convention |
|---------|------------|
| Files | PascalCase |
| Functions | camelCase |
| Classes | PascalCase |
| Constants | SCREAMING_SNAKE_CASE |

### Import Style: Relative Imports

### Export Style: Named Exports


*Preferred import style*

```typescript
// Use relative imports
import { Button } from '../components/Button'
import { useAuth } from './hooks/useAuth'
```

*Preferred export style*

```typescript
// Use named exports
export function calculateTotal() { ... }
export const TAX_RATE = 0.1
export interface Order { ... }
```

## Common Workflows

These workflows were detected from analyzing commit patterns.

### Feature Development

Standard feature implementation workflow

**Frequency**: ~4 times per month

**Steps**:
1. Add feature implementation
2. Add tests for feature
3. Update documentation

**Files typically involved**:
- `util/*`
- `示例/角色卡示例/脚本/自动更新角色卡/*`
- `/*`

**Example commit sequence**:
```
feat: 调整变量结构设计提示词
[bot] Bump deps
[bot] Bump deps
```

### Bump Dependencies

Updates project dependencies and related type definitions.

**Frequency**: ~8 times per month

**Steps**:
1. Update package.json and pnpm-lock.yaml to new dependency versions
2. Update relevant @types/*.d.ts files if type packages are bumped
3. Optionally update tavern_sync.mjs if related to dependency changes

**Files typically involved**:
- `package.json`
- `pnpm-lock.yaml`
- `@types/function/*.d.ts`
- `@types/iframe/*.d.ts`
- `tavern_sync.mjs`

**Example commit sequence**:
```
Update package.json and pnpm-lock.yaml to new dependency versions
Update relevant @types/*.d.ts files if type packages are bumped
Optionally update tavern_sync.mjs if related to dependency changes
```

### Bundle Dist Assets

Bundles and outputs built assets to the dist directory, typically after code or asset changes.

**Frequency**: ~3 times per month

**Steps**:
1. Build or bundle source code/assets
2. Output results to dist/ directory (e.g., .js, .js.map, .html)
3. Optionally update related example images or files

**Files typically involved**:
- `dist/角色卡示例/界面/状态栏/index.html`
- `dist/角色卡示例/界面/状态栏/index.js.map`
- `dist/角色卡示例/脚本/自动更新角色卡/index.js`
- `dist/角色卡示例/脚本/自动更新角色卡/index.js.map`
- `示例/角色卡示例/角色卡示例.png`

**Example commit sequence**:
```
Build or bundle source code/assets
Output results to dist/ directory (e.g., .js, .js.map, .html)
Optionally update related example images or files
```

### Update Example Or Doc Files

Makes changes to example files, documentation, or sample assets for demonstration or clarification.

**Frequency**: ~2 times per month

**Steps**:
1. Edit or add files in 示例/ (examples) or 初始模板/ (templates)
2. Update .md, .yaml, .vue, .png, or .txt files as needed
3. Optionally update related files in dist/ if assets are rebuilt

**Files typically involved**:
- `示例/角色卡示例/*`
- `示例/前端界面示例/*`
- `初始模板/角色卡/*`

**Example commit sequence**:
```
Edit or add files in 示例/ (examples) or 初始模板/ (templates)
Update .md, .yaml, .vue, .png, or .txt files as needed
Optionally update related files in dist/ if assets are rebuilt
```


## Best Practices

Based on analysis of the codebase, follow these practices:

### Do

- Use PascalCase for file names
- Prefer named exports

### Don't

- Don't deviate from established patterns without discussion

---

*This skill was auto-generated by [ECC Tools](https://ecc.tools). Review and customize as needed for your team.*
