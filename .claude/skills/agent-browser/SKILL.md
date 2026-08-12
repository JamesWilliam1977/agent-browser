```markdown
# agent-browser Development Patterns

> Auto-generated skill from repository analysis

## Overview

This skill introduces the core development patterns and workflows for the `agent-browser` repository, a TypeScript-based project with no detected frontend framework. The repository emphasizes clear documentation, modular code organization, and a disciplined approach to releases and feature development. You'll learn the project's coding conventions, how to update documentation, implement new CLI features, manage releases, and write tests.

## Coding Conventions

### File Naming

- Use **camelCase** for file names.
  - Example: `userAgentManager.ts`, `browserSessionHandler.ts`

### Import Style

- Use **alias imports** for modules.
  - Example:
    ```typescript
    import { startSession } from '@browser/sessionManager';
    ```

### Export Style

- **Mixed**: Both named and default exports are used.
  - Named export example:
    ```typescript
    export function launchBrowser() { ... }
    ```
  - Default export example:
    ```typescript
    export default BrowserAgent;
    ```

### Commit Patterns

- Commits use mixed types, with common prefixes like `docs` and `chore`.
- Keep commit messages concise (~39 characters on average).

## Workflows

### Update Documentation and References

**Trigger:** When adding new features, changing feature coverage, or updating/correcting documentation and reference material.  
**Command:** `/update-docs`

1. Edit or add `.mdx` files in `docs/src/app/` to document features or update navigation.
2. Update `skill-data/core/SKILL.md` and related references (e.g., `commands.md`, `video-recording.md`).
3. Update `README.md` for high-level documentation.
4. Optionally, update `docs/src/lib/` for navigation or page titles.

**Files Involved:**
- `docs/src/app/**/*.mdx`
- `docs/src/app/**/*.tsx`
- `docs/src/lib/docs-navigation.ts`
- `docs/src/lib/page-titles.ts`
- `skill-data/core/SKILL.md`
- `skill-data/core/references/*.md`
- `README.md`

**Example:**
```markdown
# Adding a new feature guide

1. Create `docs/src/app/new-feature.mdx`
2. Update `docs/src/lib/docs-navigation.ts` to add the new page to the sidebar.
3. Edit `README.md` to mention the new feature.
```

---

### Feature Implementation with CLI and Docs Update

**Trigger:** When adding or changing a CLI/daemon feature or output, requiring code, tests, and documentation updates.  
**Command:** `/add-cli-feature`

1. Modify or add Rust source files in `cli/src/native/` and `cli/src/output.rs` for feature logic.
2. Update or add tests in `cli/src/native/e2e_tests.rs`.
3. Update documentation in `docs/src/app/` and `README.md`.
4. Update `skill-data/core/SKILL.md` and references as needed.

**Files Involved:**
- `cli/src/native/*.rs`
- `cli/src/output.rs`
- `cli/src/native/e2e_tests.rs`
- `docs/src/app/**/*.mdx`
- `README.md`
- `skill-data/core/SKILL.md`
- `skill-data/core/references/*.md`

**Example:**
```rust
// cli/src/native/new_feature.rs
pub fn new_feature() {
    // feature logic here
}
```
```typescript
// docs/src/app/new-cli-feature.mdx
## New CLI Feature
Describe the new feature and usage here.
```

---

### Release Version Bump

**Trigger:** When preparing a new release version.  
**Command:** `/release`

1. Update `CHANGELOG.md` with release notes.
2. Bump version numbers in `cli/Cargo.toml`, `cli/Cargo.lock`, `package.json`, and `packages/dashboard/package.json`.

**Files Involved:**
- `CHANGELOG.md`
- `cli/Cargo.toml`
- `cli/Cargo.lock`
- `package.json`
- `packages/dashboard/package.json`

**Example:**
```diff
// CHANGELOG.md
+ ## 1.2.0
+ - Added new browser automation feature

// package.json
- "version": "1.1.0"
+ "version": "1.2.0"
```

## Testing Patterns

- Test files follow the pattern: `*.test.*`
- The testing framework is **unknown** (not detected), but tests are colocated with source files.
- Example test file: `browserSession.test.ts`
- Example test snippet:
  ```typescript
  describe('BrowserSession', () => {
    it('should launch a browser', () => {
      // test logic here
    });
  });
  ```

## Commands

| Command         | Purpose                                                        |
|-----------------|----------------------------------------------------------------|
| /update-docs    | Update or expand documentation and reference files             |
| /add-cli-feature| Implement or improve CLI/daemon features and update docs/tests |
| /release        | Prepare and publish a new release version                      |
```