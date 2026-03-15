# Focus and Traversal Checklist

- Traversal is coherent for both declaration-order navigation and directional navigation.
- Related controls use `focusGroup()` before custom directional overrides.
- Custom focus order uses `focusProperties` only where the visual layout genuinely needs it.
- Programmatic focus uses `FocusRequester` from event-driven code paths, not during composition.
- Large-screen inputs such as keyboard, D-pad, mouse, or controller still reach every important action predictably.
- Focus state, captured focus, or validation traps remain understandable and escapable.
