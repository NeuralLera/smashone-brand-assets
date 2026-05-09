# SmashOne Design Tokens — v2 (Dark Theme 2026)

> Canonical CSS design tokens for the SmashOne brand. Use these verbatim in any Claude Design project, product code, or marketing artifact.
>
> **System version:** v2 (established 2026-05-09)
> **Theme:** dark only (light variants deferred to future v3)

---

## 1. Surfaces (4-tier elevation)

```css
--surface-base:     #0a0a0a;   /* Layer 0 — body canvas */
--surface-raised:   #11151b;   /* Layer 1 — primary cards, panels, sidebars */
--surface-elevated: #151b22;   /* Layer 2 — nested cards, hover states */
--surface-overlay:  #1a212a;   /* Layer 3 — modals, popovers, command palettes */
```

**Rule:** each tier steps up ~5–8% luminance. NEVER use the same surface color for two adjacent stacked elements. NO pure `#000000` (depth becomes impossible — drop shadows invisible, halation absent).

---

## 2. Text (white via opacity, 6 levels)

```css
--text-strong:    rgba(255, 255, 255, 0.96);  /* hero, primary KPIs */
--text-primary:   rgba(255, 255, 255, 0.88);  /* body, headings */
--text-secondary: rgba(255, 255, 255, 0.70);  /* helper text, descriptions */
--text-tertiary:  rgba(255, 255, 255, 0.54);  /* captions, eyebrow labels */
--text-quiet:     rgba(255, 255, 255, 0.50);  /* filters, chips, chrome */
--text-disabled:  rgba(255, 255, 255, 0.36);  /* disabled inputs/buttons */
```

**Rule:** use one foreground color (white) at varying opacities — NEVER arbitrary grays.

---

## 3. Borders (light-catcher, transparent white)

```css
--border-subtle:   rgba(255, 255, 255, 0.08);  /* card outlines, dividers */
--border-strong:   rgba(255, 255, 255, 0.12);  /* active outlines, focus rings */
--border-emphasis: rgba(255, 255, 255, 0.16);  /* card hover states */
```

---

## 4. Brand

```css
--brand-gold:       #c9a646;                       /* primary CTAs, focus, key data viz */
--brand-gold-text:  #d4b46e;                       /* AAA-compliant body text variant */
--brand-gold-glow:  rgba(201, 166, 70, 0.30);      /* hover shadows, ambient glow */
--brand-gold-tint:  rgba(201, 166, 70, 0.05);      /* subtle background tinting */
```

**60-30-10 distribution rule:**
- 60% surface-base neutral
- 30% secondary surfaces + grays via opacity
- 10% brand gold (CTAs + focus + active states + positive data viz)

NEVER fill large areas with `--brand-gold`. It is a conversion anchor, not a fill.

---

## 5. State colors (dark-tuned)

Desaturated 10–15% + boosted luminance vs light theme equivalents to prevent edge vibration.

```css
--state-success:  #10B981;
--state-warning:  #F59E0B;
--state-error:    #EF4444;
--state-info:     #3B82F6;

/* Tinted backgrounds for state surfaces */
--state-success-bg: rgba(16, 185, 129, 0.10);
--state-warning-bg: rgba(245, 158, 11, 0.10);
--state-error-bg:   rgba(239, 68, 68, 0.10);
--state-info-bg:    rgba(59, 130, 246, 0.10);
```

---

## 6. Typography

### Font stack

```css
--font-display: "Geist Variable", "InterVariable", Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", sans-serif;
--font-body:    "InterVariable", Inter, "IBM Plex Sans", ui-sans-serif, system-ui, -apple-system, "Segoe UI", sans-serif;
--font-mono:    "IBM Plex Mono", "Geist Mono", "SF Mono", ui-monospace, "Cascadia Code", "JetBrains Mono", Consolas, monospace;
```

All three are open-source (OFL). Self-host or load via Google Fonts.

### Type scale (full ladder)

