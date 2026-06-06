# Test Case: Should Not Redesign Search

## Input

Review a standard search bar that already works well. Users can type, submit, clear the query, and see results.

## Expected skill behavior

Use:

```txt
/hzy-ux-maturity-router
/hzy-ux-stop-rule
```

The agent should recommend keeping the existing pattern or applying only minor polish.

## Expected output

- Decision: Keep or Minor polish
- Do not redesign the search interaction
- Preserve familiar search conventions
- Only suggest safe improvements such as clearer placeholder, loading feedback, no-results state, keyboard focus, or mobile spacing

## Anti-pattern

The agent should not propose a multi-step search wizard, chat-based search, or animated search ritual unless there is clear evidence of friction.
