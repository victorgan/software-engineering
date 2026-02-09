# Retries with Backoff

> <- Back to [[Reliability Patterns]]

Automatically retrying failed requests with exponential backoff and jitter to avoid thundering herd problems. Retries require idempotent operations to be safe. Without backoff and jitter, retries can amplify load on an already struggling service.

## Key Properties

- [[Exponential Backoff]]
- [[Jitter]]
- [[Idempotency Requirement]]

---

#sre #reliability #retries
