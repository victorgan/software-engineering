# Quorum Operations

> <- Back to [[Strong Consistency]]

Requiring a majority of nodes to acknowledge writes (W) and reads (R) where W + R > N (total replicas). This ensures reads always see the latest write. For example, with 3 replicas, writing to 2 and reading from 2 guarantees overlap. Quorum operations add latency proportional to the slowest node in the quorum.

#distributed-systems #consistency
