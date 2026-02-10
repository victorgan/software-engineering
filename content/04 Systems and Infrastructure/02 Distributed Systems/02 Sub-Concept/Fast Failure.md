# Fast Failure

> <- Back to [[Circuit Breaker]]

When the circuit is open, requests fail immediately (milliseconds) instead of waiting for a timeout (seconds). This preserves thread pool resources, prevents cascading failures, and gives the failing service time to recover. Callers receive a clear error indicating the circuit is open.

#distributed-systems #patterns #resilience
