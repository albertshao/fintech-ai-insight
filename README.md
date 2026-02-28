![FinTech AI Insight Weekly Banner](./images/common/banner-fintech-ai-insight-weekly-redbackground.png)

# FinTech AI Insight

Publishing repository for FinTech AI Insight Weekly, including bilingual reports and visual assets.

## Weekly Index

| Year | Week | Publish Date | Chinese | English | Images |
| --- | --- | --- | --- | --- | --- |
| 2026 | 07 | 2026-02-11 | [CN](./weekly/fintech-ai-insight-weekly-2026week7-CN.md) | [EN](./weekly/fintech-ai-insight-weekly-2026week7-EN.md) | [Week7 Image Map](./images/fintech-ai-insight-weekly-2026week7-EN/image-map-week7.md) |
| 2026 | 08 | 2026-02-26 | [CN](./weekly/fintech-ai-insight-weekly-2026week8-CN.md) | - | - |

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

- For each weekly report, store its images in the matching weekly folder under `images/`, not in `images/common/`.
- If CN and EN use the same image for a given week, store that shared image in the EN weekly folder (for example, `images/fintech-ai-insight-weekly-2026week7-EN/`).
- Use `images/common/` only for global assets not tied to a specific week.
- In weekly markdown files, use relative paths like: `../images/fintech-ai-insight-weekly-YYYYweekWW-EN/<file>`.

## Naming Convention

- Weekly filename format: `fintech-ai-insight-weekly-YYYYweekWW-<LANG>.md`
- `LANG` currently uses `CN` and `EN`.
- Week number `WW` should be two digits (for example, `07`, `08`).
