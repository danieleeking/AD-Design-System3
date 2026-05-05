# Page Patterns

Six production-ready page patterns for the AD Member Distribution Portal. Every pattern applies the 70/15/15 color ratio and ships with light + dark mode.

---

## Color Ratio System

All 6 pages use a **70 / 15 / 15** color distribution:

| Allocation | Color | Role | Where it appears |
|-----------|-------|------|-----------------|
| 70% | Primary `#4c6842` | Structure | App bar, nav sidebar, hero tints, CTAs, active states, fills |
| 15% | Secondary `#494e52` | Chrome | Labels, helper text, table headers, inactive states, footer bars |
| 15% | Tertiary `#885400` | Accent | Links, badges, SSO button, export button, eyebrows, highlights |

This is a visual weight guideline applied at page composition level, not a pixel measurement.

---

## Page 1 — Login

**Ratio:** 70 / 15 / 15 · **States:** Default · Error · Loading

### Layout
- Top app bar: primary `#4c6842`, logo left, help links right
- Hero strip: primary tint `#cde3c4` (T90), Arvo 700 headline, tertiary eyebrow label, "Premier Member" badge
- Centered form card: 360px max-width, 3px primary top border, 8px border radius
- Full-width footer: secondary `#494e52` with tertiary amber nav links

### Key Color Decisions
| Element | Color | Ratio bucket |
|---------|-------|-------------|
| App bar | `#4c6842` | Primary |
| Hero strip bg | `#cde3c4` | Primary tint |
| Card top border | `#4c6842` | Primary |
| Sign In button | `#4c6842` | Primary |
| SSO button | `#885400` outline | Tertiary |
| Forgot password link | `#885400` | Tertiary |
| Footer background | `#494e52` | Secondary |
| Footer links | `#f2cc88` | Tertiary |

---

## Page 2 — Dashboard

**Ratio:** 70 / 15 / 15

### Layout
- App bar: primary, logo, nav links with tertiary active indicator, avatar
- Left nav sidebar: `#2f5229` (primary T30), 152px, active item with tertiary left-border accent
- Hero strip: deep primary bg, Arvo headline, tertiary member badge
- 4-column metrics grid: primary stat border accent, tertiary trend deltas
- 2-column content: orders table left, rebate + supplier + quick actions right
- Rebate card header: tertiary bg
- Supplier card header: secondary bg

---

## Page 3 — Data Table

**Ratio:** 70 / 15 / 15

### Layout
- App bar + left nav: same as all portal pages
- Page header: Arvo 700 "Orders" title, breadcrumb, "New Order" primary button
- 4 stat cards: primary left-border accent on first card, tertiary trend text
- Toolbar: search bar + filter/status/date dropdowns + columns button + "Export CSV" tertiary amber button
- Data table: secondary slate column headers, primary hover rows, sorted column in tertiary
- Status badges: 5 semantic variants
- Pagination: primary-filled active page button

### Status Badge Reference
| Status | Background | Text |
|--------|-----------|------|
| Delivered | `#cde3c4` | `#1f3a1a` |
| Shipped | `#d1dadd` | `#373f43` |
| Pending | `#fae3bc` | `#6d4400` |
| Processing | `#e8f4e3` | `#2f5229` |
| Cancelled | `#fde8e8` | `#7a1c1c` |

---

## Page 4 — Form

**Ratio:** 70 / 15 / 15

### Layout
- App bar + left nav: standard portal nav
- Page header: Arvo 700 "New Order Request" title
- 4-step horizontal stepper: completed (primary filled ✓), active (primary + ring glow), upcoming (slate border)
- 3 numbered form sections: primary circle numbers, section titles Inter 500
- Form action bar: "Submit Order" (primary filled) + "Save as Draft" (tertiary amber outline) + Cancel

### Form Controls
- Text fields: 1px border, primary focus ring + glow
- Selects: 1px border, primary focus, chevron indicator
- Radio buttons: 1px SVG stroke, primary dot fill on selection
- Checkboxes: 1px SVG stroke, primary fill on check
- Textarea: 1px border, 60px height, resize: none

### Stepper Color
| Step state | Style |
|-----------|-------|
| Completed | Primary `#4c6842` filled circle with white checkmark |
| Active | Primary filled + `box-shadow: 0 0 0 3px #cde3c4` ring |
| Upcoming | White circle + `1px rgba(0,0,0,0.20)` border + slate number |

---

## Page 5 — Profile

**Ratio:** 70 / 15 / 15

### Layout
- App bar + left nav: "My Profile" active
- Profile hero strip: deep primary `#2f5229`, large avatar circle (tertiary amber bg), Arvo 700 name, role text, meta row, "Premier Member" + "Active" badges
- "Edit Profile" button: tertiary amber outline on dark bg
- 2-column content grid:
  - Left: Contact Information card (read-only field display)
  - Right: Account Performance card (4 mini-stats + tier progress bar)
- Full-width: Recent Activity timeline (5 items, color-coded dots)
- Footer: Save Changes (primary) + Change Password + Sign Out

### Activity Timeline Dots
| Type | Dot color |
|------|----------|
| Order events | Primary `#4c6842` |
| Finance / Reports | Tertiary `#885400` |
| Account changes | Secondary slate |

---

## Page 6 — Settings

**Ratio:** 70 / 15 / 15

### Layout
- App bar + left nav: "Settings" active
- Page header: Arvo 700 "Settings"
- Dual-level navigation: portal nav (primary) + settings category nav (white, 148px, primary left-border on active)
- Settings content panel: 3 sections
  1. Notification Preferences (5 toggle rows with channel pills)
  2. Delivery & Regional Settings (3 select rows)
  3. Danger Zone (red-bordered, Export + Deactivate)

### Toggle Switch States
- **ON:** `#4c6842` (primary) background, white knob
- **OFF:** `#d1d5db` background, white knob
- **Transition:** 150ms standard easing

### Channel Pills
| State | Background | Text |
|-------|-----------|------|
| Active (Email/SMS/Push) | `#cde3c4` | `#1f3a1a` |
| Inactive | `#f4f4f5` | `#9ca3af` |
| Amber (rebate-specific) | `#fae3bc` | `#6d4400` |

### Danger Zone
- Border: `1px solid rgba(220,38,38,0.25)`
- Header background: `#fef9f9` (light mode) / `#2d1010` (dark mode)
- Button style: red outline, `color: #dc2626`, `border: 1px solid rgba(220,38,38,0.40)`
- Uses independent semantic red — not governed by the 70/15/15 ratio
