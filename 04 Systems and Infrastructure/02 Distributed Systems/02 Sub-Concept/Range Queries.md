# Range Queries

> <- Back to [[Range-Based Partitioning]]

Range-based partitioning keeps adjacent keys on the same partition, enabling efficient range scans (e.g., all orders from January). A single partition can serve the entire range without scatter-gather. This is the primary advantage over hash-based partitioning.

#distributed-systems #sharding
