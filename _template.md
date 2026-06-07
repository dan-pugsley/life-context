# Folder Template

Defines the fractal structure used at every domain node.

## Universal files

| File | Purpose | Author |
|---|---|---|
| README.md | Describes the domain, lists children | Framework |
| profile.md | Stable user data — attributes, history, baseline benchmarks, preferences | AI (from user input) |
| status.md | Living state — current restrictions, progressions, working values. Optional: present only where a domain has volatile state | AI (from user input) |
| onboarding.md | AI onboarding playbook — guides structured conversation to populate profile and status | Framework |

## Optional folders

| Folder | Purpose | Structure |
|---|---|---|
| events/ | Timestamped entries for this domain | Flat .md files: YYYY-MM-DD_description.md |
| issues/ | Ongoing concerns or conditions | Named subfolders containing flat timestamped .md files + optional assets/ |
| assets/ | Supporting binary files | Images, PDFs, scans, reports |

## Below domain level

Below the deepest domain node, structure is domain-specific and not governed by this template. The fractal pattern (README, profile, onboarding) applies at domain boundaries only.

## Frontmatter

All data files use YAML frontmatter. Universal fields:

| Field | Type | Description |
|---|---|---|
| created | date | YYYY-MM-DD |
| updated | date | YYYY-MM-DD |
| summary | string | One-line description for AI scanning |

Event files may additionally include:

| Field | Type | Description |
|---|---|---|
| occurred | date | When the event happened, if different from created |

## Issues

An issue folder (e.g., issues/back/) is not a domain — it is a flat collection of records about a specific condition. It does not contain README.md, profile.md, or onboarding.md. Key information from issues is summarised in the parent domain's profile.md.

## Naming

- Folders: lowercase, hyphens for multi-word
- Event files: YYYY-MM-DD_kebab-case-description.md
- Framework/meta items: underscore prefix (_template.md, _decisions/)