| Token | Size | Line-height | Tracking | Weight | Use |
|---|---:|---:|---:|---:|---|
| `--display-1` | 72px | 76px | -0.040em | 650 | Hero headline (one per page) |
| `--display-2` | 56px | 60px | -0.035em | 650 | Section opener |
| `--display-3` | 48px | 52px | -0.030em | 640 | Tertiary display |
| `--h1` | 40px | 48px | -0.024em | 620 | Page heading |
| `--h2` | 32px | 40px | -0.020em | 620 | Section heading (workhorse) |
| `--h3` | 28px | 36px | -0.016em | 610 | Sub-section |
| `--h4` | 24px | 32px | -0.012em | 600 | Card heading |
| `--h5` | 20px | 28px | -0.008em | 600 | Minor heading |
| `--h6` | 18px | 26px | -0.004em | 580 | Caption-grade heading |
| `--body-lg` | 18px | 30px | 0em | 450 | Lead paragraphs, hero subheads |
| `--body-md` | 16px | 26px | 0em | 450 | Default body text |
| `--body-sm` | 14px | 22px | 0.002em | 450 | Helper, secondary body |
| `--label-md` | 13px | 18px | 0.01em | 550 | Form labels, table headers |
| `--label-sm` | 12px | 16px | 0.04em | 560 | Compact UI labels |
| `--eyebrow` | 11px | 14px | 0.08em | 600 | UPPERCASE eyebrow above headings |
| `--code-lg` | 14px | 22px | 0em | 500 | Code blocks |
| `--code-md` | 13px | 20px | 0em | 500 | Inline code, metrics |

### Typography rules

- **Sentence case everywhere** except `--eyebrow` labels (UPPERCASE 11–12px tracking 0.08em)
- **Body weight 450** (NOT 500 default — dark theme reads heavier)
- **Tighten tracking as size grows; loosen as size shrinks**
- **Tabular numbers** for prices, dashboards, metrics, tables: `font-variant-numeric: tabular-nums lining-nums; font-feature-settings: "tnum" 1, "lnum" 1;`
- **Currency symbols** at 0.78em on the same baseline as digits — NEVER superscript
- **Pricing format:** `$79` without `.00` (cents only when genuinely billable)

### Wordmark

Rendered as **TEXT**, never as image:

```css
.wordmark {
  font-family: var(--font-display);  /* Geist Variable */
  font-weight: 650;
  letter-spacing: -0.02em;
  color: var(--text-strong);
  font-size: 22px;  /* default header size */
}

.wordmark--lg { font-size: 32px; }   /* hero, marketing display */
.wordmark--sm { font-size: 18px; }   /* footer, compact */
```

---

## 7. Spacing scale

```css
--space-0:   0;
--space-1:   4px;
--space-2:   8px;
--space-3:   12px;
--space-4:   16px;
--space-5:   20px;
--space-6:   24px;
--space-8:   32px;
--space-10:  40px;
--space-12:  48px;
--space-16:  64px;
--space-20:  80px;
--space-24:  96px;
--space-32:  128px;
```

**Section vertical padding:** desktop `--space-20` to `--space-32` (80–128px), mobile `--space-12` to `--space-16` (48–64px).
**Card internal padding (default):** `--space-8` (32px).

---

## 8. Border radius

```css
--radius-xs:    4px;     /* badges, chips, tags */
--radius-sm:    8px;     /* small buttons, inputs */
--radius-md:    12px;    /* default buttons, form fields */
--radius-lg:    16px;    /* cards, bento tiles */
--radius-xl:    20px;    /* modals, large cards, pricing card */
--radius-2xl:   24px;    /* hero containers */
--radius-full:  9999px;  /* pills, avatars, circular CTAs */
```

---

## 9. Shadows (dark-theme tuned)

Lower opacity but larger blur — shadows on dark backgrounds need atmosphere, not weight.

