# 宋代（Song Dynasty）

## 范围与默认值

- 时间范围：960–1279年；北宋960–1127，南宋1127–1279。
- 默认子时期：城市与多人街景使用北宋；抒情山水和江南题材可按画面切换南宋。
- 默认地域：北宋汴京或南宋临安与江南，不在同一场景混合。
- 适用场景：市井商业、河港、庭院、山水、人物和儿童生活。

## 同时代视觉证据与特征

- 默认古画模式：`period-artwork translation`。街景优先使用工笔、界画和绢本淡设色：细密而有秩序的线描、准确的木构和舟车、赭石花青与淡墨、适度留白。北宋山水可使用宏阔的全景式构图；南宋山水可使用局部取景与大片空白。
- 写实模式：`reconstructed realism`。使用服饰、器物、建筑和城市研究控制历史内容，不添加绢本纹理或假装是传世宋画。
- 证据边界：城市长卷、院体人物、宫廷册页和文人山水分别服务不同主题、观看方式与阶层；它们不是中性的生活摄影，也不能互相替代。
- 不要把“文人意趣”“青绿山水”“市井长卷”和“院体花鸟”全部堆入同一个提示词。参考作品只提供载体、线条、设色、空间和人物语法；保持原照片的主体关系，不复制名画构图。

## 场景路由

| 场景 | 推荐媒介与视觉语法 | 参考作品 |
|---|---|---|
| 市井 / 多人街景 | gongbi and jiehua, ink and light color on silk；连续叙事与精确建筑 | 张择端《清明上河图》 |
| 北宋山水 | monumental shan shui, textured ink, layered recession | 范宽《溪山行旅图》、郭熙 |
| 南宋山水 | lyrical cropped composition, mist and negative space | 马远、夏圭 |
| 人物 / 儿童 | fine-line figure painting with restrained color；近景人物须明确发式、衣襟结构和非摄影式面部画法 | 苏汉臣《秋庭戏婴图》、传王诜《绣栊晓镜图》 |

## 服饰、建筑与器物

- 服饰与发式：男性使用交领袍、圆领袍、长衫、幞头或方巾；女性可用直领对襟、窄缘窄袖的褙子，内搭交领襦与长裙，头发完整收束为紧凑盘髻并只用少量簪饰。女性近景要明确排除现代刘海、侧分短发、蓬松波波头轮廓、浴袍式交叠 V 领和宽腰带；普通市民衣料素净，身份由帽式、衣缘、腰带和随身器物体现。
- 建筑与基础设施：木构店铺、客栈、虹桥或廊桥、瓦顶、斗拱、石板路、土路和水道。屋檐曲线保持克制，避免仙侠式飞檐。
- 交通与日常器物：驴、马、牛车、驴车、轿子、独轮车、舟船、书案、屏风、笔砚、书卷和灯笼。
- 文字与招牌：普通店招用克制的楷书或行书木牌、酒旗和幌子；Slender Gold script 只用于与宋徽宗或宫廷题款有关的场景，不作为通用店招。

## 语义替换表

| 现代功能或元素 | 时代对应物（英文提示词用） | 选择条件 |
|---|---|---|
| 汽车 / 轿车 | ox cart, donkey cart, horse, sedan chair | 依据乘员、载货和身份选择 |
| 公交车 / 大巴 | a procession of covered carts or a group of travelers | 保留人流容量，不机械复制车身 |
| 电动车 / 摩托车 / 自行车 | donkey, horse, handcart, or walking traveler | 保留骑行姿态时优先驴或马 |
| 手机 | letter scroll, route map, account booklet, or remove with corrected hand gesture | 按通信、导航、付款或阅读功能选择 |
| 电脑 / 电视 | writing desk, account books, painted screen, or scroll display | 按办公或娱乐功能选择 |
| 高架桥 | timber covered bridge or elevated gallery | 保留交通分层和轮廓 |
| 玻璃幕墙 / 混凝土 | timber-frame shops, inns, pavilions, brick-and-wood compounds | 保持体量、层数和透视 |
| 招牌 / 霓虹 / 广告 | wooden plaque, tavern banner, cloth awning, or remove | 文字不重要时留白 |
| 柏油路 | stone-paved road or packed-earth road | 保留雨水反光可用湿石板 |
| 二维码 / 条码 | seal stamp, account tally, or remove | 依据付款或识别功能选择 |

## 禁用与易混元素

- 禁止清代长辫、马褂和旗装，明代乌纱帽、翼善冠以及唐代高腰宫装。
- 禁止“保留现代发型与摄影式立体脸，只套一件泛古风袍服”的人物转换；近景脸部使用细线勾勒、浅平设色和克制的眉眼唇色，不使用现代眼线、蓬松染发、时装式露颈或浴袍轮廓。
- 禁止玻璃、青花瓷主导画面、夸张飞檐、金碧仙宫和电影式武侠服装。
- 不把《千里江山图》的强烈青绿配色套到所有宋代街景，也不把马远、夏圭的南宋构图用于明确的北宋汴京全景。

## 资料来源

- [The Met — Northern Song Dynasty (960–1127)](https://www.metmuseum.org/essays/northern-song-dynasty-960-1127)
- [The Met — Chinese Handscrolls](https://www.metmuseum.org/essays/chinese-handscrolls)
- [国立故宫博物院 — 宋元名绘册・传王诜《绣栊晓镜图》](https://digitalarchive.npm.gov.tw/Collection/Detail/381?dep=P)
- [国立故宫博物院 — 艺苑藏真册・赵伯驌《风檐展卷》](https://digitalarchive.npm.gov.tw/Collection/Detail/326?dep=P)
