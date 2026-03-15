# Performance Smells

- Broad unstable parameters: pass smaller stable values and callbacks instead.
- Missing keys: add stable item keys when lazy content identity matters.
- Composition-phase reads for fast-changing state: move the read to a later phase or narrower scope.
- Theme bypasses: replace repeated ad hoc styling with theme tokens or shared defaults.
