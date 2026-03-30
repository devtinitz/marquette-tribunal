# Design System Document: Judicial Transparency & Flow

## 1. Overview & Creative North Star: "The Digital Magistrate"
This design system moves away from the cluttered, bureaucratic aesthetic typical of legal institutions. Our Creative North Star is **"The Digital Magistrate"**—an interface that commands authority through intentional silence, expansive white space, and editorial-grade typography. 

Instead of rigid tables and heavy borders, we utilize **Tonal Layering** and **Asymmetric Balance**. The layout should feel like a high-end legal brief: structured, prestigious, and crystalline. We break the "template" look by overlapping floating action panels over soft-tinted backgrounds, ensuring the user feels a sense of calm and "judicial order" while managing complex complaint data.

---

## 2. Color Strategy & The "No-Line" Philosophy
The color palette is rooted in the Ivorian heritage but elevated through Material Design 3 tonal logic.

### The "No-Line" Rule
**Borders are prohibited for sectioning.** To define a sidebar, a header, or a content card, you must use background color shifts. 
- *Example:* A `surface-container-low` main content area sitting on a `surface` background.
- This creates a modern, high-end feel where depth is felt, not seen through harsh strokes.

### Surface Hierarchy & Nesting
Treat the UI as a series of stacked sheets of fine Ivorian vellum.
- **Level 0 (Base):** `surface` (#f8f9ff)
- **Level 1 (Main Content Area):** `surface-container-low` (#f0f4fd)
- **Level 2 (Active Cards/Modals):** `surface-container-lowest` (#ffffff)
- **Level 3 (Interactive Overlays):** `surface-container-high` (#e4e8f1)

### Glass & Gradient Rule
For high-priority dashboards, use **Glassmorphism**. Floating navigation or "Quick Action" bars should use `surface-variant` at 70% opacity with a `20px` backdrop-blur. 
- **Signature Gradient:** For primary CTAs (e.g., "New Complaint"), use a subtle linear gradient from `primary` (#006400) to `primary-container` (#008000) at 135 degrees. This adds "soul" and prevents the green from looking like a flat utility color.

---

## 3. Typography: Editorial Authority
We use **Inter** not as a system font, but as a brand asset.

*   **Display (The Statement):** `display-md` (2.75rem) for main dashboard greetings. Use `-0.02em` letter-spacing to give it a premium, "compressed" editorial feel.
*   **Headlines (The Anchor):** `headline-sm` (1.5rem) for section titles. Always pair with `on-surface-variant` to reduce visual vibration.
*   **Titles (The Action):** `title-md` (1.125rem) with `medium` weight (500) for card titles and navigation links.
*   **Body (The Record):** `body-md` (0.875rem) for all legal text and complaint descriptions. Use a generous `1.6` line-height for readability.
*   **Labels (The Metadata):** `label-md` (0.75rem) in `all-caps` with `+0.05em` tracking for status tags (e.g., "EN ATTENTE").

---

## 4. Elevation & Depth: Tonal Layering
Traditional shadows are too "web 2.0." This system uses ambient light.

*   **The Layering Principle:** Depth is achieved by "stacking." A `surface-container-lowest` card placed on a `surface-container-low` background creates a natural lift.
*   **Ambient Shadows:** For floating modals, use a custom shadow: `0px 24px 48px -12px rgba(0, 35, 102, 0.08)`. Note the use of **Justice Blue** in the shadow color to tie the elevation back to the brand identity.
*   **The "Ghost Border" Fallback:** If a border is required for accessibility, use `outline-variant` at **15% opacity**. Never use a 100% opaque border.

---

## 5. Components: The Building Blocks

### Buttons (State-Driven)
*   **Primary:** Gradient from `primary` to `primary-container`. Corner radius: `md` (0.375rem).
*   **Secondary:** Ghost style. Transparent background with a `Ghost Border` and `tertiary` (#3a5296) text.
*   **Tertiary:** `surface-container-highest` background with `on-surface` text.

### Cards & Lists (The "Anti-Grid")
*   **No Dividers:** Forbid the use of line dividers between list items. Use a `1.5` (0.375rem) vertical spacing gap or a subtle toggle of background colors (Zebra striping using `surface` and `surface-container-low`).
*   **Complaint Cards:** Use a `surface-container-lowest` base with a 4px left-accent strip of `secondary` (#8a5100) to denote "Urgent" status.

### Status Chips
*   **Pending:** `secondary-container` background with `on-secondary-container` text.
*   **Resolved:** `primary-container` background with `on-primary-container` text.
*   **Legal Review:** `tertiary-container` background with `on-tertiary-container` text.

### Input Fields
*   **Style:** Filled style (not outlined). Use `surface-container-highest` with a 2px bottom-indicator that animates from the center on focus using `primary`.

### Administrative Specialized Components
*   **The "Case Timeline":** A vertical progression component using `tertiary` dots. Avoid lines; use the proximity of text and subtle background blocks to imply the "path of justice."
*   **The "Seal of Authenticity":** A discreet, low-opacity watermark of the logo integrated into the background of printable document previews.

---

## 6. Do's and Don'ts

### Do:
*   **Use Asymmetry:** Place the main "Search" bar off-center to the left to create a dynamic, modern entry point.
*   **Embrace Breathing Room:** Use the `16` (4rem) spacing token between major dashboard sections.
*   **Respect the Flag:** The Ivorian flag in the logo must be "discreet"—use desaturated tones if necessary to ensure it doesn't clash with the vibrant UI greens.

### Don't:
*   **Don't use pure black:** Use `on-surface` (#171c22) for text. Pure black (#000) kills the sophisticated tonal depth of the system.
*   **Don't use sharp corners:** This is an administrative tool for citizens; use the `md` (0.375rem) scale to ensure the interface feels approachable and modern, not "stiff."
*   **Don't hide the Justice Blue:** Use `tertiary` (#3a5296) for all "Actionable Metadata"—links, icons, and filter toggles—to signify authoritative interaction.

---

## 7. Responsive Desktop (1920x1080)
The dashboard is optimized for large displays. 
*   **The 3-Column Split:** 
    *   Column 1 (280px): Persistent Sidebar (Glassmorphism).
    *   Column 2 (Flexible): Main Data Stream/Complaint List.
    *   Column 3 (420px): Contextual Detail Panel (Surface-container-high). This panel should "slide in" rather than pop, maintaining the "Flow" of the judicial process.

---
*Note: This design system is built to evolve. When in doubt, prioritize legibility and the "No-Line" rule to maintain a premium, custom-coded aesthetic.*