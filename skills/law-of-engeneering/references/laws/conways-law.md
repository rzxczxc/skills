# Conway's Law

> Source: https://lawsofsoftwareengineering.com/laws/conways-law/
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



## Origins

**Melvin Conway** introduced the idea in his 1967 paper "How Do Committees Invent?" After Harvard Business Review rejected it for lacking formal proof, Datamation published it in 1968.

Fred Brooks later named it "Conway's Law" in *The Mythical Man-Month*, which established the concept as foundational in software engineering.



## The Spotify Model

The Spotify Model organizes teams around features rather than technologies. Cross-functional **Squads** (6-12 people) own end-to-end features, grouped into **Tribes** by business area. **Chapters** and **Guilds** provide skill-sharing across squads. It works when it solves real coordination problems, but fails when copied blindly.



## Related Laws

- Brooks Law
- Galls Law
- Law of Leaky Abstractions
- Hyrums Law


## Further Reading

- [How Do Committees Invent?](https://www.melconway.com/Home/Committees_Paper.html) — Melvin Conway's original 1968 paper
- [Conway's Law](https://martinfowler.com/bliki/ConwaysLaw.html) — Martin Fowler's explanation of Conway's Law
- [Spotify Engineering Culture](https://engineering.atspotify.com/2014/3/spotify-engineering-culture-part-1) — The original Spotify Model blog post
- [Team Topologies](https://amzn.to/4jgRZ6V) — Modern application of Conway's Law to organizational design

---

Citation: "Conway's Law" from *Laws of Software Engineering* by Dr. Milan Milanović
Canonical URL: https://lawsofsoftwareengineering.com/laws/conways-law/
Book: "Laws of Software Engineering" (ISBN 978-969-9893-68-1) — https://lawsofsoftwareengineering.com/book/
© 2026 Dr. Milan Milanović. Attribution required.
