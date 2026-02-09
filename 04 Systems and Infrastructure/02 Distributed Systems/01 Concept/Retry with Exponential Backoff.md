# Retry with Exponential Backoff

> <- Back to [[Distributed System Patterns]]

Retrying failed operations with exponentially increasing delays (1s, 2s, 4s, 8s...) and random jitter to prevent thundering herd. Must set max retries and total timeout. Only retry on transient errors (5xx, timeouts), not permanent failures (4xx). Operations must be idempotent for safe retries.

## Key Properties

- [[Exponential Delay]]
- [[Jitter]]
- [[Idempotency Requirement]]

## Related

- [[Circuit Breaker]] (stops retrying when service is known to be down)
- [[Delivery Guarantees]] (retries provide at-least-once semantics)

---

#distributed-systems #patterns #resilience
