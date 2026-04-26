# Fallacies of Distributed Computing

> Source: https://lawsofsoftwareengineering.com/laws/fallacies-of-distributed-computing/
> Author: Dr. Milan Milanović
> Category: Architecture
> Experience Level: senior

## Definition

A set of eight false assumptions that new distributed system designers often make.

## Key Takeaways

1. Networks drop messages, introduce delays, have finite throughput, and can be insecure. Properly built distributed systems must account for these with retries, timeouts, security measures, and dynamic discovery.
2. The fallacies often manifest in subtle bugs. Assuming latency is zero might lead to chatty remote calls that work fine locally but become painfully slow over a network.
3. Taking these fallacies into account leads to defensive design: using caches (bandwidth/latency aren't perfect), building redundancy (networks aren't reliable), and handling dynamic membership (topology changes).


## Overview

The Eight Fallacies serve as a checklist of what not to assume. They all spring from treating a distributed system like a local one. Developers might write code as if calling a remote service is just like calling a local function, ignoring latency and failure.

These mistaken assumptions lead to serious issues: unhandled errors when the network breaks, poor performance due to ignoring latency, security breaches from failing to authenticate remote calls. 

By calling them "fallacies," creators sought to instill the mindset that the network will fail and behave non-ideally, so your system must be designed to tolerate that.



## Examples

A developer building a distributed caching system assumes "network latency is zero." They design the cache to fetch data from a remote node for every lookup. In practice, it thrashes with high latency and poor performance.

A system assumes "the network is secure" and sends sensitive data unencrypted or doesn't validate inputs from other services. This leads to breaches if the network is compromised. Not planning for changing topology has broken systems when machines are added or removed unexpectedly.



## Origins

Credited primarily to **L. Peter Deutsch** (with others like James Gosling adding to the list) around 1994 at Sun Microsystems. Initially there were seven fallacies; an eighth ("the network is homogeneous") was added by Gosling later.

Deutsch observed that many engineers, especially those used to local computing, would subconsciously assume the network just works. Formalizing these assumptions as a list helped teams remember to address each one.




## Related Laws

- Cap Theorem
- Murphys Law


## Further Reading

- [Fallacies of Distributed Computing - Wikipedia](https://en.wikipedia.org/wiki/Fallacies_of_distributed_computing) — Wikipedia article on the eight fallacies
- [Fallacies of Distributed Computing Explained](https://www.rgoarchitects.com/Files/fallacies.pdf) — Arnon Rotem-Gal-Oz's detailed explanation of each fallacy
- [The Eight Fallacies of Distributed Computing](https://nighthacks.com/jag/res/Fallacies.html) — James Gosling's page on the fallacies
- [Designing Data-Intensive Applications](https://amzn.to/4pVAwU5) — Martin Kleppmann's book addressing all eight fallacies in depth
- [Foraging for the Fallacies of Distributed Computing](https://medium.com/baseds/foraging-for-the-fallacies-of-distributed-computing-part-1-1b35c3b85b53) — Vaidehi Joshi's accessible explanation of each fallacy

---

Citation: "Fallacies of Distributed Computing" from *Laws of Software Engineering* by Dr. Milan Milanović
Canonical URL: https://lawsofsoftwareengineering.com/laws/fallacies-of-distributed-computing/
Book: "Laws of Software Engineering" (ISBN 978-969-9893-68-1) — https://lawsofsoftwareengineering.com/book/
© 2026 Dr. Milan Milanović. Attribution required.
