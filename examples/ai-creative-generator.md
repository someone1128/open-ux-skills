# Example: AI Creative Generator Review

This generic example shows how the skills can be applied to an AI creative generation feature.

## Situation

A product lets users generate an output from a prompt and several settings.

The current UI exposes:

- prompt
- model
- seed
- negative prompt
- reference strength
- output format
- webhook
- callback URL

## Recommended skill flow

```txt
/ux-maturity-router
/complexity-allocation-ux
/interaction-state-design
/interaction-model-explorer
/ux-change-proposal
```

## Likely recommendation

- keep prompt visible
- expose common preferences
- collapse advanced settings
- move developer/system fields out of normal UI
- show progress during generation
- show next actions after success
- explain quota/cost before irreversible actions
