# impeccable-taste

**设计品味与审查 skill（Agent Skill）** — Apple Liquid Glass 液态玻璃主题的完整落地方案、
反"AI 平均值"设计方法论、真实浏览器审查工具链，与五大坑避坑手册。

> 整合来源：
> - [taste-skill v2](https://github.com/Leonxlnx/taste-skill) — 247 站研究方法论 + 审查器全套（MIT License, © 2026 Leonxlnx）
> - [impeccable](https://github.com/pbakaus/impeccable) — oklch 色彩体系与设计保真审查门（Apache-2.0, © pbakaus）
> - 实战补丁：旅易出行项目液态玻璃主题落地的 owner 豁免流程、豁免脚本安全边界、合成层 z-index 教训

## 安装（Agent Skill）

复制本目录到 agent 技能目录（如 `~/.zcode/skills/impeccable-taste/`），新会话即可调用。

## 内容结构

| 路径 | 内容 |
|---|---|
| `SKILL.md` | 主文档：十步 run、oklch tonal ramp 色彩法、owner 豁免流程、液态玻璃引擎协同、家规 20 条、laws of the craft |
| `references/` | 12 篇细则：colour / type / layout / motion / copy / critique / imagery / scenes / tells / research / app-screens |
| `scripts/` | `draw.mjs` 方向抽签 · `inspect.mjs` 真实浏览器审查（1440/768/390）· `lint.mjs` 违规扫描 · `assets.mjs` 图库检索 · `scenes.mjs` 场景门 |
| `library/` | 247 站研究数据：方向 / 字系 / 调色板 / 构图 / 动效 / 场景 / app 规则 |
| `assets/` | 中性底座 base.css/base.js + 滚动场景库 + 应用屏 shell + SVG 图表 |

## 快速使用

```bash
# 对现有页面跑违规扫描（app 模式：仪表盘/后台/设置类）
node scripts/lint.mjs <项目路径> --app

# 真实浏览器全宽度审查
node scripts/inspect.mjs <url 或 index.html 路径>

# 为新项目抽取设计方向
node scripts/draw.mjs --sector <行业> --brief "<一句话>" --options 3
```

## 双档液态玻璃主题

配合 `liquid-glass-implementation` 引擎（SVG 位移折射 + RGB 色差 + 弹性物理）：
- **浅色档**：清亮天空底 + 白色半透明磨砂卡（白 58%~72%）+ 深色文字 —— `glass.light.template.css`
- **深色档**：`#1a1a2e→#16213e→#0f0f23` 底 + 白字 —— 复制浅色档后改三处（变量/背景/卡片白）

## 许可

- 本仓库的整合与实战补丁：MIT（© 2026 Leonxlnx）
- taste-skill 部分：MIT（© 2026 Leonxlnx）
- impeccable 概念与方法：Apache-2.0（© pbakaus）—— [NOTICE](NOTICE.md)
