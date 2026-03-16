# Android Skills

A collection of specialized skills for building Android applications with modern frameworks and best practices.

## Overview

This repository contains domain-specific skills designed to help AI coding agents work effectively on Android projects. Each skill provides structured guidance, decision matrices, and best practices for specific aspects of Android development.

## Skills

### android-compose-ui

Comprehensive guidance for building Android user interfaces with Jetpack Compose and Material 3.

**Covers:**
- Material 3 component selection and implementation
- Screen architecture and state management
- Adaptive layouts for phones, tablets, and foldables
- Theming and design system integration
- Accessibility (semantics, traversal, screen readers)
- Testing strategy (Compose testing, semantics debugging, Espresso/UiAutomator interop)
- Performance optimization and recomposition hygiene

**Key Features:**
- Routing-based architecture matching requests to relevant guidance
- 7 request taxonomies: component-choice, screen-architecture, layout-adaptive, theming-design-system, accessibility-review, testing-strategy, performance-review
- Decision matrices for quick reference
- Foundation references for deep dives
- Component-specific guidance
- Guardrails against common anti-patterns

**Location:** `android-compose-ui/`

## Repository Structure

```
android-skills/
├── android-compose-ui/
│   ├── SKILL.md                          # Main skill definition and router
│   ├── README.md                         # Skill documentation
│   ├── components/                       # Component-specific guidance
│   │   ├── buttons.md
│   │   ├── scaffold.md
│   │   ├── navigation-bar.md
│   │   └── ...
│   ├── references/
│   │   ├── decision-matrices/            # Quick decision aids
│   │   ├── foundations/                  # Core concept deep dives
│   │   ├── quality/                      # Testing, accessibility, performance
│   │   └── screen-design/                # Layout and navigation patterns
│   └── assets/                           # Images, diagrams, etc.
└── README.md                             # This file
```

## How Skills Work

Each skill in this repository follows a consistent structure:

1. **SKILL.md** - The entry point that defines the skill's purpose, taxonomy, routing table, and guardrails
2. **README.md** - Human-readable documentation explaining what the skill covers
3. **references/** - Detailed guidance organized by topic
4. **components/** - Specific component implementations and patterns
5. **assets/** - Supporting visual materials

## Using These Skills

These skills are designed to be used by AI coding agents (like Claude, Cursor, or similar) when working on Android projects. The agent reads the SKILL.md file to understand how to route requests and then follows the references to provide specific guidance.

### For Developers

When working with an AI agent on Android code:

1. **Reference the skill** - Mention which area you're working on (e.g., "I'm building a Compose UI with navigation")
2. **Be specific** - The skills work best with concrete requests (e.g., "Help me choose between BottomNavigation and NavigationRail for a tablet layout")
3. **Let the agent route** - The skill's routing table will point the agent to the most relevant guidance

### For Skill Authors

To create or modify skills:

1. Follow the existing structure (SKILL.md, README.md, references/, components/)
2. Keep guidance actionable and specific
3. Include decision matrices for common choices
4. Add guardrails against known anti-patterns
5. Test with real Android projects to ensure relevance

## Philosophy

- **Framework-first** - Prefer modern Android frameworks (Compose, Material 3) unless legacy constraints exist
- **Practical over theoretical** - Focus on patterns that work in production
- **Quality-conscious** - Accessibility, testing, and performance are first-class concerns
- **Platform-aware** - Understand Android's unique characteristics (lifecycle, configuration changes, window insets)
- **Minimal but complete** - Provide just enough guidance to be useful without overwhelming

## Contributing

Skills are living documents. To contribute:

1. Test changes with real Android projects
2. Ensure guidance aligns with current best practices
3. Update decision matrices when new patterns emerge
4. Add examples for complex scenarios
5. Document breaking changes or version-sensitive APIs

## Future Skills

Planned additions:

- **android-architecture** - MVVM, MVI, repository patterns, data layer
- **android-testing** - Unit testing, integration testing, test doubles
- **android-performance** - Profiling, memory management, startup optimization
- **android-security** - Secure storage, network security, encryption
- **android-background** - WorkManager, foreground services, notifications

## Repository

`juanfranem/android-skills`

## License

MIT License - See LICENSE file for details
