```markdown
# Design System Document

## 1. Overview & Creative North Star: "The Corporate Catalyst"

The objective of this design system is to transition the UMD Sales Club from a "student organization" to a "professional pipeline." We are moving away from the standard academic template and toward a **High-End Editorial** experience that mirrors the world of executive business and modern fintech.

**The Creative North Star: The Corporate Catalyst**
This system is defined by institutional authority blended with high-velocity business energy. We achieve this through **Organic Brutalism**—using heavy, impactful typography and large-scale imagery, broken by intentional asymmetry. Elements should feel like they are floating on a series of premium, layered surfaces rather than being locked into a rigid, boxed-in grid. We will use the UMD heritage colors not as mere accents, but as deep, atmospheric washes that command attention.

---

## 2. Colors: Tonal Depth & Atmosphere

We are moving beyond flat color applications. Our palette is designed to create a sense of physical space and "visual soul" through light and shadow.

### The "No-Line" Rule
**Explicit Instruction:** Designers are prohibited from using 1px solid borders to section off content. Boundaries must be defined solely through:
1.  **Background Color Shifts:** Placing a `surface-container-low` section against a `surface` background.
2.  **Tonal Transitions:** Using subtle shifts between neutral tokens to define where one idea ends and another begins.

### Surface Hierarchy & Nesting
Treat the UI as a series of stacked, premium materials. 
*   **Base:** `surface` (#f9f9f9) acts as our primary canvas.
*   **Layering:** Use `surface-container-lowest` for cards to create a "lifted" effect against a `surface-container` background. This "nesting" creates natural depth without the clutter of lines.

### The "Glass & Gradient" Rule
To inject energy:
*   **Glassmorphism:** Use semi-transparent variants of `surface` or `primary_container` with a `backdrop-blur` (12px–20px) for navigation bars and floating action cards.
*   **Signature Textures:** Utilize a subtle linear gradient—from `primary_container` (#7a0019) to `primary` (#51000d)—on large CTAs and Hero backgrounds. This prevents the maroon from feeling "flat" and adds a luxurious, velvet-like depth.

---

## 3. Typography: Editorial Authority

We use two distinct typefaces to balance UMD’s academic roots with a corporate future.

*   **Display & Headlines (Public Sans):** This is our "Institutional" voice. It should be used with tight letter-spacing (-0.02em) and high contrast. Do not be afraid of massive scale. A `display-lg` headline should dominate the viewport, forcing the user to acknowledge the club’s presence.
*   **Body & Labels (Inter):** This is our "Functional" voice. Inter provides the precision required for business communication. 

**Hierarchy as Identity:**
- **Display-LG (3.5rem):** Used for bold, provocative statements.
- **Headline-MD (1.75rem):** Used for section headers, always in `on_surface_variant` to keep the hierarchy sophisticated.
- **Title-SM (1rem):** Bolded for sub-headers to provide a clear entry point for the eye.

---

## 4. Elevation & Depth: Tonal Layering

Traditional drop shadows are often a crutch for poor layout. In this design system, hierarchy is achieved through **Tonal Layering**.

*   **The Layering Principle:** Depth is "stacked." Place a `surface-container-lowest` card on top of a `surface-container-low` section. The minute difference in hex code creates a soft, natural lift that feels like high-quality stationery.
*   **Ambient Shadows:** If a floating element (like a modal or dropdown) is required, use a shadow with a blur of 30px–60px and an opacity of 4%–6%. The shadow color must be a tinted version of `on_surface` (a deep, desaturated maroon-grey) rather than pure black.
*   **The "Ghost Border" Fallback:** If accessibility requires a container boundary, use the `outline-variant` token at **15% opacity**. This creates a "Ghost Border" that guides the eye without interrupting the visual flow.
*   **Softened Edges:** Use the `xl` (0.75rem) roundedness for primary containers and `md` (0.375rem) for interactive elements like buttons.

---

## 5. Components: Styled for the Elite

### Buttons
*   **Primary:** A gradient from `primary_container` to `primary`. No border. White text. Large horizontal padding (2rem) to feel significant.
*   **Secondary:** `surface_container_highest` background with `on_surface` text. This should feel like a part of the page, only revealing its interactivity on hover via a subtle lift.
*   **Tertiary:** No background. Bold `primary` text with a 2px underline that expands on hover.

### Cards & Lists
*   **No Dividers:** Forbid the use of horizontal lines. Separate list items using the spacing scale (e.g., 24px vertical gap) or by alternating background tones between `surface` and `surface-container-low`.
*   **Interactive Cards:** On hover, a card should not move; instead, the background should shift from `surface-container-low` to `surface-container-highest` to signal focus.

### Input Fields
*   **Style:** Minimalist. A bottom-only `outline-variant` (20% opacity) that transforms into a `primary` (maroon) 2px line upon focus.
*   **Labels:** Always use `label-md` in `on_surface_variant`. Never use placeholder text as a label.

### Signature Component: The "Perspective" Stat
For the Sales Club’s success metrics (e.g., "95% Job Placement"), use an asymmetric layout where the number is in `display-lg` (Gold: `secondary_container`) and the description is tucked tightly underneath in `title-sm`.

---

## 6. Do’s and Don'ts

### Do:
*   **Embrace Negative Space:** If a section feels "empty," leave it. Professionalism is signaled through the luxury of unused space.
*   **Use Intentional Asymmetry:** Offset images from their text blocks. Let a photo of a corporate speaker bleed off the edge of the screen while the text stays centered.
*   **Prioritize Typography:** Let the scale of the words do the heavy lifting before adding decorative icons or images.

### Don’t:
*   **Don't use 100% Black:** Use `on_surface` (#1a1c1c) for text. It’s softer and more sophisticated.
*   **Don't use "Academic" Blue or Red:** Stick strictly to the Maroon/Gold/Neutral palette to maintain the UMD Sales Club's specific brand equity.
*   **Don't crowd the margins:** All containers should have a minimum of 32px internal padding. Tension is the enemy of a premium experience.
*   **Don't use default "Drop Shadows":** Refer to the Tonal Layering section. If it looks like a standard "box shadow," it’s wrong.

---

## 7. Signature Textures
To ensure the site feels "custom," use a subtle noise texture (3% opacity) overlaid on `primary_container` backgrounds. This creates a tactile, paper-like quality that resonates with both academic heritage and high-end business cards.