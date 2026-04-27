# Postel's Law

> Author: Dr. Milan Milanović
> Category: Quality
> Experience Level: mid

## Definition

Be conservative in what you do, be liberal in what you accept from others.

## Key Takeaways

1. When your system emits data or interacts with the outside world, adhere closely to protocols and standards.
2. When receiving data, handle variations, minor errors, or deviations where possible. Don't crash or reject communication over minor issues.
3. In modern times, overly liberal acceptance can sometimes mask errors, so this law is occasionally tempered with security considerations.

## Overview

This law says that if your server sends HTTP responses, it should format headers exactly per spec. But if your server receives an HTTP request with an uncommon header order or an unusual format, you should still process it rather than drop the connection, as long as you can interpret it safely. 

This principle contributed to the Internet's resilience, meaning that different implementations can communicate because each side strives to be compatible.

In software in general, think of file readers: a robust one can open not-quite-perfect files (e.g., a tolerant XML parser might recover from a minor error), whereas a strict one might refuse. Postel's Law would encourage the former. However, it has caveats. Being too liberal can allow sloppy producers to proliferate, and in security contexts, accepting malformed input can be risky. Some argue that overly tolerant software can cause long-term interoperability problems because producers never fix their bugs if everyone tolerates them.

## Examples

In **web browsers**, HTML on websites is often malformed. Browsers, following Postel's spirit, perform extensive error correction and forgiving parsing. They'll still render the page even if a tag isn't closed correctly. If browsers were strict, half the web pages might not display.

In **APIs**, say your service expects a timestamp. If it receives a timestamp without a time zone, instead of rejecting, maybe you assume UTC or try to parse it anyway, being liberal in acceptance. But when your service returns data, you always include the time zone to be conservative and precise in output. 

An **email client** that receives a slightly non-conforming email (missing a MIME boundary or incorrect newline encodings) will still attempt to show the email rather than throwing an error.

## Related Laws

- Hyrums Law
- Law of Leaky Abstractions
- Fallacies of Distributed Computing

---

Citation: "Postel's Law" from *Laws of Software Engineering* by Dr. Milan Milanović
Book: "Laws of Software Engineering" (ISBN 978-969-9893-68-1)
© 2026 Dr. Milan Milanović. Attribution required.
