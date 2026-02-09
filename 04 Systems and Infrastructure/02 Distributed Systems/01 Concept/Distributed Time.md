# Distributed Time

> <- Back to [[Fundamental Concepts]]

There is no single global clock in distributed systems — each node has its own clock that can drift. Logical clocks (Lamport) establish causal ordering without physical time. Vector clocks track causality across nodes. Hybrid logical clocks combine physical and logical timestamps for both ordering and real-time approximation.

## Key Properties

- [[Lamport Clocks]]
- [[Vector Clocks]]
- [[Hybrid Logical Clocks]]

## Related

- [[Causal Consistency]] (requires tracking causal relationships)
- [[Consensus Algorithms]] (establish ordering without shared clocks)

---

#distributed-systems #fundamentals #time
