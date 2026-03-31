# Design System Strategy: The Judicial Monolith

## 1. Overview & Creative North Star
The Public Prosecutor’s Office of the Tribunal of Yopougon requires a digital presence that commands the same authority as a physical courtroom. This design system departs from generic "government portal" templates to embrace a **Creative North Star: The Sovereign Editorial.**

We treat the UI as a series of high-end judicial documents. We reject the "boxed-in" web look in favor of expansive white space, intentional asymmetry, and a sophisticated layering of Ivorian national colors. The aesthetic is "Sovereign"—meaning it feels permanent, heavy with responsibility, yet technologically advanced. We achieve this through "The Monolithic Grid": where content isn't trapped in boxes, but anchored by strong typographic alignments and shifts in tonal depth.

---

## 2. Colors & Surface Philosophy
The palette is a tribute to the Ivorian flag, elevated for a judicial context. We utilize a refined Material Design spectrum to ensure high contrast and accessibility.

### The "No-Line" Rule
To achieve a premium, modern feel, **1px solid borders are strictly prohibited for sectioning.** Boundaries must be defined through:
1.  **Background Color Shifts:** Use `surface-container-low` (#f3f3f3) sections sitting on a `surface` (#f9f9f9) background.
2.  **Tonal Transitions:** Defining the sidebar by shifting from `surface` to `surface-container-highest` (#e2e2e2) rather than using a divider line.

### Surface Hierarchy & Nesting
Treat the interface as a stack of physical judicial files.
*   **Base:** `surface` (#f9f9f9) for the primary application canvas.
*   **Structural Nesting:** Place `surface-container-lowest` (#ffffff) cards on top of `surface-container-low` (#f3f3f3) zones. This "white-on-grey" layering creates a crisp, professional depth that feels cleaner than shadows.
*   **The Glass Rule:** For floating navigation or modal headers, use `surface-variant` with an 80% opacity and a `backdrop-filter: blur(12px)`. This keeps the "Ivorian Green" and "Orange" accents visible as the user scrolls, maintaining brand presence without visual clutter.

### Signature Textures
Main CTAs and Hero sections should utilize a **Subtle Judicial Gradient**: A linear transition from `primary` (#006400) to `primary-container` (#008000) at a 135-degree angle. This adds "soul" and prevents the interface from looking like a flat, low-cost template.

---

## 3. Typography: The Editorial Voice
We use **Inter** as a tool of precision. The hierarchy is designed to make dense legal data feel readable and authoritative.

*   **Display (Editorial Hero):** `display-md` (2.75rem / 44px). Bold. Used for high-level landing titles like "Le Parquet de Yopougon."
*   **Headline (Judicial Action):** `headline-md` (1.75rem / 28px). Bold. Used for major section headers (e.g., "Dossiers En Cours").
*   **Title (Data Label):** `title-md` (1.125rem / 18px). Medium/Bold. Used for card titles and table headers.
*   **Body (The Evidence):** `body-lg` (1rem / 16px). Regular. Used for case descriptions and official correspondence. Use a line height of 1.6 for maximum legibility.
*   **Label (Metadata):** `label-md` (0.75rem / 12px). All-caps with 5% letter spacing. Used for status badges and timestamps.

---

## 4. Elevation & Depth
In this system, "Elevation" is a psychological tool. High elevation equals high priority.

*   **Tonal Layering Principle:** Avoid shadows for static elements. Use `surface-container` tiers to create hierarchy.
*   **Ambient Shadows:** For active judicial actions (modals, dropdowns), use an **Ambient Light Shadow**: `0px 12px 32px rgba(0, 35, 102, 0.06)`. Note the tint: we use a hint of `tertiary` (Deep Blue) in the shadow to make it feel integrated with the judicial theme.
*   **The Ghost Border Fallback:** If accessibility requires a container boundary, use `outline-variant` (#becab6) at **15% opacity**. It should be felt, not seen.

---

## 5. Components & Signature Patterns

### Official Judicial Buttons
*   **Primary (Action):** `primary` (#006400) background, `on-primary` (#ffffff) text. Use `rounded-md` (0.375rem). No shadow; use a subtle internal glow for depth.
*   **Secondary (Information):** `tertiary` (#3a5296) Deep Blue. Used for "View Record" or "Research."
*   **Judicial Accent:** `secondary` (#8a5100) Ivorian Orange. Reserved strictly for "Urgent" or "High Priority" actions.

### Data Tables & Dossier Lists
*   **Forbid Divider Lines:** Use `1.5` (0.375rem) vertical spacing and alternating `surface-container-low` row backgrounds for high-density data.
*   **The "Case Status" Badge:** 
    *   *En cours:* `primary-container` background with `on-primary-fixed-variant` text.
    *   *En attente:* `secondary-container` background with `on-secondary-container` text.
    *   *Clôturé:* `tertiary-container` background with `on-tertiary-fixed-variant` text.

### Sidebar Navigation
*   Use `surface-container-highest` (#e2e2e2) to create a monolithic vertical pillar on the left.
*   The Logo ('TRIBUNAL DE YOPOUGON') must be anchored at the top with a `16` (4rem) padding, using `headline-sm` typography.

### Official Forms
*   **Input Fields:** `surface-container-lowest` (#ffffff) with a `px` (1px) `outline-variant` that only becomes `primary` (#006400) on focus.
*   **Labeling:** Labels should be `label-md` and positioned 8px above the input, never inside as placeholder text.

---

## 6. Do's and Don'ts

### Do
*   **DO** use whitespace as a separator. If in doubt, increase the spacing from `8` to `12`.
*   **DO** align text-heavy legal content to a strict left-margin to create a "Vertical Axis of Trust."
*   **DO** use the Ivorian Orange (`secondary`) sparingly—it is a "Warning/Alert" color, not a decorative one.

### Don't
*   **DON'T** use 100% black text. Always use `on-surface` (#1a1c1c) to maintain a premium, editorial feel.
*   **DON'T** use rounded corners larger than `lg` (0.5rem). The judicial system is "sharp" and "rectilinear"; excessive roundness (pills/circles) feels too casual.
*   **DON'T** use standard "Grey" shadows. Always tint shadows with the `on-surface` or `tertiary` tokens.