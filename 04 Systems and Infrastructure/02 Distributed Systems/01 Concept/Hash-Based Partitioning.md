# Hash-Based Partitioning

> <- Back to [[Partitioning and Sharding]]

Partitioning data by hashing the key, distributing data evenly across partitions. Eliminates hotspots from skewed key distributions. Loses the ability to do efficient range queries since adjacent keys are scattered. Used by Cassandra, DynamoDB, and Redis Cluster.

## Key Properties

- [[Even Distribution]]
- [[Range Query Loss]]
- [[Hash Function Choice]]

## Related

- [[Range-Based Partitioning]] (preserves range queries but risks hotspots)
- [[Consistent Hashing]] (minimizes disruption when partitions change)

---

#distributed-systems #sharding
