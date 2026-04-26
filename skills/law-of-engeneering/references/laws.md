# Laws Reference

Paraphrased working checklist from https://lawsofsoftwareengineering.com/.

## Architecture

| Law | Use it to check |
| --- | --- |
| Hyrum's Law | Observable behavior can become a contract once enough users rely on it. |
| Gall's Law | Working complex systems usually evolve from working simple systems. |
| Law of Leaky Abstractions | Abstractions hide details until edge cases force those details back into view. |
| Tesler's Law | Irreducible complexity moves between system, developer, and user; it rarely disappears. |
| CAP Theorem | Under network partition, distributed data systems must choose between availability and consistency. |
| Second-System Effect | A successful first version can provoke an overbuilt replacement. |
| Fallacies of Distributed Computing | Network assumptions about latency, reliability, bandwidth, topology, and trust often fail. |
| Law of Unintended Consequences | Complex changes create side effects outside the planned path. |
| Zawinski's Law | Products tend to expand into adjacent functionality unless scope is constrained. |

## Teams

| Law | Use it to check |
| --- | --- |
| Conway's Law | System boundaries often mirror communication boundaries. |
| Brooks's Law | Adding people to late work can increase coordination cost and slow delivery. |
| Dunbar's Number | Stable coordination degrades once group size exceeds human relationship limits. |
| Ringelmann Effect | Individual contribution can shrink as group size grows. |
| Price's Law | A small subset of contributors may produce a large share of output. |
| Putt's Law | Technology leadership and management incentives can diverge. |
| Peter Principle | Promotions can move people into roles where they are no longer effective. |
| Bus Factor | Critical knowledge concentrated in few people creates continuity risk. |
| Dilbert Principle | Poor promotion incentives can move weak performers into management. |

## Planning

| Law | Use it to check |
| --- | --- |
| Premature Optimization | Optimizing before evidence can waste effort and harm design. |
| Parkinson's Law | Work can expand to fill the time allocated. |
| Ninety-Ninety Rule | The final polish and edge cases can consume disproportionate time. |
| Hofstadter's Law | Estimates remain optimistic even after accounting for optimism. |
| Goodhart's Law | A metric used as a target can stop measuring the real goal. |
| Gilb's Law | Important qualities can usually be measured better than by guesswork. |

## Quality

| Law | Use it to check |
| --- | --- |
| Boy Scout Rule | Leave touched code slightly cleaner than before. |
| Murphy's Law | If a failure path is plausible, design as if it will happen. |
| Postel's Law | Be strict in what you emit and careful about what you accept. |
| Broken Windows Theory | Visible defects invite more defects if left unrepaired. |
| Technical Debt | Shortcuts accumulate carrying cost that slows future change. |
| Linus's Law | Broader review can expose defects faster. |
| Kernighan's Law | Code that is too clever to write is harder to debug. |
| Testing Pyramid | Prefer many fast unit tests, fewer integration tests, and a small e2e layer. |
| Pesticide Paradox | Repeating the same tests finds fewer new defects over time. |
| Lehman's Laws | Useful software must evolve, and unmanaged evolution raises complexity. |
| Sturgeon's Law | Expect much output to be weak; review and filter accordingly. |

## Scale

| Law | Use it to check |
| --- | --- |
| Amdahl's Law | Parallel speedup is capped by the serial part of the system. |
| Gustafson's Law | More processors help most when the workload can grow with them. |
| Metcalfe's Law | Network value can grow rapidly with the number of connected users. |

## Design

| Law | Use it to check |
| --- | --- |
| DRY | Keep each piece of knowledge under one clear authority. |
| KISS | Prefer the simplest design that satisfies known requirements. |
| YAGNI | Do not build speculative functionality before it is needed. |
| SOLID | Use object/module boundaries that stay understandable and changeable. |
| Law of Demeter | Keep objects from reaching through strangers to do their work. |
| Principle of Least Astonishment | Interfaces should match reasonable user and developer expectations. |

## Decisions

| Law | Use it to check |
| --- | --- |
| Dunning-Kruger Effect | Low expertise can produce overconfidence; seek evidence. |
| Hanlon's Razor | Prefer ordinary error over malicious intent without evidence. |
| Occam's Razor | Prefer the simpler explanation until evidence demands complexity. |
| Sunk Cost Fallacy | Past investment does not justify continuing a bad path. |
| Map Is Not the Territory | Models, docs, and diagrams are abstractions; verify against reality. |
| Confirmation Bias | Search for disconfirming evidence, not just supporting evidence. |
| Hype Cycle and Amara's Law | Separate short-term overstatement from long-term impact. |
| Lindy Effect | Durable tools and ideas often remain useful longer. |
| First Principles Thinking | Rebuild reasoning from fundamentals when inherited assumptions are suspect. |
| Inversion | Prevent failure by reasoning backward from the unwanted outcome. |
| Pareto Principle | A minority of causes often drives most effects. |
| Cunningham's Law | Publicly wrong claims can attract corrections, but use this carefully. |
