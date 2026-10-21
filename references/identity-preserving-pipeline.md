# Identity-Preserving Cutout Pipeline

## Principle
For photos containing people, do not regenerate faces or people with a text-to-image model. Keep the original pixels.

## Minimum reproducible approach
1. Select exactly one uploaded source image and record its dimensions.
2. Generate a mask for each selected element. Refine using a foreground/background segmentation tool (such as OpenCV GrabCut) or a carefully traced mask.
3. For a person, include their whole visible silhouette and keep their original face pixels untouched. Do not upscale using generative face restoration.
4. Create RGBA cutouts: RGB must come straight from the source photograph; alpha is the mask.
5. Expand the mask by a few pixels to add a white die-cut silhouette border.
6. Render a solid background and solid dream circle as separate graphic layers.
7. Add illustration-only assets (sleeping dog, moon, stars, thin paths, optional little labels) on different layers.
8. Composite photo cutouts as-is, using simple uniform scale and translation. No AI redraw of the cutouts or aesthetic face retouching.
9. Verify face fidelity with a before/after crop at matched scale, recognizing that JPEG conversion or scaling can change pixel values. For strict identity requirements, include the unmodified original crop for verification.
10. Check all elements came from exactly one source image per output.

## Failure behavior
If segmentation or compositing tools are absent, explain that this generation-only environment cannot guarantee original face pixels. Never present a generated lookalike as faithful extraction. A face-preservation violation blocks release of a demo.

## Visual finish
Use consistent thin white borders following alpha contours; avoid borders around rectangular image patches. Keep the circle a flat color, allow a few small source cutouts, simple puppy line art, purposeful doodle lines and tiny editorial labels.

## Demo policy
Do not commit uploaded private photographs or derived portraits to a public repository unless the owner explicitly approves publishing those specific images. The user's request to use images for a demo allows preparation, not automatic public publication before reviewing the output.

## Zero-defect face acceptance test

- Never run generative enhancement, synthesis, inpainting, skin smoothing or restoration on face, hair, or body pixels.
- Inspect original and final face crops at matched scale, including eyes, nose, mouth, cheek, jaw, hairline, and glasses if present.
- Compare final image against the original mask-cropped RGB layer. Unexpected black marks, dark patches, smudges, discoloration, wrong facial structure, or missing details are automatic release blockers.
- Prefer source-only RGB composite with premultiplied or correctly handled alpha to avoid dark halo and black-edge artifacts.
- Keep die-cut borders outside the foreground mask. Do not draw decorative marks across faces.
- If automated masking cannot preserve exact appearance, stop and request manual mask refinement; do not substitute a generative lookalike.
- Publish no before/after demo until the user has explicitly approved the exact resulting image.
