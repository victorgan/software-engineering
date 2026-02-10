# Dead Letter Queues

> <- Back to [[Message Queues and Event Systems]]

A separate queue where messages that cannot be processed after a configured number of attempts are sent. Prevents poison messages (malformed or unprocessable) from blocking the main queue. Enables manual inspection, alerting, and reprocessing after the underlying issue is fixed.

## Key Properties

- [[Failed Message Handling]]
- [[Retry Policies]]
- [[Message Inspection]]

## Related

- [[Delivery Guarantees]] (DLQ is part of at-least-once delivery)
- [[Circuit Breaker]] (similar failure handling at the service level)

---

#distributed-systems #messaging
