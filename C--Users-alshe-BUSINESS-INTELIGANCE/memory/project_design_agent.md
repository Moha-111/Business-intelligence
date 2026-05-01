---
name: DesignAgent — AI-Powered Creative Design Platform
description: Multi-agent system for generating websites, landing pages, and presentations from natural language briefs. Bilingual AR/EN. Saudi market primary.
type: project
status: planning — core pipeline not yet built
originSessionId: d937747d-6ea2-4718-96d0-079067732748
---
## What It Is
A multi-agent AI platform that takes a client brief (natural language) and produces:
- Full websites / landing pages (React/Next.js)
- Presentations (interactive web + PPTX export)
- Exports: HTML bundle, React components, Figma-compatible, PDF, PPTX

## Agent Pipeline
```
Client Brief → Creative Director → [Strategist | Designer | Copywriter | Developer | Presenter] → QA Reviewer → Final Deliverable
```
5 specialized agents + 1 coordinator (Creative Director) + 1 QA Reviewer.

## Tech Stack
- Frontend: React 18 + Tailwind CSS + Framer Motion
- SSR: Next.js 14
- AI: Claude Sonnet (design reasoning) + Haiku (quick iterations)
- Image: DALL-E 3 or Stable Diffusion
- Icons: Lucide React + custom SVG
- Fonts: Google Fonts (Arabic: Tajawal, Noto Kufi | English: variable)
- Export: HTML/CSS, React, Figma-compatible, PPTX
- Hosting: Vercel + custom domain

## Key Rules
- Never generic AI aesthetics (no purple-gradient-on-white, no Inter everywhere)
- Always 3 style directions before building
- Always dark/light mode
- Always RTL support (CSS logical properties: ps-, pe-, ms-, me-)
- All text via i18n (AR + EN)
- Lighthouse ≥ 90, WCAG 2.1 AA
- Never placeholder text — all copy real or AI-generated
- Landing page structure: Hero → Problem → Solution → Social Proof → CTA
- 4px base spacing unit (4, 8, 12, 16, 24, 32, 48, 64)
- Typography: display font paired with body font
- Colors: dominant + accent (never evenly distributed)

## Commands
- `npm run dev` — port 3000
- `npm run export:html` / `export:pptx` / `export:pdf`
- `npm run lighthouse` / `a11y`

## Current Focus
Building the core agent pipeline: Brief → Strategy → Design → Code → Export

## Compliance
Saudi PDPL — data processing respects Saudi regulations
