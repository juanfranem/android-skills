# Progress Indicators

## Use when

- A process is running and the UI should communicate progress or waiting.

## Variants

- `LinearProgressIndicator`
- `CircularProgressIndicator`
- Determinate and indeterminate modes

## Guidance

- Use determinate when real progress is known.
- Use indeterminate only when the duration is unknown.
- Linear is usually better inline; circular is good for compact loading states.

## Nearby alternatives

- Brief completed/failed feedback -> snackbar

## Common mistakes

- Showing indeterminate forever when progress is actually known.
- Using circular indicators in places where linear progress communicates better.

## Official source

- https://developer.android.com/develop/ui/compose/components/progress
