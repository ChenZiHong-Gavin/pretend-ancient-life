# 假装活在古代（pretend-ancient-life）

一个"把现代照片变成古代生活"的内容创作项目：输入一张现代照片，产出对应时代的古画风格提示词，再喂给 Codex imagegen 生成图片。

## 愿景

不限于唐宋——覆盖**中国各朝代**（汉 / 唐 / 宋 / 元 / 明 / 清…）和**外国各时期**（古埃及 / 古希腊 / 古罗马 / 中世纪欧洲 / 江户日本 / 维多利亚…）。让"现代人活在古代"这个设定可批量、可复用地生产内容。

## 目录结构

| 路径 | 说明 |
|---|---|
| `references/china/` | 中国各朝代画风知识库（每朝代一个 .md） |
| `references/foreign/` | 外国各时期画风知识库（每时期一个 .md） |
| `references/_template.md` | 时代参考文件的统一模板 |
| `input/china/`、`input/foreign/` | 待转换的现代照片 |
| `output/prompts/` | 已生成的提示词存档 |
| `output/images/` | 生成后的图片 |
| `examples/prompts/` | 示例提示词（每个时代一条，展示标准输出格式） |
| `examples/before/` | 示例现代原图 |
| `examples/after/` | 示例生成图（与 before 对应） |
| `assets/` | 参考图、素材 |

## 已规划的时代

- **中国**：汉、唐、宋（已填充）、元、明、清
- **外国**：古埃及、古希腊、古罗马、中世纪欧洲、江户日本、维多利亚

## 用法

1. 把现代照片放进 `input/china/` 或 `input/foreign/`。
2. 告诉 Claude："把 `input/china/xxx.jpg` 转成宋代风"（或任意目标时代）。
3. Claude 调用 `ancient-era-conversion` 技能，读取 `references/` 里对应时代文件，产出提示词。
4. 复制提示词到 Codex imagegen 生成。

## 扩展一个新时代

复制 `references/_template.md`，改名为 `references/china/<朝代>.md` 或 `references/foreign/<时期>.md`，填四块内容：时代特征、画风关键词、参考画家/作品、现代→时代元素对照表。
