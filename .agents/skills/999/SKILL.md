```markdown
# 999 Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill documents the core development patterns, coding conventions, and automated workflows for the `999` repository, a TypeScript project using React. It covers file organization, code style, commit practices, and the main workflows for dependency management, distribution builds, and example content updates. This guide is essential for contributors aiming for consistency and efficiency in this codebase.

## Coding Conventions

- **File Naming:**  
  Use PascalCase for all file names, including components and modules.
  ```
  // Good
  MyComponent.tsx
  UserProfile.test.ts

  // Bad
  mycomponent.tsx
  user_profile.test.ts
  ```

- **Import Style:**  
  Use relative imports for all modules.
  ```typescript
  import { UserProfile } from './UserProfile';
  import { calculateScore } from '../utils/calculateScore';
  ```

- **Export Style:**  
  Use named exports exclusively.
  ```typescript
  // Good
  export const MyComponent = () => { ... };

  // Bad
  export default MyComponent;
  ```

- **Commit Patterns:**  
  - Prefixes: `[bot]`, `feat`, `fix` (freeform allowed)
  - Keep commit messages concise (average: 18 characters)
  ```
  feat: add status bar
  fix: typo in props
  [bot] bump dependencies
  ```

## Workflows

### Dependency Bump
**Trigger:** When dependencies or type definitions need to be updated (often by bot or for security/compatibility).  
**Command:** `/bump-deps`

1. Update `package.json` and `pnpm-lock.yaml` with new dependency versions.
2. Update one or more `@types/function/*.d.ts` or `@types/iframe/*.d.ts` files as needed.
3. Optionally update `tavern_sync.mjs` if related to type or dependency changes.
4. Commit the changes with a clear message (e.g., `[bot] bump deps`).

**Files Involved:**
- `package.json`
- `pnpm-lock.yaml`
- `@types/function/*.d.ts`
- `@types/iframe/*.d.ts`
- `tavern_sync.mjs`

```bash
# Example command
/bump-deps
```

---

### Bot Bundle Dist
**Trigger:** When source code or assets change, triggering a new build (often by bot).  
**Command:** `/bundle-dist`

1. Build the project to generate updated dist files (HTML, JS, maps, etc).
2. Commit the new or changed files in the `dist/` directory.
3. Optionally include updated example assets (e.g., images, YAMLs) if relevant.

**Files Involved:**
- `dist/角色卡示例/界面/状态栏/index.html`
- `dist/角色卡示例/界面/状态栏/index.js.map`
- `dist/角色卡示例/脚本/自动更新角色卡/index.js`
- `dist/角色卡示例/脚本/自动更新角色卡/index.js.map`
- `示例/角色卡示例/角色卡示例.png`

```bash
# Example command
/bundle-dist
```

---

### Example Content Update
**Trigger:** When example/demo content needs to be added or corrected.  
**Command:** `/update-example`

1. Edit or add files under `示例/角色卡示例/` or related example directories.
2. Update YAML, markdown, or image files to reflect new examples or corrections.
3. Optionally update related scripts or documentation.
4. Commit with a descriptive message (e.g., `feat: update example YAML`).

**Files Involved:**
- `示例/角色卡示例/*.yaml`
- `示例/角色卡示例/*.md`
- `示例/角色卡示例/*.png`
- `示例/角色卡示例/世界书/**/*.yaml`

```bash
# Example command
/update-example
```

## Testing Patterns

- **Test File Naming:**  
  Test files follow the pattern `*.test.*`, e.g., `UserProfile.test.tsx`.
- **Testing Framework:**  
  The specific framework is unknown, but tests are colocated with code using the above pattern.

```typescript
// Example test file: UserProfile.test.tsx
import { render } from '@testing-library/react';
import { UserProfile } from './UserProfile';

test('renders user profile', () => {
  render(<UserProfile />);
  // assertions...
});
```

## Commands

| Command         | Purpose                                                      |
|-----------------|--------------------------------------------------------------|
| /bump-deps      | Update dependencies and type definitions to latest versions.  |
| /bundle-dist    | Regenerate and commit built distribution files.               |
| /update-example | Update example YAML, markdown, or image files for demos.      |
```
