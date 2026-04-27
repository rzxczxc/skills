# Goodhart's Law

> Author: Dr. Milan Milanović
> Category: Planning
> Experience Level: senior

## Definition

When a measure becomes a target, it ceases to be a good measure.

## Key Takeaways

1. If you set a particular metric as a goal (e.g., lines of code written, number of features closed), people will find ways to optimize for that metric.
2. Metrics are proxies for what you value (productivity, quality, etc.). Once they're targets, people meet the metric even if it undermines the original intent.
3. Metrics are useful for insight, but they must be used in context and balanced with qualitative judgment.
4. Combine multiple metrics to avoid a singular focus that can be gamed.

## Overview

Goodhart's Law comes from economics and is very relevant to software teams. For instance, a manager might set a target that "we must close 100 bug tickets this month." Developers, feeling pressure, might start closing tickets that are not truly resolved or splitting a single bug into multiple tickets to inflate numbers.

The metric (tickets closed) goes up, but software quality might not. Making the metric a goal distorts the process, so it loses its correlation with actual success. This is why experienced leaders use metrics as indicators rather than targets, and always consider the broader context.

## Examples

A software team was rewarded based on the lines of code written. Developers start writing verbose code and copying and pasting into multiple places (violating DRY) to increase the line count. The software becomes bloated while the metric looks great.

Another example: a QA team measured by the number of test cases executed favored running many easy tests rather than doing proper testing. They met objectives but missed critical bugs. 

Similarly, when teams focus on **code coverage percentage** as a primary target, developers write trivial unit tests that do not assert meaningful behavior, while necessary integration tests are skipped.

In today's world we see something similar with AI tokens consumed per engineer (a practice sometimes called **tokenmaxxing**), where more tokens is considered better, and even become one of the goals that people need to fulfill for their performance reviews.

## The Cobra Effect

A related concept is the Cobra Effect, where a solution to a problem makes it worse. During British colonial rule in India, a bounty on cobras led people to breed cobras for income. When the program was cancelled, breeders released their snakes, increasing the cobra population. Similarly, poorly designed metrics can create perverse incentives that worsen the original problem.

## Related Laws

- Dilbert Principle
- Parkinsons Law

---

Citation: "Goodhart's Law" from *Laws of Software Engineering* by Dr. Milan Milanović
Book: "Laws of Software Engineering" (ISBN 978-969-9893-68-1)
© 2026 Dr. Milan Milanović. Attribution required.
