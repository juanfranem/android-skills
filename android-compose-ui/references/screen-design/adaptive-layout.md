# Adaptive Layout

## When to read this
- The request mentions tablets, foldables, panes, resizing, rails, drawers, or large screens.

## Core decisions
- Adapt to window conditions, not device labels.
- Use structural adaptation when layout meaning changes.

## Recommended patterns
- Use window size classes.
- Prefer `NavigationSuiteScaffold` or pane scaffolds when the structure truly changes, and call out when those APIs are experimental or version-sensitive in the current library version.
- Switch between bottom bar, rail, drawer, or pane layouts based on information architecture plus window conditions.
- Keep content models and event contracts consistent across layouts so only structure changes.

## Avoid
- Using the same navigation shell for every window size.
- Treating spacing tweaks as sufficient structural adaptation.
- Binding navigation chrome to device names instead of measured window state.
