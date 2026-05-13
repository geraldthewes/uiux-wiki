# Why You Only Need to Test with 5 Users

Jakob Nielsen
March 18, 2000

## Summary
Elaborate usability tests are a waste of resources. The best results come from testing no more than 5 users and running as many small tests as you can afford.

## Introduction
Some people think that usability is very costly and complex and that user tests should be reserved for the rare web design project with a huge budget and a lavish time schedule. Not true. Elaborate usability tests are a waste of resources. The best results come from testing no more than 5 users and running as many small tests as you can afford.

## The Mathematics of Usability Testing
In earlier research, Tom Landauer and I showed that the number of usability problems found in a usability test with *n* users is:

**N(1-(1-L)^n)**

Where:
- *N* = total number of usability problems in the design
- *L* = proportion of usability problems discovered while testing a single user (typically 31%)
- *n* = number of test users

Plotting the curve for *L* = 31% shows:
- 0 users: 0% of problems found
- 1 user: ~31% of problems found
- 2 users: ~50% of problems found
- 3 users: ~65% of problems found
- 4 users: ~76% of problems found
- 5 users: ~85% of problems found
- 15 users: ~99% of problems found

## Key Insights from the Curve
1. **Zero users give zero insights** - No testing means no learning
2. **First user provides biggest jump** - Going from 0 to 1 user gives ~31% insight
3. **Diminishing returns** - Each additional user provides less new information
4. **After 5 users, limited gain** - The curve flattens significantly after 5 users

## Iterative Design Approach
The curve shows we need ~15 users to find all problems, but testing 5 users 3 times is better than testing 15 users once because:

### Benefits of Multiple Small Tests
1. **Problem fixing cycle**: Test → Fix → Retest validates solutions
2. **Quality assurance**: Second test confirms fixes worked and finds remaining issues
3. **Deeper insights**: Later tests probe fundamental structure vs. surface problems
4. **Risk reduction**: Less chance of being misled by atypical user behavior
5. **Continuous improvement**: Ongoing refinement rather than one-time snapshot

### Process
1. **First test (5 users)**: Finds ~85% of usability problems
2. **Redesign**: Fix discovered problems
3. **Second test (5 different users)**: Validates fixes, finds remaining ~15%, probes deeper
4. **Third test (if needed)**: Addresses remaining issues from second test

## Why Not Test With a Single User?
Two main reasons to test more than one user:
1. **Representativeness risk**: Single user might be atypical or perform spurious actions
2. **Cost-benefit optimization**: Fixed study costs are better amortized across multiple users

Even 3 users provide diversity insight while keeping costs reasonable.

## When To Test More Users
Test additional users only for:
- **Several highly distinct user groups** (e.g., children vs. parents)
- **Sufficiently different behaviors** between categories

For multiple user groups:
- **2 groups**: 3-4 users from each category
- **3+ groups**: 3 users from each category (minimum 3 to capture intra-group diversity)

## Practical Guidelines
1. **Start with 5 users** for initial testing
2. **Fix discovered problems** before retesting
3. **Test again with 5 different users**
4. **Repeat as needed** based on resources and complexity
5. **Always use representative users** from your target audience

## Related NN/g Resources
- [How Many Test Users in a Usability Study?](https://www.nngroup.com/articles/how-many-test-users/)
- [Quantitative Studies (usability metrics)](https://www.nngroup.com/articles/quantitative-studies-how-many-users/): Test 20 Users
- [Card Sorting](https://www.nngroup.com/articles/card-sorting-how-many-users-to-test/): Test 15 Users

## See Also
- [10 Usability Heuristics](./10-usability-heuristics.md)
- [Empathy Mapping](./empathy-mapping.md)
- [Design Thinking 101](./design-thinking.md)
- [Jakob's Law](../laws-of-ux/jakobs-law.md)
- [Aesthetic-Usability Effect](../laws-of-ux/aesthetic-usability-effect.md)

[Source: Nielsen Norman Group](https://www.nngroup.com/articles/why-you-only-need-to-test-with-5-users/)