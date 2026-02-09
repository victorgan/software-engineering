# Hash Function Choice

> <- Back to [[Hash-Based Partitioning]]

The hash function must distribute uniformly but does not need to be cryptographically secure. MurmurHash, xxHash, and FNV are common choices. Consistency across all nodes is critical — all nodes must use the same hash function. The partition is typically hash(key) mod N or a consistent hashing ring.

#distributed-systems #sharding
