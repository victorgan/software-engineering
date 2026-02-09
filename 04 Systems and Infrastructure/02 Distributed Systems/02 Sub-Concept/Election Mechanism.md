# Election Mechanism

> <- Back to [[Leader Election]]

How a leader is chosen: using a consensus service (create an ephemeral node in ZooKeeper, the first creator is the leader), Raft's built-in election (randomized timeouts and majority votes), or database-based (acquire a lock row). The mechanism must handle network partitions to prevent split-brain (two leaders).

#distributed-systems #patterns
