# View Interop

## When to read this

- Use this when deciding whether to wrap an existing View, host Compose inside a View tree, or avoid interop altogether.

## Core decisions

- Interop is a boundary decision, not a default architecture.
- Ownership for state, lifecycle, and updates must stay explicit on one side of the boundary.
- Wrappers should stay narrow and local so they are easy to remove later.

## Recommended patterns

- Choose interop when a specific existing View capability still earns its keep, and treat broad screen-level interop as a migration smell unless the boundary is temporary and explicit.
- Use `AndroidView` or `AndroidViewBinding` only for targeted View-backed capabilities, and use `ComposeView` hosting when Compose is entering an existing View hierarchy incrementally.
- Keep state ownership on one side of the boundary, pass stable inputs across it, and make update lambdas minimal and idempotent.
- Make listener registration, disposal, and lifecycle cleanup obvious so wrapped Views do not leak observers, callbacks, or stale references.
- Hide interop behind small adapters that preserve semantics, testing hooks, and performance visibility instead of leaking View concepts through the full feature.
- Re-check testability, accessibility semantics, and measure or invalidation cost before keeping an interop layer in place for the long term.

## Avoid

- Do not restate general Compose architecture guidance already covered elsewhere.
- Do not let interop become a vague halfway migration layer across the entire screen.
- Do not hide ownership of mutable state or lifecycle hooks.
- Do not let wrappers silently translate too many concepts at once, because that makes behavior, semantics, and performance harder to reason about.
