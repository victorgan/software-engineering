# Zab

> <- Back to [[Consensus Algorithms]]

ZooKeeper Atomic Broadcast — the consensus protocol used by Apache ZooKeeper. Designed specifically for primary-backup replication with total order broadcast. Ensures all state changes are delivered in the same order to all replicas. Simpler than Paxos for the leader-based replication use case.

## Key Properties

- [[Atomic Broadcast]]
- [[Primary-Backup Model]]
- [[Total Order Delivery]]

## Related

- [[Raft]] (similar leader-based approach)
- [[Leader Election]] (Zab includes leader election)

---

#distributed-systems #consensus
