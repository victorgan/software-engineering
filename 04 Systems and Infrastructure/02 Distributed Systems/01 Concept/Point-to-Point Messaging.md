# Point-to-Point Messaging

> <- Back to [[Message Queues and Event Systems]]

One producer sends a message that is consumed by exactly one consumer. Messages are removed from the queue after consumption. Provides load balancing across consumers (work queue pattern). Examples include SQS and RabbitMQ work queues. Ideal for task distribution.

## Key Properties

- [[Single Consumer Delivery]]
- [[Work Queue Pattern]]
- [[Message Acknowledgment]]

## Related

- [[Pub Sub]] (one-to-many alternative)
- [[Dead Letter Queues]] (handling failed messages)

---

#distributed-systems #messaging
