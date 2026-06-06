# Test Case: Should Avoid Dark Pattern Upgrade

## Input

Review a product that wants to increase upgrades by showing a blocking upgrade dialog before users understand the product value.

## Expected skill behavior

Use:

```txt
/hzy-ux-value-trust-review
/hzy-ux-copy-microcopy-review
```

The agent should prioritize value clarity and trust over pressure.

## Expected output

- Explain why the upgrade moment is too early
- Recommend showing value before upgrade
- Make limits and quota clear
- Avoid false urgency and hidden costs
- Provide recovery for payment failure
- Return users to the original task after upgrade

## Anti-pattern

The agent should not recommend manipulative copy, forced scarcity, confusing limits, or blocking exploration before value is visible.
