# CAP Theorem

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

## Related Laws

- Fallacies of Distributed Computing

---

Citation: "CAP Theorem" from *Laws of Software Engineering* by Dr. Milan Milanović
Book: "Laws of Software Engineering" (ISBN 978-969-9893-68-1)
© 2026 Dr. Milan Milanović. Attribution required.
