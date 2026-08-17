# 示例：现代咖啡聚会 → 宋代园林茶叙

## 文件与来源

- 原图：`examples/china/song/tea-gathering/before.jpg`
- 生成图：`examples/china/song/tea-gathering/after.png`
- 第一版（因人物发式与衣襟过于现代而淘汰）：`examples/china/song/tea-gathering/after-v1.png`
- 来源：[Asian Friends Drinking Coffee in Cafe](https://www.pexels.com/photo/asian-friends-drinking-coffee-in-cafe-5709521/)
- 摄影：Sam Lion / Pexels
- 授权：[Pexels License](https://www.pexels.com/license/)

## 提示词

```text
Use case: precise-object-edit
Asset type: historical-accuracy correction for the Song-dynasty tea-gathering example
Input images: Image 1 is the current painted draft and the exact edit target. Image 2 is the original photograph and is used only to preserve the two women’s identities, poses, gestures, eye lines, and relationship.
Primary request: Correct only the two women’s hairstyles, garments, facial rendering, and tea ware so they read unmistakably as Southern Song figures. Keep the entire garden pavilion, bamboo, plantain leaves, railing, water, table placement, aged-silk surface, crop, and composition from Image 1 unchanged.
Hairstyles: Remove every modern hair signal. Both women’s black hair must be fully swept away from the forehead and neck and gathered into compact, clearly constructed Song-style coiled buns high at the back of the crown. Use a smooth center or near-center division at the hairline, no side-swept fringe, no pixie or bob silhouette, no loose bangs, no fluffy blow-dried volume, no dyed brown highlights, and no modern salon texture. Secure each bun with one restrained plain hairpin or small comb only; no floral bridal ornament.
Garments: Replace the bathrobe-like wrapped garments with historically legible Southern Song women’s layers. Each woman wears a narrow-sleeved, straight-front duijin beizi with two parallel vertical front edges and slim contrasting border bands, worn open over a cross-collar inner ru and the visible upper fold of a long full skirt. The beizi must not cross over the torso and must not be cinched like a modern robe. Use narrow cloth ties hidden or tied discreetly at the side, not a broad front sash. Keep the exact body poses and seated silhouettes.
Faces and painting language: Preserve each woman’s face shape, age, expression, and gaze from Image 2, but translate the faces completely into Southern Song fine-line figure painting: delicate continuous ink contours, shallow flat color washes, minimal cheek modeling, fine arched brows, understated eyes without eyeliner, and tiny restrained vermilion lips. Remove photographic skin shading, modern makeup, glossy highlights, hair-by-hair realism, and contemporary beauty-portrait styling. The women must look painted by the same hand as the silk album leaf, not like modern photographic faces pasted into an old setting.
Tea ware and gestures: Replace both vessels with small handleless black-glazed Jian tea bowls set on black-red lacquer tea stands. Preserve the exact raised drinking heights and the left woman’s supporting-hand gesture, but make every finger support the bowl or stand naturally from below; no finger may curl around or pass through an imaginary mug handle. Keep only a folded letter, cloth pouch, shallow celadon dish, and bamboo tea whisk on the table.
Historical visual anchors: Use the delicate figure outlines, layered garden shadows, and restrained coloring described for the National Palace Museum’s “Lady at the Mirror in the Embroidered Lattice” album leaf, and the Song garden, ladies, lacquer tea stand, tea bowl, and tea-vessel grammar documented in Zhao Bosu’s “Reading in an Open Hall.” Use them as visual grammar only; do not copy either composition.
Style/medium: authentic Southern Song gongbi figure album leaf, ink and pale mineral color on aged silk, fine even garment lines, restrained elegant coloring, flat integrated figures, no photographic depth of field.
Constraints: Change only the two women and tea objects. Preserve exactly two people, their identities, positions, expressions, eye lines, hands, drinking gestures, table edge, original 3:2 framing, garden architecture, foliage placement, water view, and daylight direction.
Avoid: modern bangs, side-parted short hair, bob or pixie silhouettes, brown salon highlights, loose modern hair, photographic faces, eyeliner, bathrobe or kimono silhouette, crossed V-neck outer robe, broad waist sash, generic theatrical hanfu, Tang court dress, Qing clothing, qipao, handled cups, imaginary cup handles, smartphone, watch, plastic, prominent writing, watermark, caption, border.
```

## 本次修订

- 第一版的问题：右侧人物保留现代侧分短发轮廓；两人的外衣形成浴袍式交叠 V 领；脸部明暗过于摄影化；茶盏手势仍像在握杯把。
- 第二版将修改范围限制在人物与茶具，并用故宫《绣栊晓镜图》和《风檐展卷》作为人物线描、庭园与茶器的视觉语法参考。
- 第二版人物造型通过，但左侧人物下方手里多出一只空漆托，因此进行一次只修改该物件的定向修补；修补前版本保留为 `after-v2.png`。

## 定向修补提示词

```text
Use case: precise-object-edit
Input images: Image 1 is the exact edit target.
Primary request: Change only the extra empty black-and-red lacquer tea stand held in the lower hand of the woman on the left. Replace that empty stand with one small, neatly folded plain silk handkerchief in muted cream, resting naturally across the same open palm.
Constraints: Keep absolutely everything else unchanged: both women’s faces, Song hairstyles, hairpins, straight-front beizi and inner robes, body poses, all hands and fingers, the two raised black-glazed Jian tea bowls with their lacquer stands, facial expressions, garden pavilion, bamboo, plantain leaves, railing, water, table objects, aged-silk texture, linework, palette, crop, and lighting. Do not move, redesign, repaint, or add any other element.
Avoid: extra bowl, extra tea stand, empty saucer, modern napkin, text, watermark, border.
```

## 主要替换

| 现代元素 | 宋代对应物 |
|---|---|
| 咖啡杯和亮色碟 | 宋代茶盏与青瓷或漆托 |
| 手机 | 折叠书信和小布囊 |
| T 恤、衬衫和长裤 | 褙子、襦裙与素色腰带 |
| 咖啡馆座椅 | 江南园林中的木构亭座 |
| 热带商业绿植 | 竹、芭蕉、湖石和庭院水景 |
