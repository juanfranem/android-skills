# Layout and Modifiers

## When to read this
- The task is about layout primitives, modifier order, lazy containers, pagers, flow layouts, or custom measurement.

## Core decisions
- Start with the simplest layout primitive that matches the structure.
- Modifier order changes behavior because constraints, drawing, input, and semantics layer in sequence.
- Keep identity stable in scrolling containers.

## Recommended patterns
- Use `Row`, `Column`, and `Box` for local structure, and `Scaffold` for screen-level slots.
- Apply layout, clipping, background, input, and semantics modifiers in deliberate order.
- Use lazy containers for long or changing collections and provide stable keys when identity matters.
- Use pager or flow layouts when the interaction pattern truly matches swiping pages or wrapping content.
- Reach for a custom layout only when standard primitives cannot express the measurement or placement rules clearly.

## Avoid
- Stacking unnecessary nested layout primitives when a simpler parent can express the same structure.
- Reordering modifiers casually and expecting the same measurement or hit-testing behavior.
- Omitting keys from dynamic lazy content where item identity affects state or animations.
