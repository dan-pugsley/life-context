---
created: 2026-05-24
status: accepted
---

# FHIR-Inspired Data Model

## Context

We needed a framework for organising health-related data that separates ongoing conditions from point-in-time events and measurements.

## Decision

Adopt the conceptual separation from the FHIR (Fast Healthcare Interoperability Resources) standard:

- **Conditions** (ongoing) — captured in profile.md files
- **Encounters** (point-in-time interactions) — captured as event files
- **Observations** (measurements/assessments) — captured as event files

Encounters and observations coexist in events/ and issues/ folders, distinguished by context rather than separate folder structures.

## Reasoning

FHIR is an established healthcare data standard. Adopting its conceptual model (without its full schema complexity) gives us proven data separation patterns that map cleanly to our profile/events architecture.
