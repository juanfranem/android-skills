# Previews and Authoring Surfaces

## When to read this

- Use this when choosing preview wrappers, fake data, multipreview patterns, or preview-specific screen shells.

## Core decisions

- Previews are design-time authoring aids, not runtime verification.
- Preview state should be stable, explicit, and cheap to construct.
- Preview wrappers should mirror production theme and shell structure without pulling in live app dependencies.

## Recommended patterns

- Build previews from isolated composables or screen entry points that accept plain state and callbacks instead of live app wiring.
- Keep sample models, fake callbacks, and preview state deterministic so layout regressions are easy to spot.
- Use shared theme wrappers or lightweight screen-shell wrappers when they remove repetition, but keep important screen inputs visible at the preview callsite.
- Preview error, loading, empty, success, and large-screen states so authoring surfaces exercise more than the happy path.
- Prefer sample data that stresses truncation, scrolling, density, and edge cases rather than only neat demo content.
- Treat previews as an authoring tool and use real UI tests when the question is runtime behavior, semantics, or interaction correctness.

## Avoid

- Do not turn preview guidance into a testing guide.
- Do not rely on real network, database, or navigation wiring inside previews.
- Do not hide critical screen state behind opaque preview-only helpers.
- Do not make preview wrappers so heavy that authors cannot see which state, shell, or data shape a screen actually depends on.
