# Accessibility

## When to read this
- The task asks for accessibility review, semantics, labels, traversal, or scalable content.

## Core decisions
- Start with accessible Compose defaults.
- Add semantics only where defaults are incomplete.

## Recommended patterns
- Provide meaningful `contentDescription` values only when the graphic carries meaning.
- Use traversal groups and semantic customization deliberately.
- Prefer visible labels, helper text, and state text that already communicate meaning before adding custom semantics.
- Verify focus order, touch targets, contrast, and scalable text behavior together.

## Avoid
- Duplicated semantics.
- Decorative content with misleading spoken labels.
- Overriding semantics in ways that hide useful built-in role or state information.
