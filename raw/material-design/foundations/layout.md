# Layout in Material Design 3

## Summary
Material Design 3's layout system provides responsive foundations for arranging UI elements across different screen sizes and orientations. Built on an 8dp grid baseline, the system offers flexible layout templates, adaptive spacing, and responsive behavior to create consistent and usable interfaces.

## Grid System

### 8dp Baseline Grid
- All dimensions and spacing multiples of 8dp for visual harmony
- Ensures consistent alignment and proportional relationships
- Facilitates collaboration between designers and developers

### Column Grid
- Responsive column counts: 1 column (extra small), 2 columns (small), 3 columns (medium), 4 columns (large)
- Gutters and margins adjust based on screen width
- Maximum width constraints for optimal readability on large screens

### Layout Templates
- **List**: Single column for simple item lists
- **List with sidebar**: Primary content with secondary navigation or controls
- **Two pane**: Equal or weighted split for complementary views
- **Three pane**: Navigation, content, and details panels
- **Canvas**: Freeform layout for creative or dashboard interfaces

## Layout Principles

### Responsive Behavior
- Elements reflow based on available space
- Breakpoints defined at 600dp, 840dp, and 1200dp window widths
- Adaptive components that change appearance or function at different sizes

### Spatial Relationships
- Elevation creates depth and hierarchy (0-24dp range)
- Consistent padding and margin values for breathing room
- Alignment to grid ensures visual order and scanability

### Adaptive Design
- Consider device posture (handheld, tablet, desktop)
- Optimize for input methods (touch, mouse, keyboard, stylus)
- Leverage platform-specific conventions while maintaining brand consistency

## Implementation Guidelines

### Measurement Units
- Use dp (density-independent pixels) for consistent physical sizing
- Scale typography with sp (scale-independent pixels) for accessibility
- Convert designs to pixels based on device density at runtime

### Spacing System
- 4dp and 8dp increments for fine and coarse spacing
- Default padding: 16dp for mobile, 24dp for tablet/desktop
- Touch targets: minimum 48x48dp for comfortable interaction

### Component Alignment
- Baseline alignment for text elements
- Edge alignment for related groups
- Center alignment for promotional or emphasised content
- Consistent horizontal and vertical rhythms

## Applications

### Mobile Layouts
- Prioritize vertical scrolling with clear hierarchies
- Use bottom navigation for primary destinations
- Implement navigation rail for larger screens when applicable

### Tablet Layouts
- Utilize horizontal space with multiple panes
- Consider adaptive side navigation that collapses
- Leverage larger canvas for content creation and multitasking

### Desktop Layouts
- Implement responsive side navigation that expands
- Use grid layouts for data-intensive interfaces
- Consider window resizing behavior and multi-window support

## See Also
- [Color](./color.md) - Visual distinction through color
- [Typography](./typography.md) - Text placement and scaling
- [Components/Navigation](../components/navigation.md) - Layout-specific navigation patterns
- [NN/g: Information Architecture](../ixdf/information-architecture.md) - General layout principles
- [Interaction Design Foundation: Grid Systems](../ixdf/README.md) - Additional layout resources

## Tags
#material-design #layout #design-system #responsive #grid

## References
- Material Design 3 Layout: https://m3.material.io/styles/layout/overview
- Grid System Details: https://m3.material.io/styles/layout/baseline-grid
- Breakpoints and Margins: https://m3.material.io/styles/layout/responsive-layout-grid
- Elevation System: https://m3.material.io/styles/layout/elevation