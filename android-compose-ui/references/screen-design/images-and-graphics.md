# Images and Graphics

## When to read this
- The task is about choosing between `Image`, `Icon`, `Painter`, `Canvas`, draw modifiers, `graphicsLayer`, or image/graphics performance tradeoffs in Compose UI.

## Core decisions
- Use the highest-level visual primitive that matches the job: iconography, media display, decorative drawing, or full custom graphics.
- Keep a clear boundary between content rendering, decoration, and layer transformation.
- Treat image size, accessibility, and draw-cost decisions as product-quality concerns, not finishing polish.

## Recommended patterns
- Use `Icon` for semantic single-color iconography that should follow Material defaults, and `Image` for general media, richer rendering, or shape-aware content presentation.
- Use `Painter` when the drawable behavior belongs to the content itself and may need reusable rendering or measurement-aware logic.
- Use `Canvas` when the composable is fundamentally a drawing surface, and draw modifiers when you are augmenting an existing composable with backgrounds, overlays, masks, or cached effects.
- Use `graphicsLayer` for composable-level transforms such as translation, scale, rotation, or transform-origin changes rather than hand-rolling those effects in draw code.
- Add meaningful `contentDescription` for semantic images and pass `null` for purely decorative ones.
- Keep image assets close to display size, use loaders that resize and cache remote or large images, and remember that `painterResource()` does not automatically downscale a huge asset to the visible bounds.

## Avoid
- Using `Icon` when the content is actually rich image content that needs `Image` behavior.
- Treating draw-time transforms as if they changed layout or hit targets.
- Recreating expensive brushes, paths, or other draw objects every frame when `drawWithCache` fits.
- Shipping image-heavy UI without checking bitmap size, accessibility semantics, and modifier order for clipping, borders, or shadows.
