# Circuit Breakers

> <- Back to [[Reliability Patterns]]

A pattern that stops calling a failing downstream service to prevent cascading failures. Like an electrical circuit breaker, it trips open after detecting failures, periodically allows test requests (half-open state), and closes when the service recovers. See also [[Distributed Systems]].

## Key Properties

- [[Circuit States (Closed, Open, Half-Open)]]
- [[Failure Threshold Configuration]]
- [[Recovery Detection]]

---

#sre #reliability #circuit-breaker
