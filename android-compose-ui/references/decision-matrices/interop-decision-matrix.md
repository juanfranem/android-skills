# Interop Decision Matrix

- Pure Compose -> Use this when the feature can be expressed with Compose primitives, state, semantics, and performance are already good enough, and no legacy View capability is required.
- Wrap an existing View -> Use `AndroidView` or `AndroidViewBinding` when one specific View-based widget or SDK surface is still needed and the wrapper can stay narrow.
- Embed Compose in a View host -> Use `ComposeView` when an existing View screen is the current shell and Compose is being adopted incrementally inside that host.
- Postpone or avoid interop altogether -> Prefer this when the interop layer would spread View concepts across the feature, hide ownership, or cost more than replacing the UI directly.
- If state ownership is unclear, do not add interop until one side of the boundary is the clear source of truth.
- If lifecycle cleanup, semantics, or performance cost are hard to explain, keep the adapter smaller or avoid the bridge.
