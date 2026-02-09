# Hybrid Logical Clocks

> <- Back to [[Distributed Time]]

Combine physical timestamps with logical counters. The physical component provides a meaningful real-time approximation; the logical component resolves ties and preserves causal ordering. Used by CockroachDB and MongoDB for transaction ordering. Simpler than vector clocks while providing both causality and time proximity.

#distributed-systems #time
