# SOLID Principles

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

---

Citation: "SOLID Principles" from *Laws of Software Engineering* by Dr. Milan Milanović
Book: "Laws of Software Engineering" (ISBN 978-969-9893-68-1)
© 2026 Dr. Milan Milanović. Attribution required.
