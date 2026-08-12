---
name: update-documentation-and-references
description: Workflow command scaffold for update-documentation-and-references in agent-browser.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /update-documentation-and-references

Use this workflow when working on **update-documentation-and-references** in `agent-browser`.

## Goal

Updates or expands documentation and reference files, often to surface new features, correct stale information, or improve discoverability.

## Common Files

- `docs/src/app/**/*.mdx`
- `docs/src/app/**/*.tsx`
- `docs/src/lib/docs-navigation.ts`
- `docs/src/lib/page-titles.ts`
- `skill-data/core/SKILL.md`
- `skill-data/core/references/*.md`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit or add .mdx files in docs/src/app/ to document features or update navigation.
- Update skill-data/core/SKILL.md and related references (e.g., commands.md, video-recording.md).
- Update README.md for high-level documentation.
- Optionally, update docs/src/lib/ for navigation or page titles.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.