# Cards in Material Design 3

## Summary
Material Design 3 cards are versatile containers that display content and actions related to a single subject. They provide a flexible way to present information with consistent visual treatment, appropriate spacing, and clear interaction patterns while maintaining accessibility and responsiveness.

## Card Anatomy

### Container
- Surface with rounded corners (typically 8dp radius)
- Elevation to create depth and separation from background
- Flexible width and height based on content
- Minimum size constraints for usability

### Content Areas
- **Header**: Optional area for titles, avatars, or metadata
- **Media**: Optional area for images, videos, or other media
- **Primary Content**: Main textual or functional content
- **Actions**: Optional area for buttons, chips, or interactive elements

### Dividers
- Optional thin lines to separate sections within the card
- Used to distinguish between different types of content
- Typically 1dp height with appropriate opacity

## Card Types

### Outline Card
- Card with visible border and transparent background
- Less prominent than filled cards
- Useful for subtle grouping or when background needs to show through

### Filled Card
- Card with solid background color (typically surface variant)
- Most common card type
- Provides strong visual separation from background

### Elevated Card
- Card with increased elevation for more pronounced depth
- Used to draw attention or indicate temporary state
- Often used for dialogs or popovers

## Usage Guidelines

### Content Organization
- One subject per card for clarity and scannability
- Progressive disclosure: show essential information first
- Consistent alignment and spacing within card
- Appropriate typographic hierarchy for readability

### Interaction Patterns
- **Tap**: Entire card tappable for primary action
- **Swipe**: Horizontal swipe for dismissal or revelation
- **Drag**: Long press and drag for reordering (in lists)
- **Expand**: Tap to reveal more detailed content

### Accessibility
- Minimum touch target: 48x48dp for tappable cards
- Clear focus indicators for keyboard navigation
- Sufficient contrast between text and background (4.5:1 normal)
- Accessible labels for icon-only actions
- Avoid relying solely on color to convey meaning

### Responsive Behavior
- Cards reflow in grids based on available width
- Consistent card height for grid alignment (when appropriate)
- Horizontal scrolling for card collections on narrow screens
- Adaptive layouts for different screen sizes

## See Also
- [Color](./../foundations/color.md) - Card surface and accent colors
- [Typography](./../foundations/typography.md) - Text styling within cards
- [Layout](./../foundations/layout.md) - Card placement in layouts
- [Components/Buttons](../components/buttons.md) - Buttons in card actions
- [Patterns/Data Entry](../patterns/data-entry.md) - Forms within cards
- [NN/g: Card-Based Interfaces](../nn-g/README.md) - General card usability principles
- [Interaction Design Foundation: Card Design](../ixdf/README.md) - Additional card resources

## Tags
#material-design #cards #components #ui-elements #accessibility

## References
- Material Design 3 Cards: https://m3.material.io/components/cards/overview
- Card Types: https://m3.material.io/components/cards/specs
- Card States: https://m3.material.io/components/cards/states
- Accessibility: https://m3.material.io/components/cards/accessibility