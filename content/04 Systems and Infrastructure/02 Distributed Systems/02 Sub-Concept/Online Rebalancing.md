# Online Rebalancing

> <- Back to [[Rebalancing]]

Moving data between partitions while the system continues to serve reads and writes. Requires careful coordination: the old partition continues serving requests until the new partition is ready, then traffic is switched over. Background copying with minimal impact on foreground operations.

#distributed-systems #sharding
