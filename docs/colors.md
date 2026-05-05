# Color System

The AD color system is built on Google's Material Design 3 tonal palette algorithm. Three source colors generate complete 13-tone palettes, from which semantic roles are assigned for every UI surface, text, border, and state.

---

## Source Colors

| Name | Hex | Role |
|------|-----|------|
| Forest Green | `#4c6842` | Primary — structural dominance |
| Steel Slate | `#494e52` | Secondary — supporting chrome |
| Warm Amber | `#885400` | Tertiary — accent energy |

The tertiary color was derived using M3's 60° hue offset rule from the primary source.

---

## Primary Palette — Forest Green

| Tone | Hex | Usage |
|------|-----|-------|
| T10 | `#0d1f0a` | Deepest surface (dark mode backgrounds) |
| T20 | `#1f3a1a` | Dark primary text, hero headlines |
| T30 | `#2f5229` | Nav sidebar background, hero strips |
| T40 | `#4c6842` | **Primary — light mode** (buttons, app bars, active states) |
| T50 | `#5e7f54` | Hover state on primary elements |
| T60 | `#77996e` | Medium primary — dividers, borders |
| T70 | `#91b389` | Light primary — tints |
| T80 | `#b3d0a9` | **Primary — dark mode** |
| T90 | `#cde3c4` | Light tint — hero strips, stat card bg |
| T95 | `#dff0d8` | Lightest tint |
| T99 | `#f4faf1` | Near-white primary surface |

---

## Secondary Palette — Steel Slate

| Tone | Hex | Usage |
|------|-----|-------|
| T20 | `#1e2528` | Deepest secondary surface |
| T30 | `#373f43` | Dark secondary — table headers |
| T40 | `#494e52` | **Secondary — light mode** |
| T80 | `#b4bec2` | **Secondary — dark mode** |
| T90 | `#d1dadd` | Light secondary tint |
| T95 | `#eef2f4` | Near-white secondary surface |

---

## Tertiary Palette — Warm Amber

| Tone | Hex | Usage |
|------|-----|-------|
| T20 | `#4a2e00` | Deepest amber — dark mode danger |
| T30 | `#6d4400` | Dark amber text |
| T40 | `#885400` | **Tertiary — light mode** (badges, links, accents) |
| T80 | `#f2cc88` | **Tertiary — dark mode** |
| T90 | `#fae3bc` | Light amber tint — pending badges, draft surfaces |

---

## Semantic Color Roles

### Light Mode

| Role | Token | Hex | Usage |
|------|-------|-----|-------|
| `primary` | T40 | `#4c6842` | Filled buttons, FAB, active nav |
| `on-primary` | T100 | `#ffffff` | Text/icons on primary surfaces |
| `primary-container` | T90 | `#cde3c4` | Tonal button fill, hero strip |
| `on-primary-container` | T10 | `#0d1f0a` | Text on primary-container |
| `secondary` | T40 | `#494e52` | Outlined button border, inactive nav |
| `on-secondary` | T100 | `#ffffff` | Text on secondary surfaces |
| `secondary-container` | T90 | `#d1dadd` | Secondary tonal surfaces |
| `tertiary` | T40 | `#885400` | Links, badges, accents, SSO button |
| `on-tertiary` | T100 | `#ffffff` | Text on tertiary surfaces |
| `tertiary-container` | T90 | `#fae3bc` | Pending badges, draft surfaces |
| `surface` | — | `#ffffff` | Card backgrounds |
| `surface-variant` | — | `#f4f6f4` | Page background |
| `on-surface` | — | `#1a1c1a` | Primary text |
| `on-surface-variant` | — | `#44483f` | Secondary text |
| `outline` | — | `rgba(0,0,0,0.20)` | Default border |
| `outline-variant` | — | `rgba(0,0,0,0.09)` | Subtle dividers |

### Dark Mode

| Role | Hex |
|------|-----|
| `primary` | `#b3d0a9` |
| `on-primary` | `#1f3a1a` |
| `primary-container` | `#2f5229` |
| `secondary` | `#b4bec2` |
| `secondary-container` | `#373f43` |
| `tertiary` | `#f2cc88` |
| `tertiary-container` | `#6d4400` |
| `surface` | `#1c1f1b` |
| `surface-variant` | `#141714` |
| `on-surface` | `#e2e4de` |
| `on-surface-variant` | `#b8bcb2` |

---

## Semantic Status Colors

Used for status badges, banners, and alerts — independent of the 70/15/15 ratio.

| State | Background | Text | Usage |
|-------|-----------|------|-------|
| Success / Delivered | `#cde3c4` | `#1f3a1a` | Delivered orders, success banners |
| Info / Shipped | `#d1dadd` | `#373f43` | Shipped orders, info states |
| Warning / Pending | `#fae3bc` | `#6d4400` | Pending orders, draft states |
| Processing | `#e8f4e3` | `#2f5229` | Processing orders, loading states |
| Error / Cancelled | `#fde8e8` | `#7a1c1c` | Errors, cancelled orders |

---

## Color Ratio Rule

All page patterns use a **70 / 15 / 15** distribution:

- **Primary (70%)** — app bars, nav sidebars, CTA buttons, hero tints, fills, active states, progress bars
- **Secondary (15%)** — table headers, field labels, helper text, inactive states, secondary actions, footer bars
- **Tertiary (15%)** — links, badges, SSO/export/draft buttons, nav badge fills, highlights, eyebrow labels

This ratio is a visual weight guideline, not a pixel-precise measurement. Apply it when composing page layouts to ensure the brand color hierarchy reads correctly.
