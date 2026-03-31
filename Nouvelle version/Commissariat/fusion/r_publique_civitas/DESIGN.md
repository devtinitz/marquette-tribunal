# Design System Document: Tribunal de Yopougon

## 1. Overview & Creative North Star
**Creative North Star: "The Sovereign Ledger"**
This design system moves away from the sterile, "bootstrap" look of typical government portals. Instead, it adopts a high-end editorial aesthetic that communicates authority, transparency, and modern efficiency. We treat the interface not as a software tool, but as a digital manifestation of the Ivorian judicial spirit.

The design breaks the traditional grid through **Intentional Asymmetry**. By using a wide sidebar juxtaposed with a spacious, airy content area, we create a layout that feels bespoke. We utilize high-contrast typography scales and overlapping "layered" surfaces to move beyond flat, 2D web patterns. Every interaction should feel deliberate, weighty, and professional.

---

## 2. Colors & Surface Philosophy
The palette honors the Ivorian flag while introducing deep, judicial tones to provide administrative gravitas.

### The Palette
- **Primary (Ivorian Green):** `#006400` – Used for primary actions and brand presence.
- **Secondary (Ivorian Orange):** `#8a5100` (Core) / `#fe9800` (Container) – Reserved for high-priority transmissions and status changes.
- **Tertiary (Justice Blue):** `#3a5296` – Used for informational accents and secondary navigation elements.
- **Neutral Surface Hierarchy:** 
    - `surface-container-lowest`: `#ffffff` (Main content cards)
    - `surface`: `#f9f9f9` (Main page background)
    - `surface-container-high`: `#e8e8e8` (Sidebar or nested utility panels)

### The "No-Line" Rule
Traditional 1px solid borders are strictly prohibited for sectioning content. Boundaries must be defined solely through background color shifts. To separate a table from the page, place a `surface-container-lowest` card upon a `surface` background. The transition of color is the border.

### The "Glass & Gradient" Rule
To add "soul" to the administrative interface:
- **Floating Elements:** Modals and dropdowns should use a backdrop-blur (12px–20px) with a semi-transparent `surface` color (85% opacity).
- **Signature Textures:** For the "Transmit" action button, use a subtle linear gradient from `secondary` to `secondary_container` (Top to Bottom). This adds a tactile, premium feel that flat colors lack.

---

## 3. Typography
We use **Inter** as a singular, powerful typeface. Its neutral yet modern geometry provides the high legibility required for legal documentation.

- **Display (The Sovereign Header):** `display-md` (2.75rem / 44px). Bold. Used for main dashboard titles to establish immediate authority.
- **Headline (Sectioning):** `headline-sm` (1.5rem / 24px). Semi-bold. Used for major card titles (e.g., "Recent Plaints").
- **Title (Actionable):** `title-md` (1.125rem / 18px). Medium. Used for table headers and button labels.
- **Body (The Record):** `body-lg` (1rem / 16px). Regular. Optimized for long-form case descriptions with a line-height of 1.6 to ensure readability.
- **Label (Metadata):** `label-md` (0.75rem / 12px). All-caps with 0.05em tracking. Used for status badges and timestamps.

---

## 4. Elevation & Depth
In this system, hierarchy is achieved through **Tonal Layering** rather than structural lines.

- **The Layering Principle:** Treat the UI as stacked sheets of fine paper. The `surface-container-low` serves as the desk, and `surface-container-lowest` serves as the active document. 
- **Ambient Shadows:** Shadows should be almost invisible. Use a 24px blur with 4% opacity, tinted with the `on-surface` color. This mimics natural light in a professional office.
- **The "Ghost Border" Fallback:** If a separation is required for accessibility (e.g., input fields), use the `outline_variant` at **15% opacity**. Never use a 100% opaque border.
- **Glassmorphism:** Use semi-transparent layers for the Sidebar Navigation to allow a hint of the background color to bleed through, softening the interface and making it feel integrated.

---

## 5. Components

### Buttons
- **Primary (Submission):** `primary` fill, `on-primary` text. Use `lg` (0.5rem) roundedness.
- **Transmission (Secondary):** `secondary` fill with the signature gradient. This is the most prominent button in the Commissariat flow.
- **Tertiary (Ghost):** No fill, `tertiary` text. Use for "Cancel" or "Go Back" actions.

### Tables (The Ledger)
- **Rule:** Forbid divider lines. Use `surface-container-low` on every second row for zebra-striping, or simply use ample vertical white space (`spacing-4`) to define rows.
- **Header:** Use `surface-dim` background with `label-md` bold text.

### Status Badges (Chips)
- **Design:** Use the `full` roundedness scale. 
- **Colors:** Use `tertiary_container` for "In Progress," `on-primary_container` for "Resolved," and `error_container` for "Urgent."

### Input Fields
- **Style:** No bottom line. Use a `surface-container-highest` background with `md` roundedness. On focus, transition the background to `surface-container-lowest` and apply a 2px "Ghost Border" in `primary`.

### Sidebar Navigation
- **Architecture:** Occupies a fixed width. Use `surface-container-high` to distinguish it from the workspace. Active states are indicated by a `primary` vertical "light-bar" (4px width) on the left edge, rather than an icon color change alone.

---

## 6. Do's and Don'ts

### Do
- **Do** use `spacing-8` (2rem) between major content cards to allow the layout to "breathe."
- **Do** use the discrete Ivory Coast flag as a subtle accent in the logo area—treat it as a mark of quality and national pride.
- **Do** prioritize the Orange Transmission button in the user's visual path; it is the "Closing" action of the workflow.

### Don't
- **Don't** use pure black (`#000000`) for text. Use `on_surface` (`#1a1c1c`) to maintain a premium, editorial feel.
- **Don't** use shadows on buttons. Let the color and gradient define the clickability.
- **Don't** use standard "Success" green for status badges if it conflicts with the Ivorian Green brand color. Use the specified `tertiary` or `secondary` tokens instead.