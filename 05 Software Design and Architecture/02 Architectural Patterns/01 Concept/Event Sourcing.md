# Event Sourcing

> <- Back to [[Event-Driven Architecture]]

Store events, derive state, complete audit trail. Instead of storing current state, store the sequence of events that led to the current state. State is reconstructed by replaying events. Provides a complete audit log and enables temporal queries.

## Key Properties

- [[Event Store]]
- [[State Reconstruction]]
- [[Temporal Queries]]

## Related

- [[CQRS]] (commonly paired with event sourcing)
- [[Domain Events]] (the events being stored)

---

#architecture #event-driven #event-sourcing
