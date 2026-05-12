# Design System: 元利四季莊園 (Season Village)

## 1. Visual Theme & Atmosphere
A restrained, "forest-in-the-city" architectural aesthetic. The atmosphere is serene, high-end, and grounded in nature — evoking the feeling of a well-lit art gallery or a luxury mountain retreat. It avoids "AI slop" by using earthy, calibrated tones and clean spatial separation.

- **Density:** Art Gallery Airy (3/10)
- **Variance:** Offset Asymmetric (6/10)
- **Motion:** Fluid CSS with Spring Physics (6/10)

## 2. Color Palette & Roles
- **Canvas Cream** (#F7F5F0) — Primary background surface. Warm, non-clinical neutral.
- **Forest Charcoal** (#2C3E2D) — Primary ink, branding, and deep structural elements.
- **Earth Gold** (#8B7355) — Accent color for labels, icons, and call-to-action highlights.
- **Shadow Ink** (rgba(0, 0, 0, 0.45)) — Contrast overlay for hero sections and image text readability.

## 3. Typography Rules
- **Display/Headlines:** `Noto Serif TC` — High-contrast Traditional Chinese serif. Track-tight, weight-driven hierarchy.
- **Body:** `Noto Sans TC` — Clean, legible Traditional Chinese sans-serif. Relaxed leading (1.8 - 1.9).
- **Accent/Numbers:** `Cormorant Garamond` — Elegant, italicized serif for numbers and luxury labels.
- **Constraint:** `font-variant-numeric: tabular-nums` is enforced for all animated counters to maintain layout stability.

## 4. Component Stylings
* **Buttons:** Flat, border-based for ghost CTAs. Earth Gold fill for primary actions. No outer glows.
* **Cards:** Minimalist. No heavy shadows; elevation is communicated through color blocks and whitespace.
* **Reveal Animations:** Staggered cascade reveals using `cubic-bezier(0.2, 0.8, 0.2, 1)`. Hardware-accelerated via `will-change`.

## 5. Layout Principles
- **Grid Architecture:** 2-column asymmetric splits for feature sections.
- **Spatial Zone:** No overlapping elements. Every text block and image occupies its own clean zone.
- **Responsiveness:** Single-column collapse below 768px. Headlines use `clamp()` for fluid scaling.

## 6. Motion & Interaction
- **Hardware Acceleration:** All transforms and opacity changes must use `will-change` and `backface-visibility: hidden`.
- **Spring Physics:** 1.2s duration with custom cubic-bezier for a weighty, premium feel.
- **Perpetual Micro-Interactions:** Navigation transitions on scroll (padding/background shift).

## 7. Anti-Patterns (Banned)
- No emojis.
- No `Inter` font.
- No pure black (#000000).
- No neon/outer glow shadows.
- No "AI Copywriting" clichés (Elevate, Seamless, Unleash).
- No 3-column equal cards (Use asymmetric grids or staggered layouts).
- No fabricated statistics (Real estate data only).
