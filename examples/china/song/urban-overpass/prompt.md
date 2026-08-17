# 示例提示词：广州街景 → 宋代市井

## 示例文件

- 原图：`examples/china/song/urban-overpass/before.jpg`
- 生成图：`examples/china/song/urban-overpass/after.png`
- 原图来源：[Urban Street Scene in Guangzhou, China](https://www.pexels.com/photo/urban-street-scene-in-guangzhou-china-35144760/)
- 摄影：Bingqian Li / Pexels
- 授权：[Pexels License](https://www.pexels.com/license/)（允许免费使用和修改；署名非强制）

## 提示词（英文）

```text
Use case: style-transfer
Asset type: before/after showcase image for the “pretend ancient life” project
Input image: Image 1 is the edit target. Preserve its landscape crop, camera position, perspective, large sweeping overhead structure, road geometry, foreground subject placement, stairs, background depth, and dramatic backlighting.

Primary request: Transform the entire modern Guangzhou street photograph into a historically coherent Northern Song dynasty urban street scene rendered as a refined gongbi ink-and-color painting on aged silk.

Subject and element conversion:
- Convert the central foreground electric-scooter rider into a Song-dynasty traveler or courier riding a donkey toward the viewer, preserving the rider’s exact scale, location, direction, posture, and long cast shadow.
- Convert every car and scooter into period-appropriate ox carts, donkey carts, horses, handcarts, or walking townspeople, keeping approximately the same traffic positions and visual rhythm.
- Convert the huge concrete overpass into a monumental timber covered bridge or elevated wooden gallery with tiled eaves, following the same sweeping diagonal silhouette and occupying the same portion of the frame.
- Convert the metal staircase and railings on the right into timber stairs and carved wooden balustrades leading to that bridge.
- Convert modern concrete and glass buildings into dense Song timber-frame shops, inns, and multi-story pavilions with tiled roofs; transform the tall glass structure at right into a timber pavilion while keeping its height and mass.
- Convert asphalt into rain-darkened stone paving, retaining the bright reflected light and shadow pattern.
- Replace streetlights, road signs, traffic barriers, and commercial signage with paper lantern posts, wooden plaques, shop banners, and understated calligraphic signs. Any writing should be minimal, plausible brush calligraphy, and not prominently legible.

Style/medium: authentic Song-dynasty gongbi and jiehua urban painting, ink and subdued mineral color on silk, fine-line brushwork, delicate architectural ruling, elegant literati restraint, visual atmosphere reminiscent of Zhang Zeduan’s urban scroll painting.
Composition/framing: exactly retain the source’s 3:2 horizontal framing, wide-angle street perspective, foreground/middle/background hierarchy, strong diagonal bridge, and central rider as focal point.
Lighting/mood: preserve the source’s luminous late-afternoon backlight, bright road reflection, deep foreground shade, and long shadows, translated into layered pale ink washes rather than photographic contrast.
Color palette: muted ochre, indigo, celadon, warm gray, pale mineral green, restrained red accents.
Materials/textures: visible aged silk weave, subtle hand-painted ink contours and mineral-pigment granulation.

Constraints: This must look like one coherent surviving Song dynasty silk painting, not a photo with a filter. Preserve the original composition and spatial relationships while replacing all anachronistic objects.
Avoid: all cars, motor vehicles, scooters, helmets, concrete, steel guardrails, glass curtain walls, electrical equipment, modern street markings, modern logos, modern typography, photorealism, neon colors, fantasy architecture, Qing-dynasty costumes, watermark, captions, borders.
```

## 元素替换清单

| 现代元素 | 宋代对应物 |
|---|---|
| 电动车与骑手 | 骑驴的行旅或信使 |
| 汽车 | 牛车、驴车、马匹和行人 |
| 混凝土高架桥 | 木构廊桥或架空游廊 |
| 金属楼梯与护栏 | 木梯与木质栏杆 |
| 玻璃及混凝土建筑 | 木构商铺、客栈和楼阁 |
| 柏油路 | 雨后石板路 |
| 路灯、路牌与现代招牌 | 灯笼、木牌和幌子 |
