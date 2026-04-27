# YAGNI (You Aren't Gonna Need It)

> Author: Dr. Milan Milanović
> Category: Design
> Experience Level: junior

## Definition

Don't add functionality until it is necessary.

## Key Takeaways

1. YAGNI is here to remind developers to focus on current tasks rather than implementing features that aren’t needed now.
2. Anticipating future needs often leads to over-engineering, and this adds complexity and maintenance issues.
3. YAGNI encourages iterative development. You implement minimal solutions and refine or extend them when needed.

## Overview

YAGNI captures a core philosophy of agile development: don't write code for features that haven't been requested or aren't immediately needed. 

If you're implementing Module A and think "in the future we might need Module B to do X, so I'll code some hooks for that now," YAGNI advises against it because that future feature may never come or may change drastically.

This principle directly fights over-engineering. To apply YAGNI successfully, teams rely on confidence in refactoring. You defer a feature only if you trust you can add it later at low cost. 

Agile methods provide that safety net via good test coverage, refactoring tools, and continuous integration. YAGNI pushes the problem of complexity to when it's actually needed.

## Examples

You're building a feature with specific behavior. You think "maybe in the future someone will want to toggle this on/off, so I'll add a configuration flag now." YAGNI challenges that. Unless there's a current requirement for configurability, implement only expected behavior, nothing more.

You're working on a library function that currently does one thing. You realize it might be useful more generally, so you might add parameters or abstraction tiers. YAGNI says implement it for the original task.

Your app needs JSON export? Implement simple JSON, not a full serialization library supporting XML, YAML, etc. 

Teams that adopt YAGNI are often comfortable refactoring because they trust that when the feature set grows, they'll have more information about real use cases, leading to better abstractions.

## Related Laws

- Kiss Principle
- Dry Principle
- Premature Optimization

---

Citation: "YAGNI (You Aren't Gonna Need It)" from *Laws of Software Engineering* by Dr. Milan Milanović
Book: "Laws of Software Engineering" (ISBN 978-969-9893-68-1)
© 2026 Dr. Milan Milanović. Attribution required.
