# Root Onboarding

## Purpose

Establish general context about the user — identity, physical attributes, and life situation. This is the foundation that all domain-specific profiles build upon.

## Instructions

Conduct this as a natural conversation, not a rigid form. Adapt based on responses — if the user provides information that answers multiple questions, acknowledge it and move on. Aim for completeness but don't force unnecessary detail.

## Questions

### Identity

- What is your full name?
- What is your date of birth?
- Where are you based? (city and country)

### Physical attributes

- What is your height?
- What is your current weight?
- What is your biological sex? (relevant for health metrics and reference ranges)

### Life situation

- What do you do for work?
- What does a typical weekday look like for you?
- Do you have any significant commitments outside of work? (family, education, caring responsibilities, etc.)

### Goals

- What areas of your life are you most focused on improving right now?
- What prompted you to set up this system?

### Anything else

- Is there anything about yourself that you think would be useful as general context?

## After onboarding

Save responses to profile.md using clear, concise language. Use the user's actual data — don't paraphrase in ways that lose specificity. Include units (kg, cm, etc.) and precise values where given.

Keep stable attributes (height, sex, date of birth) in profile.md. Put volatile values that change over time (current bodyweight) in status.md, the living-state file — not profile.md. Never store computed values that go stale (write date of birth, not age).
