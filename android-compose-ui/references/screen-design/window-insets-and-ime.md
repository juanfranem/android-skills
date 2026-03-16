# Window Insets and IME

## When to read this

- Use this when screens must behave correctly around system bars, safe areas, edge-to-edge layouts, or the on-screen keyboard.

## Core decisions

- Insets are screen-shell constraints, not ad hoc padding fixes.
- Keyboard-safe layouts need both visibility and reachability for focused fields.
- Consumption boundaries should be deliberate so padding is applied once at the right layer.

## Recommended patterns

- Treat `WindowInsets` as part of shell design so system bars, safe drawing regions, and edge ownership are decided at the screen boundary instead of patched later.
- Choose one layer to own each affected edge, place inset padding there, and consume insets only when downstream content should stop reapplying the same space.
- Verify focused fields remain visible and reachable when the IME appears, especially in forms, bottom sheets, and mixed static-plus-scroll content.
- Pair keyboard-safe layouts with scroll and focus behavior that can bring the active field back into view instead of assuming the IME animation solves reachability.
- Review overlays, sheets, and form shells separately from static content screens because their inset and keyboard behavior often diverges.
- Use modifier guidance here only to explain inset placement and consumption boundaries, not as a replacement for the broader layout-and-modifiers reference.

## Avoid

- Do not turn this into a generic modifiers guide.
- Do not stack inset and padding modifiers blindly.
- Do not assume edge-to-edge layouts are correct on every screen by default.
- Do not let IME handling depend on lucky viewport space when the screen should actively preserve focus visibility and scroll reachability.
