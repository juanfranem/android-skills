# Testing

## When to read this
- The task is about Compose UI verification, semantics queries, test tags, synchronization, or accessibility checks.

## Core decisions
- Prefer semantics-first querying over implementation detail selectors.
- Understand merged versus unmerged semantics trees before concluding a node is missing.
- Use tags as fallback structure, not the primary testing language.

## Recommended patterns
- Start with `ComposeTestRule` and verify rendering through user-observable semantics.
- Query by text, role, state, or content description before using `Modifier.testTag`.
- Switch to the unmerged tree only when merged semantics hide the node you need to assert.
- Let Compose synchronization and idling work for you before adding custom waits.
- Include accessibility checks when the interaction or semantics contract matters.

## Avoid
- Basing tests on internal layout structure or fragile implementation details.
- Using `Modifier.testTag` as the first choice for every assertion.
- Fighting synchronization with arbitrary sleeps.
