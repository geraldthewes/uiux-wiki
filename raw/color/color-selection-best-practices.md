# Considerations to Select the Main Colors for an App

**For web applications, there is no single magic number**, but best practices strongly favor a **limited, structured, and systematic color palette** rather than dozens of ad-hoc hex values. This ensures visual consistency, reduces maintenance headaches, improves accessibility, and scales well across components, states (hover, active, disabled), and modes (light/dark).

### Recommended Number of Colors
Most experts and production design systems converge on this structure:

- **Core categories / base hues (roles)**: **4–10** (the “main colors” you define in your design guide).
  - **Primary** (brand color — usually 1)
  - **Secondary / Accent** (1–2, used sparingly)
  - **Neutral** (grays — 1 family)
  - **Semantic / Functional** (4–5: success, warning, error, info, sometimes neutral/brand info)

- **Shades / tints per base color**: **5–10** (commonly 8–17 values, e.g., 50/100/200/.../900 or lightness-based naming). This gives flexibility for backgrounds, text, borders, buttons, states, and dark mode without inventing new colors.

- **Total defined values**: Often 50–150+ organized tokens, but **only a handful of base colors** are chosen by designers. The rest are systematically generated.

**Popular usage guideline**: The **60-30-10 rule** (widely recommended for web/UI):
- **60%** — Dominant/neutral colors (backgrounds, panels, most text)
- **30%** — Secondary colors
- **10%** — Accent/highlight colors (CTAs, important actions)

This keeps interfaces calm and scannable.

**Real-world examples**:
- Small/simple web apps or MVPs: 4–6 core colors total.
- Mature design systems or complex SaaS apps: 8–12 base colors with full scales.
- Ant Design: 12 primary bases + derivatives (structured, not random).
- Many teams settle on **~6 core colors** (Primary, Secondary, 3 Accents + Neutrals/Semantic handled as families).

The goal is **control and harmony**, not minimalism for its own sake. Complex systems with hundreds of random colors lead to inconsistency and developer frustration.

### How to Select the Main Colors for App Elements
Here’s a practical, repeatable process used by professional teams:

1. **Start with your brand Primary color**  
   This becomes the hero color for primary buttons, active navigation, links, and key highlights. Pull it directly from brand guidelines (logo, marketing site). It should feel ownable and emotionally aligned with your product.

2. **Choose 1–2 Secondary/Accent colors for harmony**  
   Use color theory:
   - **Complementary** (high contrast, energetic)
   - **Analogous** (calm, cohesive)
   - **Triadic** (balanced vibrancy)
   Tools: Adobe Color Wheel, Coolors.co, or Paletton. Test against your primary.

3. **Build strong Neutrals (the real workhorse)**  
   Neutrals occupy ~60% of most screens. Use cool grays (with a slight blue or warm undertone depending on brand). Avoid pure black (#000) and pure white (#FFF) in most cases — they can feel harsh. Define 8–10 shades from near-black to near-white.

4. **Define Semantic colors with meaning**  
   - **Error/Danger**: Red (or red-orange)
   - **Success/Positive**: Green (or teal-green)
   - **Warning**: Orange/Yellow
   - **Info**: Blue (or a secondary brand blue)
   These must be distinct from your primary/secondary to avoid confusion.

5. **Generate systematic scales**  
   From each base hue, create lighter and darker versions while preserving usable saturation (HSL is better than RGB/HEX for this). Many teams use 10-step scales (50–900) so the “500” shade is the main usable color.

6. **Test accessibility immediately**  
   WCAG 2.2 AA minimum: **4.5:1** contrast for normal text, **3:1** for large text. Check pairs (text on background, button text, etc.). Test in both light and dark modes. Tools: WebAIM Contrast Checker, Stark (Figma), or browser dev tools.

7. **Document usage rules in your design guide**  
   Example: “Primary 500 — Primary CTAs and active states only. Never use for error states.” Use **design tokens** (Figma Variables + CSS custom properties) so developers implement exactly what designers intend.

**Pro tips**:
- Neutrals and semantic colors often matter more for daily usability than the flashy primary.
- Plan for dark mode from the start (many modern web apps require it).
- Avoid relying on color alone (use icons, labels, patterns for color-blind users).

### Best Articles & References
These are the most practical and widely respected resources:

**Must-Read Practical Guides**
- **Refactoring UI** by Steve Schoger & Adam Wathan (book + refactoringui.com) — One of the best hands-on resources. Breaks palettes into Greys (8–10 shades), Primary (1–2 colors), and Accents (3–4 semantic colors). Emphasizes defining shades *up front* and using HSL. Highly recommended for web app teams.
- **“Color in Design Systems”** by Nathan Curtis (EightShapes, Medium) — 16 excellent lessons on stabilizing primary palettes, limiting tints/shades, accessibility rituals, and avoiding endless options.
- **“Decoding the Art of Color Palettes for Scalable Design Systems”** by Rohan Kamath — Clear breakdown of the minimum 4 categories + how to build 10-shade extended palettes with accessibility in mind.
- **“You don’t need hundreds of colors to design your UI color system”** (UX Design Collective) — Practical case study on moving from random hex values to a clean, systematic palette.

**2025–2026 Overviews & Best Practices**
- **“UI Color Palette 2026: Best Practices...”** (Interaction Design Foundation / iXDF) — Covers 60-30-10 rule, color psychology, accessibility, and choosing primary/secondary/accent wisely.
- **Design Systems Guide – Color** (designsystems.com) — Excellent overview of controlled palettes, semantic usage, tokens, and brand integration.

**Official Design System References** (great for inspiration and real implementations)
- **Material Design 3 Color System** (Google) — Excellent role-based approach (Primary, Secondary, Tertiary, Error, Surface, etc.) and tonal palettes.
- **Carbon Design System – Color** (IBM) — Very thorough, with light/dark themes and accessibility focus.
- **Ant Design Colors** — Structured 12-color base palette with clear derivation rules.
- **US Web Design System (USWDS) Color Tokens** — Government-grade, highly accessible token system.

**Additional Strong Resources**
- WCAG 2.2 Contrast guidelines (official W3C)
- Lyft’s article on re-approaching color (mentioned in many design system guides)
- Tailwind CSS color system (as a real-world implementation example many web teams adopt or adapt)

### Quick Starting Recommendation for Most Web Apps
Define these in your design guide first:
1. Primary (brand) + 8–10 shades
2. 1 Accent/Secondary + 5–8 shades
3. Neutral gray family (8–10 shades)
4. Semantic set: Error, Warning, Success, Info (each with 5–7 shades)

This gives you everything you need for buttons, forms, navigation, alerts, data visualization, and dark mode while staying maintainable.