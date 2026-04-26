---
name: laws-of-software-engineering
description: Apply classic software engineering laws and decision heuristics to architecture reviews, design plans, PR reviews, refactors, estimates, team/process questions, quality strategy, scaling tradeoffs, API contracts, and risk analysis. Use when Codex needs named lenses such as Conway's Law, Hyrum's Law, YAGNI, KISS, DRY, SOLID, CAP, Goodhart's Law, Brooks's Law, the Testing Pyramid, or related laws to critique or guide software decisions.
---

# Laws of Software Engineering

Use software engineering laws as diagnostic lenses, not as rules that override repo contracts, tests, user requirements, or current evidence.

Source catalog: https://lawsofsoftwareengineering.com/

## Workflow

1. Identify the decision type: architecture, API/contract, quality, scale, planning, team/process, design, or judgment.
2. Pick 3-6 relevant laws. Avoid forcing unrelated laws into the answer.
3. For each law, state:
   - Signal: what evidence would make this law relevant.
   - Risk: what can go wrong.
   - Action: one concrete mitigation or question.
4. Resolve conflicts by current context. Example: DRY can conflict with KISS or YAGNI; prefer duplication when abstraction is still unstable.
5. End with an executable recommendation: accept, change, defer, measure, or split.

## Fast Lenses

- API/contracts: Hyrum, Postel, Principle of Least Astonishment, DRY, Law of Demeter.
- Distributed systems: CAP, Fallacies of Distributed Computing, Leaky Abstractions, Amdahl, Murphy.
- Architecture growth: Gall, Second-System Effect, YAGNI, KISS, Conway, Unintended Consequences.
- Refactoring/code quality: Boy Scout, Broken Windows, Technical Debt, SOLID, Kernighan, Testing Pyramid.
- Estimation/planning: Parkinson, Hofstadter, Ninety-Ninety, Brooks, Goodhart, Pareto.
- Team/process: Conway, Brooks, Bus Factor, Ringelmann, Price, Dunbar.
- Product/design: Least Astonishment, Tesler, Sunk Cost, Map Is Not the Territory, First Principles.
- Decision hygiene: Dunning-Kruger, Confirmation Bias, Occam, Hanlon, Inversion, Lindy.

## Output Pattern

For short answers:

```text
Relevant laws: Hyrum, YAGNI, Testing Pyramid.
Risk: clients may depend on undocumented behavior.
Action: publish the contract, add regression tests for supported behavior, leave unsupported behavior unspecified.
Decision: defer the abstraction until the second real caller appears.
```

For reviews:

```text
[Hyrum] Signal: existing consumers depend on response shape.
Risk: "internal" fields become public by accident.
Action: add contract tests and migration notes before changing payloads.
```

## Reference

Use bundled references only when they add needed precision:

- Skip references for small answers where `Fast Lenses` already gives enough direction.
- Read `references/laws.md` when the task is broad, ambiguous, or needs a category scan before choosing laws.
- Open `references/laws/<slug>.md` when using a law as a main argument and you need concrete examples, exact source framing, origins, or related laws.
- Do not load many per-law files by default. Pick the 1-3 files that match the decision after the first category scan.
