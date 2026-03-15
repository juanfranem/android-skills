# Buttons

## Use when

- The user needs a direct action trigger with clear emphasis.

## Variants

- `Button`: primary local action
- `FilledTonalButton`: important but softer supporting action
- `ElevatedButton`: separated from busy or flat surfaces
- `OutlinedButton`: visible secondary action
- `TextButton`: low-emphasis action

## Key APIs

- `onClick`
- `enabled`
- `colors`
- `contentPadding`

## Good defaults

- Use `Button` for the clearest action in a section or dialog.
- Do not use several filled buttons at the same emphasis level unless the hierarchy is genuinely flat.

## Nearby alternatives

- Screen-level primary action -> FAB family
- Local mode switch -> segmented buttons

## Common mistakes

- Choosing by aesthetics instead of emphasis.
- Overriding colors instead of using theme tokens.

## Official source

- https://developer.android.com/develop/ui/compose/components/button
