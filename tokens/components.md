# SmashOne Components — v2 (Dark Theme 2026)

> Atomic / molecular / organism component specifications for the SmashOne design system.
> Pair with `design-tokens.md` for the underlying token reference.

---

## Atoms

### Buttons (3 variants × 3 sizes)

**Variants:**

- **Primary** — solid `--brand-gold` background, black text, weight 580. High-intent CTAs.
- **Secondary** — transparent background, `--brand-gold` border 1px, gold text, weight 550. Ghost button.
- **Tertiary** — text-only, `--text-primary` color, no border, weight 500, with underline-on-hover.

**Sizes:**

| Size | Min-height | Padding | Font-size | Line-height |
|---|---:|---|---:|---:|
| `lg` | 48px | 0 20px | 15px | 22px |
| `md` (default) | 40px | 0 16px | 14px | 20px |
| `sm` | 32px | 0 12px | 13px | 18px |

**Common rules:**
- `border-radius: var(--radius-md)` (12px)
- `font-family: var(--font-body)`
- Sentence case ALWAYS (no UPPERCASE button text)
- `transition: all var(--dur-hover) var(--ease-ui)`

**States:**
- **Hover:** `transform: translateY(-1px)` + `box-shadow: var(--shadow-md)` (no color shift for primary; secondary fills bg with `--brand-gold-tint`)
- **Active/Pressed:** `transform: translateY(0) scale(0.98)`, `--dur-press`
- **Focused:** `outline: 2px solid var(--brand-gold); outline-offset: 4px`
- **Disabled:** `opacity: 0.36; cursor: not-allowed`
- **Loading:** inline spinner + `opacity: 0.9; pointer-events: none`

### Inputs

```css
.input {
  background: var(--surface-raised);
  border: 1px solid var(--border-subtle);
  border-radius: var(--radius-md);
  padding: 12px 16px;
  font-family: var(--font-body);
  font-size: 14px;
  color: var(--text-primary);
  transition: border-color var(--dur-hover) var(--ease-ui),
              box-shadow var(--dur-hover) var(--ease-ui);
}

.input::placeholder { color: var(--text-tertiary); }

.input:focus {
  outline: none;
  border-color: var(--brand-gold);
  box-shadow: 0 0 0 3px var(--brand-gold-glow);
}

.input.is-error {
  border-color: var(--state-error);
}

.input:disabled {
  background: var(--surface-base);
  color: var(--text-disabled);
  cursor: not-allowed;
}
```

Sizes: `sm` 32px, `md` 40px (default), `lg` 48px.

### Checkbox / Radio / Toggle

- **Checkbox:** 16×16px square, `--radius-xs`, default border `--border-strong`. Checked: `--brand-gold` bg + black ✓.
- **Radio:** 16×16px circle, default `--border-strong`. Selected: gold ring + gold-filled inner dot.
- **Toggle:** 44×24px pill. OFF: `--surface-elevated` bg. ON: `--brand-gold` bg + white knob.

### Badges / Chips / Pills

- **Badge (status):** padding 2px 8px, `--radius-full`, font-size 11px, tracking 0.04em, weight 580. Variants: success / warning / error / info / neutral via `--state-*` colors.
- **Chip (filter):** padding 4px 12px, `--radius-full`, weight 500, hoverable + clickable.
- **Pill (data label):** padding 4px 8px, `--radius-sm`, mono font for numeric content.

### Avatars

- Sizes: 24, 32, 40, 56, 64, 80px (circular `--radius-full`)
- Border 2px `--border-subtle` default; gold border for active/online state
- Fallback: initials in mono font, gold gradient bg, white text

### Icons

- Sizes: 16, 20, 24px (match adjacent text x-height)
- **Stroke-based** (Lucide / Tabler / Heroicons style) — NOT filled
- Color: `--text-secondary` default, `--brand-gold` for active/CTA
- Stroke width 1.5–2px

### Tooltips

