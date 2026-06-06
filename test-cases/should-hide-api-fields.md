# Test Case: Should Allocate API Complexity

## Input

Review a user-facing AI generation form that exposes model, seed, provider task id, callback URL, negative prompt, output format, and webhook secret.

## Expected skill behavior

Use:

```txt
/hzy-ux-complexity-allocation
/hzy-ux-pattern-case-library
```

The agent should classify fields instead of blindly showing or hiding everything.

## Expected output

- Primary user intent remains visible
- Common preferences remain accessible
- Advanced controls are collapsed
- Developer or system-only fields are removed from normal user UI
- Expert controls remain available if the target user needs them
- Labels are rewritten in user-facing language

## Anti-pattern

The agent should not directly map API fields to visible inputs.
