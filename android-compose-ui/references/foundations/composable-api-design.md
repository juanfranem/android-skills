# Composable API Design

## When to read this
- The task is about designing or reviewing a reusable composable API.

## Core decisions
- Prefer explicit, idiomatic Kotlin-first Compose APIs over overload-heavy or bag-of-options designs.
- Put the ownership model in the signature so callers can see defaults, state, slots, and customization points without reading implementation.
- Treat `modifier` placement, slot order, and naming as part of the API contract, not cosmetic details.

## Recommended patterns
- Prefer default arguments over overloads when the behavior is still one API with a small set of optional knobs.
- Keep named-call clarity high: choose parameter names that read well at the call site and avoid long runs of positional booleans or nullable pseudo-defaults.
- Order parameters as required values first, then `modifier: Modifier = Modifier`, then optional parameters, then the primary trailing composable lambda.
- Use a trailing `content` lambda for the main slot and add scoped receivers such as `RowScope` only when the scope communicates real layout affordances or DSL boundaries.
- Prefer slots and thin wrapper composables over style bags when callers need structural freedom or branded variants.
- Expose customization through explicit parameters or defaults objects when values are broadly reusable and theme-like.
- Name `Unit`-returning composables as `PascalCase` entities, value-returning composables with normal function naming, and remembered factories with a `remember` prefix.
- Decide early whether the API should emit UI or return a value; if it emits, keep control surfaces in parameters or hoisted state rather than mixing emit-and-return behavior.

## Avoid
- Adding overloads for every optional combination when default parameters already describe the contract.
- Hiding major behavior behind nullable sentinels, internal-only defaults, or component-specific `CompositionLocal` reads.
- Placing slots before key structural parameters or using DSL-style lambdas when a simple content slot is enough.
- Passing state containers as a shortcut when the better API is explicit values, callbacks, or a focused hoisted state type.
