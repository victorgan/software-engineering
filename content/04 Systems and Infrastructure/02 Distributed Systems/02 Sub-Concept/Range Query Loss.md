# Range Query Loss

> <- Back to [[Hash-Based Partitioning]]

Since hashing destroys key ordering, range queries must be sent to all partitions (scatter-gather), which is expensive. Some systems (Cassandra) use a compound key: hash the first part for partition placement, use the second part for ordering within a partition, allowing limited range queries.

#distributed-systems #sharding
