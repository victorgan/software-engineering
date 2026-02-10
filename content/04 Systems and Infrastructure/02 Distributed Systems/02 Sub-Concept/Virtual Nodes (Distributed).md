# Virtual Nodes (Distributed)

> <- Back to [[Consistent Hashing]]

Each physical node is represented by multiple virtual nodes (tokens) on the hash ring. This improves load distribution (more evenly spread) and enables heterogeneous hardware (more powerful nodes get more virtual nodes). Also speeds up rebalancing since data transfers come from/to multiple nodes in parallel.

#distributed-systems #sharding
