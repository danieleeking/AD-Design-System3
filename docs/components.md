# Components

The AD Design System includes 39 components across 7 categories. Every component ships with:
- Token values for all variants and states
- Light mode and dark mode specifications
- 1px border language throughout
- Inline SVG where applicable (checkbox, radio)

Full token definitions are in `tokens/AD_design_system_v1.json` under the `components` key.

---

## Actions

### Button
4 variants · All states (default, hover, pressed, focused, disabled)

| Variant | Background | Border | Text |
|---------|-----------|--------|------|
| Filled | `#4c6842` (primary) | none | `#ffffff` |
| Outlined | transparent | `#4c6842` 1px | `#4c6842` |
| Tonal | `#cde3c4` (primary T90) | none | `#1f3a1a` |
| Text | transparent | none | `#4c6842` |

Border radius: 4px. Height: 36–40px. Font: Inter 500, 12px.

### FAB (Floating Action Button)
4 color variants (surface, primary, secondary, tertiary) · 3 sizes (regular, small, large)

### Icon Button
Standard and outlined variants · All states

### Segmented Button
Single select · Multi-select · Icon variants · All states

---

## Inputs

### Text Field
2 variants (filled, outlined) · 5 states (default, focused, error, disabled, populated)

- **Border:** 1px solid `rgba(0,0,0,0.20)` default · `#4c6842` focused
- **Focus ring:** 2px `rgba(76,104,66,0.15)` glow
- **Error state:** `#dc2626` border · error message below in Inter 400, 9px
- **Height:** 36px (standard) · 32px (compact)
- **Border radius:** 4px

### Checkbox
3 variants (unselected, selected, indeterminate) · 6 states

- **Stroke:** SVG `stroke-width="1"` — always 1px, never CSS border
- **Selected fill:** `#4c6842` (primary)
- **Checkmark:** White SVG polyline, 1px stroke

### Radio Button
2 variants (unselected, selected) · 6 states

- **Stroke:** SVG `stroke-width="1"` — 1px circle border
- **Selected dot:** `#4c6842`, 7px diameter

### Switch
All states · Light + dark

### Slider
3 variants (continuous, discrete, range) · All states

---

## Navigation

### Top App Bar
- Height: 56px
- Background: `#4c6842` (primary)
- Logo: Inline SVG, white fill, 72–120px width
- Shadow: none (tonal elevation only)

### Navigation Bar
Bottom navigation · All states

### Navigation Drawer
- Width: 152px (compact portal nav)
- Background: `#2f5229` (primary T30)
- Active item: `border-left: 2px solid #f2cc88` (tertiary) + `rgba(255,255,255,0.11)` bg
- Section labels: Inter 500, 9px, uppercase, `rgba(255,255,255,0.38)`

### Tabs
3 variants (primary text, primary icon+label, secondary) · All states
- Active indicator: 2px solid (primary or tertiary)

---

## Containment

### Card
3 variants · All states

| Variant | Background | Border | Elevation |
|---------|-----------|--------|-----------|
| Elevated | `#ffffff` | `1px rgba(0,0,0,0.09)` | Tonal level 1 |
| Filled | `#f4f6f4` | none | Tonal level 0 |
| Outlined | `#ffffff` | `1px rgba(0,0,0,0.14)` | none |

Border radius: 8px (cards use `sm` radius, not `xs`).

### Dialog
3 variants (standard, fullscreen, confirmation) · All states
- Border radius: 12px (`md`)
- Overlay: `rgba(0,0,0,0.45)`

### List
All variants · Hover, selected, disabled states

### Accordion
3 variants (standalone, icon+subtitle, group) · All states
- Chevron animation: 220ms standard easing

---

## Display

### Badge
2 variants · 5 semantic colors

| Type | Size | Shape |
|------|------|-------|
| Status dot | 4px | Circle |
| Count pill | Auto | Pill (border-radius: 9999px) |

Colors: primary (green) · secondary (slate) · tertiary (amber) · error (red) · warning (orange)

### Chip
2 variants (filter, input) · All states

### Divider
Horizontal and vertical · 1px stroke · `rgba(0,0,0,0.09)`

### Progress Indicator
Linear and circular · Determinate and indeterminate

### Tooltip
Standard and rich variants · All positions

---

## Communication

### Banner / Alert
4 semantic types (info, success, warning, error) · Full-width and inline variants

| Type | Background | Border | Icon |
|------|-----------|--------|------|
| Info | `#d1dadd` | secondary | ℹ |
| Success | `#cde3c4` | primary | ✓ |
| Warning | `#fae3bc` | tertiary | ⚠ |
| Error | `#fde8e8` | `rgba(220,38,38,0.30)` | ✕ |

### Snackbar
Standard and action variants

### Search Bar
All states (empty, focused, populated, results showing)

### Menu
Standard and context menu variants

---

## Data

### Data Table
Full-featured table with:
- Sortable column headers (sorted column highlights in tertiary amber `#f2cc88`)
- Row selection with checkboxes (1px SVG)
- Bulk action toolbar (appears on selection)
- 5 status badge variants (delivered, shipped, pending, processing, cancelled)
- Hover row state: `#f0f4ef` (primary T95 tint)
- Pagination controls with primary-filled active page

Column header background: `#494e52` (secondary T40) with white Inter 500 text.

---

## Design Rules Across All Components

- **Borders:** 1px on all interactive controls — never 2px or thicker
- **Focus rings:** 2px only — `0 0 0 2px rgba(76,104,66,0.15)` on light, adjusted for dark
- **Border radius:** 4px (inputs, buttons, chips) · 8px (cards) · 12px (dialogs)
- **Dark mode:** Every component has a complete dark variant — no exceptions
- **Disabled state:** 38% opacity on all disabled interactive elements
