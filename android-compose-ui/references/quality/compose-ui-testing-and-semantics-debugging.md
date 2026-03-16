# Compose UI Testing and Semantics Debugging

## When to read this
- Tests cannot locate a node you know exists in the UI.
- You need to choose between merged and unmerged semantics trees for assertions.
- You are debugging why a semantic property is not exposed as expected.
- You need to decide between Compose test APIs, Espresso, or UiAutomator for hybrid scenarios.
- You are deciding when `Modifier.testTag` is appropriate versus user-facing semantics.

## Core decisions
- Prefer semantics-first testing: query by text, content description, or role before falling back to tags.
- Use `Modifier.testTag` as structural fallback, not as the primary testing vocabulary.
- Choose merged tree for user-centric assertions; switch to unmerged only when child-level detail is required.
- Let Compose synchronization handle idleness before adding custom waits or sleeps.
- Stay in Compose test APIs for pure Compose UI; use Espresso or UiAutomator only for View interop or device-level flows.
- Enable `testTagsAsResourceId` only when UiAutomator or mixed tooling specifically requires resource IDs.

## Recommended patterns
- Start debugging by printing the semantics tree to verify the node exists and check whether it is merged or unmerged.
- Use `onNodeWithText` or `onNodeWithContentDescription` when labels are stable and user-facing.
- Switch to `onNode(hasTestTag(...))` when no suitable semantic hook exists or when testing structural containers.
- Prefer `onNodeWithTag(..., useUnmergedTree = true)` when the target is nested inside a merged parent.
- Add `testTagsAsResourceId = true` at the root of a composable subtree only when external tools require resource IDs.
- For hybrid apps, use Espresso `onView` for Views and Compose APIs for Compose nodes without extra configuration.
- Register custom idling resources for background work invisible to Compose or Espresso synchronization.
- Use `mainClock` APIs to control time and advance animations deterministically in tests.
- Run accessibility audits alongside functional tests to catch semantic gaps early.

## Avoid
- Using `Modifier.testTag` as the first choice for every testable element.
- Arbitrary `Thread.sleep` calls that fight Compose synchronization.
- Asserting on implementation details like internal layout structure or composable function names.
- Enabling `testTagsAsResourceId` globally without a specific interop requirement.
- Mixing merged and unmerged tree assumptions without verifying which tree the assertion targets.
- Writing tests that depend on specific timing of recompositions or animation frames.
