# Quorum Reads and Writes

> <- Back to [[Leaderless Replication]]

Writes go to W nodes and reads query R nodes, where W + R > N (total replicas). This guarantees at least one node in the read set has the latest write. Common configuration: N=3, W=2, R=2. Tunable consistency: W=1,R=N for fast writes; W=N,R=1 for fast reads.

#distributed-systems #replication
