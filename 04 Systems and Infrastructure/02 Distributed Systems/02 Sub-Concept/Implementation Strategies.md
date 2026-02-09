# Implementation Strategies

> <- Back to [[Read-Your-Writes]]

Several approaches: (1) route reads to the replica that accepted the write (session affinity), (2) track the write timestamp and only read from replicas that are up-to-date, (3) read from the leader/primary after a write, (4) use quorum reads. Each approach has different performance and availability characteristics.

#distributed-systems #consistency