```css
.tooltip {
  background: var(--surface-overlay);
  border: 1px solid var(--border-subtle);
  border-radius: var(--radius-sm);
  padding: 8px 12px;
  font-size: 13px;
  font-weight: 500;
  color: var(--text-primary);
  opacity: 0;
  transform: translateY(6px) scale(0.98);
  transition: opacity 150ms var(--ease-open),
              transform 150ms var(--ease-open);
  transition-delay: 180ms;
  pointer-events: none;
}

.trigger:hover .tooltip,
.trigger:focus-visible .tooltip {
  opacity: 1;
  transform: translateY(0) scale(1);
}
```

ALWAYS supplement (never replace) primary affordances. Tooltips are not the only way to discover meaning.

---

## Molecules

### Form field

```
┌─ Label (--label-md, --text-primary) ─────┐
│ Email address                            │
├──────────────────────────────────────────┤
│ ┌──────────────────────────────────────┐ │
│ │ [Input — --surface-raised]           │ │
│ └──────────────────────────────────────┘ │
│                                          │
│ Helper text (--body-sm, --text-tertiary) │
│   or                                     │
│ Error text (--state-error, with ⚠ icon)  │
└──────────────────────────────────────────┘
```

**Validation:** blur (field) + submit (form). Real-time only for password requirements / format masks / username availability.

### Cards

| Variant | Background | Border | Shadow | Hover |
|---|---|---|---|---|
| `card-flat` | `--surface-raised` | `1px --border-subtle` | none | translateY(-3px) + `--border-emphasis` + `--shadow-lg` |
| `card-raised` | `--surface-raised` | none | `--shadow-md` | translateY(-3px) + `--shadow-lg` |
| `card-bordered-accent` | `--surface-raised` | `1px --brand-gold` | none | `--shadow-glow` |

All cards: `border-radius: var(--radius-lg)` (16px), `padding: var(--space-8)` (32px).

### Pricing card (canonical SmashOne layout)

- Max-width: 480px, centered
- Background: `--surface-elevated`
- Border: `1px solid var(--brand-gold)`
- Border-radius: `var(--radius-xl)` (20px)
- Padding: `var(--space-10)` (40px)

Internal structure:

```
┌─────────────────────────────────────┐
│ MOST POPULAR — UNLIMITED PLATFORMS  │  eyebrow gold UPPERCASE
│                                     │
│ $79 /month                          │  display-2 gold tabular + body-md secondary
│ $199 one-time. Yours forever.       │  body-sm secondary
│ Prefer smaller payments?            │  body-sm
│ $9.95/mo over 24 months.            │  body-sm gold link
│ ─────────────────────────────────   │  divider
│ ✓ All 22 platforms                  │  body-md, gold check icons
│ ✓ 5 auto-posts/day                  │
│ ✓ Unlimited quick posts             │
│ ✓ AI replies — 1,000 DMs/month      │
│ ✓ Product catalog — 1,000 items     │
│ ✓ Real-time analytics               │
│                                     │
│ [Start my 7-day free trial]         │  primary CTA full-width
│ No credit card required • Cancel    │  microcopy --text-tertiary
└─────────────────────────────────────┘
```

### Bento tile (integrations grid)

- Background: `--surface-raised`
- Border: `1px solid var(--border-subtle)`
- Border-radius: `var(--radius-lg)` (16px)
- Aspect ratio: 1:1
- Three sizes:
  - **Large** 120×120px (major networks: facebook, instagram, tiktok, youtube, x, linkedin, threads, pinterest)
  - **Medium** 96×96px (messaging: telegram, whatsapp, discord, viber, snapchat)
  - **Small** 72×72px (regional: kakaotalk, line, reddit + future-deferred)
- Content: centered platform icon SVG from `social_icons/<name>-tile-dark.svg`
- Hover: lift 3px + border becomes `--brand-gold` + tooltip «Connect in 1 click»
- «Coming soon» state: `opacity: 0.4`, no hover effect

### Accordion item

