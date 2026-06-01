---
name: feature-implementation-with-cli-and-docs-update
description: Workflow command scaffold for feature-implementation-with-cli-and-docs-update in agent-browser.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /feature-implementation-with-cli-and-docs-update

Use this workflow when working on **feature-implementation-with-cli-and-docs-update** in `agent-browser`.

## Goal

Implements or improves a CLI/daemon feature, updates related CLI source files, adds or updates tests, and synchronizes documentation and references.

## Common Files

- `cli/src/native/*.rs`
- `cli/src/output.rs`
- `cli/src/native/e2e_tests.rs`
- `docs/src/app/**/*.mdx`
- `README.md`
- `skill-data/core/SKILL.md`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Modify or add Rust source files in cli/src/native/ and cli/src/output.rs for feature logic.
- Update or add tests in cli/src/native/e2e_tests.rs.
- Update documentation in docs/src/app/ and README.md.
- Update skill-data/core/SKILL.md and references as needed.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.