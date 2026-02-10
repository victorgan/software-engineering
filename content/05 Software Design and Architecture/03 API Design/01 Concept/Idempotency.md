# Idempotency

> <- Back to [[API Best Practices]]

Safe to retry. An idempotent operation produces the same result regardless of how many times it is executed. Critical for distributed systems where network failures cause retries. Idempotency keys allow clients to safely retry POST requests.

## Key Properties

- [[Idempotency Keys]]
- [[Safe Methods]]
- [[Retry Safety]]

## Related

- [[API Error Handling]] (retry on failure)

---

#api #best-practices #idempotency
