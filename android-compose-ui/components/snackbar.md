# Snackbar

## Use when

- The app needs to show brief, non-blocking feedback, often with an optional undo/retry action.

## Core APIs

- `Snackbar`
- `SnackbarHost`
- `SnackbarHostState`
- `showSnackbar()`

## Guidance

- Use naturally with `Scaffold`.
- Best for save confirmation, undo, and transient connectivity hints.
- Keep messages concise.

## Nearby alternatives

- Critical acknowledgment needed -> dialog
- Persistent inline issue -> inline error/supporting text

## Common mistakes

- Using snackbar for blocking or high-severity decisions.
- Hiding critical information in a transient message.

## Official source

- https://developer.android.com/develop/ui/compose/components/snackbar
