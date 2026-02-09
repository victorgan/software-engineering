# Multiple Writers

> <- Back to [[Multi-Leader Replication]]

Each leader independently accepts writes for any key, unlike single-leader where one node handles all writes. This provides lower write latency (write to the nearest leader) and higher write availability (no single point of failure). However, concurrent writes to the same key create conflicts that must be resolved.

#distributed-systems #replication
