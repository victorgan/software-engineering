# Latency vs Consistency

> <- Back to [[PACELC Theorem]]

The "ELC" part: even when the network is healthy, stronger consistency requires more coordination between nodes (quorum writes, synchronous replication), increasing latency. Weaker consistency allows faster responses by reading from local replicas without waiting for global agreement.

#distributed-systems #fundamentals #performance
