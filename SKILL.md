---
name: dream-dot-collage
description: Create a dream-core photo-cutout collage from exactly one reference image, with white die-cut borders, delicate doodle lines, tiny handwritten labels, a solid-color dream circle, and a minimal sleeping puppy. Never merge separate reference photos.
---

# Dream Dot Collage

Create a polished, richly detailed travel-journal-style dream collage. The visual language combines real photo cutouts, white sticker-like borders, fine hand-drawn lines, small handwritten labels, and a calm sleeping puppy around one large solid-color circle.

## Non-negotiable rules

1. **One source image per output.** Each reference photo must be processed independently. Never combine people, architecture, landscapes, objects, or visual details from different uploaded photos into one result. If the user provides several images, create one output per image or ask which one to process first.
2. **Multiple cutouts from one photo are allowed.** A single photo may yield 2–5 separate elements, such as a person, mountain ridge, church, flower, building detail, or distinctive object. All extracted photo elements in one result must come from that same source image.
3. **Cut out first, compose second.** Isolate the selected elements from their original background before designing the collage. Do not use the full source photo as a circular background, rectangular panel, or large scenic area.
4. **A cutout must actually look cut out.** It needs a silhouette that follows the subject and a removed/transparent background, optionally finished with a clean white die-cut border. A rectangular crop, circular crop, or full photo with its original background still attached does not count as a cutout.
5. **Preserve source fidelity.** Keep the person's identity, face, pose, proportions, clothing, and defining details recognizable. Do not invent hidden body parts or architectural details. If exact pixel-level extraction is unavailable in the image-generation environment, disclose that limitation and use a dedicated masking/compositing workflow where possible; never claim precise extraction that did not occur.
6. **The dream circle stays graphic.** Use one large solid-color circle or an almost-flat fill. Never fill it with the original photo, a scenic panorama, or a mini collage of landscapes.
7. **Rich but art-directed.** White cutout edges, thin hand-drawn paths, orbit lines, tiny stars, moons, dots, hearts, and a few handwritten words are encouraged. Keep clear hierarchy and intentional spacing; do not decorate every empty area.
8. **Original design, not imitation.** Use the general principles in this Skill; do not reproduce a specific artist's signature composition or copy an existing artwork.

## Identity-preserving production mode (mandatory for people)

For a source photo containing a person, **do not send their face or body through a generative redraw stage**. Pixel-preserving extraction and layer compositing are mandatory for any claim of identity fidelity:

1. Read the single selected source photo and create a foreground segmentation mask for the person (manual polygon, GrabCut, or reliable segmentation).
2. Apply the mask to the original photo pixels to create an RGBA cutout. Do not reconstruct or inpaint the face, hair, limbs, or clothing.
3. Add the white outline using mask dilation or the alpha channel, never by asking a model to redraw the subject.
4. Generate or draw the dog, circle, stars, lines, and labels separately from the person's pixel layer.
5. Composite the original RGBA cutout on top of the graphic background with image tools. The final face-region pixels must originate in the provided photo, except for explicit user-requested recoloring.
6. If accurate extraction is not feasible, **do not regenerate a lookalike**. Explain the problem, use a smaller faithful crop with clear labeling if the user accepts it, or choose non-person cutouts. A pretty but identity-altered result is a failure.
7. For demo acceptance, inspect original and output faces side by side. Do not upload an unapproved visual demo to the public repository.

See [Identity-preserving implementation](references/identity-preserving-pipeline.md).

## Required workflow

### Stage A — inspect and extract
1. Inspect the one selected photo and identify its main subject and distinctive supporting details.
2. Choose 2–5 elements that are visually meaningful and feasible to isolate. Avoid extracting every object.
3. Remove the background from each chosen element using a mask, segmentation, or background-removal tool when available.
4. Check the isolated elements against the source for identity, pose, shape, color, and proportions.
5. Reject cutouts that still carry large pieces of the original background or have been inaccurately reconstructed.

### Stage B — compose the artwork
1. Use a warm-white, cream, pale blue, or other source-compatible clean background.
2. Place one large solid-color circle as the main graphic field.
3. Arrange the isolated photo cutouts as separate elements inside, across, or around the circle. Do not reconstruct the original scene from the cutouts.
4. Add a restrained white die-cut outline to each photographic cutout. The border follows the subject silhouette, not a rectangle around its former background.
5. Place a small, simple line-art sleeping puppy near the circle's edge or below it.
6. Add a few fine doodles—an orbit path, stars, a moon, small dots, or a tiny paper crane/candy illustration—only where they help the composition.
7. Optionally add 1–3 tiny handwritten labels or short words. Keep them secondary and avoid long text or prominent titles.
8. Check that the result feels visually full of discoveries but not chaotic.

## Default composition
- One large solid-color circle.
- 2–5 independent photo cutouts from the same reference image.
- White die-cut borders around the photo cutouts.
- One small sleeping puppy drawn with simple, delicate lines.
- A few fine hand-drawn lines and tiny symbols.
- Optional 1–3 short handwritten labels.
- One cohesive palette guided by the source photo; purple is optional, never mandatory.
- One finished image per source image.

## Hard quality gates
Do not deliver the result if any of these fail:
- Two separate reference photos have been fused.
- The full original photo appears as the circle fill or a large background panel.
- No element is visibly isolated from its original background.
- Cutouts are merely rectangular crops or retain the source scene around them.
- The main subject is distorted or no longer recognizable.
- The circle is not a clean solid-color graphic field.

## Avoid
Full-photo circle fills, rectangular photo panels, cross-image fusion, fake cutouts, altered faces, invented source details, thick cartoon borders, excessive glitter/glow, forced purple palettes, random sticker clutter, an over-detailed puppy, and large unrequested text.

## Supporting references
- [Visual direction](references/visual-direction.md)
- [Composition rules](references/composition-rules.md)
- [Photo extraction](references/photo-extraction.md)
- [Negative constraints](references/negative-constraints.md)
- [Quality checklist](references/quality-checklist.md)
- [Prompt template](examples/prompt-template.md)
- [Example case plans](examples/example-cases.md)
