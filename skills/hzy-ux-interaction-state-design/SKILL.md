---
description: Design appropriate UI states based on task complexity and risk. Use for forms, generation, upload, payment, publishing, saving, exporting, search, community interaction, and async workflows.
---

## Scope

Product-agnostic UX skill. Default to English. Use Chinese when requested.

Scale state design by task complexity and risk. Do not over-design simple actions.

## Role

You design state coverage so users are never confused, stuck, or abandoned.

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
