# 维多利亚伦敦：现代路口 → 1875 年蛋白照片

## 目标与支持等级

- Canonical setting：`europe/victorian-britain`
- 地点与年代：伦敦商业街区，约 1875 年
- 视觉媒介：湿版火棉胶玻璃底片转蛋白相纸
- 支持等级：`baseline`
- 本地文件：`before.jpg`、`after.png`（由 `.gitignore` 排除）

## 原图来源

- 摄影者：Maggie Ramirez
- 页面：[Street in London](https://www.pexels.com/photo/street-in-london-17906166/)
- 授权：[Pexels License](https://www.pexels.com/license/)

## 最终 Prompt

```text
Edit the provided modern London photograph into a historically grounded central London street scene in the mid-Victorian period, circa 1875, presented as an albumen print made from a wet-plate collodion glass negative. This is an exact source-photo edit.

Preserve the original tall portrait crop and aspect ratio, eye-level street-corner viewpoint, strong diagonal row of monumental stone commercial buildings rising along the right, darker building edge at left, open sky in the upper left, curved street in the lower middle, cluster of pedestrians in the lower right, lone figure near the lower left, central traffic/vehicle focal area, long afternoon light from the right, and deep foreground shadows. Keep the same perspective and massing.

Convert all pedestrians into plausible Londoners of varied working and middle-class status in 1870s clothing: men in shirts, waistcoats, long coats and trousers with bowler, top, or soft felt hats; women in high-necked bodices, long skirts with restrained early-bustle silhouettes, shawls or small bonnets. Preserve their positions, walking directions, and group relationships. Replace the cyclist with a walking messenger or period pedestrian beside a simple parcel handcart while preserving the left-side silhouette.

Replace the modern double-decker bus at center with a horse-drawn London omnibus of comparable visual mass and position, with anatomically plausible horses partly visible. Replace traffic lights, Underground roundels, road markings, CCTV, modern lamp posts, signs, steel barriers, and bollards with cast-iron gas lamps, a restrained painted omnibus-stop or shop board, iron railings, stone curbs, and cobbled or macadam street surfaces. Turn modern metal scaffolding and white plastic sheeting into period timber scaffolding with canvas covers. Retain the stone façades where plausible but remove security cameras, modern glazing details, air-conditioning, bright logos, and all readable contemporary typography. No prominent pseudo-English text.

Medium: authentic 1870s albumen photographic print from wet-plate collodion, monochrome warm sepia-brown, slight edge fading, fine paper fiber, restrained chemical mottling, long-exposure softness in moving people and horses, sharp architectural detail in stationary stonework, gentle lens falloff, period tonal range. It must look like a real surviving Victorian photograph, not a color photo with a sepia filter and not steampunk concept art.

Avoid electric traffic signals, motor vehicles, modern bicycles, London Underground branding, asphalt paint, plastic, Edwardian 1900s silhouettes, Regency dress, 1920s fashion, fantasy machinery, exaggerated coal smoke, cinematic color grading, or modern HDR clarity.

Re-emphasize: keep the exact vertical crop, right-side building diagonal, upper-left sky, street curve, foreground group positions, vehicle focal point, light direction, and shadow geometry recognizable from the source.
```

## 转换映射

| 现代元素 | 历史对应物 |
|---|---|
| 双层巴士 | 马拉伦敦公共马车 omnibus |
| 红绿灯与地铁标识 | 煤气灯、铁栏与克制站牌 |
| 自行车骑手 | 手推包裹车旁的步行信使 |
| 钢架与塑料防护布 | 木脚手架与帆布罩 |
| 彩色数码摄影 | 湿版火棉胶底片转蛋白照片 |

## 证据边界与简化

- 1870 年代伦敦不同阶层、街区和职业差异很大；本例只取市中心商业街的保守基线。
- 原建筑含晚于目标年代的细节，结果保留总体体量但将可见构件改为维多利亚中期材料语言。
- 长曝光质感会牺牲部分人物身份细节，这是选择历史摄影媒介的有意代价。
- 参考：[维多利亚英国视觉基线](../../../../references/europe/victorian-britain.md)
