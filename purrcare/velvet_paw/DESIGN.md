# Design System: The Empathetic Guardian

## 1. Overview & Creative North Star
This design system is built upon the Creative North Star of **"The Digital Sanctuary."** It moves beyond a functional health utility into an immersive, nurturing environment. By eschewing rigid grids and harsh borders in favor of organic layering and soft tonal shifts, we create a space that feels as comforting as a pet's presence.

The experience breaks the "template" look by using **Intentional Asymmetry**. We utilize the "paw print trail" watermark not just as a background, but as a compositional guide—elements should feel as though they are gently resting or floating along this path. We prioritize breathing room (whitespace) to reduce cognitive load for pet owners who may be in high-stress situations.

---

## 2. Colors & Surface Philosophy
Our palette balances the authority of deep purple with the nurturing warmth of pastel pinks.

### The Color Tokens
*   **Primary (`#461599`):** Our "Command" color. Used for high-level information and primary actions to signify trust and expertise.
*   **Primary Container (`#5E35B1`):** A softer variant for prominent UI elements like large pill buttons.
*   **Secondary (`#964261` / `#F48FB1`):** The "Heart" of the app. Used for accents, progress indicators, and active states.
*   **Background (`#F9F9F9`):** A soft off-white that acts as the canvas for our subtle pink paw-print watermark.

### The "No-Line" Rule
**Strict Prohibition:** Designers are prohibited from using 1px solid borders to section content. Boundaries must be defined solely through background color shifts.
*   Use `surface-container-low` for secondary sections sitting on a `surface` background.
*   Let the content breathe; use the Spacing Scale (specifically `spacing-8` and `spacing-10`) to create "invisible" boundaries.

### The "Glass & Gradient" Rule
To elevate the "Modern Minimalist" aesthetic:
*   **Floating Elements:** Use `surface-container-lowest` with an 80% opacity and a `20px` backdrop blur for modals and floating action buttons.
*   **Signature Textures:** Apply a subtle linear gradient to main Hero cards (from `primary-container` to `primary`) to provide depth and "soul" that flat hex codes cannot achieve.

---

## 3. Typography
We utilize **Plus Jakarta Sans**, a modern rounded sans-serif that balances legibility with a friendly, approachable terminal.

*   **Display & Headline Scale:** Large, empathetic type sizes (e.g., `display-md` at 2.75rem) should be used for welcoming the user or stating health milestones. This creates an editorial, high-end feel.
*   **Title Scale:** Used for card headers. These should always be in `on-surface` to maintain clear information hierarchy.
*   **Body Scale:** Reserved for medical notes and pet details. Use `body-lg` for readability; never go below `body-sm` for accessibility.
*   **Tonal Expression:** Use `primary` (Deep Purple) for headlines to project confidence, and `on-surface-variant` for body text to keep the interface feeling "soft" and non-aggressive.

---

## 4. Elevation & Depth: Tonal Layering
Traditional shadows are too "tech." We use **Ambient Layering** to create a physical sense of care.

*   **The Layering Principle:** Stack `surface-container` tiers. 
    *   *Base:* `background` (#F9F9F9)
    *   *Section:* `surface-container-low` (#F3F3F3)
    *   *Card:* `surface-container-lowest` (#FFFFFF)
*   **Ambient Shadows:** When a card requires "lift" (e.g., a pet's health summary), use a `xl` shadow: `Blur: 40px, Spread: 0, Opacity: 4%, Color: #5E35B1 (Primary)`. This creates a soft, purple-tinted glow rather than a grey "drop" shadow.
*   **The "Ghost Border" Fallback:** If a divider is essential for accessibility (e.g., in a complex list), use the `outline-variant` token at **15% opacity**. Anything more is too loud.

---

## 5. Components

### Buttons: The "Soft Pillar"
*   **Primary Button:** Large, pill-shaped (`rounded-full`). Background: `primary-container`. Text: `on-primary`. 
*   **Interaction:** On tap, the button should subtly scale (0.98) and deepen in color to `primary`.
*   **Secondary Button:** Ghost style with a `15% opacity` pink accent stroke.

### Navigation: The Sanctuary Bar
*   **Structure:** Solid `#FFFFFF` background. No top border; use a very soft ambient shadow.
*   **Active State:** The active icon (Paw, AI Sparkles, etc.) is centered over a **Soft Glow Circle** in `secondary-fixed` (#FFD9E2) with a 50% opacity. This creates a "halo" effect.

### Cards & Lists: The Organic Container
*   **Shape:** Use `rounded-lg` (2rem) or `rounded-xl` (3rem) for a friendly, non-clinical feel.
*   **Anti-Divider Policy:** Forbid the use of line dividers in lists. Use `surface-container-low` background blocks or vertical whitespace (`spacing-6`) to separate pet records.
*   **Avatars:** All pet and vet profiles must be perfectly circular (`rounded-full`) with a 2px `secondary` (pink) ring if they have an active status or notification.

### Specialized AI Component: The "Sparkle" Layer
*   For the AI pet-health assistant, use a **Glassmorphic Container**. A semi-transparent white box with a high backdrop blur, floating over the paw-print trail. This makes the AI feel "light" and magical.

---

## 6. Do's and Don'ts

### Do:
*   **Do** embrace the asymmetry of the paw-print trail; let it guide the eye toward call-to-action buttons.
*   **Do** use "Negative Space" as a design element. If a screen feels crowded, remove a container before you shrink the text.
*   **Do** ensure all interactive elements have a minimum tap target of 48x48dp.

### Don't:
*   **Don't** use pure black `#000000`. Use `on-surface` (#1A1C1C) for all "black" text to keep the palette soft.
*   **Don't** use standard "Material Design" shadows. They are too industrial for an empathetic pet app.
*   **Don't** use sharp 90-degree corners. Everything in this system—from buttons to input fields—must have at least a `rounded-sm` (0.5rem) radius.