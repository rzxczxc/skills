# The Law of Leaky Abstractions

> Author: Dr. Milan Milanović
> Category: Architecture
> Experience Level: mid

## Definition

All non-trivial abstractions, to some degree, are leaky.

## Key Takeaways

1. No matter how well-designed, abstractions (libraries, frameworks, etc.) have edge cases that depend on internal details.
2. Developers should understand that using a high-level tool doesn't absolve them from knowing what's happening underneath, at least at a basic level.
3. "Leaky" means you might encounter performance issues, bugs, or behavior that force you to consider the underlying system (e.g., networking, OS) on which the abstraction sits.
4. When creating abstractions, strive to minimize leakage and document the cases in which it might break.

## Overview

This law observes that in complex systems, the abstractions we create, meant to hide complexity, *inevitably fail in some scenarios*, revealing the underlying complexity to the programmer.

For example, consider an ORM (object-relational mapper) that lets you treat database entries as objects. Most of the time it works, but occasionally you hit a case where performance is terrible and you have to think about the SQL queries being generated. The abstraction "leaks" details of the database. 

The law isn't saying abstractions are bad. They are essential. But it reminds us that **one must be prepared for when they break**.

## Examples

A good example is **memory management in high-level languages**. Languages like Java and Python abstract away manual memory allocation thanks to garbage collection. Yet leaks still happen (objects not being freed due to lingering references), or you encounter the abstraction's limits (such as GC pauses affecting performance). Suddenly, the developer needs to know how garbage collection works internally, and the abstraction of "infinite memory" has leaked.

Web developers often treat an HTTP request as something fast, abstracting away the network. However, when latency spikes or packets drop, the network's reality leaks into your application.

## All Models Are Wrong (George Box's Law)

George Box said, "*All models are wrong, but some are useful.*" Every abstraction you build, whether a class hierarchy, an API contract, or a data model, is a lie. It's basically **a simplified version of reality that ignores inconvenient details**. The question isn't whether your model is wrong. It's whether it's wrong in ways that matter.

Your database schema assumes users have one email address, until they don't. Your payment model treats refunds like reversed payments, until chargebacks arrive. Accept that every model will leak, and design for the leak, not against it.

## Related Laws

- Hyrums Law
- Galls Law

---

Citation: "The Law of Leaky Abstractions" from *Laws of Software Engineering* by Dr. Milan Milanović
Book: "Laws of Software Engineering" (ISBN 978-969-9893-68-1)
© 2026 Dr. Milan Milanović. Attribution required.
