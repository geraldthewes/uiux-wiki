# Buttons in Material Design 3

## Summary
Material Design 3 provides a comprehensive set of button types and styles to facilitate user actions and interactions. The button system emphasizes clarity, accessibility, and appropriate visual hierarchy to guide users toward desired actions while maintaining design consistency.

## Key Takeaways
- **Text Button**: Minimal visual emphasis with text label only, used for less prominent actions
- **Outlined Button**: Text label with thin border outline, medium visual emphasis for secondary actions
- **Contained Button**: Text label with filled background container, high visual emphasis for primary actions
- **Floating Action Button (FAB)**: Circular button that floats above UI content, represents the primary action in a screen
- **Icon Button**: Button containing only an icon (no text label), used for actions where iconography sufficiently communicates function

- **States**: Enabled, Hover, Focus, Pressed, Disabled, Dragged
- **Dimensions**: Height: Consistent 36dp for most button types; Width: Flexible based on content
- **Typography**: Label text uses Button label style from type scale; Font weight: Medium (500); Letter spacing: 0.5em

## Origins/History
Material Design 3 was introduced by Google in 2021 as the next evolution of Material Design, focusing on flexibility, personalization, and cross-platform consistency.

## Applications
- **Action Prominence**: Use contained buttons for primary actions, outlined buttons for secondary actions, text buttons for tertiary or less prominent actions; Reserve FAB for the single most important action on a screen
- **Platform Conventions**: Follow platform conventions while maintaining brand consistency (Android, iOS, Web, Desktop)
- **Accessibility**: Minimum touch target: 48x48dp; Sufficient contrast between text/icon and background (4.5:1 normal, 3:1 large); Clear focus indicators for keyboard navigation; Accessible labels for icon-only buttons; Avoid relying solely on color to convey meaning

## See Also
- [Color](./../foundations/color.md) - How button colors are determined
- [Typography](./../foundations/typography.md) - Button label styling
- [Layout](./../foundations/layout.md) - Button placement in layouts
- [Components/Cards](../cards.md) - Buttons in card components
- [NN/g: Click Patterns](../nn-g/README.md) - General button usability principles
- [Interaction Design Foundation: Button Design](../ixdf/README.md) - Additional button resources

## Sources
- [Buttons in Material Design 3](./raw/material-design/components/buttons.md)