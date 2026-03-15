# Bottom Sheet

## Use when

- You need a supplementary surface attached to the current screen.
- The flow should feel contextual rather than fully interruptive.

## Core APIs

- `ModalBottomSheet`
- `SheetState`
- `rememberModalBottomSheetState()`

## Guidance

- Good for secondary actions, drill-in details, and contextual controls.
- If content becomes long or primary, promote it to a full screen.
- Use programmatic `show()` and `hide()` when async events drive the sheet.

## Nearby alternatives

- Short interruptive decision -> dialog
- Full task or long form -> dedicated screen

## Common mistakes

- Putting complex long workflows into a sheet.

## Official source

- https://developer.android.com/develop/ui/compose/components/bottom-sheets
