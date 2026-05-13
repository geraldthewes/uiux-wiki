# Fitts’s Law

## Summary
The time to acquire a target is a function of the distance to and size of the target. This principle is fundamental to user interface design, particularly for touch targets and interactive elements.

## Key Takeaways
- Touch targets should be large enough for accurate selection (44×44 pt for iOS, 48dp for Android)
- Ample spacing between targets prevents accidental activation
- Target placement in easily reachable areas improves usability (especially thumb zones on mobile)
- Mathematical formulation: MT = a + b * log2(D/W + 1) where MT is movement time, D is distance, W is width
- Screen edges and corners benefit from effectively infinite width/height, making them prime locations for important controls

## Origins/History
Formulated by psychologist Paul Fitts in 1954 while examining the human motor system. The law describes the speed-accuracy trade-off in human movement and has been widely adopted in UX/UI design to optimize interactive elements.

## Applications
Fitts's Law is applied in UX/UI design to:
- Determine appropriate sizing for touch targets and clickable elements
- Optimize placement of frequently used actions for efficiency
- Design effective navigation systems and menus
- Improve accessibility by ensuring targets are perceivable and operable
- Guide layout decisions for expert vs. novice user interactions

## See Also
- [Hick's Law](./hicks-law.md)
- [Jakob's Law](./jakobs-law.md)
- [Aesthetic-Usability Effect](./aesthetic-usability-effect.md)
- [Touch Target Guidelines](./topics/touch-targets.md)
- [Mobile Navigation Principles](./topics/mobile-navigation.md)

## Sources
- [Fitts's Law](./raw/laws-of-ux/fitts-law.md)