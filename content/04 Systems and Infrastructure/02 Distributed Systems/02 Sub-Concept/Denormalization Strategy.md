# Denormalization Strategy

> <- Back to [[Cross-Partition Queries]]

Duplicating data across partitions so that queries can be served from a single partition. For example, storing user data with each of their orders. Reduces read latency and eliminates cross-partition joins but increases write complexity (multiple copies must be updated) and storage.

#distributed-systems #sharding
