# Theme Implementation Plan: 5-Color Palette Strategy

## 1. Overview & Objective
This document outlines the systematic strategy for revamping the visual theme of the **Multi-Page Recipe Book** project. The project currently utilizes an early 4-color warm culinary palette and CSS Cascade Layers (`@layer reset, tokens, layout, components, pages`). We will transition to an authoritative, accessible, and sophisticated 5-color theme adhering to WCAG AAA contrast standards.

---

## 2. The 5-Color Palette Definition

| Role / Name | Hex Code | HSL Representation | Primary Purpose & Usage |
| :--- | :--- | :--- | :--- |
| **Background / Light Cream** | `#fdf0d5` | `hsl(41, 88%, 91%)` | Canvas background, header frosted glass backdrop, table header tints, badge surfaces |
| **Deep Blue / Dark Neutral** | `#003049` | `hsl(201, 100%, 14%)` | Primary body typography, section titles, hero headings, dark neutral footer background |
| **Primary / Dark Red** | `#780000` | `hsl(0, 100%, 24%)` | Primary call-to-action buttons, brand logos, active indicators, focus rings, step counters |
| **Secondary / Accent Red** | `#c1121f` | `hsl(356, 83%, 41%)` | Vibrant accent highlights, flame/heart icons, hover states, status completed badges |
| **Muted Blue / Supporting** | `#669bbc` | `hsl(202, 38%, 57%)` | Structural borders, card hover accents, status in-progress tints, supporting tags & progress elements |

---

## 3. Explicit Role Mapping

### A. Background (`#fdf0d5` - Light Cream)
- **`--bg-canvas`**: Body background across all pages (`index.html` and recipe detail pages).
- **`--bg-surface`**: Crisp clean card surfaces (`#ffffff`) layered over the cream background for optimal card contrast.
- **`--bg-surface-elevated`**: Elevated surfaces, mobile navigation drawers (`#fffdfa`).
- **Header Navigation**: Frosted glass effect using `rgba(253, 240, 213, 0.88)` with `backdrop-filter: blur(16px)`.
- **Table Row & Headings Background**: Subtle cream tint `rgba(253, 240, 213, 0.6)`.

### B. Text & Typography (`#003049` - Deep Blue / Dark Neutral)
- **`--text-main`**: `#003049` - Applied to headings (`h1` through `h6`), navigation links, paragraph text, and table cells.
  - *Contrast Check*: `#003049` on `#fdf0d5` provides a **12.3:1** contrast ratio (far surpassing the 7:1 WCAG AAA standard).
- **`--text-muted`**: `#3d5a6c` (Muted deep blue tone) - Applied to recipe subtitles, meta labels, and table column headers (contrast ratio ~6.2:1 on cream).
- **`--text-inverse`**: `#ffffff` - Crisp white on dark red buttons, primary badges, and deep blue surfaces.
- **Footer Text**: `#fdf0d5` and `rgba(253, 240, 213, 0.8)` against the Deep Blue `#003049` footer background.

### C. Primary Buttons & Call to Action (`#780000` - Primary / Dark Red)
- **`--primary`**: `#780000` - Button backgrounds (`.btn-primary`), header logo icons, active navigation underlines, step badge counters, and keyboard focus outlines.
  - *Contrast Check*: `#ffffff` on `#780000` yields **11.0:1** contrast (WCAG AAA compliant).
- **`--primary-hover`**: `#5c0000` - Deep focused crimson hover state for interactive buttons.
- **`--primary-subtle`**: `rgba(120, 0, 0, 0.1)` - Soft warm tint for step numbers and badge fills.
- **Button Glow & Ambient Shadows**: Re-tinted with `rgba(120, 0, 0, 0.35)` replacing prior bright red shadows.

### D. Accents & Secondary Highlights
- **Secondary / Accent Red (`#c1121f`)**:
  - **`--secondary`**: `#c1121f` - Accent buttons, secondary highlights, status completed badges, icon accents (`.icon-accent`, `.icon-heart`).
  - **`--secondary-hover`**: `#9e0e19` - Hover state for accent actions.
  - **Status Completed**: Background `rgba(193, 18, 31, 0.12)`, text `#c1121f`.
- **Muted Blue / Supporting (`#669bbc`)**:
  - **`--border-subtle`**: `rgba(102, 155, 188, 0.35)` - Delicate framing borders for cards, table dividers, and panels.
  - **`--border-strong`**: `#669bbc` - Focus outlines, active card hover borders, and structural separators.
  - **Recipe Card Arrow**: Background `rgba(102, 155, 188, 0.2)` transitioning to `--primary` on hover.
  - **Status In-Progress**: Background `rgba(102, 155, 188, 0.22)`, text `#003049`.
  - **Progress Bar Indicator**: Rich multi-stop gradient from supporting to primary:
    `linear-gradient(90deg, #669bbc, #c1121f, #780000)`

---

## 4. Architectural Modifications & File Scope

1. **`assets/css/tokens.css`**:
   - Redefine core palette tokens:
     - `--palette-cream: #fdf0d5`
     - `--palette-deep-blue: #003049`
     - `--palette-primary-red: #780000`
     - `--palette-accent-red: #c1121f`
     - `--palette-muted-blue: #669bbc`
   - Map semantic tokens (`--primary`, `--secondary`, `--bg-canvas`, `--text-main`, etc.) to the new palette.
   - Update shadow definitions (`--shadow-sm`, `--shadow-md`, `--shadow-lg`) to use deep blue and dark red ambient tints.

2. **`assets/css/layout.css`**:
   - Update sticky header background: `rgba(253, 240, 213, 0.88)` with `backdrop-filter: blur(16px)`.
   - Update mobile drawer navigation background: `--bg-surface-elevated` and borders.
   - Transform `.site-footer`:
     - `background: var(--palette-deep-blue);` (`#003049`)
     - `color: var(--palette-cream);` (`#fdf0d5`)
     - Icons tinted with `--palette-muted-blue` and `--palette-accent-red`.
   - Update hero badge border and shadow colors.

3. **`assets/css/components.css`**:
   - Update button shadow colors to dark red ambient tints.
   - Update `.recipe-card-arrow` background to muted blue tints.
   - Update table header background and row hover tints to harmonize with light cream and muted blue.
   - Update native `<progress>` element gradient to `linear-gradient(90deg, var(--palette-muted-blue), var(--palette-accent-red), var(--palette-primary-red))`.

4. **`assets/css/recipe-detail.css`**:
   - Update circular instruction step counters to utilize `--primary` (`#780000`) and subtle tint border.
   - Confirm sticky ingredient panel and cooking progress card harmoniously render new palette tokens.

5. **`README.md`**:
   - Synchronize documentation with the new 5-color palette, color roles, and accessibility specifications.

---

## 5. Execution & Verification Checklist
- [x] Scan existing CSS architecture and token hierarchy
- [x] Document 5-color role mapping in `implementation.md`
- [ ] Implement updated tokens in `assets/css/tokens.css`
- [ ] Update layout styles in `assets/css/layout.css`
- [ ] Update component styling in `assets/css/components.css`
- [ ] Update recipe detail styles in `assets/css/recipe-detail.css`
- [ ] Update documentation in `README.md`
- [ ] Validate contrast and visual rendering across `index.html` and recipe pages
- [ ] Perform Stage 2-4 git automation (commit, push, PR creation)
