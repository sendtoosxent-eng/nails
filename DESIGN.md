# The Design System: High-End Editorial for Luxury Nail Artistry

## 1. Overview & Creative North Star
**Creative North Star: "The Tactile Atelier"**

This design system moves beyond the "standard beauty app" by treating the digital interface as an extension of a physical luxury salon. We reject the rigid, boxy constraints of traditional web design in favor of a fluid, mobile-app-first experience that feels as curated as a high-end fashion editorial. 

The system utilizes **intentional asymmetry** and **tonal depth** to create a sense of calm and exclusivity. By prioritizing breathing room (whitespace) and soft, organic layering, we ensure the user feels pampered from the first tap. We break the "template" look by overlapping high-contrast typography with soft-edged imagery, creating a sophisticated, layered "scrapbook" feel that resonates with a premium clientele.

---

## 2. Colors: Tonal Sophistication
The palette is a curated selection of rose-tinted neutrals, warm nudes, and metallic accents, designed to feel "skin-like" and inviting.

*   **Primary (`#7c5455`):** A sophisticated dusty rose used for high-impact brand moments and active states.
*   **Secondary (`#675c56`):** A taupe neutral for secondary actions and supporting text.
*   **Tertiary (`#775a19`):** Our "Gold Accent." Use this sparingly for premium callouts or luxury service indicators.

### The "No-Line" Rule
**Explicit Instruction:** Traditional 1px solid borders are strictly prohibited for sectioning. Use background shifts to define boundaries. 
*   Place a `surface-container-low` (#f5f3f1) card on a `background` (#fbf9f7) to define its shape. 
*   Separation is achieved through color transitions, never through "drawing boxes."

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers.
1.  **Base:** `surface` (#fbf9f7) - The canvas.
2.  **Sectioning:** `surface-container-low` (#f5f3f1) - Use for large background areas or grouped content.
3.  **Emphasis:** `surface-container-lowest` (#ffffff) - Use for high-priority cards or input fields to make them "pop" forward.

### The "Glass & Gradient" Rule
To elevate the interface, apply **Glassmorphism** to floating elements (like navigation bars or modals). Use `surface` colors at 80% opacity with a `20px` backdrop blur. For Hero sections, utilize a subtle linear gradient from `primary` (#7c5455) to `primary_container` (#d7a6a7) at a 45-degree angle to add "visual soul."

---

## 3. Typography: Editorial Authority
We utilize a pairing of **Plus Jakarta Sans** for expressive, editorial moments and **Inter** for high-utility, functional reading.

*   **Display & Headlines (Plus Jakarta Sans):** These are the "voice" of the brand. Use `display-lg` (3.5rem) for hero statements, allowing them to overlap images slightly to break the grid.
*   **Body & Labels (Inter):** These provide the "service." Use `body-md` (0.875rem) for most descriptions. Inter’s tall x-height ensures legibility even on small mobile screens.
*   **Signature Contrast:** Always pair a large `headline-lg` with a small `label-md` in all-caps (tracked out +10%) to create a high-end fashion magazine hierarchy.

---

## 4. Elevation & Depth: The Layering Principle
Hierarchy is achieved through **Tonal Layering** rather than structural lines or heavy shadows.

*   **Ambient Shadows:** If an element must float (e.g., a "Book Now" FAB), use a shadow with a blur of `32px`, an offset of `y: 8px`, and an opacity of `4%`. The shadow color must be a tinted version of `on-surface` (#1b1c1b), never pure black.
*   **The "Ghost Border" Fallback:** If accessibility requires a border, use the `outline-variant` (#d5c2c2) token at **15% opacity**. It should be felt, not seen.
*   **Glassmorphism:** Use `surface_container_lowest` at 70% opacity with a blur to create "frosted glass" overlays. This softens the interface and makes the app feel integrated with the photography beneath it.

---

## 5. Components: Softness & Intention

### Buttons
*   **Primary:** Background: `primary` (#7c5455), Text: `on_primary` (#ffffff). Shape: `full` (9999px) or `xl` (3rem). 
*   **Secondary:** Background: `secondary_container` (#efe0d8), Text: `on_secondary_container` (#6d625c).
*   **Micro-Interaction:** Upon hover/tap, the button should subtly scale (1.02x) rather than just changing color.

### Input Fields
*   **Style:** Background: `surface_container_lowest` (#ffffff). No visible border. Use `DEFAULT` (1rem) rounded corners.
*   **Focus:** Indicate focus with a soft glow using `primary` at 20% opacity, rather than a sharp stroke.

### Cards & Service Lists
*   **Rule:** **No Divider Lines.** 
*   Separate services in a list using `1.4rem` (Spacing 4) of vertical whitespace. 
*   Group related items within a `surface-container-low` container with `lg` (2rem) rounded corners.

### Custom Component: The "Luxury Reveal" Image Card
For showcasing nail art, use an asymmetrical card where the image has a `xl` (3rem) radius on the top-left and bottom-right, but a `sm` (0.5rem) radius on the others. This creates a custom, high-design signature look.

---

## 6. Do's and Don'ts

### Do:
*   **Do** use the `16` (5.5rem) spacing token for top-of-page margins to create a sense of luxury.
*   **Do** use `primary_fixed` (#ffdada) for background highlights on text to draw the eye softly.
*   **Do** ensure all "tappable" elements are at least 44px in height, maintaining the mobile-app-like feel.

### Don't:
*   **Don't** use pure black (#000000) for text. Always use `on_surface` (#1b1c1b).
*   **Don't** use sharp corners. The minimum radius should be `DEFAULT` (1rem).
*   **Don't** cram content. If a screen feels busy, increase the spacing by one tier on the scale (e.g., move from `6` to `8`).
*   **Don't** use standard "drop shadows." If it looks like a default Photoshop style, it is too heavy.