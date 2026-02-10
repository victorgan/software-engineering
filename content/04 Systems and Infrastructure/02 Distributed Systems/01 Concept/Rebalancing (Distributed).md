# Rebalancing (Distributed)

> <- Back to [[Partitioning and Sharding]]

The process of moving data between partitions when nodes are added, removed, or when data distribution becomes skewed. Must happen without downtime. Strategies include fixed partition count (Cassandra), dynamic splitting/merging (HBase), and consistent hashing with virtual nodes.

## Key Properties

- [[Online Rebalancing]]
- [[Data Migration]]
- [[Partition Splitting]]

## Related

- [[Consistent Hashing]] (minimizes data movement during rebalancing)
- [[Range-Based Partitioning]] (splits hot ranges)

---

#distributed-systems #sharding
