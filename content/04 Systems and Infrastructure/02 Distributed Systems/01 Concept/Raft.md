# Raft

> <- Back to [[Consensus Algorithms]]

A consensus algorithm designed for understandability. Separates consensus into leader election, log replication, and safety. A leader is elected to manage the replicated log; followers replicate the leader's log. Used in production by etcd (Kubernetes), CockroachDB, Consul, and TiKV.

## Key Properties

- [[Leader Election Raft]]
- [[Log Replication]]
- [[Safety Guarantees]]

## Related

- [[Paxos]] (equivalent capability, harder to understand)
- [[Leader Election]] (Raft includes built-in leader election)

---

#distributed-systems #consensus
