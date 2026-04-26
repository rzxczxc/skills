# Murphy's Law / Sod's Law

> Source: https://lawsofsoftwareengineering.com/laws/murphys-law/
> Author: Dr. Milan Milanović
> Category: Quality
> Experience Level: junior

## Definition

Anything that can go wrong will go wrong.

## Key Takeaways

1. If an error can happen, it will happen. Plan and code defensively with this in mind.
2. Add error handling, backups, and checks.
3. Edge cases will occur in production. Write tests for these kinds of scenarios.


## Overview

In software, Murphy's Law is often used to explain bugs and production incidents: whatever can go wrong in code (a null pointer, a race condition, a network outage) eventually will manifest, especially in large user bases or at the worst possible time.

In practice, this law encourages developers to write more defensive code. This means checking for nulls, handling exceptions, validating inputs, and failing gracefully when errors occur. It also reminds DevOps teams to anticipate failures by implementing monitoring, enabling rollbacks, and maintaining contingency plans.



## Examples

If a web form field can accept text, someone will enter a 10,000-character string of weird symbols to see what happens, unless you've explicitly handled it. If memory can run out, it will be when multiple processes align just so. 

A famous real-world instance was during a live demo (who remembers the Windows 98 presentation by Bill Gates?), if something can glitch, it likely will.

In coding, consider a function that assumes an input file exists. Murphy's Law says that one day that file won't be there or will be corrupted, so your code should handle the file-not-found or bad-data scenario rather than crash. 

Another typical case is that the server will crash on your only day off, because that's when it's most likely to cause trouble. Engineers thus build highly available systems and pager rotations to mitigate Murphy's Law.



## Origins

Attributed to Edward A. Murphy Jr., an engineer working on rocket sled experiments in 1949. It became popular in aerospace and then everywhere. In software, it's been around as long as bugs have, constantly reminding us that if there's one untested scenario, one user will find it.



## Sod's Law

In British English, the same principle may be referred to using the term “Sod’s Law”. It carries a similar meaning, although it may also reflect the element of spite, as the universe is somehow interfering in your endeavors. 

Both versions may be used interchangeably in Software Engineering to highlight the significance of defensive programming.



## Related Laws

- Confirmation Bias


## Further Reading

- [Murphy's Law - Wikipedia](https://en.wikipedia.org/wiki/Murphy%27s_law) — History and variations of the famous adage
- [Windows 98 Crash During Live Demo](https://www.youtube.com/watch?v=yeUyxjLhAxU) — Bill Gates' infamous BSOD during a Windows 98 presentation
- [Defensive Programming](https://en.wikipedia.org/wiki/Defensive_programming) — Programming practices to anticipate and handle errors
- [CrowdStrike Channel File 291 RCA Exec Summary](https://www.crowdstrike.com/falcon-content-update-remediation-and-guidance-hub/) — Root cause analysis of the CrowdStrike outage, a real-world example of Murphy's Law at scale

---

Citation: "Murphy's Law / Sod's Law" from *Laws of Software Engineering* by Dr. Milan Milanović
Canonical URL: https://lawsofsoftwareengineering.com/laws/murphys-law/
Book: "Laws of Software Engineering" (ISBN 978-969-9893-68-1) — https://lawsofsoftwareengineering.com/book/
© 2026 Dr. Milan Milanović. Attribution required.
