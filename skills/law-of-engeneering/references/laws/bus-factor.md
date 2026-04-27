# Bus Factor

> Author: Dr. Milan Milanović
> Category: Teams
> Experience Level: mid

## Definition

The minimum number of team members whose loss would put the project in serious trouble.

## Key Takeaways

1. A bus factor of 1 means one person holds critical knowledge; if they disappear, the project is essentially “doomed” or stalled. A higher bus factor (e.g., 5) means the project could lose any one of five specific people before stopping work.
2. It's basically a measure of knowledge distribution and risk. A high bus factor is good (knowledge is shared among many), while a low is bad (single points of failure in expertise).
3. Teams should work to increase their bus factor by sharing knowledge, documenting critical systems, having code reviews, and rotating responsibilities. 

## Overview

The Bus Factor highlights the human single point of failure in projects. In many software teams, one or two people might understand the legacy system, a crucial algorithm, or have all the deployment knowledge. If those people leave, others cannot easily pick up the work.

The concept encourages actively avoiding such dependency. Improving bus factor overlaps with knowledge management practices: pair programming, code reviews, documentation, mentorship, and rotating responsibilities.

## Examples

If a startup's only database expert is Alice, the bus factor for database knowledge is 1. If Alice quits, nobody else knows the backups, schema intricacies, or tuning.

The **Left-pad incident** reflects a bus factor of 1 for the broader ecosystem: a single maintainer pulled a tiny NPM package, and thousands of builds broke.

## The Dead Sea Effect

Bruce F. Webster coined this pattern in 2008. In dysfunctional organizations, talent vanishes while mediocrity accumulates, just like the Dead Sea where water escapes but salt remains. Skilled engineers have options and won't tolerate dysfunction for long. Those who stay are often the ones who can't easily find work elsewhere.

A team suffering from the Dead Sea Effect has knowledge concentrated in the wrong people. When these "residue" employees finally leave, the organization discovers its institutional knowledge was never institutional at all.

## Related Laws

- Conways Law
- Brooks Law
- Dunbars Number

---

Citation: "Bus Factor" from *Laws of Software Engineering* by Dr. Milan Milanović
Book: "Laws of Software Engineering" (ISBN 978-969-9893-68-1)
© 2026 Dr. Milan Milanović. Attribution required.
