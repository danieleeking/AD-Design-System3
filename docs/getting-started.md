# Getting Started

The AD Design System is a token-first, AI-generated Material Design 3 system built for Affiliated Distributors. It ships as a structured JSON specification alongside SVG assets and markdown documentation.

---

## What You're Working With

The system is **not a code component library** — it's a design specification and token set. It defines every visual decision (colors, spacing, typography, elevation, motion, component states) in a machine-readable format that developers translate into code and designers use in their tools.

The core file is `tokens/AD_design_system_v1.json`. Everything else — docs, assets, page patterns — is derived from or references that file.

---

## Reading the Token File

Open `tokens/AD_design_system_v1.json`. The top-level keys are:

| Key | Contents |
|-----|----------|
| `_template_machine` | Rules for forking this system for a new brand |
| `meta` | Company info, brand voice, system context |
| `source_colors` | The 3 seed hex values the entire palette derives from |
| `palettes` | Full M3 tonal palettes — 13 tones × 6 palette groups |
| `tokens` | Semantic color roles, typography, spacing, elevation, motion, radius |
| `logo` | Logo rules, SVG paths, sizing and usage guidelines |
| `components` | All 39 components — token values for every variant and state |
| `textures` | Dot Grid and Diagonal Lines — spec, CSS implementation, usage rules |
| `pages_patterns` | 6 page patterns — layout, color distribution, component usage |
| `session_log` | Full decision history from every design session |

---

## Using Tokens in Code

### Colors

Reference semantic color roles, not raw palette values:

```css
/* Do this */
background: var(--color-primary);
color: var(--color-on-primary);

/* Not this */
background: #4c6842;
```

Token values for light and dark mode are documented in `docs/colors.md`.

### Typography

```css
/* Display headlines only */
.page-title {
  font-family: 'Arvo', Georgia, serif;
  font-weight: 700;
  font-size: 24px; /* minimum for Arvo usage */
}

/* All other text */
.section-title {
  font-family: 'Inter', sans-serif;
  font-weight: 500;
}

.body-text {
  font-family: 'Inter', sans-serif;
  font-weight: 400;
}
```

Load fonts from Fontsource (not Google Fonts — blocked in sandboxed environments):

```html
<link href="https://unpkg.com/@fontsource/arvo/700.css" rel="stylesheet">
<link href="https://unpkg.com/@fontsource/inter/400.css" rel="stylesheet">
<link href="https://unpkg.com/@fontsource/inter/500.css" rel="stylesheet">
```

### Applying Textures

```css
/* Dot Grid — page background */
.page-bg {
  background-color: #f4f6f4;
  background-image: url('../assets/textures/texture_dot_grid.svg');
  background-size: 18px 18px;
  background-repeat: repeat;
}

/* Overlay approach (keeps texture separate from base color) */
.page-bg::before {
  content: '';
  position: absolute;
  inset: 0;
  background-image: url('../assets/textures/texture_dot_grid.svg');
  background-size: 18px 18px;
  opacity: 0.15; /* light mode */
  pointer-events: none;
}

/* Dark mode */
@media (prefers-color-scheme: dark) {
  .page-bg::before {
    opacity: 0.12; /* slightly reduced — dark bg amplifies contrast */
  }
}
```

---

## Logo Usage

Always embed the AD logo as **inline SVG** — never as an `<img>` tag. This ensures it inherits color context and renders at any size without quality loss.

```html
<!-- White version — for primary green or dark backgrounds -->
<svg width="120" height="80" viewBox="0 0 432 288">
  <polygon points="190.28 72.04 ..." fill="#fff"/>
  <path d="M86.74,182.32h50.69..." fill="#fff"/>
  <path d="M354.1,97.37h-41.4..." fill="#fff"/>
</svg>
```

Full SVG paths are in `assets/logo/AD_logo_white.svg` and `assets/logo/AD_logo_green.svg`.

Standard sizes: 120×80px (page headers) · 90×60px (compact headers) · 72×48px (app bars).

---

## Next Steps

- [`docs/colors.md`](colors.md) — Full palette and semantic role reference
- [`docs/typography.md`](typography.md) — Font scale and usage rules
- [`docs/components.md`](components.md) — Component token reference
- [`docs/page-patterns.md`](page-patterns.md) — Page pattern specifications
- [`docs/textures.md`](textures.md) — Texture implementation guide
- [`docs/template-machine.md`](template-machine.md) — Fork for a new brand
