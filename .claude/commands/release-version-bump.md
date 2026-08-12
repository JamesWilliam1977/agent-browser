---
name: release-version-bump
description: Workflow command scaffold for release-version-bump in agent-browser.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /release-version-bump

Use this workflow when working on **release-version-bump** in `agent-browser`.

## Goal

Prepares a new release by updating version numbers and changelogs across relevant files.

## Common Files

- `CHANGELOG.md`
- `cli/Cargo.toml`
- `cli/Cargo.lock`
- `package.json`
- `packages/dashboard/package.json`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Update CHANGELOG.md with release notes.
- Bump version numbers in cli/Cargo.toml, cli/Cargo.lock, package.json, and packages/dashboard/package.json.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.