# Message Ordering

> <- Back to [[Message Queues and Event Systems]]

Guaranteeing that messages are delivered in the order they were sent. FIFO queues preserve total order but limit throughput. Partition-level ordering (Kafka) maintains order per partition key while allowing parallel processing across partitions. True global ordering requires a single partition, limiting scalability.

## Key Properties

- [[FIFO Queues]]
- [[Partition-Level Ordering]]
- [[Ordering vs Throughput]]

## Related

- [[Delivery Guarantees]] (ordering interacts with delivery guarantees)
- [[Pub Sub]] (ordering within topic partitions)

---

#distributed-systems #messaging
