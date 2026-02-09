# Leader Election

> <- Back to [[Distributed System Patterns]]

A pattern for choosing one node among many to serve as the coordinator/leader for a task. The leader handles writes, coordination, or scheduling while followers serve reads or act as standby. Implemented using consensus services (ZooKeeper, etcd) or built-in to consensus algorithms (Raft).

## Key Properties

- [[Election Mechanism]]
- [[Leader Lease]]
- [[Failover]]

## Related

- [[Raft]] (includes built-in leader election)
- [[Single-Leader Replication]] (uses leader election for failover)

---

#distributed-systems #patterns
