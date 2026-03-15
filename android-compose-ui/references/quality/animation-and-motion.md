# Animation and Motion

## When to read this
- The task is about choosing Compose animation patterns, reviewing motion architecture, or deciding when lower-level motion control is justified.

## Core decisions
- Start with the highest-level animation API that matches the UI change.
- Prefer state-driven motion for visibility, replacement, and property changes; use lower-level orchestration only when interaction or choreography truly requires it.
- Treat shared transitions and other evolving motion APIs as experimental or version-sensitive when the target stack has not stabilized them yet.

## Recommended patterns
- Use `AnimatedVisibility`, `AnimatedContent`, `Crossfade`, or `animateContentSize()` when the problem is content presence, replacement, or size change rather than free-form choreography.
- Use `animate*AsState` for one property and `updateTransition` when several values should move together under one state change.
- Reach for `Animatable` when motion must be interrupted, snapped, decayed, or driven by gestures and coroutine timing.
- Keep gesture-coupled animation in three phases: direct manipulation during input, release evaluation, and settle-to-target or decay after release.
- Make animation testing deterministic with `ComposeTestRule.mainClock` and improve tooling visibility with labels on transitions and animated values.
- Call out experimental or version-sensitive APIs explicitly, especially for shared transitions, navigation-coupled motion, or other unstable animation surfaces.

## Avoid
- Reaching for a lower-level API when a visibility, content, or value animation already models the problem.
- Letting automated motion keep fighting live user input instead of yielding and resuming intentionally.
- Hiding version-sensitive animation choices behind generic guidance that sounds more stable than the APIs actually are.
- Treating testing and tooling as optional after motion is already complex or flaky.
