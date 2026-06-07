# Microcycle Onboarding

Playbook for planning a microcycle (1 week of training). Run this as an AI-mediated conversation to produce a week README and individual workout files.

## Theoretical basis

- **Session Sequencing and Interference Effect** (Hickson, 1980; Wilson et al., 2012) — concurrent strength and endurance training can interfere if poorly sequenced. Separate high-intensity strength from high-intensity conditioning by 6-24 hours. Place strength before conditioning within a session when both occur.
- **RAMP Warm-up Protocol** (Jeffreys, 2007) — Raise (heart rate, temperature), Activate (key muscle groups), Mobilise (working joints through range), Potentiate (progressive loading toward working sets). Replaces generic "10 min cardio" with targeted preparation.
- **Exercise Order** (NSCA) — compound before isolation, high-skill before low-skill, high-intensity before low-intensity. Exceptions: pre-exhaustion techniques, or deliberate fatigue-state skill practice.
- **Supercompensation Timing** — optimal stimulus spacing depends on intensity and muscle group. Heavy compounds need 48-72h recovery for the same pattern; lighter/smaller muscle work can be repeated sooner.
- **Daily Readiness / Autoregulation** (Tuchscherer, 2008) — adjust within-session load based on warm-up set feel. If prescribed RPE 8 and warm-ups feel heavy, the working weight adjusts down; if they fly up, adjust up. The program prescribes intent (RPE), the athlete discovers the load.

## Prerequisites

Before running this onboarding:
- The parent mesocycle README exists (split, volume/intensity plan, exercise pool)
- Previous week's feedback is reviewed (if applicable)
- Any life circumstances for the coming week are known (travel, poor sleep, extra stress)

## Onboarding steps

### 1. Context review

Gather:
- Which week of the mesocycle is this? (e.g., "Week 3 of 4 before deload")
- What does the mesocycle's progression plan prescribe for this week? (volume, RPE targets)
- If week 2+: what did last week's feedback reveal? (loads that need adjusting, movements that caused pain, energy patterns)
- Any life factors? (bad sleep, travel, high work stress, illness)

**Adjustment rules based on feedback:**
- If previous week's average RPE was >9: reduce volume 10-15% this week or hold load constant (don't progress)
- If pain was reported on a movement: substitute or reduce load, note for mesocycle review
- If energy was consistently low: check sleep/nutrition, consider a lighter day or extra rest
- If loads felt easy (RPE consistently below target): progress load faster than planned

### 2. Daily session planning

For each training day, build the session following this structure:

**A. Warm-up (10-15 min)**

Follow RAMP protocol tailored to the day's primary work:
1. **Raise** (3-5 min): Light cardio relevant to the session (row for pull days, bike for leg days, skip rope for general). Elevate heart rate and body temperature.
2. **Activate** (3-5 min): Band work or light exercises targeting muscles that will be loaded. Include any injury-specific prehab (e.g., shoulder band routine before pressing days).
3. **Mobilise** (2-3 min): Dynamic stretches for joints involved in the primary lift. Focus on any known restrictions.
4. **Potentiate** (2-4 min): Empty bar or light ramp-up sets of the primary lift. Progressive loading toward first working set.

**B. Primary lift(s) (15-25 min)**

The main strength work for the session:
- 1-2 compound lifts as prescribed by the mesocycle
- Sets × reps at target RPE for this week
- Full rest between sets (2-4 min for strength, 60-90s for hypertrophy)
- Log weight used and actual RPE

**C. Accessories (15-25 min)**

Supporting work:
- 2-4 exercises targeting weaknesses or volume goals
- Shorter rest (60-120s)
- Higher rep ranges than primary work
- Can superset non-competing movements for time efficiency

**D. Conditioning (0-20 min, where prescribed)**

Based on mesocycle's conditioning plan:
- Format: intervals, AMRAP, EMOM, time trial, or steady-state
- Intensity: as prescribed (easy/moderate/hard)
- Placed AFTER strength work (interference effect — don't fatigue before heavy lifting)
- On dedicated conditioning days, can be the session centrepiece

**E. Cool-down (5 min)**

- Light movement or stretching
- Foam rolling for managed injuries (quad rolling for knee)
- Breathing/recovery

### 3. Load prescription

For each primary lift and key accessory:
- Reference last week's loads (or mesocycle starting loads if week 1)
- Apply progression model from mesocycle plan
- Prescribe as: "{weight} or weight that hits RPE {target} for {reps}"
- First working set is exploratory: if it feels too heavy/light, adjust

**Week 1 loads (no prior data):**
- Estimate conservatively from known benchmarks
- E.g., if 1RM back squat is 125 kg and the target is 4×5 @ RPE 7-8, start around 95-100 kg
- Better to start light and build than to overshoot and need to drop

**Subsequent weeks:**
- Previous week's actual loads + progression (if RPE was at or below target)
- If RPE was above target, hold or reduce
- The athlete discovers the right weight through warm-up sets — prescriptions are guidelines, not mandates

### 4. Workout file structure

Each workout file follows this template:

```markdown
---
created: {date}
summary: "{day}: {primary lift focus} + {secondary elements}"
---

# D{N} — {Title}

## Warm-up
{RAMP protocol tailored to today's work}

## Primary
{Main lift(s): exercise, sets × reps @ RPE target}
{Rest periods noted}

## Accessories
{Supporting exercises: sets × reps @ RPE target}

## Conditioning
{Format, duration, effort level — if prescribed today}

## Cool-down
{Recovery work, mobility, rehab}

---

## Feedback

**Completed:** yes / partial / no
**RPE (overall):** /10
**Energy:** low / moderate / high
**Pain/discomfort:** none / {location + severity}
**Sleep (previous night):** poor / fair / good / great
**Notes:**
{Freeform: what felt good, what was too easy/hard, what to adjust, any observations}
```

### 5. Week README structure

The week README provides an overview and captures week-level notes:

```markdown
---
created: {date}
summary: "Week {N} of {mesocycle name} — {volume/intensity characterisation}"
---

# Week {N}

## Overview
{Where this week sits in the mesocycle progression. Key targets.}

## Schedule
| Day | Focus | Primary lift |
|---|---|---|
| D1 | ... | ... |
| D2 | ... | ... |
| D3 | ... | ... |
| D4 | ... | ... |
| D5 | ... | ... |

## Adjustments from plan
{Any modifications made based on previous week's feedback or life circumstances}

## Notes
{Anything relevant: life context, energy state going in, goals for the week}
```

### 6. Deload week specifics

If this is the deload week:
- Volume: 50-60% of peak week (halve sets, keep 1-2 working sets per exercise)
- Intensity: maintain weight from week 3-4 OR reduce 10%
- No conditioning tests, no AMRAPs
- Include: mobility work, skill practice (light), rehab exercises
- Session duration: shorter (30-45 min vs. 60-75 min)
- Purpose: feel recovered and eager to train hard again by the end

## Session duration targets

For a typical training week:
- Full training sessions: 60-75 minutes (including warm-up and cool-down)
- Deload sessions: 30-45 minutes
- If your schedule allows no strict time cap, still respect recovery by not extending sessions unnecessarily

## Notes on running this playbook

- When planning week 1 of a new mesocycle, loads are estimated from benchmarks and will be refined after the first week of feedback
- When planning weeks 2+, always review the previous week's workout feedback first
- The athlete may request mid-week adjustments ("today I feel terrible, can we make it lighter?") — autoregulation accommodates this
- Weekend rest days: only prescribe light core/rehab or walks, nothing programmed unless requested
