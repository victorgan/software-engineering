# At-Most-Once

> <- Back to [[Delivery Guarantees]]

Messages are delivered zero or one times. No retries — if delivery fails, the message is lost. Simplest to implement and lowest latency. Appropriate when occasional message loss is acceptable (metrics, logging, non-critical notifications).

#distributed-systems #messaging
