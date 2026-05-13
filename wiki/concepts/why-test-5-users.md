# Why You Only Need to Test with 5 Users

## Summary
Elaborate usability tests are a waste of resources. The best results come from testing no more than 5 users and running as many small tests as you can afford. This principle is based on the mathematics of usability testing showing diminishing returns after 5 users.

## Key Takeaways
- Testing with 5 users finds approximately 85% of usability problems
- Each additional user provides less new information (diminishing returns)
- Testing 5 users 3 times is better than testing 15 users once
- The approach enables a problem-fixing cycle: Test → Fix → Retest
- Provides representativeness by testing multiple users rather than relying on a single atypical user

## The Mathematics of Usability Testing
The number of usability problems found in a test with *n* users follows:
**N(1-(1-L)^n)**
Where:
- *N* = total number of usability problems in the design
- *L* = proportion of usability problems discovered while testing a single user (typically 31%)
- *n* = number of test users

This formula shows:
- 0 users: 0% of problems found
- 1 user: ~31% of problems found
- 2 users: ~50% of problems found
- 3 users: ~65% of problems found
- 4 users: ~76% of problems found
- 5 users: ~85% of problems found
- 15 users: ~99% of problems found

## Applications
- Conducting initial usability tests with 5 representative users
- Fixing discovered problems before retesting
- Running follow-up tests with 5 different users to validate fixes
- Iterative design approach for continuous improvement
- Testing multiple distinct user groups (3-4 users per group for 2 groups, 3 users per group for 3+ groups)

## Process
1. **First test (5 users)**: Finds ~85% of usability problems
2. **Redesign**: Fix discovered problems
3. **Second test (5 different users)**: Validates fixes, finds remaining ~15%, probes deeper
4. **Third test (if needed)**: Addresses remaining issues from second test

## See Also
- [10 Usability Heuristics](./concepts/10-usability-heuristics.md)
- [Empathy Mapping](./concepts/empathy-mapping.md)
- [Design Thinking](./workflows/design-thinking.md)
- [Jakob's Law](./concepts/jakobs-law.md)
- [Aesthetic-Usability Effect](./concepts/aesthetic-usability-effect.md)
- [Discount Usability Engineering](./concepts/discount-usability-engineering.md)

## Sources
- [Why You Only Need to Test with 5 Users](./raw/nn-g/why-test-5-users.md)