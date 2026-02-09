# Failure Modes Review

> <- Back to [[Design Review Checklist]]

What happens when each dependency fails? Is there graceful degradation? Consider circuit breakers, fallbacks, retries with backoff, and blast radius containment. Every external dependency is a potential failure point.

## Key Properties

- [[Graceful Degradation]]
- [[Blast Radius]]
- [[Recovery Mechanisms]]

---

#tradeoffs #design-review #failure-modes
