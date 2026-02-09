# Partition Splitting

> <- Back to [[Rebalancing]]

When a partition grows too large or becomes a hotspot, it is split into two smaller partitions. HBase and BigTable use this approach with range-based partitioning. The system monitors partition size and access patterns to trigger splits automatically. Merging combines underutilized partitions.

#distributed-systems #sharding
