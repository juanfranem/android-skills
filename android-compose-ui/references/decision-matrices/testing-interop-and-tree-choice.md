# Testing Interop and Tree-Choice Matrix

- Use merged semantics tree when testing user-visible behavior and high-level component contracts.
- Use unmerged semantics tree when you need to assert on child elements hidden by merged parents.
- Prefer Compose test APIs for pure Compose UI; use Espresso `onView` for View-based elements in hybrid apps.
- Choose UiAutomator when testing across app boundaries or when device-level automation is required.
- Enable `testTagsAsResourceId` only when UiAutomator or mixed tooling requires resource ID access to composables.
- Use `Modifier.testTag` as fallback when no stable user-facing semantic hook exists for the target element.
- In hybrid apps, keep Espresso and Compose tests separate; do not mix matchers from both frameworks on the same node.
- Register custom idling resources for background work invisible to Compose or Espresso synchronization.
- Switch to unmerged tree via `useUnmergedTree = true` when debugging why a node cannot be found in merged mode.
