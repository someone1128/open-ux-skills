# Test Case: Should Prototype a New Interaction Model

## Input

Review a mature but flat result page. Users can view generated outputs, but there is no comparison, no iteration, no continuation action, and no way to reuse previous outputs.

## Expected skill behavior

Use:

```txt
/hzy-ux-maturity-router
/hzy-ux-interaction-model-explorer
/hzy-ux-pattern-case-library
```

The agent should not automatically redesign the entire page. It should recommend prototyping a continuation-oriented model.

## Expected output

- Decision: Prototype or Targeted optimization
- Identify the missed continuation opportunity
- Suggest result action bar, comparison view, version branching, or history-as-continuation pattern
- Preserve familiar viewing and basic actions
- Define validation metrics

## Anti-pattern

The agent should not replace the whole product structure without evidence.
