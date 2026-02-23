![FinTech AI Insight Weekly Banner](./images/common/banner-fintech-ai-insight-weekly-redbackground.png)

# FinTech AI Insight

FinTech AI Insight Weekly 的发布仓库，集中维护中英文周报与配图资源。

## Weekly Index

| Year | Week | Publish Date | 中文版 | English | Images |
| --- | --- | --- | --- | --- | --- |
| 2026 | 07 | 2026-02-11 | [CN](./weekly/fintech-ai-insight-weekly-2026week7-CN.md) | [EN](./weekly/fintech-ai-insight-weekly-2026week7-EN.md) | [Week7 Image Map](./images/common/image-map-week7.md) |

## Repository Structure

```text
fintech-ai-insight/
├── README.md
├── weekly/
│   ├── fintech-ai-insight-weekly-YYYYweekWW-CN.md
│   └── fintech-ai-insight-weekly-YYYYweekWW-EN.md
└── images/
    ├── common/
    ├── fintech-ai-insight-weekly-YYYYweekWW-CN/
    └── fintech-ai-insight-weekly-YYYYweekWW-EN/
```

## Asset Rules

- 共用图片优先放在 `images/common/`，CN/EN 两版复用同一资源。
- 如果某语言有独占图片，再放到对应语言目录。
- 周报内图片链接建议使用相对路径：`../images/common/<file>`。

## Naming Convention

- Weekly 文件名：`fintech-ai-insight-weekly-YYYYweekWW-<LANG>.md`
- `LANG` 目前使用 `CN` 与 `EN`。
- 周序号 `WW` 使用两位数（如 `07`、`08`）。
