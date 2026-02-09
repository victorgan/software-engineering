# Anti-Entropy

> <- Back to [[Leaderless Replication]]

Background processes that compare data between replicas and fix inconsistencies. Uses Merkle trees to efficiently identify differing data ranges without comparing every record. Complements read repair by fixing data that has not been recently read. Runs continuously to drive convergence.

#distributed-systems #replication
