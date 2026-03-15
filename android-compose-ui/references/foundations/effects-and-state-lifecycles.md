# Effects and State Lifecycles

## When to read this
- The task involves side effects, coroutine launch timing, restart keys, saved state, retained state, or derived state.

## Core decisions
- Choose the narrowest effect API that matches the lifecycle you need.
- Treat restart keys as correctness boundaries, not convenience toggles.
- Preserve user-visible state intentionally with saveable or retained mechanisms.

## Recommended patterns
- Use `LaunchedEffect` for composition-scoped suspend work tied to explicit keys.
- Use `DisposableEffect` for setup and cleanup when the composable enters and leaves composition.
- Use `rememberCoroutineScope` for event-driven work launched from callbacks.
- Use `rememberUpdatedState` when an effect should keep running but read the latest lambda or value.
- Use `produceState` to bridge external async sources into Compose state.
- Use `derivedStateOf` only when derived values reduce unnecessary recomposition or expensive recalculation.
- Use `rememberSaveable` for UI state that should survive configuration change and process recreation when supported by a saver.
- Use `retain` only when the project and Compose version support it, and explicitly caveat that it is version-sensitive or experimental where applicable.
- Keep restart keys minimal, stable, and complete enough to avoid stale work.

## Avoid
- Launching ongoing work directly in composition without an effect API.
- Using unstable or overly broad restart keys that cause accidental restarts.
- Replacing event-driven coroutine launches with `LaunchedEffect` when no composition key should control them.
- Treating `derivedStateOf` as a default wrapper for every computed value.
