# CAP Theorem

> Source: https://lawsofsoftwareengineering.com/laws/cap-theorem/
> Author: Dr. Milan Milanović
> Category: Architecture
> Experience Level: senior

## Definition

A distributed system can guarantee only two of: consistency, availability, and partition tolerance.

## Key Takeaways

1. A distributed system can only guarantee two out of three things at once: Consistency, Availability, and Partition Tolerance. When the network is healthy you can have all three, but the moment a partition happens, you have to give one up.
2. When a network split occurs, you face a choice: stay consistent (every node agrees, but some requests may fail) or stay available (every request gets an answer, but the data might be slightly out of date). You can't fully have both.
3. Real databases pick a side. MongoDB leans toward consistency, blocking writes during a partition so all replicas stay in sync. Cassandra leans toward availability, keeping the lights on and serving queries even if replicas briefly disagree.


## Overview

The CAP theorem states that a distributed system cannot simultaneously provide all three guarantees: **Consistency** (all nodes see the same data), **Availability** (every request receives a response), and **Partition Tolerance** (the system operates despite network failures).

Since network partitions are unavoidable in practice, systems must be partition-tolerant. This means choosing between consistency and availability when designing distributed architectures. The CAP theorem is a useful starting point, though it is a simplification that doesn't cover all aspects of the design space.



## Examples

The **Domain Name System (DNS)** is designed as AP (Available and Partition-tolerant). If some name servers are partitioned, they still reply (availability), even if their information might be slightly outdated until zones sync up.

**MongoDB** is a CP (Consistent and Partition-Tolerant) database, blocking writes during a partition so all replicas stay in sync. **Cassandra** is an AP (Available and Partition-Tolerant) database, serving queries even if replicas briefly disagree.



## Origins

Eric Brewer created the theorem in 2000 in the context of web services, and it was later formalized by Gilbert and Lynch in 2002. Brewer observed that designers of large-scale systems faced three concerns: keeping data consistent across nodes, keeping the service up, and handling network unreliability.

The formal proof showed that in a distributed system with shared data, you **must sacrifice either consistency or availability when a network partition occurs**. CAP became a guiding principle in the NoSQL movement and distributed database design in the 2000s.




## Related Laws

- Fallacies of Distributed Computing


## Further Reading

- [Brewer's CAP Theorem](https://www.infoq.com/articles/cap-twelve-years-later-how-the-rules-have-changed/) — Eric Brewer's reflection on CAP, twelve years later
- [CAP Twelve Years Later: How the 'Rules' Have Changed](https://sites.cs.ucsb.edu/~rich/class/cs293b-cloud/papers/brewer-cap.pdf) — Brewer's 2012 IEEE paper revisiting and refining the CAP theorem
- [Gilbert & Lynch 2002 Paper](https://groups.csail.mit.edu/tds/papers/Gilbert/Brewer2.pdf) — The formal proof of the CAP theorem
- [Designing Data-Intensive Applications](https://amzn.to/4pVAwU5) — Martin Kleppmann's comprehensive guide covering CAP and distributed systems
- [A Critique of the CAP Theorem](https://www.cl.cam.ac.uk/research/dtg/archived/files/publications/public/mk428/cap-critique.pdf) — Martin Kleppmann's 2015 paper arguing the theorem's definitions are ambiguous

---

Citation: "CAP Theorem" from *Laws of Software Engineering* by Dr. Milan Milanović
Canonical URL: https://lawsofsoftwareengineering.com/laws/cap-theorem/
Book: "Laws of Software Engineering" (ISBN 978-969-9893-68-1) — https://lawsofsoftwareengineering.com/book/
© 2026 Dr. Milan Milanović. Attribution required.
