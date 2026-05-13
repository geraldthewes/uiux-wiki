# Data Entry Patterns in Material Design 3

## Summary
Material Design 3 provides comprehensive patterns for data entry and form interactions, focusing on usability, accessibility, and clear communication. These patterns help users input, edit, and submit information efficiently while minimizing errors and cognitive load.

## Text Fields

### Filled Text Field
- Text input with background fill (typically surface variant)
- Most common text field style
- Clear visual indication of input area
- Supports helper text, error messages, and character counters

### Outlined Text Field
- Text input with border outline
- Less prominent than filled fields
- Good for forms with many fields to reduce visual noise
- Same functionality as filled text field

### Text Area
- Multi-line text input for longer content
- Available in filled and outlined variants
- Resizable or fixed height options
- Character counter support

### Password Field
- Specialized text field for secure input
- Obscured characters by default
- Toggle visibility button for user control
- Same styling options as regular text fields

## Selection Controls

### Radio Buttons
- For selecting one option from a set
- Vertical or horizontal layout
- Clear visual distinction between selected and unselected states
- Used when all options should be visible

### Checkboxes
- For selecting zero or more options from a set
- Independent selection of each option
- Vertical or horizontal layout
- Indeterminate state for partial selection

### Switches
- For toggling a single setting on/off
- Visual representation of state (typically with track and thumb)
- Immediate effect upon change
- Used for settings that take effect immediately

### Dropdown Menus
- For selecting one option from a list
- Compact when closed, expands to show options
- Supports search within long lists
- Can include icons or secondary text

## Date and Time Pickers

### Date Picker
- Calendar-based interface for date selection
- Single date, date range, or multiple dates
- Month/year navigation for quick selection
- Min/max date constraints

### Time Picker
- Analog or digital interface for time selection
- Hour and minute selection
- AM/PM or 24-hour format options
- Minute stepping (e.g., 5, 10, 15 minute intervals)

## Validation and Feedback

### Inline Validation
- Real-time feedback as user interacts with field
- Success, warning, and error states
- Clear, actionable error messages
- Avoid validating on every keystroke for performance

### Blur Validation
- Validation when field loses focus
- Good balance between immediate feedback and performance
- Particularly useful for server-side validation

### Submit Validation
- Validation upon form submission
- Collects all errors before preventing submission
- Presents errors in summary or inline

### Helper Text
- Persistent or conditional text below field
- Provides guidance, format examples, or constraints
- Changes to error message when validation fails
- Associated with field via aria-describedb

## Input Enhancements

### Prefix and Suffix
- Text or icon elements inside field boundaries
- Used for units, currency symbols, or common formats
- Clear visual distinction from input text
- Doesn't affect input value

### Autocomplete
- Suggests options as user types
- Reduces typing effort and spelling errors
- Keyboard accessible with arrow key navigation
- Can be local or remote data source

### Input Masks
- Formats input as user types (phone, credit card, date)
- Guides user toward correct format
- Can restrict input to valid characters
- Clear visual indication of expected format

## Accessibility Considerations

### Labeling
- Every input has associated label
- Label visible or accessible via aria-label/aria-labelledby
- Placeholder text is not a substitute for label
- Error messages associated via aria-describedb

### Touch Targets
- Minimum 48x48dp for interactive elements
- Adequate spacing between fields
- Consider thumb reach on mobile devices

### Keyboard Navigation
- Logical tab order following visual flow
- Visible focus indicators
- Enter key submits forms where appropriate
- Escape key cancels or closes dialogs

### Screen Reader Support
- Proper role and state announcements
- Live regions for dynamic error messages
- Descriptive labels for custom controls
- Announcements for required fields

## See Also
- [Color](./../foundations/color.md) - Field colors and states
- [Typography](./../foundations/typography.md) - Label and helper text styling
- [Layout](./../foundations/layout.md) - Form layout and spacing
- [Components/Buttons](../components/buttons.md) - Submit and action buttons
- [Patterns/Error Handling](../patterns/error-handling.md) - Form validation errors
- [NN/g: Form Design](../nn-g/README.md) - General form usability principles
- [Interaction Design Foundation: Form Design](../ixdf/README.md) - Additional form resources

## Tags
#material-design #forms #data-entry #components #accessibility

## References
- Material Design 3 Text Fields: https://m3.material.io/components/text-fields/overview
- Selection Controls: https://m3.material.io/components/selection-controls/overview
- Date and Time Pickers: https://m3.material.io/components/date-pickers/overview
- Validation and Error Handling: https://m3.material.io/components/text-fields/states#validation