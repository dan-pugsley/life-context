# Life

Structured AI context store for personal life data. See [_template.md](_template.md) for structural conventions.

## Navigation

1. Read root README.md for structure overview
2. Read root profile.md for general user context
3. Navigate to the domain relevant to the user's question
4. Each folder's README.md orients you — read it before exploring further

## Cross-cutting context

Before answering, consider whether sibling domains have relevant context. Check their READMEs to assess relevance.

## Data entry

- Prefer AI-mediated data entry. Ask clarifying questions to ensure quality.
- If a profile.md is empty, offer to run the onboarding.md for that domain.
- Onboarding **must** run top-down: root profile before health, health before exercise, etc. Do not offer to skip or reorder — each level's profile informs the next.
- Reference parent profiles during onboarding to avoid redundant questions.
- Capture all useful information the user provides, even if not explicitly covered by the onboarding playbook. The playbook is a minimum, not a ceiling.
- When the user mentions supporting documents (MRI reports, diagnostic reports, images), proactively offer to import them into the relevant assets/ folder.
- The user may also edit files directly.
- Avoid writing computed values that go stale (e.g., write date of birth, not age). Let the AI calculate derived values at query time.

## Living state vs. stable profile

Volatile facts — current injury restrictions, rehab progression stages, working loads, bodyweight, current training block — live in status.md, the single source of truth. Reference status.md from plans, READMEs, and workouts; never restate its contents. Keep it current as state changes. Stable facts (identity, history, baseline benchmarks, preferences) stay in profile.md.

## Proactive maintenance

As new information arises — from events, issues, or conversation — keep the relevant profile.md, status.md, and README.md files up-to-date, including adding new children sections and updating summaries.

If a profile.md or status.md relevant to the current question appears outdated — either because the `updated` timestamp is old or because there's a disconnect with what the user is saying — flag this and offer to update it.
