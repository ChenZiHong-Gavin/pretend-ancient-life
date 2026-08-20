---
name: pretend-ancient-life
description: Transform modern photos into historically grounded images or production-ready prompts for specific places and periods worldwide, using scene-appropriate contemporaneous art when an ancient-art result is wanted while preserving composition, people, gestures, and scene meaning. Use when the user asks to 把照片变成某个朝代或历史时期、穿越到古代、生成古画版照片、按宋画或其他同时代艺术风格转换, convert a modern scene to Han/Tang/Song China, Edo Japan, Mughal India, ancient Egypt, Greece, Rome, medieval Europe, another world-history period, or create historically routed before/after concepts.
---

# Pretend Ancient Life

Turn a modern photograph into a coherent historical scene. Preserve what makes the source recognizable while replacing anachronisms according to function. Route by historical place and date; never treat `foreign`, `ancient`, `Asian`, `African`, or `medieval` as a complete visual setting.

## Route the place and period

1. Resolve four dimensions: historical place, approximate date, political or cultural unit, and local social setting.
2. Read [references/index.md](references/index.md) when any dimension is broad, missing, or ambiguous.
3. Read exactly one relevant regional catalog, then the single best detailed period reference:
   - [China](references/regions/china.md)
   - [East Asia outside China](references/regions/east-asia.md)
   - [South and Southeast Asia](references/regions/south-southeast-asia.md)
   - [Central Asia, West Asia, and North Africa](references/regions/central-west-asia-north-africa.md)
   - [Europe and the Mediterranean](references/regions/europe.md)
   - [Sub-Saharan Africa](references/regions/sub-saharan-africa.md)
   - [Americas](references/regions/americas.md)
   - [Oceania](references/regions/oceania.md)
4. Use `dynasty` only where the relevant historiography does. Else use period, empire, kingdom, city-state, archaeological culture, or local community.
5. Route a year by its intersection with place. Account for simultaneous polities: a twelfth-century scene may be Song, Liao, Jin, Western Xia, Goryeo, Khmer, Fatimid, or another setting depending on location.
6. Do not map modern borders backward without explanation. Use the historical city, region, polity, or culture in the prompt and retain the modern place only as a geographic aid.
7. When the user gives only a broad label, offer two well-separated candidates with dates and one-sentence visual differences. If the user requests immediate generation, state a conservative default explicitly.

## Respect support levels

- `reviewed`: use the detailed reference directly and apply its validation rules.
- `baseline`: use the detailed reference, verify decisive clothing / architecture / object details against authoritative collections, and label the result as a baseline reconstruction.
- `catalogued`: do not improvise an accurate reconstruction. Research the period first or offer an explicitly creative interpretation.

For a `catalogued` period, build a compact temporary brief from at least two authoritative sources when browsing is available:

1. Use the regional catalog row's `contemporaneous visual media research lead` to scope queries, not as verified evidence or a ready-made style.
2. Prefer a local museum, archaeological service, archive, cultural institution, descendant-community source, or primary collection record.
3. Add a chronological or comparative source such as a major museum timeline or scholarly publication.
4. Record the exact date range, historical geography, evidence types, evidence bias, clothing, built environment, transport, daily objects, writing system, contemporaneous visual media, and easy anachronisms.
5. Separate surviving material evidence from later artistic depictions. Do not use a revival painting, film costume, tourist reconstruction, colonial image, or restricted cultural image as silent primary evidence.
6. Use [references/_template.md](references/_template.md) when turning repeated research into a new bundled reference.

## Route the output mode and visual medium

1. Choose an output mode before writing the image prompt:
   - `period-artwork translation`: default when the user asks for a dynasty / period style, an ancient painting, or gives no contrary medium request
   - `reconstructed realism`: use when the user asks for a photograph, documentary reconstruction, realistic people, or camera-like rendering
   - `creative interpretation`: use only when evidence is insufficient or the user explicitly wants invention; label it clearly
2. Maintain two separate evidence lanes:
   - material-culture evidence controls clothing, hair, objects, buildings, transport, technology, and social status
   - contemporaneous visual evidence controls carrier, format, line, color, spatial construction, figure conventions, surface, and text treatment
3. For `period-artwork translation`, select a dated visual medium from the same place and period that fits the scene. “Song painting,” “Edo art,” or “medieval manuscript” is still too broad; route urban, landscape, portrait, domestic, court, religious, and funerary scenes separately.
4. Treat the carrier and viewing format as part of the style. A handscroll, album leaf, mural, painted vessel, manuscript illumination, woodblock print, and early photograph organize space differently; do not apply them as surface filters over unchanged photographic rendering.
5. Use a named work as a visual anchor only after checking date, place, subject, carrier, and evidence context. Extract its grammar; never copy its composition or treat elite, religious, or funerary imagery as universal daily life.
6. If no close contemporaneous visual source survives, follow the fallback ladder and disclose the gap. Never silently substitute a later revival style.
7. Read [visual-medium-routing.md](references/visual-medium-routing.md) whenever using period artwork, resolving sparse visual evidence, or reviewing a possible medium mismatch.

## Transform the image

