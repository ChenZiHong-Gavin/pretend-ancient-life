# 古典希腊运动：现代街头体操 → 前 450 年红绘陶器

## 目标与支持等级

- Canonical setting：`europe/classical-greece`
- 地点与年代：雅典 palaistra，约前 450 年
- 视觉媒介：阿提卡红绘陶器
- 支持等级：`baseline`
- 本地文件：`before.jpg`、`after.png`（由 `.gitignore` 排除）

## 原图来源

- 摄影者：Ivica Džambo
- 页面：[Group of Men Exercising Outdoors](https://www.pexels.com/photo/group-of-men-exercising-outdoors-4246446/)
- 授权：[Pexels License](https://www.pexels.com/license/)

## 最终 Prompt

```text
Edit the supplied vertical photograph into an athletic training scene inspired by Classical Athens circa 450 BCE, represented entirely as an Attic red-figure vase painting. This is the exact source composition target.

Preserve the original tall portrait crop and aspect ratio, the dominant adult athlete inverted in the center with legs spread in a high V, both hands planted below him, two adult athletes grouped at left, one adult observer/trainer seated at right, the open negative space above, low ground line, and relative size and placement of all four prominent figures. Preserve facing directions and relationships.

For this family-safe reconstruction, keep every adult figure modestly covered: give the central athlete and the other active athlete simple close-fitting dark knee-length athletic wraps that clearly cover waist, hips, and upper legs; give the second left observer a short chiton with a himation over one shoulder; give the seated bearded trainer a full himation and simple sandals. Do not expose genitals or buttocks. Preserve only the athletic pose and visible arms, shoulders, lower legs, and torso where already present in the source.

Correct the central athlete’s hands to rest directly on the painted ground line rather than modern metal parallettes. Replace modern dumbbells with a pair of ancient halteres resting nearby. Remove graffiti, concrete, plastic, caps, tank tops, sneakers, tattoos, and modern exercise equipment. Add only a restrained palaistra cue: a hanging strigil and aryballos, one simple column, trainer's slender staff.

Medium and surface: authentic Attic red-figure ceramic painting, black gloss slip field, reserved terracotta-red figures, precise relief-line anatomy and drapery, dilute glaze for hair and interior lines, restrained meander borders at top and bottom, slight curvature and fine craquelure of a fired amphora surface. Flat ancient pictorial grammar; not photorealism recolored orange. No readable inscriptions.

Avoid exposed nudity, erotic framing, minors, Roman togas, gladiators, Spartan fantasy armor, white marble fantasy cities, gym machines, modern sportswear, Renaissance chiaroscuro, neoclassical oil painting, anime, or glossy digital illustration.

Re-emphasize: exact vertical crop, central upside-down V-legged pose, two left standing adults, one right seated adult, large upper negative space, and the source spatial hierarchy remain recognizable.
```

## 转换映射

| 现代元素 | 历史对应物 |
|---|---|
| 双杠支架 | 手掌直接落在陶绘地线上 |
| 现代哑铃 | 一对 halteres 跳跃石 / 铅制重物 |
| 运动装与帽子 | 安全化运动裹衣、chiton 与 himation |
| 海边混凝土场地 | 极简 palaistra 柱、刮汗器与油瓶 |

## 证据边界与简化

- 古典希腊成年男性运动员常以裸体训练和被描绘；本例因生成安全约束改用明确遮盖的现代安全化裹衣，**不可作为真实运动服饰证据**。
- 手倒立动作来自原照片的叙事保持要求，不表示它是红绘陶器中常见或已充分证实的训练项目。
- halteres、strigil 与 aryballos 是运动场景提示物，不代表原动作必然同时使用它们。
- 参考：[古典希腊视觉基线](../../../../references/europe/classical-greece.md)
