# Exactly-Once Semantics

> <- Back to [[Delivery Guarantees]]

Each message is processed exactly once — no loss, no duplicates. The hardest guarantee to achieve in distributed systems. Approaches: idempotent consumers with deduplication (using message IDs), transactional outbox pattern, or Kafka's exactly-once semantics (idempotent producer + transactional consumer).

#distributed-systems #messaging
