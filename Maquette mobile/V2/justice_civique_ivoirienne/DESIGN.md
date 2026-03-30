# Design System Document: Tribunal de Yopougon

## 1. Overview & Creative North Star: "The Civic Sanctuary"
This design system moves away from the cold, bureaucratic aesthetic typical of legal interfaces. Our Creative North Star is **"The Civic Sanctuary"**—a digital space that feels authoritative yet profoundly approachable. 

Instead of a rigid, boxy grid, we utilize **Intentional Asymmetry** and **Tonal Depth**. By breaking the "template" look with generous white space and overlapping editorial elements, we signal to the citizen that this is a premium, modern institution. The interface does not just provide information; it guides the user through a stressful process with the calm of a high-end architectural space.

---

## 2. Color Theory & Surface Logic
The palette reflects the Ivorian identity through a sophisticated Material 3 lens, prioritizing legibility and emotional reassurance.

### The "No-Line" Rule
**Explicit Instruction:** 1px solid borders for sectioning are strictly prohibited. Boundaries must be defined solely through background color shifts or subtle tonal transitions. For example, a `surface-container-low` card sits on a `surface` background to create a "soft edge."

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers—like stacked sheets of fine Ivorian vellum.
- **Base Layer:** `surface` (#f8f9ff)
- **Content Blocks:** `surface-container-low` (#f0f4fd)
- **Interactive Elevated Cards:** `surface-container-lowest` (#ffffff)
- **Deep Content Wells:** `surface-container-high` (#e4e8f1)

### The "Glass & Gradient" Rule
To avoid a flat, "out-of-the-box" feel, use **Glassmorphism** for floating action buttons or sticky headers. Apply a 20px Backdrop Blur to `surface` colors at 80% opacity. Use subtle gradients for Hero backgrounds, transitioning from `primary` (#006400) to `primary-container` (#008000) at a 135° angle to add "soul" and professional polish.

---

## 3. Typography: Editorial Authority
We use **Inter** not as a standard sans-serif, but as an editorial tool. The scale is high-contrast to ensure the most important legal status updates are impossible to miss.

| Level | Token | Size | Weight | Intent |
| :--- | :--- | :--- | :--- | :--- |
| **Display** | `display-md` | 2.75rem | 700 | Large, welcoming numbers (e.g., case counts). |
| **Headline** | `headline-sm` | 1.5rem | 600 | Page titles and primary section headers. |
| **Title** | `title-md` | 1.125rem | 500 | Card titles and sub-headings. |
| **Body** | `body-lg` | 1rem | 400 | Legal text and complaint descriptions. |
| **Label** | `label-md` | 0.75rem | 600 | Status badges and metadata (ALL CAPS). |

*Director's Note:* Pair a `display-md` number with a `label-md` descriptor to create asymmetrical hero stats that break the horizontal rhythm of the page.

---

## 4. Elevation & Depth
Depth is achieved through **Tonal Layering**, mimicking natural light rather than synthetic UI shadows.

- **The Layering Principle:** Stack `surface-container-lowest` on top of `surface-container-low`. The 2-step jump in brightness creates a natural lift.
- **Ambient Shadows:** For floating elements (like a "File New Complaint" button), use a diffused shadow: `Y: 8px, Blur: 24px, Color: rgba(23, 28, 34, 0.06)`. This mimics soft, ambient light.
- **The "Ghost Border" Fallback:** If a border is essential for accessibility, use `outline-variant` (#becab6) at **15% opacity**. Never use a 100% opaque border.
- **Glassmorphism:** Navigation bars should use a `surface` background with `backdrop-filter: blur(12px)` to allow the brand colors of the scrollable content to bleed through softly.

---

## 5. Components

### Buttons & CTAs
- **Primary:** Roundedness `xl` (0.75rem). Background: `primary` (#006400). Text: `on-primary` (#ffffff). Use a subtle inner-glow gradient for a "glass-press" effect.
- **Secondary (Action):** `secondary-container` (#fe9800) with `on-secondary-container` (#643900). Reserved for "Urgent" or "Update" actions.
- **Ghost Action:** No background. `tertiary` (#3a5296) text with `label-md` styling for "View Details."

### Input Fields & Search
- Forgo the standard box. Use a `surface-container-highest` background with a `none` border and a 2px `primary` underline that animates from the center on focus. This mimics the "underlining" of a legal document.

### Case Status Chips
- **Status: Pending:** `secondary-fixed` background, `on-secondary-fixed` text.
- **Status: Processed:** `primary-fixed` background, `on-primary-fixed` text.
- **Status: Action Required:** `error-container` background, `on-error-container` text.

### Cards & Lists (The No-Divider Rule)
- **Forbid dividers.** To separate complaints in a list, use vertical spacing (`spacing-4` / 1rem) and a background shift. Each complaint should be a `surface-container-lowest` card on a `surface-container-low` background.

### Signature Component: The Progress Ribbon
A vertical, asymmetric line using `tertiary` (#3a5296) that connects "milestone" nodes. The nodes use `primary` when complete and `outline-variant` when upcoming. This provides a clear, reassured "path to justice."

---

## 6. Do's and Don'ts

### Do
- **Do** use `spacing-10` (2.5rem) or larger for top-level page margins to create an "Editorial" feel.
- **Do** use the Ivorian flag in the logo as a small, sophisticated accent (6px height) rather than a dominant background element.
- **Do** leverage "Justice Blue" (`tertiary`) for all links and icons related to legal documentation to build cognitive association.

### Don't
- **Don't** use pure black (#000000). Use `on-surface` (#171c22) for all text to maintain a softer, high-end feel.
- **Don't** use "Alert Red" for everything. Reserve `error` (#ba1a1a) strictly for critical system failures; use `secondary` (Orange) for warnings to maintain a "Reassuring" tone.
- **Don't** use standard Material icons. Opt for thin-stroke (1.5pt) custom iconography that feels more like a legal seal.

---

## 7. Logo & Brand Integration
The logo **TRIBUNAL DE YOPOUGON** must be rendered in `title-lg`, tracked out (+5%), using `on-surface`. The CI Flag should be a minimalist 16x10px rectangle placed at the end of the text string, slightly offset vertically to align with the cap height of the typography.