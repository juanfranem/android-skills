# Floating Action Button

## Use when

- The screen has one main primary action such as create, add, or compose.

## Variants

- `FloatingActionButton`
- `SmallFloatingActionButton`
- `LargeFloatingActionButton`
- `ExtendedFloatingActionButton`

## Key APIs

- `onClick`
- `containerColor`
- `contentColor`

## Guidance

- Use one FAB per screen in the common case.
- Prefer the extended variant when the icon alone is ambiguous.

## Nearby alternatives

- Local action inside content -> `Button`
- Several primary shortcuts -> rethink the screen; do not stack FAB semantics

## Common mistakes

- Using FAB for generic toolbar shortcuts.
- Giving a screen multiple unrelated FABs.

## Official source

- https://developer.android.com/develop/ui/compose/components/fab
