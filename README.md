# AI Perception Gap

AI 기술의 실제 발전 속도와 일반 대중의 인식 사이에 벌어지고 있는 격차를 시각화한 인터랙티브 웹 페이지입니다.

[Matt Shumer의 포스트](https://x.com/mattshumer_/status/2021256989876109403)와 ["Something Big Is Happening"](https://shumer.dev/something-big-is-happening) 블로그 글, [METR 벤치마크](https://metr.org/blog/2026-1-29-time-horizon-1-1/) 데이터를 기반으로 구성되었습니다.

## 주요 내용

- **인식 격차 시각화** — 테크 업계 vs 일반 대중이 체감하는 AI 수준의 차이
- **METR 벤치마크 실측 데이터** — GPT-4(3.5분)부터 GPT-5.2(6.6시간)까지 모델별 자율 작업 시간
- **2월 5일 동시 출시 모델 비교** — GPT-5.3-Codex와 Claude Opus 4.6의 벤치마크 데이터
- **지수적 성장 추세** — 197일 → 89일로 가속되는 더블링 주기 (로그 스케일 차트)
- **직업 영향** — 분야별 AI 대체 위험도
- **인터랙티브 슬라이더** — 2020~2027 시점별 AI 능력 변천사

## 기술 스택

- 단일 `index.html` 파일 (의존성 없음)
- [Chart.js](https://www.chartjs.org/) — 차트 시각화 (CDN)
- [Pretendard](https://github.com/orioncactus/pretendard) — 타이포그래피 (CDN)
- 디자인 시스템: [KT Seamless Flow](https://uxdesign.kt.com/054231ea3/p/164517-seamless-flow) + [shadcn/ui](https://ui.shadcn.com/) 참고

## 로컬 실행

```bash
open index.html
```

별도의 빌드나 서버가 필요 없습니다.

## 데이터 출처

| 데이터 | 출처 |
|--------|------|
| METR Time Horizon 1.1 | [metr.org](https://metr.org/blog/2026-1-29-time-horizon-1-1/) |
| GPT-5.3-Codex 벤치마크 | [OpenAI 공식 발표](https://openai.com/index/introducing-gpt-5-3-codex/) (2026.02.05) |
| Claude Opus 4.6 벤치마크 | [Anthropic 공식 발표](https://www.marktechpost.com/2026/02/05/anthropic-releases-claude-opus-4-6-with-1m-context-agentic-coding-adaptive-reasoning-controls-and-expanded-safety-tooling-capabilities/) (2026.02.05) |
| 더블링 주기 (89일) | METR TH1.1 — post-2024 분석 |

## 라이선스

MIT
