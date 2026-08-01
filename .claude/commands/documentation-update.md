---
name: documentation-update
description: Workflow command scaffold for documentation-update in openai-agents-python.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /documentation-update

Use this workflow when working on **documentation-update** in `openai-agents-python`.

## Goal

Updates or improves documentation files, including main docs, translated pages, and configuration.

## Common Files

- `docs/*.md`
- `docs/**/index.md`
- `README.md`
- `mkdocs.yml`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit one or more files in docs/ and/or README.md
- Optionally update mkdocs.yml or other doc config
- Commit with 'docs:' prefix in message

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.