```css
--shadow-sm:    0 1px 2px rgba(0, 0, 0, 0.30);
--shadow-md:    0 4px 12px rgba(0, 0, 0, 0.32);
--shadow-lg:    0 10px 28px rgba(0, 0, 0, 0.36);
--shadow-xl:    0 16px 40px rgba(0, 0, 0, 0.40);
--shadow-glow:  0 0 24px var(--brand-gold-glow);   /* gold ambient glow */
```

---

## 10. Motion

### Easings

```css
--ease-ui:       cubic-bezier(0.2, 0, 0.38, 0.9);   /* routine state changes */
--ease-open:     cubic-bezier(0, 0, 0.38, 0.9);     /* entrances */
--ease-close:    cubic-bezier(0.2, 0, 1, 0.9);      /* exits */
--ease-emphasis: cubic-bezier(0.05, 0.7, 0.1, 1);   /* hero / shared-element */
```

### Durations

```css
--dur-press: 110ms;   /* button press */
--dur-hover: 160ms;   /* hover states */
--dur-card:  200ms;   /* card lift */
--dur-panel: 260ms;   /* drawers, modals */
--dur-page:  220ms;   /* page transitions */
```

### Motion rules

- Single `--ease-ui` for routine surface/state changes
- NEVER bounce, elastic, overshoot — premium SaaS curves only
- All animations gated by `@media (prefers-reduced-motion: reduce)`
- Animate ONLY `transform` + `opacity` (selectively `filter`)
- 60 FPS minimum target

```css
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 1ms !important;
    transition-duration: 1ms !important;
    scroll-behavior: auto !important;
  }
}
```

---

## 11. Tile background composition (4-layer hero)

The canonical hero pattern uses 4 stacked background layers:

```css
.hero {
  position: relative;
  background-color: var(--surface-base);   /* Layer 1: solid base */
}

.hero::before {
  content: "";
  position: absolute; inset: 0;
  background-image: url('logos/smashone-tile-dark/empty-tile-dark.svg');
  background-repeat: repeat;
  background-size: 512px 512px;
  opacity: 0.05;                            /* 3-7% optimal range */
  mix-blend-mode: soft-light;               /* Layer 2: tile texture */
  pointer-events: none;
}

.hero::after {
  content: "";
  position: absolute; inset: 0;
  background: radial-gradient(
    ellipse at center 30%,
    var(--brand-gold-tint) 0%,
    transparent 60%
  );                                        /* Layer 3: gold glow behind CTA */
  pointer-events: none;
}

.hero .vignette {
  position: absolute; inset: 0;
  background: linear-gradient(
    to bottom,
    rgba(0,0,0,0) 60%,
    rgba(0,0,0,0.4) 100%
  );                                        /* Layer 4: vignette focus */
  pointer-events: none;
}

.hero .content {
  position: relative;
  z-index: 1;                               /* content above bg layers */
}

@media (max-width: 768px) {
  .hero::before { background-size: 768px 768px; }   /* +50% mobile, less noise */
}
```

**Use only in:** hero sections, final-CTA banners, splash screens, auth pages.
**NOT in:** body content sections, dashboards, data tables, forms (creates visual noise).

---

## 12. Iron rules (non-negotiable)

1. Dark theme only in v2 (no light variant)
2. Sentence case everywhere except eyebrow UPPERCASE
3. Tabular numbers in pricing/dashboards/tables
4. `$79` without `.00` unless cents billable
5. Brand gold ≤ 10% surface coverage, never large bg fill
6. NO bounce/elastic motion — premium SaaS curves only
7. All animations gated by `prefers-reduced-motion`
8. Focus indicators always visible — 2px gold outline + 4px offset
9. First-person CTA copy («Start my trial» NOT «Start your trial»)
10. Reading level 5th–7th grade — no jargon, quantified outcomes preferred
11. Body weight 450 (NOT 500 — dark theme heavier)
12. NO pure `#000000` — always near-black `#0a0a0a`
13. 4-tier surfaces mandatory — clear z-axis purpose per tier
14. WCAG 2.2 — AA (4.5:1) body, AAA (7:1) hero/pricing/CTA copy
15. Wordmark = TEXT only «SmashOne» in Geist Variable, NO image logo
