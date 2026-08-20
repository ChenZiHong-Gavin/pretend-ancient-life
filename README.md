# 假装活在古代（pretend-ancient-life）

一个面向 Codex 的全球历史影像转换 Skill：把现代照片重构为具体地点、具体年代的历史场景，同时尽量保留人物身份、动作关系和画面叙事，并用当地、同时代、与场景匹配的艺术作品决定古画模式的视觉语法。

它不把世界历史简化成“中式古风”和“外国古风”。Skill 会先确定历史地点，再选择当时实际存在的王朝、帝国、王国、历史时期或考古文化，最后按物件的功能完成替换：手机可以变成信件、蜡板、简牍或账册，汽车可以变成当地同时代的舟船、马车、轿或步行队伍。

## 特点

- **地域优先**：先定城市或文化区域，再定时间；不会把现代国界直接投射到古代。
- **世界史分期**：中国可按王朝，日本按时代，欧洲按古典 / 中世纪 / 文艺复兴等时期，其他地区按当地帝国、王国或考古文化命名。
- **三级支持**：区分 `reviewed`、`baseline` 和 `catalogued`，避免目录里有名字就假装已经能准确复原。
- **按功能替换**：先判断现代元素的用途，再寻找当地同时代的对应物，而不是逐像素换皮。
- **同时代艺术媒介**：宋代不只写“宋画”，而会按市井、人物、北宋山水或南宋山水选择不同作品传统、载体与空间语法。
- **双证据链**：服饰、器物和建筑来自物质文化证据；线条、设色、空间、人物比例和画幅来自同时代视觉作品。
- **保留原图叙事**：锁定人物数量、相对位置、姿态、视角、画幅和主光方向。
- **证据边界明确**：区分考古实物、宫廷艺术、宗教图像、墓葬材料与后世再现，不把精英证据当作全民日常。
- **生成与审查一体化**：生成后继续检查现代残留、地域错置、时代混搭、人物漂移和文字伪影。
- **支持 prompt-only**：也可以只输出结构化提示词、元素替换表和历史不确定性。

## 支持等级

| 等级 | 说明 | 使用方式 |
|---|---|---|
| `reviewed` | 有独立视觉参考和已审查示例 | 可直接生成，并按参考规则验收 |
| `baseline` | 有独立视觉参考，尚无已审查示例 | 可以生成，但会复核关键细节并注明基础参考 |
| `catalogued` | 已进入世界史分期表，尚无独立参考 | 先查权威资料，或明确标注为创作性诠释 |

### 已审查：中国

| 时期 | 典型场景 | 视觉参考 |
|---|---|---|
| 汉 | 宴饮、车马、庭院、驿路 | [汉代参考](references/china/han.md) |
| 唐 | 长安市井、商旅、宴乐 | [唐代参考](references/china/tang.md) |
| 宋 | 北宋市井、河港、书斋、园林、山水行旅 | [宋代参考](references/china/song.md) |
| 元 | 草原骑行、多族群城市、农耕、文人山水 | [元代参考](references/china/yuan.md) |
| 明 | 港口、江南城市、园林、商贸 | [明代参考](references/china/ming.md) |
| 清 | 城市、驿站、行旅、宫廷纪实 | [清代参考](references/china/qing.md) |

### 基础参考：新增时期

| 地区 | 时期 |
|---|---|
| 中国 | [商](references/china/shang.md)、[周](references/china/zhou.md)、[秦](references/china/qin.md)、[魏晋南北朝](references/china/six-dynasties.md)、[隋](references/china/sui.md)、[五代十国](references/china/five-dynasties.md) |
| 日本 | [江户时代](references/east-asia/japan-edo.md) |
| 南亚 | [莫卧儿印度](references/south-asia/mughal.md) |
| 西亚 | [奥斯曼帝国](references/west-asia/ottoman.md) |
| 北非 | [埃及新王国](references/north-africa/egypt-new-kingdom.md) |
| 欧洲 | [古典希腊](references/europe/classical-greece.md)、[罗马帝国](references/europe/roman-empire.md)、[西欧中世纪](references/europe/medieval-western-europe.md)、[维多利亚英国](references/europe/victorian-britain.md) |

