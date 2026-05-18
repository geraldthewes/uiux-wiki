# Color Selection for Applications

## Summary
Effective color selection for web applications involves creating limited, systematic palettes that ensure visual consistency, accessibility, and maintainability rather than using ad-hoc hex values. Professional teams follow structured processes to define core brand colors, build harmonious relationships, establish semantic meanings, and generate scalable shade systems.

## Key Takeaways
- **Limited palette approach**: 4-10 core base hues with systematic scales (50-150+ total tokens) works best
- **Core structure**: Primary (1), Secondary/Accent (1-2), Neutrals (gray family), Semantic (4-5: success, warning, error, info)
- **60-30-10 rule**: 60% neutrals, 30% secondary, 10% accent colors for balanced interfaces
- **Systematic generation**: Create 5-10 shades/tints per base color using HSL for better control
- **Accessibility first**: WCAG 2.2 AA minimum 4.5:1 contrast for normal text, 3:1 for large text
- **Documentation critical**: Define usage rules and implement as design tokens (Figma Variables + CSS custom properties)

## Selection Process
1. **Start with brand Primary** - Extract from brand guidelines, use for primary buttons, active navigation
2. **Choose 1-2 Secondary/Accent colors** - Apply color theory (complementary, analogous, triadic)
3. **Build strong Neutrals** - Cool/warm grays (8-10 shades), avoid pure black/white
4. **Define Semantic colors** - Error (red), Success (green), Warning (orange/yellow), Info (blue)
5. **Generate systematic scales** - Create lighter/darker versions preserving saturation (HSL preferred)
6. **Test accessibility** - Check contrast ratios in both light and dark modes
7. **Document usage rules** - Specify exact applications for each color/shade combination

## Applications
- Brand-aligned interface design
- Accessible color systems meeting WCAG standards
- Consistent UI component styling (buttons, forms, navigation)
- Dark mode implementation readiness
- Design token systems for developer-designer handoff
- Maintenance-friendly color management

## See Also
- [[../concepts/color-theory-basics|Color Theory Basics]]
- [[../concepts/color-palettes|Color Palettes]]
- [[../concepts/color-accessibility|Color Accessibility]]
- [[../concepts/color-psychology|Color Psychology]]
- [[../sources/color-color-selection-best-practices|Considerations to Select the Main Colors for an App]]
- [[../concepts/material-design-foundations-color|Material Design Color System]]

## Sources
- [[../../raw/color/color-selection-best-practices.md|Considerations to Select the Main Colors for an App]]
- [[../../raw/color/color-theory-basics.md|Color Theory Basics]]
- [[../../raw/color/color-palettes.md|Color Palettes]]
- [[../../raw/color/color-accessibility.md|Color Accessibility]]
- [[../../raw/color/color-psychology.md|Color Psychology]]

## Tags
#color #design-system #accessibility #ui-design #ux-design #color-palette #design-tokens