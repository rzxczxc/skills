# Confirmation Bias

> Source: https://lawsofsoftwareengineering.com/laws/confirmation-bias/
> Author: Dr. Milan Milanović
> Category: Decisions
> Experience Level: mid

## Definition

A tendency to favor information that supports our existing beliefs or ideas.

## Key Takeaways

1. When reviewing code or debugging, notice if you're only looking for evidence that supports your initial hunch.
2. Challenge yourself when actively thinking about problems. If you have an opinion about an issue, try to ask, “What would I expect to see if I’m wrong?” In this, we can counteract our natural bias only to confirm.
3. Regarding team decision-making (for example, tech stacks and/or design decisions), seek input from people with differing opinions. Bias confirmation can be overcome by looking into alternative solutions. For example, if the whole team “feels” that technology X is the superior choice, assign someone to look into the opposing view on technology X.
4. Base decision-making on objective criteria (facts, not opinions). Automated tests, performance criteria, and experimentation (A/B tests) can provide truths regardless of human bias.


## Overview

We all like to be right. Confirmation bias is our mind's way of cheating to feel right more often. Psychologically, once we form an opinion, we subconsciously filter information, noticing bits that support our view and ignoring those that contradict it.

In software, a typical scenario is debugging. A developer convinced that module A caused a production issue will comb through module A's code intensively. If module B (assumed to be fine) is also throwing errors, they might not even look there, missing the real cause. Awareness of this bias leads to asking "What am I missing? Maybe there is another explanation?" and encouraging environments where beliefs are constructively questioned.



## Examples

In code reviews, a reviewer who trusts a colleague's skills might skim over potential issues, assuming the code is probably fine. Or the opposite: a reviewer expecting sloppy code from a junior developer might find "issues" that aren't really important.

Confirmation bias also affects testing. A developer may write unit tests that assert the code works on typical inputs (happy path), but might not try edge cases that could break it. Teams combat this through code reviews with fresh eyes, writing tests specifically aimed at breaking their own code, and post-mortems asking "What went wrong and why didn't we see it?"

By checking for confirmation bias, engineers can become better at solving problems with an open and critical mind.



## Origins

One of the first to identify confirmation bias was Peter Cathcart Wason, an English cognitive psychologist. In 1960, he conducted a famous experiment (Wason's rule discovery task) where participants had to guess a rule for a sequence of numbers. He found people tended to test sequences that would confirm their initial thoughts rather than those that could prove them wrong.

Wason coined the term "confirmation bias" to explain this phenomenon. Since then, countless studies have confirmed the existence of confirmation bias in human reasoning.




## Related Laws

- Dunning Kruger Effect
- Hanlons Razor
- Goodharts Law


## Further Reading

- [Confirmation Bias: A Ubiquitous Phenomenon in Many Guises](https://journals.sagepub.com/doi/10.1037/1089-2680.2.2.175) — Raymond Nickerson's comprehensive 1998 review of confirmation bias research
- [On the Failure to Eliminate Hypotheses in a Conceptual Task](https://www.tandfonline.com/doi/abs/10.1080/17470216008416717) — Peter Wason's 1960 foundational paper on the rule discovery task
- [Thinking, Fast and Slow](https://amzn.to/48WboH0) — Daniel Kahneman's exploration of cognitive biases including confirmation bias

---

Citation: "Confirmation Bias" from *Laws of Software Engineering* by Dr. Milan Milanović
Canonical URL: https://lawsofsoftwareengineering.com/laws/confirmation-bias/
Book: "Laws of Software Engineering" (ISBN 978-969-9893-68-1) — https://lawsofsoftwareengineering.com/book/
© 2026 Dr. Milan Milanović. Attribution required.
