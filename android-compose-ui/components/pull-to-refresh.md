# Pull To Refresh

## Use when

- A scrollable surface should support manual refresh through downward drag.

## Core APIs

- `PullToRefreshBox`
- `isRefreshing`
- `onRefresh`
- `indicator`

## Guidance

- Wrap the scrollable content and connect it to a real refresh state.
- Use a custom indicator only when the default does not fit the product.

## Important note

- Official docs mark this API as experimental. Mention `@OptIn(ExperimentalMaterial3Api::class)` when relevant.

## Official source

- https://developer.android.com/develop/ui/compose/components/pull-to-refresh
