# Dream Dot Collage Skill

A focused image-generation Skill for turning **one reference photo into one restrained dream-core collage**.

The visual signature:
- A minimal line-art puppy sleeping peacefully.
- One large dream circle with a clean, solid-color interior.
- A small number of isolated cutouts extracted from the same reference photo.
- A few quiet symbolic details, such as candy, origami cranes, stars, or a single orbit line.
- Editorial spacing, a controlled palette, and a dreamy atmosphere without visual clutter.

## Core rule

**One reference image = one independent output.** Never blend content from multiple reference images into one collage. If a user provides several images, treat each as a separate task or ask which single image to process first.

## Files

- `SKILL.md` — primary Skill instructions and workflow.
- `references/visual-direction.md` — mood, palette, line work, and texture.
- `references/composition-rules.md` — hierarchy, spacing, and placement.
- `references/photo-extraction.md` — source fidelity and cutout handling.
- `references/negative-constraints.md` — failure modes to avoid.
- `references/quality-checklist.md` — final quality gate.
- `examples/prompt-template.md` — reusable generation prompt template.

## How to use

1. Provide one reference image.
2. Ask for a Dream Dot Collage treatment.
3. Keep the main subject recognizable and select only a few supporting details from that image.
4. Generate one finished composition, then refine only the elements that fail the quality checklist.

This repository provides prompt and composition guidance. The actual image-generation capability depends on the model or application in which the Skill is used.

## Design principles

**Quiet, not empty. Dreamlike, not chaotic. Source-faithful, not a generic sticker collage.**

The circle is a graphic color field, not a window onto another scene. Photo-derived elements remain separate, small, recognizable accents. The puppy and symbols create a dream narrative while generous negative space keeps the image composed.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE).
