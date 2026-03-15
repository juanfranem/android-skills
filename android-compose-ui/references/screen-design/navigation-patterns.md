# Navigation Patterns

## When to read this
- The task is about choosing app navigation structure, tabs versus segmented controls, pane navigation, or route boundaries.

## Core decisions
- Choose navigation by hierarchy, destination count, and window conditions.
- Keep route parsing and controller usage at the edges.

## Recommended patterns
- Use bottom bar on compact layouts, rail on medium layouts, and drawer when navigation density or hierarchy grows.
- Use tabs for sibling content sections and segmented buttons for local mode switches.
- Use pane-based adaptive navigation when simultaneous regions improve task flow, and caveat pane APIs when they are experimental or version-sensitive.
- Pass route arguments as plain data and keep callback boundaries explicit between navigation and screen UI.

## Avoid
- Switching between bottom bar, rail, and drawer by aesthetic preference alone.
- Treating tabs as a replacement for top-level app navigation.
- Passing controllers deep into the composable tree when callbacks and state are enough.
