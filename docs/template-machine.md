# Template Machine — Fork for a New Brand

The AD Design System was architected from the start to be re-skinned. The Template Machine is the set of instructions embedded in the token file that lets you create a complete new design system by changing only the brand-specific inputs.

---

## What Changes vs. What Stays

| Stays the same | Changes |
|----------------|---------|
| All 39 component structures | Source colors (3 hex values) |
| All 6 page pattern layouts | Tonal palette generation |
| Spacing scale (8pt grid) | Semantic color role assignments |
| Elevation model (tonal, no shadows) | Logo SVG paths |
| Motion tokens | Meta / company name |
| Border radius scale | Border radius values (optional) |
| Typography rules (Arvo + Inter) | Brand voice notes in `meta` |
| Texture patterns | Texture fill colors |
| 70/15/15 color ratio | — |

You are **re-skinning**, not rebuilding. The system's architecture, component count, page patterns, and design language are all preserved.

---

## Step-by-Step

### 1. Duplicate the Token File

```bash
cp tokens/AD_design_system_v1.json tokens/NEWBRAND_design_system_v1.json
```

### 2. Update `meta`

Open the new JSON and update the `meta` section:

```json
"meta": {
  "company": "New Brand Name",
  "industry": "Your industry",
  "brand_voice": "How the brand speaks",
  "primary_use": "What the system is used for"
}
```

### 3. Replace `source_colors`

Provide three hex values — primary, secondary, tertiary:

```json
"source_colors": {
  "primary": "#YOUR_PRIMARY",
  "secondary": "#YOUR_SECONDARY",
  "tertiary": "#YOUR_TERTIARY"
}
```

**Choosing colors:**
- **Primary** — the dominant brand color. Used for 70% of the UI. Should work well at both dark (buttons/navbars) and light tint (backgrounds/cards) versions.
- **Secondary** — a neutral or complementary color. Often a slate, gray, or muted tone. Used for supporting chrome.
- **Tertiary** — M3 recommends a 60° hue offset from primary for visual harmony. Used for accents, badges, and highlights.

### 4. Regenerate Tonal Palettes

Using the M3 algorithm, generate 13 tones (T0 through T100) for each source color. The key tones used in the system are T20, T30, T40, T80, T90.

Tools for M3 palette generation:
- [Material Theme Builder](https://m3.material.io/theme-builder)
- [Material Color Utilities](https://github.com/material-foundation/material-color-utilities) (npm package)

Update the `palettes` section in the JSON with the generated values.

### 5. Update Semantic Color Roles

Update `tokens.colors.light` and `tokens.colors.dark` with values from your new palettes. The role names stay identical — only the hex values change.

### 6. Swap the Logo

Replace the SVG paths in `assets/logo/` with your new brand's logo. Update the `logo` section in the JSON with:
- New `viewBox` dimensions
- New inline SVG path data
- Any updated sizing rules

### 7. Adjust Border Radius (Optional)

If the new brand calls for a different corner radius style:

```json
"border_radius": {
  "xs": "2px",   // was 4px — sharper
  "sm": "6px",   // was 8px
  "md": "10px",  // was 12px
  "full": "9999px"
}
```

Round brands typically use 8px+ defaults. Precise/technical brands use 2–4px. AD uses 4px (precise, industrial).

### 8. Update Texture Colors

In `textures`, update `color` values for both textures to the new primary color:

```json
"light_mode": {
  "color": "#YOUR_PRIMARY_T40"
},
"dark_mode": {
  "color": "#YOUR_PRIMARY_T80"
}
```

### 9. Rename and Ship

Rename all references from `AD` to your new brand name. The component structures, page patterns, and documentation templates are now ready for the new brand.

---

## What a Full Re-skin Takes

A complete new brand design system using this template typically requires:

| Phase | Work | Time |
|-------|------|------|
| Color generation + approval | Source colors → palettes → token review | 1 session |
| Component spot-check | Verify 5–10 key components render correctly with new colors | 1 session |
| Page pattern adaptation | Update 6 page patterns with new brand context + copy | 2–3 sessions |
| Asset swap | Logo, textures, any brand-specific icons | 1 session |

The bulk of the work — all 39 component structures, all spacing/elevation/motion rules, the 70/15/15 ratio system — carries over without change.
