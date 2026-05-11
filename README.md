# SmashOne Brand Assets

Visual identity assets for **SmashOne** — premium SaaS for SMB social media automation. Dual-theme (dark-first + light variant for public marketing surfaces).

> **Brand owner:** NeuralLera (Valery Maltsev)
> **Domain (US):** smashone.us — operated by SMASHONE CORPORATION (Florida C-Corp)
> **Domain (EU):** smashone.ai — operated by SmashOne Polska Sp. z o.o.
> **Visual identity is shared** across both jurisdictions; business entities are independent.

## Repository scope

This repo contains **visual brand identity** only — logos, social platform icons, design tokens, and component specifications. It is referenced by Claude Design (https://claude.ai/design) projects and downstream implementation in product code.

### What's here

- `logos/` — wordmark and tile background patterns (dual-theme)
  - `smashone-tile-dark/` — dark theme tile (canonical bg pattern + favicon variants) + `empty-tile-dark.svg`
  - `smashone-tile-light/` — light theme tile + `empty-tile-light.svg`
  - `smashone-wordmark-dark/` — PNG raster wordmark for dark backgrounds (5 sizes: 64/128/256/512/1254)
  - `smashone-wordmark-light/` — PNG raster wordmark for light backgrounds (5 sizes)
  - `eu-emblem/` — EU jurisdiction marker (dark + light variants)
  - `usa-emblem/` — US jurisdiction marker (dark + light variants)
- `social_icons/` — 22 social platform icons (SVG + PNG sizes 64/128/256/512 in dark and light variants)
- `tokens/` — design system specifications
  - `design-tokens.md` — color, typography, spacing, motion, radius, shadow tokens
  - `components.md` — atomic / molecular / organism component specs

### What's NOT here

- ❌ Marketing copy / pricing values / launch dates / financial details
- ❌ Page layouts or specific product screens (those live in private product repos)
- ❌ Cross-entity business context (US Corp ↔ EU Polska legal/financial relationships)

## Brand identity summary

- **Theme:** dual-theme (dark-first canonical + light variant for public marketing surfaces). Cabinet / admin surfaces remain dark-only. Theme toggle via Lucide Sun/Moon on every public-facing surface, cookie persistence per entity domain.
- **Surface base:** `#0a0a0a` (near-black — never pure `#000000`)
- **Brand accent:** gold `#c9a646` — used as conversion anchor at ~10% surface coverage
- **Typography stack:**
  - Display / hero: **Geist Variable** (Vercel, OFL)
  - Body / UI: **Inter Variable** (Rasmus Andersson, OFL)
  - Code / metrics: **IBM Plex Mono** (IBM, OFL)
- **Voice:** clear, quantified, sentence-case, 5th–7th grade reading level
- **Inspirations:** Linear (calm density), Mercury (trust depth), Stripe (mesh hero), Anthropic (academic restraint)

See `tokens/design-tokens.md` for the full design system specification.

## Usage in Claude Design

When creating a new Design System or Prototype project in Claude Design:

1. **Field «Link code on GitHub»:** paste this repo URL → `https://github.com/NeuralLera/smashone-brand-assets`
2. Claude Design will pull all assets (icons, tile backgrounds, token specs)
3. Reference assets by path inside generated code, e.g.:
   - `social_icons/facebook-tile-dark.svg`
   - `logos/smashone-tile-dark/empty-tile-dark.svg`

## Social platform coverage

22 platforms supported in `social_icons/` (each with `*-tile-dark.svg`, `*-tile-light.svg`, and PNG raster sizes 64/128/256/512):

**Major social networks:** facebook, instagram, tiktok, youtube, x, linkedin, threads, pinterest
**Messaging apps:** telegram, whatsapp, discord, viber, snapchat
**Regional / niche:** kakaotalk, line, reddit
**Future expansion:** vk, ok, dzen, max, aitu, zalo

Filename conventions:
- Most platforms: `<platform>-tile-dark.svg` / `<platform>-tile-light.svg`
- Telegram exception: `telegram-dark.svg` / `telegram-light.svg` (no «tile» suffix)
- X exception: `x-tile-dark-official.svg` / `x-tile-light-official.svg` (uses official mark)

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

Current canonical system version: **v2.1** (Dual-Theme 2026, established 2026-05-09 dark / 2026-05-11 light additions).
