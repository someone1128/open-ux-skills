---
description: A reusable UX pattern and case library. Use for inspiration, not prescription, when improving interaction design across products.
---

## Scope

Product-agnostic UX skill. Default to English. Use Chinese when requested.

Do not assume a specific product, brand, industry, business model, interface type, or implementation framework.

## Role

You match UX problems to reusable interaction patterns without mechanically applying them.

Your job is to expand the solution space, not force the current interface into a familiar template.

## Anti-bias rule

Patterns are references, not prescriptions.

Before applying a pattern, verify:

- user goal
- task frequency
- user expertise
- task risk
- business impact
- implementation cost
- existing user habits
- whether the pattern reduces or increases friction

If the current pattern is already clear, familiar, and efficient, recommend keeping it or applying only minor polish.

---

# Pattern Cases

## Case 1: API fields exposed directly

### Problem

The UI mirrors backend or API fields instead of the user's task.

Common symptoms:

- model, seed, provider task id, callback URL, webhook secret, internal enum values
- too many fields visible by default
- labels match implementation names rather than user language

### Better pattern

Use an intent-first interface.

Visible by default:

- primary user goal
- main input
- common preferences
- smart defaults
- primary action

Secondary:

- customize details
- advanced settings

Hidden from normal users:

- developer/system fields
- provider routing
- internal task ids
- webhook or callback configuration

### Use when

- users are not technical specialists
- the task is creative, consumer-facing, or workflow-oriented
- the interface exposes implementation details too early

### Do not use when

- the product is explicitly a developer tool
- expert users expect raw controls
- the fields are few, familiar, and important

### Component ideas

- PrimaryIntentInput
- CommonPreferences
- AdvancedSettingsAccordion
- DeveloperDebugPanel
- SmartDefaults

---

## Case 2: Blank start anxiety

### Problem

The user sees an empty input area and does not know what to write, choose, upload, or create.

### Better pattern

Offer starter examples, templates, chips, recent items, or remixable examples.

Examples:

- AI image: subject chips, style cards, aspect ratio presets
- AI video: scene starters, camera motion presets, duration presets
- AI writing: genre, tone, audience, outline templates
- SaaS dashboard: report templates, saved views, sample query

### Use when

- the task starts from an open-ended input
- users are new or unsure
- examples can become direct starting points

### Do not use when

- the action is simple and obvious
- examples distract expert users from fast input

### Component ideas

- ExampleChips
- TemplateGallery
- StarterCards
- RecentItems
- GuidedEmptyState

---

## Case 3: Too many choices too early

### Problem

The interface asks users to make many decisions before they understand the task or see value.

### Better pattern

Use progressive disclosure.

- show essentials first
- provide smart defaults
- group common preferences
- collapse advanced controls
- reveal detail only when relevant

### Use when

- many settings exist
- beginner and expert users share the same product
- optional details compete with the primary task

### Do not use when

- users must compare all fields at once
- hiding options makes expert work slower

### Component ideas

- ProgressiveForm
- AdvancedSettingsAccordion
- ExpertModeToggle
- PreferenceGroups

---

## Case 4: Technical labels

### Problem

Labels use system language instead of user-facing language.

Examples:

- `negative_prompt`
- `style_strength`
- `callback_url`
- `duration_seconds`
- `permission_scope`

### Better pattern

Translate technical terms into user impact.

Examples:

- `negative_prompt` -> Things to avoid
- `style_strength` -> How strongly to follow the style
- `duration_seconds` -> Length
- `permission_scope` -> What this access allows
- `callback_url` -> developer/system-only for most user interfaces

### Use when

- labels come from API fields
- users ask what a field means
- fields affect cost, output, privacy, or irreversible actions

### Component ideas

- UserFacingLabel
- FieldHelpPopover
- InlineHelperText
- ExampleTooltip

---

## Case 5: Weak success state

### Problem

After success, the UI only says done or shows a static result.

### Better pattern

Turn success into continuation.

Possible next actions:

- edit
- make another version
- compare
- save
- share
- publish
- export
- use as reference
- schedule
- invite collaborators
- create follow-up task

### Use when

- the result is the start of more work
- the product has multiple related capabilities
- success is a high-intent moment

### Do not use when

- the action is trivial and frequent
- extra actions would distract from completion

### Component ideas

- SuccessActionPanel
- ResultActionBar
- NextStepSuggestions
- ShareExportPanel

---

## Case 6: Poor error recovery

### Problem

The error state only says failed, invalid, or error.

### Better pattern

Explain:

- what happened
- why it matters
- what was affected
- what the user can do next

For paid, quota, data, or long-running tasks, also explain whether cost, quota, or saved work was affected.

### Use when

- failure can block progress
- user trust is at risk
- retry or recovery is possible

### Component ideas

- RecoverableErrorState
- RetryAction
- ErrorDetailsDisclosure
- ContactSupportLink

---

## Case 7: Long-running task uncertainty

### Problem

The user waits with only a spinner and does not know whether the task is still working.

