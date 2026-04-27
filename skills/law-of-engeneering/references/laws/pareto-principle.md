# Pareto Principle (80/20 Rule)

> Author: Dr. Milan Milanović
> Category: Decisions
> Experience Level: junior

## Definition

80% of the problems result from 20% of the causes.

## Key Takeaways

1. Identify the top 20% of factors that contribute to 80% of whatever you care about. This could be 20% of features that account for 80% of usage, or 20% of bugs that cause 80% of crashes. Prioritize your time and resources on those vital few for maximum impact.
2. Don’t spend the same effort on everything. If a particular area of code is rarely run, it probably doesn’t need the same optimization or attention as a hotspot.
3. It's not always exactly 80/20, but the idea is the same. Use profiling, analytics, and data gathering to empirically identify where the imbalances are.
4. On a personal level, as an engineer or manager, identify which tasks produce most of your value. It might be coding core features or coaching team members. 

## Overview

The Pareto Principle is more of an observation than a law, but the 80/20 pattern (or similar ratios like 90/10) appears frequently. 

In the domain of software engineering we say that, "80% of the time in a program is spent in 20% of the code." This insight is significant for optimization: instead of micro-optimizing everything, profile to identify the hot 20% and optimize that.

The principle influences product development too. Often, a few core features satisfy the majority of user needs. When planning an MVP, teams focus on that core set rather than trying to do everything. It is an essential check against equal prioritization: everything is not equally important. 

The Pareto Principle encourages strategic allocation of effort to maximize outcomes by investing where returns are highest.

## Examples

Microsoft found that around **20% of bugs in Windows and Office caused 80% of all crashes**, and a tiny 1% of bugs caused around 50% of errors. By focusing on the critical 1-20% of bugs, they dramatically improved stability. This is textbook Pareto: address the small set of high-impact issues to make most users happier quickly.

A software team analyzed usage analytics and discovered that out of 50 features, only 5-10 (10-20%) were used by 80%+ of users. This guided them to simplify the interface around core features and remove unused ones.

**Hot spots in code** follow the Pareto pattern. A small part of the codebase drives most defects, slowdowns, and "scary to touch" work. Track commits plus incidents to find them, then pay down debt where it compounds: add tests, simplify paths, reduce coupling, tighten interfaces.

## Related Laws

- Premature Optimization
- Kiss Principle
- Teslers Law

---

Citation: "Pareto Principle (80/20 Rule)" from *Laws of Software Engineering* by Dr. Milan Milanović
Book: "Laws of Software Engineering" (ISBN 978-969-9893-68-1)
© 2026 Dr. Milan Milanović. Attribution required.
