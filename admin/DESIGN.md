# Design System: High-End Editorial Ceramics

## 1. Overview & Creative North Star
### The Creative North Star: "The Earth’s Echo"
This design system moves away from the rigid, sterile grids of typical e-commerce. It treats the digital screen as a curated gallery space. The brand identity of "MAGMA CERÁMICA" is rooted in the earth, the kiln, and the hand of the maker. 

To break the "template" look, the system employs **The Kinetic Stillness**—a layout strategy using intentional asymmetry, generous negative space, and large-scale editorial typography that feels as though it was typeset for a premium print monograph. We avoid the "boxed-in" feeling by overlapping product imagery with typography and using a tonal layering system that feels like stacked sheets of handmade paper.

---

## 2. Colors
The palette is a sophisticated blend of raw earth minerals and soft, atmospheric neutrals. 

- **Primary (`#8a3b2d`):** Used for signature accents and brand moments.
- **Secondary (`#745949`):** Grounding earth tones for supporting elements.
- **Surface & Neutrals (`#fcf9f4`, `#f0ede8`):** These are the "air" of the system, providing the calm, gallery-like backdrop.

### The "No-Line" Rule
**Explicit Instruction:** Prohibit the use of 1px solid borders for sectioning or containment. Boundaries must be defined solely through background color shifts. For example, a `surface-container-low` section should sit directly on a `surface` background to denote a change in context. This creates a "seamless" feel that mimics natural transitions in light and shadow.

### Surface Hierarchy & Nesting
Treat the UI as a physical stack of materials. 
- Use the `surface-container` tiers (Lowest to Highest) to create depth. 
- **Layering Pattern:** Place a `surface-container-lowest` card on a `surface-container-low` section. This subtle contrast defines the component’s footprint without the need for harsh structural lines.

### The "Glass & Gradient" Rule
To add a premium "soul" to the interface:
- **Glassmorphism:** Use semi-transparent surface colors (e.g., `surface` at 80% opacity) with a `backdrop-blur(12px)` for floating navigation or sticky filters.
- **Signature Gradients:** Use a subtle linear gradient from `primary` to `primary-container` for CTAs. This creates a "glazed" look reminiscent of fired ceramic, moving beyond the flatness of standard web buttons.

---

## 3. Typography
The typography is a dialogue between the artisanal (`notoSerif`) and the precise (`manrope`).

- **Display & Headlines (`notoSerif`):** These are the "voice" of the brand. Use `display-lg` and `headline-lg` with generous tracking and occasional italicization for an editorial, high-end feel. 
- **Titles & Body (`manrope`):** Used for functional clarity. `manrope` provides a modern, clean contrast to the serif headings, ensuring the shop remains highly usable and accessible.
- **Hierarchy as Identity:** The massive contrast between a `display-lg` headline and a `label-sm` technical detail (e.g., weight, dimensions) mimics the layout of a museum exhibit placard.

---

## 4. Elevation & Depth
In this system, depth is felt rather than seen. We reject the "heavy shadow" aesthetic.

- **The Layering Principle:** Stacking `surface-container` tiers is the primary method of elevation. This is a "Tonal Lift" approach.
- **Ambient Shadows:** For elements that truly float (like a cart drawer or a modal), use a shadow color tinted with the brand’s clay tones: `rgba(138, 59, 45, 0.06)`. Blur values must be high (24px to 48px) to mimic soft, ambient studio lighting.
- **The "Ghost Border" Fallback:** If a container needs further definition, use the `outline-variant` token at **15% opacity**. This creates a "whisper" of a line that guides the eye without interrupting the flow.
- **Backdrop Blurs:** Apply a subtle blur to any layer sitting above image content to maintain the "frosted glass" aesthetic, ensuring text remains legible while keeping the colors of the ceramics underneath visible.

---

## 5. Components

### Buttons
- **Primary:** Gradient fill (`primary` to `primary-container`), no border, `rounded-md` (0.75rem). Text in `on-primary`.
- **Secondary:** Surface-tinted background (`surface-container-highest`) with `on-surface` text.
- **Interaction:** On hover, a subtle increase in shadow spread (ambient) and a 1% scale increase.

### Cards (Product & Story)
- **Structure:** No borders. Use `surface-container-low` for the card background. 
- **Imagery:** Aspect ratios should be intentional (e.g., 4:5 or 2:3) to feel more like a photography portfolio.
- **Spacing:** Minimum 24px padding within cards to ensure "much air."

### Input Fields
- **Style:** Underline only or a very soft `surface-container-high` background. 
- **Ghost Border:** Use the 15% opacity `outline-variant` for the bottom border. 
- **Focus:** Transition the underline to `primary` with a 2px stroke.

### Specialized Component: The "Curator List"
Instead of a standard horizontal divider, use a 48px vertical gap between list items. Every third item in a product list should be sized differently (asymmetric) to maintain the "organic" feel of the system.

---

## 6. Do's and Don'ts

### Do:
- **Do** allow text to breathe. If you think there is enough margin, double it.
- **Do** use `notoSerif` for storytelling and `manrope` for transaction.
- **Do** utilize the `surface-variant` and `surface-container` shifts to separate "Inspiration" content from "Shopping" content.
- **Do** ensure all ceramic product shots have consistent lighting to complement the ambient shadow system.

### Don't:
- **Don't** use 100% black (`#000000`) for text. Use `on-surface` (`#1c1c19`) to keep the warmth.
- **Don't** use hard-edged rectangles. Always apply the `rounded-sm` to `rounded-lg` scale to mimic the softness of clay.
- **Don't** use "Alert Red" for errors if possible. Use the `error` token (`#ba1a1a`) which is tuned to the siena/terracota palette.
- **Don't** use standard 12-column grids strictly. Allow elements to break the margin to create visual interest.