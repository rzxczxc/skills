# The Ninety-Ninety Rule

> Source: https://lawsofsoftwareengineering.com/laws/ninety-ninety-rule/
> Author: Dr. Milan Milanović
> Category: Planning
> Experience Level: mid

## Definition

The first 90% of the code accounts for the first 90% of development time; the remaining 10% accounts for the other 90%.

## Key Takeaways

1. The final parts of a project (polishing, edge cases, integration, bug fixes) often take far more effort than anticipated, often as much as the initial development.
2. What looks like the “finishing touches” involves many tricky problems and unknowns.
3. Reaching a “mostly done” state can create optimism, but the rule warns that “almost done” often means only halfway in terms of time.


## Overview

This rule quantifies the extent to which projects get stuck in the final phase. Often, teams make good progress at the start, building core functionality, which leads to optimism. Then integration, corner cases, performance tuning, and bug fixing consume an unexpectedly large amount of time, often equal to or greater than what has already been spent.

In practical terms, this rule advises that the last bit of a project is not a small bit. You should plan for a significant effort in finishing, polishing, and delivering. 

It is also related to Hofstadter's Law, as it is another way our estimates fall short. We do not realize how hard that last leg is.



## Examples

A team develops a new app. In three months, the core features are done, and they hit "90% of the functionality." Everyone expects to ship in one more month. Instead, integration testing reveals that multiple modules do not talk correctly, specific edge inputs crash the app, memory usage is too high. That final "10%" takes another three months.

When implementing a new website, you get a basic version up quickly (login, basic pages). The last bits: cross-browser fixes, responsive design adjustments, accessibility improvements, writing tests, and performance improvements seem like 10% of the work, but they take as much time as the main coding.

The rule is an important reminder: **Do not celebrate too early!**



## Origins

Credited to Tom Cargill of Bell Labs, and popularized by Jon Bentley's September 1985 "Bumper-Sticker Computer Science" column in Communications of the ACM. It was originally called the "Rule of Credibility", a name which did not stick.

It became popular in programming circles and is frequently referenced in discussions of why software is usually delivered late or why "90% done" claims can be misleading.



## The 180% Problem

The humor of this rule lies in the math: 90% + 90% = 180% of the originally estimated time. This is not a bug in the joke but a feature. It captures how badly we underestimate the tail end of projects. 

As developers say, "We are 90% done... and the other 90% is still to go."



## Related Laws

- Hofstadters Law
- Parkinsons Law
- Pareto Principle


## Further Reading

- [Programming Pearls - Bumper Sticker Computer Science](https://moss.cs.iit.edu/cs100/Bentley_BumperSticker.pdf) — Jon Bentley's original column where the rule was popularized
- [Programming Pearls (Book)](https://amzn.to/49bLHkn) — Jon Bentley's classic book on programming wisdom and techniques
- [Ninety-Ninety Rule - Wikipedia](https://en.wikipedia.org/wiki/Ninety%E2%80%93ninety_rule) — Overview of the rule and its origins at Bell Labs
- [Identifying and Mitigating the Ninety-Ninety Rule in Software Development](https://dev.to/ben/identifying-and-mitigating-the-ninety-ninety-rule-in-software-development-4ap3) — Practical strategies for recognizing and countering the ninety-ninety trap

---

Citation: "The Ninety-Ninety Rule" from *Laws of Software Engineering* by Dr. Milan Milanović
Canonical URL: https://lawsofsoftwareengineering.com/laws/ninety-ninety-rule/
Book: "Laws of Software Engineering" (ISBN 978-969-9893-68-1) — https://lawsofsoftwareengineering.com/book/
© 2026 Dr. Milan Milanović. Attribution required.