- Card-flat style with `--surface-raised` background
- Padding: `var(--space-5) var(--space-6)` (20px 24px)
- Question row: body-md, weight 500 + chevron icon right (rotates 180° on open)
- Answer reveal: `200ms slide-down + fade`, `--ease-open`
- **Single-open behavior** for FAQ (only one item open at a time)
- Border between items: `1px solid var(--border-subtle)`

### Dropdown / Select menu

- Trigger: same style as text input + chevron-down icon
- Menu: `--surface-overlay` bg, `--border-subtle`, `--shadow-xl`, `--radius-md`, max-height 320px
- Items: padding 8px 12px, font-size 14px
- Hover: `--surface-elevated` bg
- Selected: `--brand-gold-tint` bg + gold ✓ on right
- Animation: fade + 4–8px Y offset, 200ms `--ease-open`

### Modal / Dialog (native `<dialog>` recommended)

```css
dialog {
  width: min(640px, calc(100vw - 32px));
  background: var(--surface-elevated);
  border: 1px solid var(--border-subtle);
  border-radius: var(--radius-xl);
  padding: var(--space-8);
  color: var(--text-primary);
  opacity: 0;
  transform: translateY(10px) scale(0.98);
  transition: opacity 240ms var(--ease-open),
              transform 240ms var(--ease-open),
              display 240ms allow-discrete;
  transition-behavior: allow-discrete;
}

dialog[open] { opacity: 1; transform: translateY(0) scale(1); }

@starting-style {
  dialog[open] { opacity: 0; transform: translateY(10px) scale(0.98); }
}

dialog::backdrop {
  background: rgba(3, 6, 10, 0.56);
  backdrop-filter: blur(6px);
  transition: background-color 180ms var(--ease-ui);
}
```

**Mobile sheets:** slide-up 16-24px translate over 240–300ms instead of scaling.

### Toast notification

- Width: 320–400px
- Background: `--surface-overlay`
- Border-left: 4px state color (`--state-success` / `--state-warning` / `--state-error` / `--state-info`)
- Border-radius: `--radius-md`
- Padding: `--space-4` (16px)
- **Position:** bottom-right desktop, bottom-center mobile
- **Stack:** max 3
- **Auto-dismiss:** 4–7s for success only. Errors / business-critical = stay until dismissed.
- **Animation:** enter 160–220ms (translateX from off-screen), exit 120–160ms (fade)
- `role="status"` for polite, `role="alert"` for assertive (sparingly)

### Skeleton loader

```css
.skeleton {
  position: relative;
  overflow: hidden;
  border-radius: var(--radius-md);
  background: rgba(255, 255, 255, 0.06);
}

.skeleton::after {
  content: "";
  position: absolute;
  inset: 0;
  transform: translateX(-100%);
  background: linear-gradient(
    90deg,
    transparent,
    rgba(255, 255, 255, 0.08),
    transparent
  );
  animation: shimmer 1.4s linear infinite;
}

@keyframes shimmer { to { transform: translateX(100%); } }
```

Shimmer cycle 1.2–1.6s — slow, low-contrast. NEVER bright metallic sweep.

---

## Organisms

### Header (sticky, glass-morphic)

- Height: 64px desktop, 56px mobile
- Background: `rgba(10, 10, 10, 0.7)` + `backdrop-filter: blur(16px) saturate(180%)`
- Border-bottom: `1px solid var(--border-subtle)`
- **Left:** TEXT wordmark «SmashOne» in `var(--font-display)` weight 650, font-size 22px, letter-spacing -0.02em, color `var(--text-strong)`. NO image logo.
- **Center/Right:** simple text nav — Pricing · Automator program · Sign in
- **Far right:** primary CTA button (compact, "Start free trial")
- **Mobile:** hamburger menu, full-screen overlay nav
- **Scroll behavior:** at scroll > 100px, optionally reduce wordmark to 18px (compact mode)

### Footer (multi-column)

- Background: `var(--surface-base)` (or slightly elevated `--surface-raised`)
- Top section: 5 columns desktop, 2 columns tablet, 1 column mobile

