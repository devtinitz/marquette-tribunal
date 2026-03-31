# Design System Document: Judicial Excellence & Ivorian Heritage

## 1. Overview & Creative North Star: "The Modern Magistrate"
The design system for the Tribunal de Yopougon transcends the utility of a standard government app to become a "Digital Sanctuary of Justice." Our Creative North Star is **The Modern Magistrate**: an experience that feels authoritative yet accessible, rigid in its integrity but fluid in its navigation.

To break the "template" look common in judicial software, we employ **Intentional Asymmetry** and **Editorial Breathing Room**. We move away from cluttered grids toward a layout that feels like a premium law journal. By utilizing high-contrast typography scales and overlapping surface elements, we create a sense of depth and "Ivorian Flair" without resorting to literal flag motifs. The national identity is baked into the very DNA of the color transitions and the warmth of the interface.

---

## 2. Colors & Tonal Depth
We utilize the Ivory Coast’s tricolor palette not as flat fills, but as sophisticated tonal layers. 

### The Palette (Material Convention)
*   **Primary (`#006400`):** The deep "Forest of Law." Used for core actions and authoritative states.
*   **Secondary (`#8a5100`):** The "Earthen Orange." Used for attention-seeking elements and progress tracking.
*   **Tertiary (`#3a5296`):** The "Justice Blue." Provides a calm, institutional anchor for navigation.

### The "No-Line" Rule
**Explicit Instruction:** Designers are prohibited from using 1px solid borders to section content. Boundaries must be defined solely through background color shifts. 
*   *Example:* A `surface-container-low` section sitting on a `surface` background provides all the separation needed. Lines create visual noise; tonal shifts create elegance.

### The "Glass & Gradient" Rule
To escape the "default" mobile feel, floating elements (like bottom navigation bars or quick-action FABs) must use **Glassmorphism**. 
*   **Spec:** Apply `surface` color at 70% opacity with a `16px` backdrop-blur. 
*   **Signature Textures:** Use subtle linear gradients for Hero headers, transitioning from `primary` to `primary-container`. This adds a "soul" to the UI that flat colors lack.

---

## 3. Typography: The Editorial Voice
We use **Inter** not as a system font, but as a high-end editorial tool. By exaggerating the scale between `display` and `body` text, we create a clear hierarchy that guides a stressed user through legal complexities.

*   **Display (Large: 3.5rem / Medium: 2.75rem):** Reserved for "Status at a Glance" or welcoming the user. Should be tracked slightly tighter (-0.02em) to feel authoritative.
*   **Headline (Small: 1.5rem):** Used for case titles. This is the "Anchor" of the page.
*   **Title (Medium: 1.125rem):** Semi-bold weight. Used for field headers and section titles.
*   **Body (Large: 1rem):** Standardized for legal descriptions. Line height must be generous (1.6) to ensure accessibility for all citizens.
*   **Label (Medium: 0.75rem):** All-caps with increased letter spacing (+0.05em) when used for metadata like "DATE FILED" or "CASE ID."

---

## 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are banned in favor of **Tonal Layering**. We treat the UI as a series of physical layers—stacked sheets of fine Ivorian paper.

*   **The Layering Principle:** 
    *   **Base:** `surface`
    *   **Sections:** `surface-container-low`
    *   **Primary Cards:** `surface-container-lowest` (This creates a "lifted" effect through brightness rather than shadow).
*   **Ambient Shadows:** If a floating element (like a modal) requires a shadow, use a "Justice Blue" tint: `rgba(0, 35, 102, 0.06)` with a 32px blur and 12px Y-offset.
*   **The Ghost Border:** For high-stakes inputs where accessibility is a concern, use the `outline-variant` token at **15% opacity**. It should be felt, not seen.

---

## 5. Components: Precision & Accessibility

### Buttons
*   **Primary:** High-gloss gradient from `primary` to `primary-container`. `xl` (1.5rem) rounded corners. Large 56px touch target.
*   **Secondary:** Ghost-style. No fill, `tertiary` text. Used for "Cancel" or "Back" actions.

### Cards & Lists (The Modern Docket)
*   **Rule:** Forbid the use of divider lines. 
*   **Implementation:** Separate list items using the `3` (1rem) spacing scale. Each list item should be its own `surface-container` shape with `md` (0.75rem) rounded corners. This creates a "chunky," accessible feel that is easier to tap than a thin list item.

### Input Fields
*   **Style:** Filled containers (`surface-container-high`) rather than outlined boxes.
*   **Focus State:** A 2px signature glow of `secondary_container` (Ivorian Orange) to signify active engagement.

### Specialized Component: The "Progress Totem"
A custom vertical stepper for tracking complaints. Instead of generic dots, use the `tertiary_fixed` (Justice Blue) for completed steps and a pulsing `secondary` (Orange) for the current status, mimicking the rhythm of the Ivorian flag.

---

## 6. Do’s and Don’ts

### Do:
*   **Do** use asymmetrical white space. Allow a case number to sit higher than its label to create an editorial look.
*   **Do** use `xl` (1.5rem) corner radii for main containers to convey friendliness and approachability.
*   **Do** use large, clear icons from a rounded set (e.g., Lucide or Material Symbols Rounded) to ensure the judicial process feels modern.

### Don’t:
*   **Don’t** use pure black (`#000000`) for text. Use `on-surface` (`#181d15`) to keep the "Forest Green" undertone throughout.
*   **Don’t** use harsh 90-degree corners. The law is firm, but the interface for the citizen should be soft and supportive.
*   **Don’t** use standard "Error Red" alone. Soften error states with `error_container` backgrounds to keep the user from feeling "judged" by the app.

---
**Director's Note:** This system is not just a tool; it is an extension of the state's commitment to its people. Every pixel must feel intentional, every transition smooth, and every color choice a nod to the dignity of the Tribunal de Yopougon.