# 东海道行旅：现代乡间骑行 → 1830 年前后江户旅人

## 目标与支持等级

- Canonical setting：`japan/edo`
- 地点与年代：东海道式驿路与箱根山麓，约 1830 年
- 视觉媒介：风景锦绘木版画
- 支持等级：`baseline`
- 本地文件：`before.jpg`、`after.png`（由 `.gitignore` 排除）

## 原图来源

- 摄影者：Rachel Claire
- 页面：[People Riding Bikes in the Countryside Road](https://www.pexels.com/photo/people-riding-bikes-in-the-countryside-road-7264036/)
- 授权：[Pexels License](https://www.pexels.com/license/)

原图不必摄于日本；示例使用其竖幅道路、远山、巨大天空、左侧近景遮挡和队伍纵深来测试跨地域转换。

## 最终 Prompt

```text
Edit the supplied modern countryside cycling photograph into ordinary travelers on a Tokaido-style post road in late Edo Japan, circa 1830. Preserve the tall portrait crop, camera position, immense bright sky, receding road, wooded mountain focal mass, diagonal verge and the original group's spacing, scale progression, travel direction and depth rhythm. Keep the close dark vertical mass at the far left, but reinterpret it plausibly.

Replace every bicycle and helmet with walking travelers, porters and one packhorse, arranged to preserve the cyclist silhouettes. Convert sportswear into practical commoner kosode, short work jackets, leggings, straw hats, sandals, bundles, staffs and rain capes. Convert the left-edge vehicle/window mass into the cropped wooden side and projecting carrying pole of a passing kago or roadside wooden structure. Convert asphalt into packed earth with drainage ruts and stone edging; replace poles, wires and signs with small waymarkers, bamboo fencing, fields and post-road vegetation.

Keep the travelers ordinary and socially varied. Do not turn the group into samurai, geisha or a ceremonial procession. Remove bicycles, helmets, buses, mirrors, asphalt, power lines, plastic, synthetic sportswear, modern shoes and signage. No armor, Heian court dress, Meiji clothing or large invented calligraphy.

Render in the visual language of a scenic late-Edo nishiki-e: crisp key lines, broad flat shapes, indigo and muted green, strong bokashi in the sky and visible handmade-paper texture, without reproducing a specific historic print. Hands, feet, staffs, loads and horse anatomy must be coherent. The result should read first as the same travel photograph transformed in time.
```

## 转换映射

| 现代元素 | 历史对应物 |
|---|---|
| 骑行队伍 | 步行旅人、脚夫与一匹驮马 |
| 自行车、头盔、骑行服 | 行杖、斗笠、脚绊、草鞋与行囊 |
| 柏油乡道 | 驿路土道、石缘与排水沟 |
| 左侧车辆遮挡 | 近景木构、駕笼侧面或挑杆轮廓 |

## 证据边界与简化

- 原图山体与植被不是日本地貌证据，结果将其解释为箱根式山麓，而非复原具体地点。
- 骑行队伍与步行旅团并非逐人等价，转换优先保留数量感、纵深和运动节奏。
- 输出把左侧近景更接近路旁木构，而非完整駕笼；这是模型对遮挡轮廓的保守解释。
- 参考：[江户时代视觉基线](../../../../references/east-asia/japan-edo.md)
