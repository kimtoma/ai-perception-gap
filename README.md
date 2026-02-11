# Something Big Is Happening — AI Perception Gap

An interactive web page visualizing the growing gap between actual AI capabilities and public perception.

Based on [Matt Shumer's post](https://x.com/mattshumer_/status/2021256989876109403), ["Something Big Is Happening"](https://shumer.dev/something-big-is-happening), and [METR benchmark](https://metr.org/blog/2026-1-29-time-horizon-1-1/) data.

> **5 languages supported**: English (default), 한국어, 中文 (简体), Español, हिन्दी

---

AI 기술의 실제 발전 속도와 일반 대중의 인식 사이에 벌어지고 있는 격차를 시각화한 인터랙티브 웹 페이지입니다.

[Matt Shumer의 포스트](https://x.com/mattshumer_/status/2021256989876109403)와 ["Something Big Is Happening"](https://shumer.dev/something-big-is-happening) 블로그 글, [METR 벤치마크](https://metr.org/blog/2026-1-29-time-horizon-1-1/) 데이터를 기반으로 구성되었습니다.

## Key Features

- **Perception gap visualization** — The difference in AI levels perceived by the tech industry vs. the general public
- **METR benchmark data** — Autonomous task duration from GPT-4 (3.5 min) to GPT-5.2 (6.6 hrs)
- **Feb 5 simultaneous launch comparison** — GPT-5.3-Codex and Claude Opus 4.6 benchmark data
- **Exponential growth trend** — Doubling time accelerating from 197 to 89 days (log-scale chart)
- **Job impact** — AI replacement risk by field
- **Interactive slider** — AI capability timeline from 2020 to 2027
- **Multilingual support** — Language switcher with 5 languages (EN, KO, ZH, ES, HI)

## Tech Stack

- Single `index.html` file (no build tools)
- [Chart.js](https://www.chartjs.org/) — Chart visualization (CDN)
- [Pretendard](https://github.com/orioncactus/pretendard) — Typography (CDN)
- Design system: [KT Seamless Flow](https://uxdesign.kt.com/054231ea3/p/164517-seamless-flow) + [shadcn/ui](https://ui.shadcn.com/) reference

## Run Locally

```bash
open index.html
```

No build or server required.

## i18n

The page supports 5 languages with a fixed-position language switcher in the top-right corner.

| Code | Language | Display |
|------|----------|---------|
| en | English | EN |
| ko | 한국어 | KO |
| zh | 中文 (简体) | ZH |
| es | Español | ES |
| hi | हिन्दी | HI |

- Default: English (falls back from `navigator.language` or `localStorage`)
- All translatable elements use `data-i18n` attributes (~93 keys)
- Charts are destroyed and recreated on language change
- Language preference persists via `localStorage`

## Data Sources

| Data | Source |
|------|--------|
| METR Time Horizon 1.1 | [metr.org](https://metr.org/blog/2026-1-29-time-horizon-1-1/) |
| GPT-5.3-Codex benchmarks | [OpenAI official announcement](https://openai.com/index/introducing-gpt-5-3-codex/) (2026.02.05) |
| Claude Opus 4.6 benchmarks | [Anthropic official announcement](https://www.marktechpost.com/2026/02/05/anthropic-releases-claude-opus-4-6-with-1m-context-agentic-coding-adaptive-reasoning-controls-and-expanded-safety-tooling-capabilities/) (2026.02.05) |
| Doubling time (89 days) | METR TH1.1 — post-2024 analysis |

## License

MIT