| Column | Content |
|---|---|
| 1 — Brand block | TEXT wordmark «SmashOne» (Geist Variable, weight 650, 18px) + tagline body-sm secondary + jurisdiction text «🇺🇸 United States» (or applicable region) |
| 2 — Product | Pricing, Features, Integrations, Demo, Roadmap |
| 3 — Company | About, Blog, Careers, Press |
| 4 — Resources | Help center, API docs, Status, Community |
| 5 — Legal | Terms, Privacy, Refund policy, Cookie policy |

Bottom strip (`--surface-elevated`, `--border-subtle` divider above):
- **Left:** entity legal text (e.g., «© 2026 SMASHONE CORPORATION • Florida C-Corp • P26000023598»)
- **Center:** small social icon row (use `social_icons/x-tile-dark-official.svg`, `linkedin-tile-dark.svg`, `youtube-tile-dark.svg` at 24×24px, opacity 0.7, hover 1.0)
- **Right:** language switcher

### Hero pattern (4-layer composition)

See `design-tokens.md § 11` for full CSS. 4 stacked layers: solid base + tile texture + gold radial glow + vignette. Use only in hero / final-CTA banners / splash / auth pages.

### Section container

```
┌────────────────────────────────────────────┐
│  [Eyebrow label, gold or tertiary]         │  --eyebrow
│                                            │
│  Section heading (--h2 or --display-3)     │  --text-strong
│                                            │
│  Subhead — body-lg, --text-secondary       │
│                                            │
│  ─── content area ───                      │
└────────────────────────────────────────────┘
```

- Section vertical padding: `--space-20` desktop, `--space-12` mobile
- Max content width: 1200px on desktop, full-bleed bg

### Validation strip

- Single horizontal band immediately below hero
- Eyebrow centered: «TRUSTED BY 5,000+ LOCAL BUSINESSES» (or applicable claim)
- Below: 6–8 logo placeholders in monochrome white, 32px height, `opacity: 0.5`
- Right edge: G2 «Leader» badge + Capterra rating widget
- Background: `--surface-base`, `1px solid --border-subtle` top
- Padding: `--space-12` vertical

### Pain / Solution split

Two cards side-by-side, 50/50 desktop, stacked mobile.

- **Pain card (left):** `--surface-raised` + `1px solid rgba(239, 68, 68, 0.15)` (red-tinted) + heading «Without [Product]» + bullets with red ✗ icons
- **Solution card (right):** `--surface-raised` + `1px solid var(--brand-gold-glow)` + heading «With [Product]» + bullets with gold ✓ icons

### Persona card grid

- 4-up desktop (4×1), 2-up tablet (2×2), 1-up mobile
- Each card: `--surface-raised`, `--border-subtle`, `--radius-lg`, padding `--space-8`
- Content: gold icon top + h4 industry name + body-md secondary outcome line + micro-CTA «See how →»
- Hover: lift 3px + gold border + `--shadow-lg`

### Final CTA banner

- Full-width band, repeating tile bg at 5% + centered gold radial glow
- H2 centered (display-3, `--text-strong`)
- Subhead body-lg `--text-secondary`
- Single primary CTA, large size (height 56px)
- Microcopy below CTA: «No credit card required • Cancel anytime»
- Padding: `--space-20` to `--space-24` vertical

---

## Iron rules summary

See `design-tokens.md § 12` for the full canonical list. Key reminders for component implementation:

1. **Sentence case** in all button text, headings, body. UPPERCASE only for eyebrow labels (11–12px tracking 0.08em).
2. **First-person CTAs** — «Start my trial», never «Start your trial».
3. **Tabular numbers** for prices, dashboards, metrics.
4. **Focus indicators always visible** — 2px gold outline + 4px offset.
5. **Wordmark as TEXT** — never embed logo image.
6. **All animations gated** by `prefers-reduced-motion`.
7. **NO bounce/elastic motion** in product UI.
8. **WCAG 2.2 AA minimum**, AAA for hero / pricing / CTA copy.
