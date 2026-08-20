# 商家账房：现代居家办公 → 1790 年前后江户记账

## 目标与支持等级

- Canonical setting：`japan/edo`
- 地点与年代：江户商家账房，约 1790 年
- 视觉媒介：克制的彩色木版册页
- 支持等级：`baseline`
- 本地文件：`before.jpg`、`after.png`（由 `.gitignore` 排除）

## 原图来源

- 摄影者：Ofspace LLC, Culture
- 页面：[Man Working on Laptop at Home Office](https://www.pexels.com/photo/man-working-on-laptop-at-home-office-16323455/)
- 授权：[Pexels License](https://www.pexels.com/license/)

原图只提供单人侧后方姿态、桌面物件关系与大面积留白；人物身份和拍摄地点不被当作历史事实。

## 最终 Prompt

```text
Edit the supplied modern home-office photograph into a historically plausible Edo merchant accounting room, circa 1790. Preserve the landscape crop, the single seated man on the left seen from behind in three-quarter profile, his forward-working posture and hand positions, the main work surface at center-right, the stack of books at far right, and the unusually large quiet wall area across the upper half.

Replace the laptop with an open vertical Japanese ledger resting on a low slanted writing support, positioned at the same angle and scale. Replace the modern notebook and loose stationery with bound washi account books, brush, inkstone, seal box and account slips. Replace the phone with a vertical soroban or a small bundle of correspondence while keeping the right-side object rhythm. Convert the desk and room into a restrained timber-and-tatami merchant office with shoji light and a blue-gray plaster wall.

Dress the clerk in an ordinary striped kosode and work apron; keep him a merchant employee or shopkeeper, not a samurai or scholar-official stereotype. Remove screen glow, keyboard, electricity, plastic, modern binding, watches, logos, Western clothes and modern typography. Ledger marks may be tiny and subordinate; do not create large fake calligraphy.

Render as a restrained deluxe late-Edo woodblock album illustration on fibrous washi, with fine key lines, soft indigo, gray-blue and warm brown, broad negative space and little theatrical decoration. Keep hands and writing tools coherent. The exact source composition should remain immediately recognizable.
```

## 转换映射

| 现代元素 | 历史对应物 |
|---|---|
| 笔记本电脑 | 斜架上的竖写账册 |
| 手机 | 算盘或往来书信 |
| 精装书与便签 | 和装账簿、账票与封套 |
| 居家办公桌 | 町人商家低桌与账房 |

## 证据边界与简化

- “账房”来自对现代办公功能的映射，不代表原图人物的真实职业。
- 账簿中的笔迹是从属视觉纹理，不能作为可读的江户文书史料。
- 竖置算盘主要为适配原图手机和书堆的垂直轮廓，实际使用时通常会平放。
- 参考：[江户时代视觉基线](../../../../references/east-asia/japan-edo.md)
