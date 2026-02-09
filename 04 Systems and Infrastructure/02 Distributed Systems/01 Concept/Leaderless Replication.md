# Leaderless Replication

> <- Back to [[Replication]]

Any node can accept reads and writes. Consistency is achieved through quorum reads/writes (R + W > N). Read repair and anti-entropy processes resolve divergence. Dynamo-style systems: Cassandra, Riak, DynamoDB. Provides high availability (no single point of failure) at the cost of complexity.

## Key Properties

- [[Quorum Reads and Writes]]
- [[Read Repair]]
- [[Anti-Entropy]]

## Related

- [[Single-Leader Replication]] (simpler but with single point of failure for writes)
- [[Consistent Hashing]] (often used for data placement in leaderless systems)

---

#distributed-systems #replication
