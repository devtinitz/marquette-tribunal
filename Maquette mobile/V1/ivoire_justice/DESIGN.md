# Design System Document: Judicial Excellence

This design system serves as the foundational visual and interactive framework for the "Tribunal de Yopougon" mobile experience. It is designed to bridge the gap between rigorous legal authority and modern digital accessibility, ensuring that every citizen interaction feels secure, transparent, and dignified.

---

### 1. Creative North Star: "The Digital Magistrate"
The "Digital Magistrate" concept moves away from the cold, bureaucratic aesthetic of traditional government apps. Instead, it adopts an **Editorial Authority**—using expansive white space, sophisticated tonal layering, and high-contrast typography to guide the user.

*   **Intentional Asymmetry:** Avoid perfectly centered, "templated" layouts. Use heavy left-aligned headlines and offset floating action buttons to create a sense of dynamic movement and modernism.
*   **Atmospheric Depth:** The UI should feel like a series of high-quality vellum sheets stacked atop one another, using light and transparency to signify hierarchy rather than harsh lines.

---

### 2. Color Strategy & The "No-Line" Rule
The palette is rooted in the national identity of Côte d'Ivoire, elevated through Material Design 3 logic to ensure functional depth.

#### Core Tones
*   **Primary (`#006400`):** The "Deep Ivorian Green." Used for core actions to represent growth and stability.
*   **Secondary (`#8a5100`):** "Burnished Orange." Used for secondary highlights and callouts, providing warmth without sacrificing professionalism.
*   **Tertiary (`#3a5296`):** "Justice Blue." The accent color for informational states and legal status indicators.

#### The "No-Line" Rule
To achieve a premium feel, **1px solid borders are strictly prohibited for sectioning.** 
*   **Boundary Definition:** Separate sections using background shifts. Place a `surface_container_low` element on a `surface` background.
*   **Surface Nesting:** Create depth by nesting. An inner card should use `surface_container_lowest` (white/near-white) when placed on a `surface_container` background.

#### Glass & Gradient
*   **Signature CTA:** Use a subtle linear gradient for primary buttons: `primary` to `primary_container`.
*   **Glassmorphism:** Navigation bars and floating headers must use `surface` at 80% opacity with a `backdrop-blur` of 12px.

---

### 3. Typography: Editorial Authority
We use **Inter** exclusively. Its neutral, geometric construction provides the clarity required for complex legal texts.

*   **Display & Headline (The Lead):** Use `display-md` or `headline-lg` for screen titles. These should be "Heavy" or "Bold" weight to anchor the page.
*   **Body (The Testimony):** `body-lg` is the workhorse. Ensure a line-height of 1.5x for legal readability.
*   **Labels (The Footnote):** Use `label-md` for metadata. These should use `on_surface_variant` to recede visually, allowing the primary content to breathe.

---

### 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are too "web 2.0." We use **Ambient Depth**.

*   **The Layering Principle:** 
    *   Level 0 (Base): `surface`
    *   Level 1 (Section): `surface_container_low`
    *   Level 2 (Interactive Card): `surface_container_lowest`
*   **The Ghost Border:** If a container requires further definition (especially in Dark Mode), use `outline_variant` at **15% opacity**. Never use a 100% opaque border.
*   **Ambient Shadows:** For high-priority floating elements, use a shadow with a 24px blur, 0px offset, and 6% opacity of the `on_surface` color.

---

### 5. Components & Interaction

#### Buttons (Les Actions)
*   **Primary:** Large (`spacing-12` height), rounded to `lg` (`0.5rem`). Uses the Green gradient.
*   **Secondary:** Ghost-style. No background. `primary` text color with a `surface_variant` hover/press state.
*   **Large Intuitive Buttons:** For main dashboard actions (e.g., "Suivre mon dossier"), use full-width cards with `surface_container_highest` and a `secondary` (Orange) icon.

#### Cards & Lists (Les Dossiers)
*   **Rule:** Forbid divider lines. 
*   **Structure:** Use `spacing-4` vertical gaps between list items. Each item sits on its own subtle `surface_container_low` plinth.

#### Status Indicators (Indicateurs d'État)
*   **Success (Terminé):** `primary` text on `on_primary_container` background.
*   **Warning (En Attente):** `secondary` text on `secondary_container` background.
*   **Error (Rejeté):** `error` text on `error_container`.
*   **Info (Instruction):** `tertiary` text on `tertiary_container`.

#### Progress Bars (Suivi de Procédure)
*   Track: `surface_container_highest`.
*   Indicator: `primary` to `primary_fixed` gradient.
*   Height: `spacing-2` (8px) with `full` rounding.

---

### 6. Do's and Don'ts

| **Do** | **Don't** |
| :--- | :--- |
| **Do** use `spacing-8` or `spacing-10` for generous padding between legal sections. | **Don't** use 1px dividers to separate content; use white space. |
| **Do** use "Surface Tints" to make Dark Mode feel deep and premium. | **Don't** use pure #000000 for Dark Mode backgrounds. |
| **Do** use `title-lg` for case numbers to give them importance. | **Don't** use high-contrast borders that "trap" the content. |
| **Do** leverage Glassmorphism for the "Tribunal de Yopougon" top branding bar. | **Don't** use more than two font weights on a single screen. |

---

### 7. Accessibility (Accessibilité)
*   **Contrast:** All text-on-background combinations must meet WCAG AA standards (4.5:1).
*   **Touch Targets:** Every interactive element must have a minimum hit area of `spacing-12` (48px).
*   **Language:** Use clear, non-legalistic French where possible, reserving technical terms for official document previews.