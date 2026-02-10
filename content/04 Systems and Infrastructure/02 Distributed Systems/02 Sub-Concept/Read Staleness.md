# Read Staleness

> <- Back to [[Eventual Consistency]]

Reads may return data that is not the most recent write. The degree of staleness depends on replication lag, which varies with network conditions and write volume. Applications must be designed to tolerate stale reads or use additional mechanisms (read-your-writes, quorum reads) for specific operations.

#distributed-systems #consistency
