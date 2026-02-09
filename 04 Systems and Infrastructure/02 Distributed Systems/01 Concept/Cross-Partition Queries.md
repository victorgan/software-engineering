# Cross-Partition Queries

> <- Back to [[Partitioning and Sharding]]

Queries that need data from multiple partitions. Scatter-gather sends the query to all relevant partitions and merges results. Denormalization duplicates data to avoid cross-partition queries. Secondary indexes can be local (partition-scoped) or global (requiring scatter-gather).

## Key Properties

- [[Scatter-Gather]]
- [[Denormalization Strategy]]
- [[Secondary Index Partitioning]]

## Related

- [[Range-Based Partitioning]] (range queries may be single-partition)
- [[Hash-Based Partitioning]] (most range queries become cross-partition)

---

#distributed-systems #sharding
