# Majority Agreement

> <- Back to [[Paxos]]

A value is chosen when a majority (more than half) of acceptors have accepted it. Since any two majorities overlap by at least one member, this ensures that once a value is chosen, it cannot be overwritten. With 2f+1 nodes, the system tolerates f failures.

#distributed-systems #consensus
