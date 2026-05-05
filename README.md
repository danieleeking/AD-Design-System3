# AD Design System

**AI-First Material Design 3 system for Affiliated Distributors.**  
39 components · 6 page patterns · 7 foundation token sets · Light + dark mode · Template Machine for new brands.

---

## Color System

Built on Google's Material Design 3 tonal palette algorithm from three source colors.

| Role | Token | Light Mode | Dark Mode | Usage |
|------|-------|-----------|-----------|-------|
| Primary | T40 / T80 | `#4c6842` | `#b3d0a9` | App bars, nav, CTAs, active states |
| Secondary | T40 / T80 | `#494e52` | `#b4bec2` | Supporting chrome, labels, inactive states |
| Tertiary | T40 / T80 | `#885400` | `#f2cc88` | Badges, accents, links, action highlights |

**Color ratio rule — 70 / 15 / 15** across all page patterns:
- **70%** Primary — structural dominance (nav, app bars, CTAs, fills)
- **15%** Secondary — supporting chrome (labels, inactive states, secondary actions)
- **15%** Tertiary — accent energy (badges, links, highlights, draft/export buttons)

---

## Typography

| Font | Weight | Usage |
|------|--------|-------|
| [Arvo](https://fonts.google.com/specimen/Arvo) | 700 | Display headlines only — single h1 per screen, 24px or larger |
| [Inter](https://fonts.google.com/specimen/Inter) | 500 | Section titles, card headers, labels, nav links, metric values |
| [Inter](https://fonts.google.com/specimen/Inter) | 400 | Body copy, table data, helper text, captions |

**Arvo rule:** One instance per screen maximum. Never for subheads, card titles, or any text below 24px. If in doubt, use Inter 500.

Font delivery via [Fontsource](https://fontsource.org/) — `unpkg.com/@fontsource/arvo/700.css` and `unpkg.com/@fontsource/inter/400.css` / `500.css`.

---

## What's Included

### Foundation Tokens (7 sets)
Colors · Typography · Spacing (8pt grid, 14 steps) · Elevation (6 tonal levels, no drop shadows) · Motion (4 easing curves, duration scale) · Border Radius (4px / 8px / 12px) · Logo

### Components (39)

| Category | Components |
|----------|-----------|
| Actions | Button (filled, outlined, tonal, text) · FAB · Icon Button · Segmented Button |
| Inputs | Text Field (filled, outlined) · Checkbox · Radio Button · Switch · Slider |
| Navigation | Top App Bar · Navigation Bar · Navigation Drawer · Tabs |
| Containment | Card (elevated, filled, outlined) · Dialog · List · Accordion |
| Display | Badge · Chip (filter, input) · Divider · Progress Indicator · Tooltip |
| Communication | Banner / Alert · Snackbar · Search Bar · Menu |
| Data | Data Table |

### Page Patterns (6)

| Page | Color Ratio | Key Components |
|------|-------------|---------------|
| Login | 70/15/15 | App bar, form card, text fields, SSO button, error state |
| Dashboard | 70/15/15 | Metrics grid, orders table, rebate card, quick actions |
| Data Table | 70/15/15 | Search, filter toolbar, sortable table, status badges, pagination |
| Form | 70/15/15 | 4-step stepper, 3 form sections, all control types |
| Profile | 70/15/15 | Hero strip, stats grid, tier progress, activity timeline |
| Settings | 70/15/15 | Category nav, toggle rows, select dropdowns, danger zone |

All page patterns include light mode and dark mode.

### Textures (2)

| Texture | Tile | Opacity | Best Surfaces |
|---------|------|---------|--------------|
| Dot Grid | 18px · 1.2px radius | 15% light / 12% dark | Dashboard, Data Table, Settings, Form backgrounds |
| Diagonal Lines | 12px · 0.8px stroke · 45° | 15% light / 12% dark | Hero strips, Login hero, banner sections |

---

## Directory Structure

```
AD-Design-System/
├── README.md
├── LICENSE
├── CHANGELOG.md
│
├── tokens/
│   └── AD_design_system_v1.json      # Complete token + component spec
│
├── assets/
│   ├── logo/
│   │   ├── AD_logo_white.svg          # White version — for dark/colored backgrounds
│   │   └── AD_logo_green.svg          # Green version — for light backgrounds
│   └── textures/
│       ├── texture_dot_grid.svg       # 18px dot grid pattern tile
│       └── texture_diagonal_lines.svg # 12px diagonal line pattern tile
│
└── docs/
    ├── getting-started.md             # How to use and adapt the system
    ├── colors.md                      # Full color palette reference
    ├── typography.md                  # Font rules and scale
    ├── components.md                  # Component token reference
    ├── page-patterns.md               # Page pattern specifications
    ├── textures.md                    # Texture usage guidelines
    └── template-machine.md            # How to fork this for a new brand
```

---

## Template Machine — Fork for a New Brand

This system was designed to be re-skinned. To create a new design system from this template:

1. **Duplicate** `tokens/AD_design_system_v1.json` → rename for your new brand
2. **Replace** `source_colors` — provide three hex values: primary, secondary, tertiary
3. **Regenerate** M3 tonal palettes using the same algorithm (13 tones per palette)
4. **Swap** the logo SVG paths in `assets/logo/`
5. **Adjust** border radius tokens if the new brand calls for a different radius scale
6. **Update** `meta` — company name, brand voice, context notes

Components, spacing, elevation, and motion tokens carry over as-is. You're re-skinning, not rebuilding.

See [`docs/template-machine.md`](docs/template-machine.md) for the full walkthrough.

---

## Design Language

- **1px strokes** on all form controls, borders, and dividers — no 2px or thicker borders on interactive elements
- **No drop shadows** — elevation communicated through surface color shifts (tonal elevation)
- **No gradients** — flat surfaces only
- **Inline SVG logo** — the AD logo is always embedded as inline SVG, never as an `<img>` tag referencing a file
- **Dark mode** — every component and page pattern ships with a complete dark mode variant
- **Focus rings** — 2px only, never 1px or 3px

---

## Elevation Scale

Elevation is communicated through tonal surface color shifts — not drop shadows.

| Level | Surface | Use |
|-------|---------|-----|
| 0 | Base | Page background |
| 1 | +T5 tint | Cards (default) |
| 2 | +T8 tint | Raised cards |
| 3 | +T11 tint | Navigation drawer |
| 4 | +T12 tint | App bar (scrolled) |
| 5 | +T14 tint | Modals and dialogs |

---

## Motion Tokens

| Token | Duration | Easing | Use |
|-------|----------|--------|-----|
| `duration-short` | 100ms | Standard | Hover states |
| `duration-medium` | 200ms | Standard | Component transitions |
| `duration-long` | 300ms | Emphasized | Page-level transitions |
| `duration-extra-long` | 500ms | Emphasized decelerate | Complex entries |

---

## License

[MIT](LICENSE) — Free to use, adapt, and fork for commercial and personal projects.

---

*Built with the AD AI-First Design System Template Machine · v1.0 · 2026*
