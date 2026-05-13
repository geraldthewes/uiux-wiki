# Buttons in Material Design 3

## Summary
Material Design 3 provides a comprehensive set of button types and styles to facilitate user actions and interactions. The button system emphasizes clarity, accessibility, and appropriate visual hierarchy to guide users toward desired actions while maintaining design consistency.

## Button Types

### Text Button
- Minimal visual emphasis with text label only
- Used for less prominent actions
- Ideal for inline actions or secondary options
- No container or elevation by default

### Outlined Button
- Text label with thin border outline
- Medium visual emphasis
- Suitable for actions that need more prominence than text buttons but less than contained
- Good for secondary actions in forms or dialogs

### Contained Button
- Text label with filled background container
- High visual emphasis
- Used for primary actions and important calls-to-action
- Default button type for most prominent actions

### Floating Action Button (FAB)
- Circular button that floats above UI content
- Represents the primary action in a screen
- Typically positioned at bottom right corner
- Available in regular, small, and large sizes

### Icon Button
- Button containing only an icon (no text label)
- Used for actions where iconography sufficiently communicates function
- Common in toolbars, app bars, and as supplementary actions
- Accessible with proper aria-label or content description

## Button Properties

### States
- **Enabled**: Normal interactive state
- **Hover**: Visual feedback when pointer is over button (web/desktop)
- **Focus**: Visual indicator when button receives keyboard focus
- **Pressed**: Visual feedback during activation
- **Disabled**: Non-interactive state with reduced opacity
- **Dragged**: State during drag operations (for specific button types)

### Dimensions
- Height: Consistent 36dp for most button types
- Width: Flexible based on content with minimum and maximum constraints
- Padding: Horizontal padding adjusts to accommodate text length
- Icon size: 24dp for most buttons, 20dp for icon buttons

### Typography
- Label text uses Button label style from type scale
- Font weight: Medium (500) for emphasized hierarchy
- Text transformation: None (preserves original casing)
- Letter spacing: 0.5em for improved readability

## Usage Guidelines

### Action Prominence
- Use contained buttons for primary actions
- Use outlined buttons for secondary actions
- Use text buttons for tertiary or less prominent actions
- Reserve FAB for the single most important action on a screen

### Platform Conventions
- Android: FAB commonly used for primary screen action
- iOS: Less common use of FAB; prefer toolbar/button bar patterns
- Web: Follow platform conventions while maintaining brand consistency
- Desktop: Consider mouse hover states and keyboard navigation

### Accessibility
- Minimum touch target: 48x48dp (can exceed visual bounds)
- Sufficient contrast between text/icon and background (4.5:1 normal, 3:1 large)
- Clear focus indicators for keyboard navigation
- Accessible labels for icon-only buttons
- Avoid relying solely on color to convey meaning

## See Also
- [Color](./../foundations/color.md) - How button colors are determined
- [Typography](./../foundations/typography.md) - Button label styling
- [Layout](./../foundations/layout.md) - Button placement in layouts
- [Components/Cards](../cards.md) - Buttons in card components
- [NN/g: Click Patterns](../nn-g/README.md) - General button usability principles
- [Interaction Design Foundation: Button Design](../ixdf/README.md) - Additional button resources

## Tags
#material-design #buttons #components #ui-elements #accessibility

## References
- Material Design 3 Buttons: https://m3.material.io/components/buttons/overview
- Button Types: https://m3.material.io/components/buttons/specs
- Button States: https://m3.material.io/components/buttons/states
- Accessibility: https://m3.material.io/components/buttons/accessibility