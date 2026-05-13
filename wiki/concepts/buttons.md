# Buttons in Material Design 3

## Summary
Material Design 3 provides a comprehensive set of button types and styles to facilitate user actions and interactions. The button system emphasizes clarity, accessibility, and appropriate visual hierarchy to guide users toward desired actions while maintaining design consistency.

## Button Types
- **Text Button**: Minimal visual emphasis with text label only, used for less prominent actions
- **Outlined Button**: Text label with thin border outline, medium visual emphasis for secondary actions
- **Contained Button**: Text label with filled background container, high visual emphasis for primary actions
- **Floating Action Button (FAB)**: Circular button that floats above UI content, represents primary action
- **Icon Button**: Button containing only an icon, used where iconography sufficiently communicates function

## Button Properties
- **States**: Enabled, Hover, Focus, Pressed, Disabled, Dragged
- **Dimensions**: Consistent 36dp height for most button types, flexible width
- **Typography**: Button label style from type scale, Medium (500) font weight, 0.5em letter spacing

## Usage Guidelines
- Use contained buttons for primary actions
- Use outlined buttons for secondary actions
- Use text buttons for tertiary or less prominent actions
- Reserve FAB for the single most important action on a screen
- Follow platform conventions while maintaining brand consistency
- Ensure accessibility: minimum 48x48dp touch target, sufficient contrast, clear focus indicators

## Applications
- Primary calls-to-action (contained buttons)
- Secondary actions in forms or dialogs (outlined buttons)
- Tertiary or less prominent actions (text buttons)
- Toolbars, app bars, and supplementary actions (icon buttons)
- Primary screen actions (Floating Action Button)

## See Also
- [Material Design Overview](./sources/material-design-overview.md)
- [Color Theory](./concepts/color-theory.md)
- [Typography](./concepts/typography.md)
- [Layout & Spacing](./concepts/layout.md)
- [Cards](./concepts/cards.md)
- [Interaction Design Foundation: Button Design](./ixdf/ux-design.md)
- [NN/g: Click Patterns](./nn-g/README.md)

## Sources
- [Buttons in Material Design 3](./raw/material-design/components/buttons.md)
- [Material Design 3 Buttons Specification](https://m3.material.io/components/buttons/overview)