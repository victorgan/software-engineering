# Aggregates

> <- Back to [[Tactical Design]]

A cluster of entities and value objects with a root entity that serves as the entry point. The aggregate root enforces invariants across the cluster. External objects can only reference the aggregate root, not internal entities. The aggregate is the consistency boundary.

## Key Properties

- [[Aggregate Root]]
- [[Consistency Boundary]]
- [[Transactional Boundary]]

## Related

- [[Entities]] (composing the aggregate)
- [[Value Objects]] (composing the aggregate)
- [[DDD Repositories]] (persist aggregates)

---

#ddd #aggregates
