# Sync vs Async Decision

> <- Back to [[When to Choose What]]

Choose sync (HTTP/gRPC) when low latency is needed, for simple request-response, and when strong consistency is required. Choose async (queues/events) for decoupled services, eventual consistency, spike traffic handling, and long-running tasks.

## Key Properties

- [[Latency Requirements]]
- [[Consistency Requirements]]
- [[Traffic Pattern Factor]]

## Related

- [[Inter-Service Communication]] (implementation)

---

#tradeoffs #decision #sync #async
