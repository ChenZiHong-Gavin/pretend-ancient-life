# 同时代艺术媒介路由

Use this reference to decide how a historical transformation should look, not what its people owned or wore. Keep visual evidence separate from material-culture evidence.

## Contents

- [Choose the output mode](#choose-the-output-mode)
- [Keep two evidence lanes](#keep-two-evidence-lanes)
- [Select a visual anchor](#select-a-visual-anchor)
- [Translate the medium](#translate-the-medium-not-just-the-surface)
- [Match scene and evidence context](#match-scene-and-evidence-context)
- [Write the prompt block](#write-the-prompt-block)
- [Validate the result](#validate-the-result)
- [Routing examples](#routing-examples)

## Choose the output mode

| Mode | Use when | Visual rule |
|---|---|---|
| `period-artwork translation` | The user asks for a dynasty / period style, an ancient painting, or does not request realism | Use a scene-compatible visual medium that existed in the selected place and period |
| `reconstructed realism` | The user asks for a realistic photo, documentary reconstruction, or camera-like people | Use material evidence for historical content; do not fake a historical artwork surface |
| `creative interpretation` | Evidence is sparse or the user explicitly requests invention | State which parts are inferred and do not present the result as direct period evidence |

Do not drift into an unlabeled hybrid. Photographic faces with an aged-paper overlay are not a period artwork; historically dressed people in cinematic lighting are reconstructed realism, not a manuscript, mural, or handscroll.

## Keep two evidence lanes

| Evidence lane | Controls | Does not prove |
|---|---|---|
| Material culture: excavated objects, garments, buildings, technical studies, archives | Clothing construction, hair, tools, furniture, transport, architecture, technology, status | Historical line, palette, spatial grammar, or picture format |
| Contemporaneous visual culture: paintings, prints, murals, manuscripts, reliefs, vessels, photographs | Carrier, format, line, color, space, figure convention, surface, text placement | That every depicted object, body, costume, or ritual was ordinary daily life |

Use both lanes in period-artwork mode. A convincing brush style cannot repair anachronistic clothing; accurate objects do not by themselves create a Song painting, Edo print, Egyptian mural, or Victorian photograph.

## Select a visual anchor

1. Fix the target place, date range, social setting, scene type, and output mode.
2. Prefer an original or securely dated visual work from the same place and subperiod.
3. Prefer a subject with compatible scene logic: urban views for streets, domestic images for interiors, landscape formats for travel, portrait formats for close figures.
4. Check the work's carrier, intended audience, patronage, religious or funerary function, gender, class, and regional bias.
5. Record what is safe to extract and what is not. For example, extract line and spatial rhythm from a court scroll without assigning court dress to ordinary citizens.
6. Use this fallback ladder when an exact match does not survive:
   - same place and nearby date, compatible subject
   - connected region and same period, with the geographic difference stated
   - another contemporaneous medium from the same culture, with the format change stated
   - archaeologically grounded reconstructed realism
   - explicitly labeled creative interpretation
7. Never use a later revival, academic history painting, film still, tourist costume, fantasy illustration, or modern “retro” filter as silent primary evidence.

There is no universal acceptable year gap. State the source date and explain any gap that could change dress, technology, artistic convention, or political context.

## Translate the medium, not just the surface

Specify each applicable dimension in the prompt:

| Dimension | Questions to answer |
|---|---|
| Carrier | Silk, paper, plaster wall, stone relief, ceramic vessel, parchment, woodblock print, glass plate, or another actual support? |
| Format | Handscroll, hanging scroll, album leaf, mural register, vessel band, manuscript page, single-sheet print, photograph? |
| Line | Even fine outline, calligraphic modulation, incised contour, carved key line, hatching, brush mass? |
| Color | Ink, transparent wash, opaque mineral color, earth pigment, limited print palette, monochrome photograph? |
| Space | Continuous narrative, layered registers, oblique projection, ruled architecture, atmospheric recession, corner composition, optical perspective? |
| Figures | Profile or three-quarter view, scale by status, individualized portrait, repeated types, flat or modeled faces? |
| Surface | Woven silk, fibrous paper, plaster wear, vessel curvature, parchment, plate grain? Keep it subordinate to structural grammar. |
| Text | Which script and placement existed? If text is not essential, keep it absent or visually subordinate. |

Preserve the source photograph's people, relationships, focal hierarchy, and major geometry, but translate photographic perspective when the historical medium constructs space differently. Preserve recognizability, not anachronistic lens behavior.

## Match scene and evidence context

- Urban and commercial scenes: prefer city views, narrative scrolls, prints, maps, archival photographs, or architectural images with crowd and building logic.
- Domestic and family scenes: prefer household, genre, portrait, manuscript, mural, or excavated-interior evidence; do not inherit court luxury automatically.
- Landscape and travel: match panoramic, handscroll, album, print, or topographic conventions to the source crop and movement.
- Court and ceremony: use courtly media only for appropriate people and spaces; retain hierarchy and ritual function.
- Religious and funerary evidence: its visual grammar may be usable, but sacred gestures, afterlife objects, ideal bodies, and status scale require explicit limits.
- Periods with little surviving painting: use reliefs, vessels, manuscripts, textiles, sculpture, photography, or reconstructed realism. Do not invent a mature painting tradition merely to satisfy “ancient art.”
- Periods with photography: match the actual process, date, exposure logic, tonal range, posing, and print surface rather than applying a sepia filter.

## Write the prompt block

Include a compact block like this:

```text
Output mode: period-artwork translation.
Visual anchor: [dated work or medium], [place], [date], [carrier and format].
Extract: [line], [palette], [space], [figure convention], [surface], [text treatment].
Scene fit: [why this evidence suits the source scene].
Do not copy: preserve the source photo's composition; do not reproduce the anchor's composition or iconography.
Evidence boundary: [court / religious / funerary / elite / regional / later-copy limitation].
Material culture: source clothing, objects, buildings, and technology from the separate period brief.
```

For reconstructed realism, replace the visual-anchor block with the requested camera / documentary treatment and keep historical artwork only as secondary evidence, not as a surface style.

## Validate the result

Reject or retry when:

- the medium did not exist in the selected place and date
- a neighboring culture or later revival supplies the dominant style without disclosure
- the scene uses the wrong branch of a broad tradition, such as treating all Song scenes as one painting style
- only paper texture changed while anatomy, space, lens blur, or lighting remained modern-photographic
- the historical format no longer fits the source scene or crop and no translation rationale is given
- court, religious, funerary, or elite conventions are generalized to ordinary people
- the result copies a famous work's arrangement instead of the source photo's composition
- the prompt names a style but does not specify executable line, color, space, figure, and carrier rules

## Routing examples

- Song China: route an urban crowd to fine-line urban handscroll and ruled-architecture grammar, a Northern Song mountain scene to monumental layered recession, a Southern Song lyrical landscape to cropped album composition, and a close figure scene to period figure-painting conventions. “Song style” alone is insufficient.
- Edo Japan: route a merchant street to urban woodblock-print grammar, a domestic scene to an appropriate interior or illustrated-book convention, and travel to landscape-print grammar; do not make every person a samurai or entertainer.
- New Kingdom Egypt: funerary painting and temple relief provide strong contemporary visual grammar but biased contexts; use archaeological evidence separately for ordinary housing and tools.
- Classical Greece: painted pottery, relief, sculpture, and archaeological architecture are valid contemporary media; later Neoclassical oil painting is not direct Classical-period visual evidence.
- Victorian Britain: choose wet-plate, albumen print, engraving, illustrated press, or painting by exact decade and use case; sepia alone is not a process specification.
