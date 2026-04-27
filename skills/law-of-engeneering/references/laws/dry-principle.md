# DRY (Don't Repeat Yourself)

> Author: Dr. Milan Milanović
> Category: Design
> Experience Level: junior

## Definition

Every piece of knowledge must have a single, unambiguous, authoritative representation.

## Key Takeaways

1. The DRY principle is about avoiding duplication of knowledge in code. If the same idea or logic is in multiple places, it's a signal to refactor.
2. When requirements change, you should update logic in only one place. Repeated code increases the risk of inconsistencies and bugs (you might fix a bug in one copy and forget about the others).
3. Be careful to apply DRY wisely. It’s about knowledge repetition, not just duplication. Sometimes two pieces of code look alike but do different jobs; merging them could over-complicate things.

## Overview

The idea of DRY is simple: each fact or piece of logic in your system should be expressed once and only once. If you find the same code, formula, or rule in multiple modules, you're violating DRY. Such repetition creates hidden maintenance cost. When the business rule changes, you must hunt down every duplicate instance.

By following DRY, developers strive for a single, unique implementation of any given behavior. This often means abstracting common code into a function or class, or consolidating configuration into a single file. 

DRY also applies to database schemas, tests, and documentation. 

However, remember that DRY is about duplicated intent, not just similar-looking code. Two pieces of code can look identical but serve different purposes in an application.

## Examples

An application has a database connection URL in five different source files. If the database host changes, you'd have to edit all five places. The DRY approach keeps that URL in a single configuration variable that all modules read.

If two parts of an app both format dates the same way, create a single `formatDate()` utility function and call it from both places. Now if the date format needs to change, there's precisely one function to modify. 

Large codebases benefit from DRY through shared libraries. If multiple applications need the same security logic, create a shared library instead of copying code across applications.

## Related Laws

- Solid Principles
- Law of Demeter

---

Citation: "DRY (Don't Repeat Yourself)" from *Laws of Software Engineering* by Dr. Milan Milanović
Book: "Laws of Software Engineering" (ISBN 978-969-9893-68-1)
© 2026 Dr. Milan Milanović. Attribution required.
