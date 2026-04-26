# The Map Is Not the Territory

> Source: https://lawsofsoftwareengineering.com/laws/map-is-not-the-territory/
> Author: Dr. Milan Milanović
> Category: Decisions
> Experience Level: mid

## Definition

Our representations of reality are not the same as reality itself.

## Key Takeaways

1. Design docs, UML diagrams, and architecture schematics are abstractions. Don't confuse the blueprint with the actual running software.
2. When implementing a system, expect that unforeseen factors will emerge that weren’t captured in the initial designs. Be prepared to adapt the plan as you discover new “terrain” during development and testing.
3. Models and designs are valuable for guiding development, but always be willing to question assumptions when evidence from the real system contradicts them.


## Overview

"The Map Is Not the Territory" is a mental model originating from general semantics. It encapsulates the idea that our perceptions or conceptual models of things are not the things themselves. 

In software, we constantly create "maps": requirements documents map user needs, architecture diagrams map how components should interact, and our mental understanding of a codebase is a personal map of how we think the code works.

These maps are useful and necessary. Without them, we couldn't plan or reason about complex systems. However, problems arise when we forget the map's limits.

 A typical example is overconfidence in initial design: a team designs a system on paper, but when coding begins, they discover modules cannot communicate due to latency issues not captured in their assumptions.
 
 As statistician George Box said, "All models are wrong, but some are useful."



## Examples

Consider designing a microservice system where Service A communicates with Services B and C via Kafka topics. The diagram assumed "the network is reliable" or "latency is negligible," but in cloud infrastructure reality, those assumptions fall apart. The team updates the design to include retry mechanisms or schema validation.

In performance modeling, an engineer might model a database handling 10,000 queries per second based on specs. In production, due to specific query patterns and data distribution, it only achieves 5,000 qps. The model didn't account for query plan edge cases. 

The Agile methodology itself embodies "map vs territory" thinking: instead of detailed 2-year plans, Agile uses short iterations with continuous feedback from reality to correct its maps.



## Origins

The phrase was popularized in "Science and Sanity" (1933) by Alfred Korzybski, a Polish-American scholar. Korzybski highlighted how our language and knowledge mislead us into believing our constructs actually represent reality.




## Related Laws

- Goodharts Law
- Galls Law
- Law of Leaky Abstractions


## Further Reading

- [Science and Sanity](https://www.holybooks.com/wp-content/uploads/Science-and-Sanity.pdf) — Alfred Korzybski's foundational work on general semantics
- [Steps to an Ecology of Mind](https://www.press.uchicago.edu/ucp/books/book/chicago/S/bo3620295.html) — Gregory Bateson's collected essays on anthropology, psychiatry, and epistemology

---

Citation: "The Map Is Not the Territory" from *Laws of Software Engineering* by Dr. Milan Milanović
Canonical URL: https://lawsofsoftwareengineering.com/laws/map-is-not-the-territory/
Book: "Laws of Software Engineering" (ISBN 978-969-9893-68-1) — https://lawsofsoftwareengineering.com/book/
© 2026 Dr. Milan Milanović. Attribution required.
