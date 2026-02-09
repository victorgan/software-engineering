# Minimal Redistribution

> <- Back to [[Consistent Hashing]]

When a node is added or removed, only K/N keys need to be moved (K = total keys, N = total nodes), compared to hash mod N where nearly all keys must be remapped. This makes cluster scaling operations fast and low-impact, critical for large-scale distributed systems.

#distributed-systems #sharding
