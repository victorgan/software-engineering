# Circuit Breaker

> <- Back to [[Distributed System Patterns]]

A pattern that prevents cascading failures by detecting when a downstream service is failing and short-circuiting requests to it. Three states: Closed (normal), Open (failing, reject immediately), Half-Open (test with limited requests). Fails fast instead of waiting for timeouts, preserving resources.

## Key Properties

- [[Circuit States]]
- [[Failure Threshold]]
- [[Fast Failure]]

## Related

- [[Bulkhead]] (isolates failures to limit blast radius)
- [[Retry with Exponential Backoff]] (complementary pattern)

---

#distributed-systems #patterns #resilience
