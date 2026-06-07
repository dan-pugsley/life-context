---
created: 2026-05-24
status: accepted
---

# Fractal Template Structure

## Context

We needed a consistent, navigable structure that scales across any life domain while remaining easy for AI to discover and traverse.

## Decision

Every domain folder follows a fractal template:

- README.md (domain description, children)
- profile.md (stable user data)
- status.md (living state — optional, where volatile state exists)
- onboarding.md (AI onboarding playbook)

Optional folders: events/, issues/, assets/.

Below domain-level nodes, structure is domain-specific and not governed by the template. Framework/meta items use underscore prefixes to distinguish from life domains.

## Reasoning

A consistent template means the AI knows what to expect at any level, reducing navigation overhead. The fractal pattern scales naturally — adding a new domain is just creating a folder with the three standard files. Domain-specific structure below the template level allows flexibility where needed (e.g., periodization hierarchy for exercise programming).
