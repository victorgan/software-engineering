# Partition-Level Ordering

> <- Back to [[Message Ordering]]

Kafka guarantees ordering within a partition but not across partitions. Messages with the same partition key (e.g., user_id) go to the same partition and are consumed in order. Different partition keys can be processed in parallel. This balances ordering guarantees with throughput.

#distributed-systems #messaging
