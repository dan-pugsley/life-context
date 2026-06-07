# Macrocycle Onboarding

Playbook for planning a macrocycle (6-12 months). Run this as an AI-mediated conversation to produce a macrocycle README.

## Theoretical basis

- **General Adaptation Syndrome** (Selye, 1956) — training is stress; adaptation occurs during recovery; too much stress without recovery leads to overtraining
- **Fitness-Fatigue Model** (Banister et al., 1975) — training produces both a fitness response and a fatigue response; net performance = fitness minus fatigue; macrocycle manages this balance over months
- **Block Periodization** (Issurin, 2008, 2016) — sequential concentrated phases for advanced athletes; each block develops 1-2 qualities while maintaining others; superior to concurrent everything-at-once for trained individuals
- **Needs Analysis** (NSCA) — systematic comparison of sport demands vs. athlete strengths/weaknesses to identify training priorities

## Prerequisites

Before running this onboarding:
- Root profile.md is populated (life context, schedule, goals)
- health/profile.md is populated (conditions, medications, sleep, recovery)
- health/exercise/profile.md is populated (training history, benchmarks, injuries, preferences)

## Onboarding steps

### 1. Review previous macrocycle

If a previous macrocycle exists:
- Read its README (goals, phase plan)
- Read its review section (what worked, what didn't)
- Read mesocycle reviews within it (patterns, trends)
- Identify: what should continue, what should change, what was learned

If this is the first macrocycle, skip to step 2.

### 2. Current state assessment

Gather from profiles and conversation:

**Training state:**
- Current fitness level (benchmarks, recent performance)
- Training age and history
- Current training status (fully fit / returning from injury / in rehab)
- Recent training volume and intensity (what the body is adapted to)

**Constraints:**
- Active injuries and restrictions (from exercise/status.md)
- Schedule (days/week, session duration, time of day)
- Equipment access
- Recovery capacity (sleep, nutrition, stress, age)
- Life events during the macrocycle period (travel, moves, work changes)

**Readiness indicators:**
- Has the athlete had adequate recovery since the last training block?
- Are there any red flags (chronic fatigue, persistent pain, motivation issues)?

### 3. Goal setting

Define goals using a priority hierarchy:

**Primary goal** (1 only) — the single most important outcome of this macrocycle. Must be specific and measurable where possible. Examples:
- Increase back squat from 125 kg to 140 kg
- Return to full CrossFit class participation pain-free
- Build aerobic base (2k row under 6:45)

**Secondary goals** (2-3) — important but subordinate to the primary goal. These should not conflict with the primary goal. Examples:
- Maintain muscle mass during a cut
- Improve strict HSPU from 1 to 5 unbroken
- Address left shoulder impingement long-term

**Maintenance goals** — qualities to preserve without active development. Examples:
- Keep conditioning at current level
- Maintain gymnastics skills

**Anti-goals** — what we are explicitly NOT trying to do, to prevent scope creep. Examples:
- Not trying to peak for competition
- Not cutting weight
- Not training for a marathon

### 4. Phase sequencing

Select and sequence mesocycle phases based on goals, training state, and periodization principles.

**Common phase types:**

| Phase | Primary quality | Typical duration | Characteristics |
|---|---|---|---|
| Accumulation | Hypertrophy, work capacity | 4-6 weeks | Higher volume (3-5 sets × 8-12 reps), moderate intensity (RPE 6-8), broad exercise selection |
| Intensification | Maximal strength | 4-6 weeks | Moderate volume (3-5 sets × 3-6 reps), higher intensity (RPE 8-9), focused exercise selection |
| Realization | Power, sport-specific | 3-4 weeks | Lower volume, high intensity, competition movements, express built strength |
| Conditioning | Aerobic/anaerobic capacity | 3-5 weeks | Energy system development, mixed modal, CrossFit-style |
| Skill | Gymnastics, Olympic lifting | 3-4 weeks | Technical focus, moderate fatigue, high frequency of skill practice |
| Deload | Recovery | 1 week | 50-60% of normal volume, maintain intensity, active recovery |

**Sequencing principles:**
- Accumulation before Intensification before Realization (general → specific → expressive)
- Build capacity before loading it heavily
- Place deload weeks between major phase transitions (or every 4-6 weeks based on fatigue)
- Consider seasonal factors, life events, and motivation cycles
- Ensure the sequence serves the primary goal — don't include phases "just because"

**For CrossFit athletes specifically:**
- Pure strength phases still include conditioning at maintenance (2-3 sessions/week, reduced intensity)
- Conditioning phases still include strength at maintenance (2-3 heavy lifts/week)
- Gymnastics skill work can thread through most phases at low fatigue cost
- Olympic lifting benefits from its own concentrated phase OR integration during realization

### 5. Benchmark selection

Choose 5-8 measurable benchmarks to test at macrocycle start and end (minimum). These should:
- Align with stated goals
- Cover multiple fitness domains (strength, conditioning, gymnastics)
- Be repeatable under consistent conditions
- Include both primary-goal benchmarks and maintenance checks

Examples: 1RM back squat, 1RM bench press, max unbroken strict HSPU, 2k row time, Fran time, max bar muscle-ups unbroken.

### 6. Risk assessment

Identify factors that could derail the macrocycle:
- Injury recurrence (which movements, what load thresholds)
- Life disruptions (known schedule changes, travel)
- Motivation risks (monotony tolerance, phase length preferences)
- Recovery bottlenecks (sleep issues, nutrition gaps, stress periods)

For each risk, define a mitigation strategy or decision point ("if X happens, we will Y").

### 7. Timeline and milestones

Map out the macrocycle on a rough calendar:
- Start and expected end date
- Phase sequence with approximate durations
- Planned benchmark testing points (start, mid if applicable, end)
- Known life events that affect training
- Decision points (where to assess and potentially adjust the plan)

## Output

The result of this onboarding is a macrocycle README containing:

```markdown
---
created: {date}
updated: {date}
summary: "{duration} macrocycle — {primary goal summary}"
---

# {Macrocycle name}

## Overview
{1-2 sentence summary of the macrocycle's purpose and duration}

## Goals
### Primary
### Secondary
### Maintenance
### Anti-goals

## Phase plan
{Table or list of mesocycles in sequence with approximate durations}

## Benchmarks
{What will be tested, when}

## Timeline
{Calendar mapping of phases to approximate dates}

## Constraints and risks
{Active injuries, restrictions, known schedule disruptions, mitigations}

## Review
{Filled in at macrocycle end — synthesis of mesocycle reviews, goal achievement, lessons learned}
```
