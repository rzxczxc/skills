# Conway's Law

> Author: Dr. Milan Milanović
> Category: Teams
> Experience Level: senior

## Definition

Organizations design systems that mirror their own communication structure.

## Key Takeaways

1. The architecture of software systems often mirrors the organization's org chart or team structure.
2. If your company is organized in silos, you might end up with siloed software modules that don't communicate well, reflecting those barriers.
3. To achieve a desired software architecture (e.g., microservices), you might need to restructure teams accordingly, because teams build software aligned with their communication paths.
4. When starting a project, realize that how you split teams or departments will likely lead to software boundaries at the same places.

## Overview

Conway's Law states that **software systems reflect the communication structure of the organization that builds them**. A company with separate frontend, backend, and database departments will likely produce a three-tier architecture. Small, distributed teams tend to produce modular service architectures, while large, collocated teams tend to build monoliths.

To mitigate this, teams can use the **Inverse Conway Maneuver**: intentionally structuring the organization to match the desired software architecture.

## Examples

A company had separate departments for frontend, backend, and database. The software they built had a three-tier architecture, with each tier independently designed by its respective department. Integration between tiers was painful because the teams had misaligned goals.

Amazon famously organized "two-pizza teams", each owning a specific service. Conway's Law suggests that's why Amazon's architecture is service-oriented, with clear API contracts between services.

## The Spotify Model

The Spotify Model organizes teams around features rather than technologies. Cross-functional **Squads** (6-12 people) own end-to-end features, grouped into **Tribes** by business area. **Chapters** and **Guilds** provide skill-sharing across squads. It works when it solves real coordination problems, but fails when copied blindly.

## Related Laws

- Brooks Law
- Galls Law
- Law of Leaky Abstractions
- Hyrums Law

---

Citation: "Conway's Law" from *Laws of Software Engineering* by Dr. Milan Milanović
Book: "Laws of Software Engineering" (ISBN 978-969-9893-68-1)
© 2026 Dr. Milan Milanović. Attribution required.
