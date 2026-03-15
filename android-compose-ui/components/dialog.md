# Dialog

## Use when

- The flow must pause for confirmation, acknowledgment, or short focused input.

## Variants

- `AlertDialog`
- `Dialog`

## Guidance

- Prefer `AlertDialog` for standard confirm/cancel patterns.
- Use `Dialog` for fully custom content.
- If the content is long or complex, a full screen is often better.

## Nearby alternatives

- Supplementary contextual content -> bottom sheet

## Common mistakes

- Building long forms inside dialogs.

## Official source

- https://developer.android.com/develop/ui/compose/components/dialog