1. Inspect every edit target with the available image-viewing tool before prompting.
2. Record invariants:
   - crop and aspect ratio
   - camera position, perspective, and depth
   - number, placement, pose, gesture, and facing direction of prominent people
   - identity-defining facial and body features when faces are visible
   - dominant light direction, weather, reflections, and shadows
   - visual role of major structures and objects
3. Inventory modern elements by function: transport, electronics, clothing, architecture, infrastructure, text, furniture, packaging, and materials.
4. Apply the routed output mode. For period artwork, translate the source composition into the selected historical carrier and spatial grammar; for reconstructed realism, keep camera-like perspective and lighting while using historically grounded material culture.
5. Replace modern elements by semantic function:
   - preserve travel with local period travel, commerce with local period commerce, communication with local period communication, and public infrastructure with an analogous structure
   - delete an element only when no plausible analogue exists and removal will not break the composition
   - correct a person's hand gesture whenever a held device is removed
6. Build a structured prompt with: use case, edit target, canonical historical setting, output mode, material-culture evidence, visual anchors and their limits, subject conversion, environment conversion, carrier / medium, scene grammar, composition invariants, lighting, palette, text handling, constraints, and avoid list.
7. If the user asks only for a prompt, return the English production prompt, a short Chinese explanation, the modern-to-historical mapping table, and any historical uncertainty.
8. If the user asks for an image, follow the installed `imagegen` skill and use its edit path. Generate one call per asset, inspect the result, and make at most one targeted retry for a concrete defect unless the user asks for variants.

## Prompt rules

- Use the source image as an edit target, not loose inspiration.
- Repeat composition and identity invariants near the end of the prompt.
- Use local, dated material and construction terms; avoid generic phrases such as `ancient Chinese style`, `African tribal`, `Oriental`, or `generic medieval costume`.
- State city or region, century or reign, social role, output mode, carrier, and visual medium when these affect the result.
- In period-artwork mode, name the executable grammar: line, palette, spatial construction, figure convention, surface, and format. A dynasty label alone is not a style specification.
- Treat named artworks as evidence for medium and scene grammar, not permission to copy their composition or proof that all people lived as depicted.
- Do not combine photographic skin, lens blur, volumetric cinematic light, or modern anatomical rendering with a historical medium unless the user explicitly requests a labeled hybrid.
- Preserve recognizable people unless anonymization is requested. In stylized media, preserve face shape, hairstyle silhouette, age, pose, and relationships rather than promising pixel identity.
- Remove modern logos and typography. Use historically correct scripts only when necessary and visually subordinate; prominent pseudo-writing is a defect.
- Match status: ordinary people should not acquire royal regalia, priestly objects, ceremonial armor, or elite architecture without a reason.
- Preserve local diversity and colonial context. Do not replace Indigenous or local material culture with the style of a contemporary empire merely because that empire claimed the region.

## Validate the result

Reject or retry when any major check fails:

- modern vehicles, electronics, power lines, road paint, logos, contemporary type, plastics, or inappropriate glass and concrete remain
- clothing, hair, transport, architecture, writing, and props do not agree on place, date, and social setting
- a neighboring culture, later revival, fantasy genre, film costume, or tourist cliché has replaced the selected period
- the chosen visual medium is later than, foreign to, or incompatible with the selected place, date, scene, or output mode without an explicit rationale
- a historical carrier is present only as texture while faces, perspective, lighting, and depth remain conspicuously photographic
- one famous artwork has been copied compositionally or generalized beyond its court, religious, funerary, gender, class, or regional evidence boundary
- prominent people drift in count, placement, pose, facing direction, identity, or relationships
- removed devices leave broken hand gestures
- animals, limbs, wheels, stairs, boats, furniture, and building joints are implausible
- source spatial relationships, aspect ratio, focal hierarchy, light direction, and major shadows are no longer recognizable, unless a documented historical-medium translation intentionally changes optical perspective or shadow logic
- evidence known only from royal, religious, or funerary contexts is presented as universal daily life
- signs contain prominent garbled writing
- uncertainty is hidden for a `baseline` or newly researched period

When retrying, request one concrete correction and repeat every invariant that must remain unchanged.

## Save results

Use descriptive lowercase slugs; never create a `foreign/` bucket.

- image: `output/images/<place>/<period>/<source-stem>-<period>.png`
- prompt: `output/prompts/<place>/<period>/<source-stem>-<period>.md`
- curated prompt example: `examples/<place>/<period>/prompt.md`, or `examples/<place>/<period>/<scene-slug>/prompt.md` for multiple scenes
- local before / after images may sit beside a prompt for review but remain Git-ignored

Record source URL, creator, license, final prompt, transformation map, output mode, visual anchors, support level, evidence limitations, and intentional simplifications for externally sourced examples.

## Add a period

Copy [references/_template.md](references/_template.md), add the period to the correct regional catalog and [references/index.md](references/index.md), and cite authoritative local or specialist sources. Document material evidence and contemporaneous visual evidence separately. Start at `baseline`; promote to `reviewed` only after a realistic prompt and generated result have been inspected for historical, medium, and visual defects.
