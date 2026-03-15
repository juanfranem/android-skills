# Search Bar

## Use when

- Search is a first-class interaction and the surface needs query, expansion, and suggestions/results behavior.

## Core APIs

- `SearchBar`
- `SearchBarDefaults.InputField`
- `query`
- `onQueryChange`
- `expanded`
- `onExpandedChange`
- `onSearch`

## Guidance

- Prefer this over styling a plain text field like search when search behavior is substantial.
- Configure semantics carefully if the search UI has rich suggestion content.

## Important note

- Official docs mark this API as experimental. Mention `@OptIn(ExperimentalMaterial3Api::class)` when relevant.

## Official source

- https://developer.android.com/develop/ui/compose/components/search-bar
