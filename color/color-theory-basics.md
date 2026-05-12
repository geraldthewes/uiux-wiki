# Color Theory Basics for UI/UX Design

Color theory is the foundation of effective visual design in user interfaces. Understanding how colors work together and affect user perception is essential for creating accessible, aesthetically pleasing, and functional designs.

## The Color Wheel

The color wheel is a circular diagram that shows the relationships between colors. It's organized based on the visible spectrum and helps designers understand color harmony.

### Primary Colors
- Red, Blue, Yellow (in traditional color theory)
- Red, Green, Blue (RGB - for digital displays)
- Cyan, Magenta, Yellow (CMYK - for print)

### Secondary Colors
Created by mixing two primary colors:
- Orange (Red + Yellow)
- Green (Blue + Yellow)
- Purple (Red + Blue)

### Tertiary Colors
Created by mixing a primary and secondary color:
- Red-Orange, Yellow-Orange, Yellow-Green, Blue-Green, Blue-Purple, Red-Purple

## Color Harmony Principles

Color harmony refers to the pleasing arrangement of colors. Several established color schemes create harmonious combinations:

### Complementary
Colors opposite each other on the color wheel (e.g., blue and orange). Creates high contrast and vibrancy.

### Analogous
Colors next to each other on the color wheel (e.g., blue, blue-green, green). Creates harmonious, serene designs.

### Triadic
Three colors equally spaced around the color wheel (e.g., red, yellow, blue). Offers vibrant contrast while maintaining balance.

### Split-Complementary
A base color plus the two colors adjacent to its complement (e.g., blue with yellow-orange and red-orange). Provides contrast with less tension than complementary.

### Tetradic (Rectangle)
Four colors arranged into two complementary pairs (e.g., blue and orange with red and green). Offers rich color possibilities but can be challenging to balance.

### Monochromatic
Variations in lightness and saturation of a single color. Creates cohesive, elegant designs with subtle contrast.

## Color Properties

Understanding the three main properties of color helps in precise color selection and manipulation:

### Hue
The pure color itself (e.g., red, blue, green). Represents where the color falls on the color wheel (0-360 degrees).

### Saturation (Chroma)
The intensity or purity of the color. Ranges from 0% (gray) to 100% (full color). High saturation = vivid; low saturation = muted.

### Value (Lightness/Brightness)
How light or dark the color is. Ranges from 0% (black) to 100% (white). Affects contrast and readability.

## Color Models for Digital Design

Different color models serve different purposes in UI/UX design:

### RGB (Red, Green, Blue)
- Additive color model used for digital screens
- Values range from 0-255 for each channel
- Example: rgb(255, 0, 0) for pure red
- Used in CSS: `rgb(255, 0, 0)` or `rgb(100%, 0%, 0%)`

### HEX (Hexadecimal)
- Hexadecimal representation of RGB values
- Format: #RRGGBB (e.g., #FF0000 for red)
- Shorthand format: #RGB (e.g., #F00 for red)
- Most commonly used in web design

### HSL (Hue, Saturation, Lightness)
- More intuitive for designers than RGB
- Hue: 0-360 degrees (0=red, 120=green, 240=blue)
- Saturation: 0-100% (0=gray, 100=full color)
- Lightness: 0-100% (0=black, 50=normal, 100=white)
- Example: hsl(0, 100%, 50%) for pure red
- CSS: `hsl(0, 100%, 50%)`

### HSV/HSB (Hue, Saturation, Value/Brightness)
- Similar to HSL but uses Value/Brightness instead of Lightness
- Value: 0-100% (0=black, 100=full brightness)
- Often used in color pickers and design tools

## Color Psychology and Associations

Colors evoke emotional and psychological responses that can influence user behavior:

### Warm Colors
- **Red**: Energy, passion, urgency, danger, importance
- **Orange**: Enthusiasm, creativity, friendliness, confidence
- **Yellow**: Happiness, optimism, attention, caution

### Cool Colors
- **Blue**: Trust, stability, calmness, professionalism, sadness
- **Green**: Growth, nature, health, wealth, envy
- **Purple**: Luxury, spirituality, creativity, mystery

### Neutral Colors
- **Black**: Sophistication, power, elegance, mourning
- **White**: Purity, simplicity, cleanliness, emptiness
- **Gray**: Neutrality, balance, sophistication, depression
- **Brown**: Stability, reliability, comfort, dullness

## Color Accessibility

Ensuring color choices are accessible to all users, including those with visual impairments:

### Contrast Ratios
- WCAG 2.1 AA requires:
  - Normal text: minimum 4.5:1 contrast ratio
  - Large text (18pt+ or 14pt+ bold): minimum 3:1 contrast ratio
- WCAG 2.1 AAA requires:
  - Normal text: minimum 7:1 contrast ratio
  - Large text: minimum 4.5:1 contrast ratio

