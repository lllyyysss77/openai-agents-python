---
name: version-bump
description: Workflow command scaffold for version-bump in openai-agents-python.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /version-bump

Use this workflow when working on **version-bump** in `openai-agents-python`.

## Goal

Bumps the project version and updates lock files for a new release.

## Common Files

- `pyproject.toml`
- `uv.lock`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Update version in pyproject.toml
- Update uv.lock or other lock files
- Commit with 'Bump version' in message

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.