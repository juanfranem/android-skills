# Focus and Input Patterns

## When to read this
- The task is about focus traversal, keyboard or D-pad navigation, large-screen input behavior, or deciding how interactive layouts should behave beyond touch.

## Core decisions
- Build layouts so focus and input behavior work for keyboard, D-pad, mouse, and large-screen contexts, not touch alone.
- Prefer the highest abstraction level that already carries focus, semantics, and interaction behavior correctly.
- Use explicit focus overrides only after checking whether grouping or layout structure solves the problem more cleanly.

## Recommended patterns
- Start with Compose's default traversal model and use `focusGroup()` when related elements should be traversed as one logical cluster before moving elsewhere.
- Make custom interactive elements intentionally focusable and react to `onFocusChanged` only when the UI needs custom visual state or container awareness.
- Use `FocusRequester` for event-driven focus moves and keep `requestFocus()` out of composable execution so focus remains tied to real interactions.
- Add explicit `focusProperties` directions only when declaration order or geometry does not match the intended keyboard or D-pad path.
- Keep interaction high-level whenever possible by favoring built-in components or gesture modifiers that already include keyboard, hover, and semantics support.
- Test screens with keyboard, D-pad, mouse, stylus, and other large-screen inputs when the feature could run outside a phone-only touch context.

## Avoid
- Hand-writing focus order first when grouping or cleaner layout structure would make traversal obvious.
- Using raw pointer APIs for common tap, click, scroll, or drag behavior that higher-level APIs already model.
- Triggering programmatic focus during composition instead of from a real event or side effect boundary.
- Assuming touch-centric behavior is enough for tablets, ChromeOS, TV, controller, or accessibility users.
