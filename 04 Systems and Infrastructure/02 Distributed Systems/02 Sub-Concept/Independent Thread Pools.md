# Independent Thread Pools

> <- Back to [[Bulkhead]]

A common bulkhead implementation where each external dependency gets its own thread pool. If calls to Service A are slow and exhaust their thread pool, requests to Service B use a separate pool and are unaffected. Hystrix (now in maintenance mode) popularized this pattern; Resilience4j is the modern alternative.

#distributed-systems #patterns #resilience
