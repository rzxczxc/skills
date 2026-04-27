# Laws Reference

Overview table for choosing relevant laws quickly. Follow `[ref]` only when a specific law needs examples, tradeoffs, or related laws.

## Architecture

| Law | Use it to check |
| --- | --- |
| CAP Theorem | Distributed data systems must choose behavior under partition: consistency, availability, or scoped tradeoffs. [ref](laws/cap-theorem.md) |
| Fallacies of Distributed Computing | Network assumptions about latency, reliability, bandwidth, topology, and trust often fail. [ref](laws/fallacies-of-distributed-computing.md) |
| Gall's Law | Working complex systems usually evolve from working simple systems. [ref](laws/galls-law.md) |
| Hyrum's Law | Observable behavior can become a contract once enough users rely on it. [ref](laws/hyrums-law.md) |
| The Law of Leaky Abstractions | Abstractions hide details until edge cases force those details back into view. [ref](laws/law-of-leaky-abstractions.md) |
| Law of Unintended Consequences | Complex changes create side effects outside the planned path. [ref](laws/law-of-unintended-consequences.md) |
| Second-System Effect | A successful first version can provoke an overbuilt replacement. [ref](laws/second-system-effect.md) |
| Tesler's Law (Conservation of Complexity) | Irreducible complexity moves between system, developer, and user; it rarely disappears. [ref](laws/teslers-law.md) |
| Zawinski's Law | Products tend to expand into adjacent functionality unless scope is constrained. [ref](laws/zawinskis-law.md) |

## Teams

| Law | Use it to check |
| --- | --- |
| Brooks's Law | Adding people to late work can increase coordination cost and slow delivery. [ref](laws/brooks-law.md) |
| Bus Factor | Critical knowledge concentrated in few people creates continuity risk. [ref](laws/bus-factor.md) |
| Conway's Law | System boundaries often mirror communication boundaries. [ref](laws/conways-law.md) |
| Dilbert Principle | Poor promotion incentives can move weak performers into management. [ref](laws/dilbert-principle.md) |
| Dunbar's Number | Stable coordination degrades once group size exceeds human relationship limits. [ref](laws/dunbars-number.md) |
| Peter Principle | Promotions can move people into roles where they are no longer effective. [ref](laws/peter-principle.md) |
| Price's Law | A small subset of contributors may produce a large share of output. [ref](laws/prices-law.md) |
| Putt's Law | Technology leadership and management incentives can diverge. [ref](laws/putts-law.md) |
| The Ringelmann Effect | Individual contribution can shrink as group size grows. [ref](laws/ringelmann-effect.md) |

## Planning

| Law | Use it to check |
| --- | --- |
| Gilb's Law | Important qualities can usually be measured better than by guesswork. [ref](laws/gilbs-law.md) |
| Goodhart's Law | A metric used as a target can stop measuring the real goal. [ref](laws/goodharts-law.md) |
| Hofstadter's Law | Estimates remain optimistic even after accounting for optimism. [ref](laws/hofstadters-law.md) |
| The Ninety-Ninety Rule | The final polish and edge cases can consume disproportionate time. [ref](laws/ninety-ninety-rule.md) |
| Parkinson's Law | Work can expand to fill the time allocated. [ref](laws/parkinsons-law.md) |
| Premature Optimization (Knuth's Optimization Principle) | Optimizing before evidence can waste effort and harm design. [ref](laws/premature-optimization.md) |

## Quality

| Law | Use it to check |
| --- | --- |
| The Boy Scout Rule | Leave touched code slightly cleaner than before. [ref](laws/boy-scout-rule.md) |
| Broken Windows Theory | Visible defects invite more defects if left unrepaired. [ref](laws/broken-windows-theory.md) |
| Kernighan's Law | Code that is too clever to write is harder to debug. [ref](laws/kernighans-law.md) |
| Lehman's Laws of Software Evolution | Useful software must evolve, and unmanaged evolution raises complexity. [ref](laws/lehmans-laws.md) |
| Linus's Law | Broader review can expose defects faster. [ref](laws/linuss-law.md) |
| Murphy's Law / Sod's Law | If a failure path is plausible, design as if it will happen. [ref](laws/murphys-law.md) |
| Pesticide Paradox | Repeating the same tests finds fewer new defects over time. [ref](laws/pesticide-paradox.md) |
| Postel's Law | Be strict in what you emit and careful about what you accept. [ref](laws/postels-law.md) |
| Sturgeon's Law | Expect much output to be weak; review and filter accordingly. [ref](laws/sturgeons-law.md) |
| Technical Debt | Shortcuts accumulate carrying cost that slows future change. [ref](laws/technical-debt.md) |
| Testing Pyramid | Prefer many fast unit tests, fewer integration tests, and a small e2e layer. [ref](laws/testing-pyramid.md) |

## Scale

| Law | Use it to check |
| --- | --- |
| Amdahl's Law | Parallel speedup is capped by the serial part of the system. [ref](laws/amdahls-law.md) |
| Gustafson's Law | More processors help most when the workload can grow with them. [ref](laws/gustafsons-law.md) |
| Metcalfe's Law | Network value can grow rapidly with the number of connected users. [ref](laws/metcalfes-law.md) |

## Design

| Law | Use it to check |
| --- | --- |
| DRY (Don't Repeat Yourself) | Keep each piece of knowledge under one clear authority. [ref](laws/dry-principle.md) |
| KISS (Keep It Simple, Stupid) | Prefer the simplest design that satisfies known requirements. [ref](laws/kiss-principle.md) |
| Law of Demeter | Keep objects from reaching through strangers to do their work. [ref](laws/law-of-demeter.md) |
| Principle of Least Astonishment | Interfaces should match reasonable user and developer expectations. [ref](laws/principle-of-least-astonishment.md) |
| SOLID Principles | Use object and module boundaries that stay understandable and changeable. [ref](laws/solid-principles.md) |
| YAGNI (You Aren't Gonna Need It) | Do not build speculative functionality before it is needed. [ref](laws/yagni.md) |

## Decisions

| Law | Use it to check |
| --- | --- |
| Confirmation Bias | Search for disconfirming evidence, not just supporting evidence. [ref](laws/confirmation-bias.md) |
| Cunningham's Law | Publicly wrong claims can attract corrections, but use this carefully. [ref](laws/cunninghams-law.md) |
| Dunning-Kruger Effect | Low expertise can produce overconfidence; seek evidence. [ref](laws/dunning-kruger-effect.md) |
| First Principles Thinking | Rebuild reasoning from fundamentals when inherited assumptions are suspect. [ref](laws/first-principles-thinking.md) |
| Hanlon's Razor | Prefer ordinary error over malicious intent without evidence. [ref](laws/hanlons-razor.md) |
| The Hype Cycle & Amara's Law | Separate short-term overstatement from long-term impact. [ref](laws/hype-cycle-amaras-law.md) |
| Inversion | Prevent failure by reasoning backward from the unwanted outcome. [ref](laws/inversion.md) |
| The Lindy Effect | Durable tools and ideas often remain useful longer. [ref](laws/lindy-effect.md) |
| The Map Is Not the Territory | Models, docs, and diagrams are abstractions; verify against reality. [ref](laws/map-is-not-the-territory.md) |
| Occam's Razor | Prefer the simpler explanation until evidence demands complexity. [ref](laws/occams-razor.md) |
| Pareto Principle (80/20 Rule) | A minority of causes often drives most effects. [ref](laws/pareto-principle.md) |
| Sunk Cost Fallacy | Past investment does not justify continuing a bad path. [ref](laws/sunk-cost-fallacy.md) |
