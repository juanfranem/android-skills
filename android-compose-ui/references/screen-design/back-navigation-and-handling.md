# Back Navigation and Handling

## When to read this

- Use this when a screen, sheet, dialog, search state, or selection mode needs local back behavior without redefining app navigation architecture.

## Core decisions

- Local back consumption should be exceptional and easy to explain.
- Route-level navigation remains outside this file.
- Back priority must stay predictable when several transient surfaces are visible.

## Recommended patterns

- Use `BackHandler` for transient UI dismissal and local mode exit, such as closing a sheet, dismissing a dialog, clearing search focus or expanded state, or leaving selection mode.
- Keep the owning surface responsible for deciding when it can consume back so the condition stays close to the UI state it controls.
- Resolve stacked surfaces from the most local visible owner outward so back behavior stays predictable when dialogs, sheets, overlays, and temporary modes overlap.
- Treat route changes and destination popping as navigation responsibilities, and point back to `navigation-patterns.md` when the question is app-level flow rather than local UI handling.
- Call out predictive-back or stack-specific caveats when APIs are version-sensitive, especially if local interception changes animation expectations or handoff to the navigation stack.

## Avoid

- Do not turn this into a navigation graph guide.
- Do not let multiple unrelated layers compete silently for back events.
- Do not hide irreversible navigation decisions inside local UI handlers.
- Do not keep `BackHandler` active when the owning transient surface is no longer visible or relevant.
