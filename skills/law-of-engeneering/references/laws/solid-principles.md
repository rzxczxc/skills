# SOLID Principles

> Source: https://lawsofsoftwareengineering.com/laws/solid-principles/
> Author: Dr. Milan Milanović
> Category: Design
> Experience Level: mid

## Definition

Five main guidelines that enhance software design, making code more maintainable and scalable.

## Key Takeaways

1. Following SOLID leads to software that is easier to extend, test, and refactor without breaking existing functionality. Each principle addresses a different aspect of good OO design.
2. A class with a single responsibility (SRP) that depends on well-defined interfaces (ISP, DIP) and uses inheritance appropriately (LSP) and polymorphism for extensions (OCP) will likely be easy to maintain.
3. Changes to one part of the system won’t cascade into breakages elsewhere, because the code is loosely coupled and well-encapsulated.
4. SOLID does not guarantee a perfect design, but it provides proven guidelines for object-oriented programming.


## Overview

The SOLID principles are five high-level guidelines for object-oriented design: **Single Responsibility** (one concern per class), **Open/Closed** (open for extension, closed for modification), **Liskov Substitution** (subclasses must be substitutable for their parent), **Interface Segregation** (no forced dependency on unused interfaces), and **Dependency Inversion** (depend on abstractions, not concretions).

When applied together, these principles produce systems that are modular, extensible, and robust under change. Code becomes easier to test, refactor, and extend without breaking existing functionality.



## Examples

For the **Single Responsibility Principle**, consider a web application managing user accounts. An anti-SRP design might have a single `UserManager` class handling validation, database operations, sending emails, and logging. A better design separates these into `UserValidator`, `UserRepository`, `EmailService`, and a `UserRegistrationService` that orchestrates them. Each class has one focus, and if the email format changes, you only touch `EmailService`.

For the **Dependency Inversion Principle**, imagine a `NotificationService` that sends alerts. Without DIP, it directly uses `EmailSender` or `SMSSender`. With DIP, you define an `INotificationChannel` interface, and all senders implement it. The service depends only on the abstraction, making it easy to add new channels or swap in test doubles.



## Origins

The five SOLID principles emerged over the years and were collected and popularized by Robert C. Martin (Uncle Bob). The acronym SOLID was coined around 2004 by Michael Feathers, who noticed the initial letters spelled out a catchy word.

Uncle Bob described SRP, OCP, LSP, ISP, and DIP in various articles from the late 1990s and early 2000s, including his "Principles of Object-Oriented Design" papers and his 2002 book Agile Software Development: Principles, Patterns, and Practices. These principles drew from earlier thinkers: OCP from Bertrand Meyer (1988), LSP from Barbara Liskov (1987), ISP from work at Xerox PARC, and DIP and SRP were Martin's formulations inspired by layering and cohesion practices.



## When SOLID goes too far

It's possible to overapply the SOLID principles. Sometimes, too many small interfaces or too many abstract layers are overkill for a problem and create complexity, the so-called "AbstractFactoryFactory" problem. 

When used correctly, though, these principles are genuinely helpful in managing object-oriented system complexity, which is why they've become so popular to teach.



## Related Laws

- Law of Demeter
- Hyrums Law
- Law of Leaky Abstractions
- Dry Principle
- Kiss Principle
- Yagni


## Further Reading

- [Design Principles and Design Patterns](https://web.archive.org/web/20150906155800/http://www.objectmentor.com/resources/articles/Principles_and_Patterns.pdf) — Robert C. Martin's foundational paper on OO design principles
- [Agile Software Development: Principles, Patterns, and Practices](https://amzn.to/497oH7H) — Uncle Bob's comprehensive book introducing SOLID principles
- [Clean Architecture](https://amzn.to/4jeeN7k) — Robert C. Martin's guide to software architecture and design
- [SOLID - Wikipedia](https://en.wikipedia.org/wiki/SOLID) — Overview of all five principles with examples
- [Design Patterns: Elements of Reusable Object-Oriented Software](https://amzn.to/3LnM5o6) — The Gang of Four's classic on OO patterns that complement SOLID

---

Citation: "SOLID Principles" from *Laws of Software Engineering* by Dr. Milan Milanović
Canonical URL: https://lawsofsoftwareengineering.com/laws/solid-principles/
Book: "Laws of Software Engineering" (ISBN 978-969-9893-68-1) — https://lawsofsoftwareengineering.com/book/
© 2026 Dr. Milan Milanović. Attribution required.
