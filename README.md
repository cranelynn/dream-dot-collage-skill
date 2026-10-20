# Dream Dot Collage Skill

A focused image-generation Skill for making a dream-core collage from **one reference photo at a time**.

## Visual signature

- One large circle with a clean, solid-color interior.
- Two to five independent photo cutouts taken from the same source image.
- Clean white die-cut borders that follow each subject's silhouette.
- A minimal line-art sleeping puppy.
- Delicate hand-drawn paths, stars, moons, tiny dots, and optional handwritten labels.
- A cohesive palette, editorial layering, and a rich-but-controlled scrapbook feeling.

## The most important rule

**One reference image = one independent output.** Never fuse content from separate uploaded photos. Multiple cutouts are welcome only when they all come from the same selected photo. If the user supplies several photos, process each separately.

## Real extraction is required

The Skill explicitly distinguishes cutouts from crops. A cutout must have its background removed and a silhouette that follows the subject; a rectangle, circle crop, or original photo used as a background does not qualify. If the active image model cannot guarantee accurate extraction, use a dedicated masking/compositing workflow where available and disclose limitations.

## Repository structure

- SKILL.md — core instructions and required workflow.
- references/visual-direction.md — mood, palette, lines, and texture.
- references/composition-rules.md — hierarchy, layering, and spacing.
- references/photo-extraction.md — extraction and source-fidelity rules.
- references/negative-constraints.md — failure modes to reject.
- references/quality-checklist.md — final acceptance gates.
- examples/prompt-template.md — reusable generation prompt.
- examples/example-cases.md — two separate example plans based on the selected travel photos.

## Example cases

The two chosen reference photos are intended as **two independent demos**, not as ingredients for a single collage:
1. **Dolomites mountain village** — extract the mountain ridge, church/village cluster, and one small natural detail from that photo only.
2. **Gothic cathedral with a visitor** — extract the visitor and selected architectural details from that photo only.

The repository currently contains the case plans and prompt template. Finished before/after image assets still need to be added before these can be presented as fully visual demos.

## How to use

1. Select one photo.
2. Inspect and isolate 2–5 meaningful elements from that photo.
3. Compose those cutouts around a solid-color circle with white borders and a few fine doodles.
4. Run the quality checklist and revise if the cutouts are not real, independent silhouettes.

This repository provides prompt and composition guidance. Results depend on the image model and tools available in the host application.

## Design principle

**Rich in detail, clear in hierarchy.** The photo-derived elements carry the personal memory; the circle, puppy, lines, and tiny labels provide a consistent visual system without replacing the source photo.

## License

This project is licensed under the MIT License. See LICENSE.
