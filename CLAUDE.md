# CLAUDE.md

## Project Overview

Interactive single-page web project visualizing the AI perception gap. Single `index.html` file with 5-language support (EN/KO/ZH/ES/HI).

## Architecture

- Single HTML file — inline CSS + JS, external dependencies via CDN
- Chart.js 4.x — 4 charts (METR bar, Feb5 comparison, trend scatter, gap line)
- i18n via `data-i18n` attributes (~93 keys) + JS translations object `T`
- `setLang(lang)` updates all text, recreates charts, persists to localStorage
- No build tools — `open index.html` to run

## i18n

- Default language: English
- Languages: en, ko, zh, es, hi
- Translation keys in `T.en`, `T.ko`, `T.zh`, `T.es`, `T.hi`
- `setLang()` sets innerHTML on all `[data-i18n]` elements, destroys/recreates charts
- Language detection: localStorage > navigator.language > fallback to 'en'
- Language switcher: fixed top-right dropdown (`.lang-switch`)

## Design System

- KT Seamless Flow light theme
- Pretendard Variable font
- shadcn/ui style components (border-radius: 0.5rem, 1px border, subtle shadow)
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

All chart data is hardcoded in JS. Based on METR TH1.1 official data.
GPT-5.3-Codex and Opus 4.6 use official benchmark numbers from each company.

## Conventions

- English as default content language, multilingual via i18n
- No emojis (text + SVG icons only)
- No AI slop style (no gradients, glows, excessive animations)
- All data must cite sources
