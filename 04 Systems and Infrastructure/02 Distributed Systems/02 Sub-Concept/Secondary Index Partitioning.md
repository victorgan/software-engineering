# Secondary Index Partitioning

> <- Back to [[Cross-Partition Queries]]

Two approaches: local indexes (each partition indexes only its own data — reads require scatter-gather) and global indexes (the index itself is partitioned differently from the data — writes must update multiple partitions). Local indexes are simpler for writes; global indexes are faster for reads.

#distributed-systems #sharding
