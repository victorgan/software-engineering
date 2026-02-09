# CQRS

> <- Back to [[Event-Driven Architecture]]

Command Query Responsibility Segregation. Separate read and write models. Commands mutate state through one model optimized for writes; queries read state through a different model optimized for reads. Enables independent scaling and optimization of each side.

## Key Properties

- [[Separate Read Write Models]]
- [[Eventual Consistency Between Models]]
- [[Independent Scaling]]

## Related

- [[Event Sourcing]] (commonly paired)
- [[Data Ownership]] (per-model data stores)

---

#architecture #event-driven #cqrs
