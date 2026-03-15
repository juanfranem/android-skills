# Compose UI Architecture

## When to read this
- The task is about state ownership, event flow, navigation boundaries, or screen structure.

## Core decisions
- Prefer state down, events up.
- Hoist state to the lowest common owner.
- Pass callbacks into screens instead of framework controllers.

## Recommended patterns
- Keep composable parameters small and explicit.
- Use state holders or `ViewModel` only when the responsibility actually requires them.
- Keep navigation decisions outside destination composables and pass route arguments as data.
- Reach for `CompositionLocal` only for true cross-cutting ambient concerns.

## Avoid
- Passing `NavController` into destination composables.
- Using `CompositionLocal` for screen-specific dependencies.
- Growing parameter lists by passing broad mutable state objects instead of focused values and callbacks.
