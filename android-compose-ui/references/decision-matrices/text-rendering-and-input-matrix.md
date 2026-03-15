# Text Rendering and Input Matrix

- `Text` -> default choice for app copy, theming, and Material-aligned display text.
- `BasicText` -> foundation display primitive when you intentionally own decoration or rendering behavior.
- `TextField` or `OutlinedTextField` -> default Material text input surfaces.
- `BasicTextField` -> low-level editing primitive when you need custom decoration and can own semantics carefully.
- Value-based text field -> legacy or compatibility path when state-based APIs are unavailable for the target stack.
- State-based text field -> preferred new architecture when `TextFieldState`, selection, and transformations should live together.
- `TextStyle` only -> whole-text styling.
- `AnnotatedString` with `SpanStyle` or `ParagraphStyle` -> mixed styling, links, or paragraph-specific formatting inside one text block.
- Autofill semantics matter -> add `contentType` semantics and treat the field as a production form element, not only a visual input.
