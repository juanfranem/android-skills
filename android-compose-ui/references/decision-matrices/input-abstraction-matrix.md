# Input Abstraction Matrix

- Built-in component behavior fits -> use the component API first for semantics, focus, and accessibility.
- Custom surface with a common gesture -> use gesture modifiers such as `clickable`, `combinedClickable`, `draggable`, `transformable`, or scrolling modifiers.
- Truly custom or composite gesture -> use `pointerInput` or gesture detectors and rebuild semantics and keyboard behavior deliberately.
- Custom scroll container with standard container behavior -> prefer `scrollableArea` over raw `scrollable` deltas.
- Swipe-to-dismiss or other canonical gesture pattern -> prefer the dedicated high-level component before custom detectors.
- Gesture review smell -> if the code owns raw events and now has to manually restore hover, focus, semantics, or tests, the abstraction may be too low.
