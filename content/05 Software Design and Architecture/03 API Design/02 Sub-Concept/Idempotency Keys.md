# Idempotency Keys

> <- Back to [[Idempotency]]

A unique key sent by the client with each request. The server stores the result of the first execution and returns the same result for subsequent requests with the same key. Commonly used with payment APIs and other non-idempotent operations.

#property #idempotency #idempotency-keys
