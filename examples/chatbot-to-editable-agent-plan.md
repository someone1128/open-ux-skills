# Example: Chatbot to Editable Agent Plan

## Situation

A product includes an AI assistant. The assistant accepts a message, calls a tool, and returns a result.

The assistant behaves like a chat-styled button instead of a workflow partner.

## Recommended skills

```txt
/hzy-ux-ai-assisted-workflow-review
/hzy-ux-interaction-model-explorer
/hzy-ux-pattern-case-library
/hzy-ux-change-proposal
```

## Current flow

1. User types a request.
2. Assistant says it will do the task.
3. Assistant runs a tool.
4. Assistant returns a result.
5. User must figure out what to do next.

## Better flow

1. User types a request.
2. Assistant identifies intent and missing details.
3. Assistant shows a short editable plan.
4. User confirms or adjusts the plan.
5. Assistant runs the workflow with visible progress.
6. Assistant returns the result with critique, assumptions, and next actions.
7. User can refine, branch, save, export, or continue.

## Pattern references

- Chatbot wrapper
- AI result iteration
- Long-running task uncertainty
- Weak success state

## Validation metrics

- plan confirmation rate
- plan edit rate
- task completion rate
- refinement rate
- user satisfaction feedback
- reduction in failed or vague requests
