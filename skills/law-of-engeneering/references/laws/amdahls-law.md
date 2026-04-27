# Amdahl's Law

> Author: Dr. Milan Milanović
> Category: Scale
> Experience Level: senior

## Definition

The speedup from parallelization is limited by the fraction of work that cannot be parallelized.

## Key Takeaways

1. Sequential work sets the ceiling, and no amount of parallelism can overcome it.
2. Scaling exposes bottlenecks. More resources make limits visible, not disappear.
3. Fix before you scale: reduce sequential paths first. Parallelism comes second.
4. It applies to people, too. Decision bottlenecks can dominate at the team scale.

## Overview

As you add CPU cores, only the parallelizable fraction of your code speeds up. The sequential fraction remains unchanged and eventually dominates total execution time. If "s" is the sequential fraction, the maximum speedup with infinite parallel resources is 1/s. So if 10% is sequential, maximum speedup is 10x. If 50% is sequential, maximum speedup is only 2x.

This applies beyond hardware. If your system has a database that can't be parallelized, adding application servers hits a wall. The same holds for organizations: if one person or committee handles all architectural decisions, adding engineers increases coordination costs without increasing throughput.

## Examples

Adding application servers doesn't help if all requests hit a single database instance. One database becomes the limit.

Another example is breaking a monolith into microservices won't improve performance if all requests ultimately serialize through a shared dependency, such as an authentication or billing service. 

## Related Laws

- Gustafsons Law
- Metcalfes Law

---

Citation: "Amdahl's Law" from *Laws of Software Engineering* by Dr. Milan Milanović
Book: "Laws of Software Engineering" (ISBN 978-969-9893-68-1)
© 2026 Dr. Milan Milanović. Attribution required.
