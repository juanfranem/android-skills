# Performance

## When to read this
- The task is about recomposition cost, unstable parameters, list performance, phase-aware reads, or jank in Compose UI.

## Core decisions
- Keep parameters minimal and stable.
- Preserve list identity with correct keys.
- Read fast-changing state in the latest safe phase.

## Recommended patterns
- Pass focused immutable values and callbacks instead of broad mutable objects.
- Provide stable keys for lazy items when identity, animations, or remembered state matter.
- Keep fast-changing reads out of composition when layout or draw phases are better fits.
- Reduce unnecessary recomposition by narrowing state ownership and derived work.
- Review broad parameters, accidental state reads, and theme bypasses as common sources of churn.

## Avoid
- Broad unstable parameters.
- Missing keys in dynamic collections.
- Composition-phase reads for fast-changing state.
- Bypassing theme tokens with repeated ad hoc styling that fragments reuse.
