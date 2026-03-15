# Text and Typography

## When to read this
- The task is about typography choices, readable text-heavy screens, mixed styling, or form-text presentation in Compose UI.

## Core decisions
- Use typography tokens and text styles intentionally so screens stay readable across hierarchy, density, and localization.
- Treat inline styling, paragraph behavior, and constrained layout as separate tools with different readability tradeoffs.
- Prefer production font strategies that include fallbacks and version-aware caveats when advanced font features are involved.

## Recommended patterns
- Use `TextStyle` for whole-text presentation and reserve `SpanStyle` plus `ParagraphStyle` for ranges that truly need mixed inline or paragraph treatment.
- Reach for `AnnotatedString` when one block needs mixed emphasis, clickable spans, or multiple paragraph segments rather than stacking many tiny text nodes.
- Tune readability with `lineHeight`, locale-aware alignment such as `TextAlign.Start`, appropriate line-break settings, and explicit `maxLines` plus overflow behavior when space is constrained.
- Use `LineBreak.Paragraph` and optional hyphenation for body copy, and simpler strategies for headings or live editing where stability matters more than polish.
- Build app typography from `FontFamily` resources or downloadable fonts with fallbacks, and treat variable-font usage as version- and device-sensitive rather than universal.
- Keep text-heavy forms readable by balancing typography, line limits, and overflow rules instead of relying only on decoration or truncation.

## Avoid
- Using paragraph-level tools when the problem is only a simple whole-text style change.
- Letting overflow, line count, or font-loading defaults silently decide readability on dense screens.
- Treating advanced font loading or variable fonts as risk-free without device fallback planning.
- Breaking text into many composables when one annotated text block better preserves reading flow and semantics.
