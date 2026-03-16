# Advanced Semantics and Accessibility Review

## When to read this
- You are reviewing a custom component that needs more than default Compose accessibility.
- You need to decide when advanced semantics justify the added complexity.
- You want to optimize spoken output, traversal order, or gesture substitutes for complex UI.
- You are building custom progress indicators, sliders, or composite controls.
- TalkBack or VoiceOver users report confusing or incomplete announcements for your custom UI.

## Core decisions
- Use advanced semantics only when Compose defaults create gaps in the spoken model.
- Prefer explicit semantics modifiers over `clearAndSetSemantics` unless you are completely replacing the accessibility subtree.
- Group related elements when the logical unit differs from the visual layout.
- Treat custom component review as an accessibility contract: define what assistive technologies will announce, not just what appears on screen.
- Test with actual screen readers regularly; semantic correctness does not guarantee a good user experience.
- Document your accessibility contract for custom components so future maintainers understand the intended behavior.

## Recommended patterns
- Use `liveRegion` for dynamic content that must interrupt or queue announcements (e.g., form errors, status changes).
- Add `paneTitle` when a screen region represents a distinct navigation destination or modal surface.
- Apply `stateDescription` for toggle or custom control states not captured by standard roles.
- Use `progressBarRangeInfo` for custom progress indicators so screen readers announce value and bounds correctly.
- Provide `customActions` when standard gestures are insufficient; keep labels concise and actions reversible.
- Merge semantics for container-like components only when children should be announced as a single unit.
- Use `traversalIndex` sparingly to correct order when visual and logical sequences diverge significantly.
- Hide decorative elements with `invisibleToUser()` rather than leaving empty semantics nodes.
- Validate semantics changes with TalkBack or VoiceOver on real devices, not just the IDE preview.
- Test edge cases like rapid state changes and screen rotation to ensure announcements remain coherent.

## Avoid
- Adding semantics to every element "just in case."
- Overriding semantics in ways that remove useful state or role information from assistive technologies.
- Using `clearAndSetSemantics` as a quick fix for complex layouts instead of restructuring composition.
- Hardcoded traversal orders that break when content changes or localization adjusts text length.
- Assuming that matching platform behavior is sufficient; Compose accessibility differs from View system patterns.
