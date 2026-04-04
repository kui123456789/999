```markdown
# 999 Development Patterns

> Auto-generated skill from repository analysis

## Overview

This skill introduces the core development patterns, coding conventions, and automated workflows used in the `999` repository—a TypeScript React codebase. You'll learn how to structure code, manage dependencies, bundle artifacts, update example assets, maintain build configurations, and refine documentation. The guide also covers commit conventions and provides ready-to-use commands for common automation tasks.

## Coding Conventions

### File Naming

- Use **camelCase** for file names.
  - Example: `autoUpdateCard.ts`, `commonUtils.ts`

### Import Style

- Use **absolute imports** for modules.
  - Example:
    ```typescript
    import { updateStatusBar } from 'util/common';
    ```

### Export Style

- **Mixed**: Both default and named exports are used.
  - Example:
    ```typescript
    // Named export
    export function updateCharacterCard() { ... }

    // Default export
    export default CharacterCard;
    ```

### Commit Message Patterns

- Use prefixes: `[bot]`, `feat`, `fix`, `chore`
- Keep messages concise (average ~17 characters)
  - Example: `feat: add status bar`

## Workflows

### Bump Dependencies

**Trigger:** When you need to update project dependencies or type definitions.  
**Command:** `/bump-deps`

1. Update one or more `@types/* .d.ts` files and/or `tavern_sync.mjs`.
2. Update `package.json` and `pnpm-lock.yaml`.
3. Commit with a message like `Bump deps` or similar.

**Example:**
```sh
pnpm up
git add package.json pnpm-lock.yaml
git commit -m "Bump deps: update @types"
```

---

### Bot Bundle Artifacts

**Trigger:** After building the project, when you need to update and commit `dist/` artifacts (often via bot).  
**Command:** `/bundle`

1. Build the project to generate updated `dist/` files.
2. Commit updated files such as `.js`, `.js.map`, `.html`, `.png`.
3. Use commit message: `[bot] bundle`

**Example:**
```sh
pnpm build
git add dist/
git commit -m "[bot] bundle"
```

---

### Update Example Character Card

**Trigger:** When adding or updating features for the example character card (scripts, YAML, images).  
**Command:** `/update-character-card`

1. Edit or add files in `示例/角色卡示例/` (YAML, PNG, scripts).
2. Optionally update `util/common.ts` or related scripts.
3. Commit your changes.

**Example:**
```sh
vim 示例/角色卡示例/index.yaml
git add 示例/角色卡示例/index.yaml
git commit -m "feat: update example card"
```

---

### Update Build Config

**Trigger:** When changing build or CI behavior.  
**Command:** `/update-build-config`

1. Edit `webpack.config.ts` or `.github/workflows/bundle.yaml`.
2. Commit your changes.

**Example:**
```sh
vim webpack.config.ts
git add webpack.config.ts
git commit -m "chore: update build config"
```

---

### Update Prompt or Rule Docs

**Trigger:** When refining prompts, rules, or documentation for AI/codegen tools.  
**Command:** `/update-prompt-docs`

1. Edit `.cursor/rules/*.mdc` or similar rule/prompt files.
2. Optionally update `.augment`, `.clinerules`, `.kilocode`, `.roo` files.
3. Commit your changes.

**Example:**
```sh
vim .cursor/rules/character-card.mdc
git add .cursor/rules/character-card.mdc
git commit -m "chore: update prompt docs"
```

## Testing Patterns

- **Test files** use the pattern: `*.test.*`
- **Testing framework:** Unknown (look for `.test.ts` or `.test.js` files)
- Place tests alongside source files or in a dedicated test directory.
- Example test file: `statusBar.test.ts`

## Commands

| Command                  | Purpose                                                      |
|--------------------------|--------------------------------------------------------------|
| /bump-deps               | Update dependencies and type definitions                      |
| /bundle                  | Build and commit updated `dist/` artifacts                   |
| /update-character-card   | Add or update example character card features                 |
| /update-build-config     | Change build or CI configuration                             |
| /update-prompt-docs      | Update AI/codegen prompt or rule documentation               |
```