---
created: 2026-06-01
updated: 2026-06-03
summary: "The interview to run when recording post-workout feedback — what to ask, why, and where it lands; grounded in session-RPE, RIR autoregulation, wellness, and the pain-monitoring model"
---

# Workout feedback playbook

Run this whenever the athlete says something like _"let's record my feedback for D3."_ They narrate how the session went; the AI extracts the dimensions below, writes the `## Feedback` block at the bottom of that workout file, and propagates any durable change (working loads → [status.md](../status.md), rehab → [status.md](../status.md) / [issues/](../issues/)). The point is a **consistent, decision-useful** record, so that week to week — and at the mesocycle/macrocycle `## Review` — there's real data behind every load change, not vibes.

## How to run it

1. **Open with the previous session's morning-after read.** Ask how they pulled up the morning after the last session — any soreness or pain, and whether it had settled to baseline. Use the answer to (a) **backfill that session's deferred `Next-morning read`** in its feedback block and (b) inform today's `Readiness`. One question, two records. Skip if it was already logged (e.g. they volunteered it earlier, or reported it before the session).
2. Let the athlete narrate the current session freely.
3. Fill only the _gaps_ with targeted questions from the checklist — don't re-ask what they already volunteered.
4. Keep it short: six dimensions, a handful of questions. This is a signal-gathering tool for load and rehab decisions, not a survey to grind through.
5. Write the block, update [status.md](../status.md) / [issues/](../issues/) where warranted, and tell the athlete what changed.

**Stay session-focused.** This is the only routine touchpoint — there is no mandatory daily wellness log. If the athlete _volunteers_ a morning wellness/pain reading at some other time (including rest days), capture it the same way: backfill the relevant session's deferred read, or just note it. Don't prompt for it off-session; it's opportunistic, not a daily survey. (Revisit if a rehab phase ever needs tighter day-by-day monitoring.)

## What to capture, and why

| Dimension                | Ask                                                                                                                                    | Why it matters                                                                                      | Lands in                                                              |
| ------------------------ | -------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------- |
| **Completion & mods**    | Did you get through it? Anything subbed, skipped, or limited by equipment/time?                                                        | Context for everything else; repeated subs flag a program-fit problem                               | Feedback block                                                        |
| **Session RPE**          | Overall, how hard was the whole session, 1–10?                                                                                         | Single validated internal-load marker; trend it across the week/block to catch accumulating fatigue | Feedback block (watch the trend for deloads)                          |
| **Per-lift performance** | For each main lift — what load, did you get the reps, how many left in the tank (RIR)?                                                 | The autoregulation signal that drives double progression: add reps/load when RIR beats target       | Feedback block; primaries → status.md, accessories carry to next week |
| **Readiness**            | How were sleep, energy, soreness, and life stress (work/life — not training)?                                                          | Separates "load too high" from "rough day"; declining wellness precedes overreaching                | Feedback block                                                        |
| **Pain / discomfort**    | Any pain? Where, how bad /10, which movement? (The _next-morning_ part is deferred — captured at the next session's open, per step 1.) | The safety gate; for managed injuries (e.g. back, shoulder, knee) it can override progression                     | Feedback block (`Next-morning read` deferred); rehab stage + issues/  |
| **Notes**                | Anything else — technique, how it felt, what you'd change?                                                                             | Catches what the fields miss                                                                        | Feedback block                                                        |

### Reading the signals

- **RIR vs target.** Prescriptions carry a target RPE (e.g. 6–7 = 3–4 RIR). If actual RIR is consistently _above_ target, progress it (double progression: add reps to the top of the range, then add load). If _below_ target — training hotter than prescribed — hold or ease, especially on on-ramp/accumulation weeks where leaving a rep in reserve is the plan. RPE↔RIR table is in the [programming README](README.md#autoregulation).
- **Pain — the acceptable-pain rule.** Discomfort that stays low (≈ ≤3–4/10) during and just after, and is back to baseline by the next morning, is acceptable to train through. Pain that climbs during the set, lingers into the next day, or is sharp/flashing → modify or regress the movement and open/append an [issues/](../issues/) note. This gate outranks load progression.
- **Readiness explains performance.** A flat session on poor sleep or high life stress isn't a reason to drop a load; a flat session on good readiness is. A "none / good" reading is still useful — it confirms readiness wasn't the limiter.

## Routing rules

- **Working loads.** Primary lifts → update the table in [status.md](../status.md). Accessories → record the established load in the feedback block; it carries into next week's workout (no need to bloat status.md with every isolation move).
- **Don't rewrite a completed workout's prescription.** The plan stays as written; the `## Feedback` block is the as-performed record, and the gap between the two is itself useful data. Corrected numbers flow forward via status.md (primaries) and the next microcycle (accessories). _Exception: improving an unclear or unsafe instruction/cue — that's reusable reference text, so fix it in place and wherever it recurs._
- **Deferred next-morning read.** Backfilling the prior session's `Next-morning read` is _completing_ its feedback record, not rewriting the prescription — so it's allowed and expected. If that read breaks the acceptable-pain rule, also route it to [issues/](../issues/) and adjust the rehab stage in [status.md](../status.md).
- **Rehab.** Advance or hold a stage in the [status.md](../status.md) rehab table per the physio criteria; pain that breaks the acceptable-pain rule → [issues/](../issues/).
- **Review feed.** These blocks are the raw input for the mesocycle/macrocycle `## Review` synthesis.

## The `## Feedback` block format

Every workout ends with this (a workout may append one or two specific fields — e.g. D4 _strict-press position_, D5 _AMRAP result_):

```
## Feedback

**Date:**
**Completed:** yes / partial / no — note subs, skips, equipment/time limits
**Session RPE:** /10
**Performance (key lifts):** load × reps × RIR per main movement
**Readiness:** sleep · energy · soreness · life stress
**Pain/discomfort:** none / location · severity (/10) · which movement (during & just after)
**Next-morning read:** *pending* — filled at the next session's open: did soreness/pain settle to baseline by morning? (The rehab gate; stays "pending" until then.)
**Notes:**
**Actions:** what was updated (status.md loads, rehab stage, next-week tweaks)
```

## Evidence basis

These dimensions mirror what the load-monitoring literature and applied S&C practice actually use:

- **Session RPE (sRPE)** — a single 0–10 rating of overall session effort, taken after the session, is a validated, low-cost marker of internal training load. ([Haddad et al., 2017](https://pmc.ncbi.nlm.nih.gov/articles/PMC5673663/))
- **RIR-based RPE / autoregulation** — rating effort as reps-in-reserve (RPE = 10 − RIR) lets load be regulated to daily readiness rather than fixed percentages. ([Zourdos et al., 2016](https://pubmed.ncbi.nlm.nih.gov/26049792/); [applied](https://journals.lww.com/nsca-scj/fulltext/2016/08000/application_of_the_repetitions_in_reserve_based.10.aspx))
- **Subjective wellness / readiness** — brief daily ratings of sleep, fatigue, soreness, and stress (the Hooper index) track training load and flag fatigue cheaply; psychological/life stress impairs recovery independently of training. ([Clemente et al., 2019](https://pmc.ncbi.nlm.nih.gov/articles/PMC6390199/))
- **Pain-monitoring model** — during loaded rehab, pain up to ~5/10 that settles to baseline by the next morning is acceptable; persistent or rising pain means back off. ([Silbernagel et al., 2007](https://journals.sagepub.com/doi/abs/10.1177/0363546506298279))
