# 日本江户时代（Edo Period Japan）

## 身份与范围

- Canonical ID：`japan/edo`
- 单元类型：历史时期 / 德川幕府；1615–1868年。
- 默认值：18世纪江户町人街区与日常出行；支持等级 `baseline`。
- 证据边界：浮世绘偏城市娱乐和商业出版，不能覆盖农村、武家、宫廷与所有地区。

## 同时代视觉证据与场景路由

- 默认古画模式：`period-artwork translation`。先按城市、室内、行旅、名所、武家或地方生活选择浮世绘、绘本、画卷或其他江户视觉传统；写实请求使用 `reconstructed realism`，不添加和纸与木版套色表面。
- 同时代视觉证据以商业出版、城市娱乐、名所与特定阶层为强项；可提取木版轮廓、套色、斜向空间、俯瞰构图和人物类型，但不能把艺伎、演员、游郭或武家服饰推广给所有居民。
- 必须匹配子时期：十九世纪成熟风景锦绘不能无说明地套到十七世纪或十八世纪早期场景；绘本、单张锦绘和画卷也不是同一种画幅语法。

- 城市 / 商业：采用浮世绘木版画的清晰轮廓、平涂色块和斜向街景；店铺、桥梁、人流与身份有秩序。
- 家庭 / 室内：选择适用的风俗画或绘本语法；榻榻米、障子、木构柱网、低家具与可变隔断依据町人、武家或农家调整。
- 行旅 / 郊野：东海道驿站、步行旅客、轿、驮马与山水版画；成熟风景锦绘用于合适的十九世纪日期，不自动加入武士决斗。
- 武家 / 城郭：仅在相应身份使用刀、裃或正式礼服；普通人受佩刀与服饰规定限制。

## 服饰、建筑与器物

- 使用小袖 / 和服、带、羽织、袴、月代等具体轮廓并按性别、职业、阶层和年代选择；不要用现代振袖和动漫发型替代。
- 木构町屋、瓦或木板屋面、纸 / 木格隔扇、桥、运河、道路与火见橹按城市选择。
- 使用行灯、提灯、木桶、漆器、陶瓷、木屐、草鞋、包袱、算盘、书卷与烟管。

## 常用替换

| 现代元素 | 历史对应物 | 条件 |
|---|---|---|
| 汽车 / 自行车 | walking traveler, palanquin, packhorse or handcart | 依据乘员与载货功能 |
| 手机 | folded letter, woodblock-printed guide, account book, or corrected hand | 按通信 / 导航 / 付款功能 |
| 霓虹招牌 | noren curtain, restrained wooden sign, lantern or blank fascia | 不生成醒目伪日文 |
| 玻璃写字楼 | timber machiya shops, warehouses and tiled roofs | 保持街谷透视 |

## 禁用与来源

- 禁止平安贵族服、战国全甲、明治西装和现代艺伎旅游造型混用；不要把所有男子都画成武士。
- [The Met — Art of the Edo Period](https://www.metmuseum.org/essays/art-of-the-edo-period-1615-1868)
- [The Met — Edo-Period Japanese Porcelain](https://www.metmuseum.org/essays/edo-period-japanese-porcelain)
