# Emerald Impact Design System

### 1. Overview & Creative North Star
**Creative North Star: "The Impact Architect"**
Emerald Impact is a high-end editorial dashboard system designed for clarity, prestige, and actionable data. It rejects the cluttered "box-and-line" aesthetic of traditional SaaS in favor of **Organic Structuralism**. The system uses generous whitespace (spacing: 3) and deep tonal layering to create a sense of breathability and importance. It is characterized by high-contrast typography and a "Bento Box" layout logic that prioritizes information through scale and color saturation rather than rigid borders.

### 2. Colors
The palette is rooted in a deep, authoritative Emerald (`#006857`), complemented by a warm Burnt Orange (`#964900`) for alerts and emphasis.

*   **The "No-Line" Rule:** Visual separation is achieved strictly through shifts in surface containers. Use `surface_container_low` for sidebars and `surface_container_lowest` (pure white) for elevated content cards. 1px solid borders are strictly forbidden for sectioning.
*   **Surface Hierarchy:**
    *   **Level 0 (Background):** `surface` (#f8f9fa)
    *   **Level 1 (Sidebars/Inputs):** `surface_container_low` (#f3f4f5)
    *   **Level 2 (Cards/Containers):** `surface_container_lowest` (#ffffff)
*   **Glass & Gradient:** Floating headers must use `surface/80` with a `backdrop-blur-xl` to maintain a sense of environment. Hero metrics utilize a `bg-gradient-to-br` from `primary` to `primary_container` to draw immediate focus.

### 3. Typography
The system relies on a single, high-performance typeface: **Inter**. The hierarchy is driven by extreme weight variance and tight tracking for large displays.

*   **Display / Hero:** 2.75rem (44px), Bold, -0.02em tracking. Used for page titles and impact headlines.
*   **Metric Titles:** 2.25rem (36px), Bold, Tight tracking.
*   **Section Headers:** 1.125rem (18px) to 1.25rem (20px), Bold.
*   **Body Text:** 0.875rem (14px), Regular/Medium. Used for descriptive text and details.
*   **Labels/Caps:** 10px to 11px, Bold, Uppercase, 0.1em tracking. Used for category headers and timestamps to provide a technical, "data-sheet" feel.

### 4. Elevation & Depth
Depth is created through "Tonal Stacking" rather than heavy drop shadows.

*   **The Layering Principle:** A card (Lowest) sits on a canvas (Surface), creating a natural 3D hierarchy through color value contrast.
*   **Ambient Shadows:** Use extremely diffused shadows for cards: `shadow-[0_8px_24px_rgba(25,28,29,0.04)]`. Avoid high-opacity shadows.
*   **The "Ghost Border" Fallback:** In high-density areas, use `outline_variant` (#bccac4) at 50% opacity only if background contrast is insufficient.
*   **Glassmorphism:** Navigation headers use 80% opacity with a blur to feel "light" while scrolling.

### 5. Components
*   **Buttons:** Primary buttons are pill-shaped (`rounded-full`) with a subtle gradient and a shadow matching the primary color's tone. Secondary buttons use a simple `outline_variant` border.
*   **Navigation Links:** Active states use the full `primary` color with a `rounded-full` shape and a localized shadow. Hover states use a subtle `translate-x-1` transition instead of a color change to maintain elegance.
*   **Bento Cards:** Standardize on `rounded-xl` (1rem) for data containers. Internal padding should be a minimum of `p-6` or `p-8` to maintain the editorial feel.
*   **Progress Bars:** Thin (h-1.5), using `surface_container_highest` for the track and `primary` for the fill, with a subtle glow/shadow on the active indicator.

### 6. Do's and Don'ts
*   **Do:** Use uppercase 10px labels for metadata to create a "curated" look.
*   **Do:** Align elements to a generous 32px (p-8) outer margin.
*   **Don't:** Use standard squares or sharp corners; maintain the `rounded-xl` or `rounded-full` rhythm.
*   **Don't:** Use "pure black" for text. Use `on_surface` (#191c1d) to keep the contrast high but sophisticated.
*   **Do:** Utilize `backdrop-blur` for all sticky elements to maintain context of the underlying data.