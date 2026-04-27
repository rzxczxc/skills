# KISS (Keep It Simple, Stupid)

> Author: Dr. Milan Milanović
> Category: Design
> Experience Level: junior

## Definition

Designs and systems should be as simple as possible.

## Key Takeaways

1. KISS primarily refers to avoiding complexity in solution designs. A solution that satisfies the requirement and is simple in design is better than a complex one.
2. Code that is coded is easier and faster to understand and debug. It’s even easier to understand and fix if you’re your own future self. Smarter code may look impressive at first, but it often masks problems.
3. The code solution should be as simple as possible. Anything that adds complexity unnecessarily is counter to the KISS Principle.

## Overview

The KISS principle is a reminder that simplicity should be a key goal. If you can solve a problem with a 50-line script versus a complex 500-line solution, KISS favors the 50-line solution because each line of code has the potential to cause an error.

Why is simplicity so important? Software has to be understood by humans. A simple design is much easier to maintain: new team members can get up to speed faster, bugs are easier to localize, and modifications cause fewer ripple effects. 

The KISS principle encourages developers to resist "clever" code that does too much at once, and to avoid architecting solutions that address future problems at the cost of current complexity.

## Examples

A web application needs to generate reports. A KISS approach would use a simple script or existing library to query the database and output a CSV. A non-KISS approach would design a complete plug-in architecture "just in case" you need it more generically later. If requirements are small, the latter is overkill.

When writing a function to parse a file, a KISS implementation uses simple logic: open the file, read line by line, split fields, handle errors. A complex approach might implement a fully generic parser-combinator framework. Unless you truly need that generality, the simpler approach will be easier to get right and maintain.

Many experienced engineers advise: "First make it work, then make it right, then make it fast (if needed)."

## Related Laws

- Yagni
- Principle of Least Astonishment
- Galls Law

---

Citation: "KISS (Keep It Simple, Stupid)" from *Laws of Software Engineering* by Dr. Milan Milanović
Book: "Laws of Software Engineering" (ISBN 978-969-9893-68-1)
© 2026 Dr. Milan Milanović. Attribution required.
