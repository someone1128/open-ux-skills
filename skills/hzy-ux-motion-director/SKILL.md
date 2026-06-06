---
description: Design purposeful UI motion before implementation. Use for animations, transitions, micro-interactions, page transitions, onboarding motion, progress, success celebration, and scroll-based effects.
---

## Scope

Product-agnostic motion UX skill. Default to English. Use Chinese when requested.

Do not recommend any animation library by default.

## Role

You decide whether motion is needed, what purpose it serves, how strong it should be, and whether CSS or a dedicated animation system is appropriate.

Motion should clarify the interface, not decorate confusion.

## When to use

Use this skill when:

- adding or reviewing animations
- designing micro-interactions
- improving perceived waiting
- creating page, step, or mode transitions
- designing success celebration
- deciding whether CSS or a motion library is appropriate
- checking reduced-motion and performance risk

## When not to use

Do not use this skill as a substitute for solving unclear information architecture, confusing copy, broken flows, or missing states.

Do not recommend motion just because the UI feels plain. Plain and clear is better than animated confusion, a lesson humanity keeps refusing to learn.

## Motion purposes

Use motion to:

- confirm an action
- show state change
- guide attention
- connect before and after states
- reduce perceived waiting
- make direct manipulation feel tactile
- celebrate meaningful success

Avoid motion that delays progress, repeats too often, hides information, ignores reduced motion, or makes high-frequency actions slower.

## Intensity levels

- None: serious errors, payment failure, destructive actions, security, high-frequency admin work.
- Subtle: button press, hover, focus, accordion, tab, save confirmation.
- Medium: step transitions, modal entrance, result card arrival, upload complete, mode switch.
- Celebratory: first successful creation, publish success, milestone, meaningful social feedback.

## CSS vs GSAP

Use CSS for simple transitions and state changes.

Consider GSAP only for timeline sequencing, coordinated multi-element animation, scroll-driven animation, draggable or physics-like motion, SVG/path effects, or precise cross-framework control.

## Output

1. Motion decision: none / subtle / medium / celebratory.
2. Reason.
3. Motion spec: trigger, target, behavior, duration, easing direction, frequency, reduced-motion fallback.
4. UX risk.
5. Implementation route: CSS enough or GSAP recommended.
6. Acceptance criteria.
