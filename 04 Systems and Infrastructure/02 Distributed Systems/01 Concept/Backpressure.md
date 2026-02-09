# Backpressure

> <- Back to [[Message Queues and Event Systems]]

A mechanism for slow consumers to signal producers to reduce the sending rate. Without backpressure, fast producers overwhelm slow consumers, causing message queues to grow unbounded, leading to memory exhaustion or message loss. Strategies include blocking producers, dropping messages, or buffering with limits.

## Key Properties

- [[Flow Control Messaging]]
- [[Consumer Rate Limiting]]
- [[Buffer Management]]

## Related

- [[Flow Control]] (TCP-level backpressure)
- [[Circuit Breaker]] (stops requests to overwhelmed services)

---

#distributed-systems #messaging
