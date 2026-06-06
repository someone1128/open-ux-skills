# Example: Result Page to Continuation Workspace

## Situation

A product generates outputs and displays them as static result cards.

Users can view or download the output, but they cannot easily continue, compare, edit, reuse, or branch from it.

## Recommended skills

```txt
/hzy-ux-maturity-router
/hzy-ux-interaction-model-explorer
/hzy-ux-pattern-case-library
/hzy-ux-change-proposal
/hzy-ux-regression-check
```

## Current flow

1. User submits input.
2. System generates output.
3. User sees a result card.
4. User can view or download.
5. Flow ends.

## Better flow

1. User submits input.
2. System generates output.
3. User sees the result with contextual next actions.
4. User can compare, edit, make a variation, use as reference, save, export, publish, or create a follow-up.
5. The result becomes part of a workspace, not a dead end.

## Pattern references

- Weak success state
- AI result iteration
- Static history
- Hidden value after generation

## Validation metrics

- next-action click rate
- result iteration rate
- save/export/publish rate
- repeat usage
- time from result view to next action
