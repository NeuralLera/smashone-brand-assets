# SmashOne Brand Assets

Visual identity assets for **SmashOne** — premium SaaS for SMB social media automation. Dark theme and light theme both supported.

> **Brand owner:** NeuralLera (Valery Maltsev)
> **Domain (US):** smashone.us — operated by SMASHONE CORPORATION (Florida C-Corp)
> **Domain (EU):** smashone.ai — operated by SmashOne Polska Sp. z o.o.
> **Visual identity is shared** across both jurisdictions; business entities are independent.

## Repository scope

This repo contains **visual brand identity** only — logos, social platform icons, design tokens, and component specifications. It is referenced by Claude Design (https://claude.ai/design) projects and downstream implementation in product code.

### What's here

- `logos/`
  - `smashone-tile-dark/` — dark theme tile (canonical bg pattern + favicon variants — SVG + 64/128/256/512/1254 PNG sizes)
  - `smashone-tile-light/` — light theme tile (canonical bg pattern + favicon variants — SVG + 64/128/256/512/1254 PNG sizes)
  - `smashone-wordmark-dark/` — dark theme wordmark «SmashOne» (PNG sizes 64/128/256/512/1254 — fallback rasters; primary use is TEXT rendering via Geist Variable)
  - `smashone-wordmark-light/` — light theme wordmark (PNG sizes — fallback rasters)
  - `eu-emblem/` — EU jurisdiction marker (smashone.ai)
  - `usa-emblem/` — US jurisdiction marker (smashone.us)
- `social_icons/` — **6 social platform icons** (SVG + PNG sizes 64/128/256/512 in dark and light variants)
- `tokens/`
  - `design-tokens.md` — color, typography, spacing, motion, radius, shadow tokens (dark + light themes)
  - `components.md` — atomic / molecular / organism component specs
- `examples/`
  - `homepage-v5-dark-reference.html` — reference design (stylistic ДНК for downstream Prototype generations — layout / typography / brand gold restraint pattern). NOT for copy/messaging (outdated 18-platform refs).
  - `README.md` — usage guide for reference designs

### What's NOT here

- ❌ Marketing copy / pricing values / launch dates / financial details
- ❌ Page layouts or specific product screens (those live in private product repos)
- ❌ Cross-entity business context (US Corp ↔ EU Polska legal/financial relationships)
- ❌ Cut platform icons (18 deprecated platforms removed from scope per canonical v6.0 LOCKED 2026-05-11)

## Brand identity summary

- **Themes:** Dark + Light — both first-class, user-toggleable via theme switcher
- **Surface base (dark):** `#0a0a0a` (near-black — never pure `#000000`)
- **Surface base (light):** `#fafafa` (near-white — never pure `#ffffff`)
- **Brand accent:** gold `#c9a646` (UI) + `#8c6f1e` (AAA text on light) — used as conversion anchor at ~10% surface coverage
- **Typography stack:**
  - Display / hero: **Geist Variable** (Vercel, OFL)
  - Body / UI: **Inter Variable** (Rasmus Andersson, OFL)
  - Code / metrics: **IBM Plex Mono** (IBM, OFL)
- **Voice:** clear, quantified, sentence-case, 5th–7th grade reading level, Tone B honest framing (no fabricated stats / no fake awards / no fake testimonials)
- **Inspirations:** Linear (calm density), Mercury (trust depth), Stripe (mesh hero), Anthropic (academic restraint)

See `tokens/design-tokens.md` for the full design system specification.

## Usage in Claude Design

When creating a new Design System or Prototype project in Claude Design:

1. **Field «Link code on GitHub»:** paste this repo URL → `https://github.com/NeuralLera/smashone-brand-assets`
2. Claude Design will pull all assets (icons, tile backgrounds, token specs)
3. Reference assets by path inside generated code, e.g.:
   - `social_icons/facebook-tile-dark.svg` / `facebook-tile-light.svg`
   - `logos/smashone-tile-dark/empty-tile-dark.svg` / `logos/smashone-tile-light/empty-tile-light.svg`
   - `logos/smashone-wordmark-light/smashone-wordmark-light-256.png`

## Social platform coverage

**6 platforms total** (canonical v6.0 LOCKED 2026-05-11 — supersedes prior 22-platform list):

### Base trio (Wave 1 — included в $99/€99 subscription)

- **Facebook** — `facebook-tile-{dark,light}.svg` + PNG sizes
- **Instagram** — `instagram-tile-{dark,light}.svg` + PNG sizes
- **Telegram** — `telegram-tile-{dark,light}.svg` + PNG sizes

### Premium addons (Wave 2 — separate subscription per addon)

- **WhatsApp Business** — `whatsapp-tile-{dark,light}.svg` + PNG sizes
- **TikTok** — `tiktok-tile-{dark,light}.svg` + PNG sizes
- **Google Business Profile** — `googlebusiness-tile-dark.svg` + PNG sizes (light variant pending — generate via Claude Design)

### Filename conventions

- All platforms: `<platform>-tile-{dark,light}.svg` + PNG raster sizes (64 / 128 / 256 / 512 px) — uniform across all 6 platforms.

## Cut platforms (removed from scope)

Per canonical v6.0 (LOCKED 2026-05-11), the following 18 platforms are NOT supported and have been removed from this repo:

**Russian:** VK / OK / MAX / Дзен
**Asian:** Aitu / LINE / KakaoTalk / Zalo
**Community:** Reddit / Discord
**Eastern EU:** Viber / Viber Business
**Niche:** Snapchat / LinkedIn / YouTube / Pinterest / X (Twitter) / Threads

Do not add icons for any of these platforms. Do not reference them in marketing copy, customer-facing UI, or product roadmaps.

## License

Copyright © 2026 Valery Maltsev (NeuralLera). All rights reserved.

These assets are made publicly visible for the operational purpose of integrating with Claude Design and similar AI design tools that require public asset URLs. Public visibility does not constitute an open-source license.

You may NOT:
- Reproduce, modify, or redistribute these assets without written permission
- Use them in commercial products other than SmashOne
- Claim derivative rights

You MAY:
- Reference them through Claude Design / similar AI tooling for SmashOne projects
- Inspect their structure for educational reference

For commercial licensing inquiries, contact: neurallera@gmail.com

## Versioning

Assets are not strictly semver-versioned — git history is the source of truth for change tracking. Major iterations of the design system will be tagged (e.g., `system-v2`, `system-v3`).

Current canonical system version: **v3** (Dark + Light Theme 2026, dual-theme established 2026-05-11, 6-platform canonical v6.0 LOCKED 2026-05-11).

Previous versions:
- v2.1 (Dual-Theme partial, established 2026-05-11 morning — superseded by v3 cycle 164 cleanup)
- v2 (Dark Theme 2026, established 2026-05-09 — deprecated by v3)
