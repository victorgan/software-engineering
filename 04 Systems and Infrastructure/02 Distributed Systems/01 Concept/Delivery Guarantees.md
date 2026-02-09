# Delivery Guarantees

> <- Back to [[Message Queues and Event Systems]]

Three levels: at-most-once (fire and forget, no retries), at-least-once (retry until acknowledged, may duplicate), and exactly-once (the hardest — requires idempotent consumers or transactional processing). Most systems provide at-least-once and rely on consumer idempotency for effective exactly-once behavior.

## Key Properties

- [[At-Most-Once]]
- [[At-Least-Once]]
- [[Exactly-Once Semantics]]

## Related

- [[Dead Letter Queues]] (handling messages that repeatedly fail)
- [[Retry with Exponential Backoff]] (retry strategy for at-least-once)

---

#distributed-systems #messaging
