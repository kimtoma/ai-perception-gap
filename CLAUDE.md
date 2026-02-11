# CLAUDE.md

## Project Overview

AI 인식 격차를 시각화하는 단일 페이지 웹 프로젝트. `index.html` 하나로 구성.

## Architecture

- 단일 HTML 파일 — 인라인 CSS + JS, 외부 의존성은 CDN으로 로드
- Chart.js 4.x — 4개 차트 (METR 바 차트, Feb5 비교, 시계열 산점도, 격차 라인)
- 빌드 도구 없음 — `open index.html`로 실행

## Design System

- KT Seamless Flow 기반 라이트 테마
- Pretendard Variable 폰트
- shadcn/ui 스타일 컴포넌트 (border-radius: 0.5rem, 1px border, subtle shadow)
- CSS custom properties in `:root` for all tokens

## Key Color Tokens

```
--text-primary: #191A1B
--text-secondary: #55585D
--border: #E9EAEE
--red: #E0282F (accent/warning)
--blue: #2563EB
--amber: #D97706
```

## Data Sources

차트 데이터는 모두 JS 내 하드코딩. METR TH1.1 공식 데이터 기반.
GPT-5.3-Codex, Opus 4.6은 각 사의 공식 발표 벤치마크 수치 사용.

## Conventions

- 한국어 콘텐츠
- 이모지 사용 금지 (텍스트 + SVG 아이콘만)
- AI slop 스타일 금지 (그라디언트, 글로우, 과도한 애니메이션 지양)
- 데이터는 반드시 출처 명시
