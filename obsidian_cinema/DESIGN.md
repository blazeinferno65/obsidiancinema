# High-End Editorial Design System: The Cinematic Canvas

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Digital Theater."** 

Unlike standard streaming layouts that feel like rigid grids of data, this system treats the interface as a living, breathing cinematic experience. We move beyond the "template" look by prioritizing high-contrast imagery, intentional asymmetry, and a sense of infinite depth. The user is not just browsing a list; they are standing in a dark gallery where content is the only light source. By utilizing a deep, obsidian-like foundation and vibrant crimson accents, we create a sense of premium urgency and immersive focus.

## 2. Colors
Our palette is designed to disappear, allowing the content (imagery) to provide the primary visual stimulation.

- **Primary & Accents:** The core brand energy comes from `primary_container` (#E50914). This is used sparingly but powerfully for critical calls to action.
- **Surface Hierarchy (The Depth Principle):** We avoid flat design. Instead, we use "Nesting" to define importance:
    - **Base:** `surface` (#131313) for the overall background.
    - **Sectioning:** `surface_container_low` (#1C1B1B) for large content blocks.
    - **Elevated Components:** `surface_container_high` (#2A2A2A) for interactive elements like input fields or focused cards.
- **The "No-Line" Rule:** 1px solid borders are strictly prohibited for defining sections. Boundaries must be achieved through background shifts or typography-led spacing.
- **The "Glass & Gradient" Rule:** Floating UI elements (like the sleek navigation bar) should utilize a `surface_bright` tint with a 20px backdrop-blur and 80% opacity to create a "frosted glass" effect. CTAs should use a subtle linear gradient from `primary_container` to `on_secondary_fixed_variant` to add tactile dimension.

## 3. Typography
Typography is the architectural backbone of the system. We use two distinct weights of the `Be Vietnam Pro` and `Inter` families to create an editorial feel.

- **Display (Be Vietnam Pro):** Used for "The Big Moment." Large-scale, bold headings that command attention. `display-lg` (3.5rem) should be used for hero movie titles to feel like a theatrical poster.
- **Headline (Be Vietnam Pro):** Used for section headings (e.g., "Trending Now"). These should feel authoritative but not overwhelming.
- **Body & Labels (Inter):** The "Workhorse." `body-md` and `body-lg` handle all functional descriptions. We use a high contrast between `on_surface` (white/light grey) and the background to ensure absolute readability in low-light environments.
- **Editorial Intent:** Use `label-sm` in all-caps with generous letter-spacing (0.1em) for metadata like "NEW RELEASE" or "4K ULTRA HD" to evoke high-end magazine styling.

## 4. Elevation & Depth
In a dark-themed cinematic environment, light behaves differently. We use **Tonal Layering** instead of structural lines.

- **The Layering Principle:** Depth is achieved by stacking. A `surface_container_lowest` card sitting on a `surface_container_low` background creates a "inset" look, while a `surface_container_highest` element creates a "lifted" look.
- **Ambient Shadows:** Shadows are never black; they are a tinted version of the `surface_container_lowest`. Use a 40px - 60px blur with only 6% opacity. This creates a soft "glow" of darkness that feels like a natural shadow in a theater.
- **The "Ghost Border" Fallback:** If accessibility requires a border, use `outline_variant` (#5E3F3B) at 15% opacity. It should feel like a suggestion of an edge, not a cage.
- **Glassmorphism:** Navigation bars and "More Info" overlays should always utilize `backdrop-filter: blur(12px)` to allow the vibrant colors of the movie posters behind them to bleed through softly.

## 5. Components

### Navigation Bar
- **Style:** A sleek, floating persistent bar at the top.
- **Tokens:** `surface` with 70% opacity and a `backdrop-filter`. No bottom border; use a subtle `surface_container_high` gradient fade at the bottom edge.

### Buttons
- **Primary (The Red CTA):** `primary_container` (#E50914) background with `on_primary_container` text. Use `md` (0.375rem) roundedness. 
- **Secondary:** `surface_bright` with a "Ghost Border."
- **Interaction:** On hover, the primary button should "glow"—a subtle drop shadow using the `primary` color at 20% opacity.

### Movie Cards
- **Structure:** Forbid divider lines or borders. Cards should be pure imagery.
- **Hover State:** On hover, the card should scale slightly (1.05x) and transition from `surface_container_low` to `surface_container_highest` background if text is present. 
- **Typography:** Titles should be `title-sm`, metadata in `label-sm`.

### Input Fields (e.g., Email Signup)
- **Style:** `surface_container_lowest` background with a `Ghost Border` (10% `outline`). 
- **Focus:** The border transitions to `primary` (#E50914) to signal activity.

### Accordions (FAQs)
- **Style:** Large, horizontal blocks using `surface_container`. 
- **Separation:** No lines. Use 8px of vertical `surface` (background) color between items to create a "slat" look rather than a single divided list.

## 6. Do's and Don'ts

### Do
- **Do** use high-quality, high-contrast photography. The UI is the frame; the imagery is the art.
- **Do** lean into negative space. If a layout feels crowded, increase the spacing between sections to the `xl` scale.
- **Do** use `primary_container` (#E50914) only for high-intent actions. Overuse dilutes the cinematic tension.
- **Do** use Tonal Layering to group related content.

### Don't
- **Don't** use pure `#000000` for backgrounds. Use the specified `surface` (#131313) to allow for subtle shadow depth.
- **Don't** ever use a 1px white or grey border to separate movie cards. Use margin and tonal shifts.
- **Don't** use "drop shadows" that are too dark or sharp. If you can see the edge of the shadow, it’s too heavy.
- **Don't** mix more than two font families. Stick to the specified `Be Vietnam Pro` and `Inter` hierarchy.