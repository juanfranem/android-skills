---
name: android-compose-ui
description: Use this whenever the agent or a subagent is working on Android UI in Jetpack Compose and needs to choose, compare, implement, review, or explain Compose UI structure, Material 3 components, screen architecture, adaptive layout, theming, accessibility, testing, or performance-sensitive UI behavior.
---

# Android Compose UI

Use this skill as a compact router for Jetpack Compose UI work. Keep the main skill short, read only the files that match the request, and prefer `androidx.compose.material3` unless the project already wraps or replaces it.

## Default stance

- Prefer `MaterialTheme` tokens over hard-coded styling.
- Prefer state down, events up, and hoist state to the lowest common owner.
- Respect project wrappers, existing design-system layers, and established accessibility patterns.
- Call out experimental or version-sensitive APIs explicitly.

## Request taxonomy

- `component-choice`
- `screen-architecture`
- `layout-adaptive`
- `theming-design-system`
- `accessibility-review`
- `testing-strategy`
- `performance-review`

## Workflow

1. Classify the request with the taxonomy above.
2. Read the smallest matching reference set.
3. Read component docs only when the question depends on a concrete Material 3 component family.
4. Recommend the strongest fit first and mention alternatives only when the distinction matters.
5. Preserve repo conventions for state, previews, theming, testability, and accessibility.

## Routing table

- Component comparisons, nearby Material 3 families, or ambiguous UI choices -> `references/decision-matrices/component-selection-matrix.md`
- State ownership review, hoisting decisions, or ambient dependency questions -> `references/decision-matrices/screen-architecture-decision-tree.md`
- Adaptive navigation choice across window conditions -> `references/decision-matrices/adaptive-navigation-matrix.md`
- Accessibility QA pass -> `references/decision-matrices/accessibility-review-checklist.md`
- Quick UI test planning -> `references/decision-matrices/testing-playbook.md`
- Quick smell scan for Compose performance issues -> `references/decision-matrices/performance-smells.md`
- Composable API review, slot design, defaults, or `modifier` contract questions -> `references/decision-matrices/composable-api-review-checklist.md`, `references/foundations/composable-api-design.md`, or `references/foundations/stability-and-state-exposure.md`
- Text structure, typography, or annotated text choices -> `references/foundations/text-system-architecture.md` or `references/screen-design/text-and-typography.md`
- Text input model choice, autofill concerns, or state-based field migration questions -> `references/decision-matrices/text-rendering-and-input-matrix.md` or `references/foundations/text-system-architecture.md`
- Focus order, keyboard or D-pad behavior, and large-screen interaction review -> `references/screen-design/focus-and-input-patterns.md` or `references/decision-matrices/focus-and-traversal-checklist.md`
- Pointer input versus gesture modifiers, or interaction-feedback review -> `references/decision-matrices/input-abstraction-matrix.md` or `references/quality/interaction-and-gesture-review.md`
- Animation API choice, shared-transition caveats, or motion review -> `references/decision-matrices/animation-api-selection.md`, `references/decision-matrices/motion-review-checklist.md`, or `references/quality/animation-and-motion.md`
- Image, icon, painter, canvas, or graphics-layer choice -> `references/screen-design/images-and-graphics.md`
- Screen architecture, state ownership, navigation boundaries, or `CompositionLocal` use -> `references/foundations/compose-ui-architecture.md`
- Compose theming, color roles, typography, shapes, dynamic color, or design-system boundaries -> `references/foundations/material3-theming.md`
- Effect APIs, restart keys, state retention, or lifecycle-driven side effects -> `references/foundations/effects-and-state-lifecycles.md`
- Adaptive layout, panes, window size classes, or large-screen navigation -> `references/screen-design/adaptive-layout.md`
- Layout primitives, modifier order, lazy containers, or custom layout escape hatches -> `references/screen-design/layout-and-modifiers.md`
- Common screen types such as forms, settings, search, feeds, or UI state surfaces -> `references/screen-design/screen-patterns.md`
- App navigation structure, tabs, segmented controls, pane navigation, or route boundaries -> `references/screen-design/navigation-patterns.md`
- Accessibility review or semantics concerns -> `references/quality/accessibility.md`
- UI testing strategy, semantics-first assertions, or Compose test APIs -> `references/quality/testing.md`
- Recomposition hygiene, stable parameters, or performance smells -> `references/quality/performance.md`

## Component routing

- Read the matching file in `components/` only after the reference routing above narrows the problem.
- Common destinations: actions -> `components/buttons.md`, screen shell -> `components/scaffold.md`, top-level navigation -> `components/navigation-bar.md`, `components/navigation-rail.md`, or `components/navigation-drawer.md`, peer sections -> `components/tabs.md`, local mode switches -> `components/segmented-button.md`, feedback -> `components/snackbar.md`, sheets and dialogs -> `components/bottom-sheet.md` or `components/dialog.md`, text and search input -> `components/text-fields.md` or `components/search-bar.md`.
- If the UI pattern is not obvious, resolve it through the decision matrices first and then open the closest component file.

## Cross-cutting guardrails

- Watch for passing `NavController` directly into destination composables.
- Watch for overusing `CompositionLocal` for screen-level dependencies.
- Watch for reading fast-changing state too early in composition.
- Watch for choosing navigation by personal preference instead of window conditions.
- Watch for hard-coded styling instead of theme tokens.
- Watch for missing semantics, weak testability, or unstable broad parameters.

## Response pattern

1. Best recommendation
2. Why it fits
3. Closest alternative if the distinction matters
4. Key implementation note
5. Key accessibility, testing, or performance note when relevant
