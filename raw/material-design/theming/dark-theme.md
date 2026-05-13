# Dark Theme in Material Design 3

## Summary
Material Design 3's dark theme provides a comfortable viewing experience in low-light conditions while maintaining accessibility, visual hierarchy, and brand expression. The system uses elevated surfaces with darker tones to create depth and distinction, ensuring readability and usability in dark environments.

## Dark Theme Foundations

### Surface Elevation
- Surfaces use darker tones based on elevation level
- Higher elevation = lighter surface (within dark theme constraints)
- Creates intuitive depth perception in dark environments
- Typically ranges from #121212 (base) to #1E1E1E (high elevation)

### Color Application
- Primary colors use lighter tints for better visibility on dark surfaces
- On colors (text/icons) use lighter shades for contrast
- Surface colors maintain sufficient contrast with content
- Accent colors retain vibrancy while ensuring accessibility

### Accessibility
- Minimum contrast ratios maintained: 4.5:1 for normal text, 3:1 for large text
- Surface variants provide accessible combinations
- System ensures text remains readable against all surface elevations

## Implementation Approach

### Tonal Palettes in Dark Theme
- Uses same tonal palettes as light theme
- Different tones selected for dark background
- Primary color typically uses tones 40-90 instead of 0-60
- Ensures sufficient contrast against dark surfaces

### Dynamic Dark Theme
- Can be system-driven (follows device setting)
- User-toggleable within app
- Scheduled based on time of day or ambient light
- Persists user preference across sessions

### Color Roles Adaptation
- **Primary**: Lighter tint for visibility on dark surfaces
- **Secondary/Tertiary**: Adjusted for dark background contrast
- **Surface**: Dark base with elevation-based variations
- **Background**: Usually same as surface or slightly lighter
- **Error**: Maintains visibility with appropriate lightness
- **On Colors**: Light variants for text and icons

## Design Considerations

### Visual Comfort
- Avoid pure black (#000000) for large areas
- Use dark gray (#121212) as base for reduced eye strain
- Consider ambient lighting conditions
- Provide option to switch between light and dark

### Brand Expression
- Adapt brand colors for dark theme viability
- Maintain brand recognition through consistent hues
- Consider how brand feels in dark vs. light contexts
- Test brand colors for accessibility in both themes

### Content Adaptation
- Images and media may need adjustment for dark backgrounds
- Consider adding subtle outlines or drop shadows
- Ensure videos and animations remain visible
- Provide dark-optimized assets when necessary

## See Also
- [Color](./../foundations/color.md) - Color system basics
- [Typography](./../foundations/typography.md) - Text styling in dark theme
- [Layout](./../foundations/layout.md) - Surface elevation and spacing
- [Components/Buttons](../components/buttons.md) - Button appearance in dark theme
- [Theming/Custom Themes](../theming/custom-themes.md) - Extended theming capabilities
- [NN/g: Visual Design Principles](../aesthetics/visual-design-principles.md) - General dark mode considerations
- [Interaction Design Foundation: Dark Mode](../ixdf/README.md) - Additional dark theme resources

## Tags
#material-design #dark-theme #theming #accessibility #color-system

## References
- Material Design 3 Dark Theme: https://m3.material.io/styles/color/dark-theme/overview
- Dark Theme Color Application: https://m3.material.io/styles/color/dark-theme/applying-color
- Accessibility in Dark Theme: https://m3.material.io/styles/color/dark-theme/accessibility
- Dynamic Theming: https://m3.material.io/styles/color/dynamic-color/overview