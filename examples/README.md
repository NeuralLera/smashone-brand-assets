# SmashOne — Reference Designs

This folder contains **reference design artifacts** generated through Claude Design — used as stylistic ДНК (DNA) reference for downstream Prototype generations. These are NOT production code, but visual / structural references for brand identity expression patterns.

## Files

### `homepage-v5-dark-reference.html`

**Source:** Generated 2026-05-10 evening via Claude Design (TASK-001 Homepage v5 honest framing rewrite).
**Theme:** Dark theme (v2 design system).
**Purpose:** Stylistic ДНК reference for new light theme Homepage generations (v6+).

**What to inherit from this reference:**
- Hero composition (50/50 split — text left + inline dashboard mockup right)
- Typography hierarchy (Geist Display oversized hero, Inter body lead 18-22px)
- Brand gold restraint (~10% surface coverage — primary CTAs + key data viz + accent moments only)
- Tile background subtle texture pattern
- Compact metric row pattern below hero
- Validation bar / trust signals strip composition
- Pricing card centered emphasis
- FAQ accordion patterns

**What NOT to inherit (this is OUTDATED messaging — superseded by canonical v6.0):**
- ❌ Platform messaging — uses «18 platforms» / outdated copy. **Current canon = 6 platforms unified declaration** (Facebook + Instagram + Telegram + WhatsApp Business + TikTok + Google Business Profile).
- ❌ Pricing — installment language («$19.92×12», «$239 installment») — deprecated per pricing canon v4.0. **Current canon = no installment, Day 15 unified transaction, 4-paths model**.
- ❌ «Wave 1 base + Wave 2 addons» / «Coming July 2026» — superseded. **Current canon = 6 platforms unified declaration upfront, no temporal split**.
- ❌ Theme — this is dark only. **Current canon = light theme primary for public marketing surfaces, dark via toggle**.

## Usage

When generating downstream Prototypes (Homepage v6 LIGHT, Pricing, Automator, etc.) — reference this file path в PROMPT.md attachment list:

```
- `examples/homepage-v5-dark-reference.html` — stylistic ДНК reference (layout / typography / brand gold restraint pattern). NOT for copy or messaging — only visual structure.
```

Claude Design will auto-pull from this repo when DS is set as DEFAULT.

## Future additions

When new reference designs land (Pricing v6 LIGHT generated and approved, Automator v6 LIGHT, etc.), add them here as `<surface>-v<version>-<theme>-reference.html` for downstream Prototype generations.
