# Leader Writes

> <- Back to [[Single-Leader Replication]]

All write operations go through a single leader node, which serializes them into a total order. This eliminates write conflicts by design. The leader is a single point of failure for writes — if it goes down, a failover process must promote a replica to become the new leader.

#distributed-systems #replication
