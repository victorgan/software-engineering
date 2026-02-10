# Multi-Leader Replication

> <- Back to [[Replication]]

Multiple nodes accept writes independently and replicate to each other. Enables write availability in multiple regions but introduces write conflicts when different leaders modify the same data. Conflict resolution strategies include last-writer-wins, merge functions, and CRDTs.

## Key Properties

- [[Multiple Writers]]
- [[Conflict Resolution]]
- [[Cross-Region Writes]]

## Related

- [[Single-Leader Replication]] (simpler, no conflicts)
- [[CRDTs]] (conflict-free approach to multi-writer systems)

---

#distributed-systems #replication
