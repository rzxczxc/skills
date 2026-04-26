# Gustafson's Law

> Source: https://lawsofsoftwareengineering.com/laws/gustafsons-law/
> Author: Dr. Milan Milanović
> Category: Scale
> Experience Level: senior

## Definition

It is possible to achieve significant speedup in parallel processing by increasing the problem size.

## Key Takeaways

1. As computing resources grow, you can compute more problems in a given time, rather than solving the same issues faster.
2. It opposes the pessimism of Amdahl's Law by assuming the size of the problem to be solved will increase proportionally with computing power, so that parallel processors remain busy.
3. Practically, Gustafson’s Law promotes the use of more resources in computation to achieve more in terms of the scope of tasks, rather than obtaining diminishing returns.
4. “The law,” it says, “teaches that software and algorithms should be designed to ‘scale out.’ That means that as available processor cores or machines increase, the amount of work that can be done can be scaled up accordingly.”


## Overview

Gustafson's Law is a principle in parallel computing that offers an optimistic view of scalability. Where Amdahl's Law assumes a fixed problem size and concludes that speedup is limited by serial work, Gustafson's Law changes the perspective.

It observes that when more processors are available, developers tend to increase the problem size to use that extra power. If you have a cluster twice as powerful, you might process twice as much data in the same time. 

The parallel portion of work grows with N processors while the serial portion remains about the same, leading to "scaled speedup" that can be almost linear. 

Gustafson's insight is that developers naturally use more computing power by asking bigger questions.



## Examples

In high-performance computing, climate modeling or molecular simulations routinely increase model resolution when more processors are available. A weather simulation on 1000 CPUs won't just finish 1000x faster; instead, they run a far more detailed global model in the same time, yielding a better forecast.

In big data processing, if analyzing 1 million records takes an hour on one machine, a 10-machine cluster might analyze 10 million records in an hour instead of finishing in 6 minutes. 

Modern distributed systems like MapReduce and Spark encourage splitting datasets into more partitions as nodes increase, keeping all processors busy.



## Origins

Gustafson's Law was formulated by computer scientist John L. Gustafson (with Edwin Barsis) in 1988, in a paper titled "Reevaluating Amdahl's Law." Gustafson was working at Sandia National Laboratories on high-performance computing.

At that time, Amdahl's 1967 result cast doubt on massively parallel supercomputers. Gustafson observed that this held only if workload was kept constant. His 1988 argument demonstrated that by increasing problem size, a 1024-processor system could achieve near-1024x speedup on suitably scaled tasks.




## Related Laws

- Amdahls Law
- Metcalfes Law


## Further Reading

- [Reevaluating Amdahl's Law](https://dl.acm.org/doi/10.1145/42411.42415) — John L. Gustafson's original 1988 paper
- [Gustafson's Law - Wikipedia](https://en.wikipedia.org/wiki/Gustafson%27s_law) — Overview of the law and its relationship to Amdahl's Law

---

Citation: "Gustafson's Law" from *Laws of Software Engineering* by Dr. Milan Milanović
Canonical URL: https://lawsofsoftwareengineering.com/laws/gustafsons-law/
Book: "Laws of Software Engineering" (ISBN 978-969-9893-68-1) — https://lawsofsoftwareengineering.com/book/
© 2026 Dr. Milan Milanović. Attribution required.
