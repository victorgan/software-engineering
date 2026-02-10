# Single-Leader Replication

> <- Back to [[Replication]]

One node (the leader/primary) accepts all writes and replicates them to read replicas (followers). Writes are serialized through the leader, ensuring consistency. Read replicas provide read scalability. Replication can be synchronous (strong consistency, higher latency) or asynchronous (risk of data loss on leader failure).

## Key Properties

- [[Leader Writes]]
- [[Read Replicas]]
- [[Replication Lag]]

## Related

- [[Multi-Leader Replication]] (allows writes on multiple nodes)
- [[Leaderless Replication]] (no designated leader)

---

#distributed-systems #replication
