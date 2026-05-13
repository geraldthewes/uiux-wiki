# Navigation in Material Design 3

## Summary
Material Design 3 provides a comprehensive set of navigation components and patterns to help users move through an application efficiently and intuitively. The navigation system emphasizes consistency, accessibility, and appropriate information hierarchy to support user goals and reduce cognitive load.

## Navigation Types

### App Bar
- **Top App Bar**: Contains navigation, title, and actions at the top of the screen
- **Center Aligned Top App Bar**: Title centered with navigation and actions on sides
- **Small Top App Bar**: Compact version for dense interfaces
- **Bottom App Bar**: Houses primary navigation and actions at the bottom (common on mobile)

### Navigation Drawer
- **Permanent Navigation Drawer**: Always visible, typically for larger screens
- **Temporary Navigation Drawer**: Slides in from left/right, hides content temporarily
- **Persistent Navigation Drawer**: Remains open on larger screens, collapses on smaller

### Navigation Rail
- Vertical navigation along the left or right edge
- Suitable for medium to large screens
- Can contain destinations, headers, and dividers

### Bottom Navigation
- Horizontal navigation at the bottom of the screen
- Typically 3-5 destinations
- Icon-only or icon-with-label variants

### Tabs
- Horizontal or vertical tabs for switching between views
- Scrollable tabs for more than visible destinations
- Icon-only, icon-with-label, or label-only variants

### Menu
- **Text Menu**: List of text options
- **Icon Menu**: List of icon options
- **Composite Menu**: Combination of text and icons
- **Dropdown Menu**: Appears below anchor point
- **Popup Menu**: Appears near anchor point

## Navigation Principles

### Consistency
- Maintain consistent navigation patterns across the app
- Use standard placement for navigation components
- Keep navigation behavior predictable

### Hierarchy
- Clearly distinguish between primary, secondary, and tertiary navigation
- Use visual emphasis to indicate current location
- Provide clear paths to parent and sibling destinations

### Accessibility
- Ensure all navigation elements are keyboard accessible
- Provide sufficient touch targets (minimum 48x48dp)
- Use clear labels and icons with accessible descriptions
- Maintain appropriate contrast for text and icons

### Responsiveness
- Adapt navigation patterns to different screen sizes
- Consider device posture and input methods
- Preserve navigation state when possible

## Implementation Guidelines

### App Bar
- Navigation icon (hamburger or arrow) on leading edge
- Title centered or aligned based on variant
- Action items on trailing edge
- Elevation to separate from content
- Responsive behavior: collapse, hide, or transform on scroll

### Navigation Drawer
- Width: 320dp for permanent, 280dp for temporary/persistent
- Contains: header (optional), destinations, dividers
- Supports nested navigation with subheaders
- Scrim behind temporary drawer to dim content

### Navigation Rail
- Width: 72dp (compact) or 240px (standard)
- Destinations: icon-only, icon-with-label, or label-only
- Selected state indicated by color change or indicator
- Can include header and footer sections

### Bottom Navigation
- Height: 56dp (standard) or 48dp (compact)
- 3-5 destinations recommended
- Selected state indicated by color change in icon and label
- Label visibility: always show, show on selected, or hide

### Tabs
- Height: 48dp (standard) or 40dp (compact)
- Scrollable horizontally when exceeding visible width
- Indicator below selected tab
- Label behavior: always show, show on selected, or hide

### Menu
- Appearance: anchored to UI element
- Elevation: appears above UI content
- Width: based on content with minimum and maximum constraints
- Dividers: optional between sections
- Icons: leading or trailing based on content type

## See Also
- [Color](./../foundations/color.md) - Navigation colors and theming
- [Typography](./../foundations/typography.md) - Label styling in navigation
- [Layout](./../foundations/layout.md) - Navigation placement in layouts
- [Components/Buttons](../components/buttons.md) - Buttons in app bars and menus
- [Components/Cards](../components/cards.md) - Cards in navigation drawers
- [NN/g: Navigation Patterns](../nn-g/README.md) - General navigation usability
- [Interaction Design Foundation: Navigation Design](../ixdf/README.md) - Additional navigation resources

## Tags
#material-design #navigation #components #ui-elements #accessibility

## References
- Material Design 3 Navigation: https://m3.material.io/components/app-bars-top/overview
- Navigation Drawer: https://m3.material.io/components/navigation-drawer/overview
- Navigation Rail: https://m3.material.io/components/navigation-rail/overview
- Bottom Navigation: https://m3.material.io/components/bottom-navigation/overview
- Tabs: https://m3.material.io/components/tabs/overview
- Menus: https://m3.material.io/components/menus/overview