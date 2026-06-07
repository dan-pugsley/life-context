---
created: 2026-05-24
status: accepted
---

# Markdown with YAML Frontmatter

## Context

We needed a file format that is readable by both humans and AI, works well with git version control, and supports structured metadata.

## Decision

Use Markdown (.md) files with YAML frontmatter for all data files.

Universal frontmatter fields: created, updated, tags, summary. Event files may additionally include occurred.

## Reasoning

- Human readable and editable in any text editor
- AI parseable — every major LLM handles markdown natively
- Git-friendly — text-based with clean diffs
- YAML frontmatter provides structured metadata without sacrificing readability
- Converts cleanly to HTML for potential future web app use
- Universally supported by tooling (VS Code, GitHub, static site generators)
