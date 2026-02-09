# Train Wreck Anti-Pattern

> <- Back to [[Law of Demeter]]

Long chains of method calls like `a.getB().getC().getD().doSomething()`. Each dot represents a coupling to an intermediate object's structure. Violates the Law of Demeter and makes code fragile to structural changes.

#property #law-of-demeter #anti-pattern
