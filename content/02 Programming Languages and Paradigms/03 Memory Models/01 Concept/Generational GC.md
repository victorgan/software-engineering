# Generational GC

> <- Back to [[Garbage Collection (GC)]]

A GC strategy based on the generational hypothesis: most objects die young. Memory is divided into young and old generations with separate collection frequencies. Minor collections (young gen) are fast and frequent; major collections (old gen) are thorough but rare.

## Key Properties

- [[Young and Old Generations]]
- [[Minor and Major Collections]]

## Related

- Used by JVM, .NET

---

#memory-models #gc #generational
