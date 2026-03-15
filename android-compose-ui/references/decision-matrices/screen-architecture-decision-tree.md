# Screen Architecture Decision Tree

- Keep state local when only one composable needs it and the state is ephemeral UI detail.
- Hoist to a parent when multiple children need to read or update the same screen state.
- Move to a state holder when screen logic grows beyond simple event wiring but does not need Android lifecycle integration.
- Move to a `ViewModel` when state must survive configuration change, coordinate business logic, or integrate with lifecycle-aware sources.
- Use explicit parameters first; use `CompositionLocal` only for true cross-cutting ambient dependencies.
