# CRDTs

> <- Back to [[Replication]]

Conflict-Free Replicated Data Types — data structures that can be replicated across nodes and merged without coordination, always converging to the same state. Examples: G-Counter (grow-only counter), PN-Counter, G-Set, OR-Set (observed-remove set), LWW-Register. Used in collaborative editing and offline-first applications.

## Key Properties

- [[G-Counter and PN-Counter]]
- [[OR-Set]]
- [[Automatic Merge]]

## Related

- [[Multi-Leader Replication]] (CRDTs eliminate conflict resolution need)
- [[Eventual Consistency]] (CRDTs guarantee convergence)

---

#distributed-systems #replication #crdts
