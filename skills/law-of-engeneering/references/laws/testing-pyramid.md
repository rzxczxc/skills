# Testing Pyramid

> Source: https://lawsofsoftwareengineering.com/laws/testing-pyramid/
> Author: Dr. Milan Milanović
> Category: Quality
> Experience Level: junior

## Definition

A project should have many fast unit tests, fewer integration tests, and only a small number of UI tests.

## Key Takeaways

1. Unit testing is where you start. Unit tests are run as separate functions and execute quickly. That means you can afford to write lots of unit tests.
2. After the unit tests, there must be an integration test layer. These verify the integration of modules. You will require fewer integration tests than unit tests.
3. End-to-end tests at the top simulate real-world user scenarios. They are essential but slow and expensive to maintain.
4. Organizing tests this way, you receive quick feedback (most tests are quick unit tests), and when your UI test fails, there’s a better chance it’s due to a real problem


## Overview

The pyramid is a visual metaphor: the largest level (at the bottom) is unit tests, which are fast and the most numerous. The middle layer is integration tests, fewer in number. The top is UI/end-to-end tests, the least numerous. As you go up, tests become more expensive in time, effort, and fragility, so you want proportionally fewer of them.

By following the pyramid, most bugs are caught at the cheapest level. If the pyramid is inverted (lots of end-to-end tests, few unit tests), the test suite tends to be slow and fragile.



## Examples

Consider a web e-commerce application. Following the test pyramid, the team writes extensive unit tests for functions such as price calculation, discount logic, and validation (hundreds of unit tests). They also write API integration tests verifying that order placement connects inventory, payment, and notification services correctly (a few dozen tests). Finally, they have a few end-to-end tests simulating user journeys like browsing, adding to cart, and checkout.

Because they have so many unit tests, if something in business logic breaks, it's caught before end-to-end tests run. This approach takes little time in CI and allows confident deployments.

Now consider a team that did not follow the pyramid. They have few unit tests and instead rely on 50 end-to-end GUI tests that run nightly for hours. They often find failing tests, but it's hard to tell if it's genuine bugs or test flakiness. Developers get feedback with a day's delay. This is the *anti-pattern* the pyramid warns against.



## Origins

Mike Cohn is credited with popularizing the Test Pyramid. He described it in his book *Succeeding with Agile* and blog posts around 2009, coining the term and concept.

The idea builds on earlier testing theory (such as test levels in the ISTQB foundation or the general practice in TDD of writing many unit tests). Modern discussions sometimes add layers or modify terms, but the core principle remains: **test more at the unit level than at the UI level**.



## The Beyoncé Rule

The Beyoncé Rule states: "If you liked it, you should put a test on it." At Google, if infrastructure teams land a change that passes your tests but breaks your product, the missing tests are your responsibility. Your test suite is your contract with the world; the absence of a test is a silent permission slip to ship broken.



## Related Laws

- Lehmans Laws


## Further Reading

- [The Practical Test Pyramid](https://martinfowler.com/articles/practical-test-pyramid.html) — Martin Fowler's comprehensive guide to the test pyramid
- [Succeeding with Agile](https://amzn.to/4pb7Q8v) — Mike Cohn's book where the Test Pyramid was popularized
- [Test Pyramid - Wikipedia](https://en.wikipedia.org/wiki/Test_automation#Testing_at_different_levels) — Overview of test automation at different levels
- [Software Engineering at Google, Chapter 11: Testing Overview](https://abseil.io/resources/swe-book/html/ch11.html) — Titus Winters, Tom Manshreck & Hyrum Wright on Google's testing philosophy and practices

---

Citation: "Testing Pyramid" from *Laws of Software Engineering* by Dr. Milan Milanović
Canonical URL: https://lawsofsoftwareengineering.com/laws/testing-pyramid/
Book: "Laws of Software Engineering" (ISBN 978-969-9893-68-1) — https://lawsofsoftwareengineering.com/book/
© 2026 Dr. Milan Milanović. Attribution required.
