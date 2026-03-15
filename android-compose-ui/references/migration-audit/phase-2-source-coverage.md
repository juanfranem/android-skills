# Phase 2 Source Coverage

## Primary sources

### STYLE_GUIDELINES.md
- default arguments vs overloads -> migrated -> `android-compose-ui/references/foundations/composable-api-design.md`
- named arguments and call-site clarity -> migrated -> `android-compose-ui/references/foundations/composable-api-design.md`
- trailing lambdas and slot placement -> migrated -> `android-compose-ui/references/foundations/composable-api-design.md`
- receiver scopes and DSL boundaries -> migrated -> `android-compose-ui/references/foundations/composable-api-design.md`
- state parameters and hoisting expectations -> migrated -> `android-compose-ui/references/foundations/stability-and-state-exposure.md`
- modifier parameter conventions -> migrated -> `android-compose-ui/references/foundations/composable-api-design.md`
- naming and reusable composable API design -> migrated -> `android-compose-ui/references/foundations/composable-api-design.md`
- stability and evolution concerns -> migrated -> `android-compose-ui/references/foundations/stability-and-state-exposure.md`

### TEXT.md
- text primitives vs Material text APIs -> migrated -> `android-compose-ui/references/foundations/text-system-architecture.md`
- typography and text style boundaries -> migrated -> `android-compose-ui/references/screen-design/text-and-typography.md`
- annotated text and mixed styling -> migrated -> `android-compose-ui/references/screen-design/text-and-typography.md`
- paragraph behavior, overflow, and line limits -> migrated -> `android-compose-ui/references/screen-design/text-and-typography.md`
- modern text-field state and transformations -> migrated -> `android-compose-ui/references/foundations/text-system-architecture.md`
- text interaction and selection -> migrated -> `android-compose-ui/references/decision-matrices/text-rendering-and-input-matrix.md`
- font strategy -> migrated -> `android-compose-ui/references/screen-design/text-and-typography.md`
- autofill and production-form integration -> migrated -> `android-compose-ui/references/decision-matrices/text-rendering-and-input-matrix.md`

### TOUCH_INPUT.md
- input abstraction levels: components vs modifiers vs raw pointer APIs -> migrated -> `android-compose-ui/references/decision-matrices/input-abstraction-matrix.md`
- focus traversal and focus groups -> migrated -> `android-compose-ui/references/screen-design/focus-and-input-patterns.md`
- keyboard, D-pad, mouse, and large-screen input expectations -> migrated -> `android-compose-ui/references/screen-design/focus-and-input-patterns.md`
- programmatic focus and traversal overrides -> migrated -> `android-compose-ui/references/decision-matrices/focus-and-traversal-checklist.md`
- scrolling, dragging, and gesture boundaries -> migrated -> `android-compose-ui/references/quality/interaction-and-gesture-review.md`
- interaction feedback and `InteractionSource` -> migrated -> `android-compose-ui/references/quality/interaction-and-gesture-review.md`
- drag-and-drop or clipboard-adjacent interaction concerns if clearly durable -> migrated -> `android-compose-ui/references/quality/interaction-and-gesture-review.md`

### ANIMATIONS.md
- choosing the right animation API -> migrated -> `android-compose-ui/references/decision-matrices/animation-api-selection.md`
- visibility/content/size transitions -> migrated -> `android-compose-ui/references/quality/animation-and-motion.md`
- property animations and multi-value transitions -> migrated -> `android-compose-ui/references/decision-matrices/animation-api-selection.md`
- gesture-coupled animation and lower-level motion primitives -> migrated -> `android-compose-ui/references/quality/animation-and-motion.md`
- shared transitions and navigation-related motion -> migrated -> `android-compose-ui/references/decision-matrices/animation-api-selection.md`
- animation testing and tooling -> migrated -> `android-compose-ui/references/quality/animation-and-motion.md`

## Secondary sources

### MATERIAL.md
- Gap filled: tonal elevation, emphasis hierarchy, and `*Defaults` customization heuristics -> `android-compose-ui/references/foundations/material3-theming.md`

### DESIGN.md
- Gap filled: none -> already covered by `android-compose-ui/references/screen-design/layout-and-modifiers.md`, `android-compose-ui/references/screen-design/adaptive-layout.md`, `android-compose-ui/references/screen-design/navigation-patterns.md`, and `android-compose-ui/references/screen-design/screen-patterns.md`

### GRAPHICS.md
- Gap filled: image, painter, canvas, draw-modifier, and graphics-layer selection plus image performance guidance -> `android-compose-ui/references/screen-design/images-and-graphics.md`
