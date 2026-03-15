# Time Pickers

## Use when

- The user needs explicit time input.

## Variants

- `TimePicker`
- `TimeInput`
- Dialog presentation guidance on a companion page

## Core APIs

- `TimePickerState`
- `rememberTimePickerState(initialHour, initialMinute, is24Hour)`

## Guidance

- Use dial UI when direct time selection is comfortable.
- Use text input when typed precision is better.
- Often presented inside dialogs.

## Important note

- Official docs mark these APIs as experimental. Mention `@OptIn(ExperimentalMaterial3Api::class)` when relevant.

## Official sources

- https://developer.android.com/develop/ui/compose/components/time-pickers
- https://developer.android.com/develop/ui/compose/components/time-pickers-dialogs
