# Hick’s Law

The time it takes to make a decision increases with the number and complexity of choices.

## Takeaways
- Minimize choices when response times are critical to decrease decision time.
- Break complex tasks into smaller steps in order to decrease cognitive load.
- Avoid overwhelming users by highlighting recommended options.
- Use progressive onboarding to minimize cognitive load for new users.
- Be careful not to simplify to the point of abstraction.

## Examples
### Google Homepage
Google keeps the decisions required to enter a keyword to a minimum by eliminating any additional content that could distract from the act of typing a keyword or require additional decision-making.

### Apple TV Remote
Apple TV remotes don’t require a substantial amount of working memory and therefore incurs much less cognitive load. By transferring complexity to the TV interface itself, information can be effectively organized and progressively disclosed within menus.

### Slack’s Progressive Onboarding
Instead of dropping users into a fully featured app after enduring a few onboarding slides, Slack uses a bot to engage users and prompt them to learn the messaging feature consequence-free. To prevent new users from feeling overwhelmed, Slack hides all features except for the messaging input. Once users have learned how to message via Slackbot, they are progressively introduced to additional features.

## Origins
Hick’s Law (or the Hick-Hyman Law) is named after a British and an American psychologist team of William Edmund Hick and Ray Hyman. In 1952, this pair set out to examine the relationship between the number of stimuli present and an individual’s reaction time to any given stimulus. As you would expect, the more stimuli to choose from, the longer it takes the user to make a decision on which one to interact with. Users bombarded with choices have to take time to interpret and decide, giving them work they don’t want.

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

[Source: Laws of UX](https://lawsofux.com/hicks-law/)