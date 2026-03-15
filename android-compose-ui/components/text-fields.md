# Text Fields

## Use when

- The screen needs general text entry, secure entry, formatting, filtering, or lower-level text editing control.

## Variants

- `TextField`
- `OutlinedTextField`
- `SecureTextField`
- `BasicTextField`
- State-based and value-based models

## State model

- Prefer the newer state-based approach when the project and library version support it.
- `TextFieldState` can live outside UI-only classes, including in a ViewModel.
- `rememberTextFieldState()` creates a remembered saveable state holder.

## Advanced APIs

- `InputTransformation`
- `OutputTransformation`
- `TextFieldLineLimits`

## Guidance

- Use filled or outlined variants based on the surrounding visual density and existing product pattern.
- Use `SecureTextField` for password-like inputs.
- Use `BasicTextField` only when Material decoration should be removed intentionally.

## Important note

- Some newer text-field APIs are documented as experimental on the official pages. Mention opt-in when applicable.

## Official source

- https://developer.android.com/develop/ui/compose/text/user-input
