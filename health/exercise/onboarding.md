# Exercise Onboarding

## Purpose

Build a comprehensive training profile — history, current routine, goals, injuries, preferences, and recovery capacity. This enables AI-generated programming that rivals an expert personal trainer's output.

Informed by personal trainer intake frameworks from NASM, ISSA, and AFPA.

## Prerequisites

Root and health profiles must be completed first. Reference them for physical attributes, conditions, medications, and lifestyle factors already recorded. Do not re-ask for information already captured.

## Instructions

This is the most detailed onboarding in the system. An expert personal trainer's initial consultation typically covers 30-60 minutes of conversation. Conduct this naturally — listen more than you talk. Probe deeper when the user mentions injuries, limitations, or strong preferences, as these details directly impact programming quality.

The injury section is particularly important. For each injury, gather enough detail to create an event file in issues/. Don't rush through it.

## Questions

### Training history

- What physical activities or sports do you do, and for how many years each?
- How did you get into each of them?
- Have you worked with a personal trainer or coach before? What did you like or dislike about that experience?

### Current routine

- Describe your current training schedule — what activities, how often, how long per session?
- Where do you train? What equipment or facilities do you have access to?
- Do you follow a structured programme, or train intuitively / follow a class?

### Fitness level

- How would you rate your current fitness? (beginner / intermediate / advanced / elite)
- Are there specific benchmarks you can share? (e.g., max lifts, run times, WOD scores, competition results)
- What movements or activities do you feel strongest at?
- What are your biggest weaknesses or areas you struggle with?

### Goals

- What are your primary training goals? (e.g., strength, endurance, body composition, sport-specific performance, rehab, general fitness, longevity)
- What timeline do you have in mind for these goals?
- Do you have competitive aspirations or specific events you're training for?

### Injury and issue history

This is critical for safe, effective programming. For each current injury or ongoing physical issue:

- What is the injury or condition?
- When did it start or first appear?
- Have you had it diagnosed? By whom, and what was the diagnosis?
- Do you have any imaging or reports? (MRI, X-ray, ultrasound)
- What is the current status? (acute / recovering / chronic-managed / resolved)
- What management or rehab do you currently do for it?
- What movements aggravate it?
- What movements are safe or even helpful?
- Has a professional advised you to avoid anything specific?

Also ask:

- Do you have any past injuries that are fully resolved but worth noting?
- Any surgeries related to physical activity?

### Recovery

- How well do you typically recover between sessions?
- Do you use any recovery strategies? (stretching, foam rolling, cold/heat, massage, etc.)
- Reference sleep and stress from the health profile — ask how these affect training.

### Preferences

- What types of training do you enjoy most?
- What do you dislike or dread?
- Do you prefer training alone, with a partner, or in a group/class?
- What are you looking for from AI-guided programming? (strict plans, flexible guidance, education, accountability)

### Movement and mobility

- Are there any movements you've been told to avoid?
- Do you have any notable mobility restrictions? (e.g., limited overhead range, tight hips, ankle mobility)
- Do you warm up or cool down? What does that typically include?

## After onboarding

Save to profile.md structured under these headings:

- **Activities** — list with years of experience
- **Current routine** — schedule summary
- **Fitness level** — self-assessment with specific benchmarks where available
- **Goals** — prioritised list with timeframes
- **Issues summary** — brief summary of each injury/condition with current status and key restrictions (detail goes in issues/ folder)
- **Recovery** — strategies used and general recovery capacity
- **Preferences** — training likes, dislikes, style, and what they want from AI programming
- **Mobility** — restrictions, warm-up/cool-down habits

Record current, changing state — active restrictions, rehab progression stages, and working loads — in status.md (the living-state file), not profile.md. Profile holds stable history and baselines; status.md is the single source of truth for what changes week to week.

For each injury or ongoing issue, create:
1. A named subfolder under issues/ (e.g., issues/back/, issues/knees/)
2. An initial event file with full details from the conversation
3. Additional event files for any imaging, reports, or professional consultations mentioned

Cross-reference the issue summaries in the profile with the detailed records in issues/.