### Better pattern

Use staged progress, a persistent task card, background processing, and leave-safe messaging.

Examples:

- preparing input
- processing
- generating
- reviewing
- finalizing
- saving result

### Use when

- tasks take more than a few seconds
- users may leave the page
- results can be saved or delivered later

### Do not use when

- progress would be fake and misleading
- the task is nearly instant

### Component ideas

- ProgressTaskCard
- StageProgress
- BackgroundTaskQueue
- CompletionNotification

---

## Case 8: Tool menu overload

### Problem

Users must search a menu or navigation structure to find the right tool after selecting an object or result.

### Better pattern

Move actions closer to the object and moment where they are needed.

Examples:

- result card action bar
- contextual toolbar
- inline action menu
- floating action bar
- command palette

### Use when

- the product has many tools
- users often continue from an object or result
- navigation separates users from action

### Component ideas

- ContextualActionBar
- ObjectActionMenu
- FloatingToolbar
- CommandPalette

---

## Case 9: AI result iteration

### Problem

The user can only regenerate the entire result even when they only want to change part of it.

### Better pattern

Support iteration and partial control.

Possible patterns:

- revision chips
- keep/change controls
- partial editing
- region selection
- compare versions
- version branching
- undo and restore

### Use when

- results are subjective or creative
- users frequently say almost right
- users need control without starting over

### Component ideas

- RevisionChips
- VersionComparison
- PartialEditSelector
- VersionTree
- KeepChangePanel

---

## Case 10: Static history

### Problem

History is only a storage list.

### Better pattern

Turn history into a continuation surface.

Actions:

- continue editing
- duplicate
- branch
- restore
- compare versions
- reuse settings
- use as reference
- export

### Use when

- previous outputs are useful inputs for future tasks
- users return to refine or reuse work

### Component ideas

- ContinuationCard
- VersionHistory
- ReuseSettingsAction
- BranchFromHere

---

## Case 11: Passive feed

### Problem

Users can browse content, but browsing does not lead to meaningful action.

### Better pattern

Connect consumption to action.

Possible actions:

- remix this
- use as template
- create similar
- save inspiration
- follow creator
- see how it was made
- add to workspace

### Use when

- content can inspire creation
- users need discovery before action
- community content can become workflow input

### Component ideas

- RemixableFeedCard
- InspirationSave
- TemplateFromPost
- CreationCTA

---

## Case 12: Flat interaction feedback

### Problem

Actions only change color or text, making the product feel unresponsive or flat.

### Better pattern

Add small feedback when it confirms action:

- press state
- selected state
- subtle scale
- saved/copied toast
- count update
- first-time delight

### Use when

- actions are social, save-related, publish-related, or emotionally positive
- feedback confirms a state change

### Do not use when

- the action is serious, destructive, payment-related, or error-related
- the animation slows high-frequency work

### Component ideas

- MicroInteractionButton
- SaveFeedback
- CopyConfirmation
- SubtleCelebration

---

## Case 13: Chatbot wrapper

### Problem

An AI assistant behaves like a chat-styled button. It accepts text, calls a tool, and returns a result without clarifying intent, showing a plan, or helping the user iterate.

### Better pattern

Turn the assistant into an AI-assisted workflow.

Possible elements:

- intent clarification
- editable plan
- assumptions summary
- tool execution status
- result critique
- next action suggestions
- memory-aware defaults

### Use when

- AI is part of task completion
- user intent is ambiguous
- the output needs iteration

### Component ideas

- EditableAgentPlan
- AssumptionReviewCard
- ToolExecutionTimeline
- ResultRefinementPanel

---

## Case 14: Parameters instead of direct manipulation

### Problem

Users control objects by typing abstract values when they could manipulate the object directly.

Examples:

- entering start/end time instead of selecting a timeline region
- typing crop dimensions instead of dragging a crop box
- typing layout positions instead of dragging objects

### Better pattern

Use direct manipulation with optional precise controls.

### Use when

- the object is visual, spatial, temporal, or media-based
- users need to understand the result by seeing it

### Component ideas

- TimelineSelector
- CanvasEditor
- CropHandle
- DragRegion
- PrecisionInputPanel

---

## Case 15: Hidden value after generation

### Problem

A product has useful follow-up capabilities, but users never discover them because the result screen is passive.

### Better pattern

Use contextual education through next actions, not a forced tutorial.

Examples:

- improve result
- export
- compare
- automate
- reuse
- publish
- collaborate

### Use when

- the product has a broader workflow
- feature discovery matters
- users learn by doing

### Component ideas

- ContextualNextActions
- CapabilityHint
- InlineWorkflowEducation

---

# Output

When applying this library, return:

1. Matched patterns and why.
2. Current interaction problem.
3. Why the pattern may help.
4. When not to use this pattern.
5. Better structure.
6. Before and after flow.
7. Microcopy.
8. Component suggestions.
9. Metrics to validate.
10. Risks of applying this pattern.
11. Final recommendation.
