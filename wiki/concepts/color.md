# Color in Material Design 3

## Summary
Material Design 3's color system is built around tonal palettes, providing a flexible foundation for creating expressive and accessible UIs. The system emphasizes the use of color to convey meaning, establish hierarchy, and create visual interest while maintaining accessibility.

## Core Principles

### Tonal Palettes
- Built from a single source color (the primary color)
- Each palette contains 13 tones ranging from -25 to 100
- Tones are perceptually uniform, ensuring consistent contrast ratios
- Enables dynamic theming and easy creation of light/dark variants

### Color Roles
- **Primary**: Key brand color, used for prominent UI elements
- **Secondary**: Accent color, less prominent than primary
- **Tertiary**: Complementary accent color for extended flexibility
- **Surface**: Background for UI elements
- **Background**: Overall page/screen background
- **Error**: Indicates errors or problematic states
- **On Colors**: Text and icon colors that appear on top of each role (e.g., on-primary, on-surface)

### Accessibility
- Minimum contrast ratios: 4.5:1 for normal text, 3:1 for large text
- System provides accessible color combinations by default
- Tools available to test and adjust contrast

## Applications

### Brand Expression
- Use primary color for brand recognition
- Secondary and tertiary for brand extensions
- Consistent application across touchpoints

### Information Hierarchy
- Guide user attention through color emphasis
- Distinguish between primary, secondary, and tertiary actions
- Use surface variants to create depth

### State Indication
- Communicate interactive states (hover, focus, pressed)
- Indicate enabled vs. disabled states
- Provide feedback through color changes

## Implementation Guidelines

### Dynamic Color
- System can generate palettes from user's wallpaper
- Enables personalization while maintaining design system integrity
- Available on Android 12+ and web through JavaScript APIs

### Dark Theme
- Uses elevated surfaces with darker tones
- Maintains accessibility in dark environments
- Reduces power consumption on OLED screens

### Content Prioritization
- Reserve vibrant colors for important actions
- Use muted tones for background and less important elements
- Ensure sufficient contrast for readability

## See Also
- [Typography](./typography.md) - How type works with color
- [Layout](./layout.md) - Structural foundation for color application
- [Components/Buttons](../components/buttons.md) - Practical color usage
- [Theming/Dark Theme](../theming/dark-theme.md) - Dark theme specifics
- [NN/g: Visual Design Principles](../aesthetics/visual-design-principles.md) - General color theory

## Tags
#material-design #color #design-system #accessibility #tonal-palettes

## References
- Material Design 3 Color System: https://m3.material.io/styles/color/overview
- Accessibility in Material Design: https://m3.material.io/styles/color/accessibility
- Dynamic Color: https://m3.material.io/styles/color/dynamic-color/overview