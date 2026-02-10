# At-Least-Once

> <- Back to [[Delivery Guarantees]]

Messages are delivered one or more times. The system retries until the consumer acknowledges. May result in duplicate delivery if the acknowledgment is lost after processing. The most common guarantee in production systems. Consumers must be idempotent to handle duplicates safely.

#distributed-systems #messaging
