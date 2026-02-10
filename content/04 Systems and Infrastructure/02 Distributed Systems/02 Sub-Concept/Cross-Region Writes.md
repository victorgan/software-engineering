# Cross-Region Writes

> <- Back to [[Multi-Leader Replication]]

Multi-leader replication enables each region to have its own leader, accepting writes locally with low latency. Changes are replicated asynchronously across regions. Critical for global applications where users need write access from any region without cross-region round trips for every write.

#distributed-systems #replication