更多时期已经按区域进入 [世界历史时期索引](references/index.md)，包括东亚、南亚与东南亚、中亚与西亚、非洲、欧洲、美洲和大洋洲。Catalog 是研究入口，不等于已经拥有完整视觉复原资料。

## 安装

Codex 会从 `$HOME/.agents/skills` 发现用户级 Skill：

```bash
mkdir -p "$HOME/.agents/skills"
git clone https://github.com/ChenZiHong-Gavin/pretend-ancient-life.git \
  "$HOME/.agents/skills/pretend-ancient-life"
```

如果已经有本地仓库，可以创建符号链接：

```bash
mkdir -p "$HOME/.agents/skills"
ln -s /absolute/path/to/pretend-ancient-life \
  "$HOME/.agents/skills/pretend-ancient-life"
```

若只希望在单个项目中使用，可将仓库放入 `.agents/skills/pretend-ancient-life`。Codex 通常会自动发现修改；如果没有出现，请重启 Codex。更多机制说明见 [OpenAI：Build skills](https://learn.chatgpt.com/docs/build-skills.md)。

## 快速开始

附加照片或提供本地路径，然后显式调用 Skill：

```text
使用 $pretend-ancient-life，把这张照片转换成北宋汴京市集。
使用北宋市井长卷与界画的画面语法，保留人物数量、站位和街道结构，
不要照抄任何现存名画的构图。
```

世界其他地区也使用同一入口：

```text
使用 $pretend-ancient-life，把这张咖啡馆合照转换成18世纪江户町人茶屋。

使用 $pretend-ancient-life，把这张河边照片转换成公元前13世纪底比斯附近的尼罗河日常。

使用 $pretend-ancient-life，把这张步行街转换成12世纪英格兰城镇，只生成 prompt。
```

如果只说“古代欧洲”“古代非洲”或“印度古代”，Skill 会先提供两个有明显差异的地点 / 时期候选，不会擅自选择一种泛历史风格。

输出默认保存到：

```text
output/images/<place>/<period>/
output/prompts/<place>/<period>/
```

例如：

```text
output/images/japan/edo/
output/prompts/egypt/new-kingdom/
```

## 工作原理

```text
确定历史地点
    ↓
确定年代与当地政治 / 文化单元
    ↓
检查支持等级，读取区域 catalog 与一个时期 reference
    ↓
选择古画转译 / 写实复原 / 创作性诠释
    ↓
分别建立物质文化证据与同时代视觉证据
    ↓
按场景选择载体、格式、线条、设色与空间语法
    ↓
锁定人物、构图、画幅、光影与可转译的空间关系
    ↓
建立“现代功能 → 当地同时代对应物”替换表
    ↓
生成图像或结构化 prompt
    ↓
检查现代残留、地域 / 时代一致性与主体漂移
    ↓
保存结果、资料来源、证据限制与创作性简化
```

世界史路由主要参考 [The Met Heilbrunn Timeline of Art History](https://www.metmuseum.org/toah/chronology) 的“地理 + 年代”结构；实际生成还会用当地博物馆、考古机构或专题馆藏校正。

## 艺术媒介不是朝代滤镜

Skill 会先选择输出模式：

| 模式 | 适用请求 | 处理方式 |
|---|---|---|
| `period-artwork translation` | “变成宋画”“生成古画版”或未指定写实媒介 | 使用当地同时代、与场景匹配的绘画、版画、壁画、手稿、器物图像或摄影语法 |
| `reconstructed realism` | “像真实照片”“考据式真人复原” | 保留摄影式空间和光线，用物质文化证据校正历史内容 |
| `creative interpretation` | 证据不足或明确要求想象 | 标注推断部分，不冒充直接历史证据 |

“宋画”仍然过于宽泛：北宋市井可参考城市长卷和界画语法，北宋山水可采用全景式层叠空间，南宋山水可采用局部取景与大片留白，近景人物则应路由到同时代人物画。代表作品只用来提取线条、设色、空间、人物和载体逻辑，不能照抄构图，也不能把宫廷、宗教或墓葬图像中的身份和器物直接推广给所有普通人。完整规则见 [同时代艺术媒介路由](references/visual-medium-routing.md)。

目前仓库中的 20 个详细时期参考都已采用这一结构。商、周、秦等传世绘画证据不足的分支会明确回退到考据式写实或标注过的创作性诠释；汉唐墓葬图像、埃及墓室艺术、欧洲宗教手稿等则会记录其葬祭、宗教和阶层偏差；江户、莫卧儿、奥斯曼、希腊、罗马、中世纪和维多利亚分支都会按具体场景、子时期与载体继续细分，而不是只使用一个地区标签。

其余 105 个 `catalogued` 条目也已逐条补充“同时代视觉媒介研究入口”，覆盖考古器物、壁画、浮雕、手稿、纺织、雕塑、建筑、版画、摄影及相关社群知识。它们仍然只是研究方向，不是已验证画风：实际生成前必须进一步核对当地机构、权威馆藏或后裔社群资料，完成独立 reference 和生成审查后才能升级为 `baseline`。

## 中国示例 Prompt

为控制仓库体积，`before / after` 图片只保留在本地并由 `.gitignore` 排除；仓库提交 `prompt.md` 与图片来源记录。

| 朝代 | Prompt / 来源记录 |
|---|---|
| 汉 | [prompt](examples/china/han/prompt.md) |
| 唐 | [prompt](examples/china/tang/prompt.md) |
| 宋 | 6 组场景（见下表） |
| 元 | [prompt](examples/china/yuan/prompt.md) |
| 明 | [prompt](examples/china/ming/prompt.md) |
| 清 | [prompt](examples/china/qing/prompt.md) |

### 宋代多场景

| 场景 | Prompt / 来源记录 |
|---|---|
| 城市高架街景 → 北宋市井 | [prompt](examples/china/song/urban-overpass/prompt.md) |
| 北京步行街 → 汴京市集 | [prompt](examples/china/song/market-street/prompt.md) |
| 现代咖啡聚会 → 园林茶叙 | [prompt](examples/china/song/tea-gathering/prompt.md) |
| 笔记本电脑办公 → 文人书斋 | [prompt](examples/china/song/scholar-studio/prompt.md) |
| 上海现代航运 → 汴河漕运 | [prompt](examples/china/song/river-port/prompt.md) |
| 雾山徒步 → 南宋山径行旅 | [prompt](examples/china/song/mountain-travel/prompt.md) |

`prompt.md` 记录图片来源、摄影者、授权、完整提示词、元素替换表与历史简化说明。当前示例原图来自 Pexels，并按照 [Pexels License](https://www.pexels.com/license/) 在本地使用和修改。

## 日本江户示例 Prompt

下面 6 组都转换为江户时代，但原图不要求拍摄于日本。原图在这里提供的是构图、人物关系、动作和现代物件的功能；目标地区与年代则由江户视觉参考约束。这样可以直接测试 Skill 的跨地域转换能力，而不是依赖“原图本来就有日本感”。

| 场景 | 重点测试 | 媒介 | Prompt / 来源记录 |
|---|---|---|---|
| 东京商业街人潮 → 江户町人街 | 高机位、人群密度与街道消失点 | 浮世绘木版画 | [prompt](examples/japan/edo/nihonbashi-street/prompt.md) |
| 现代家庭用餐 → 町人家庭午餐 | 三人关系、窗面与侧向日光 | 室内题材锦绘 | [prompt](examples/japan/edo/family-meal/prompt.md) |
| 多代同堂做饭 → 町屋厨房 | 五人手部动作与近景重叠 | 手彩江户绘本 | [prompt](examples/japan/edo/townhouse-kitchen/prompt.md) |
| 笔记本电脑办公 → 商家账房 | 单人侧姿、桌面映射与大面积留白 | 彩色木版册页 | [prompt](examples/japan/edo/merchant-accounting/prompt.md) |
| 乡间骑行 → 东海道行旅 | 竖幅纵深、队伍节奏与远山 | 风景锦绘 | [prompt](examples/japan/edo/countryside-travel/prompt.md) |
| 俯拍野餐 → 郊外赏花行乐 | 严格俯视、裁切肢体与器物分布 | 摺物式精细木版画 | [prompt](examples/japan/edo/garden-picnic/prompt.md) |

每个示例都先锁定人物数量、相对位置、画幅、视角、光线或物件布局，再按功能替换不符合时代的元素。风格媒介也按场景分别选择，避免所有结果被压成同一种“泛浮世绘”滤镜。

## 跨区域示例 Prompt

下面 5 组使用不同的原图结构与历史媒介，测试 Skill 是否能在保留照片构图的同时避免把世界史压成同一种“古风”滤镜。它们目前仍是 `baseline` 示例，不等同于专家审定的考古复原。

| 地区 / 时期 | 现代原图 → 历史场景 | 媒介 | Prompt / 来源记录 |
|---|---|---|---|
| 日本江户 | 东京商业街人潮 → 约 1780 年江户町人街 | 浮世绘木版画 | [prompt](examples/japan/edo/nihonbashi-street/prompt.md) |
| 埃及新王国 | 卢克索现代三角帆船 → 约前 1250 年尼罗河运输 | 墓室彩绘壁画 | [prompt](examples/egypt/new-kingdom/nile-felucca/prompt.md) |
| 莫卧儿印度 | 现代俯拍花市 → 约 1590 年阿格拉市集 | 莫卧儿细密画 | [prompt](examples/india/mughal/flower-market/prompt.md) |
| 古典希腊 | 现代街头体操 → 约前 450 年 palaistra 运动 | 阿提卡红绘陶器 | [prompt](examples/greece/classical/outdoor-athletes/prompt.md) |
| 维多利亚英国 | 现代伦敦路口 → 约 1875 年商业街 | 湿版火棉胶 / 蛋白照片 | [prompt](examples/britain/victorian/london-street/prompt.md) |

这些目录中的 `before.jpg` 与 `after.png` 继续只供本地检查，不进入 Git；因此公开仓库可以复现 Prompt 和来源判断，而不被大体积图片占满。

## 仓库结构

```text
SKILL.md                               核心路由、转换流程和验收规则
agents/openai.yaml                     Codex Skill 界面元数据
references/index.md                    全球地域入口与支持等级
references/visual-medium-routing.md    同时代艺术作品、输出模式与媒介路由
references/regions/<region>.md         各区域的世界史分期 catalog
references/<place>/<period>.md         可直接使用的时期视觉知识
references/_template.md                新时期参考模板
examples/<place>/<period>/             Prompt 与来源记录
input/                                 用户输入照片（可选）
output/                                实际任务输出
```

## 扩展一个时期

1. 从 [世界历史时期索引](references/index.md) 找到所属区域，不创建 `foreign/` 目录。
2. 复制 `references/_template.md`，注明历史地域、单元类型、时间、证据类型和资料偏差。
3. 至少使用一项当地或专题机构资料，以及一项可核对服饰、建筑或器物的馆藏 / 考古资料。
4. 古画模式至少记录一项可核对日期、地域、载体和原用途的同时代视觉作品；没有合适作品时必须记录证据缺口与回退模式。
5. 在对应区域 catalog 中登记，初始等级设为 `baseline`。
6. 用真实 `before / after` 在本地测试并提交 `prompt.md`；同时检查物质文化与艺术媒介，通过后再提升为 `reviewed`。

欢迎通过 Issue 或 Pull Request 补充分期、纠正史实或贡献经审查的 Prompt。

## 关于历史准确性

本项目生成的是基于资料约束的视觉重构，不等同于考古复原。服饰、器物、建筑和生活方式会因地点、阶层、季节、宗教与具体年代变化；同时代艺术作品也可能服务于宫廷、宗教、墓葬、商业出版或特定审美，并不是中性的生活快照。若用于出版、展览或教学，请再由相关地区和时期的专家复核。
