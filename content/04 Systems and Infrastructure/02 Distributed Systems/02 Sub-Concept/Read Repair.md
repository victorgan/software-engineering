# Read Repair

> <- Back to [[Leaderless Replication]]

When a read quorum returns different values from different replicas, the client detects the stale replica and sends the latest value back to it. This opportunistic repair mechanism fixes inconsistencies during normal read operations. Only repairs data that is actually read.

#distributed-systems #replication
