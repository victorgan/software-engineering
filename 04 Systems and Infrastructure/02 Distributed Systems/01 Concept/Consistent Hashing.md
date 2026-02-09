# Consistent Hashing

> <- Back to [[Partitioning and Sharding]]

A hash-based partitioning scheme where adding or removing a node only requires remapping 1/n of the keys (minimal redistribution). Keys and nodes are placed on a hash ring; each key is assigned to the next node clockwise. Virtual nodes improve balance. Used by Cassandra, DynamoDB, and CDNs.

## Key Properties

- [[Hash Ring]]
- [[Minimal Redistribution]]
- [[Virtual Nodes]]

## Related

- [[Hash-Based Partitioning]] (consistent hashing is an improvement)
- [[Rebalancing]] (consistent hashing minimizes rebalancing work)

---

#distributed-systems #sharding
