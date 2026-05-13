# Error Handling in Material Design 3

## Summary
Material Design 3 provides guidelines for error handling that focus on clear communication, user empowerment, and minimal disruption. Effective error handling helps users understand what went wrong, why it happened, and how to recover, while maintaining trust in the system.

## Error Types

### System Errors
- Issues preventing the app from functioning correctly
- Examples: network failure, server error, permission denied
- Typically require user action or waiting for resolution

### User Errors
- Mistakes made by the user while interacting with the app
- Examples: invalid input, missing required fields, incorrect format
- Usually resolvable by correcting the input

### Edge Cases
- Uncommon or unexpected situations
- Examples: empty states, overflow content, unsupported file types
- May require special handling or user guidance

## Error Communication Principles

### Visibility
- Errors should be noticeable without being alarming
- Use color, icons, and typography to draw attention
- Avoid relying solely on color to convey meaning

### Clarity
- Use plain language that users understand
- Avoid technical jargon and error codes
- Be specific about what went wrong and where

### Actionability
- Provide clear steps for users to resolve the issue
- Offer shortcuts or direct links to relevant settings
- Suggest alternatives when the primary action isn't possible

### Consistency
- Use consistent patterns for similar types of errors
- Maintain uniform appearance and behavior across the app
- Follow platform conventions for error presentation

## Error Presentation

### Inline Errors
- Appear directly below or adjacent to the problematic field
- Ideal for form validation and input errors
- Disappear when the issue is resolved

### Toast Messages
- Temporary notifications that appear at the bottom of the screen
- Suitable for non-critical, transient feedback
- Auto-dismiss after a short duration or on user action

### Snackbars
- Similar to toasts but can include an action button
- Appear at the bottom of the screen
- Remain visible until dismissed or timeout

### Dialogs
- Modal interruptions that require user acknowledgment
- Used for critical errors or when immediate action is needed
- Should be used sparingly to avoid disruption

### Error Pages
- Full-screen views for significant issues preventing normal operation
- Examples: 404, 500, offline states
- Provide clear navigation paths to restore functionality

## Error States in Components

### Text Fields
- Red outline or background for error state
- Error message displayed below the field
- Icon (exclamation triangle) optionally added
- Helper text replaced by error message when invalid

### Buttons
- Visual indication when action cannot be completed
- May show loading state during processing
- Disabled state with tooltip explaining why
- Error state distinct from disabled state

### Icons
- Use error icons (exclamation triangle, error outline) appropriately
- Pair with text for clarity
- Consider colorblind-friendly palettes

### Lists and Collections
- Empty states with guidance when no items due to error
- Partial loading indicators with retry options
- Bulk error actions for multiple item failures

## Recovery Strategies

### Immediate Actions
- Provide undo options for reversible actions
- Offer retry buttons for transient failures
- Suggest corrections for input errors

### Preventive Measures
- Use constraints and defaults to prevent errors
- Validate input incrementally where appropriate
- Provide clear examples and format requirements

### User Support
- Link to help documentation or support channels
- Provide contact information for persistent issues
- Offer guided troubleshooting for complex problems

## Accessibility Considerations

### Screen Reader Support
- Error messages announced immediately when they appear
- Use live regions for dynamic error updates
- Associate errors with fields via aria-describedb
- Ensure error messages are concise and clear

### Color and Contrast
- Error colors meet minimum contrast ratios (4.5:1 for text)
- Supplement color with icons, patterns, or text
- Consider colorblind-friendly palettes

### Focus Management
- Move focus to error message or problematic field when appropriate
- Return focus to corrected field after resolution
- Avoid trapping users in error states

## See Also
- [Color](./../foundations/color.md) - Error colors and states
- [Typography](./../foundations/typography.md) - Error message styling
- [Layout](./../foundations/layout.md) - Placement of error messages
- [Components/Buttons](../components/buttons.md) - Buttons in error dialogs
- [Patterns/Data Entry](../patterns/data-entry.md) - Form validation errors
- [NN/g: Error Messages](../nn-g/README.md) - General error handling principles
- [Interaction Design Foundation: Error Prevention](../ixdf/README.md) - Additional error handling resources

## Tags
#material-design #error-handling #components #accessibility #user-feedback

## References
- Material Design 3 Error States: https://m3.material.io/components/text-fields/states#errors
- Snackbars and Toasts: https://m3.material.io/components/snackbars/overview
- Dialogs: https://m3.material.io/components/dialogs/overview
- Accessibility: https://m3.material.io/components/text-fields/accessibility#errors