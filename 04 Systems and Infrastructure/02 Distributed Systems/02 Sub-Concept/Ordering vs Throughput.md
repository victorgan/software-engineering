# Ordering vs Throughput

> <- Back to [[Message Ordering]]

Strict global ordering requires a single partition/queue, limiting throughput to a single consumer. Relaxing to partition-level ordering enables parallelism proportional to the number of partitions. Most applications only need ordering within an entity (per-user, per-order) rather than globally.

#distributed-systems #messaging #performance
