# Eventual Consistency

> <- Back to [[Consistency Models]]

Given sufficient time without new updates, all replicas will converge to the same value. No guarantee about when convergence happens or what intermediate states are visible. The weakest common consistency model but enables the highest availability and lowest latency. Used by DNS, CDN caches, Cassandra, DynamoDB.

## Key Properties

- [[Convergence Guarantee]]
- [[Read Staleness]]
- [[Anti-Entropy Mechanisms]]

## Related

- [[Strong Consistency]] (opposite end of the spectrum)
- [[CRDTs]] (data structures that guarantee convergence)

---

#distributed-systems #consistency
