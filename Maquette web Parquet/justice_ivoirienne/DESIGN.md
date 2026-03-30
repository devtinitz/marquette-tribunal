# Design System: Excellence Judiciaire

## 1. Overview & Creative North Star: "The Digital Magistrate"
This design system moves away from the "cluttered bureaucracy" of traditional legal platforms, embracing a Creative North Star we call **"The Digital Magistrate."** 

The aesthetic is rooted in authoritative clarity, using intentional asymmetry and high-contrast editorial typography to guide the user through complex judicial data. We reject the "standard grid" in favor of a layered, editorial layout that feels as prestigious as a high court chamber. By utilizing breathing room (whitespace) and tonal depth instead of rigid borders, we create an environment that feels secure, modern, and profoundly professional.

---

## 2. Color Strategy & Surface Logic
The palette honors the Ivorian national identity while introducing a sophisticated "Justice Blue" for critical gravity.

### Tonal Hierarchy
*   **Primary (`#006400`):** Used for growth and resolution states. Represents the official green of the Republic.
*   **Secondary (`#8a5100`):** Reserved for alerts or "Action Required" status without the alarmism of red.
*   **Tertiary/Accent (`#3a5296`):** The "Justice Blue." This is our color of authority, used for final decisions and critical judicial actions.

### The "No-Line" Rule
To achieve a premium, modern feel, **1px solid borders are strictly prohibited for sectioning.** Boundaries must be defined through background color shifts:
*   **Background:** `surface` (`#f9f9f6`)
*   **Sectioning:** Place a `surface-container-low` (`#f3f4f1`) area on top of the main background to define a zone.
*   **Nesting:** For an even deeper level of focus, use `surface-container-high` (`#e8e8e5`) inside a lower tier. This creates a "sheet-on-sheet" physical feel.

### The "Glass & Gradient" Rule
For floating elements like "Nouveau Dossier" modals or judicial sidebars, use **Glassmorphism**:
*   **Background:** `surface_variant` at 80% opacity.
*   **Effect:** `backdrop-blur` (12px to 20px).
*   **Signature Texture:** Use a subtle linear gradient (from `primary` to `primary_container`) on main action buttons to provide a "silk-finish" depth that differentiates the UI from generic flat designs.

---

## 3. Typography: Editorial Authority
We use **Inter** exclusively, but we treat it with the spacing of a high-end legal gazette.

*   **Display (lg/md):** Used for total case counts or major landing headers. Kerned slightly tighter (-0.02em) to feel impactful.
*   **Headline (sm/md):** Used for "Détails de la Plainte." These carry the weight of the document.
*   **Body (md/lg):** Optimized for readability in long-form legal descriptions. Line height should be generous (1.6x) to reduce cognitive load.
*   **Label (sm/md):** Used for metadata (Dates, ID Numbers). Always uppercase with +0.05em letter spacing to maintain a "stamped" official look.

---

## 4. Elevation & Depth: Tonal Layering
Traditional shadows are often "dirty." In this system, we use light and tone to define space.

*   **The Layering Principle:** Place a `surface-container-lowest` card on a `surface-container-low` section. This creates a soft, natural lift that mimics fine ivory paper.
*   **Ambient Shadows:** For floating sidebars or tooltips, use a shadow with a 24px blur and only 6% opacity, tinted with the `on-surface` color (`#1a1c1a`). It should look like a glow of depth, not a drop-shadow.
*   **The "Ghost Border":** If accessibility requires a stroke, use `outline-variant` (`#becab6`) at **15% opacity**. It should be felt, not seen.

---

## 5. Signature Components

### Judicial Sidebar
A fixed-position container using `surface_container_low`. It does not have a border on the right; instead, it uses a subtle `surface_dim` background shift to separate it from the main content.

### Status Badges (Les Macarons de Statut)
Do not use heavy, solid backgrounds. Use a "Soft Tint" approach:
*   **Classement:** `surface-container` background with `on-surface` text.
*   **Poursuites:** `primary-container` background with `on-primary-fixed-variant` text.
*   **Instruction:** `tertiary-container` background with `on-tertiary-fixed-variant` text.
*   *Shape:* Use `roundedness.full` for a pill shape that stands out against the angular judicial grid.

### Official Data Tables
*   **No Dividers:** Remove all horizontal and vertical lines.
*   **Separation:** Use `spacing.4` vertical padding. Every second row uses `surface-container-lowest` as a subtle zebra stripe.
*   **Header:** `label-md` typography, all caps, using `on-surface-variant`.

### Critical Action Buttons (Justice Blue)
*   **Color:** `tertiary` (`#3a5296`).
*   **Style:** `roundedness.md`.
*   **Interaction:** On hover, transition to `tertiary_container`. These buttons represent "Le Droit" (The Law) and should feel heavy and intentional.

---

## 6. Do’s and Don’ts

### Do
*   **Do** use `spacing.16` or `spacing.20` for page margins to allow the content to breathe like a luxury document.
*   **Do** use `tertiary` (`#002366`) for the most important judicial actions (e.g., "Signer l'ordonnance").
*   **Do** ensure Dark Mode uses `surface-dim` for backgrounds to maintain the "Legal Paper" texture without eye strain.

### Don’t
*   **Don't** use pure black (`#000000`) for text. Use `on-surface` (`#1a1c1a`) to keep the interface feeling premium.
*   **Don't** use icons without labels. In a judicial context, clarity is legally required; icons should only supplement text.
*   **Don't** use "Alert Red" for everything. Use the `secondary` (Ivorian Orange) for warnings to maintain a professional, calm environment.

---

## 7. French Localization & Tone
The tone of all micro-copy must be **Soutenu** (Formal).
*   *Instead of:* "Supprimer le fichier" -> *Use:* "Révoquer la pièce jointe"
*   *Instead of:* "Ok" -> *Use:* "Confirmer la saisie"
*   *Instead of:* "Erreur" -> *Use:* "Anomalie de procédure"