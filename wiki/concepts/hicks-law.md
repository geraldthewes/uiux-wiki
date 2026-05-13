# Hick's Law

## Summary
The time it takes to make a decision increases with the number and complexity of choices. This principle helps designers simplify interfaces by reducing cognitive load.

## Key Takeaways
- Minimize choices when response times are critical to decrease decision time
- Break complex tasks into smaller steps to reduce cognitive load
- Avoid overwhelming users by highlighting recommended options
- Use progressive onboarding to minimize cognitive load for new users
- Be careful not to simplify to the point of abstraction

## Origins/History
Hick's Law (or the Hick-Hyman Law) is named after British psychologist William Edmund Hick and American psychologist Ray Hyman. In 1952, they examined the relationship between the number of stimuli present and an individual's reaction time to any given stimulus.

## Mathematical Formula
RT = a + b * log2(n + 1)
Where:
- RT = Reaction time
- a, b = Constants determined empirically
- n = Number of equally probable alternatives

## Applications in UX/UI Design
### Menu Design
- Limit top-level navigation items (typically 5-9 based on Miller's Law)
- Use progressive disclosure for complex menus
- Highlight recommended or most common options

### Form Design
- Break long forms into multiple steps
- Group related fields together
- Use smart defaults to reduce decision-making

### Navigation
- Limit choices in navigation hierarchies
- Use search and filtering to reduce visible options
- Consider alphabetical or logical ordering when appropriate

### Onboarding
- Introduce features progressively
- Start with core functionality
- Reveal advanced features as users become proficient

## Related Concepts
- **Miller's Law**: The average person can only keep 7 (plus or minus 2) items in working memory
- **Cognitive Load**: Total mental effort required to process information
- **Decision Fatigue**: Deterioration of decisions after long session of decision making
- **Analysis Paralysis**: Over-analyzing or over-thinking a situation causing decision paralysis

## Design Implications
1. **Chunking**: Break information into meaningful groups
2. **Progressive Disclosure**: Show only essential options initially
3. **Visual Hierarchy**: Guide attention to most important choices
4. **Smart Defaults**: Pre-select optimal choices for most users
5. **Search & Filtering**: Help users reduce large sets to manageable chunks
6. **Pagination**: Break long lists into pages
7. **Recommendations**: Highlight suggested or popular options

## See Also
- [Laws of UX](./sources/laws-of-ux-overview.md)
- [Miller's Law](./concepts/millers-law.md)
- [Cognitive Load](./concepts/cognitive-load.md)
- [Progressive Disclosure](./concepts/progressive-disclosure.md)
- [Decision Making](./concepts/decision-making.md)

## Sources
- [Hick's Law](./raw/laws-of-ux/hicks-law.md)