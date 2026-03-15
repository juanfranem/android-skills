# Interaction and Gesture Review

## When to read this
- The task is about reviewing gesture choices, custom input behavior, semantics impact, or interaction feedback quality in Compose UI.

## Core decisions
- Choose the highest abstraction that fits before reaching for raw pointer handling.
- Review custom input through semantics, testability, and non-touch compatibility, not gesture success alone.
- Treat interaction feedback as part of the contract, not optional polish.

## Recommended patterns
- Prefer components and gesture modifiers such as `clickable`, `combinedClickable`, `verticalScroll`, `draggable`, or `transformable` before `pointerInput`.
- When raw input is truly necessary, restore any keyboard, semantics, or accessibility behavior that high-level APIs would have supplied automatically.
- Review scrolling and dragging in terms of both gesture detection and visible state application, since detectors like `draggable` and `transformable` do not move content for you.
- Check whether nested scrolling, swipe-to-dismiss, or other canonical patterns already exist as higher-level APIs before building custom gesture stacks.
- Use `MutableInteractionSource` and interaction-derived state for pressed, focused, hovered, or dragged feedback instead of re-implementing that state machine manually.

## Avoid
- Dropping to `pointerInput` because it feels flexible when a higher-level API already captures the product intent.
- Shipping custom gestures that lost semantics, keyboard access, or predictable test hooks along the way.
- Confusing gesture detection with full behavior when the UI still needs offset, scroll, feedback, or dismissal state applied separately.
- Ignoring clipboard, drag-and-drop, or rich content pathways when the feature behaves like production content transfer rather than simple taps.
