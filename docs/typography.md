# Typography

The AD Design System uses a strict two-font system: Arvo for display moments and Inter for all UI text.

---

## Fonts

### Arvo — Display Only

- **Weight:** 700 exclusively
- **Usage:** Single h1 per screen, 24px minimum, major display context only
- **Source:** `https://unpkg.com/@fontsource/arvo/700.css`

**Ask before using Arvo:** Is this the single most important headline on this screen? Is it 24px or larger? If both answers are yes → Arvo. Otherwise → Inter 500.

**Never use Arvo for:**
- Section subheadings
- Card titles
- Stat or metric labels
- Navigation links
- Any text below 24px
- More than one element per screen

### Inter — All UI Text

- **Weight 500:** Section titles, card headers, metric values, nav links, button labels, chip labels, badge text, table column headers, field labels
- **Weight 400:** Body copy, table data, helper text, captions, descriptions, placeholder text
- **Source:** `https://unpkg.com/@fontsource/inter/400.css` and `500.css`

---

## Type Scale

| Role | Font | Weight | Size | Line Height | Letter Spacing |
|------|------|--------|------|-------------|----------------|
| Display / Hero H1 | Arvo | 700 | 24–28px | 1.15 | 0 |
| Section Title | Inter | 500 | 13–15px | 1.4 | 0 |
| Card Title | Inter | 500 | 12–13px | 1.4 | 0 |
| Metric Value | Inter | 500 | 18–24px | 1.0 | 0 |
| Metric Label | Inter | 500 | 9–10px | 1.3 | 0.06–0.08em |
| Button Label | Inter | 500 | 11–12px | 1.0 | 0 |
| Nav Link | Inter | 500 | 11–12px | 1.0 | 0 |
| Table Header | Inter | 500 | 10–11px | 1.0 | 0.03–0.05em |
| Table Data | Inter | 400 | 11–12px | 1.4 | 0 |
| Body | Inter | 400 | 12–13px | 1.6 | 0 |
| Helper / Caption | Inter | 400 | 9–10px | 1.4 | 0 |
| Badge / Chip | Inter | 500 | 9–10px | 1.0 | 0.02em |
| Eyebrow | Inter | 500 | 9–10px | 1.0 | 0.08–0.10em |

---

## Font Loading

Always load from Fontsource via unpkg. Never use Google Fonts — it is blocked in sandboxed rendering environments and fails silently, causing Arvo to fall back to Georgia.

```html
<!-- Required in every page/component -->
<link href="https://unpkg.com/@fontsource/arvo/700.css" rel="stylesheet">
<link href="https://unpkg.com/@fontsource/inter/400.css" rel="stylesheet">
<link href="https://unpkg.com/@fontsource/inter/500.css" rel="stylesheet">
```

Or via CSS import:

```css
@import url('https://unpkg.com/@fontsource/arvo/700.css');
@import url('https://unpkg.com/@fontsource/inter/400.css');
@import url('https://unpkg.com/@fontsource/inter/500.css');
```

---

## CSS Declarations

```css
/* Display headline */
.display-headline {
  font-family: 'Arvo', Georgia, serif;
  font-weight: 700;
  font-size: 24px;
  line-height: 1.15;
  color: #1f3a1a; /* primary T20 */
}

/* Section title */
.section-title {
  font-family: 'Inter', sans-serif;
  font-weight: 500;
  font-size: 13px;
  line-height: 1.4;
}

/* Body */
.body-text {
  font-family: 'Inter', sans-serif;
  font-weight: 400;
  font-size: 12px;
  line-height: 1.6;
}

/* Eyebrow label */
.eyebrow {
  font-family: 'Inter', sans-serif;
  font-weight: 500;
  font-size: 9px;
  letter-spacing: 0.09em;
  text-transform: uppercase;
  color: #885400; /* tertiary T40 */
}

/* Table column header */
.table-header {
  font-family: 'Inter', sans-serif;
  font-weight: 500;
  font-size: 10px;
  letter-spacing: 0.04em;
}
```

---

## Dark Mode Text Colors

| Role | Light | Dark |
|------|-------|------|
| Primary text | `#1a1c1a` | `#e2e4de` |
| Secondary text | `#44483f` | `#b8bcb2` |
| Muted / helper | `#6b7280` | `#6b7280` |
| Primary headline | `#1f3a1a` | `#b3d0a9` |
| Tertiary accent | `#885400` | `#f2cc88` |
