# Programming

AI-managed training programming for long-term strength and fitness development.

## Philosophy

Block periodization (Issurin, 2008) with daily undulating elements within blocks. Each mesocycle emphasises 1-2 primary training qualities while maintaining others at a reduced dose. Autoregulated via RPE/RIR rather than fixed percentages.

Core principles:
- **Progressive overload** — the non-negotiable driver of adaptation
- **Specificity** — train movements and energy systems relevant to your sport or training goals
- **Variation** — strategic, not random; prevents accommodation and boredom
- **Individualisation** — informed by accumulated feedback, injury history, and preferences
- **Fatigue management** — respect recovery capacity; deload proactively

## Cycle hierarchy

| Level | Duration | Contains | Purpose |
|---|---|---|---|
| Macrocycle | 6-12 months | Mesocycles | Long-term direction, phase sequencing, benchmark targets |
| Mesocycle | 3-6 weeks | Microcycles (weeks) | Concentrated development of primary quality |
| Microcycle | 1 week (5 sessions) | Workouts | Day-to-day training structure |
| Workout | Single session | Movements | Execution unit |

## Folder conventions

```
programming/
  README.md                          # This file
  onboarding/
    macrocycle.md                     # Planning playbook
    mesocycle.md                      # Planning playbook
    microcycle.md                     # Planning playbook
  {YYYY-MM}_{name}/                  # Macrocycle (date-prefixed)
    README.md                        # Plan, goals, timeline, review
    {NN}_{name}/                     # Mesocycle (numbered)
      README.md                      # Focus, targets, exercise selection, review
      w{N}/                          # Microcycle / week
        README.md                    # Week overview, adjustments
        d{N}-{description}.md        # Workout
```

Naming: lowercase, hyphens. Macrocycles date-prefixed (YYYY-MM). Mesocycles zero-padded numbered. Weeks as `w1`, `w2`, etc. Workouts as `d1`, `d2`, etc.

**Workout files are unique per-week instances**, regenerated each microcycle from the plan — not reusable templates shared across weeks. A completed workout file is therefore the dated record of that one session: the prescription is what was planned, the `## Feedback` block is what actually happened. (This is why feedback lives co-located in each file rather than in a separate log.)

## Feedback system

After each session the athlete narrates how it went and the AI records it in a `## Feedback` block at the bottom of that workout file — capturing completion, session RPE, per-lift performance (load × reps × RIR), readiness (sleep/energy/soreness/stress), pain, and notes. The interview to run, what each item is for, and where durable changes go (working loads → status.md, rehab → status.md/issues) are defined in the [feedback playbook](feedback-playbook.md), grounded in established methods: session-RPE, RIR autoregulation, wellness monitoring, and the rehab pain-monitoring model.

A completed workout's prescription is left as written; the `## Feedback` block records what was actually done. Corrected loads flow forward via status.md (primaries) and the next week's workout (accessories).

At the end of each mesocycle, workout feedback is synthesised into a `## Review` section in the mesocycle README; same at macrocycle level. This accumulated feedback is the primary input for personalising subsequent cycles.

## Autoregulation

Load prescription uses RPE (Rate of Perceived Exertion) / RIR (Reps in Reserve):

| RPE | RIR | Meaning |
|---|---|---|
| 10 | 0 | Maximum effort, no reps left |
| 9 | 1 | Could do 1 more rep |
| 8 | 2 | Could do 2 more reps |
| 7 | 3 | Could do 3 more reps |
| 6 | 4+ | Warm-up / light work |

Target RPE is prescribed per exercise. Actual RPE is logged in feedback. This allows progressive overload without rigid percentages, accommodating daily readiness variation.

## Writing workouts

- **Be specific with movements.** Never write vague descriptions like "light chest stretch" or "shoulder mobility." Always name the exact exercise (e.g., "doorway chest stretch, 30s each side"). The athlete may not know which movements target which areas. For stretches, include the target area and body position.
- **Be specific with loads.** Always suggest a starting weight, even if approximate. "Adjust on feel" is fine as a qualifier but not as the only instruction.
- **Explain unfamiliar exercises inline** the first time they appear in a block, or use widely-understood names. If an exercise has a colloquial name (e.g., "skull crushers"), also include the descriptive name (e.g., "lying DB tricep extensions").
- **Maximise structure.** Every movement needs a specific format (sets x reps, EMOM, time cap, etc.), rest periods, and execution cues. Never write "5 min practice" or "work up to a heavy set" — give a concrete protocol (e.g., "EMOM 5 min: max distance walk"). The athlete should be able to read and execute without making decisions mid-session. Structure is a guideline they can deviate from, but it must always be there.

## How to use

1. Read the relevant onboarding playbook before planning a new cycle
2. Run the onboarding conversation to produce the cycle's README
3. Execute the cycle, recording feedback per workout
4. At cycle end, write the review section
5. Use accumulated feedback to inform the next cycle
