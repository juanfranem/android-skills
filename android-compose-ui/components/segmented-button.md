# Segmented Button

## Use when

- The user needs a compact set of side-by-side options.
- The control changes a local mode, view, sort, or compact selection set.

## Variants

- `SingleChoiceSegmentedButtonRow`
- `MultiChoiceSegmentedButtonRow`
- `SegmentedButton`

## Guidance

- Best for small option sets, often 2-5 items.
- Prefer chips when the set is larger or semantically more filter-like.
- Prefer tabs when switching sibling content sections rather than local modes.

## Key APIs

- row composables
- `SegmentedButton`
- `space`

## Common mistakes

- Using segmented buttons as top-level navigation.
- Using them for large option sets that should be chips or menus.

## Official source

- https://developer.android.com/develop/ui/compose/components/segmented-button
