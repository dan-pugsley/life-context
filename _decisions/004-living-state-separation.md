---
created: 2026-05-31
status: accepted
---

# Living-State Separation (status.md)

## Context

`profile.md` mixed stable facts (history, baseline benchmarks, preferences) with volatile state (current injury restrictions, rehab progression stages, working loads, bodyweight). The volatile facts were copied into multiple READMEs and plans, creating a maintenance burden and at least one traceability failure — a workout asserting a rehab stage with no authoritative source. Changing one fact required edits in several files, and copies drifted.

## Decision

Separate every fact into one of three layers, each with a single home:

- **Stable profile** (`profile.md`) — identity, history, baseline benchmarks, preferences. Rarely edited.
- **Living status** (`status.md`, new) — current restrictions, rehab progression stages, working loads, bodyweight, current block. Edited often. The single source of truth for volatile state.
- **Dated history** (`issues/`, `events/`) — append-only source records (injury notes, imaging, test results).

`status.md` is an **optional** universal file, present only where a domain has meaningful live state (no empty stubs). Plans, READMEs, and workouts **reference** `status.md`; they must not restate its contents.

## Reasoning

- One source of truth per changing fact — update once, every consumer inherits it.
- Restores traceability: "where am I right now" (rehab stage, working loads) has an authoritative home instead of being re-derived or guessed.
- `status.md` is the current-snapshot layer; `events/` is the dated history that feeds it; `profile.md` is the stable backstory — mirroring how clinical summaries separate current state from the record (see [001-fhir-inspired-data-model.md](001-fhir-inspired-data-model.md)).
- Tags were dropped project-wide in the same pass: inert without tooling and inconsistently applied. Reintroduce as a deliberate, queryable taxonomy if and when a structured app consumes the data.
