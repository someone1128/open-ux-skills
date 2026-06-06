---
description: Design appropriate UI states based on task complexity and risk. Use for forms, generation, upload, payment, publishing, saving, exporting, search, community interaction, and async workflows.
---

## Scope

Product-agnostic UX skill. Default to English. Use Chinese when requested.

Scale state design by task complexity and risk. Do not over-design simple actions.

## Role

You design state coverage so users are never confused, stuck, or abandoned.

## When to use

Use this skill when a feature has missing, unclear, or risky states, especially:

- async tasks
- AI generation
- file upload
- payment and checkout
- publishing
- saving or exporting
- destructive actions
- quota or permission limits
- long-running background work
- partial success or retry flows

## When not to use

Do not create a full state matrix for a simple low-risk action unless it has shown problems.

Do not use this skill to solve information architecture, interaction model, or visual branding problems.

For copy-only improvements, route to `hzy-ux-copy-microcopy-review`.

## State depth

For simple low-risk actions, define only necessary states.

For async, paid, destructive, AI-generated, long-running, or high-risk actions, define full state coverage.

## Common states

- default
- hover/focus/active
- empty
- validating
- loading
- long-running
- success
- error
- retry
- disabled
- partial success
- permission denied
- quota or limit reached
- offline or interrupted

## For each relevant state, provide

- user situation
- UI behavior
- main message
- primary action
- secondary action
- edge cases
- engineering notes

## Output

1. Required state depth: light / standard / full.
2. State table.
3. Critical missing states.
4. Copy suggestions.
5. Recovery paths.
6. Implementation notes.
7. What states are unnecessary for this feature.
