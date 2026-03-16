# Accessibility Semantics Review Checklist

- Review spoken labels: each interactive element announces a clear, concise purpose without duplication.
- Review announced state: checked, selected, expanded, error, loading, and disabled states are communicated appropriately.
- Review grouping: logically related elements are grouped so assistive technologies present them as coherent units.
- Review traversal order: focus sequence matches the intended task flow and reading order.
- Review actions and gesture substitutes: custom gestures have accessible alternatives via `customActions` or visible controls.
- Review progress and error announcements: dynamic changes use `liveRegion` or equivalent to notify users without stealing focus.
- Review scalable content: text remains readable and touch targets remain usable when font sizes increase.
- Review semantics overrides: confirm that hiding or clearing semantics does not remove essential information from assistive technologies.
