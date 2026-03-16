# Android Compose UI

A comprehensive skill for building Android user interfaces with Jetpack Compose. Provides structured guidance for component selection, screen architecture, adaptive layouts, theming, accessibility, testing, and performance optimization.

## What it covers

This skill helps agents work effectively with:

- **Material 3 Components** - Choosing and implementing the right components for your UI
- **Screen Architecture** - State ownership, navigation boundaries, and composition patterns
- **Adaptive Layouts** - Responsive designs that work across phone, tablet, and foldable form factors
- **Theming & Design Systems** - Material 3 theming, dynamic color, and custom design systems
- **Accessibility** - Semantics, traversal order, screen reader support, and advanced accessibility patterns
- **Testing Strategy** - Compose UI testing, semantics debugging, and interoperability with Espresso/UiAutomator
- **Performance** - Recomposition hygiene, stable parameters, and optimization patterns

## How it works

The skill uses a **routing-based architecture** that matches your request to the most relevant guidance:

1. **Classify** - Identifies which category your request falls into from the taxonomy
2. **Route** - Points to specific reference documents and decision matrices
3. **Guide** - Provides actionable recommendations with alternatives when relevant
4. **Guard** - Watches for common anti-patterns and Compose-specific pitfalls

## Request Taxonomy

The skill recognizes these types of requests:

- `component-choice` - Selecting between Material 3 components
- `screen-architecture` - Structuring screens and managing state
- `layout-adaptive` - Building responsive layouts for different screen sizes
- `theming-design-system` - Theming decisions and design system integration
- `accessibility-review` - Ensuring accessibility compliance and best practices
- `testing-strategy` - Testing approaches and debugging techniques
- `performance-review` - Identifying and fixing performance issues

## Quick Reference

### Decision Matrices

Quick guides for common decisions:

- **Component Selection** - `references/decision-matrices/component-selection-matrix.md`
- **Screen Architecture** - `references/decision-matrices/screen-architecture-decision-tree.md`
- **Adaptive Navigation** - `references/decision-matrices/adaptive-navigation-matrix.md`
- **Accessibility Checklist** - `references/decision-matrices/accessibility-review-checklist.md`
- **Testing Playbook** - `references/decision-matrices/testing-playbook.md`
- **Performance Smells** - `references/decision-matrices/performance-smells.md`
- **API Review** - `references/decision-matrices/composable-api-review-checklist.md`

### Foundation References

Deep dives into core concepts:

- **Composable API Design** - `references/foundations/composable-api-design.md`
- **State & Stability** - `references/foundations/stability-and-state-exposure.md`
- **Text System** - `references/foundations/text-system-architecture.md`
- **Material 3 Theming** - `references/foundations/material3-theming.md`
- **View Interop** - `references/foundations/view-interop.md`
- **Effects & Lifecycles** - `references/foundations/effects-and-state-lifecycles.md`

### Screen Design Guides

Patterns for building screens:

- **Adaptive Layout** - `references/screen-design/adaptive-layout.md`
- **Navigation Patterns** - `references/screen-design/navigation-patterns.md`
- **Screen Patterns** - `references/screen-design/screen-patterns.md`
- **Layouts & Modifiers** - `references/screen-design/layout-and-modifiers.md`
- **Window Insets** - `references/screen-design/window-insets-and-ime.md`
- **Focus & Input** - `references/screen-design/focus-and-input-patterns.md`

### Quality References

Guidance for building high-quality UI:

- **Accessibility** - `references/quality/accessibility.md`
- **Advanced Accessibility** - `references/quality/advanced-semantics-and-accessibility-review.md`
- **Testing** - `references/quality/testing.md`
- **Testing & Debugging** - `references/quality/compose-ui-testing-and-semantics-debugging.md`
- **Performance** - `references/quality/performance.md`
- **Animation** - `references/quality/animation-and-motion.md`

### Component References

Specific component guidance in `components/`:

- Actions: `buttons.md`
- Navigation: `navigation-bar.md`, `navigation-rail.md`, `navigation-drawer.md`, `tabs.md`, `segmented-button.md`
- Containers: `scaffold.md`, `bottom-sheet.md`, `dialog.md`
- Input: `text-fields.md`, `search-bar.md`
- Feedback: `snackbar.md`

## Default Principles

When working with this skill, the agent will:

- Prefer `MaterialTheme` tokens over hard-coded styling
- Use state down, events up, with state hoisted to the lowest common owner
- Respect project wrappers and existing design-system layers
- Call out experimental or version-sensitive APIs explicitly
- Preserve repo conventions for state, previews, theming, testability, and accessibility

## Guardrails

The skill watches for these common issues:

- Passing `NavController` directly into destination composables
- Overusing `CompositionLocal` for screen-level dependencies
- Reading fast-changing state too early in composition
- Choosing navigation by personal preference instead of window conditions
- Hard-coded styling instead of theme tokens
- Missing semantics, weak testability, or unstable broad parameters

## Response Pattern

For each request, the skill provides:

1. **Best recommendation** - The strongest fit for your situation
2. **Why it fits** - Explanation of the reasoning
3. **Closest alternative** - If the distinction matters
4. **Key implementation note** - Critical detail for implementation
5. **Key quality note** - Accessibility, testing, or performance consideration when relevant

## Repository

`juanfranem/android-skills`

This skill lives in the `android-compose-ui/` directory of the repository.

## Philosophy

- **Material 3 First** - Prefer Material 3 components unless the project has specific replacements
- **Minimal Reading** - Only read the files that match the specific request
- **Practical Guidance** - Focus on actionable patterns, not exhaustive documentation
- **Quality Conscious** - Accessibility and testing are first-class concerns
- **Platform Aware** - Understands Compose's unique characteristics compared to the View system
