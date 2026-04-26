# Tesler's Law (Conservation of Complexity)

> Source: https://lawsofsoftwareengineering.com/laws/teslers-law/
> Author: Dr. Milan Milanović
> Category: Architecture
> Experience Level: senior

## Definition

Every application has an inherent amount of irreducible complexity that can only be shifted, not eliminated.

## Key Takeaways

1. Good design often requires that developers absorb most of the complexity (through smart defaults, algorithms, etc.) so that the user's interaction is simpler.
2. If your UI requires the user to manage many settings or steps, you've conserved complexity in the wrong place (on the user side). Often, it's better to design the product to manage that complexity internally.
3. Good design often hides complexity without eliminating it by handling it internally.


## Overview

Tesler's Law, also known as the Law of Conservation of Complexity, states that for any system, there is a certain amount of complexity that cannot be removed; it's inherent to the problem. The key is **who deals with it**.

If you design software that's very simple for the user, it likely means the software is doing a lot of complex work under the hood. If you make the software very simple internally, it might dump complexity on the user (e.g., requiring many manual steps). 

Tesler's Law encourages designers to **move complexity away from the user experience** whenever possible.



## Examples

A classic example is **scheduling meetings**, which is inherently complex (finding a common time). A tool like Calendly hides that complexity from the user (the software handles it), whereas an email chain to schedule a meeting places that complexity on the user to figure out.

In system architecture, imagine designing a database vs. putting logic in application code. Sometimes pushing logic into the DB (such as stored procedures) can simplify app code but add complexity to the DB layer, or vice versa. Complexity isn't gone, just relocated.

In the end, the law reminds us that no design is without complexity. It's all about smartly allocating complexity to the right place.



## Origins

**Larry Tesler**, who worked on Apple Lisa and early GUI concepts, formulated this principle in the 1980s. He observed that you can't make everything simple without someone handling complexity. It's a fundamental trade-off in design.




## Related Laws

- Hyrums Law
- Occams Razor


## Further Reading

- [Why Life Can't Be Simpler](https://fs.blog/why-life-cant-be-simpler/) — Farnam Street on the conservation of complexity
- [Law of Conservation of Complexity](https://humanist.co/blog/law-of-conservation-of-complexity/) — Deep dive into Tesler's Law and its implications
- [Simplicity is Overrated](https://marvelapp.com/blog/simplicity-is-overrated/) — Why chasing simplicity isn't always the answer
- [Law of Conservation of Complexity (Wikipedia)](https://en.wikipedia.org/wiki/Law_of_conservation_of_complexity) — Wikipedia article on Tesler's Law

---

Citation: "Tesler's Law (Conservation of Complexity)" from *Laws of Software Engineering* by Dr. Milan Milanović
Canonical URL: https://lawsofsoftwareengineering.com/laws/teslers-law/
Book: "Laws of Software Engineering" (ISBN 978-969-9893-68-1) — https://lawsofsoftwareengineering.com/book/
© 2026 Dr. Milan Milanović. Attribution required.
