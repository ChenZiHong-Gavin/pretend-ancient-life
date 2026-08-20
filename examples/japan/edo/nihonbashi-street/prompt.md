# 江户町人街道：现代东京人潮 → 1780 年前后浮世绘

## 目标与支持等级

- Canonical setting：`japan/edo`
- 地点与年代：江户町人商业街区，约 1780 年
- 视觉媒介：晚期江户浮世绘木版画
- 支持等级：`baseline`
- 本地文件：`before.jpg`、`after.png`（由 `.gitignore` 排除）

## 原图来源

- 摄影者：Ahmad Shakir Shamsulbadri
- 页面：[Vibrant Street Life in Tokyo, Japan](https://www.pexels.com/photo/vibrant-street-life-in-tokyo-japan-30736822/)
- 授权：[Pexels License](https://www.pexels.com/license/)

## 最终 Prompt

```text
Edit the provided source photograph into a historically grounded scene: an ordinary crowded merchant street in Edo, Japan, circa 1780, represented as a refined late-Edo ukiyo-e woodblock print. This is an image edit, not loose inspiration.

Preserve the original portrait crop and aspect ratio, elevated camera position, steep central street receding toward the middle, dense crowd filling the lower two-thirds, shopfronts enclosing both sides, and the same overall distribution of light and shadow. Preserve the crowd as many distinct ordinary pedestrians rather than a single mass.

Convert every person into plausible Edo-period townspeople, shopkeepers, porters, women, men, and children in status-appropriate kosode/kimono, obi, haori, simple work garments, tenugui, wooden geta or straw sandals; vary garments modestly. Do not turn everyone into samurai, courtiers, geisha, or festival performers. Preserve the figures' walking directions and crowd flow.

Replace concrete, glass, steel, electrical wiring, cameras, modern poles, storefronts, and signs with two-story timber machiya, tiled or wood-shingle roofs, wooden lattice fronts, cloth noren, restrained lanterns, handcarts, baskets, bundles, and a distant fire-watch tower and tiled warehouses. Preserve the street-canyon perspective while reducing all building heights to historically plausible Edo scale. Remove all logos, prices, Latin text, traffic infrastructure, and modern typography. If signboards are present, keep them small and use only a few visually subordinate, credible Edo-period brush marks; no prominent invented writing.

Medium: authentic-looking multiblock ukiyo-e print on slightly aged washi, crisp carved key lines, flat mineral and vegetable color areas, bokashi gradients, restrained indigo, warm ochre, persimmon red, gray-green, and unprinted paper tone. No photographic skin, no cinematic depth of field, no anime, no glossy digital painting.

Avoid Meiji Western dress, modern furisode tourist styling, full armor, fantasy pagodas, neon, glass towers, cars, bicycles, asphalt, plastic, power lines, photographic realism, or garbled large text. Re-emphasize: keep the exact vertical crop, elevated viewpoint, vanishing street, crowd density, shop placement, and light direction recognizable from the source.
```

## 转换映射

| 现代元素 | 历史对应物 |
|---|---|
| 玻璃高层与混凝土店铺 | 两层町屋、土藏、瓦顶与火见橹 |
| 电线、监控与灯杆 | 木构店面、提灯、行灯与空白立面 |
| 商业招牌与价格 | 小型木牌、暖帘与少量从属笔迹 |
| 现代人潮 | 町人、商贩、脚夫、妇女与儿童 |

## 证据边界与简化

- 浮世绘是商业出版物，不是对整座江户和所有阶层的中性记录。
- 原图中央高楼无法在江户建筑尺度中逐体量保留，因此改为低层土藏群与火见橹，优先保留街道消失点。
- 生成结果仍出现少量装饰性笔迹；它们只作从属纹理，不应被当作可读史料。
- 参考：[江户时代视觉基线](../../../../references/east-asia/japan-edo.md)
