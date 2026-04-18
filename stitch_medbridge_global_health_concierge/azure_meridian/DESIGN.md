# Design System Strategy: The Curated Sanctuary

## 1. Overview & Creative North Star
**The Creative North Star: The Curated Sanctuary**
This design system rejects the sterile, "template-heavy" aesthetic of traditional medical portals. Instead, it positions world-class healthcare through the lens of high-end travel and bespoke hospitality. We are building a "Digital Sanctuary"—a space that feels as calm as a luxury lounge but as authoritative as a leading surgical center.

The experience is defined by **intentional asymmetry** and **breathable editorial layouts**. We break the rigid grid by allowing imagery to bleed off-canvas and using typography as a structural anchor. By leveraging overlapping elements and high-contrast typography scales, we create a sense of bespoke care rather than mass-produced service.

---

## 2. Colors: Tonal Depth & Soul
The palette moves beyond "healthcare blue" into a sophisticated spectrum of navy, slate, and ethereal whites.

*   **Primary Roles:** Use `primary` (#003461) for moments of absolute authority and `surface_tint` (#27609d) for interactive depth.
*   **The "No-Line" Rule:** To maintain a premium editorial feel, **1px solid borders are prohibited for sectioning.** Boundaries must be defined solely through background color shifts. For instance, a section in `surface_container_low` (#f3f4f5) sitting atop a `surface` (#f8f9fa) background provides a sophisticated, "borderless" containment.
*   **Surface Hierarchy & Nesting:** Treat the UI as physical layers of fine paper. 
    *   **Level 0:** `surface` (#f8f9fa) as the base canvas.
    *   **Level 1 (Sections):** `surface_container_low` (#f3f4f5) for secondary content areas.
    *   **Level 2 (Cards):** `surface_container_lowest` (#ffffff) for primary interactive objects to create a natural "lift."
*   **The "Glass & Gradient" Rule:** For floating navigation or mobile overlays, use Glassmorphism. Apply a backdrop blur (12px–20px) to a 70% opaque `surface_container_lowest`. 
*   **Signature Textures:** Use subtle linear gradients transitioning from `primary` (#003461) to `primary_container` (#004b87) for hero backgrounds. This prevents the "flat" look and adds a sense of "visual soul" and professional polish.

---

## 3. Typography: The Editorial Voice
We utilize a dual-typeface system to balance clinical precision with human warmth.

*   **The Authority (Manrope):** Used for `display` and `headline` scales. Its geometric yet friendly curves suggest a modern, world-class institution. Use `display-lg` (3.5rem) with tighter letter-spacing (-0.02em) to create high-impact editorial anchors.
*   **The Concierge (Public Sans):** Used for `title`, `body`, and `label` scales. It provides neutral, high-readability support. 
*   **Hierarchy as Identity:** Large `display-md` headlines should often be paired with `body-lg` (1rem) sub-text with generous leading (1.6) to ensure the interface feels spacious and unhurried—essential for patient trust.

---

## 4. Elevation & Depth: Tonal Layering
Traditional shadows are often "dirty" and break the clean medical aesthetic. We use **Tonal Layering** to convey hierarchy.

*   **The Layering Principle:** Depth is achieved by stacking surface-container tiers. A `surface_container_lowest` (#ffffff) card placed on a `surface_container` (#edeeef) section creates a soft, natural lift without the need for a shadow.
*   **Ambient Shadows:** When an element must float (e.g., a modal or a primary CTA), use an "Ambient Shadow." 
    *   **Spec:** Blur: 40px, Spread: 0, Color: `on_surface` (#191c1d) at 5% opacity. This mimics natural light rather than a digital effect.
*   **The "Ghost Border" Fallback:** If accessibility requires a stroke, use a "Ghost Border." Apply the `outline_variant` (#c2c6d1) at 15% opacity. **Never use 100% opaque borders.**
*   **Glassmorphism & Depth:** Use semi-transparent layers of `surface_container_lowest` with a backdrop blur on navigation bars. This allows the medical imagery or travel landscapes to bleed through, softening the interface's edges.

---

## 5. Components: Precision & Grace

*   **Buttons:**
    *   *Primary:* Solid `primary` (#003461) with `on_primary` (#ffffff) text. Use `rounded-lg` (0.5rem) to balance softness and professionalism.
    *   *Tertiary (Ghost):* No background or border. Use `primary` text with a 4px underline in `primary_fixed` (#d3e4ff) for a high-end editorial feel.
*   **Cards & Lists:** 
    *   **Forbid divider lines.** Use vertical white space (32px or 48px from the spacing scale) or subtle background shifts between `surface_container_low` and `surface_container_high` to separate content.
*   **Input Fields:** Use a "Minimalist Tray" style. No full border; use a `surface_container_highest` (#e1e3e4) background with a 2px `primary` bottom-border that activates on focus.
*   **Concierge "Status" Chips:** Use `secondary_container` (#d2e1f2) with `on_secondary_container` (#556472) text. Shapes should be `full` rounded for a soft, pill-like "calm" aesthetic.
*   **Travel Itinerary Stepper:** A bespoke component for medical travel. Use thin vertical lines in `outline_variant` at 30% opacity, with active nodes highlighted in `primary`.

---

## 6. Do's and Don'ts

### Do:
*   **Embrace White Space:** Treat white space as a luxury feature, not "empty" space.
*   **Use Intentional Asymmetry:** Align text to the left but allow imagery to sit slightly off-center to create an organic, high-end feel.
*   **Prioritize Accessibility:** Ensure that while layers are subtle, the `on_surface` (#191c1d) text always maintains a high contrast ratio against `surface` containers.

### Don't:
*   **Don't use "Pure" Greys:** Always use the tinted neutrals provided (e.g., `secondary`, `tertiary`) to keep the "calming blue" soul of the brand alive.
*   **Don't over-shadow:** If you need more contrast, change the background color of the container instead of adding a heavier shadow.
*   **Don't use standard icons:** Use "Light" or "Thin" weight iconography (1px stroke) to match the sophisticated typography scale.