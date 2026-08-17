---
name: pretend-ancient-life
description: Transform modern photos into historically grounded ancient-life images or production-ready image prompts while preserving composition, people, gestures, and scene meaning. Use when the user asks to 把照片变成某个朝代、穿越到古代、生成古画版照片、convert a modern scene to an ancient era, or create before/after examples for Han, Tang, Song, Yuan, Ming, or Qing China.
---

# Pretend Ancient Life

Turn a modern photograph into a coherent historical scene. Preserve what makes the source recognizable while replacing anachronisms according to their function, not by a fixed word-for-word mapping.

## Route the era

1. Read [references/index.md](references/index.md) when the requested era is missing, ambiguous, or broader than one dynasty.
2. Read exactly one primary era reference unless the user explicitly requests a comparison:
   - [Han](references/china/han.md)
   - [Tang](references/china/tang.md)
   - [Song](references/china/song.md)
   - [Yuan](references/china/yuan.md)
   - [Ming](references/china/ming.md)
   - [Qing](references/china/qing.md)
3. Do not improvise a supposedly accurate unsupported era. State what is supported and offer either a clearly labeled creative interpretation or a new researched reference.

## Workflow

1. Resolve the target culture, dynasty, subperiod, location, social setting, and desired medium. Ask only when a missing choice would materially change the result; otherwise use the era reference default and state it in the prompt.
2. Inspect every edit target with the available image-viewing tool before prompting.
3. Record invariants before making replacements:
   - crop and aspect ratio
   - camera position, perspective, and depth
   - number, placement, pose, gesture, and facing direction of prominent people
   - identity-defining facial and body features when faces are visible
   - dominant light direction, weather, reflections, and shadows
   - the visual role of major structures and objects
4. Inventory modern elements by category: transport, electronics, clothing, architecture, infrastructure, text, furniture, packaging, and materials.
5. Choose one coherent scene mode from the era reference. Do not mix court portraiture, literati landscape, tomb mural, and street-scroll conventions in one image unless the reference explicitly permits it.
6. Replace each modern element by semantic function:
   - preserve travel with period travel, commerce with period commerce, communication with period communication, and public infrastructure with an analogous period structure
   - delete an element only when no plausible analogue exists and its removal will not break the composition
   - change a person's hand gesture when removing a device; never leave a pose that visibly expects a missing object
7. Build a structured prompt with these useful fields: use case, edit target, historical setting, subject conversion, environment conversion, style/medium, composition invariants, lighting, palette, text handling, constraints, and avoid list.
8. If the user asks only for a prompt, return the English prompt, a short Chinese explanation, and the element mapping table.
9. If the user asks for an image, follow the installed `imagegen` skill and use its built-in edit path by default. Generate one call per requested asset, inspect the result, and make at most one targeted retry for a concrete defect unless the user asks for more variants.
10. Save project-bound results non-destructively:
    - normal outputs: `output/images/<culture>/<era>/<source-stem>-<era>.png`
    - archived prompts: `output/prompts/<culture>/<era>/<source-stem>-<era>.md`
    - curated examples: use `examples/<culture>/<era>/before.jpg`, `after.png`, and `prompt.md` when the era has one example; when it has multiple examples, use `examples/<culture>/<era>/<scene-slug>/before.jpg`, `after.png`, and `prompt.md`
11. Record the source URL, creator, license, final prompt, transformation map, and any intentional historical simplification for every externally sourced example.

## Prompt rules

- Use the image as an edit target, not merely as loose inspiration.
- Repeat invariants near the end of the prompt to reduce composition drift.
- Use historically meaningful material and construction terms; avoid the generic phrase `ancient Chinese style`.
- Preserve recognizable people unless the user requests anonymization. In highly stylized media, preserve face shape, hairstyle silhouette, age, pose, and relationships rather than promising pixel-level identity.
- Remove modern logos and typography. Prefer blank or visually subordinate plaques when exact historical text is unnecessary; image-model pseudo-writing is a defect when it becomes a focal point.
- Keep roof curvature and ornament proportional to the selected period. Do not use exaggerated fantasy eaves, palace architecture for ordinary homes, or mixed-dynasty costume shorthand.
- Treat named artworks as visual references for medium and scene grammar, not as permission to copy a whole composition.

## Validate the result

Reject or retry when any major check fails:

- no modern vehicles, electronics, glass curtain walls, power lines, road paint, logos, or contemporary type remain
- clothing, hair, transport, architecture, and props belong to the same dynasty and social setting
- prominent people retain their count, placement, pose, facing direction, and relationships
- removed devices do not leave broken hand gestures
- animals, limbs, wheels, stairs, boats, and building joints are structurally plausible
- source perspective, aspect ratio, focal hierarchy, light direction, and major shadows remain recognizable
- signs contain no prominent garbled writing
- the image reads as the selected medium rather than a photographic filter
- the output and prompt are saved in the requested project location with provenance

When retrying, request one concrete correction and repeat all invariants that must stay unchanged.

## Add another era

Copy [references/_template.md](references/_template.md), research authoritative museum or archaeological sources, add the new reference to [references/index.md](references/index.md), and add a realistic example under `examples/<culture>/<era>/`. Mark an era supported only after its reference and at least one prompt have been reviewed.
