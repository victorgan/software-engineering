# Scatter-Gather

> <- Back to [[Cross-Partition Queries]]

A query pattern where the request is sent to all (or multiple) partitions in parallel, each partition executes the query locally, and results are gathered and merged by a coordinator. Latency is determined by the slowest partition. Common for aggregations and searches across partitioned data.

#distributed-systems #sharding
