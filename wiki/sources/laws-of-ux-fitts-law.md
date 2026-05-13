# Laws of UX: Fitts's Law

## Summary
The time to acquire a target is a function of the distance to and size of the target. This principle predicts how long it takes users to reach a target based on its distance and size.

## Key Takeaways
- Touch targets should be large enough for users to accurately select them
- Touch targets should have ample spacing between them to prevent accidental activation
- Touch targets should be placed in easily reachable areas of an interface
- The original formulation: MT = a + b * log2(D/W + 1) where MT is movement time, D is distance to target, and W is target width

## Origins/History
In 1954, psychologist Paul Fitts examined the human motor system and showed that movement time to a target depends on distance yet relates inversely to size. His law explains the speed-accuracy trade-off: fast movements and small targets result in greater error rates.

## Applications in UX/UI Design
### Touch Targets
- Minimum recommended size: 44×44 pt for iOS, 48dp for Android
- Adequate spacing between targets to prevent accidental activation
- Placement in easily reachable areas (especially thumb zones on mobile)

### Menu Design
- Larger, closer targets for frequently used actions
- Consider Fitts's Law when designing radial/pie menus
- Screen edges and corners benefit from effectively infinite width/height

### Navigation
- Global navigation should be easily accessible
- Consider placement of primary actions in thumb-reachable zones
- Use of accelerator keys for expert users

## See Also
- [Laws of UX Overview](./sources/laws-of-ux-overview.md)
- [Hick's Law](./concepts/hicks-law.md)
- [Touch Target Size](./concepts/touch-target-size.md)
- [Fitts's Law (NN/g)](https://www.nngroup.com/articles/fitts-law/)
- [Interaction Design Foundation: Fitts's Law](https://www.interaction-design.org/literature/article/fitts-s-law-the-importance-of-size-and-distance-in-ui-design)

## Sources
- [Fitts's Law](./raw/laws-of-ux/fitts-law.md)