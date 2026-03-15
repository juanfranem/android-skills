# Material 3 Theming

## When to read this
- The request is about Compose theming, color roles, typography, shapes, dynamic color, or design-system boundaries.

## Core decisions
- Prefer `MaterialTheme` tokens over hard-coded styling.
- Use role-correct color pairing.
- Call out experimental or version-sensitive Material 3 APIs explicitly.

## Recommended patterns
- Define theme tokens centrally through `MaterialTheme(colorScheme = ..., typography = ..., shapes = ...)`.
- Extend Material before replacing it with one-off per-screen styling.
- Use semantic color pairs such as `primary` with `onPrimary` and `primaryContainer` with `onPrimaryContainer`.
- Keep dynamic color opt-in intentional, with app-defined light and dark fallbacks on older devices.
- Reach for component `*Defaults` helpers before local ad hoc overrides.
- Use the Material 3 type scale and shape scale as reusable systems, then tune emphasis with role-correct color, typography weight, and tonal or shadow elevation instead of one-off visual exceptions.
- Prefer `Surface` and component defaults for tonal elevation, shadow elevation, and container emphasis before inventing a parallel styling model.

## Avoid
- Per-screen hard-coded color systems.
- Mixing Material 2 and Material 3 mental models.
- Using dynamic color accidentally or without fallback behavior.
- Treating elevation or shapes as isolated one-off styling choices.
- Using experimental Material 3 APIs without naming the required opt-in or caveating library-version sensitivity.
- Pairing foreground and background roles incorrectly or bypassing theme tokens when accessible contrast depends on the role system.
