# Kernighan's Law

> Author: Dr. Milan Milanović
> Category: Quality
> Experience Level: junior

## Definition

Debugging is twice as hard as writing the code in the first place.

## Key Takeaways

1. Bug detection and removal is more complex than programming because debugging requires understanding both the code and why it doesn't work.
2. If you write code at the limit of your intelligence, you won't be able to understand or troubleshoot it later.
3. Simple code with good structure and documentation is easier to debug, saving time in the long run.
4. Even if your code runs successfully when you write it, it's fragile if it's too complex.

## Overview

Kernighan's Law says that debugging requires understanding what the code *actually* does, which can be twice as hard as writing it. When coding, you operate with a specific mental model and full context. When debugging, you might be dealing with someone else's code or your own code after that context has faded.

Writing "clever" or complex code is essentially setting a trap for your future self. A maintainable version is usually superior to an optimized version that is difficult to understand. As Kernighan implies, if you make your code too tricky, you've essentially outsmarted yourself.

## Examples

Imagine a developer writing a function in a compressed style, chaining multiple operations in one line:

<pre><code class="language-csharp">public string GetUserDisplay(User u) =>
     u?.IsActive == true ? (u.Name ?? "").Trim() is var n && n.Length > 0
     ? n + (u.Role > 0 ? $" ({(Role)u.Role})" : "") : "Unknown" : "Inactive";</code></pre>

The proper, readable version:

<pre><code class="language-csharp">public string GetUserDisplay(User user)
{
    if (user is null || !user.IsActive)
        return "Inactive";

    var name = user.Name?.Trim();

    if (string.IsNullOrEmpty(name))
        return "Unknown";

    if (user.Role > 0)
        return $"{name} ({(Role)user.Role})";

    return name;
}</code></pre>

The clever version might have taken 30 minutes to write, but debugging took 3 hours. Had the code been written clearly, it would've taken 45 minutes to write, but only 30 minutes to debug later.

## Related Laws

- Kiss Principle
- Premature Optimization

---

Citation: "Kernighan's Law" from *Laws of Software Engineering* by Dr. Milan Milanović
Book: "Laws of Software Engineering" (ISBN 978-969-9893-68-1)
© 2026 Dr. Milan Milanović. Attribution required.
