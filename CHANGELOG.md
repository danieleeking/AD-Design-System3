# Changelog

All notable changes to the AD Design System are documented here.  
Format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

---

## [1.0.0] — 2026-05-05

### Added — Foundation Tokens
- Color system: M3 tonal palettes for Primary (`#4c6842`), Secondary (`#494e52`), Tertiary (`#885400`)
- Full semantic color roles for light and dark themes (40+ roles)
- Typography scale: Arvo 700 (display) + Inter 400/500 (all UI text)
- Spacing scale: 8pt base unit, 14 steps
- Elevation scale: 6 tonal levels, no drop shadows
- Motion tokens: 4 easing curves, duration scale (100ms–500ms)
- Border radius scale: 4px (default) / 8px (cards) / 12px (dialogs)
- Logo tokens: inline SVG rules, sizing guidelines, color adaptation rules

### Added — Components (39)
- **Actions:** Button (filled, outlined, tonal, text) — all states, light + dark
- **Actions:** FAB (surface, primary, secondary, tertiary sizes) — all states
- **Actions:** Icon Button — all states
- **Actions:** Segmented Button (single select, multi-select, icon) — all states
- **Inputs:** Text Field (filled + outlined) — 5 states, light + dark
- **Inputs:** Checkbox — all 3 variants, all 6 states, 1px stroke
- **Inputs:** Radio Button — all 2 variants, all 6 states, 1px stroke
- **Inputs:** Switch — all states, light + dark
- **Inputs:** Slider (continuous, discrete, range) — all states
- **Navigation:** Top App Bar — all states, light + dark
- **Navigation:** Navigation Bar — all states
- **Navigation:** Navigation Drawer — all states
- **Navigation:** Tabs (primary text, primary icon+label, secondary) — all states
- **Containment:** Card (elevated, filled, outlined) — all states
- **Containment:** Dialog (standard, fullscreen, confirmation) — all states
- **Containment:** List — all variants
- **Containment:** Accordion (standalone, icon+subtitle, group) — all states
- **Display:** Badge (status 4px dot, count pill) — 5 semantic colors
- **Display:** Chip (filter, input) — all states
- **Display:** Divider — horizontal and vertical
- **Display:** Progress Indicator — linear and circular
- **Display:** Tooltip — all variants
- **Communication:** Banner / Alert — 4 semantic types (info, success, warning, error)
- **Communication:** Snackbar — all variants
- **Communication:** Search Bar — all states
- **Communication:** Menu — all variants
- **Data:** Data Table — sort, select, paginate, bulk action toolbar, 5 status badges

### Added — Page Patterns (6)
- Login page — 70/15/15 color ratio, default + error + loading states
- Dashboard page — 70/15/15, metrics grid, orders table, rebate card, quick actions
- Data Table page — 70/15/15, search + filter toolbar, sortable table, pagination
- Form page — 70/15/15, 4-step stepper, 3 form sections, all control types
- Profile page — 70/15/15, hero strip, performance stats, tier progress, activity timeline
- Settings page — 70/15/15, dual-level nav, notification toggles, danger zone

### Added — Textures (2)
- Dot Grid — 18px pitch, 1.2px radius, Primary T40 at 15% (light) / 12% (dark)
- Diagonal Lines — 12px pitch, 0.8px stroke, 45°, Primary T40 at 15% (light) / 12% (dark)

### Added — Repo Structure
- GitHub-ready scaffold: `tokens/`, `assets/`, `docs/`
- Full documentation suite in `docs/`
- MIT License

### Design Decisions
- **1px strokes** on all form controls — no 2px borders on interactive elements
- **No drop shadows** — tonal elevation only
- **No gradients** — flat surfaces throughout
- **70/15/15 color ratio** — uniform across all 6 page patterns
- **Arvo display rule** — one instance per screen, 24px+ only
- **Dark mode** — every component and page pattern includes complete dark variant
- **Template Machine** — system designed to be re-skinned for new brands

---

## Planned

- [ ] Icon system — angular geometric style, 1.5–2px stroke, no rounded terminals
- [ ] Component code exports (React / HTML / CSS)
- [ ] Figma token sync
- [ ] Additional page patterns as needed
- [ ] Developer handoff documentation
