# Custom Theming in Material Design 3

## Summary
Material Design 3 provides extensive theming capabilities that allow designers and developers to express brand identity while maintaining usability and accessibility. The theming system is built around tonal palettes, component themes, and type scales that work together to create cohesive, customizable experiences.

## Theming Foundations

### Tonal Palette System
- Core innovation in Material Design 3 theming
- Generated from a single source color (seed)
- Produces 13 tonal variants (-25 to 100) for each color role
- Ensures perceptual uniformity and consistent contrast ratios
- Enables easy creation of light/dark themes from same seed

### Color Roles
- **Primary**: Brand expression color
- **Secondary**: Accent color for less prominent elements
- **Tertiary**: Additional accent for extended flexibility
- **Neutral**: Background and surface colors
- **Neutral Variant**: Alternate background/surface options
- **Error**: Indicates error states
- **On Colors**: Text and icon colors for each role

### Component Theming
- Components derive colors from tonal palettes
- Consistent application across component states
- Ability to override specific component colors
- Maintains accessibility through tonal relationships

## Customization Approaches

### Seed Color Customization
- Start with brand primary color as seed
- System generates complete tonal palettes
- Automatically derives secondary, tertiary, and neutral colors
- Ensures harmonic relationships and accessibility

### Selective Color Overrides
- Override specific color roles when needed
- Maintain tonal relationships for accessibility
- Consider impact on dependent components
- Test overrides in both light and dark themes

### Component-Specific Theming
- Customize individual component appearances
- Override colors, shapes, typography, or dimensions
- Apply themes to specific component instances
- Maintain consistency through design tokens

### Shape Customization
- Modify corner radii for components
- Apply consistent shape families across app
- Consider different shapes for different component types
- Maintain accessibility with sufficient touch targets

### Typography Customization
- Adjust type scale for brand expression
- Customize font family, weight, size, or spacing
- Maintain hierarchy and readability
- Consider language support and accessibility

## Implementation Guidelines

### Theme Definition
- Define seed colors for light and dark themes
- Specify optional overrides for specific roles
- Configure shape and typography preferences
- Generate theme objects for application consumption

### Application Integration
- Apply theme at app or activity level
- Support runtime theme switching
- Handle configuration changes (e.g., system dark mode)
- Ensure consistent theming across all screens

### Design Token Approach
- Extract colors, shapes, and typography as tokens
- Use tokens consistently in design and code
- Facilitates collaboration between designers and developers
- Enables easy theme updates and maintenance

### Accessibility Considerations
- Verify contrast ratios after customization
- Test with color blindness simulators
- Ensure touch targets remain accessible
- Validate screen reader compatibility

## Advanced Themings

### Dynamic Color
- Generate themes from user's wallpaper
- Personalize experience while maintaining brand integrity
- Available on Android 12+ and web platforms
- Option to combine with brand seed colors

### Themed Components
- Create custom components with theme awareness
- Ensure components respond to theme changes
- Maintain encapsulation and reusability
- Document theming API for custom components

### Theme Variants
- Create multiple themes for different contexts
- Seasonal, promotional, or event-based themes
- User-selectable theme options
- Consistent application across platform-specific implementations

## See Also
- [Color](./../foundations/color.md) - Color system basics
- [Typography](./../foundations/typography.md) - Type scale fundamentals
- [Layout](./../foundations/layout.md) - Shape and spacing relationships
- [Components/Buttons](../components/buttons.md) - Themed component examples
- [Theming/Dark Theme](../theming/dark-theme.md) - Dark theme specifics
- [NN/g: Visual Design Principles](../aesthetics/visual-design-principles.md) - General branding principles
- [Interaction Design Foundation: Design Systems](../ixdf/README.md) - Additional theming resources

## Tags
#material-design #theming #customization #design-system #branding

## References
- Material Design 3 Theming: https://m3.material.io/styles/theming/color
- Tonal Palettes: https://m3.material.io/styles/color/tonal-palettes/overview
- Custom Color: https://m3.material.io/styles/color/custom-color/overview
- Dynamic Color: https://m3.material.io/styles/color/dynamic-color/overview
- Shape: https://m3.material.io/styles/shape/overview
- Typography: https://m3.material.io/styles/typography/overview