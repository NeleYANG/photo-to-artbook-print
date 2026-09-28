---
name: photo-to-artbook-print
description: Use when turning an uploaded photograph into a quiet handmade art-book illustration, small independent print, hand-printed keepsake, or restrained visual-journal artwork.
---

# Photo to Art-book Print

Transform the user's photograph into one finished 3:4 portrait illustration with a compact painted footprint and generous page-level negative space. Preserve the scene's identity while simplifying its rendering.

## Input and tool choice

- Require the intended reference photograph to be visible in the conversation. If it is missing or no longer available, ask the user to attach it again; do not invent the scene.
- Use the built-in image-generation tool in edit/reference mode. For a local image, inspect it with `view_image` first. Include the smallest number of recent images that contains every intended reference.
- Generate immediately when the request is otherwise clear. Do not return only a rewritten prompt.

## Build the generation prompt

Label the request as `Use case: style-transfer` and identify every input image as a scene-and-subject reference. Carry forward any explicit user additions, then include all of these requirements:

```text
Create a single finished illustration in a 3:4 portrait format. Use the supplied photograph only as reference; do not reproduce or display the photograph in the final output.

Redraw the most recognizable subjects and key elements as a small handmade print-like illustration centered on warm, lightly textured paper. Keep the illustrated footprint compact with generous negative space. Preserve essential silhouettes, natural human proportions, poses, characteristic hairstyles, clothing, gestures, objects, and spatial relationships. Keep people recognizable but simplified; use minimal, understated facial features rather than cartoon features.

Use uneven pen lines, opaque acrylic-like color shapes, dry-brush traces, broken pigment coverage, irregular painted edges, and subtle hand-printed texture. Derive four to six principal colors from the photograph. Keep them restrained and slightly muted while preserving important source color relationships.

Reduce the background to a few loose marks, flat color patches, or incomplete shapes. Do not fully render the environment. Simplify incidental detail without adding new narrative elements.

Use no title or place name unless the user supplied the exact text. Never invent a location, name, date, or caption. If exact text is supplied, keep it discreet and omit it when the user asks for no text.

Output only one finished illustration. No original-photo panel, photographic element, split layout, contact sheet, or before-and-after comparison.

Avoid photorealistic painting, polished vector art, glossy 3D rendering, watercolor washes, gouache washes, crayon, colored pencil, pastel, waxy strokes, children's-book styling, cute cartoon proportions, anime, busy decoration, large headings, logos, signatures, and watermarks.
```

## Validate before returning

Check the result for: one image only; 3:4 portrait composition; no source-photo panel; recognizable subjects and relationships; compact artwork with ample paper; four to six source-derived colors; opaque print-like media; incomplete background; and no invented text. If one constraint clearly fails, make one targeted correction while repeating all invariants.

Return the final image directly. Mention the tool used and saved path only when the surrounding environment requires it.
