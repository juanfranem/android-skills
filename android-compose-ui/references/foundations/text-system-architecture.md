# Text System Architecture

## When to read this
- The task is about choosing text primitives, text-field architecture, or the boundary between Material text APIs and foundation text APIs.

## Core decisions
- Start with Material text APIs for product UI and drop to foundation primitives only when decoration or behavior control requires it.
- Separate display, styling, editing, filtering, and output formatting concerns instead of collapsing them into one text abstraction.
- Prefer state-based text-field architecture for new flows, while calling out experimental or version-sensitive APIs explicitly.

## Recommended patterns
- Use `Text` for normal app copy and localized resource-backed strings; use `BasicText` only when you need a lighter primitive without Material decoration.
- Use `TextField` or `OutlinedTextField` for Material input flows and `BasicTextField` only when you are intentionally owning decoration, semantics, and container behavior yourself.
- Prefer `TextFieldState` and `rememberTextFieldState()` for new text entry flows so text, selection, and composition stay in one hoistable state holder.
- Split filtering from formatting: use `InputTransformation` for accepted input and `OutputTransformation` for display-only formatting instead of mutating persisted text for both jobs.
- Keep localized text sourcing outside the composable when possible, and prefer resource or locale-aware text sources over hardcoded strings.
- Treat text-field model choices as version-sensitive when the documented state-based Material APIs are still experimental in the targeted Compose version.

## Avoid
- Reaching for `BasicText` or `BasicTextField` just to recreate Material behavior manually.
- Mixing validation, formatting, and stored text mutation in one callback-heavy flow.
- Building new forms around legacy value-based state when state-based text fields fit the project constraints.
- Hardcoding user-visible copy when the screen should participate in localization.
