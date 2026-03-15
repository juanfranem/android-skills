# Screen Patterns

## When to read this
- The task is about structuring a common screen type or handling loading, empty, error, and success states.

## Core decisions
- Match the screen shell to the primary task.
- Make state changes legible before adding decorative complexity.

## Recommended patterns
- For forms, group fields by meaning, keep the submit action clear, and surface validation near the field and at submission time.
- For settings screens, use obvious grouping, immediate-toggle semantics where appropriate, and concise supporting text.
- For search-first screens, make search state primary, keep empty and recent states explicit, and avoid burying filter context.
- For feeds and browsing surfaces, stabilize item identity, keep hierarchy scannable, and separate browsing from item-detail actions.
- For loading, empty, error, and success states, preserve layout continuity where possible and make recovery actions explicit.

## Avoid
- Reusing the same generic shell for forms, browsing, and settings when their interaction patterns differ.
- Hiding important state transitions behind transient-only feedback.
- Letting placeholder or error states collapse the structure users need to recover.
