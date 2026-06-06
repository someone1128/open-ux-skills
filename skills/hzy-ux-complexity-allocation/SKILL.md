---
description: Allocate complexity to the right user, moment, and surface. Use when a UI exposes too many technical fields, hides expert controls, or mixes beginner, advanced, and system concerns.
---

## Scope

Product-agnostic UX skill. Default to English. Use Chinese when requested.

Do not hide complexity blindly. Classify it.

## Role

You redesign complexity distribution. The goal is not to remove power, but to place complexity where it helps instead of where it overwhelms.

## When to use

Use this skill when:

- a user-facing UI exposes API fields directly
- too many technical settings appear before the user can start
- beginner and expert users are forced into the same interface
- advanced controls are either too visible or too hidden
- system, developer, or provider fields appear in normal user flows
- labels reflect backend terminology instead of user intent
- users need smart defaults but experts still need control

## When not to use

Do not use this skill to remove all advanced controls.

Do not use it when the target users are explicitly developers or experts who expect raw configuration.

Do not use it when the issue is mainly navigation, mobile responsiveness, copy clarity, or accessibility. Use the relevant skill instead.

## Complexity classes

- Primary user intent: visible by default.
- Common preferences: visible or lightly grouped.
- Advanced controls: available but collapsed or secondary.
- Professional workflow controls: accessible for expert users.
- Developer/system-only fields: not shown in normal user UI.
- Unnecessary complexity: remove.

## Review checklist

- Are raw API fields exposed directly?
- Are beginners and experts forced into the same interface?
- Are system fields shown to normal users?
- Are advanced controls hidden so deeply that experts cannot find them?
- Are defaults smart enough to let users start?
- Are labels written in user language rather than backend terms?

## Output

1. Current complexity problem.
2. User's real goal.
3. Field classification table.
4. Better interaction structure.
5. Labels and helper text.
6. Default values.
7. Progressive disclosure rules.
8. Edge states.
9. What expert controls must remain accessible.
10. Implementation notes.
