# CQRS with DDD

> <- Back to [[DDD in Practice]]

Separate command and query models aligned with aggregates. Commands go through the domain model (aggregates enforce invariants), while queries bypass the domain model and read from optimized views. Enables complex domain logic without compromising read performance.

## Key Properties

- [[Command Through Domain Model]]
- [[Query Bypass]]
- [[Aggregate Alignment]]

## Related

- [[CQRS]] (architectural pattern)
- [[Aggregates]] (command-side consistency)

---

#ddd #cqrs
