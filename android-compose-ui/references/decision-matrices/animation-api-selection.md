# Animation API Selection

- Show or hide content -> `AnimatedVisibility`.
- Replace one content tree with another -> `AnimatedContent`; use `Crossfade` when a simple fade is enough.
- Animate one value from state -> `animate*AsState`.
- Animate several values from one state transition -> `updateTransition`.
- Animate layout growth or shrinkage -> `Modifier.animateContentSize()`.
- Need gesture coupling, interruption, `snapTo`, or decay -> `Animatable`.
- Need bounded or repeating motion -> `repeatable`, `infiniteRepeatable`, or `rememberInfiniteTransition` depending on whether the motion should stop.
- Need cross-screen continuity -> shared transitions, but treat `sharedElement()` and `sharedBounds()` as experimental or version-sensitive and verify target-stack support.
