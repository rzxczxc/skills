# Hanlon's Razor

> Author: Dr. Milan Milanović
> Category: Decisions
> Experience Level: junior

## Definition

Never attribute to malice that which is adequately explained by stupidity or carelessness.

## Key Takeaways

1. When something goes wrong, it's likely not malicious but rather an error or misunderstanding.
2. Don't jump to “the system is hacked” or “someone intentionally broke this.” First, consider simpler explanations (e.g., a configuration file was missed or a typographical error).
3. If a colleague's code is problematic, it's probably not sabotage. It may be due to being rushed or unaware of something. Try to approach with questions, not accusations.

## Overview

Hanlon's Razor advises against assuming bad faith when an outcome may be due to human error or ignorance. If a commit introduces a security hole, it's probably a mistake, not intentional sabotage. So one responds with help and fixes, not with blame.

This doesn't mean ignoring the possibility of malice when truly warranted (security does consider malicious actors). But for day-to-day development and operations, Hanlon's Razor keeps you grounded: the build failed likely due to a misconfiguration, not because someone deliberately broke it.

## Examples

A customer reports that your software "deleted all my data!" It's easy to panic and think a disgruntled employee planted a logic bomb. But Hanlon's Razor would have you first check for a mundane bug, perhaps a boundary condition in a delete function that wipes more than intended. Indeed, you find a bug where, when a user's account name was empty, the cleanup script deleted all records. No malice, just a bug.

In security, consider a sudden spike in server traffic. Before screaming "it's a DDoS attack!", check first if it's a misconfigured client spamming or a known pattern. Most weird behaviors in systems are due to mistakes, not malicious intent.

## Related Laws

- Occams Razor
- Goodharts Law
- Postels Law

---

Citation: "Hanlon's Razor" from *Laws of Software Engineering* by Dr. Milan Milanović
Book: "Laws of Software Engineering" (ISBN 978-969-9893-68-1)
© 2026 Dr. Milan Milanović. Attribution required.
