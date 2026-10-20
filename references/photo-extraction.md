# Photo Extraction Rules

## Source boundary
Use exactly one source photo for each output. If multiple photos are provided, handle them as separate jobs. Never mix a person from one photo with scenery or objects from another.

## Choose elements
Select 2–5 recognizable elements from the selected photo. Examples include a person, a mountain ridge, a church, a flower, a distinctive building detail, or a memorable object. Prioritize meaningful and visually distinct shapes.

## What counts as a cutout
A valid cutout has the original background removed and a silhouette that follows the subject. It may have transparent pixels around the silhouette and a white die-cut border added later.

These do not count:
- A rectangular crop with the original background intact.
- A circular crop of the whole photo.
- A full photo placed inside a large circle.
- A newly generated lookalike that replaces the source subject.

## Preferred technical process
1. Create a foreground mask or segmentation for each chosen element.
2. Refine edges around hair, branches, fine architecture, and other complex contours.
3. Preserve the original subject pixels wherever possible.
4. Export each isolated element with transparency when the workflow supports it.
5. Add a white outline following the mask silhouette, not the rectangle of the image canvas.
6. Inspect the cutout on both light and dark backgrounds to find halos and leftover background fragments.

## Fidelity
Preserve identity-defining features, face shape, hairstyle, clothing, pose, proportions, and distinctive colors. Do not invent unseen details or reconstruct hidden portions of people or objects. If an element is too small or obscured to extract faithfully, omit it.

## Composition handoff
Pass isolated elements to the composition stage as separate assets. Arrange them around a solid-color circle; do not merge them back into a full scene. Keep photo cutouts photographic and recognizable while puppy art, symbols, and lines remain illustrated.

## Tool limitations
Some generative image models imitate the appearance of cutouts but do not perform pixel-accurate segmentation. When exact source fidelity matters, use a dedicated background-removal or image-editing tool. Be transparent about limitations; never label a crop as a successful background removal.