### Color Blindness Considerations
- Approximately 8% of men and 0.5% of women have some form of color blindness
- Most common types: deuteranomaly (green-blind) and protanomaly (red-blind)
- Don't rely solely on color to convey information
- Use patterns, textures, labels, or icons alongside color
- Test designs with color blindness simulators

### Tools for Accessibility Testing
- WebAIM Contrast Checker
- Stark (Sketch/Figma/Adobe XD plugin)
- Color Oracle (free color blindness simulator)
- axe DevTools (browser extension for accessibility testing)

## Creating Effective Color Palettes

Steps for developing a UI/UX color palette:

1. **Define Purpose and Personality**
   - What emotions should the interface evoke?
   - What brand personality are we expressing?
   - What is the context of use (professional, playful, etc.)?

2. **Choose a Base Color**
   - Select a primary color that represents the brand/core purpose
   - Consider cultural associations and target audience

3. **Build Supporting Colors**
   - Secondary colors for accents and highlights
   - Neutral colors for backgrounds, text, and UI elements
   - Status colors (success, warning, error, info)

4. **Establish Usage Guidelines**
   - Define where each color should be used
   - Create rules for color combinations and proportions
   - Document accessibility requirements

5. **Test and Iterate**
   - Check contrast ratios for all text/background combinations
   - Test with color blindness simulators
   - Gather user feedback on color effectiveness
   - Refine based on testing results

## Common UI Color Applications

### Primary Colors
- Used for main branding elements
- Applied to primary action buttons
- Used for key navigation elements
- Typically the most prominent color in the interface

### Secondary Colors
- Used for secondary actions and less prominent elements
- Applied to hover states, active states
- Used for highlighting information
- Should complement but not compete with primary colors

### Neutral Colors
- Backgrounds (pages, cards, modals)
- Text (primary, secondary, disabled)
- Borders, dividers, subtle UI elements
- Form fields, input backgrounds

### Status Colors
- Success: Green (typically #28a745 or similar)
- Warning: Amber/Orange (typically #ffc107 or similar)
- Error: Red (typically #dc3545 or similar)
- Info: Blue (typically #17a2b8 or similar)

### Interactive States
- Hover: Usually 10-20% lighter/darker than base color
- Active/Pressed: Usually 20-30% lighter/darker than base color
- Disabled: Usually reduced opacity (often 50%) or moved toward neutral

## Platform-Specific Color Guidelines

### Material Design 3
- Uses a tonal palette system with 5 tones for each color
- Emphasizes expressive color with dynamic theming
- Primary, secondary, and tertiary colors from brand
- Neutral colors derived from surface tones
- Uses color roles rather than fixed assignments

### Apple Human Interface Guidelines
- Recommends using system colors for consistency
- Emphasizes vibrancy and translucency effects
- Provides specific color palettes for different platforms (iOS, macOS, watchOS)
- Encourages limited use of custom colors for branding

### Web Content Accessibility Guidelines (WCAG)
- Focuses on contrast ratios and color use
- Requires non-color-dependent information conveyance
- Provides specific technical requirements for color accessibility

## Resources for Color Inspiration and Tools

### Color Palette Generators
- Coolors.co
- Adobe Color
- Paletton
- Colormind
- Khroma (AI-powered)

### Color Inspiration Sites
- Dribbble
- Behance
- Color Hunt
- UI Gradients
- Material Design Color Tool

### Accessibility Tools
- WebAIM Contrast Checker
- Contrast Ratio (by Lea Verou)
- Stark
- Color Oracle
- axe DevTools

### Design System References
- Material Design 3 Color System
- Apple Human Interface Guidelines Color
- Atlassian Design System Color
- IBM Design Language Color
- Salesforce Lightning Design System Color

## Best Practices for Color in UI/UX

1. **Start with Grayscale**: Design layout and hierarchy in grayscale first, then add color
2. **Limit Palette Size**: Typically 1-3 primary colors, 1-2 secondary colors, and neutrals
3. **Consider Context**: Colors appear differently based on surrounding colors and lighting
4. **Maintain Consistency**: Use the same colors for the same purposes throughout the interface
5. **Test Across Devices**: Colors can vary significantly between different screens and calibrations
6. **Document Usage**: Create clear guidelines for when and how to use each color
7. **Consider Cultural Context**: Color meanings vary across cultures
8. **Prioritize Functionality**: Aesthetic choices should never compromise usability or accessibility
9. **Use Color Purposefully**: Every color choice should serve a specific purpose in the interface
10. **Iterate Based on Feedback**: Test color choices with real users and refine based on results

## See Also
- [Color Palettes](./color-palettes.md)
- [Color Accessibility](./color-accessibility.md)
- [Material Design Color](./material-design/color.md)
- [Apple HIG Color](./apple-hig/color.md)
- [Color Psychology](./color-psychology.md)

## Tags
#color #design-theory #ui-design #ux-design #accessibility #color-psychology #color-harmony

## Source
Adapted from UI/UX design best practices, Material Design guidelines, Apple HIG, and accessibility standards.