# Textures

Two approved texture tokens for the AD Design System. Both are SVG-based repeating patterns applied as semi-transparent overlays on page backgrounds and hero surfaces.

---

## Rules

- **Always as overlays** — never replacing a content surface
- **Cards, inputs, and nav bars are never textured** — UI components sit above the texture layer with full-opacity surfaces
- **15% opacity (light) / 12% opacity (dark)** — the 3% reduction in dark mode accounts for the dark background amplifying perceived contrast
- **Primary color family** — both textures use `#4c6842` (light) / `#b3d0a9` (dark), keeping them within the 70% primary allocation

---

## Texture 01 — Dot Grid

**File:** `assets/textures/texture_dot_grid.svg`

```
Tile size:   18 × 18px
Element:     circle
Center:      (9, 9)
Radius:      1.2px
Fill:        #4c6842 (light) / #b3d0a9 (dark)
Opacity:     15% (light) / 12% (dark)
```

**Best surfaces:** Dashboard, Data Table page, Settings page, Form page, any data-dense neutral background.

**CSS implementation:**

```css
/* Light mode */
.textured-bg {
  position: relative;
  background-color: #f4f6f4;
}
.textured-bg::before {
  content: '';
  position: absolute;
  inset: 0;
  background-image: url('../assets/textures/texture_dot_grid.svg');
  background-size: 18px 18px;
  background-repeat: repeat;
  opacity: 0.15;
  pointer-events: none;
  z-index: 0;
}

/* Dark mode */
@media (prefers-color-scheme: dark) {
  .textured-bg { background-color: #141714; }
  .textured-bg::before { opacity: 0.12; }
}
```

---

## Texture 02 — Diagonal Lines

**File:** `assets/textures/texture_diagonal_lines.svg`

```
Tile size:     12 × 12px
Element:       line
Points:        (0,12) → (12,0)
Angle:         45° (bottom-left to top-right)
Stroke width:  0.8px
Stroke:        #4c6842 (light) / #b3d0a9 (dark)
Opacity:       15% (light) / 12% (dark)
```

**Best surfaces:** Hero strips, Login page hero section, Profile page hero, banner/section accent zones, card accent headers.

**CSS implementation:**

```css
/* Light mode */
.hero-textured {
  position: relative;
  background-color: #cde3c4; /* primary T90 — typical hero bg */
}
.hero-textured::before {
  content: '';
  position: absolute;
  inset: 0;
  background-image: url('../assets/textures/texture_diagonal_lines.svg');
  background-size: 12px 12px;
  background-repeat: repeat;
  opacity: 0.15;
  pointer-events: none;
  z-index: 0;
}

/* Dark mode */
@media (prefers-color-scheme: dark) {
  .hero-textured { background-color: #1f3a1a; }
  .hero-textured::before { opacity: 0.12; }
}
```

---

## Combining Textures with Colored Backgrounds

The textures are designed to work on any of the AD color family backgrounds:

| Background | Texture | Effect |
|-----------|---------|--------|
| `#f4f6f4` (page bg) | Dot Grid | Subtle precision grid on neutral |
| `#cde3c4` (primary T90) | Dot Grid | Green-on-green dot texture |
| `#cde3c4` (hero strip) | Diagonal Lines | Structured hero energy |
| `#2f5229` (dark nav strip) | Diagonal Lines | Dark industrial texture |
| `#1c1f1b` (dark card) | Dot Grid | Refined dark surface |

---

## Opacity Reference

| Context | Opacity | Reason |
|---------|---------|--------|
| Light mode standard | 15% | Approved — subtle and refined |
| Dark mode standard | 12% | Dark bg amplifies contrast — 3% reduction maintains visual equivalence |
| Print / export | 8% | Further reduced for print fidelity |
| High-emphasis hero | 18% | Acceptable maximum — above this the texture competes with content |
