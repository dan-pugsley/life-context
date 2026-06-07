# life-context

**An AI-managed context store for your life.** A structured, fractal knowledge base that gives any AI agent deep, persistent context about you — so it stops giving generic advice and starts giving advice that actually fits *you*.

This repository is the open **framework**: the architecture, conventions, and AI onboarding playbooks — with **no personal data**. You instantiate it, fill it with your own life (kept private), and point an AI agent at it.

> 👉 **Want to see it filled in?** Check out the **[`demo` branch](../../tree/demo)** for a complete worked example built around a fictional persona — real structure, synthetic data.

---

## The idea: context beats cleverness

Generic AI gives generic answers because it lacks context. Ask a chatbot *"how should I train this week?"* and it can't know about your knee injury, your travel schedule, last week's sessions, or that you respond badly to high volume — so it hedges into uselessness.

The usual workaround is to paste context into each chat. That has two problems:

1. **It doesn't persist.** You re-explain yourself every single time.
2. **It's silently biased.** You unconsciously steer the answer by *choosing* which context to share. Mention the knee but forget the deadline and you get a different plan — and you never notice the ones you didn't mention.

`life-context` fixes both. It's a durable, structured store of your life that sits *beside* the AI. All the relevant context is on the table **before** any question is asked — so the advice is both more personalised and less cherry-picked. Closer to what a great coach, advisor, or doctor who actually *knows you* would say.

The catalyst was training programming (managing real injuries across a real training block — see the [`demo` branch](../../tree/demo)), but the architecture is domain-agnostic: health, career, finances, relationships, learning — anything.

## How it works

### A fractal folder structure

Every domain of your life is a folder. Each folder follows the **same** template, all the way down — so an AI agent always knows what to expect at any level (see [`_template.md`](_template.md)).

| File | Purpose | Authored by |
|---|---|---|
| `README.md` | Orients an agent: what this domain is, what's beneath it | Framework |
| `profile.md` | **Stable** facts — identity, history, baselines, preferences | AI, from your input |
| `status.md` | **Living state** — what changes over time (optional; only where it's needed) | AI, from your input |
| `onboarding.md` | A playbook the AI runs to interview you and populate the above | Framework |

Domains nest as deeply as they need to (`health/exercise/programming/...`), and below the domain level the structure is free to become domain-specific.

### Stable profile vs. living status

The one rule that keeps the whole thing honest: **separate what's stable from what changes.** Your training history goes in `profile.md`; this week's working loads and current rehab stage go in `status.md`. Everything else *references* `status.md` rather than copying it, so there's a single source of truth for every volatile fact and nothing drifts out of date. ([Why →](_decisions/004-living-state-separation.md))

### AI-mediated onboarding

You don't fill these files in by hand. Each domain ships an `onboarding.md` — a structured interview playbook grounded in real frameworks (e.g. the exercise intake draws on NASM/ISSA personal-training models; career on Hoffman's *Start-up of You* and 80,000 Hours). Point an agent at the repo, and it walks you through a conversation and writes the results in the right place, in the right format.

Onboarding runs **top-down** — root before health, health before exercise — so each level informs the next.

## Privacy model: the framework vs. your data

This is the part worth understanding before you start.

- **Framework files** (`README.md`, `onboarding.md`, `_template.md`, `_decisions/`, `CLAUDE.md`) contain conventions and structure — **never personal data.** They're identical for everyone.
- **Data files** (`profile.md`, `status.md`, plus any `events/`, `issues/`, `assets/`) contain *your* life. They stay in **your private copy** and never come back here.

Because the framework files are data-free, the framework can be improved and shared freely, while your private instance pulls in those improvements — without any of your data ever leaking upward. (This repo is exactly that: a real personal system with the data swapped out for a synthetic example.)

## Getting started

1. **Create your own private copy.** Click **"Use this template"** (or fork/clone) and **make your copy private.** This is where your real data will live.
2. **Point an AI agent at it.** Anything that can read your files works — [Claude Code](https://claude.com/claude-code), Cursor, etc. The root [`CLAUDE.md`](CLAUDE.md) tells the agent how to navigate and maintain the store.
3. **Onboard, top-down.** Ask the agent to run the root `onboarding.md`, then each domain's. It interviews you and fills in the `profile.md` / `status.md` files.
4. **Use it.** Ask domain questions ("plan my training week", "should I take this contract?"). The agent reads your context first. As life changes, ask it to keep `status.md` current.

You don't have to fill in every domain — start with the one you care about most and grow from there. Delete domains you don't want; add your own by copying the template pattern.

## Repository structure

```
.
├── CLAUDE.md            # Agent instructions: how to navigate & maintain the store
├── _template.md         # The fractal convention every domain folder follows
├── _decisions/          # Architecture decision records — the "why"
├── onboarding.md        # Root onboarding playbook
├── profile.md           # Stable root context (identity, attributes, goals)  ← you fill in
├── status.md            # Living root state (e.g. bodyweight)                ← you fill in
│
├── health/              # README · onboarding · profile
│   ├── diet/            # README · onboarding · profile
│   └── exercise/        # README · onboarding · profile · status
│       └── programming/ # Periodised training: macro → meso → micro → workout
│           ├── README.md  feedback-playbook.md
│           └── onboarding/   # macrocycle · mesocycle · microcycle playbooks
│
└── career/              # README · onboarding · profile · status
```

The included domains (health, career) are a starting set, not a prescription — they're the ones the system was first built around.

## Design decisions

The reasoning behind the architecture lives in [`_decisions/`](_decisions/):

- [001 — FHIR-inspired data model](_decisions/001-fhir-inspired-data-model.md)
- [002 — Markdown with YAML frontmatter](_decisions/002-markdown-with-yaml-frontmatter.md)
- [003 — Fractal template structure](_decisions/003-fractal-template-structure.md)
- [004 — Living-state separation](_decisions/004-living-state-separation.md)

## License

[MIT](LICENSE) — use it, fork it, make it yours.
