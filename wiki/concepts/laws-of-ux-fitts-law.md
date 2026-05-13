# Fitts’s Law

The time to acquire a target is a function of the distance to and size of the target.

## Takeaways
- Touch targets should be large enough for users to accurately select them.
- Touch targets should have ample spacing between them.
- Touch targets should be placed in areas of an interface that allow them to be easily acquired.

## Origins
In 1954, psychologist Paul Fitts, examining the human motor system, showed that the time required to move to a target depends on the distance to it, yet relates inversely to its size. By his law, fast movements and small targets result in greater error rates, due to the speed-accuracy trade-off. Although multiple variants of Fitts’ law exist, all encompass this idea. Fitts’ law is widely applied in user experience (UX) and user interface (UI) design. For example, this law influenced the convention of making interactive buttons large (especially on finger-operated mobile devices)—smaller buttons are more difficult (and time-consuming) to click. Likewise, the distance between a user’s task/attention area and the task-related button should be kept as short as possible.

## Mathematical Formula
The original formulation of Fitts's Law is:
```
MT = a + b * log2(D/W + 1)
```
Where:
- MT = Movement time
- a, b = Constants determined experimentally
- D = Distance from starting point to target center
- W = Width of target measured along axis of motion

## Applications in UX/UI Design
### Touch Targets
- Minimum recommended size: 44×44 pt for iOS, 48dp for Android
- Adequate spacing between targets to prevent accidental activation
- Placement in easily reachable areas (especially for thumb zones on mobile)

### Menu Design
- Larger, closer targets for frequently used actions
- Consider Fitts's Law when designing radial/pie menus
- Screen edges and corners benefit from effectively infinite width/height

### Navigation
- Global navigation should be easily accessible
- Consider placement of primary actions in thumb-reachable zones
- Use of accelerator keys for expert users

## Related Resources
- [Fitts's Law and Its Applications in UX](https://www.nngroup.com/articles/fitts-law/) - Nielsen Norman Group
- [Fitts’ Law In The Touch Era](https://www.smashingmagazine.com/2012/06/fitts-law-touch-devices/) - Smashing Magazine
- [Fitts’s Law: The Importance of Size and Distance in UI Design](https://www.interaction-design.org/literature/article/fitts-s-law-the-importance-of-size-and-distance-in-ui-design) - Interaction Design Foundation
- [Design for Fingers, Touch, and People, Part 1](https://uxmatters.com/mt/archives/2009/06/design-for-fingers-touch-and-people.php) - Steven Hoober | UX Matters
- [The information capacity of the human motor system in controlling the amplitude of movement](https://www.semanticscholar.org/paper/The-information-capacity-of-the-human-motor-system-in-Fitts/5f5b6c8e8a3f3b3b3b3b3b3b3b3b3b3b3b3b3b3b) - Semantic Scholar

## Related Laws
- [Choice Overload](https://lawsofux.com/choice-overload/)
- [Doherty Threshold](https://lawsofux.com/doherty-threshold/)
- [Flow](https://lawsofux.com/flow/)

[Source: Laws of UX](https://lawsofux.com/fittss-law/)