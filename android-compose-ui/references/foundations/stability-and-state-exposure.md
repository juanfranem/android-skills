# Stability and State Exposure

## When to read this
- The task is about hoisted state, stable parameters, public Compose API evolution, or broad parameter smells.

## Core decisions
- Prefer stateless composables by default and make ownership boundaries obvious when state must be shared.
- Treat stable and immutable types as behavioral contracts that affect recomposition and API compatibility.
- Evolve public APIs by adding defaulted surface area carefully instead of reshaping existing contracts casually.

## Recommended patterns
- Pass plain values and callbacks when the state relationship is simple and the caller should remain the source of truth.
- Introduce a hoisted `...State` type when related values and operations need to travel together; keep it focused, stable, and practical to remember or save.
- Prefer immutable models where practical, and use `@Stable` only when the type truly notifies Compose correctly as it changes.
- Keep parameter lists narrow enough that callers can reason about stability; split broad mutable parameter bags into smaller contracts when they mix unrelated concerns.
- Read broad theme-like defaults from parameter defaults rather than deep implementation so callers can still override them explicitly.
- For public APIs, add new parameters near the end with defaults and use compatibility-friendly extension patterns instead of removing or reordering established parameters.

## Avoid
- Accepting `MutableState<T>` or `State<T>` just because it is convenient when explicit values and callbacks would be clearer.
- Marking types stable or immutable casually without honoring equality and change-notification expectations.
- Letting a composable both own meaningful internal state and expose a competing external ownership path.
- Breaking callers by removing parameters, changing stable contracts lightly, or forcing every variant through one broad mutable object.
