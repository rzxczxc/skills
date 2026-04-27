# Inversion

> Author: Dr. Milan Milanović
> Category: Decisions
> Experience Level: mid

## Definition

Solving a problem by considering the opposite outcome and working backward from it.

## Key Takeaways

1. For any goal, also ask the inverted question. If the goal is “deliver the project on time,” we should think about “what would make us miss the deadline?” Making a list of those factors (scope creep, underestimating tasks, etc.) can help us achieve those goals and escape issues.
2. Use techniques like pre-mortems. Our project failed, and we tried to determine what could have caused it. This critical thinking can show risks that optimistic planning overlooks.
3. In design and testing, we can account for edge cases and use cases of your system. For example, how could a malicious user break this API? Inverting in this way leads to better solutions (e.g., adding validation, rate limiting, etc., once you understand how things break).

## Overview

The core idea is that specific insights become clear when you look at a problem from the opposite angle. In software engineering, instead of designing only for the best case, you deliberately design for the worst case: What if the database goes down? What if latency spikes?

By thinking of how things can fail, you add features like circuit breakers, retries, or failover strategies. Inversion pairs well with First-Principles Thinking and is a form of defensive design that leads to robust outcomes by avoiding possible problems.

## Examples

**Netflix's Chaos Monkey** is a prime example. Usually, engineers try to keep systems running. Chaos Monkey does the opposite: it randomly terminates servers in production to test resilience. This allowed Netflix to build fault-tolerant services that survive server failures.

**Test-Driven Development (TDD)** applies inversion by writing a failing test first. You define the failure before writing code to make it pass, forcing you to think about how code could fail before implementing it.

## Related Laws

- First Principles Thinking
- Murphys Law
- Premature Optimization

---

Citation: "Inversion" from *Laws of Software Engineering* by Dr. Milan Milanović
Book: "Laws of Software Engineering" (ISBN 978-969-9893-68-1)
© 2026 Dr. Milan Milanović. Attribution required.
