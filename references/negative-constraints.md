# Negative Constraints

Reject or revise the result if any hard failure appears.

## Source integrity
- Content from two or more reference photos appears in one result.
- A person, building, or object has been altered enough to lose recognizable source details.
- The model invents hidden features or fills missing regions without support.

## Fake extraction
- The full source image is used as the circle fill or as a large scenic background.
- A supposedly extracted element still contains its original rectangular background.
- The image only crops the photo into a circle or rectangle.
- White borders surround a rectangular image canvas rather than following the subject silhouette.
- A generated lookalike is substituted for the source subject.

## Circle misuse
- The circle contains a photo, landscape, room, or detailed panorama.
- The circle is visually lost among competing elements.
- Too many objects fill the circle's interior.

## Clutter and weak hierarchy
- Every gap is decorated.
- Lines, labels, stars, and symbols compete with the photo cutouts.
- All cutouts are the same size or arranged mechanically.
- The output resembles an unstructured sticker sheet rather than a designed composition.

## Style drift
- Thick cartoon outlines, heavy glow, lens flare, glitter overload, metallic effects, or excessive 3D rendering.
- A forced purple/neon palette unrelated to the source.
- The puppy is over-detailed or becomes the main subject.
- Large unrequested text, illegible paragraphs, watermarks, or logos appear.

## Output format
- A grid or multi-panel image is generated when one output was requested.
- Separate source photos are fused rather than processed independently.
