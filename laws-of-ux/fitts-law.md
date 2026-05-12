# Fitts's Law

The time to acquire a target is a function of the distance to and size of the target.

## Mathematical Formula
MT = a + b * log2(D/W + 1)
Where:
- MT = Movement time
- a, b = Constants determined experimentally
- D = Distance from starting point to target center
- W = Width of target measured along axis of motion

## UX Applications
- Larger, closer targets are easier and faster to acquire
- Critical for touch targets (minimum 44×44 pt for iOS, 48dp for Android)
- Explains why screen corners and edges are valuable real estate (infinite width/height)
- Menu bars at top of screen benefit from Fitts's Law
- Radial/pie menus leverage Fitts's Law effectively

## Design Implications
1. Make frequently used controls larger and closer
2. Place important UI elements at screen edges/corners
3. Ensure touch targets meet minimum size requirements
4. Consider using radial menus for expert users

[Source: Laws of UX](https://lawsofux.com/fittss-law/)