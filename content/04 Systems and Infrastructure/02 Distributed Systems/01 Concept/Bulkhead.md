# Bulkhead

> <- Back to [[Distributed System Patterns]]

Isolating components so that a failure in one does not cascade to others, like watertight compartments in a ship. Implementation: separate thread pools, connection pools, or process groups for different dependencies. If one dependency slows down, only its dedicated resources are affected.

## Key Properties

- [[Resource Isolation]]
- [[Blast Radius Limitation]]
- [[Independent Thread Pools]]

## Related

- [[Circuit Breaker]] (detects failures; bulkhead contains them)
- [[Sidecar Pattern]] (sidecars can implement bulkhead logic)

---

#distributed-systems #patterns #resilience
