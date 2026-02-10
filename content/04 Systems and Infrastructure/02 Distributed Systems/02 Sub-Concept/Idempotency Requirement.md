# Idempotency Requirement

> <- Back to [[Retry with Exponential Backoff]]

For retries to be safe, the operation must produce the same result whether executed once or multiple times. Use idempotency keys (unique request IDs) so the server can detect and deduplicate retries. Non-idempotent operations (transfer $100) must be made idempotent (transfer $100 with txn_id=abc123).

#distributed-systems #patterns #resilience
